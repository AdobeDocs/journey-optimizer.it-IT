---
title: Tracciare i messaggi
description: Scopri come tenere traccia dei messaggi inviati
feature: Monitoraggio
topic: Gestione dei contenuti
role: User
level: Intermediate
source-git-commit: e27472cc6186cf7cb25fdb93d15720fc837c58bb
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 2%

---

# Tracciamento dei messaggi {#tracking}

Utilizza [!DNL Journey Optimizer] per tenere traccia dei messaggi inviati e del comportamento dei destinatari.

## Abilita tracciamento {#enable-tracking}

Puoi abilitare il tracciamento a livello di messaggio selezionando le opzioni **[!UICONTROL Open Tracking for email]** e/o **[!UICONTROL Click Tracking for email]** durante la [creazione del messaggio](create-message.md).

![](assets/message-tracking.png)

>[!NOTE]
>
>Entrambe le opzioni sono abilitate per impostazione predefinita.

In questo modo puoi tenere traccia del comportamento dei destinatari attraverso:
* **[!UICONTROL Open Tracking for email]**: Messaggi aperti.
* **[!UICONTROL Click Tracking for email]**: Fai clic sui collegamenti in un’e-mail.

## Inserisci collegamenti {#insert-links}

Durante la progettazione di un messaggio, puoi aggiungere collegamenti al contenuto.

>[!NOTE]
>
>Quando [il tracciamento è abilitato](#enable-tracking), tutti i collegamenti inclusi nel contenuto del messaggio vengono tracciati.

Per inserire collegamenti nel contenuto delle e-mail, segui la procedura seguente:

1. Seleziona un elemento e fai clic su **[!UICONTROL Insert link]** nella barra degli strumenti contestuale.

   ![](assets/message-tracking-insert-link.png)

1. Scegli il tipo di collegamento che desideri creare:

   * **[!UICONTROL External link]**: Inserisci un collegamento a un URL esterno.

   * **[!UICONTROL Unsubscription link]**: Inserisci un collegamento per non ricevere comunicazioni dal tuo marchio. Ulteriori informazioni sulla gestione delle rinunce in [questa sezione](consent.md#opt-out-management).

   * **[!UICONTROL Mirror page]**: Inserisci un collegamento per visualizzare il contenuto dell’e-mail in un browser web.

   ![](assets/message-tracking-links.png)

1. Puoi personalizzare i collegamenti utilizzando solo una semplice espressione. Ulteriori informazioni sulla personalizzazione in [questa sezione](personalization/personalization-syntax.md).

1. Salva le modifiche.

1. Una volta creato il collegamento, puoi comunque modificarlo dal riquadro **[!UICONTROL Component settings]** a destra.

   * Fai clic sull’icona a forma di matita per modificare il collegamento.
   * Puoi scegliere di sottolineare il collegamento o meno selezionando l’opzione corrispondente.

   ![](assets/message-tracking-link-settings.png)

## Gestire il tracciamento {#manage-tracking}

Il [E-mail Designer](create-email-content.md) consente di gestire gli URL tracciati, ad esempio modificando il tipo di tracciamento per ogni collegamento.

1. Fai clic sull’icona **[!UICONTROL Links]** nel riquadro a sinistra per visualizzare l’elenco di tutti gli URL del contenuto che verranno tracciati.

   Questo elenco consente di avere una visualizzazione centralizzata e di individuare ogni URL nel contenuto dell’e-mail.

1. Per modificare un collegamento, fai clic sull’icona a forma di matita corrispondente.

   ![](assets/message-tracking-edit-links.png)

1. Se necessario, puoi modificare la sezione **[!UICONTROL Tracking Type]**:


   ![](assets/message-tracking-edit-a-link.png)

   Per ogni URL tracciato, puoi impostare la modalità di tracciamento su uno dei seguenti valori:

   * **[!UICONTROL Tracked]**: Attiva il tracciamento su questo URL.
   * **[!UICONTROL Opt out]**: Considera questo URL come un URL di rinuncia o di annullamento dell’abbonamento.
   * **[!UICONTROL Mirror page]**: Considera questo URL come un URL della pagina speculare.
   * **[!UICONTROL Never]**: Non attiva mai il tracciamento di questo URL.  <!--This information is saved: if the URL appears again in a future message, its tracking is automatically deactivated.-->

Il numero di messaggi aperti e il numero di collegamenti su cui è stato fatto clic sono elencati nella scheda [Esecuzioni](message-monitoring.md).

Il reporting su aperture e clic è disponibile nel [rapporto Email Live](reports/email-live-report.md) e nel [rapporto globale e-mail](reports/email-global-report.md).


