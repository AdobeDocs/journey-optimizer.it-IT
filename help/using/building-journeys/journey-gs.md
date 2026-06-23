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
TQID: https://experienceleague.adobe.com/7zNDOi2SUTyttgR6I1iOYQb61ejxpqLYznweU8alnPw
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: ad78185d-8f79-40ad-9bad-cbde74af74eeid: b3538224-471e-4c63-a444-9b19d89ae29cid: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: b15c7c2e-788c-4eb7-86a8-390565b0d2c9id: a6c67b0d-bd3e-4d5d-95a8-882e3709d632
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5520579-b31f-4df7-9281-f0d9f91e2edcid: c1579802-ddd4-4214-8a91-97b2066abe11id: d00e9f03-e50b-4162-b143-0c0817c937c2id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 0bbbbf94550d4cb762ecca300932620c8d3da50e
workflow-type: tm+mt
source-wordcount: 2143
ht-degree: 8%

---

# Creare il primo percorso {#jo-quick-start}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri i passaggi chiave per creare il tuo primo percorso in Adobe Journey Optimizer, dalla definizione del pubblico o dell&#39;evento di ingresso all&#39;aggiunta di azioni e alla pubblicazione in tempo reale.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_homepage_card2"
>title="Creare i percorsi"
>abstract="**[!DNL Adobe Journey Optimizer]** crea casi di utilizzo di orchestrazione in tempo reale utilizzando dati contestuali archiviati in eventi o origini dati."

>[!CONTEXTUALHELP]
>id="ajo_journey_create"
>title="Percorsi"
>abstract="I percorsi di clienti offrono esperienze personalizzate e contestuali. Journey Optimizer consente di creare casi d’uso di orchestrazione in tempo reale sfruttando i dati contestuali archiviati negli eventi o nelle origini dati. La scheda **Panoramica** visualizza una dashboard con metriche chiave relative ai percorsi. La scheda **Sfoglia** presenta l’elenco dei percorsi esistenti."

[!DNL Adobe Journey Optimizer] include un&#39;area di lavoro di orchestrazione omnicanale che consente agli addetti marketing di armonizzare l&#39;attività di marketing con il coinvolgimento dei clienti uno a uno. L’interfaccia utente ti consente di trascinare facilmente le attività dalla palette all’interno dell’area di lavoro per creare il percorso. L&#39;interfaccia utente del percorso è descritta in [questa pagina](journey-ui.md).

![esempio di area di lavoro percorso](assets/journey38.png)

I passaggi principali per la creazione di un percorso sono descritti in questa pagina. Sono semplificate come segue:

![Passaggi per la creazione del percorso: creazione, progettazione, test e pubblicazione](assets/journey-creation-process.png)

In questa guida:

* Definire un punto di ingresso percorso: un segmento di pubblico o un evento in tempo reale
* Aggiungi azioni messaggio tra i canali: e-mail, push, SMS, in-app, web, esperienza basata su codice, scheda di contenuto e altro ancora. [Visualizza canali supportati](journey-action.md)
* Verifica il percorso con i profili di test prima dell’attivazione
* Pubblicare il percorso e monitorarne le prestazioni

Crea percorsi di clienti in più passaggi per avviare in tempo reale una sequenza di interazioni, offerte e messaggi tra i canali. Questo approccio assicura il coinvolgimento dei clienti nei momenti ottimali in base alle loro azioni e ai segnali di business rilevanti.

<!--
>[!TIP]
>
>Not sure whether to use a journey or a campaign? [Learn how to choose the right approach](../start/journeys-vs-campaigns.md).
-->

## Prima di iniziare {#prerequisites}

Ciò che devi configurare prima di creare dipende da come viene attivato il percorso. La maggior parte dei percorsi inizia da uno dei due punti di ingresso seguenti:

* **Voce basata su pubblico**: il percorso viene eseguito per un set definito di profili in un orario pianificato. [Crea un pubblico](../audience/about-audiences.md) in Adobe Experience Platform prima di creare il percorso. Questo è il punto di partenza consigliato se hai poca esperienza con Journey Optimizer.

