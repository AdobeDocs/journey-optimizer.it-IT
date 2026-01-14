---
solution: Journey Optimizer
product: journey optimizer
title: Introduzione ai connettori di origine in Journey Optimizer
description: Scopri come acquisire dati da origini esterne in Adobe Journey Optimizer
feature: Integrations, Data Ingestion
role: User
level: Beginner
exl-id: 359ea3c6-7746-469e-8a24-624f9726f2d8
source-git-commit: 7864012ad148c2e52bc38598016e7bd7fac9644e
workflow-type: ht
source-wordcount: '584'
ht-degree: 100%

---

# Introduzione ai connettori di origine {#sources-gs}

## Che cosa è un’origine? {#what-is-source}

Un’**origine** è un connettore che porta dati esterni in Adobe Journey Optimizer. Le origini consentono di importare le informazioni sulla clientela dai sistemi già in uso, ad esempio piattaforme CRM, archiviazione cloud o database, e di rendere tali dati disponibili per la creazione di percorsi cliente personalizzati.

Considera le origini come ponti tra Journey Optimizer e i sistemi di dati esterni. Sincronizzano automaticamente i dati in modo da disporre sempre di informazioni aggiornate sulla clientela per alimentare le campagne di marketing.

## Perché le origini sono importanti {#why-sources-matter}

Le origini sono essenziali per la creazione di esperienze cliente personalizzate e basate sui dati in Journey Optimizer. Ecco il perché:

* **Vista della clientela unificata**: combina dati provenienti da più sistemi per visualizzare il quadro completo di ciascun cliente
* **Personalizzazione in tempo reale**: utilizza dati aggiornati per inviare messaggi tempestivi e rilevanti nei percorsi
* **Sincronizzazione automatizzata dei dati**: mantieni aggiornate le informazioni del cliente senza importare manualmente i dati
* **Flussi di lavoro efficienti**: connettiti una volta, poi i dati fluiranno automaticamente nei percorsi

Ad esempio, puoi utilizzare le origini per importare la cronologia degli acquisti dalla piattaforma di e-commerce, quindi creare percorsi che inviano consigli di prodotti personalizzati in base a ciò che la clientela ha acquistato.

## Cosa puoi fare con le origini {#sources-use-cases}

I casi d’uso comuni per le origini in Journey Optimizer includono:

* **Importare dati cliente da sistemi CRM**: sincronizza informazioni di contatto, preferenze e cronologia del coinvolgimento da piattaforme come Salesforce o Microsoft Dynamics
* **Collegare dati di acquisto**: importa la cronologia degli ordini e le preferenze dei prodotti dalle piattaforme di e-commerce per personalizzare le offerte
* **Integrare i dati del programma fedeltà**: accedi al saldo dei punti e alle informazioni sul livello raggiunto per premiare la clientela più coinvolta
* **Sincronizzare dati comportamentali**: importa interazioni con siti web e pattern di utilizzo delle app per attivare percorsi rilevanti
* **Aggiornare attributi profilo**: mantieni aggiornati i profili della clientela con dati provenienti da archiviazione cloud o database

## Tipi di origini comuni {#source-types}

Journey Optimizer supporta diversi tipi di origini per la connessione con i sistemi esistenti:

**Applicazioni di Adobe:**
* Adobe Analytics
* Adobe Audience Manager
* Adobe Campaign
* Adobe Commerce

**Archiviazione cloud:**
* Amazon S3
* Archiviazione BLOB di Azure
* Google Cloud Storage
* SFTP

**Database:**
* Amazon Redshift
* Google BigQuery
* Microsoft SQL Server
* MySQL
* PostgreSQL

**Automazione del marketing e CRM:**
* Microsoft Dynamics
* Salesforce
* Salesforce Marketing Cloud

➡️ Consulta l’elenco completo nel [catalogo origini Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/sources/home.html?lang=it#sources-catalog){target="_blank"}

## Prima di iniziare {#prerequisites}

Prima di configurare le origini, assicurati di disporre di:

* **Autorizzazioni appropriate**: accesso alla gestione delle origini in Adobe Experience Platform
* **Credenziali del sistema di origine**: dettagli di autenticazione per il sistema esterno che desideri connettere
* **Comprensione dei dati**: conoscere di quali campi dati necessiti e come mapparli ai profili Journey Optimizer

➡️ Scopri il [controllo degli accessi e delle autorizzazioni](../administration/permissions.md)

## Come funzionano le origini {#how-sources-work}

Adobe Journey Optimizer utilizza il framework delle origini di Adobe Experience Platform. Di seguito è riportato il flusso di lavoro di base:

1. **Connetti**: configura l’autenticazione per il sistema dati esterno
2. **Seleziona dati**: scegli quali dati importare e con quale frequenza sincronizzare
3. **Mappa campi**: definisci come i campi dati esterni corrispondono agli attributi del profilo di Journey Optimizer
4. **Pianifica**: configura intervalli di aggiornamento automatico dei dati
5. **Monitora**: tieni traccia del flusso di dati e risolvi eventuali problemi di sincronizzazione

Una volta configurate, le origini vengono eseguite automaticamente in background, mantenendo i dati cliente aggiornati e pronti per l’uso in percorsi.

## Ulteriori informazioni {#learn-more}

![](assets/sources-home.png)

Guarda questo video per comprendere i connettori di origine e come configurarli in Journey Optimizer:

>[!VIDEO](https://video.tv.adobe.com/v/3422584?captions=ita&quality=12)

Per informazioni dettagliate sulla configurazione e la gestione delle origini, consulta la [documentazione sulle origini di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/sources/home.html?lang=it){target="_blank"}.

## Passaggi successivi {#next-steps}

Ora che comprendi cosa sono le origini e il motivo per cui sono importanti:

* Esplora il [catalogo origini](https://experienceleague.adobe.com/docs/experience-platform/sources/home.html?lang=it#sources-catalog){target="_blank"} per trovare i connettori per i sistemi
* Scopri come [creare una connessione di origine](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/overview.html?lang=it){target="_blank"}
* Comprendi la [trasformazione e la mappatura dei dati](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/dataflow/overview.html?lang=it){target="_blank"}
* Scopri come [utilizzare i dati importati in percorsi](../building-journeys/journey-gs.md)
