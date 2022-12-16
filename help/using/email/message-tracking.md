---
solution: Journey Optimizer
product: journey optimizer
title: Tracciare i messaggi
description: Scopri come aggiungere collegamenti e tenere traccia dei messaggi inviati
feature: Monitoring
topic: Content Management
role: User
level: Intermediate
exl-id: 689e630a-00ca-4893-8bf5-6d1ec60c52e7
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '693'
ht-degree: 9%

---

# Aggiungere collegamenti e tracciare i messaggi {#tracking}

Utilizzo [!DNL Journey Optimizer] aggiungere collegamenti al contenuto e tenere traccia dei messaggi inviati per monitorare il comportamento dei destinatari.

## Abilita tracciamento {#enable-tracking}

Puoi abilitare il tracciamento a livello di messaggio e-mail controllando il **[!UICONTROL Aperture e-mail]** e/o **[!UICONTROL Fai clic su e-mail]** quando crei il messaggio all’interno di un percorso o di una campagna.

>[!BEGINTABS]

>[!TAB Abilitare il tracciamento in un percorso]

![](assets/message-tracking-journey.png)

>[!TAB Abilitare il tracciamento in una campagna]

![](assets/message-tracking-campaign.png)

>[!ENDTABS]

>[!NOTE]
>
>Entrambe le opzioni sono abilitate per impostazione predefinita.

In questo modo puoi tenere traccia del comportamento dei destinatari attraverso:

* **[!UICONTROL Aperture e-mail]**: Messaggi aperti.
* **[!UICONTROL Fai clic su e-mail]**: Fai clic sui collegamenti in un’e-mail.

## Inserire collegamenti {#insert-links}

Durante la progettazione di un messaggio, puoi aggiungere collegamenti al contenuto.

>[!NOTE]
>
>Quando [tracciamento abilitato](#enable-tracking), vengono tracciati tutti i collegamenti inclusi nel contenuto del messaggio.

Per inserire collegamenti nel contenuto delle e-mail, segui la procedura seguente:

1. Seleziona un elemento e fai clic su **[!UICONTROL Inserisci collegamento]** dalla barra degli strumenti contestuale.

   ![](assets/message-tracking-insert-link.png)

1. Scegli il tipo di collegamento che desideri creare:

   * **[!UICONTROL Collegamento esterno]**: Inserisci un collegamento a un URL esterno.

   * **[!UICONTROL Pagina di destinazione]**: Inserisci un collegamento a una pagina di destinazione. [Ulteriori informazioni](../landing-pages/get-started-lp.md)

   * **[!UICONTROL Rinuncia con un clic]**: Inserisci un collegamento per consentire agli utenti di annullare rapidamente l’iscrizione alle tue comunicazioni senza dover confermare l’rinuncia. Ulteriori informazioni in [questa sezione](../privacy/opt-out.md#one-click-opt-out).

   * **[!UICONTROL Opt-in/abbonamento esterno]**: Inserisci un collegamento per accettare la ricezione di comunicazioni dal tuo marchio.

   * **[!UICONTROL Rinuncia/annullamento esterno dell’abbonamento]**: Inserisci un collegamento per non ricevere comunicazioni dal tuo marchio. Ulteriori informazioni sulla gestione delle rinunce sono disponibili in [questa sezione](../privacy/opt-out.md#opt-out-management).

   * **[!UICONTROL Pagina speculare]**: Inserisci un collegamento per visualizzare il contenuto dell’e-mail in un browser web. Ulteriori informazioni in [questa sezione](#mirror-page).

   ![](assets/message-tracking-links.png)

1. Puoi personalizzare i tuoi collegamenti. Ulteriori informazioni sugli URL personalizzati sono disponibili in [questa sezione](../personalization/personalization-syntax.md#perso-urls).

1. Salva le modifiche.

1. Una volta creato il collegamento, puoi comunque modificarlo dal **[!UICONTROL Impostazioni dei componenti]** a destra.

   * Puoi modificare il collegamento e modificarne il tipo.
   * Puoi scegliere di sottolineare il collegamento o meno selezionando l’opzione corrispondente.

   ![](assets/message-tracking-link-settings.png)

>[!NOTE]
>
>I messaggi e-mail di tipo marketing devono includere un [collegamento di rinuncia](../privacy/opt-out.md#opt-out-management), non necessaria per i messaggi transazionali. La categoria del messaggio (**[!UICONTROL Marketing]** o **[!UICONTROL Transazionale]**) è definita per la [superficie di canale](../configuration/channel-surfaces.md#email-type) (ossia per il predefinito del messaggio) e durante la creazione del messaggio.

## Collegamento a una pagina speculare {#mirror-page}

La pagina speculare è una pagina HTML accessibile online tramite un browser web. Il contenuto è identico a quello dell’e-mail.

Per aggiungere un collegamento a una pagina speculare nell’e-mail, [inserire un collegamento](#insert-links) e seleziona **[!UICONTROL Pagina speculare]** come tipo di collegamento.

![](assets/message-tracking-mirror-page.png)

La pagina speculare viene creata automaticamente.

>[!IMPORTANT]
>
>I collegamenti alle pagine mirror vengono generati automaticamente e non possono essere modificati. Contengono tutti i dati personalizzati crittografati necessari per eseguire il rendering dell’e-mail originale. Di conseguenza, l’utilizzo di attributi personalizzati con valori di grandi dimensioni può generare URL per pagine mirror lunghe, il che può impedire il funzionamento del collegamento nei browser web con una lunghezza massima di URL.

Una volta inviata l’e-mail, quando i destinatari fanno clic sul collegamento della pagina speculare, il contenuto dell’e-mail viene visualizzato nel browser Web predefinito.

>[!NOTE]
>
>In [prova](preview.md#send-proofs) inviato ai profili di test, il collegamento alla pagina speculare non è attivo. Viene attivato solo nei messaggi finali.

Il periodo di conservazione per una pagina speculare è di 60 giorni. Dopo tale ritardo, la pagina speculare non sarà più disponibile.

## Gestire il tracciamento {#manage-tracking}

La [E-mail Designer](content-from-scratch.md) consente di gestire gli URL tracciati, ad esempio modificando il tipo di tracciamento per ogni collegamento.

1. Fai clic sul pulsante **[!UICONTROL Collegamenti]** per visualizzare l’elenco di tutti gli URL del contenuto che verranno tracciati.

   Questo elenco consente di avere una visualizzazione centralizzata e di individuare ogni URL nel contenuto dell’e-mail.

1. Per modificare un collegamento, fai clic sull’icona a forma di matita corrispondente.

   ![](assets/message-tracking-edit-links.png)

1. Puoi modificare la **[!UICONTROL Tipo di tracciamento]** se necessario:

   ![](assets/message-tracking-edit-a-link.png)

   Per ogni URL tracciato, puoi impostare la modalità di tracciamento su uno dei seguenti valori:

   * **[!UICONTROL Tracciato]**: Attiva il tracciamento su questo URL.
   * **[!UICONTROL Rinuncia]**: Considera questo URL come un URL di rinuncia o di annullamento dell’abbonamento.
   * **[!UICONTROL Pagina speculare]**: Considera questo URL come un URL della pagina speculare.
   * **[!UICONTROL Mai]**: Non attiva mai il tracciamento di questo URL. <!--This information is saved: if the URL appears again in a future message, its tracking is automatically deactivated.-->

Il reporting su aperture e clic è disponibile nella [Report live](../reports/live-report.md) e [Report globale](../reports/global-report.md).
