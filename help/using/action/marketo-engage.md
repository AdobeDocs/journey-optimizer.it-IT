---
solution: Journey Optimizer
product: journey optimizer
title: Integrare con Marketo Engage
description: Scopri come utilizzare l’azione Marketo Engage
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate
keywords: marketo, integrazione marketo engagement
source-git-commit: 92591457d2189e3c43ea38c4a09d7cf565bb5d57
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 4%

---


# Integrare con Marketo Engage {#integrating-with-marketo-engage}

Approfitta di un percorso di integrazione perfetta dei dati con il Marketo Engage. Questa azione personalizzata specifica in Journey Optimizer supporta l’acquisizione di due tipi di dati chiave:

* Persone (profili): Marketo trasforma i profili in informazioni fruibili.
* Oggetti personalizzati: personalizza i tuoi dati con oggetti personalizzati, come prodotti, per un approccio di marketing personalizzato.

## Prerequisiti {#prerequisites}

* L’istanza cliente del Marketo Engage deve essere abilitata per IMS.
* L’istanza di Marketo Engage e l’istanza AEP/AJO devono trovarsi nella stessa organizzazione IMS.
* Al cliente deve essere fornito l&#39;accesso **MktoSync: servizio di acquisizione**

## Configurazione dell’azione {#configure-marketo-action}

* Passa a Amministrazione > Configurazioni > Azioni e fai clic su Gestisci
* Nell&#39;elenco Azioni fare clic su Crea azione. Ulteriori informazioni sulle [azioni personalizzate](../building-journeys/using-custom-actions.md){target="_blank"}.
* Immetti Nome, Descrizione e seleziona Adobe Marketo Engage come tipo di azione

![](assets/engage-customaction-creation.png){width="40%" align="left"}

* Fai clic su Modifica payload per i payload **Richiesta** e **Risposta**.
* Per entrambi, componi il payload e incollalo nella finestra a comparsa dedicata.

![](assets/engage-customaction-payload.png){width="70%" align="left"}

* Inspect e configurare i valori del payload
Nota: per passare i valori in modo dinamico, per ogni campo cambia **Costante** in **Variabile**.

![](assets/engage-customaction-payload-fields.png){width="70%" align="left"}

* Fai clic su **Salva** nella finestra di configurazione del campo, quindi su **Salva** per eseguire l&#39;azione personalizzata.

Ora puoi utilizzare l’azione personalizzata nell’area di lavoro dedicata.


## Sintassi del payload {#payload-syntax}

### Persona

![](assets/payload-person.png)

### CustomObject

![](assets/payload-customobject.png)


**Esempio di payload per la persona**

```json
{
   "munchkinID": "388-KKG-245",  
   "person": {
    "priority": "normal",
    "partitionName": "XYZ",
    "dedupeFields": {
      "field1": "email",
      "field2": "firstName"
    },
    "objects": [
      {
        "email": "Email address",
        "firstName": "First name",
        "lastName": "Last name"
      }
    ]
  }
}
```

**Esempio di payload per l&#39;oggetto personalizzato**

```json
{
  "munchkinID": "388-KKG-245", 
  "customObject": {
    "priority": "normal",
    "objectName": "products",
    "objects": [
      {
        "email": "Email Address",
        "productName": "Product Name",
        "productQty": "Product Quantity",
        "priceTotal": "Price Total"
      }
    ]
  }
}
```


## Utilizzo dell’azione {#engage-using}

* Trascina l’azione personalizzata nell’area di lavoro del percorso.
* Nella sezione **Parametri richiesta**, fai clic su Modifica per ciascuno dei parametri con valori dinamici configurati nel payload.

![](assets/engage-use-canvas.png){width="70%" align="left"}

