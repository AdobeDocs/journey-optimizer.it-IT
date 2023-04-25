---
solution: Journey Optimizer
product: journey optimizer
title: Introduzione alle campagne
description: Ulteriori informazioni sulle campagne in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Intermediate
keywords: campagna, come , iniziare, ottimizzatore
exl-id: e2506a43-e4f5-48af-bd14-ab76c54b7c90
source-git-commit: 8b1bf0b0469c1efc5194dae56ddddd9f05dbf722
workflow-type: tm+mt
source-wordcount: '406'
ht-degree: 20%

---

# Introduzione alle campagne {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="campaigns_list"
>title="Campagne"
>abstract="Crea campagne per consegnare contenuti una tantum a un segmento specifico su vari canali. Prima di creare la campagna, accertati di avere una superficie del canale (ad esempio un messaggio preimpostato) e un segmento Adobe Experience Platform pronto per l’uso."

Utilizza le campagne Journey Optimizer per distribuire contenuti una tantum a un segmento specifico utilizzando vari canali. Quando si utilizzano i percorsi, le azioni vengono eseguite in sequenza. Con le campagne, le azioni vengono eseguite simultaneamente, immediatamente o in base a una pianificazione specifica.

Puoi creare due tipi di campagne:

* **Campagne pianificate** consentono comunicazioni batch semplici ad hoc per casi d’uso di marketing come offerte promozionali, campagne di coinvolgimento, annunci, avvisi legali o aggiornamenti dei criteri.
* **Campagne attivate dall’API** consenti semplici messaggi operativi/transazionali con API REST (reimpostazione della password, abbandono del carrello, ecc.), dove la necessità di personalizzare utilizzando gli attributi del profilo e i dati contestuali del payload.

I passaggi principali per creare una campagna sono i seguenti:

![](assets/create-campaign-process.png)

➡️ [Scopri questa funzione nel video](#video)

## Prima di iniziare {#campaign-prerequisites}

Prima di iniziare a creare la prima campagna in Journey Optimizer, verifica i seguenti prerequisiti:

1. **Sono necessarie autorizzazioni adeguate**. Le campagne sono disponibili solo per gli utenti con accesso a una campagna correlata **[!UICONTROL Profilo di prodotto]** come l’amministratore di Campaign, l’approvatore di Campaign, il manager di Campaign e/o il visualizzatore di Campaign.

   Se non riesci ad accedere alle campagne, devi estendere le tue autorizzazioni. Se hai accesso a [Adobe Admin Console](https://adminconsole.adobe.com/){target="_blank"} per la tua organizzazione, segui i passaggi seguenti. In caso contrario, contattare l&#39;amministratore Journey Optimizer.

   +++Scopri come assegnare le autorizzazioni della campagna

   Per assegnare il corrispondente **[!UICONTROL Profilo di prodotto]** agli utenti:

   1. Da [Adobe Admin Console](https://adminconsole.adobe.com/){target="_blank"}, seleziona [!DNL Adobe Experience Platform] prodotto.

   1. Sfoglia il **[!UICONTROL Profilo di prodotto]** , seleziona una delle campagne integrate correlate **[!UICONTROL Profilo di prodotto]**: Amministratore di Campaign, approvatore di Campaign, manager di Campaign o visualizzatore di Campaign.

      Per ulteriori informazioni sulla campagna Journey Optimizer **[!UICONTROL Profili di prodotto]** e **[!UICONTROL Autorizzazioni]**, [fai riferimento a questa pagina](../administration/ootb-product-profiles.md).

      ![](assets/do-not-localize/admin_1.png)

   1. Fai clic su **[!UICONTROL Aggiungi utente]** per assegnare all&#39;utente il **[!UICONTROL Profilo di prodotto]**.

      ![](assets/do-not-localize/admin_2.png)

   1. Digita il nome utente, il gruppo o l’indirizzo e-mail e fai clic su **[!UICONTROL Salva]**.
   L&#39;utente è ora in grado di accedere a **[!UICONTROL Campagne]**.

+++

1. **Hai bisogno di un pubblico**. I segmenti di pubblico devono essere disponibili prima di creare la campagna. Ulteriori informazioni sulla creazione di un pubblico [in questa pagina](../segment/about-segments.md).
1. **È necessaria una superficie del canale**. Per poter selezionare un canale, è necessario che la superficie del canale corrispondente (preimpostata) sia creata e disponibile. Ulteriori informazioni sulle superfici dei canali [in questa pagina](../configuration/channel-surfaces.md).

## Video introduttivo {#video}

Scopri come creare la tua prima campagna.

>[!VIDEO](https://video.tv.adobe.com/v/346680?quality=12)
