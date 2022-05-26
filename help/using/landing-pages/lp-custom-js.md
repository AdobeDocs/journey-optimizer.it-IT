---
title: Utilizzare JavaScript personalizzato in una pagina di destinazione
description: Scopri come progettare il contenuto di una pagina di destinazione in Journey Optimizer
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
source-git-commit: f4b3a9de47e724f7b23df8a02b8106c131cf1b12
workflow-type: tm+mt
source-wordcount: '558'
ht-degree: 2%

---

# Utilizzare JavaScript personalizzato in una pagina di destinazione {#lp-custom-js}

Puoi definire il contenuto della pagina di destinazione utilizzando JavaScript personalizzato. Ad esempio, se devi eseguire uno stile avanzato o se desideri aggiungere comportamenti personalizzati alle pagine di destinazione, puoi creare controlli personalizzati ed eseguirli in [!DNL Journey Optimizer].

## Inserire codice JavaScript in una pagina di destinazione

Per inserire JavaScript personalizzato nel contenuto della pagina di destinazione, puoi effettuare una delle seguenti operazioni:

* Importa il contenuto esistente di HTML quando inizi a creare il contenuto, quindi seleziona il file che include il codice JavaScript personalizzato. Scopri come importare il contenuto [in questa sezione](../design/existing-content.md).

