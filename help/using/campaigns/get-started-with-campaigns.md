---
title: Introduzione alle campagne
description: Ulteriori informazioni sulle campagne in [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: e2506a43-e4f5-48af-bd14-ab76c54b7c90
source-git-commit: 711fdf1dce0688d2e21d405a4e3e8777612b2f3b
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 3%

---

# Introduzione alle campagne {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="campaigns_list"
>title="Campagne"
>abstract="Con Campagne è possibile distribuire contenuti una tantum a un segmento specifico su più canali. Prima di creare una nuova campagna, accertati di disporre di una superficie del canale (ad es. un messaggio preimpostato) e di un segmento Adobe Experience Platform pronto per l’uso."

## Informazioni sulle campagne {#about}

>[!IMPORTANT]
>
>Questa funzione è disponibile solo per gli utenti con accesso a un profilo di prodotto relativo a Campaign, come l’amministratore di Campaign, l’approvatore di Campaign, il manager di Campaign e/o il visualizzatore di Campaign. Per ulteriori informazioni su come assegnare i profili di prodotto, consulta [questa pagina](../administration/permissions.md).

Le campagne consentono di inviare contenuti una tantum a un segmento specifico utilizzando più canali. A differenza dei percorsi, in cui le azioni sono progettate per essere eseguite in sequenza, le campagne vengono eseguite simultaneamente, immediatamente o su una pianificazione specifica.

Questo consente di inviare semplici comunicazioni batch ad hoc per casi di utilizzo del marketing come offerte promozionali, campagne di coinvolgimento, annunci, avvisi legali o aggiornamenti dei criteri.

<!--You can create two types of campaigns:

* **Scheduled campaigns** allow for simple ad-hoc batch communications for marketing use cases like promotional offers, engagement campaigns, announcements, legal notices, or policy updates.
* **API Triggered Campaigns** allow for simple transactional/operational messages with REST APIs (password reset, card abandonment, etc.), where the need may involve personalization using profile attributes and contextual data from payload.-->

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
* **[!UICONTROL Completed]**: La campagna è completa. Questo stato viene assegnato automaticamente 3 giorni dopo l’attivazione di una campagna oppure alla data di fine della campagna, se presenta un’esecuzione ricorrente.
* **[!UICONTROL Archived]**: La campagna è stata archiviata.

>[!NOTE]
>
>Icona &quot;Apri versione bozza&quot; accanto a una **[!UICONTROL Live]** o **[!UICONTROL Scheduled]** lo stato indica che è stata creata una nuova versione della campagna e che non è ancora stata attivata (vedi [Modificare una campagna](modify-stop-campaign.md#modify)).
