---
solution: Journey Optimizer
product: journey optimizer
title: Creare un messaggio e-mail
description: Scopri come creare un’e-mail in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: c77dc420-a375-4376-ad86-ac740e214c3c
source-git-commit: 9b4ab81a362c38dce5ff4b10fb301c81ed117688
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 10%

---

# Creare un messaggio e-mail {#configure-email}

>[!CONTEXTUALHELP]
>id="ajo_message_email"
>title="Creazione di e-mail"
>abstract="Definisci i parametri e-mail in tre semplici passaggi."

Le e-mail possono essere create:

* In una **Percorso**: Dopo aver aggiunto un’attività E-mail nel percorso e definito le impostazioni di base, utilizza **[!UICONTROL Azioni: E-mail]** riquadro a destra per creare il contenuto per le notifiche push.

   Per ulteriori informazioni su come configurare il percorso, consulta questo [page](../building-journeys/journey-gs.md).

   ![](assets/email-edit-content.png)

* In una **Campaign**: Dopo aver creato una campagna, seleziona e-mail come azione e definisci le impostazioni di base.

   Per ulteriori informazioni su come configurare la campagna, consulta questo [page](../campaigns/create-campaign.md#configure).

   ![](assets/email_campaign.png)

## Definire il contenuto dell’e-mail{#email-content}

Utilizzo [!DNL Journey Optimizer] Invia a E-mail Designer [progettare l&#39;e-mail da zero](../design/create-email-content.md). Se disponi di un contenuto esistente, puoi [importarlo in E-mail Designer](../design/existing-content.md)oppure [codificare il proprio contenuto](../design/code-content.md) in [!DNL Journey Optimizer].

[!DNL Journey Optimizer] viene fornito con un set di [modelli incorporati](../design/email-templates.md) per aiutarti a iniziare. Qualsiasi e-mail può anche essere salvata come modello.

Utilizzo [!DNL Journey Optimizer] Editor espressioni per personalizzare i messaggi con i dati dei profili. Per ulteriori informazioni sulla personalizzazione, consulta [questa sezione](../personalization/personalize.md).

Adatta il contenuto dei messaggi ai profili target utilizzando [!DNL Journey Optimizer] funzionalità di contenuto dinamico. [Introduzione ai contenuti dinamici](../personalization/get-started-dynamic-content.md)

## Tracciamento e-mail{#email-tracking}

Se desideri tenere traccia del comportamento dei destinatari attraverso le aperture e/o i clic sui collegamenti, abilita le seguenti opzioni: **[!UICONTROL Aperture e-mail]** e **[!UICONTROL Fai clic su e-mail]**.

Ulteriori informazioni sul tracciamento in [questa sezione](../design/message-tracking.md).

## Convalidare il contenuto dell’e-mail{#email-content-validate}

Controlla il rendering del tuo messaggio e-mail e controlla le impostazioni di personalizzazione con i profili di test, utilizzando la sezione di anteprima sul lato sinistro. Per ulteriori informazioni al riguardo, consulta [questa sezione](../design/preview.md).

![](assets/messages-simple-preview.png)


È inoltre necessario controllare gli avvisi nella sezione superiore dell’editor.  Alcuni sono semplici avvisi, altri possono impedire l’utilizzo del messaggio. Ulteriori informazioni in [questa sezione](alerts.md).


>[!NOTE]
>
>La **[!UICONTROL Da e-mail]** e **[!UICONTROL Nome mittente]** sono determinati **[!UICONTROL Superficie]** che è stato selezionato quando [creazione del messaggio](get-started-content.md).

