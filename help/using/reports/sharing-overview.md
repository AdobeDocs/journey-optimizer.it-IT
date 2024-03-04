---
solution: Journey Optimizer
product: journey optimizer
title: Panoramica sulla condivisione delle fasi del percorso
description: Panoramica sulla condivisione delle fasi del percorso
feature: Journeys, Reporting
topic: Content Management
role: Data Engineer, Data Architect, Admin
level: Experienced
source-git-commit: c82e0a4f44cda4afeb88f7dd8e645e967e4a878f
workflow-type: tm+mt
source-wordcount: '469'
ht-degree: 3%

---

# Creare rapporti sul percorso {#design-jo-reports}

Oltre a [rapporti in tempo reale](live-report.md) e incorporato [funzionalità di reporting globale](global-report.md), [!DNL Journey Optimizer] può inviare automaticamente i dati sulle prestazioni del percorso a Adobe Experience Platform in modo che possano essere combinati con altri dati a scopo di analisi.

>[!NOTE]
>
>Questa funzione viene attivata per impostazione predefinita su tutte le istanze per gli eventi dei passaggi di percorso. Non è possibile modificare o aggiornare gli schemi e i set di dati creati durante il provisioning per gli eventi dei passaggi. Per impostazione predefinita, questi schemi e set di dati sono in modalità di sola lettura.

Ad esempio, hai impostato un percorso che invia più e-mail. Questa funzionalità consente di combinare [!DNL Journey Optimizer] dati con dati di eventi a valle come il numero di conversioni avvenute, quanto coinvolgimento si è verificato sul sito web o quante transazioni si sono verificate nello store. Le informazioni sul percorso possono essere combinate con i dati su Adobe Experience Platform, provenienti da altre proprietà digitali o da proprietà offline, per offrire una visione più completa delle prestazioni.

[!DNL Journey Optimizer] crea automaticamente gli schemi e i flussi necessari nei set di dati da Adobe Experience Platform per ogni passaggio che un singolo utente compie in un percorso. Un evento di passaggio corrisponde a un singolo spostamento da un nodo all’altro in un percorso. Ad esempio, in un percorso che ha un evento, una condizione e un’azione, vengono inviati a Adobe Experience Platform tre eventi di passaggio.

L’elenco dei campi XDM passati è completo. Alcuni contengono codici generati dal sistema, altri nomi descrittivi leggibili dall&#39;utente. Alcuni esempi includono l’etichetta dell’attività del percorso o lo stato del passaggio: quante volte un’azione è scaduta o è terminata in errore.

>[!CAUTION]
>
>Non è possibile attivare i set di dati per il servizio profilo in tempo reale. Assicurarsi che il **[!UICONTROL Profilo]** l&#39;interruttore è disattivato.

[!DNL Journey Optimizer] invia i dati così come si verificano, in modo streaming. Puoi eseguire query su questi dati utilizzando Query Service. È possibile connettersi al Customer Journey Analytics o ad altri strumenti di business intelligence per visualizzare i dati relativi a questi passaggi.

Vengono creati i seguenti schemi:

* Schema evento passaggio percorso per [!DNL Journey Orchestration] : evento del passaggio del Percorso associato a un metadati del Percorso.
* Schema percorso con campi Percorso per [!DNL Journey Orchestration] - Metadati del Percorso per descrivere i Percorsi.

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

[!DNL Journey Optimizer] gli eventi dei passaggi possono essere collegati ad altri set di dati in [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=it){target="_blank"}.

Il flusso di lavoro generale è:

* [!DNL Customer Journey Analytics] acquisisce il set di dati &quot;Evento passaggio Percorso&quot;.
* Il **profileID** Il campo associato allo &quot;Schema evento del passaggio del Percorso per il Journey Orchestration&quot; è definito come un campo Identità. In entrata [!DNL Customer Journey Analytics], puoi quindi collegare questo set di dati a qualsiasi altro set di dati con lo stesso valore dell’identificatore basato su persona.
* Per utilizzare questo set di dati in [!DNL Customer Journey Analytics], per l&#39;analisi del percorso cross-channel, fare riferimento a [Documentazione del Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-usecases/cross-channel.html){target="_blank"}.

➡️ [Utilizzare il Customer Journey Analytics](cja-ajo.md){target="_blank"}

