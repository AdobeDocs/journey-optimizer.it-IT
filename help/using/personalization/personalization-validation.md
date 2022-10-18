---
solution: Journey Optimizer
product: journey optimizer
title: Convalida della personalizzazione
description: Ulteriori informazioni sulla convalida della personalizzazione e su come risolvere i problemi.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
exl-id: 7abeec5e-743f-48fb-a4a6-056665e8bfda
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 2%

---

# Convalida della personalizzazione {#personalization-validation}

## Meccanismi di convalida {#validation-mechanisms}

In **Editor espressioni** , utilizza **Convalida** per controllare la sintassi di personalizzazione.

>[!NOTE]
> La convalida viene eseguita automaticamente quando si fa clic sul pulsante **Aggiungi** per chiudere la finestra dell’editor.

![](assets/perso_validation1.png)

>[!IMPORTANT]
> Se la sintassi di personalizzazione non è valida, non è possibile chiudere la finestra dell’editor espressioni.

## Errori comuni {#common-errors}

* **Percorso &quot;XYZ&quot; non trovato**

Quando si tenta di fare riferimento a un campo non definito nello schema.

In questo caso **firstName1** non è definito come attributo nello schema del profilo:

```
{{profile.person.name.firstName1}}
```

* **Tipo non corrispondente per la variabile &quot;XYZ&quot;. Matrice prevista. Stringa trovata.**

Quando si tenta di eseguire iterazioni su una stringa invece che su una matrice:

In questo caso **prodotto** non è una matrice:

```
{{each profile.person.name.firstName as |product|}}
 {{product.productName}}
{{/each}}
```

* **Sintassi handlebars non valida. Trovato`‘[XYZ}}’`**

Se viene utilizzata una sintassi handlebar non valida.

Le espressioni Handlebars sono circondate da **{{expression}}**

```
   {{[profile.person.name.firstName}}
```

* **Definizione del segmento non valida**

```
No segment definition found for 988afe9f0-d4ae-42c8-a0be-8d90e66e151
```

## Errori specifici relativi alle offerte {#specific-errors}

Gli errori relativi all’integrazione delle offerte in un messaggio e-mail o push hanno il seguente pattern:

```
Offer.<offerType>.[PlacementID].[ActivityID].<offer-attribute>
```

La convalida viene eseguita durante la convalida del contenuto di personalizzazione nell’editor espressioni.

<table> 
 <thead> 
  <tr> 
   <th> Titolo dell’errore<br /> </th> 
   <th> Convalida/Risoluzione <br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>Risorsa con id placementID e tipo OfferPlacement non trovata <br/>
Risorsa con id activityID e tipo OfferActivity non trovata<br/></td> 
   <td>Controlla se sono disponibili gli ID attività e/o posizionamento</td> 
  </tr> 
   <tr> 
   <td>Impossibile convalidare la risorsa.</td> 
   <td>Il componentType nel Placement deve corrispondere all'offerta offerType</td> 
  </tr> 
   <tr> 
   <td>L'URL pubblico non è presente in offerId.</td> 
   <td>Le Offerte immagine (tutte le offerte personalizzate e di fallback associate alla coppia decisione e posizionamento) devono avere un URL pubblico popolato (deliveryURL non deve essere vuoto).</td> 
  </tr> 
  <tr> 
   <td>La decisione contiene attributi non di profilo.</td> 
   <td>Offerte L'utilizzo del modello deve contenere solo gli attributi del profilo.</td> 
  </tr> 
  <tr> 
   <td>Errore durante il recupero dell'utilizzo della decisione.</td> 
   <td>Questo errore potrebbe verificarsi quando l’API sta tentando di recuperare il modello di offerta.</td> 
  </tr>
  <tr> 
   <td>Attributo di offerta non valido.</td> 
   <td>Controlla se l'attributo dell'offerta a cui si fa riferimento nell'offerta drp è valido. Di seguito sono riportati gli attributi validi: <br/>
Immagine: deliveryURL, linkURL<br/>
Testo: content<br/>
HTML: content<br/></td> 
  </tr> 
 </tbody> 
</table>
