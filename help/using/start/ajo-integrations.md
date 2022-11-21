---
solution: Journey Optimizer
product: journey optimizer
title: Integrare con altre soluzioni
description: Ulteriori informazioni su come integrare Journey Optimizer con altre soluzioni
topic: Content Management
role: User
level: Intermediate
exl-id: 700dc66e-ae2d-418f-b75e-ece15af57ab3
source-git-commit: 90d7d4d39fe04198707be3d5b24888cfe5bed308
workflow-type: tm+mt
source-wordcount: '580'
ht-degree: 5%

---

# Integrare con altre soluzioni {#integration}

Con Adobe Journey Optimizer puoi gestire, conservare ed esportare facilmente questi dati in piattaforme o sistemi che fanno parte dello stack di tecnologia. Queste integrazioni consentono di risolvere casi d’uso specifici e di estendere l’ambito funzionale di Adobe Journey Optimizer.

>[!NOTE]
>
> Basato su Adobe Experience Platform, Adobe Journey Optimizer è connesso nativamente a [Profilo cliente in tempo reale di Adobe](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=it){target=&quot;_blank&quot;}. Questa origine dati incorporata è preconfigurata ed è progettata per recuperare e utilizzare i dati dal Profilo cliente in tempo reale (ad esempio, verifica se la persona che ha inserito un percorso è un cliente o meno). Ti consente di utilizzare i dati Profilo e i dati Eventi esperienza. [Ulteriori informazioni](../datasource/adobe-experience-platform-data-source.md).

## Adobe Customer Journey Analytics{#integration-cja}

Puoi utilizzare Customer Journey Analytics per eseguire analisi avanzate sui dati generati da Journey Optimizer.

Journey Optimizer memorizza i dati in Adobe Experience Platform e con il Customer Journey Analytics fornisce una visualizzazione olistica di tutti i tuoi percorsi, campagne e offerte con distribuzione automatizzata dei rapporti e visualizzazioni personalizzate dei dati.

Dopo aver creato il percorso in Journey Optimizer, il Customer Journey Analytics può acquisire dati dalla piattaforma per avviare rapporti e comprendere l’impatto di ogni interazione che un cliente ha con i tuoi percorsi.

Ulteriori informazioni [Journey Optimizer + Customer Journey Analytics](../reports/cja-ajo.md).

## Adobe Analytics{#integration-aa}

Puoi sfruttare tutti i dati dell’evento comportamentale di Adobe Analytics che stai già acquisendo e trasferendo in Adobe Experience Platform per attivare percorsi in tempo reale e automatizzare le esperienze per i tuoi clienti. Questi dati possono essere utilizzati anche per creare segmenti che possono essere coinvolti utilizzando Journey Optimizer.

Ulteriori informazioni [Journey Optimizer + Analytics](../event/about-analytics.md).

## Adobe Intelligent Services{#integration-intelligent-service}

I servizi intelligenti Adobe nativi di Real Time Customer Data Platform ti consentono di sfruttare la potenza dell’intelligenza artificiale e dell’apprendimento automatico nei casi d’uso della customer experience. Questo consente agli analisti di marketing di impostare previsioni specifiche per le esigenze di un’azienda utilizzando configurazioni a livello di business senza la necessità di competenze scientifiche in materia di dati.

Customer AI consente ai marchi di creare punteggi basati sull’apprendimento automatico di abbandono o conversione che saranno disponibili come attributi di profilo in Adobe Experience Platform e che possono essere utilizzati per personalizzare un percorso.

[Ulteriori informazioni](../building-journeys/ai-services-overview.md).


## Adobe Campaign{#integration-ac}

È disponibile un’integrazione se disponi di Adobe Campaign v7 o v8. Utilizza questa integrazione per inviare e-mail, notifiche push e SMS utilizzando le funzionalità di messaggistica transazionale di Adobe Campaign.

Ulteriori informazioni [Journey Optimizer + Campaign](../building-journeys/ajo-ac.md).

Puoi anche impostare un’integrazione con Adobe Campaign Standard per l’invio di messaggi nei tuoi percorsi.

Ulteriori informazioni [Journey Optimizer + Campaign Standard](../building-journeys/ajo-ac.md).

## Canali personalizzati{#integration-custom}

Se utilizzi un sistema di terze parti per l’invio di messaggi o se desideri che i percorsi inviino chiamate API a un sistema di terze parti, utilizza azioni personalizzate per connettersi al percorso. Ad esempio, è possibile connettersi ai seguenti sistemi con azioni personalizzate: Epsilon, Slack, [Adobe Developer](https://developer.adobe.com/){target=&quot;_blank&quot;}, Firebase, ecc.

Le azioni personalizzate sono azioni aggiuntive definite dagli utenti tecnici e rese disponibili agli addetti al marketing. Una volta configurati, vengono visualizzati nella palette a sinistra del percorso nella **[!UICONTROL Azione]** categoria. Per ulteriori informazioni, consulta [questa pagina](../building-journeys/about-journey-activities.md#action-activities).

Ulteriori informazioni [azioni personalizzate](../action/about-custom-action-configuration.md).

## Origini dati esterne{#integration-external-systems}

Journey Optimizer consente di configurare connessioni a sistemi esterni tramite origini dati personalizzate e azioni personalizzate. Questo ti consente, ad esempio, di arricchire i tuoi percorsi con i dati provenienti da un sistema di prenotazione esterno.

Scopri come utilizzare le origini dati esterne per definire una connessione a un sistema di terze parti in [questa sezione](../datasource/external-data-sources.md).
