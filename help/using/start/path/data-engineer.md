---
solution: Journey Optimizer
product: journey optimizer
title: Guida introduttiva di Journey Optimizer per l’ingegnere dati
description: In qualità di ingegnere dati, scopri di più su come utilizzare Journey Optimizer
feature: Get Started
role: Developer
level: Intermediate
exl-id: 8beaafc2-e68d-46a1-be5c-e70892575bfb
source-git-commit: 5ff7987c00afda3263cb97654967c5b698f726c2
workflow-type: tm+mt
source-wordcount: '806'
ht-degree: 52%

---

# Guida introduttiva per l’ingegnere dati {#data-engineer}

In qualità di **Adobe Journey Optimizer Data Engineer**, devi preparare e gestire i dati del profilo cliente per potenziare le esperienze orchestrate da [!DNL Journey Optimizer], modellare i dati di clienti e aziende negli schemi e configurare i connettori di origine per l&#39;acquisizione dei dati. Una volta che l’[amministratore di sistema](administrator.md) ti avrà concesso l’accesso e avrà preparato il tuo ambiente, puoi iniziare a lavorare con [!DNL Adobe Journey Optimizer].

>[!NOTE]
>
>Ulteriori informazioni sull’**acquisizione dei dati** nella [documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html?lang=it){target="_blank"}.

## Passaggi fondamentali per la configurazione dei dati

Segui questi passaggi per configurare la base dati per Journey Optimizer:

1. **Creare spazi dei nomi di identità**. In Adobe [!DNL Journey Optimizer], le **Identità** collegano i consumatori tra dispositivi e canali creando un grafico delle identità. Il grafico delle identità collegato viene utilizzato per personalizzare le esperienze in base alle interazioni tra tutti i punti di contatto aziendali. Ulteriori informazioni su identità e spazi dei nomi di identità sono disponibili [in questa pagina](../../audience/get-started-identity.md).

   Inoltre, configura **identificatori supplementari** per abilitare lo stesso profilo per immettere più istanze di percorso in base a identificatori secondari come ID ordine o ID prenotazione. Scopri [identificatori supplementari](../../building-journeys/supplemental-identifier.md).

1. **Creare schemi** e abilitarli per i profili. Uno schema è un set di regole che rappresentano e convalidano la struttura e il formato dei dati. In pratica, gli schemi forniscono una definizione astratta di un oggetto reale (ad esempio una persona) e delineano i dati da includere in ogni istanza di tale oggetto (ad esempio nome, cognome, compleanno e così via).

   * Per percorsi e campagne standard: utilizza [schemi XDM](../../data/get-started-schemas.md)
   * Per le campagne orchestrate: crea [schemi relazionali](../../orchestrated/gs-schemas.md) per abilitare la segmentazione con più entità

1. **Crea set di dati** e abilitali per i profili. Un set di dati è un costrutto di archiviazione e gestione per una raccolta di dati, in genere una tabella, che contiene uno schema (colonne) e dei campi (righe). I set di dati contengono anche metadati che descrivono vari aspetti dei dati memorizzati. Una volta creato un set di dati, puoi mapparlo su uno schema esistente e aggiungervi dati. Ulteriori informazioni sui set di dati sono disponibili [in questa pagina](../../data/get-started-datasets.md).

   Per scenari avanzati, prepara **set di dati per le ricerche runtime** per arricchire l&#39;esecuzione del percorso con dati in tempo reale da set di dati record. Scopri [ricerca set di dati](../../building-journeys/dataset-lookup.md).

1. **Configurare i connettori di origine**. Adobe Journey Optimizer consente l’acquisizione di dati da fonti esterne e allo stesso tempo di strutturare, etichettare e migliorare i dati in entrata utilizzando i servizi di Platform. È possibile acquisire dati da diverse origini, ad esempio applicazioni Adobe, archivi basati su cloud, database e molte altre. Ulteriori informazioni sui connettori di origine sono disponibili [in questa pagina](../get-started-sources.md).

