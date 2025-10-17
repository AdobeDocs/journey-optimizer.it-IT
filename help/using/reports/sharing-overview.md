---
solution: Journey Optimizer
product: journey optimizer
title: Panoramica sulla condivisione delle fasi del percorso
description: Panoramica sulla condivisione delle fasi del percorso
feature: Journeys, Reporting
topic: Content Management
role: Data Engineer, Data Architect, Admin
level: Experienced
exl-id: 29d6b881-35a3-4c62-9e7d-d0aeb206ea77
source-git-commit: efae7f7d366690af71430bb9eb62523d1881c50e
workflow-type: tm+mt
source-wordcount: '620'
ht-degree: 3%

---

# Creare rapporti sul percorso {#design-jo-reports}

Oltre ai [rapporti in tempo reale](live-report.md) e alle [funzionalità di reporting](report-gs-cja.md) integrate, [!DNL Journey Optimizer] può inviare automaticamente i dati sulle prestazioni del percorso a Adobe Experience Platform in modo che possano essere combinati con altri dati a scopo di analisi.

>[!NOTE]
>
>Questa funzione viene attivata per impostazione predefinita su tutte le istanze per gli eventi dei passaggi di percorso. Non è possibile modificare o aggiornare gli schemi e i set di dati creati durante il provisioning per gli eventi dei passaggi. Per impostazione predefinita, questi schemi e set di dati sono in modalità di sola lettura.

Ad esempio, hai impostato un percorso che invia più e-mail. Questa funzionalità consente di combinare i dati di [!DNL Journey Optimizer] con i dati di eventi a valle, ad esempio il numero di conversioni avvenute, il livello di coinvolgimento nel sito Web o il numero di transazioni avvenute nello store. Le informazioni sul percorso possono essere combinate con i dati su Adobe Experience Platform, provenienti da altre proprietà digitali o da proprietà offline, per offrire una visione più completa delle prestazioni.

[!DNL Journey Optimizer] crea automaticamente gli schemi e i flussi necessari nei set di dati a Adobe Experience Platform per ogni passaggio che un singolo utente compie in un percorso. Un evento di passaggio corrisponde a un singolo spostamento da un nodo all’altro in un percorso. Ad esempio, in un percorso che ha un evento, una condizione e un’azione, vengono inviati a Adobe Experience Platform tre eventi di passaggio.

>[!NOTE]
>
>Oltre agli eventi dei passaggi a livello di profilo, il sistema genera anche eventi interni per le attività **Read Audience**. Questi eventi, denominati `segmentExportJob` eventi, registrano il ciclo di vita del nodo Read Audience (ad esempio creazione di processi di esportazione, accodamento, completamento ed errori) e vengono generati per attività Read Audience, non per singolo profilo. Di conseguenza, a questi eventi potrebbe non essere associato un identificatore di profilo (UPMID). Questi eventi interni sono utili per monitorare e risolvere i problemi relativi alle prestazioni Read Audience e possono essere interrogati utilizzando i campi documentati nella sezione [serviceEvents](../reports/sharing-field-list.md#servicevents-field). Per esempi di query su come utilizzare gli eventi segmentExportJob, vedi [Query relative all&#39;audience di lettura](../reports/query-examples.md#read-segment-queries).

In alcuni casi è possibile creare più eventi per lo stesso nodo. Ad esempio, nel caso dell’attività Attendi:

* Un evento viene generato quando il profilo entra nell’attesa (l’attributo journeyNodeProcessed è uguale a false)
* Un evento viene generato quando il profilo ne esce (l’attributo journeyNodeProcessed è uguale a true)

L’elenco dei campi XDM passati è completo. Alcuni contengono codici generati dal sistema, altri nomi descrittivi leggibili dall&#39;utente. Alcuni esempi includono l’etichetta dell’attività del percorso o lo stato del passaggio: quante volte un’azione è scaduta o è terminata in errore.

>[!CAUTION]
>
>Non è possibile attivare i set di dati per il servizio profilo in tempo reale. Assicurarsi che l&#39;interruttore **[!UICONTROL Profilo]** sia disattivato.

[!DNL Journey Optimizer] invia i dati mentre si verificano, in streaming. Puoi eseguire query su questi dati utilizzando Query Service. È possibile connettersi a Customer Journey Analytics o ad altri strumenti di business intelligence per visualizzare i dati relativi a questi passaggi.

Vengono creati i seguenti schemi:

* Schema evento passaggio percorso per [!DNL Journey Orchestration] - evento passaggio Percorso associato a un metadati Percorso.
* Schema percorso con campi Percorso per [!DNL Journey Orchestration] - Metadati Percorso per descrivere i Percorsi.

![](assets/sharing1.png)

![](assets/sharing2.png)

Vengono passati i seguenti set di dati:

* Eventi passaggio percorso
* Percorsi

![](assets/sharing3.png)

Gli elenchi dei campi XDM passati a Adobe Experience Platform sono descritti qui:

* [Elenco dei campi evento del passaggio](../reports/sharing-field-list.md)
* [Campi evento del passaggio precedente](../reports/sharing-legacy-fields.md)

## Integrazione con Customer Journey Analytics {#integration-cja}

Gli eventi del passaggio [!DNL Journey Optimizer] possono essere collegati ad altri set di dati in [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=it){target="_blank"}.

Il flusso di lavoro generale è:

* [!DNL Customer Journey Analytics] acquisisce il set di dati &quot;Evento passaggio Percorso&quot;.
* Il campo **profileID** nello &quot;Schema evento passaggio di Percorso per Journey Orchestration&quot; associato è definito come campo Identity. In [!DNL Customer Journey Analytics] è quindi possibile collegare questo set di dati a qualsiasi altro set di dati con lo stesso valore dell&#39;identificatore basato su persona.
* Per utilizzare questo set di dati in [!DNL Customer Journey Analytics], per l&#39;analisi del percorso cross-channel, fare riferimento alla [documentazione di Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-usecases/cross-channel.html){target="_blank"}.

➡️ [Utilizzare Customer Journey Analytics](cja-ajo.md){target="_blank"}
