---
solution: Journey Optimizer
product: journey optimizer
title: Panoramica sulla condivisione delle fasi del percorso
description: Panoramica sulla condivisione delle fasi del percorso
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 07d25f8e-0065-4410-9895-ffa15d6447bb
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 0%

---

# Creare rapporti sui percorsi {#design-jo-reports}

Oltre a [rapporti in tempo reale](live-report.md) e incorporati [funzionalità di reporting globale](global-report.md), [!DNL Journey Optimizer] può inviare automaticamente i dati sulle prestazioni del percorso ad Adobe Experience Platform in modo che possano essere combinati con altri dati a scopo di analisi.

>[!NOTE]
>
>Questa funzione è attivata per impostazione predefinita su tutte le istanze per gli eventi dei passaggi del percorso. Non è possibile modificare o aggiornare gli schemi e i set di dati creati durante il provisioning per gli eventi delle fasi. Per impostazione predefinita, questi schemi e set di dati sono in modalità di sola lettura.

Ad esempio, hai impostato un percorso che invia più e-mail. Questa funzionalità consente di combinare [!DNL Journey Optimizer] dati con dati evento a valle come quante conversioni si sono verificate, quanto coinvolgimento è avvenuto sul sito web o quante transazioni sono avvenute nel negozio. Le informazioni sul percorso possono essere combinate con i dati su Adobe Experience Platform, provenienti da altre proprietà digitali o da proprietà offline, per fornire una visione più completa delle prestazioni.

[!DNL Journey Optimizer] crea automaticamente gli schemi e i flussi necessari nei set di dati ad Adobe Experience Platform per ogni passaggio effettuato da un singolo utente in un percorso. Un evento step corrisponde a un singolo passaggio da un nodo all’altro in un percorso. Ad esempio, in un percorso con un evento, una condizione e un’azione, tre eventi di passaggio vengono inviati ad Adobe Experience Platform.

L’elenco dei campi XDM passati è completo. Alcuni contengono codici generati dal sistema e altri hanno nomi descrittivi leggibili dall&#39;uomo. Alcuni esempi includono l’etichetta dell’attività di percorso o lo stato del passaggio: quante volte un&#39;azione è scaduta o terminata con un errore.

>[!CAUTION]
>
>Impossibile attivare i set di dati per il servizio di profilo in tempo reale. Assicurati che la **[!UICONTROL Profile]** l&#39;interruttore è disattivato.

[!DNL Journey Optimizer] invia i dati mentre si verificano, in modo streaming. È possibile eseguire query su questi dati utilizzando il servizio query. Puoi connetterti a Customer Journey Analytics o ad altri strumenti BI per visualizzare i dati relativi a questi passaggi.

Vengono creati i seguenti schemi:

* Schema evento del passaggio del percorso per [!DNL Journey Orchestration] - Evento passaggio del percorso associato a metadati del percorso.
* Schema del percorso con i campi del percorso per [!DNL Journey Orchestration] - Metadati del percorso per descrivere i percorsi.

![](assets/sharing1.png)

![](assets/sharing2.png)

Vengono passati i seguenti set di dati:

* Eventi dei passaggi del percorso
* Percorsi

![](assets/sharing3.png)

Gli elenchi dei campi XDM passati ad Adobe Experience Platform sono descritti in dettaglio qui:

* [Elenco dei campi evento del passaggio](../reports/sharing-field-list.md)
* [Campi evento del passaggio precedente](../reports/sharing-legacy-fields.md)

## Integrazione con Customer Journey Analytics {#integration-cja}

[!DNL Journey Optimizer] gli eventi di passaggio possono essere collegati ad altri set di dati in [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html){target=&quot;_blank&quot;}.

Il flusso di lavoro generale è:

* [!DNL Customer Journey Analytics] Inserisce il set di dati &quot;Journey Step Event&quot;.
* La **profileID** Il campo nello &quot;schema evento del passaggio del percorso per Journey Orchestration&quot; associato è definito come un campo Identity. In [!DNL Customer Journey Analytics], puoi quindi collegare questo set di dati a qualsiasi altro set di dati con lo stesso valore dell’identificatore basato su persona.
* Per utilizzare questo set di dati in [!DNL Customer Journey Analytics], per l’analisi del percorso cross-channel, consulta [Documentazione di Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-usecases/cross-channel.html){target=&quot;_blank&quot;}.

