---
title: Guida introduttiva di Journey Optimizer per data engineer
description: In qualità di data engineer, scopri di più su come lavorare con Journey Optimizer
level: Intermediate
exl-id: 8beaafc2-e68d-46a1-be5c-e70892575bfb
source-git-commit: f0c5b42984b76fee005fe0c0e10312d47f9d10e8
workflow-type: tm+mt
source-wordcount: '574'
ht-degree: 9%

---

# Introduzione per Data Engineer {#data-engineer}

![ingegnere informatico](assets/do-not-localize/user-1.png)

Come **Adobe Journey Optimizer Data Engineer**, preparare e gestire i dati del profilo cliente per potenziare le esperienze orchestrate da [!DNL Journey Optimizer], modella i dati di clienti e aziende negli schemi e configura i connettori sorgente per l’acquisizione dei dati. Puoi iniziare a lavorare con [!DNL Adobe Journey Optimizer] una volta che [Amministratore di sistema](administrator.md) ti ha concesso l&#39;accesso e preparato il tuo ambiente.


Scopri come **identificare dati e creare schema e set di dati** per inserire i dati in Adobe Experience Platform in questa pagina.

>[!NOTE]
>
>Ulteriori informazioni **inserimento dati** in [Documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html?lang=it){target=&quot;_blank&quot;}.

I passaggi per creare uno spazio dei nomi di identità e un set di dati abilitati per i profili e i profili di test sono descritti nelle sezioni seguenti:

1. **Creare uno spazio dei nomi di identità**. In Adobe [!DNL Journey Optimizer], **Identità** collega i consumatori tra dispositivi e canali, il risultato è un grafico dell&#39;identità. Il grafico dell’identità collegato viene utilizzato per personalizzare le esperienze in base alle interazioni tra tutti i punti di contatto aziendali.  Ulteriori informazioni su identità e namespace di identità [in questa pagina](../get-started-identity.md).

1. **Creare uno schema** e abilitalo per i profili. Uno schema è un insieme di regole che rappresentano e convalidano la struttura e il formato dei dati. Ad alto livello, gli schemi forniscono una definizione astratta di un oggetto reale (ad esempio una persona) e delineano quali dati includere in ogni istanza dell’oggetto (ad esempio nome, cognome, compleanno e così via).  Ulteriori informazioni sugli schemi [in questa pagina](../get-started-schemas.md).

1. **Creare set di dati** e abilitalo per i profili. Un set di dati è un costrutto di archiviazione e gestione per una raccolta di dati, in genere una tabella, che contiene uno schema (colonne) e campi (righe). I set di dati contengono anche metadati che descrivono vari aspetti dei dati memorizzati. Una volta creato un set di dati, puoi mapparlo su uno schema esistente e aggiungerlo. Ulteriori informazioni sui set di dati [in questa pagina](../get-started-datasets.md).

1. **Configurare i connettori di origine**. Adobe Percorsi Optimizer consente di acquisire dati da sorgenti esterne e allo stesso tempo di strutturare, etichettare e migliorare i dati in arrivo tramite i servizi Platform. È possibile acquisire dati da diverse sorgenti, come applicazioni di Adobe, archivi basati su cloud, database e molti altri. Ulteriori informazioni sui connettori sorgente [in questa pagina](../get-started-sources.md).

1. **Creare profili di test**. I profili di test sono necessari quando si utilizza il [modalità di prova](../building-journeys/testing-the-journey.md) in un percorso e [visualizzare in anteprima e verificare i messaggi](../preview.md) prima dell’invio. Scopri i passaggi per creare profili di test [in questa pagina](../../using/building-journeys/creating-test-profiles.md).


Inoltre, per poter inviare messaggi in percorsi, devi configurare **[!UICONTROL Data Sources]**, **[!UICONTROL Events]** e **[!UICONTROL Actions]**. [Ulteriori informazioni](../../using/configuration/about-data-sources-events-actions.md).

![](../assets/admin-menu.png)

* La **Origine dati** La configurazione ti consente di definire una connessione a un sistema per recuperare informazioni aggiuntive che verranno utilizzate nei tuoi percorsi. Ulteriori informazioni su Origini dati [in questa sezione](../datasource/about-data-sources.md).

* **Eventi** ti consente di attivare i tuoi percorsi singolarmente per inviare messaggi in tempo reale all’utente che entra nel percorso. Nella configurazione dell’evento, puoi configurare gli eventi previsti nei percorsi. I dati degli eventi in arrivo vengono normalizzati seguendo Adobe Experience Data Model (XDM). Gli eventi provengono dalle API Streaming Ingestion per gli eventi autenticati e non autenticati, ad esempio gli eventi SDK di Adobe Mobile. Ulteriori informazioni sugli eventi [in questa sezione](../event/about-events.md).

* [!DNL Journey Optimizer] include funzionalità integrate per messaggi: puoi progettare il contenuto e pubblicare il messaggio. Se utilizzi un sistema di terze parti per l’invio dei messaggi, ad esempio Adobe Campaign, crea un **azione personalizzata**. Ulteriori informazioni sulle azioni in questo [in questa sezione](../action/action.md).
