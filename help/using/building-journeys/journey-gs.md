---
solution: Journey Optimizer
product: journey optimizer
title: Creare il primo percorso
description: Passaggi chiave per creare il primo percorso con  [!DNL Adobe Journey Optimizer]
feature: Journeys, Get Started
topic: Content Management
role: User
level: Intermediate
keywords: percorso, primo, inizio, avvio rapido, pubblico, evento, azione
exl-id: d940191e-8f37-4956-8482-d2df0c4274aa
version: Journey Orchestration
source-git-commit: 7d176d5e2fbaa26d9b4ac22e08c7a86ccea22c45
workflow-type: tm+mt
source-wordcount: '1213'
ht-degree: 10%

---

# Creare il primo percorso {#jo-quick-start}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card2"
>title="Creare i percorsi"
>abstract="Utilizza **[!DNL Adobe Journey Optimizer]** per generare l’orchestrazione in tempo reale per diversi casi d’uso, sfruttando i dati contestuali provenienti da eventi o da origini dati."

>[!CONTEXTUALHELP]
>id="ajo_journey_create"
>title="Percorsi"
>abstract="Progetta i percorsi cliente per offrire esperienze personalizzate e contestuali. Journey Optimizer consente di creare casi d’uso di orchestrazione in tempo reale sfruttando i dati contestuali archiviati negli eventi o nelle origini dati. La scheda **Panoramica** visualizza una dashboard con metriche chiave relative ai percorsi. La scheda **Sfoglia** presenta l’elenco dei percorsi esistenti."

[!DNL Adobe Journey Optimizer] include un&#39;area di lavoro di orchestrazione omnicanale che consente agli addetti marketing di armonizzare l&#39;attività di marketing con il coinvolgimento dei clienti uno a uno. L’interfaccia utente ti consente di trascinare facilmente le attività dalla palette all’interno dell’area di lavoro per creare il percorso. L&#39;interfaccia utente del percorso è descritta in [questa pagina](journey-ui.md).

![esempio di area di lavoro percorso](assets/journey38.png)

I passaggi principali per la creazione di un percorso sono descritti in questa pagina. Sono semplificate come segue:

![Passaggi per la creazione del percorso: creazione, progettazione, test e pubblicazione](assets/journey-creation-process.png)

In questa guida:

* Definire un punto di ingresso percorso: un segmento di pubblico o un evento in tempo reale
* Aggiungere azioni messaggio tra canali diversi (e-mail, push o SMS)
* Verifica il percorso con i profili di test prima dell’attivazione
* Pubblicare il percorso e monitorarne le prestazioni

Crea percorsi di clienti in più passaggi per avviare in tempo reale una sequenza di interazioni, offerte e messaggi tra i canali. Questo approccio assicura il coinvolgimento dei clienti nei momenti ottimali in base alle loro azioni e ai segnali di business rilevanti. I tipi di pubblico di Target sono definiti in base al comportamento, ai dati contestuali e agli eventi di business. I prerequisiti dipendono dal caso d&#39;uso e dal [tipo di percorso](entry-management.md#types-of-journeys) che si sta creando.

