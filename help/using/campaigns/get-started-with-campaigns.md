---
solution: Journey Optimizer
product: journey optimizer
title: Introduzione alle campagne
description: Ulteriori informazioni sulle campagne in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Intermediate
keywords: campagna, come fare, inizio, optimizer
exl-id: e2506a43-e4f5-48af-bd14-ab76c54b7c90
source-git-commit: 11c1945f8e7f7ca74a2c9ca33ff85fea77bcf5db
workflow-type: ht
source-wordcount: '431'
ht-degree: 100%

---

# Introduzione alle campagne {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="campaigns_list"
>title="Campagne"
>abstract="Crea campagne per distribuire contenuti una tantum a un segmento specifico su vari canali. Prima di creare la campagna, accertati di avere una superficie del canale (ad esempio, un messaggio preimpostato) e un segmento Adobe Experience Platform pronto per l’uso."

Utilizza le campagne Journey Optimizer per distribuire contenuti una tantum a un segmento specifico utilizzando vari canali. Quando si utilizzano i percorsi, le azioni vengono eseguite in sequenza. Con le campagne, le azioni vengono eseguite simultaneamente, immediatamente o in base a una pianificazione specifica.

Puoi creare due tipi di campagne:

* Le **Campagne pianificate** consentono comunicazioni batch semplici ad hoc per casi d’uso di marketing come offerte promozionali, campagne di coinvolgimento, annunci, avvisi legali o aggiornamenti dei criteri.
* **Campagne attivate da API** consente alle comunicazioni di marketing di raggiungere un pubblico al momento giusto oppure di inviare messaggi transazionali/operativi a utenti individuali, come la reimpostazione della password, dove può essere necessario applicare la personalizzazione non solo utilizzando l’attributo di profilo, ma anche i dati contestuali in tempo reale nel trigger, che è un payload API REST.

I passaggi principali per creare una campagna sono i seguenti:

![](assets/create-campaign-process.png)

➡️ [Scopri questa funzione nel video](#video)

## Prima di iniziare {#campaign-prerequisites}

Prima di iniziare a creare la prima campagna in Journey Optimizer, verifica i seguenti prerequisiti:

1. **Sono necessarie autorizzazioni adeguate**. Le campagne sono disponibili solo per gli utenti con accesso a un **[!UICONTROL profilo di prodotto]** relativo a una campagna, come amministratore di campagna, approvatore di campagna, manager di campagna e/o visualizzatore di campagna.

   Se non riesci ad accedere alle campagne, devi estendere le tue autorizzazioni. Se hai accesso a [Adobe Admin Console](https://adminconsole.adobe.com/){target="_blank"} per la tua organizzazione, segui i passaggi seguenti. In caso contrario, contatta l’amministratore di Journey Optimizer.

   +++Scopri come assegnare le autorizzazioni della campagna

   Per assegnare il corrispondente **[!UICONTROL profilo di prodotto]** agli utenti:

   1. Da [Adobe Admin Console](https://adminconsole.adobe.com/){target="_blank"}, seleziona il prodotto [!DNL Adobe Experience Platform].

   1. Sfoglia la scheda **[!UICONTROL Profilo di prodotto]**, seleziona un **[!UICONTROL Profilo di prodotto]** relativo a una delle campagne integrate correlate: amministratore di campagna, approvatore di campagna, manager di campagna o visualizzatore di campagna.

      Per ulteriori informazioni sui **[!UICONTROL Profili di prodotto]** e le **[!UICONTROL Autorizzazioni]** della campagna di Journey Optimizer, [fai riferimento a questa pagina](../administration/ootb-product-profiles.md).

      ![](assets/do-not-localize/admin_1.png)

   1. Fai clic su **[!UICONTROL Aggiungi utente]** per assegnare all’utente il **[!UICONTROL Profilo di prodotto]** selezionato.

      ![](assets/do-not-localize/admin_2.png)

   1. Digita il nome utente, il gruppo o l’indirizzo e-mail e fai clic su **[!UICONTROL Salva]**.

   L’utente è ora in grado di accedere a **[!UICONTROL Campagne]**.

+++

1. **Hai bisogno di un pubblico**. I segmenti di pubblico devono essere disponibili prima di creare la campagna. Ulteriori informazioni sulla creazione di pubblico in [questa pagina](../segment/about-segments.md).
1. **È necessaria una superficie di canale**. Per poter selezionare un canale, è necessario che la superficie di canale corrispondente (ovvero, preimpostata) sia creata e disponibile. Ulteriori informazioni sulle superfici di canale in [questa pagina](../configuration/channel-surfaces.md).

## Video introduttivo {#video}

Scopri come creare la tua prima campagna.

>[!VIDEO](https://video.tv.adobe.com/v/346680?quality=12)