* **Voce basata su eventi**: il percorso viene attivato in tempo reale quando un utente esegue un&#39;azione, ad esempio un acquisto o un abbonamento. [Configura un evento](../event/about-events.md) per definire il trigger e i dati che contiene.

**Non sei sicuro del punto di ingresso da utilizzare?** La tabella seguente mappa i casi d’uso più comuni all’attività iniziale corretta.

| Punto di ingresso | Usa quando... | I profili entrano |
|---|---|---|
| **[Read Audience](read-audience.md)** | Desideri inviare un messaggio pianificato o ricorrente a un set definito di profili (newsletter, promozioni, serie di onboarding). | Tutti i profili di un pubblico batch, in una sola volta o secondo una pianificazione. |
| **[Qualificazione del pubblico](audience-qualification-events.md)** | Devi reagire in tempo reale quando un profilo entra o esce da un pubblico (aggiornamento del livello fedeltà, flag di rischio di abbandono). | Un profilo alla volta, non appena si qualificano in un pubblico in streaming. |
| **Evento unitario** | Un’azione profilo attiva una risposta immediata (conferma di acquisto, invio di moduli, accesso all’app). | Un profilo alla volta, in tempo reale. |
| **[Evento di business](../event/about-creating-business.md)** | Un evento non relativo al profilo interessa più persone contemporaneamente (cancellazione del volo, rifornimento di scorte, avviso di ultime notizie). | Tutti i profili associati all’evento tramite un passaggio Read Audience automatico. |

I seguenti elementi sono facoltativi, ma possono essere richiesti a seconda del caso d’uso:

* **Origine dati**: per arricchire le condizioni di percorso o la personalizzazione con i dati di un sistema esterno, impostare un&#39;origine dati [](../datasource/about-data-sources.md).

* **Azione personalizzata**: se recapiti messaggi tramite un sistema di terze parti anziché tramite i canali incorporati, configura [azione personalizzata](../action/action.md).

>[!NOTE]
>
>* Se sei un ingegnere dati responsabile della configurazione tecnica (eventi, origini dati e azioni), consulta [questa sezione](../configuration/about-data-sources-events-actions.md).
>
>* I guardrail e le limitazioni del percorso sono descritti in dettaglio in [questa pagina](../start/guardrails.md).

## Creare un percorso {#jo-build}

Per creare un percorso con più passaggi, effettuare le seguenti operazioni:

1. Nella sezione del menu GESTIONE PERCORSO fare clic su **[!UICONTROL Percorsi]**.

1. Fare clic sul pulsante **[!UICONTROL Crea Percorso]** per creare un nuovo percorso.

1. Modificate il riquadro di configurazione del percorso per definire il nome del percorso e impostarne le proprietà. Scopri come impostare le proprietà del percorso in [questa pagina](journey-properties.md).

   >[!TIP]
   >
   >**Quale tipo di percorso scegliere?** Se hai poca esperienza con Journey Optimizer, inizia con un percorso basato sul pubblico utilizzando un&#39;attività **[!UICONTROL Read Audience]**, non richiede alcuna configurazione precedente dell&#39;evento ed è il modo più semplice per acquisire familiarità con l&#39;area di lavoro. Per esperienze in tempo reale attivate da eventi (ad esempio, in risposta a un acquisto o all’invio di un modulo), configura prima un evento e utilizza una voce basata su eventi. Sei pronto ad approfondire? [Scopri tutti i tipi di percorso e le relative regole di ingresso](entry-management.md#types-of-journeys).

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

Dopo aver creato il percorso, testarlo prima di pubblicarlo. Journey Optimizer offre una **modalità di test** per visualizzare i profili di test mentre si spostano lungo il percorso, rilevando potenziali errori prima dell&#39;attivazione. L’esecuzione di test rapidi garantisce il corretto funzionamento dei percorsi, in modo da consentirne la pubblicazione sicura. Scopri come testare il percorso [ in questa sezione](testing-the-journey.md)