Ulteriori informazioni sul modo in cui i profili passano attraverso i percorsi e le velocità di elaborazione dei percorsi in [questa sezione](entry-management.md#journey-processing-rate).

<!--
>[!TIP]
>
>Not sure whether to use a journey or a campaign? [Learn how to choose the right approach](../start/journeys-vs-campaigns.md).
-->

## Prima di iniziare {#prerequisites}

Ciò che devi configurare prima di creare dipende da come viene attivato il percorso. La maggior parte dei percorsi inizia da uno dei due punti di ingresso seguenti:

* **Voce basata su pubblico**: il percorso viene eseguito per un set definito di profili in un orario pianificato. [Crea un pubblico](../audience/about-audiences.md) in Adobe Experience Platform prima di creare il percorso. Questo è il punto di partenza consigliato se hai poca esperienza con Journey Optimizer.

* **Voce basata su eventi**: il percorso viene attivato in tempo reale quando un utente esegue un&#39;azione, ad esempio un acquisto o un abbonamento. [Configura un evento](../event/about-events.md) per definire il trigger e i dati che contiene.

I seguenti elementi sono facoltativi, ma possono essere richiesti a seconda del caso d’uso:

* **Origine dati**: per arricchire le condizioni di percorso o la personalizzazione con i dati di un sistema esterno, impostare un&#39;origine dati [&#128279;](../datasource/about-data-sources.md).

* **Azione personalizzata**: se recapiti messaggi tramite un sistema di terze parti anziché tramite i canali incorporati, configura [azione personalizzata](../action/action.md).

>[!NOTE]
>
>Se sei un ingegnere dati responsabile della configurazione tecnica (eventi, origini dati e azioni), consulta [questa sezione](../configuration/about-data-sources-events-actions.md).

>[!NOTE]
>
>I guardrail e le limitazioni del percorso sono descritti in dettaglio in [questa pagina](../start/guardrails.md).

## Creare un percorso {#jo-build}

Per creare un percorso con più passaggi, effettuare le seguenti operazioni:

1. Nella sezione del menu GESTIONE PERCORSO fare clic su **[!UICONTROL Percorsi]**.

1. Fare clic sul pulsante **[!UICONTROL Crea Percorso]** per creare un nuovo percorso.

1. Modificate il riquadro di configurazione del percorso per definire il nome del percorso e impostarne le proprietà. Scopri come impostare le proprietà del percorso in [questa pagina](journey-properties.md).

   >[!TIP]
   >
   >**Quale tipo di percorso scegliere?** Se hai poca esperienza con Journey Optimizer, inizia con un percorso basato sul pubblico utilizzando un&#39;attività **[!UICONTROL Read Audience]**, non richiede alcuna configurazione precedente dell&#39;evento ed è il modo più semplice per acquisire familiarità con l&#39;area di lavoro. Per esperienze in tempo reale attivate da eventi (ad esempio, in risposta a un acquisto o all’invio di un modulo), configura prima un evento e utilizza una voce basata su eventi. Ulteriori informazioni sui [tipi di percorso](entry-management.md#types-of-journeys).

   ![Pannello proprietà Percorso con impostazioni e opzioni di configurazione](assets/jo-properties.png)

A questo punto è possibile iniziare a progettare il percorso.

## Progettare il percorso {#jo-design}

Il designer del percorso consente di creare percorsi con più passaggi mediante un&#39;interfaccia intuitiva basata sul trascinamento della selezione. Le attività nella palette a sinistra sono organizzate in tre categorie: **Eventi**, **Orchestrazione** e **Azioni**. Per una panoramica completa dell&#39;area di lavoro e dei relativi controlli, vedere [questa pagina](using-the-journey-designer.md).

![Interfaccia di Progettazione Percorsi con tavolozza attività e area di lavoro](assets/journey38.png)

Per progettare il percorso, effettuare le seguenti operazioni:

1. **Aggiungi un punto di ingresso**. Trascina un evento o un&#39;attività **[!UICONTROL Read Audience]** dalla palette nell&#39;area di lavoro. Definisce il modo in cui i profili entrano nel percorso: singolarmente in tempo reale (in base a un evento) oppure tutti contemporaneamente da un pubblico definito (in base al pubblico).

   ![Leggi configurazione attività pubblico per selezionare il pubblico di destinazione](assets/read-segment.png)

1. **Aggiungi azioni messaggio** — Dalla sezione **[!UICONTROL Azioni]** della palette, trascina un&#39;azione canale nell&#39;area di lavoro per inviare messaggi ai profili che attraversano il percorso. Le azioni sono disponibili per e-mail, notifiche push, SMS e altro ancora.

1. **Aggiungi attività di orchestrazione**. Utilizzare un&#39;attività **[!UICONTROL Condition]** per diramare il percorso in più percorsi in base agli attributi o al comportamento del profilo. Utilizza un&#39;attività **[!UICONTROL Attendi]** per introdurre un ritardo tra i passaggi.

>[!TIP]
>
>Per percorsi con più fasi o molti punti di contatto, prova a suddividere il flusso end-to-end in percorsi secondari più piccoli connessi all&#39;attività **[!UICONTROL Jump]**. Questo riduce la complessità e semplifica il test indipendente di ogni percorso secondario. Ulteriori informazioni in [Strategia di progettazione: percorsi secondari con dimensioni ridotte](jump.md#jump-strategy).

## Test del percorso {#jo-test}

Dopo aver creato il percorso, testarlo prima di pubblicarlo. Journey Optimizer offre una **modalità di test** per visualizzare i profili di test mentre si spostano lungo il percorso, rilevando potenziali errori prima dell&#39;attivazione. L’esecuzione di test rapidi garantisce il corretto funzionamento dei percorsi, in modo da consentirne la pubblicazione sicura. Scopri come testare il percorso [&#x200B; in questa sezione](testing-the-journey.md)

Puoi anche eseguire il percorso in **Dry run**. La prova del percorso è una modalità speciale di pubblicazione di un percorso in Adobe Journey Optimizer che consente ai professionisti del percorso di poterne effettuare un test, utilizzando dati di produzione reali e senza la necessità di contattare la clientela reale o aggiornare le informazioni di profilo. Questa funzione aiuta i professionisti del percorso ad acquisire fiducia nella progettazione del percorso e nel targeting del pubblico prima di pubblicarlo in diretta. Scopri come pubblicare un percorso in modalità di esecuzione a secco [in questa sezione](journey-dry-run.md).

## Pubblicare il percorso {#jo-pub}

Devi pubblicare un percorso per attivarlo e renderlo disponibile per i nuovi profili per poterlo inserire. Prima di pubblicare il percorso, verificarne la validità e verificare che non siano presenti errori. Impossibile pubblicare un percorso con errori. Ulteriori informazioni sulla pubblicazione di percorso in questa [sezione](publish-journey.md).

![Flusso di percorso completo con pubblico, condizioni e azioni](assets/jo-journeyuc2_32bis.png)

Dopo la pubblicazione, puoi monitorare il percorso utilizzando gli strumenti di reporting dedicati per misurare l’efficacia del percorso.

![Report analisi Percorso con metriche e statistiche delle prestazioni](assets/jo-dynamic_report_journey_12.png)

Ulteriori informazioni sui report di percorso sono disponibili in questa [sezione](../reports/live-report.md).

## Casi d’uso comuni {#use-cases}

Non sei sicuro di dove iniziare? Di seguito sono riportati tre scenari tipici in cui i percorsi offrono il massimo valore:

<table style="table-layout:fixed">
  <tr style="border: 0;">
    <td>
      <a href="https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/use-cases/customer-onboarding" target="_blank">
        <img src="../assets/do-not-localize/icon-quick-start.svg">
      </a>
      <div><strong>Serie di benvenuto</strong><br/>Effettua automaticamente l'onboarding dei nuovi utenti con una sequenza di messaggi dopo l'iscrizione, guidandoli attraverso il prodotto o il servizio.</div>
    </td>
    <td>
      <a href="https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/use-cases/abandoned-cart" target="_blank">
        <img src="../assets/do-not-localize/icon-campaign.svg">
      </a>
      <div><strong>Abbandono del carrello</strong><br/>Rivolgiti ai clienti che hanno lasciato il carrello senza completare l'acquisto inviando un promemoria puntuale con contenuti personalizzati.</div>
    </td>
    <td>
      <a href="jo-use-cases.md">
        <img src="../assets/do-not-localize/icon-content.svg">
      </a>
      <div><strong>Nuovo coinvolgimento</strong><br/>Ripristina gli utenti inattivi con offerte o aggiornamenti mirati in base all'ultimo comportamento noto.</div>
    </td>
  </tr>
  <tr style="border: 0;">
    <td align="center"><a href="https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/use-cases/customer-onboarding" target="_blank"><img src="../assets/do-not-localize/learn-more-button.svg"></a></td>
    <td align="center"><a href="https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/use-cases/abandoned-cart" target="_blank"><img src="../assets/do-not-localize/learn-more-button.svg"></a></td>
    <td align="center"><a href="jo-use-cases.md"><img src="../assets/do-not-localize/learn-more-button.svg"></a></td>
  </tr>
</table>

## Risorse aggiuntive

* **[Panoramica di Progettazione Percorsi](using-the-journey-designer.md)** - Eseguire il master dell&#39;interfaccia dell&#39;area di lavoro del percorso per progettare e orchestrare percorsi di clienti.
* **[Attività di Percorso](about-journey-activities.md)** - Scopri tutte le attività disponibili, inclusi eventi, azioni e componenti di orchestrazione.
* **[Verifica dei percorsi](testing-the-journey.md)** - Scopri come eseguire il test dei percorsi utilizzando la modalità di test prima di pubblicare in produzione.
* **[percorsi di pubblicazione](publish-journey.md)** - Comprendere il processo di pubblicazione del percorso e come gestire i percorsi live.
* **[Rapporti sui Percorsi](report-journey.md)** - Tieni traccia e analizza le prestazioni del percorso con metriche e informazioni dettagliate.
* **[Risoluzione dei problemi dei percorsi](troubleshooting.md)** - Trova soluzioni ai problemi comuni del percorso e alle best practice per il debug.
* **[Esercitazioni Percorso](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/journeys/introduction-to-building-a-journey){target="_blank"}** - Esplora esercitazioni video dettagliate sulla creazione di percorsi e sulle best practice.

