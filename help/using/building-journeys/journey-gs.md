---
solution: Journey Optimizer
product: journey optimizer
title: Creare il primo percorso
description: Passaggi chiave per creare il primo percorso con Adobe Journey Optimizer
feature: Journeys, Get Started
topic: Content Management
role: User
level: Intermediate
keywords: percorso, primo, inizio, avvio rapido, pubblico, evento, azione
exl-id: d940191e-8f37-4956-8482-d2df0c4274aa
source-git-commit: 5f48c3df14768e699e174e5a3539438e9b774e1a
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 25%

---

# Creare il primo percorso {#jo-quick-start}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card2"
>title="Creare i percorsi"
>abstract="Utilizza **Adobe Journey Optimizer** per generare l’orchestrazione in tempo reale per diversi casi d’uso, sfruttando i dati contestuali provenienti da eventi od origini dati."

>[!CONTEXTUALHELP]
>id="ajo_journey_create"
>title="Percorsi"
>abstract="Progetta i percorsi cliente per offrire esperienze personalizzate e contestuali. Journey Optimizer consente di creare casi d’uso di orchestrazione in tempo reale sfruttando i dati contestuali archiviati negli eventi o nelle origini dati. La scheda **Panoramica** visualizza una dashboard con metriche chiave relative ai percorsi. La scheda **Sfoglia** presenta l’elenco dei percorsi esistenti."

Adobe Journey Optimizer include un’area di lavoro di orchestrazione omni-channel, che consente ai marketer di armonizzare le attività di marketing con il coinvolgimento dei clienti in modalità uno a uno. L’interfaccia utente ti consente di trascinare facilmente le attività dalla palette all’interno dell’area di lavoro per creare il percorso. L&#39;interfaccia utente del percorso è descritta in [questa pagina](journey-ui.md).

![esempio di area di lavoro percorso](assets/journey38.png)


I passaggi principali per la creazione di un percorso sono descritti in questa pagina. Sono semplificate come segue:

![Passaggi per la creazione del percorso: creazione, progettazione, test e pubblicazione](assets/journey-creation-process.png)


La creazione di percorsi di clienti in più fasi avvia una sequenza di interazioni, offerte e messaggi tra i canali in tempo reale. Questo approccio assicura il coinvolgimento dei clienti nei momenti ottimali in base alle loro azioni e ai segnali di business rilevanti. I tipi di pubblico di Target possono essere definiti in base al comportamento, ai dati contestuali e agli eventi di business. I prerequisiti dipendono dal tuo caso d&#39;uso e dal [tipo di percorso](entry-management.md#types-of-journeys) che stai creando.

Prima di iniziare a creare il percorso, controllare che siano stati completati i passaggi di configurazione pertinenti:

* Se desideri attivare i percorsi in modo unitario quando viene ricevuto un evento, devi **configurare un evento**. È possibile definire le informazioni previste e le modalità di elaborazione. [Ulteriori informazioni](../event/about-events.md).

<!--   ![](assets/jo-event7bis.png)  -->

* Il percorso può anche ascoltare i tipi di pubblico di Adobe Experience Platform per inviare messaggi in batch a un set specifico di profili. Per questo, devi **creare tipi di pubblico**. [Ulteriori informazioni](../audience/about-audiences.md).

<!--   ![](assets/segment2.png)  -->

* È possibile definire una connessione a un sistema per il recupero di informazioni aggiuntive che verranno utilizzate nei percorsi, ad esempio nelle condizioni specificate. Questa connessione si basa su un&#39;origine dati **1}.** [Ulteriori informazioni](../datasource/about-data-sources.md)

<!--   ![](assets/jo-datasource.png)  -->

* Journey Optimizer viene fornito con le funzionalità di [messaggio integrato](../building-journeys/journeys-message.md). Se si utilizza un sistema di terze parti per l&#39;invio dei messaggi, è possibile **creare un&#39;azione personalizzata**. Ulteriori informazioni in questa [sezione](../action/action.md).

<!--    ![](assets/custom2.png)  -->


Per i data engineer, i passaggi per configurare i percorsi, inclusi Origini dati, Eventi e Azioni, sono descritti in [questa sezione](../configuration/about-data-sources-events-actions.md).


>[!NOTE]
>
>Per i guardrail e le limitazioni applicabili ai percorsi, visita [questa pagina](../start/guardrails.md).

## Creare un percorso {#jo-build}

Per creare un percorso con più passaggi, effettuare le seguenti operazioni:

1. Nella sezione del menu GESTIONE PERCORSO fare clic su **[!UICONTROL Percorsi]**.

1. Fare clic sul pulsante **[!UICONTROL Crea Percorso]** per creare un nuovo percorso.

1. Modificate il riquadro di configurazione del percorso per definire il nome del percorso e impostarne le proprietà. Scopri come impostare le proprietà del percorso in [questa pagina](journey-properties.md).

   ![](assets/jo-properties.png)

A questo punto è possibile iniziare a progettare il percorso.

## Progettare il percorso {#jo-design}

Il designer di percorsi omni-channel, con la sua un’interfaccia intuitiva basata su selezione e trascinamento, ti aiuta a creare percorsi con più passaggi per tipi di pubblico target, aggiornamenti basati su interazioni del cliente o aziendali in tempo reale e messaggi omni-channel.

![](assets/journey38.png)

1. Per iniziare, trascina un evento o un&#39;attività **Read Audience** dalla palette nell&#39;area di lavoro. Per ulteriori informazioni sulla progettazione del percorso, consulta [questa sezione](using-the-journey-designer.md).

   ![](assets/read-segment.png)

1. Trascina e rilascia i passaggi successivi che il singolo utente seguirà. Ad esempio, puoi aggiungere una condizione seguita da un’azione di canale. Per ulteriori informazioni sulle attività, consulta [questa sezione](about-journey-activities.md).

## Test del percorso {#jo-test}

Dopo aver creato il percorso, puoi testarlo prima di pubblicarlo. Journey Optimizer offre la &quot;modalità di test&quot; come modo per visualizzare i profili di test mentre si spostano lungo il percorso, rilevando potenziali errori prima dell’attivazione. L’esecuzione di test rapidi consente di verificare il corretto funzionamento dei percorsi e di pubblicarli in modo affidabile.

Ulteriori informazioni in questa [sezione](testing-the-journey.md)

## Pubblica il percorso {#jo-pub}

Devi pubblicare un percorso per attivarlo e renderlo disponibile per i nuovi profili per poterlo inserire. Prima di pubblicare il percorso, verificane la validità e l’assenza di errori. Impossibile pubblicare un percorso con errori. Ulteriori informazioni sulla pubblicazione di percorso in questa [sezione](publishing-the-journey.md).

![](assets/jo-journeyuc2_32bis.png)

Dopo la pubblicazione, puoi monitorare il percorso utilizzando gli strumenti di reporting dedicati per misurare l’efficacia del percorso.

![](assets/jo-dynamic_report_journey_12.png)

Ulteriori informazioni sui report di percorso sono disponibili in questa [sezione](../reports/live-report.md).

>[!NOTE]
>
>Se devi modificare un percorso **live**, [crea una nuova versione](journey-ui.md#journey-versions) del percorso.