Puoi anche eseguire il percorso in **Dry run**. La prova del percorso è una modalità speciale di pubblicazione di un percorso in Adobe Journey Optimizer che consente ai professionisti del percorso di poterne effettuare un test, utilizzando dati di produzione reali e senza la necessità di contattare la clientela reale o aggiornare le informazioni di profilo. Questa funzione aiuta i professionisti del percorso ad acquisire maggiore sicurezza rispetto alla progettazione di un percorso e al targeting del pubblico, prima della pubblicazione effettiva. Scopri come pubblicare un percorso in modalità di esecuzione a secco [in questa sezione](journey-dry-run.md).

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
        <img src="../assets/do-not-localize/icon-quick-start.svg" width="35px">
      </a>
      <div><strong>Serie di benvenuto</strong><br/>Effettua automaticamente l'onboarding dei nuovi utenti con una sequenza di messaggi dopo l'iscrizione, guidandoli attraverso il prodotto o il servizio.</div>
    </td>
    <td>
      <a href="https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/use-cases/abandoned-cart" target="_blank">
        <img src="../assets/do-not-localize/icon-campaign.svg" width="35px">
      </a>
      <div><strong>Abbandono del carrello</strong><br/>Rivolgiti ai clienti che hanno lasciato il carrello senza completare l'acquisto inviando un promemoria puntuale con contenuti personalizzati.</div>
    </td>
    <td>
      <a href="jo-use-cases.md">
        <img src="../assets/do-not-localize/icon-content.svg" width="35px">
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

* **[Tipi di Percorso e voce di profilo](entry-management.md)** - Comprendi tutti i tipi di percorso (evento unitario, evento di business, pubblico di lettura, qualificazione del pubblico) e il modo in cui i profili entrano, entrano di nuovo e scorrono nei percorsi.
* **[Panoramica di Progettazione Percorsi](using-the-journey-designer.md)** - Eseguire il master dell&#39;interfaccia dell&#39;area di lavoro del percorso per progettare e orchestrare percorsi di clienti.
* **[Attività di Percorso](about-journey-activities.md)** - Scopri tutte le attività disponibili, inclusi eventi, azioni e componenti di orchestrazione.
* **[Verifica dei percorsi](testing-the-journey.md)** - Scopri come eseguire il test dei percorsi utilizzando la modalità di test prima di pubblicare in produzione.
* **[percorsi di pubblicazione](publish-journey.md)** - Comprendere il processo di pubblicazione del percorso e come gestire i percorsi live.
* **[Rapporti sui Percorsi](report-journey.md)** - Tieni traccia e analizza le prestazioni del percorso con metriche e informazioni dettagliate.
* **[Risoluzione dei problemi dei percorsi](troubleshooting.md)** - Trova soluzioni ai problemi comuni del percorso e alle best practice per il debug.
* **[Esercitazioni Percorso](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/journeys/introduction-to-building-a-journey){target="_blank"}** - Esplora esercitazioni video dettagliate sulla creazione di percorsi e sulle best practice.

+++ Guida di riferimento della Knowledge Base di AI

Questa sezione contiene informazioni strutturate che supportano l&#39;interpretazione, il recupero e la risposta alle domande relative a questo argomento.

Per una comprensione completa, queste informazioni devono essere unite alla documentazione su questa pagina. Nessuna delle due origini è progettata per essere indipendente; la pagina descrive la funzione, mentre questa sezione fornisce un contesto aggiuntivo che aiuta a non ambiguare la terminologia, le finalità, l’applicabilità e i vincoli.

* **TL;DR:** In questa pagina vengono illustrati i quattro passaggi chiave per la creazione di un primo percorso in Adobe Journey Optimizer, ovvero la definizione di un punto di ingresso, la progettazione dell&#39;area di lavoro, i test con la modalità di test o Dry run e la pubblicazione, insieme alle indicazioni per la scelta del tipo di voce corretto.

**Intenti:**
* Creare un nuovo percorso e configurarne le proprietà nel menu Gestione Percorso
* Scegli il punto di ingresso corretto (Read Audience, Audience Qualification, evento unitario o evento di business) per un dato caso d’uso
* Progettare un percorso in più passaggi trascinando eventi, attività di orchestrazione e azioni di canale sull’area di lavoro
* Testare un percorso utilizzando la simulazione, la modalità di test con profili di test AEP persistenti o l’esecuzione in prova prima della pubblicazione
* Esegui un’esecuzione in prova per convalidare il targeting del pubblico con dati di produzione reali senza contattare i clienti
* Pubblicare un percorso per renderlo live e monitorarne le prestazioni con strumenti di reporting

