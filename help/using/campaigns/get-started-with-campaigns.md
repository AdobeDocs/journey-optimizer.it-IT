---
title: Introduzione alle campagne
description: Ulteriori informazioni sulle campagne in [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: 6177a33edeb3b8381c3eb5609762b4d974dc93e3
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 8%

---


# Introduzione alle campagne {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="campaigns_list"
>title="Campagne"
>abstract="Con Campagne è possibile distribuire contenuti una tantum a un segmento specifico su più canali. Prima di creare una nuova campagna, accertati di disporre di un predefinito per messaggi e di un segmento Adobe Experience Platform pronto per l’uso."

## Informazioni sulle campagne {#about}

Le campagne consentono di inviare contenuti una tantum a un segmento specifico utilizzando più canali. A differenza dei percorsi, in cui le azioni sono progettate per essere eseguite in sequenza, le campagne vengono eseguite simultaneamente, immediatamente o su una pianificazione specifica.

Puoi creare due tipi di campagne:

* **Campagne pianificate** consentono comunicazioni batch semplici ad hoc per casi d’uso di marketing come offerte promozionali, campagne di coinvolgimento, annunci, avvisi legali o aggiornamenti dei criteri.
* **Campagne attivate dall’API** consenti messaggi operativi/transazionali semplici con API REST (reimpostazione della password, abbandono della scheda, ecc.), dove la necessità di personalizzare utilizzando gli attributi del profilo e i dati contestuali dal payload.

Scopri come utilizzare le campagne:
* [Creare una campagna](create-campaign.md)
* [Creare campagne con attivazione API](api-triggered-campaigns.md)
* [Modificare o interrompere una campagna](modify-stop-campaign.md)
* [Rapporto live della campagna](campaign-live-report.md)
* [Rapporto globale della campagna](campaign-global-report.md)

## Accedere alle campagne {#access}

Le campagne sono accessibili dal **[!UICONTROL Campaigns]** menu.

Per impostazione predefinita, l’elenco mostra tutte le campagne con **[!UICONTROL Draft]**, **[!UICONTROL Scheduled]** e **[!UICONTROL Live]** stati. Per visualizzare le campagne interrotte, completate e archiviate, devi cancellare il filtro.

![](assets/create-campaign-list.png)

## Stati di Campaign {#statuses}

Le campagne possono avere più stati:

* **[!UICONTROL Draft]**: La campagna è in corso di modifica e non è stata attivata.
* **[!UICONTROL Activating]**: È in corso l’attivazione della campagna.
* **[!UICONTROL Live]**: La campagna è stata attivata.
* **[!UICONTROL Scheduled]**: La campagna è stata configurata per essere attivata in una data di inizio specifica.
* **[!UICONTROL Stopped]**: La campagna è stata arrestata manualmente. Non è più possibile attivarlo o riutilizzarlo (vedi [Interrompere una campagna](modify-stop-campaign.md#stop))
* **[!UICONTROL Completed]**: La campagna è completa.
* **[!UICONTROL Archived]**: La campagna è stata archiviata.

>[!NOTE]
>
>Icona &quot;Apri versione bozza&quot; accanto a una **[!UICONTROL Live]** o **[!UICONTROL Scheduled]** lo stato indica che è stata creata una nuova versione della campagna e che non è ancora stata attivata (vedi [Modificare una campagna](modify-stop-campaign.md#modify)).
