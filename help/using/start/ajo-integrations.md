---
solution: Journey Optimizer
product: journey optimizer
title: Integrazione con altre soluzioni
description: Ulteriori informazioni su come integrare Journey Optimizer con altre soluzioni
feature: Integrations
role: User
level: Intermediate
exl-id: 700dc66e-ae2d-418f-b75e-ece15af57ab3
source-git-commit: 4899dbe71243184b6283a32a4fe7eb2edb82f872
workflow-type: tm+mt
source-wordcount: '715'
ht-degree: 98%

---

# Integrazione con altre soluzioni {#integration}

Con Adobe Journey Optimizer puoi gestire, conservare ed esportare facilmente questi dati in piattaforme o sistemi che fanno parte dello stack tecnologico. Queste integrazioni consentono di risolvere casi d’uso specifici e di estendere l’ambito funzionale di Adobe Journey Optimizer.

>[!NOTE]
>
> Basato su Adobe Experience Platform, Adobe Journey Optimizer è connesso in modalità nativa al [Profilo cliente in tempo reale di Adobe](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=it){target="_blank"}. Questa origine dati incorporata è preconfigurata ed è progettata per recuperare e utilizzare i dati dal Profilo cliente in tempo reale (ad esempio, verificare se la persona che ha inserito un percorso è un cliente oppure no). Consente di utilizzare i dati del Profilo e i dati di Eventi esperienza. [Maggiori informazioni](../datasource/adobe-experience-platform-data-source.md).
>

## Adobe Customer Journey Analytics {#integration-cja}

Puoi utilizzare Customer Journey Analytics per eseguire analisi avanzate sui dati generati da Journey Optimizer.

Journey Optimizer archivia i dati in Adobe Experience Platform e con Customer Journey Analytics fornisce una vista olistica di tutti i tuoi percorsi, campagne e offerte con distribuzione dei rapporti automatizzata e visualizzazioni personalizzate dei dati.

Dopo aver creato il percorso in Journey Optimizer, Customer Journey Analytics può acquisire dati dalla piattaforma per avviare rapporti e comprendere l’impatto di ogni interazione di un cliente con i tuoi percorsi.

Ulteriori informazioni su [Journey Optimizer + Customer Journey Analytics](../reports/cja-ajo.md).

## Adobe Analytics {#integration-aa}

Puoi sfruttare tutti i dati dell’evento comportamentale di Adobe Analytics che già acquisisci e trasferisci in Adobe Experience Platform per attivare i percorsi in tempo reale e automatizzare le esperienze per i clienti. Questi dati possono essere utilizzati anche per creare tipi di pubblico da coinvolgere utilizzando Journey Optimizer.

Ulteriori informazioni su [Journey Optimizer + Analytics](../event/about-analytics.md).


## Adobe Experience Manager Assets {#integration-assets}

Riunisci flussi di lavoro creativi e di marketing utilizzando [!DNL Adobe Experience Manager Assets]. Integrato in modo nativo con [!DNL Adobe Journey Optimizer], accedi a [!DNL Adobe Experience Manager Assets] per archiviare, gestire, individuare e distribuire le risorse digitali. Fornisce un archivio di risorse unico e centralizzato da utilizzare per compilare i messaggi.

[!DNL Adobe Experience Manager Assets] è accessibile direttamente da [!DNL Adobe Journey Optimizer] tramite la sezione **[!UICONTROL Risorse]** del menu a sinistra.

Ulteriori informazioni su [JOURNEY OPTIMIZER + ADOBE EXPERIENCE MANAGER ASSETS](../content-management/assets.md).


## Adobe Stock {#integration-stock}

Il plug-in per l’integrazione di E-mail designer di [!DNL Adobe Stock] e [!DNL Adobe Journey Optimizer] offre ai clienti un modo semplice per cercare le immagini da utilizzare nella creazione dei messaggi, acquistarne la licenza e salvarle.

Con [!DNL Adobe Journey Optimizer], puoi caricare le immagini nelle e-mail direttamente da [!DNL Adobe Stock] e aggiungerle alla cartella **[!UICONTROL Risorse]** utilizzando l’opzione **[!UICONTROL Trova le foto di Adobe Stock]**. Inoltre, l’opzione **[!UICONTROL Trova foto Stock simili]** consente di trovare immagini che corrispondono al contenuto, al colore e alla composizione della risorsa utilizzata nella consegna.

Ulteriori informazioni su [Journey Optimizer + Stock](../content-management/stock.md).


## Adobe Intelligent Services {#integration-intelligent-service}

Adobe Intelligent Services che sono servizi nativi di Real Time Customer Data Platform ti consentono di sfruttare la potenza dell’intelligenza artificiale e dell’apprendimento automatico nei casi d’uso dell’esperienza del cliente. Questo consente agli analisti di marketing di impostare previsioni specifiche per le esigenze di un’azienda utilizzando configurazioni a livello aziendale senza la necessità di competenze in materia di data science.

L’IA per l’analisi dei clienti consente ai marchi di creare punteggi basati sull’apprendimento automatico di abbandono o conversione che saranno disponibili come attributi di profilo in Adobe Experience Platform e che possono essere utilizzati per personalizzare un percorso.

[Ulteriori informazioni](../building-journeys/ai-services-overview.md).


## Adobe Campaign {#integration-ac}

Se si dispone di Adobe Campaign v7 o v8, è disponibile un’integrazione. Questa integrazione può essere utilizzata per inviare e-mail, notifiche push e SMS tramite le funzionalità di messaggistica transazionale di Adobe Campaign.

Ulteriori informazioni su [Journey Optimizer + Campaign](../building-journeys/ajo-ac.md).

Per inviare i messaggi nei percorsi, è possibile anche impostare un’integrazione con Adobe Campaign Standard.

Ulteriori informazioni su [Journey Optimizer + Campaign Standard](../building-journeys/using-adobe-campaign-standard.md).

## Canali personalizzati {#integration-custom}

Se utilizzi un sistema di terze parti per l’invio di messaggi o se desideri che i percorsi inviino chiamate API a un sistema di terze parti, utilizza azioni personalizzate per connettersi al tuo percorso. Ad esempio, mediante azioni personalizzate è possibile connettersi ai seguenti sistemi: Epsilon, Slack, [Adobe Developer](https://developer.adobe.com){target="_blank"}, Firebase, ecc.

Le azioni personalizzate sono azioni aggiuntive definite dagli utenti tecnici e rese disponibili agli esperti di marketing. Una volta configurate, vengono visualizzate nella palette a sinistra del percorso nella categoria **[!UICONTROL Azione]**. Per ulteriori informazioni, consulta [questa pagina](../building-journeys/about-journey-activities.md#action-activities).

Ulteriori informazioni sulle [azioni personalizzate](../action/about-custom-action-configuration.md).

## Origini dati esterne {#integration-external-systems}

Journey Optimizer consente di configurare connessioni a sistemi esterni tramite origini dati e azioni personalizzate. Questo ti consente, ad esempio, di arricchire i tuoi percorsi con i dati provenienti da un sistema di prenotazione esterno.

Scopri come utilizzare le origini dati esterne per definire una connessione a un sistema di terze parti in [questa sezione](../datasource/external-data-sources.md).
