---
solution: Journey Optimizer
product: journey optimizer
title: Configurare dispositivi mobili e web
description: Scopri come configurare e monitorare i canali web e per dispositivi mobili
feature: Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: canale, superficie, tecnico, parametri, ottimizzatore
exl-id: 846e0d11-798b-4f3b-80db-848a17d32830
source-git-commit: f916d91ffd2c41261612f2127f35c41275c9d013
workflow-type: tm+mt
source-wordcount: '770'
ht-degree: 100%

---

# Introduzione alla configurazione guidata del canale {#set-mobile-config}

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_name"
>title="Nome configurazione per dispositivi mobili e web"
>abstract="Immetti il nome della configurazione mobile o web. Questo nome verrà utilizzato per ogni risorsa creata automaticamente con la Configurazione guidata del canale."

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_validate_assurance"
>title="Convalidare con Assurance"
>abstract="Adobe Experience Platform Assurance è incorporato in questo flusso di lavoro per aiutarti a controllare l’implementazione dell’SDK e a simulare e convalidare gli eventi dell’applicazione."
>additional-url="https://experienceleague.adobe.com/it/docs/experience-platform/assurance/home" text="Panoramica di Adobe Experience Platform Assurance"

Questa configurazione facilita la configurazione rapida dei canali di marketing, garantendo che tutte le risorse richieste siano prontamente disponibili in Experience Platform, Journey Optimizer e Raccolta dati. Questo consente al team di marketing di iniziare la creazione di campagne e percorsi.

La configurazione guidata del canale supporta le seguenti piattaforme e canali.

* Piattaforme e SDK:

   * Swift di Apple, iOS

   * Kotlin, Android

   * JavaScript, Web

* Canali:

   * In-app per dispositivi mobili

   * Messaggio push per dispositivo mobile

   * Base web


Tieni presente che per ogni piattaforma da configurare è necessario creare una configurazione separata. Questo perché ogni applicazione richiede una configurazione dei canali specifica, offrendo la flessibilità di stabilire i canali desiderati per ciascuna piattaforma.

## Prerequisiti {#prereq}

* Per implementare in modo efficace questa impostazione, è essenziale che un membro dell’organizzazione con l’autorità e la capacità tecnica di modificare il codice di un sito web o di un dispositivo mobile supervisioni la configurazione.

  Di seguito sono riportate le autorizzazioni necessarie per eseguire la configurazione guidata del canale.

  +++ Autorizzazioni richieste

  <table>
    <thead>
      <tr>
        <th><strong>Soluzione</strong></th>
        <th><strong>Autorizzazioni</strong></th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>
          <p>Raccolta dati</p>
        </td>
        <td>
          <ul>
            <li>Diritti dell’azienda &gt; Proprietà</li>
            <li>Diritti di proprietà: sviluppare, pubblicare, gestire estensioni e ambienti</li>
            <li>Superfici app: gestire la configurazione dell’app</li>
         </ul>
        </td>
      </tr>
      <tr>
        <td>
          <p>Adobe Experience Platform</p>
        </td>
        <td>
        <ul>
            <li>Raccolta dati: gestire gli stream di dati</li>
           <li>Sandbox: concedere l’accesso alle sandbox</li>
            <li>Gestione dei segmenti: leggere, creare, modificare ed eliminare le definizioni dei segmenti</li>
            <li>Gestione dei profili: leggere, creare, modificare ed eliminare i profili</li>
            <li>Lettura dei set di dati: accesso di sola lettura ai set di dati</li>
            <li>Lettura degli schemi: accesso di sola lettura agli schemi</li>
            <li>Lettura dello spazio dei nomi identità: accesso di sola lettura allo spazio dei nomi identità</li>
          </ul>
        </td>
      </tr>
      <tr>
        <td>
         <p>Adobe Journey Optimizer</p>
        </td>
        <td>
          <p>Campagne: gestire e pubblicare le campagne</p>
        </td>
      </tr>
    </tbody>
  </table>

  +++

