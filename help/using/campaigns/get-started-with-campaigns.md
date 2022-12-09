---
solution: Journey Optimizer
product: journey optimizer
title: Guida introduttiva alle campagne
description: Ulteriori informazioni sulle campagne in [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: e2506a43-e4f5-48af-bd14-ab76c54b7c90
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 0%

---

# Guida introduttiva alle campagne {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="campaigns_list"
>title="Campagne"
>abstract="Crea campagne per distribuire contenuti una tantum a un segmento specifico su vari canali. Prima di creare la campagna, accertati di disporre di una superficie del canale (ad es. un messaggio preimpostato) e di un segmento Adobe Experience Platform pronto per l’uso."

Utilizza le campagne di Journey Optimizer per distribuire contenuti una tantum a un segmento specifico utilizzando vari canali. Quando utilizzi i percorsi, le azioni vengono eseguite in sequenza. Con le campagne, le azioni vengono eseguite simultaneamente, immediatamente o in base a una pianificazione specifica.

Puoi creare due tipi di campagne:

* **Campagne pianificate** consentono comunicazioni batch semplici ad hoc per casi d’uso di marketing come offerte promozionali, campagne di coinvolgimento, annunci, avvisi legali o aggiornamenti dei criteri.
* **Campagne attivate dall’API** consenti messaggi operativi/transazionali semplici con API REST (reimpostazione della password, abbandono della scheda, ecc.), dove la necessità di personalizzare utilizzando gli attributi del profilo e i dati contestuali dal payload.

I passaggi principali per creare una campagna sono i seguenti:

![](assets/create-campaign-process.png)

➡️ [Scopri questa funzione nel video](#video)

## Prima di iniziare {#campaign-prerequisites}

Verifica i seguenti prerequisiti prima di iniziare a creare la tua prima campagna in Journey Optimizer:

1. **Sono necessarie autorizzazioni adeguate**. Le campagne sono disponibili solo per gli utenti con accesso a una campagna correlata **[!UICONTROL Product profile]** come l’amministratore di Campaign, l’approvatore di Campaign, il manager di Campaign e/o il visualizzatore di Campaign.

   Se non riesci ad accedere alle campagne, devi estendere le tue autorizzazioni. Se hai accesso a [Adobe Admin Console](https://adminconsole.adobe.com/){target=&quot;_blank&quot;} per la tua organizzazione, segui i passaggi seguenti. In caso contrario, contatta l’amministratore di Journey Optimizer.

   +++Scopri come assegnare le autorizzazioni della campagna

   Per assegnare il corrispondente **[!UICONTROL Product profile]** agli utenti:

   1. Da [Adobe Admin Console](https://adminconsole.adobe.com/){target=&quot;_blank&quot;}, seleziona il [!DNL Adobe Experience Platform] prodotto.

   1. Sfoglia il **[!UICONTROL Product profile]** , seleziona una delle campagne integrate correlate **[!UICONTROL Product profile]**: Amministratore di Campaign, approvatore di Campaign, manager di Campaign o visualizzatore di Campaign.

      Per ulteriori informazioni sulla campagna di Journey Optimizer **[!UICONTROL Product profiles]** e **[!UICONTROL Permissions]**, [fai riferimento a questa pagina](../administration/ootb-product-profiles.md).

      ![](assets/do-not-localize/admin_1.png)

   1. Fai clic su **[!UICONTROL Add user]** per assegnare all&#39;utente il **[!UICONTROL Product profile]**.

      ![](assets/do-not-localize/admin_2.png)

   1. Digita il nome utente, il gruppo o l’indirizzo e-mail e fai clic su **[!UICONTROL Save]**.
   L&#39;utente è ora in grado di accedere a **[!UICONTROL Campaigns]**.

+++

1. **Hai bisogno di un pubblico**. I segmenti di pubblico devono essere disponibili prima di creare la campagna. Ulteriori informazioni sulla creazione di un pubblico [in questa pagina](../segment/about-segments.md).
1. **È necessaria una superficie del canale**. Per poter selezionare un canale, è necessario che la superficie del canale corrispondente (preimpostata) sia creata e disponibile. Ulteriori informazioni sulle superfici dei canali [in questa pagina](../configuration/channel-surfaces.md).

## Video introduttivo {#video}

Scopri come creare la tua prima campagna.

>[!VIDEO](https://video.tv.adobe.com/v/346680?quality=12)
