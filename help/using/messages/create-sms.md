---
title: Creare un messaggio SMS
description: Scopri come creare un messaggio SMS in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 1f88626a-b491-4b36-8e3f-57f2b7567dd0
source-git-commit: 47b1c2832f82a5c168cd03f1d1b43a9223c945b3
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 9%

---

# Creare un messaggio SMS {#create-sms}

>[!CONTEXTUALHELP]
>id="ajo_message_sms"
>title="Creazione di SMS"
>abstract="Aggiungi il messaggio di testo e inizia a personalizzarlo con l’editor espressioni."

Una volta [creato un messaggio](get-started-content.md), utilizza **[!UICONTROL SMS]** per definire le impostazioni e il contenuto del messaggio SMS.


>[!AVAILABILITY]
>
>Il canale SMS è attualmente disponibile solo per un set di organizzazioni (disponibilità limitata). Per ulteriori informazioni, contatta il tuo rappresentante Adobe.

![](assets/sms_1.png)

Se è la prima volta che crei un messaggio SMS, assicurati che il canale SMS sia stato configurato. [Ulteriori informazioni](../configuration/sms-configuration.md).

## Definire il contenuto SMS{#sms-content}

Per iniziare a personalizzare il messaggio SMS, segui questi passaggi:

1. Fai clic sul pulsante **[!UICONTROL Add text message]** per aprire l’editor espressioni.

   ![](assets/sms_3.png)

1. Utilizza l’editor espressioni per definire il contenuto. Puoi utilizzare qualsiasi attributo per personalizzare il contenuto, ad esempio il nome del profilo o la città. Ulteriori informazioni sulla personalizzazione nell’editor espressioni in [questa sezione](../personalization/personalize.md)

   >[!NOTE]
   >
   > Un messaggio SMS può contenere fino a 160 caratteri, compresi spazi e interruzioni di riga.

   ![](assets/sms_2.png)

1. Fai clic su **[!UICONTROL Save]** quando il messaggio è pronto.

## Convalidare l’SMS{#sms-preview}

Una volta definito il contenuto del messaggio, puoi utilizzare i profili di test per visualizzarlo in anteprima e testarlo. Se hai inserito [contenuti personalizzati](../personalization/personalize.md), puoi controllare come questo contenuto viene visualizzato nel messaggio, sfruttando i dati del profilo di test.

Per visualizzare la modalità di visualizzazione del messaggio SMS sui dispositivi mobili, passa alla pagina **[!UICONTROL Preview]** scheda .

Per ulteriori informazioni al riguardo, consulta [questa sezione](../design/preview.md).

## Pubblicare l’SMS {#sms-publish}

Quando il messaggio è pronto, puoi pubblicarlo per renderlo disponibile per l’esecuzione con il **[!UICONTROL Publish]** pulsante . Questa azione pubblica la nuova versione del messaggio che verrà utilizzata per le successive esecuzioni nei tuoi percorsi.

È ora possibile utilizzare il messaggio SMS in un percorso. [Scopri come creare percorsi](../building-journeys/journey-gs.md).

## Consenso e rinuncia{#sms-opt-in-out}

Per tutti i messaggi di marketing, l’SMS deve contenere un modo per consentire ai destinatari di annullare facilmente l’iscrizione. Una volta annullato l’abbonamento, i profili vengono rimossi automaticamente dal pubblico dei messaggi di marketing futuri. L’aggiunta di un collegamento di annullamento all’abbonamento non è obbligatoria per i messaggi transazionali.

I destinatari degli SMS possono rispondere con parole chiave di consenso e rinuncia. In conformità agli standard e alle normative del settore, Adobe Journey Optimizer elabora automaticamente le seguenti parole chiave nei messaggi in arrivo: INIZIA, ARRESTA e DISARSI. Queste parole chiave attivano le risposte standard automatiche dal provider SMS.

**Argomenti correlati**

* [Configurare il canale SMS](../configuration/sms-configuration.md)
* [Rapporto SMS](../reports/journey-global-report.md#sms-global)
* [Creare un nuovo messaggio](get-started-content.md)
* [Aggiungere un messaggio in un percorso](../building-journeys/journeys-message.md)