* Se utilizzi l’opzione di configurazione esistente, assicurati di utilizzare le seguenti versioni dell’estensione Adobe Experience Platform Mobile SDK. Per ulteriori dettagli sulla configurazione dell’SDK, incluse le dipendenze richieste e il codice di inizializzazione, consulta la [seguente documentazione](https://experienceleague.adobe.com/it/docs/platform-learn/implement-mobile-sdk/app-implementation/install-sdks).

  Per Android

   * Mobile Core v3.1.0 o versione successiva
   * Adobe Journey Optimizer v3.1.0 o versione successiva

  Per iOS

   * Mobile Core v5.2.0 o versione successiva
   * Adobe Journey Optimizer v5.1.1 o versione successiva

## Risorse create automaticamente {#auto-create-resources}

La configurazione guidata del canale semplifica la configurazione rapida dei canali di marketing, rendendo immediatamente disponibili tutte le risorse essenziali nelle app Experience Platform, Journey Optimizer e Data Collection. Questo consente al team di marketing di iniziare rapidamente a creare campagne e percorsi. Di seguito è riportato un elenco delle risorse generate e configurate automaticamente come parte della configurazione guidata del canale.

Sfoglia le schede di seguito per accedere agli elenchi completi di tutte le risorse generate automaticamente:

>[!BEGINTABS]

>[!TAB iOS]

Per la **configurazione iniziale**, di seguito è riportato un elenco completo di tutte le risorse create nella schermata **Dettagli configurazione** quando si fa clic su **Crea automaticamente le risorse**.

<table>
  <thead>
  <tr>
  <th><strong>Soluzione</strong></th>
  <th><strong>Risorse create automaticamente</strong></th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td>
  <p>Tag</p>
  </td>
  <td>
  <ul>
  <li>Proprietà tag Mobile</li>
  <li>Regole</li>
  <li>Elementi dati</li>
  <li>Libreria</li>
  <li>Ambienti (staging, produzione, sviluppo)</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>Estensioni tag</p>
  </td>
  <td>
  <ul>
  <li>Adobe Experience Platform Edge Network</li>
  <li>Adobe Journey Optimizer</li>
  <li>AEP Assurance</li>
  <li>Consent (con i criteri di consenso predefiniti abilitati)</li>
  <li>Identità (con ECID predefinito, con regole di unione predefinite)</li>
  <li>Mobile Core</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>Assurance</p>
  </td>
  <td>
  <p>Sessione Assurance</p>
  </td>
  </tr>
  <tr>
  <td>
  <p>Stream di dati</p>
  </td>
  <td>
  <p>Stream di dati con servizi</p>
  </td>
  </tr>
  <tr>
  <td>
  <p>Experience Platform</p>
  </td>
  <td>
  <ul>
  <li>Set di dati</li>
  <li>Schema</li>
  </ul>
  </td>
  </tr>
  </tbody>
  </table>

Per la **Configurazione canale**, di seguito è riportato un elenco completo di tutte le risorse create nella schermata **Aggiungi canali**.

<table>
  <thead>
  <tr>
  <th><strong>Soluzione</strong></th>
  <th><strong>Risorse create automaticamente</strong></th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td>
  <p>Journey Optimizer</p>
  </td>
  <td>
  <ul>
  <li>Configurazione dei canali</li>
  <li>Caricare credenziali push (solo messaggi push per dispositivi mobili)</li>
  </ul>
  </td>
  </tr>
  </tbody>
  </table>

>[!TAB Android]

Per la **Configurazione iniziale**, di seguito è riportato un elenco completo di tutte le risorse create nella schermata **Dettagli di configurazione** quando si fa clic su **Crea automaticamente le risorse**.

<table>
  <thead>
  <tr>
  <th><strong>Soluzione</strong></th>
  <th><strong>Risorse create automaticamente</strong></th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td>
  <p>Tag</p>
  </td>
  <td>
  <ul>
  <li>Proprietà tag Mobile</li>
  <li>Regole</li>
  <li>Elementi dati</li>
  <li>Libreria</li>
  <li>Ambienti (staging, produzione, sviluppo)</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>Estensioni tag</p>
  </td>
  <td>
  <ul>
  <li>Adobe Experience Platform Edge Network</li>
  <li>Adobe Journey Optimizer</li>
  <li>AEP Assurance</li>
  <li>Consent (con i criteri di consenso predefiniti abilitati)</li>
  <li>Identità (con ECID predefinito, con regole di unione predefinite)</li>
  <li>Mobile Core</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>Assurance</p>
  </td>
  <td>
  <p>Sessione Assurance</p>
  </td>
  </tr>
  <tr>
  <td>
  <p>Stream di dati</p>
  </td>
  <td>
  <p>Stream di dati con servizi</p>
  </td>
  </tr>
  <tr>
  <td>
  <p>Experience Platform</p>
  </td>
  <td>
  <ul>
  <li>Set di dati</li>
  <li>Schema</li>
  </ul>
  </td>
  </tr>
  </tbody>
  </table>

Per la **Configurazione canale**, di seguito è riportato un elenco completo di tutte le risorse create nella schermata **Aggiungi canali**.

<table>
  <thead>
  <tr>
  <th><strong>Soluzione</strong></th>
  <th><strong>Risorse create automaticamente</strong></th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td>
  <p>Journey Optimizer</p>
  </td>
  <td>
  <ul>
  <li>Configurazione dei canali</li>
  <li>Caricare credenziali push (solo messaggi push per dispositivi mobili)</li>
  </ul>
  </td>
  </tr>
  </tbody>
  </table>

>[!TAB Web]

Per la **Configurazione iniziale**, di seguito è riportato un elenco completo di tutte le risorse create nella schermata **Dettagli di configurazione** quando si fa clic su **Crea automaticamente le risorse**.

<table>
  <thead>
  <tr>
  <th><strong>Soluzione</strong></th>
  <th><strong>Risorse create automaticamente</strong></th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td>
  <p>Tag</p>
  </td>
  <td>
  <ul>
  <li>Proprietà tag Mobile</li>
  <li>Regole</li>
  <li>Elementi dati</li>
  <li>Libreria</li>
  <li>Ambienti (staging, produzione, sviluppo)</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>Estensioni tag</p>
  </td>
  <td>
  <ul>
  <li>Adobe Experience Platform Edge Network</li>
  <li>Adobe Journey Optimizer</li>
  <li>AEP Assurance</li>
  <li>Consent (con i criteri di consenso predefiniti abilitati)</li>
  <li>Identità (con ECID predefinito, con regole di unione predefinite)</li>
  <li>Mobile Core</li>
  </ul>
  </td>
  </tr>
  <tr>
  <td>
  <p>Assurance</p>
  </td>
  <td>
  <p>Sessione Assurance</p>
  </td>
  </tr>
  <tr>
  <td>
  <p>Stream di dati</p>
  </td>
  <td>
  <p>Stream di dati con servizi</p>
  </td>
  </tr>
  <tr>
  <td>
  <p>Experience Platform</p>
  </td>
  <td>
  <ul>
  <li>Set di dati</li>
  <li>Schema</li>
  </ul>
  </td>
  </tr>
  </tbody>
  </table>

>[!ENDTABS]