* Progetta la pagina di destinazione da zero o da un modello salvato. Trascina e rilascia la **[!UICONTROL HTML]** componente contenuto nell’area di lavoro e mostra il codice sorgente per aggiungere JavaSCript al componente. Scopri come utilizzare il componente HTML in [questa sezione](../design/content-components.md#HTML). <!--You can also simply switch the whole landing page content to code view and enter or paste your JavaScript code.-->

   ![](assets/lp_designer-html-component.png)

* Immetti o incolla il codice JavaScript direttamente nella finestra di progettazione dei contenuti. Scopri come codificare i contenuti personalizzati [in questa sezione](../design/code-content.md).

>[!NOTE]
>
>Attualmente non è possibile visualizzare JavaScript in azione quando [visualizzazione dell’anteprima della pagina di destinazione](create-lp.md#test-landing-page).

Affinché la pagina di destinazione sia visualizzata correttamente, utilizza la sintassi seguente come descritto nelle sezioni seguenti.

## Inizializzazione del codice

Per inizializzare il codice JavaScript, è necessario utilizzare il `lpRuntimeReady` evento. Questo evento verrà attivato dopo l&#39;inizializzazione della libreria completata. Il callback viene eseguito con `lpRuntime` oggetto per esporre il metodo e gli hook della libreria.

`LpRuntime` sta per &quot;Landing page Runtime&quot;. Questo oggetto è l&#39;identificatore della libreria principale. Verranno esposti hook, metodi di invio dei moduli e altri metodi di utilità utilizzabili in JavaScript personalizzato.

**Esempio:**

```
if(window.lpRuntime){
    init(window.lpRuntime);
}else{
    window.addEventListener('lpRuntimeReady',function(e){
        init(e.detail);
    });
}
 
function init(lpRuntime){
    // Enter custom JavaScript here using methods from lpRuntime.
}
```

## Hook

Utilizzando gli hook, è possibile allegare un metodo durante il ciclo di vita dell’invio del modulo. Ad esempio, è possibile utilizzare gli hook per eseguire una convalida del modulo prima che il modulo venga effettivamente inviato.

Ecco gli hook che puoi utilizzare:

| Nome | Descrizione |
|--- |--- |
| addBeforeSubmitHook | Gancio personalizzato da chiamare prima dell’invio del modulo. Restituisce true per continuare l&#39;invio, else restituisce false per bloccare l&#39;invio. |
| addBeforeSubmitHook | Gancio personalizzato da chiamare per l&#39;invio del modulo non riuscito. |
| addOnSuccessHook | Gancio personalizzato da chiamare in caso di invio corretto del modulo. |

**Esempio:**

```
//LpRuntime hooks
lpRuntime.hooks.addBeforeSubmitHook(function(){
    // Add your validation logic here.
});
```

## Invio di moduli personalizzati

I metodi elencati di seguito vengono utilizzati per eseguire invii di moduli personalizzati.

>[!NOTE]
>
>Poiché l’invio del modulo è gestito da JavaScript personalizzato, l’invio predefinito deve essere disabilitato esplicitamente impostando una variabile globale `disableDefaultFormSubmission` a `true`.

| Nome | Descrizione |
|--- |--- |
| submitForm | Questo metodo sottometterà il modulo e gestirà il flusso di invio successivo. |
| submitFormPartial | Questo metodo invia anche il modulo, ma ignora il flusso di invio successivo. Ad esempio, se hai configurato il reindirizzamento alla pagina di successo dopo l’invio con esito positivo, tale reindirizzamento non verrà eseguito in caso di invio parziale del modulo. |

**Esempi:**

```
//LpRuntime methods
window.disableDefaultFormSubmission = true        // Flag to disable the default submission flow.
 
lpRuntime.submitForm(formSubmissionData);         // This will trigger the default form submission handling like redirecting to error or success page.
  
lpRuntime.submitFormPartial(formSubmissionData,{   // This will not trigger the default submission handling.
    beforeSubmit : callback,
    onFailure : failureCallback,                   // Custom onFailureCallback - will be used in partial submission of form.
    onSuccess : successCallback                    // Custom onSuccessCallback - will be used in partial submission of form.
})
```

## Funzione utility

| Nome | Descrizione |
|--- |--- |
| getFormData | Questo metodo può essere utilizzato per ottenere `formData` sotto forma di un oggetto JSON. Questo oggetto può essere passato a `submitForm` per l’invio del modulo. |

**Esempio:**

```
let formData = lpRuntime.getFormData();                           // Method to generate formdata
 
lpRuntime.submitForm(formData);
```

## Casi d’uso

### Caso d&#39;uso 1: Aggiunta di una convalida prima dell’invio del modulo

```
<html>
<body>
// Enter HTML body here.
  
<script>
        if(window.lpRuntime){
          console.log('got runtime',lpRuntime);
          init(window.lpRuntime);
        }else{
          window.addEventListener('lpRuntimeReady',function(e){
            init(window.lpRuntime);
          });
        }
        
  
      // Here validate the function is checking if the checkbox is selected. This method should return true if you want form submission.
      function validateForm(){
        return document.querySelector('.spectrum-Checkbox-input').checked;
      }    
  
      function init(lpRuntime){
          lpRuntime.hooks.addBeforeSubmitHook(function(){
              return validateForm(); // This method should return true if you want to proceed with submission.
          })
      }
  
</script>  
  
</body>
</html>
```

### Caso d&#39;uso 2: Invio parziale del modulo

Ad esempio, si dispone di un modulo con più caselle di controllo sulla pagina. Selezionando una casella di controllo, si desidera salvare tali dati nel backend senza attendere che l’utente faccia clic sul pulsante di invio.

```
<html>
<body>
    <form>
        <input type='checkbox' value="1" name="name1"/>
        <input type='checkbox' value="2" name="name2"/>
        <input type='checkbox' value="3" name="name3"/>
        <input type='checkbox' value="4" name="name4"/>
    </form>
  
<script>
      window.disableDefaultFormSubmission=true;
 
      window.addEventListener('lpRuntimeReady',function(e){        
        init(e.detail)
      }
 
     function init(lpRuntime){
        window.getElementByTagName('input').addEventListener('change',function(e){
            let formData = lpRuntime.getFormData();
            lpRuntime.submitFormPartial(formData);
        })
      }
    </script>
  
</body>
</html>
```

### Caso d&#39;uso 3: Tag di analisi personalizzati

Utilizzando JavaScript puoi aggiungere ascoltatori di campi di input e allegare un trigger di chiamata di analisi personalizzato.

```
<html>
<body>
    <form>
        <input type='checkbox' value="1" name="name1"/>
        <input type='checkbox' value="2" name="name2"/>
        <input type='checkbox' value="3" name="name3"/>
        <input type='checkbox' value="4" name="name4"/>
    </form>
  
<script>
      window.disableDefaultFormSubmission=false;  
 
      window.addEventListener('lpRuntimeReady',function(e){        
        init(e.detail)
      }
 
     function init(lpRuntime){
         window.getElementByTagName('input').addEventListener('change',function(e){
            //trigger analytics events
        })
      }
        
    </script>
  
</body>
</html>
```

### Caso d&#39;uso 4: Modulo dinamico

```
<html>
<body>
    <form>
        <input type='checkbox' value="1" name="name1"/>
        <div class="hiddenInput hidden">
            <input type='text' name="name2"/>
        </div>
    </form>
  
<script>
      window.disableDefaultFormSubmission=false;     
 
      window.addEventListener('lpRuntimeReady',function(e){        
        init(e.detail)
      }
 
      function init(lpRuntime){
        window.getElementByTagName('input').addEventListener('change',function(e){
            document.querySelector('.hiddenInput').toggleClass('hidden');
        })
      }
        
    </script>
  
</body>
</html>
```
