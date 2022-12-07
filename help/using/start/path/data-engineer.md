---
solution: Journey Optimizer
product: journey optimizer
title: Guida introduttiva di Journey Optimizer per l’ingegnere dati
description: In qualità di ingegnere dati, scopri di più su come utilizzare Journey Optimizer
level: Intermediate
exl-id: 8beaafc2-e68d-46a1-be5c-e70892575bfb
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '580'
ht-degree: 100%

---

# Guida introduttiva per l’ingegnere dati {#data-engineer}

Come **ingegnere dati di Adobe Journey Optimizer**, devi preparare e gestire i dati del profilo cliente per potenziare le esperienze orchestrate da [!DNL Journey Optimizer], modellare i dati di clienti e aziende negli schemi e configurare i connettori origine per l’acquisizione dei dati. Una volta che l’[amministratore di sistema](administrator.md) ti avrà concesso l’accesso e avrà preparato il tuo ambiente, puoi iniziare a lavorare con [!DNL Adobe Journey Optimizer].


Scopri come **identificare dati e creare schemi e set di dati** per inserire i dati in Adobe Experience Platform in questa pagina.

>[!NOTE]
>
>Ulteriori informazioni sull’**acquisizione dei dati** nella [documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html?lang=it){target=&quot;_blank&quot;}.

I passaggi per creare uno spazio dei nomi delle identità, un set di dati abilitati per i profili e i profili di test sono descritti nelle sezioni seguenti:

1. **Creare uno spazio dei nomi di identità**. In Adobe [!DNL Journey Optimizer], le **Identità** collegano i consumatori tra dispositivi e canali creando un grafico delle identità. Il grafico delle identità collegato viene utilizzato per personalizzare le esperienze in base alle interazioni tra tutti i punti di contatto aziendali.  Per ulteriori informazioni su identità e spazio dei nomi delle identità, consulta [questa pagina](../../segment/get-started-identity.md).

1. **Creare uno schema** e abilitarlo per i profili. Uno schema è un set di regole che rappresentano e convalidano la struttura e il formato dei dati. A un livello avanzato, gli schemi forniscono una definizione astratta di un oggetto reale (ad esempio una persona) e delineano quali dati includere in ogni istanza di tale oggetto (ad esempio nome, cognome, compleanno e così via).  Per ulteriori informazioni sugli schemi, consulta [questa pagina](../../data/get-started-schemas.md).

1. **Creare set di dati** e abilitarli per i profili. Un set di dati è un costrutto di archiviazione e gestione per una raccolta di dati, in genere una tabella, che contiene uno schema (colonne) e dei campi (righe). I set di dati contengono anche metadati che descrivono vari aspetti dei dati memorizzati. Una volta creato un set di dati, puoi mapparlo su uno schema esistente e aggiungervi dati. Per ulteriori informazioni sui set di dati, consulta [questa pagina](../../data/get-started-datasets.md).

1. **Configurare i connettori di origine**. Adobe Journey Optimizer consente di acquisire dati da origini esterne e allo stesso tempo di strutturare, etichettare e migliorare i dati in arrivo tramite i servizi Platform. È possibile acquisire dati da diverse origini, ad esempio applicazioni Adobe, archivi basati su cloud, database e molte altre. Per ulteriori informazioni sui connettori di origine, consulta [questa pagina](../get-started-sources.md).

1. **Creare profili di test**. I profili di test sono necessari quando si utilizza la [modalità di test](../../building-journeys/testing-the-journey.md) in un percorso e per [visualizzare in anteprima e verificare i messaggi](../../email/preview.md) prima di inviarli. I passaggi per creare i profili di test sono descritti in dettaglio [in questa pagina](../../segment/creating-test-profiles.md).


Inoltre, per poter inviare messaggi nei percorsi, devi configurare **[!UICONTROL Origini dati]**, **[!UICONTROL Eventi]** e **[!UICONTROL Azioni]**. Per ulteriori informazioni, consulta [questa sezione](../../configuration/about-data-sources-events-actions.md).

![](../assets/admin-menu.png)

* La configurazione dell‘**origine dati** consente di definire una connessione a un sistema per il recupero di informazioni aggiuntive le quali verranno utilizzate nei percorsi. Per ulteriori informazioni sulle origini dati, consulta [questa sezione](../../datasource/about-data-sources.md).

* **Eventi** ti consente di attivare i tuoi percorsi in modo unitario per inviare messaggi in tempo reale all’utente che entra nel percorso. Nella configurazione dell’evento, puoi configurare gli eventi previsti nei percorsi. I dati degli eventi in arrivo vengono normalizzati seguendo Adobe Experience Data Model (XDM). Gli eventi provengono dalle API Streaming Ingestion (acquisizione dati in streaming) per gli eventi autenticati e non autenticati, ad esempio gli eventi SDK di Adobe Mobile. Per ulteriori informazioni sugli eventi, consulta [questa sezione](../../event/about-events.md).

* [!DNL Journey Optimizer] viene fornito con funzionalità per i messaggi incorporate: puoi creare i messaggi all’interno di un percorso e progettare il contenuto. Se per l’invio di messaggi utilizzi un sistema di terze parti, ad esempio Adobe Campaign, è possibile creare un‘**azione personalizzata**. Per ulteriori informazioni sulle azioni, consulta [questa sezione](../../action/action.md).
