---
solution: Journey Optimizer
product: journey optimizer
title: Convalida della personalizzazione
description: Ulteriori informazioni sulla convalida della personalizzazione e su come risolvere i problemi.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: espressione, editor, convalida, errori, personalizzazione
exl-id: 7abeec5e-743f-48fb-a4a6-056665e8bfda
source-git-commit: ff6619925a36d2687922d1b631d1cabbcb98167e
workflow-type: tm+mt
source-wordcount: '315'
ht-degree: 2%

---

# Convalida della personalizzazione {#personalization-validation}

## Meccanismi di convalida {#validation-mechanisms}

Nella schermata dell&#39;**editor di personalizzazione**, utilizza il pulsante **Convalida** per verificare la sintassi di personalizzazione.

>[!NOTE]
> La convalida viene eseguita automaticamente quando si fa clic sul pulsante **Aggiungi** per chiudere la finestra dell&#39;editor.

![](assets/perso_validation1.png)

>[!IMPORTANT]
> Se la sintassi di personalizzazione non è valida, non puoi chiudere la finestra dell’editor di personalizzazione.

## Errori comuni {#common-errors}

* **Percorso &quot;XYZ&quot; non trovato**

Quando tenti di fare riferimento a un campo non definito nello schema.

In questo caso **firstName1** non è definito come attributo nello schema del profilo:

```
{{profile.person.name.firstName1}}
```

* **Tipo non corrispondente per la variabile &quot;XYZ&quot;. Previsto array. Trovata stringa.**

Quando si tenta di eseguire l’iterazione su una stringa invece che su un array:

In questo caso **product** non è un array:

```
{{each profile.person.name.firstName as |product|}}
 {{product.productName}}
{{/each}}
```

* **Sintassi Handlebars non valida. Trovato`‘[XYZ}}’`**

Se viene utilizzata una sintassi Handlebars non valida.

Le espressioni Handlebars sono circondate da **{{expression}}**

```
   {{[profile.person.name.firstName}}
```

* **Definizione segmento non valida**

```
No segment definition found for 988afe9f0-d4ae-42c8-a0be-8d90e66e151
```

## Errori specifici relativi alle offerte {#specific-errors}

Gli errori relativi all’integrazione delle offerte in un messaggio e-mail o push hanno il seguente pattern:

```
Offer.<offerType>.[PlacementID].[ActivityID].<offer-attribute>
```

La convalida viene eseguita durante la convalida del contenuto di personalizzazione nell’editor di personalizzazione.

<table> 
 <thead> 
  <tr> 
   <th> Titolo errore<br /> </th> 
   <th> Convalida/risoluzione <br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>Risorsa con ID placementID e tipo OfferPlacement non trovata <br/>
Risorsa con ID activityID e tipo OfferActivity non trovata<br/></td> 
   <td>Controlla se ActivityID e/o PlacementID sono disponibili</td> 
  </tr> 
   <tr> 
   <td>Impossibile convalidare la risorsa.</td> 
   <td>Il componentType nel posizionamento deve corrispondere all’offerta offerType</td> 
  </tr> 
   <tr> 
   <td>L’URL pubblico non è presente in offerId.</td> 
   <td>Le offerte di immagini (tutte le offerte personalizzate e di fallback associate alla coppia decisione-posizionamento) devono avere un URL pubblico popolato (deliveryURL non deve essere vuoto).</td> 
  </tr> 
  <tr> 
   <td>La decisione contiene attributi non di profilo.</td> 
   <td>Offerte L’utilizzo del modello deve contenere solo gli attributi del profilo.</td> 
  </tr> 
  <tr> 
   <td>Si è verificato un errore durante il recupero dell’utilizzo della decisione.</td> 
   <td>Questo errore può verificarsi quando l’API tenta di recuperare il modello di offerta.</td> 
  </tr>
  <tr> 
   <td>Attributo offerta attributo offerta non valido.</td> 
   <td>Verifica se l’attributo dell’offerta a cui si fa riferimento nel pacchetto di offerta è valido. Di seguito sono riportati gli attributi validi: <br/>
Immagine: deliveryURL, linkURL<br/>
Testo: content<br/>
HTML: content<br/></td> 
  </tr> 
 </tbody> 
</table>
