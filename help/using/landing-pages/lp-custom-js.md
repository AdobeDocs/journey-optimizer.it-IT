---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare JavaScript personalizzato in una pagina di destinazione
description: Scopri come progettare il contenuto di una pagina di destinazione in Journey Optimizer
feature: Landing Pages
topic: Content Management
role: Developer
level: Experienced
keywords: landing, pagina di destinazione, javascript, codice
exl-id: 2a7ebead-5f09-4ea5-8f00-8b5625963290
source-git-commit: 8579acfa881f29ef3947f6597dc11d4c740c3d68
workflow-type: tm+mt
source-wordcount: '568'
ht-degree: 2%

---

# Utilizzare JavaScript personalizzato in una pagina di destinazione {#lp-custom-js}

Puoi definire il contenuto della pagina di destinazione utilizzando JavaScript personalizzato. Ad esempio, per applicare uno stile avanzato o aggiungere comportamenti personalizzati alle pagine di destinazione, puoi creare controlli personalizzati ed eseguirli in [!DNL Journey Optimizer].

## Inserire codice JavaScript in una pagina di destinazione

Per inserire un JavaScript personalizzato nel contenuto della pagina di destinazione, puoi effettuare le seguenti operazioni:

* Importa il contenuto HTML esistente quando inizi a creare il contenuto e seleziona il file che include il codice JavaScript personalizzato. Scopri come importare i contenuti [in questa sezione](../email/existing-content.md).

* Progetta la pagina di destinazione da zero o da un modello salvato. Trascina la **[!UICONTROL HTML]** componente contenuto nell’area di lavoro e mostra il codice sorgente per aggiungere il codice JavaScript al componente. Scopri come utilizzare il componente HTML in [questa sezione](../email/content-components.md#HTML). <!--You can also simply switch the whole landing page content to code view and enter or paste your JavaScript code.-->

  ![](assets/lp_designer-html-component.png)

* Inserisci o incolla il codice JavaScript direttamente nel designer del contenuto. Scopri come programmare i contenuti [in questa sezione](../email/code-content.md).

>[!NOTE]
>
>Attualmente non è possibile visualizzare JavaScript in azione quando [anteprima della pagina di destinazione](create-lp.md#test-landing-page).

Per visualizzare correttamente la pagina di destinazione, utilizza la sintassi seguente come descritto nelle sezioni seguenti.

## Inizializzazione del codice

Per inizializzare il codice JavaScript, devi utilizzare `lpRuntimeReady` evento. Questo evento verrà attivato dopo la corretta inizializzazione della libreria. Il callback verrà eseguito con `lpRuntime` oggetto per esporre il metodo e gli hook della libreria.

`LpRuntime` sta per &quot;Runtime pagina di destinazione&quot;. Questo oggetto è l’identificatore della libreria principale. Verranno esposti hook, metodi di invio dei moduli e altri metodi di utilità che possono essere utilizzati in JavaScript personalizzato.

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

Gli hook consentono di allegare un metodo durante il ciclo di vita dell&#39;invio del modulo. Ad esempio, è possibile utilizzare gli hook per eseguire una convalida del modulo prima che venga effettivamente inviato.

Di seguito sono riportati gli hook che puoi utilizzare:

| Nome | Descrizione |
|--- |--- |
| addBeforeSubmitHook | Hook personalizzato da chiamare prima dell’invio del modulo. Restituisce true per continuare l’invio, altrimenti restituisce false per bloccare l’invio. |
| addOnFailureHook | Hook personalizzato da chiamare in caso di invio del modulo non riuscito. |
| addOnSuccessHook | Hook personalizzato da chiamare in caso di invio corretto del modulo. |

**Esempio:**

```
//LpRuntime hooks
lpRuntime.hooks.addBeforeSubmitHook(function(){
    // Add your validation logic here.
});
```

## Invio di moduli personalizzati

I metodi elencati di seguito vengono utilizzati per eseguire l’invio di moduli personalizzati.

>[!NOTE]
>
>Poiché l’invio del modulo viene gestito da JavaScript personalizzato, l’invio predefinito deve essere disabilitato esplicitamente impostando una variabile globale `disableDefaultFormSubmission` a `true`.

| Nome | Descrizione |
|--- |--- |
| submitForm | Questo metodo invia il modulo e gestisce il flusso di invio dei post. |
| submitFormPartial | Anche questo metodo invierà il modulo, ma salterà il flusso di invio dei post. Ad esempio, se hai configurato il reindirizzamento alla pagina di successo dopo l’invio corretto, tale reindirizzamento non si verifica in caso di invio parziale del modulo. |

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
| getFormData | Questo metodo può essere utilizzato per ottenere `formData` sotto forma di oggetto JSON. Questo oggetto può essere passato a `submitForm` per l’invio di moduli. |

**Esempio:**

```
let formData = lpRuntime.getFormData();                           // Method to generate formdata
 
lpRuntime.submitForm(formData);
```

## Casi d’uso

### Caso d’uso 1: aggiunta della convalida prima dell’invio del modulo

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

### Caso d’uso 2: invio parziale di moduli

Ad esempio, nella pagina è presente un modulo con più caselle di controllo. Selezionando una casella di controllo, si desidera salvare i dati nel backend senza attendere che l’utente faccia clic sul pulsante Invia.

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

### Caso d’uso 3: tag di analisi personalizzati

Utilizzando JavaScript puoi aggiungere listener di campi di input e allegare un trigger di chiamata di analisi personalizzato.

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

### Caso d’uso 4: forma dinamica

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
