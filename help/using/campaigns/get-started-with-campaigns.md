---
title: Introduzione alle campagne
description: Ulteriori informazioni sulle campagne in [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: e2506a43-e4f5-48af-bd14-ab76c54b7c90
source-git-commit: d747cc9a4d065ea9110cb8065c113326959e2a41
workflow-type: tm+mt
source-wordcount: '488'
ht-degree: 4%

---

# Introduzione alle campagne {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="campaigns_list"
>title="Campagne"
>abstract="Crea campagne per distribuire contenuti una tantum a un segmento specifico su vari canali. Prima di creare la campagna, accertati di avere una superficie del canale (ad es. un messaggio preimpostato) e un segmento Adobe Experience Platform pronto per l’uso."

Utilizza le campagne Journey Optimizer per distribuire contenuti una tantum a un segmento specifico utilizzando vari canali. Quando si utilizzano i percorsi, le azioni sono progettate per essere eseguite in sequenza. Con le campagne, le azioni vengono eseguite simultaneamente, immediatamente o in base a una pianificazione specifica.

Crea campagne per inviare semplici comunicazioni batch ad hoc per casi di utilizzo di marketing come offerte promozionali, campagne di coinvolgimento, annunci, avvisi legali o aggiornamenti di policy.

➡️ [Scopri questa funzione nel video](#video)

<!--You can create two types of campaigns:

* **Scheduled campaigns** allow for simple ad-hoc batch communications for marketing use cases like promotional offers, engagement campaigns, announcements, legal notices, or policy updates.
* **API Triggered Campaigns** allow for simple transactional/operational messages with REST APIs (password reset, card abandonment, etc.), where the need may involve personalization using profile attributes and contextual data from payload.-->

## Prima di iniziare {#campaign-prerequisites}

Prima di iniziare a creare la prima campagna in Journey Optimizer, verifica i seguenti prerequisiti:

1. **Sono necessarie autorizzazioni adeguate**. Le campagne sono disponibili solo per gli utenti con accesso a una campagna correlata **[!UICONTROL Product profile]** come l’amministratore di Campaign, l’approvatore di Campaign, il manager di Campaign e/o il visualizzatore di Campaign. Se non riesci ad accedere alle campagne, devi estendere le tue autorizzazioni. Se hai accesso a [Adobe Admin Console](https://adminconsole.adobe.com/){target=&quot;_blank&quot;} per la tua organizzazione, segui i passaggi seguenti. In caso contrario, contattare l&#39;amministratore Journey Optimizer.

+++Scopri come assegnare le autorizzazioni della campagna

Per assegnare il corrispondente **[!UICONTROL Product profile]** agli utenti:

1. Da [!DNL Admin console], seleziona [!DNL Adobe Experience Platform] prodotto.

1. Da **[!UICONTROL Product profile]** seleziona una delle schede integrate relative a Campaign **[!UICONTROL Product profile]**: Amministratore di Campaign, approvatore di Campaign, manager di Campaign o visualizzatore di Campaign.

   Per ulteriori informazioni sulla campagna Journey Optimizer **[!UICONTROL Product profiles]** e **[!UICONTROL Permissions]**, [fai riferimento a questa pagina](../administration/ootb-product-profiles.md).

   ![](assets/do-not-localize/admin_1.png)

1. Fai clic su **[!UICONTROL Add user]** per assegnare all&#39;utente il **[!UICONTROL Product profile]**.

   ![](assets/do-not-localize/admin_2.png)

1. Digita il nome utente, il gruppo o l’indirizzo e-mail e fai clic su **[!UICONTROL Save]**.

L’utente potrà ora accedere a **[!UICONTROL Campaigns]**.

+++

1. **Hai bisogno di un pubblico**. I segmenti di pubblico devono essere disponibili prima di creare la campagna. Ulteriori informazioni sulla creazione di un pubblico [in questa pagina](../segment/about-segments.md).
1. **È necessaria una superficie del canale**. Per poter selezionare un canale, è necessario che la superficie del canale corrispondente sia creata e disponibile. Ulteriori informazioni sulle superfici dei canali (ad esempio i predefiniti) [in questa pagina](../configuration/channel-surfaces.md)

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

## Video introduttivo {#video}

Scopri come creare la tua prima campagna.

>[!VIDEO](https://video.tv.adobe.com/v/346680?quality=12)
