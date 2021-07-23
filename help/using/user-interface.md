---
title: Interfaccia utente
description: Interfaccia utente Journey Optimizer
feature: Panoramica
topic: Gestione dei contenuti
role: User
level: Intermediate
source-git-commit: ac6ba317909c962a81c7043bfa2a56e94bc5c9ad
workflow-type: tm+mt
source-wordcount: '1093'
ht-degree: 91%

---

# Interfaccia utente {#cjm-user-interface}

Una volta connesso ad [Adobe Experience Cloud](http://experience.adobe.com), passa a [!DNL Journey Optimizer].

>[!NOTE]
>
>* I concetti chiave della navigazione nell’interfaccia utente sono gli stessi di Adobe Experience Platform. Per ulteriori informazioni, consulta la [documentazione Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-ui/ui-guide.html#adobe-experience-platform-ui-guide){target=&quot;_blank&quot;} .
   >
   >
* Questa documentazione viene aggiornata spesso per riflettere le recenti modifiche all’interfaccia utente del prodotto. Tuttavia, alcune schermate possono risultare leggermente diverse dall’interfaccia del prodotto.
   >
   > 
* I componenti e le funzionalità disponibili nell’interfaccia utente dipendono dalle autorizzazioni e dal pacchetto di licenze. Per qualsiasi domanda, contatta il tuo Adobe Customer Success Manager.


## Pannello di navigazione a sinistra

Utilizza i collegamenti a sinistra per sfogliare le funzionalità.

![](assets/ajo-home.png)

>[!NOTE]
>
>Le funzionalità disponibili possono variare a seconda delle autorizzazioni e del contratto di licenza.

Di seguito è riportato l’elenco completo dei servizi e delle funzionalità disponibili nella barra a sinistra, con i collegamenti alla relativa documentazione.

**Home**

La pagina Home di [!DNL Journey Optimizer] contiene collegamenti e risorse chiave per iniziare. L’elenco **[!UICONTROL Recents]** fornisce collegamenti ai messaggi, agli eventi e ai percorsi creati o aggiornati di recente. Questo elenco mostra le relative date e lo stato di creazione e modifica.

**[!UICONTROL JOURNEY MANAGEMENT]**

* **[!UICONTROL Journeys]**: crea, configura e gestisci i percorsi dei clienti. [Ulteriori informazioni](building-journeys/journey-gs.md#jo-build)

* **[!UICONTROL Messages]**: crea, progetta, testa e pubblica e-mail e messaggi push. [Ulteriori informazioni](create-message.md)

**[!UICONTROL DECISION MANAGEMENT]**

* **[!UICONTROL Offers]**: accedi alle origini e ai set di dati recenti da questo menu. Usa questa sezione per creare nuove offerte. [Ulteriori informazioni](offers/offer-library/creating-personalized-offers.md)

* **[!UICONTROL Components]**: crea posizionamenti, regole e tag. [Ulteriori informazioni](offers/offer-library/key-steps.md)

**[!UICONTROL CONTENT MANAGEMENT]**

* **[!UICONTROL Assets]**: [!DNL Adobe Experience Manager Assets Essentials] è un archivio centralizzato di risorse che puoi utilizzare per compilare i messaggi. [Ulteriori informazioni](assets-essentials.md)

**[!UICONTROL DATA MANAGEMENT]**

* **[!UICONTROL Schemas]**: utilizza Adobe Experience Platform per creare e gestire gli schemi Experience Data Model (XDM) in un’area di lavoro visiva e interattiva, denominata Editor di schema. [Ulteriori informazioni](get-started-schemas.md)

* **[!UICONTROL Datasets]**: tutti i dati acquisiti in Adobe Experience Platform vengono mantenuti all’interno del Data Lake come set di dati. Un set di dati è un costrutto di archiviazione e gestione per una raccolta di dati, in genere una tabella, che contiene uno schema (colonne) e campi (righe). [Ulteriori informazioni](get-started-datasets.md)

* **[!UICONTROL Queries]**: utilizza Adobe Experience Platform Query Service per scrivere ed eseguire query, visualizzare le query eseguite in precedenza e accedere a quelle salvate dagli utenti della tua organizzazione. [Ulteriori informazioni](get-started-queries.md)

* **[!UICONTROL Monitoring]**: usa questo menu per monitorare l’inserimento dei dati nell’interfaccia utente di Adobe Experience Platform. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/experience-platform/ingestion/quality/monitor-data-ingestion.html?lang=it){target=&quot;_blank&quot;}

**[!UICONTROL CONNECTIONS]**

* **[!UICONTROL Sources]**: utilizza questo menu per acquisire i dati da diverse origini, ad esempio applicazioni Adobe, archivi basati su cloud, database e altro ancora, nonché per strutturare, etichettare e ottimizzare i dati in arrivo. [Ulteriori informazioni](get-started-sources.md)

**[!UICONTROL CUSTOMER]**

* **[!UICONTROL Segments]**: crea e gestisci le definizioni dei segmenti di Experience Platform per utilizzarle nei tuoi percorsi. [Ulteriori informazioni](segment/about-segments.md)

* **[!UICONTROL Profiles]**: la funzione Profilo cliente in tempo reale crea una visualizzazione olistica di ciascuno dei singoli clienti, combinando dati provenienti da più canali tra cui dati online, offline, del sistema CRM e di terze parti. [Ulteriori informazioni](get-started-profiles.md)

* **[!UICONTROL Identities]**: il servizio Adobe Experience Platform Identity gestisce l’identificazione dei clienti in tempo reale, tra dispositivi e canali diversi, in quello che viene definito un grafico di identità in Adobe Experience Platform. [Ulteriori informazioni](get-started-identity.md)

**[!UICONTROL ADMINISTRATION]**

* **[!UICONTROL Journey Administration]**: utilizza questo menu per configurare [eventi](event/about-events.md), [origini dati](datasource/about-data-sources.md) e [azioni](action/action.md) da utilizzare nei tuoi percorsi.

* **[!UICONTROL Sandboxes]**: Adobe Experience Platform fornisce ambienti sandbox che permettono di suddividere una singola istanza in ambienti virtuali separati, utili per le attività di sviluppo e aggiornamento delle applicazioni di esperienza digitale. [Ulteriori informazioni](administration/sandboxes.md)


## Casi d’uso accessibili dal prodotto

Sfrutta i casi d’uso di [!DNL Adobe Journey Optimizer] accessibili dalla pagina Home e fornisci alcuni dati per creare un percorso del cliente.

![](assets/use-cases-home.png)

I casi di utilizzo disponibili sono:

* **Creare profili di test**, per creare profili di test utilizzando il modello CSV per sperimentare messaggi e percorsi personalizzati. Scopri come implementare il caso d’uso [in questa pagina](building-journeys/creating-test-profiles.md#use-case-1).
* **Inviare un messaggio di compleanno ai clienti**, per inviare automaticamente un’e-mail ai clienti in occasione del loro compleanno. (disponibile a breve)
* **Inviare e-mail a bordo di nuovi clienti**, per inviare facilmente fino a due e-mail per dare il benvenuto ai clienti appena registrati. (disponibile a breve)
* **Inviare messaggi push a un elenco importato dei clienti**, per inviare rapidamente una notifica push a un elenco di clienti importati da un file CSV. (disponibile a breve)

Per ulteriori informazioni su ogni caso d’uso, fai clic su **[!UICONTROL View details]**.

Per iniziare il caso d’uso, fai clic sul pulsante **[!UICONTROL Begin]**.

Puoi accedere ai casi di utilizzo eseguiti dal pulsante **[!UICONTROL View use case library]**.

## Assistenza e supporto

Dalla sezione inferiore della pagina Home puoi accedere alle pagine importanti della guida di Adobe Journey Optimizer.

Utilizza l’icona **Aiuto** per accedere alle pagine della guida, contattare il supporto e condividere i tuoi commenti. Puoi cercare articoli e video di supporto dal campo di ricerca.

![](assets/ajo-help.png)

## Browser supportati

L’interfaccia di Adobe [!DNL Journey Optimizer] è progettata per funzionare in modo ottimale nell’ultima versione di Google Chrome. L’utilizzo di versioni precedenti o di altri browser potrebbe comportare problemi durante l’utilizzo di alcune funzioni.

## Preferenze di lingua

L’interfaccia utente è attualmente disponibile nelle seguenti lingue:

* Inglese
* Francese
* Tedesco

La lingua predefinita dell’interfaccia è determinata dalla lingua preferita specificata nel profilo utente.

Per cambiare lingua:

* Fai clic su **Preferenze** dal tuo avatar, in alto a destra.
   ![](assets/preferences.png)
* Quindi fai clic sulla lingua visualizzata sotto il tuo indirizzo e-mail
* Seleziona la lingua preferita e fai clic su **Salva**. Se il componente che utilizzi non è localizzato nella tua lingua, puoi selezionare una seconda lingua.
   ![](assets/select-language.png)

## Cerca

In qualsiasi punto dell’interfaccia di Adobe Journey Optimizer, utilizza la ricerca Adobe Experience Cloud al centro della barra superiore per trovare risorse, percorsi o messaggi nelle sandbox. Inizia a immettere il contenuto per visualizzare i risultati migliori.

![](assets/unified-search.png)

Premi **Invio** per accedere a tutti i risultati e filtrarli.

![](assets/search-and-filter.png)


## Filtrare gli elenchi{#section_lgm_hpz_pgb}

Nella maggior parte degli elenchi, una barra di ricerca consente di cercare un elemento specifico e selezionare i criteri di filtro.

Per accedere ai filtri, fai clic sulla relativa icona in alto a sinistra nell’elenco. Il menu dei filtri consente di filtrare gli elementi visualizzati in base a criteri diversi. Puoi scegliere di visualizzare solo gli elementi di un determinato tipo o stato, quelli che hai creato oppure quelli modificati negli ultimi 30 giorni. Le opzioni disponibili dipendono dal contesto.

Nell’elenco dei percorsi, è possibile filtrare i percorsi in base al loro stato, tipo e versione da **[!UICONTROL Status and version filters]**. Il tipo può essere: **[!UICONTROL Unitary event]**, **[!UICONTROL Segment qualification]**, **[!UICONTROL Read segment]**, **[!UICONTROL Business event]** o **[!UICONTROL Burst]**. Puoi scegliere di visualizzare solo i percorsi che utilizzano un dato evento, un gruppo di campi o un’azione particolare con le opzioni **[!UICONTROL Activity filters]** e **[!UICONTROL Data filters]**. La sezione **[!UICONTROL Publication filters]** consente di selezionare una data di pubblicazione o un utente. Ad esempio, puoi scegliere di visualizzare le versioni più recenti dei percorsi live pubblicati ieri. [Ulteriori informazioni](building-journeys/using-the-journey-designer.md).

>[!NOTE]
>
>Le colonne visualizzate possono essere personalizzate utilizzando il pulsante di configurazione, posto in alto a destra degli elenchi. La personalizzazione viene salvata per ogni utente.

Utilizza le colonne **[!UICONTROL Last update]** e **[!UICONTROL Last update by]** per verificare quando è avvenuto l’ultimo aggiornamento dei percorsi e chi l’ha salvato.

![](assets/filter-journeys.png)

Nei riquadri di configurazione dell’evento, dell’origine dati e dell’azione, il campo **[!UICONTROL Used in]** mostra il numero di percorsi che utilizzano quel particolare evento, gruppo di campi o azione. Per visualizzare l’elenco dei percorsi corrispondenti, puoi fare clic sul pulsante **[!UICONTROL View journeys]**.

![](assets/journey3bis.png)

All’interno dei vari elenchi, puoi eseguire le azioni di base su ciascun elemento. Ad esempio, è possibile duplicare o eliminare un elemento.

![](assets/journey4.png)