1. **Creare profili di test**. I profili di test sono necessari quando si utilizza la [modalità di test](../../building-journeys/testing-the-journey.md) in un percorso e per [visualizzare in anteprima e verificare i messaggi](../../content-management/preview-test.md) prima di inviarli. I passaggi per creare i profili di test sono descritti [in questa pagina](../../audience/creating-test-profiles.md).

1. **Configurare gli attributi calcolati** (facoltativo). Crea attributi derivati dai dati del profilo per semplificare la segmentazione e la personalizzazione. Gli attributi calcolati calcolano automaticamente metriche complesse come &quot;acquisti totali negli ultimi 90 giorni&quot; o &quot;valore medio dell’ordine&quot;. Scopri gli [attributi calcolati](../../audience/computed-attributes.md).

Inoltre, per poter inviare messaggi in percorsi, devi configurare **[!UICONTROL Origini dati]**, **[!UICONTROL Eventi]** e **[!UICONTROL Azioni]**. Per ulteriori informazioni, consulta [questa sezione](../../configuration/about-data-sources-events-actions.md).

![](../assets/admin-menu.png)

* La configurazione dell‘**origine dati** consente di definire una connessione a un sistema per il recupero di informazioni aggiuntive le quali verranno utilizzate nei percorsi. Per ulteriori informazioni sulle origini dati, consulta [questa sezione](../../datasource/about-data-sources.md).

* **Eventi** ti consente di attivare i tuoi percorsi in modo unitario per inviare messaggi in tempo reale all’utente che entra nel percorso. Nella configurazione dell’evento, puoi configurare gli eventi previsti nei percorsi. I dati degli eventi in arrivo vengono normalizzati seguendo Adobe Experience Data Model (XDM). Gli eventi provengono dalle API di acquisizione in streaming per gli eventi autenticati e non autenticati, ad esempio gli eventi SDK di Adobe Mobile. Per ulteriori informazioni sugli eventi, consulta [questa sezione](../../event/about-events.md).

* [!DNL Journey Optimizer] viene fornito con funzionalità per i messaggi incorporate: puoi creare i messaggi all’interno di un percorso e progettare il contenuto. Se per l’invio di messaggi utilizzi un sistema di terze parti, ad esempio Adobe Campaign, è possibile creare un‘**azione personalizzata**. Ulteriori informazioni sulle azioni [sono disponibili in questa sezione](../../action/action.md).

## Monitorare e analizzare i dati del percorso

Una volta che i percorsi sono in esecuzione, puoi eseguire query sugli eventi dei passaggi del percorso nel Data Lake per monitorare le prestazioni, risolvere i problemi e analizzare il comportamento dei clienti. Utilizzare le query SQL per analizzare:

* Modelli di entrata e uscita profilo
* Tassi di errore e motivi di eliminazione
* Prestazioni processo di esportazione Read Audience
* Metriche delle prestazioni delle azioni personalizzate
* Stati e colli di bottiglia dell&#39;istanza di percorso

Esplora gli esempi di query pronti all&#39;uso [per l&#39;analisi dei percorsi](../../reports/query-examples.md) per iniziare a utilizzare l&#39;analisi dei dati e la risoluzione dei problemi.

## Rimani aggiornato

Tenere il passo con le funzionalità e i miglioramenti più recenti di Journey Optimizer:

* **[Note sulla versione](../../rn/release-notes.md)**: rivedi le nuove funzioni, i miglioramenti e le correzioni rilasciati ogni mese
* **[Aggiornamenti alla documentazione](../../rn/documentation-updates.md)**: tieni traccia delle modifiche recenti apportate alla documentazione, inclusi nuove pagine e contenuto aggiornato
* **Notifiche prodotto**: abilita le notifiche nel tuo [profilo Adobe Experience Cloud](https://experience.adobe.com/preferences){target="_blank"} per ricevere avvisi su:
   * Nuove versioni del prodotto e funzioni
   * Finestre di manutenzione e aggiornamenti del sistema
   * Annunci e modifiche importanti

  Per abilitare le notifiche, fai clic sull&#39;icona del tuo profilo in alto a destra di Adobe Experience Cloud, vai a **Preferenze > Notifiche** e configura le preferenze per le notifiche Journey Optimizer.