**Glossario:**
* **Read Audience**: attività di ingresso che elabora tutti i profili in un pubblico batch contemporaneamente o secondo una pianificazione *(specifico per prodotto)*
* **Qualificazione del pubblico**: un&#39;attività di ingresso attivata in tempo reale quando un profilo entra o esce da un pubblico in streaming *(specifico per prodotto)*
* **Evento unitario**: trigger in tempo reale che immette un profilo alla volta in un percorso quando si verifica un&#39;azione specifica *(specifico per prodotto)*
* **Evento di business**: un evento non di profilo (ad esempio, annullamento di un volo, rifornimento di scorte) che attiva un percorso per più profili contemporaneamente tramite un passaggio automatico Read Audience *(specifico per prodotto)*
* **Modalità di test**: una modalità di convalida che utilizza profili di test Adobe Experience Platform persistenti (contrassegnati in modo esplicito come profili di test) per attraversare un percorso bozza prima della pubblicazione *(specifico per prodotto)*
* **Simulazione**: una modalità di convalida che utilizza utenti simulati temporanei generati al volo; gli utenti simulati non persistono in Adobe Experience Platform *(specifico per prodotto)*
* **Esecuzione in prova**: una modalità di pubblicazione speciale che utilizza dati di produzione reali per convalidare la logica di percorso senza contattare i clienti effettivi o aggiornare i profili *(specifici del prodotto)*

**Guardrail:**
* Impossibile pubblicare un percorso se contiene errori. È necessario risolvere tutti gli errori
* La configurazione dell’evento (per l’immissione basata su eventi) deve essere completata da un tecnico dati prima che il percorso possa essere generato
* I guardrail e le limitazioni del percorso sono documentati separatamente e devono essere rivisti prima della progettazione su larga scala
* La creazione di tipi di pubblico in Adobe Experience Platform è un prerequisito per i percorsi basati sul pubblico

**Terminologia:**
* Nome canonico: Percorso — Acronimo: none — varianti: percorso del cliente, flusso di orchestrazione
* Sinonimi: &quot;Modalità di prova&quot; = &quot;Test percorso&quot;; &quot;Esecuzione a secco&quot; = &quot;Modalità di esecuzione a secco&quot;
* Non confondere: &quot;Simulazione&quot; ≠ &quot;Modalità di test&quot; ≠ &quot;Esecuzione in prova&quot; — La simulazione utilizza utenti simulati temporanei; la modalità di test utilizza profili di test AEP persistenti; l’esecuzione in prova utilizza dati di produzione reali senza contattare i clienti o aggiornare i profili

**Domande frequenti:**
* **D: qual è la prima cosa da fare prima di creare un percorso attivato da eventi?** — Configurare l&#39;evento con un data engineer per definire l&#39;attivatore e i dati che porta con sé; quindi fare riferimento all&#39;evento come punto di ingresso del percorso.
* **Q: quale punto di ingresso è consigliato per un nuovo utente di Journey Optimizer?** un percorso basato sul pubblico che utilizza un’attività Read Audience. Non richiede alcuna configurazione di evento precedente ed è il modo più semplice per acquisire familiarità con l’area di lavoro.
* **Q: posso testare il mio percorso prima che diventi attivo?** — Sì; utilizza la simulazione con utenti simulati temporanei, la modalità di test con profili di test AEP persistenti o l’esecuzione in prova per eseguire l’esecuzione su dati di produzione reali senza inviare comunicazioni.
* **D: cosa succede se il mio percorso presenta errori quando tento di pubblicare?** — Non è possibile pubblicare un percorso con errori; tutti gli errori di configurazione devono essere risolti prima della pubblicazione.
* **D: come posso interrompere un percorso complesso con molti passaggi?** utilizzo dell&#39;attività Salta per collegare percorsi secondari più piccoli, riducendo la complessità e rendendo più semplice il test indipendente di ciascun percorso secondario.

+++
