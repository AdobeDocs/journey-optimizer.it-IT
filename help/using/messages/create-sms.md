---
title: Creare un messaggio SMS
description: Scopri come creare un messaggio SMS in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 1f88626a-b491-4b36-8e3f-57f2b7567dd0
source-git-commit: 0e978d0eab570a28c187f3e7779c450437f16cfb
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 15%

---

# Creare un messaggio SMS {#create-sms}

>[!CONTEXTUALHELP]
>id="ajo_message_sms"
>title="Creazione di SMS"
>abstract="Aggiungi il messaggio di testo e inizia a personalizzarlo con l’editor espressioni."

Utilizzo [!DNL Journey Optimizer] per inviare messaggi di testo ai clienti sui loro dispositivi mobili. Puoi creare, personalizzare e visualizzare in anteprima i messaggi in formato testo dall’editor SMS.

Una volta [è stato aggiunto un SMS](get-started-content.md) attività nel tuo percorso e impostazioni di base definite, utilizza le **[!UICONTROL Actions: SMS]** riquadro a destra per creare il contenuto per il messaggio SMS.

>[!AVAILABILITY]
>
>Il canale SMS è attualmente disponibile solo per un set di organizzazioni (disponibilità limitata). Per ulteriori informazioni, contatta il tuo rappresentante Adobe.

![](assets/sms-edit-content.png)

Se è la prima volta che crei un messaggio SMS, assicurati che il canale SMS sia stato configurato. [Ulteriori informazioni](../configuration/sms-configuration.md).

## Definire il contenuto SMS{#sms-content}

Per iniziare a personalizzare il messaggio SMS, segui questi passaggi:

1. Fai clic sul pulsante **[!UICONTROL Message]** per aprire l’editor espressioni.

   ![](assets/sms-content.png)

1. Utilizza l’editor espressioni per definire il contenuto. Puoi utilizzare qualsiasi attributo per personalizzare il contenuto, ad esempio il nome del profilo o la città. Ulteriori informazioni sulla personalizzazione nell’editor espressioni in [questa sezione](../personalization/personalize.md).

1. Fai clic su **[!UICONTROL Save]** e controlla il messaggio nell’anteprima.

   ![](assets/sms-content-preview.png)


## Convalidare l’SMS{#sms-preview}

Una volta definito il contenuto del messaggio, puoi utilizzare i profili di test per visualizzarlo in anteprima e testarlo. Se hai inserito [contenuti personalizzati](../personalization/personalize.md), puoi controllare come questo contenuto viene visualizzato nel messaggio, sfruttando i dati del profilo di test.

Per visualizzare la modalità di visualizzazione del messaggio SMS sui dispositivi mobili, fai clic sul pulsante **[!UICONTROL Simulate content]** scheda . Ulteriori informazioni sulla simulazione dei contenuti in [questa sezione](../design/preview.md).

È inoltre necessario controllare gli avvisi nella sezione superiore dell’editor.  Alcuni sono semplici avvisi, altri possono impedire l’utilizzo del messaggio. Ulteriori informazioni in [questa sezione](alerts.md).

![](assets/sms-alert-button.png)


## Consenso e rinuncia{#sms-opt-in-out}

Per tutti i messaggi di marketing, l’SMS deve contenere un modo per consentire ai destinatari di annullare facilmente l’iscrizione. Una volta annullato l’abbonamento, i profili vengono rimossi automaticamente dal pubblico dei messaggi di marketing futuri. L’aggiunta di un collegamento di annullamento all’abbonamento non è obbligatoria per i messaggi transazionali.

I destinatari degli SMS possono rispondere con parole chiave di consenso e rinuncia. In conformità agli standard e alle normative del settore, Adobe Journey Optimizer elabora automaticamente le seguenti parole chiave nei messaggi in arrivo: INIZIA, ARRESTA e DISARSI. Queste parole chiave attivano le risposte standard automatiche dal provider SMS.

Per ulteriori informazioni sul funzionamento del supporto nativo per parole chiave in entrata (start, stop e unstop) per SMS, consulta il seguente video.

>[!VIDEO](https://video.tv.adobe.com/v/344026?quality=12)

<!--
## How-to video

Learn how to configure, author, and include SMS messaging into your customer journeys.

>[!VIDEO](https://video.tv.adobe.com/v/344460?quality=12)
-->
**Argomenti correlati**

* [Configurare il canale SMS](../configuration/sms-configuration.md)
* [Rapporto SMS](../reports/journey-global-report.md#sms-global)
* [Creare un nuovo messaggio](get-started-content.md)
* [Aggiungere un messaggio in un percorso](../building-journeys/journeys-message.md)
