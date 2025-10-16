---
solution: Journey Optimizer
product: journey optimizer
title: Modificare il contenuto della campagna attivata dall’API
description: Scopri come modificare il contenuto della campagna attivata da API.
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: campagne, attivate da API, REST, ottimizzatore, messaggi
exl-id: b7f12c65-c1af-4c49-b126-c13a51940a43
source-git-commit: 93698c93f3750b4d7feff18509f8144a7c79f156
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 2%

---

# Modificare il contenuto della campagna attivata dall’API {#api-content}

Per configurare il contenuto del messaggio, passa alla scheda **[!UICONTROL Contenuto]** o fai clic sul pulsante **[!UICONTROL Modifica contenuto]**.

![](assets/campaign-content.png)

## Progettare il contenuto {#design}

Il processo di creazione dei contenuti dipende dal canale selezionato. Scopri i passaggi dettagliati per creare il contenuto del messaggio nelle pagine seguenti:

<table style="table-layout:fixed"><tr style="border: 0;">
<td><a href="../email/create-email.md"><img alt="e-mail" src="../channels/assets/do-not-localize/email.png"></a>
<div align="center"><a href="../email/create-email.md"><strong>E-mail</strong></a></div></td>
<td><a href="../sms/create-sms.md"><img alt="SMS" src="../channels/assets/do-not-localize/sms.png"></a>
<div align="center"><a href="../sms/create-sms.md"><strong>SMS</strong></a></div></td>
<td><a href="../push/create-push.md"><img alt="push" src="../channels/assets/do-not-localize/push.png"></a>
<div align="center"><a href="../push/create-push.md"><strong>Notifica push</strong></a></div></td>
</tr></table>

## Personalizzare i contenuti utilizzando i dati contestuali {#contextual}

Puoi trasmettere dati aggiuntivi nel payload API che puoi sfruttare per personalizzare il messaggio.

Prendiamo questo esempio, in cui i clienti vogliono reimpostare la propria password e desideri inviare loro un URL di reimpostazione della password generato in uno strumento di terze parti. Con le campagne attivate da API, puoi passare l’URL generato nel payload API e sfruttarlo nella campagna per aggiungerlo al messaggio.

A questo scopo, devi passarli nel payload API e aggiungerli nel messaggio utilizzando l’editor di personalizzazione. Utilizza la sintassi `{{context.<contextualAttribute>}}`, in cui `<contextualAttribute>` deve corrispondere al nome della variabile nel payload dell&#39;API contenente i dati che desideri trasmettere.

Per il momento non è disponibile alcun attributo contestuale da utilizzare nel menu della barra a sinistra. Gli attributi devono essere digitati direttamente nell&#39;espressione di personalizzazione, senza alcun controllo eseguito da [!DNL Journey Optimizer].

![](assets/api-triggered-context.png)

**Deve leggere**

* Gli attributi contestuali passati nella richiesta non possono superare i 200 kb e sono sempre considerati di tipo stringa.
* La sintassi `context.system` è limitata all&#39;uso interno di Adobe e non deve essere utilizzata per trasmettere attributi contestuali.
* A differenza degli eventi abilitati per il profilo, i dati contestuali passati nell’API REST vengono utilizzati per una comunicazione una tantum e non memorizzati rispetto al profilo. Al massimo, il profilo viene creato con i dettagli dello spazio dei nomi, se questo è stato trovato mancante.
* L’utilizzo di un numero elevato o di dati contestuali pesanti nel contenuto può influire sulle prestazioni.

## Verifica e verifica il contenuto

Una volta definito il contenuto, utilizza il pulsante **[!UICONTROL Simula contenuto]** per visualizzare in anteprima e verificare il contenuto con profili di test o dati di input di esempio caricati da un file CSV/JSON, oppure aggiunti manualmente. [Scopri come visualizzare in anteprima e verificare il contenuto](../content-management/preview-test.md). Per tornare alla schermata di creazione della campagna, fai clic sulla freccia sinistra.

![](assets/create-campaign-design.png)

## Passaggi successivi {#next}

Una volta che la configurazione e il contenuto della campagna sono pronti, puoi definire il pubblico della campagna. [Ulteriori informazioni](api-triggered-campaign-audience.md)
