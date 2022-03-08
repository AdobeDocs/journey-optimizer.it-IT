---
title: 'Creare un messaggio '
description: Scopri come creare un messaggio
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 186a43cd-c5eb-4de1-8713-95399d802d36
source-git-commit: 68407db81224e9c2b6930c800e57b65e081781fe
workflow-type: tm+mt
source-wordcount: '482'
ht-degree: 4%

---

# Creare un messaggio  {#create-message}

I messaggi sono disponibili dal **[!UICONTROL Messages]** scorciatoia nella navigazione a sinistra. Tutti i messaggi sono elencati, ordinati in base alla data di pubblicazione (per i messaggi pubblicati) o alla data di creazione (per le bozze dei messaggi).

>[!NOTE]
>
>Gli utenti possono accedere, creare, modificare e/o pubblicare i messaggi in base al loro profilo di prodotto. Ulteriori informazioni sulle autorizzazioni per gli utenti [in questa sezione](../administration/permissions.md).

![](assets/messages-list.png)

Utilizza la **[!UICONTROL Show recents]** per aggiungere collegamenti diretti ai messaggi a cui hai effettuato l’accesso negli ultimi 5 giorni.

![](assets/show-recent-messages.png)

Utilizza l’icona del filtro per visualizzare solo i messaggi di bozza, pubblicati o in corso di pubblicazione. Puoi anche eseguire ricerche sull’etichetta del messaggio, come segue:

![](assets/filter-messages.png)

## Creare un nuovo messaggio {#create-new-message}

Per creare un nuovo messaggio, segui i passaggi seguenti:

1. Accedi all&#39;elenco dei messaggi, quindi fai clic su **[!UICONTROL Create Message]**.

1. Definisci le proprietà del messaggio.

   ![](assets/create-message-properties.png)

   * Inserisci un **[!UICONTROL Title]** (obbligatorio) e **[!UICONTROL Description]**.

   * Seleziona la **[!UICONTROL Message category]**: Marketing o transazionale.

   * Seleziona la **[!UICONTROL Preset]** da utilizzare per il messaggio.

      I predefiniti includono tutti i parametri necessari per inviare una notifica e-mail e/o push in base al marchio. [Ulteriori informazioni sui predefiniti](../configuration/message-presets.md).

   * Seleziona i canali da utilizzare per il messaggio: Notifica e-mail e/o push. Per creare il messaggio, devi selezionare almeno un canale.
   Puoi accedere e modificare il titolo, la descrizione e il predefinito del messaggio in qualsiasi momento utilizzando la **[!UICONTROL Properties]** nell’interfaccia dei messaggi.

1. Fai clic su **[!UICONTROL Create]** per confermare la creazione dei messaggi. Il messaggio viene aggiunto nell’elenco dei messaggi nella **[!UICONTROL Draft]** stato.

   È disponibile una scheda per ogni canale selezionato. Utilizza queste schede per configurare il contenuto per ogni canale. Per rimuovere una scheda, selezionala e fai clic sul pulsante **[!UICONTROL Delete channel]** a destra.

   ![](assets/create-messages-content.png)

   Ora puoi creare il contenuto del messaggio e adattare le impostazioni. Informazioni dettagliate sulla configurazione delle notifiche e-mail e push sono disponibili nelle sezioni seguenti:

   * [Creare un messaggio e-mail](create-email.md)
   * [Creare notifiche push](create-push.md)

   >[!NOTE]
   >   
   >Puoi personalizzare i messaggi utilizzando i dati dei profili utilizzando l’editor espressioni. Per ulteriori informazioni sulla personalizzazione, consulta [questa sezione](../personalization/personalize.md).

1. Controlla il rendering dei messaggi e controlla le impostazioni di personalizzazione con i profili di test, utilizzando la sezione di anteprima sul lato sinistro. Per ulteriori informazioni al riguardo, consulta [questa sezione](preview.md).

   ![](assets/messages-simple-preview.png)

1. Controlla gli avvisi nella sezione superiore dell&#39;editor.  Alcuni sono semplici avvisi, altri possono impedire la pubblicazione del messaggio. [Ulteriori informazioni](alerts.md).

1. Per pubblicare il messaggio, fai clic sul pulsante **[!UICONTROL Publish]** oppure puoi mantenerlo come bozza e pubblicarlo in un secondo momento. Per ulteriori informazioni su come pubblicare i messaggi, consulta [questa sezione](publish-manage-message.md).

## Duplicare un messaggio {#duplicate-message}

Per creare un messaggio da un messaggio esistente, utilizza il **[!UICONTROL Duplicate]** dall’interfaccia dei messaggi. Tutte le impostazioni e la configurazione verranno copiate nel nuovo messaggio

![](assets/message-duplicate.png)

È possibile rinominare il messaggio prima di confermare la duplicazione.

![](assets/message-duplicate-confirm.png)

Una volta creato il nuovo messaggio, nella parte inferiore della finestra viene visualizzato un messaggio di conferma.

Puoi anche duplicare un messaggio dall’elenco dei messaggi utilizzando l’icona dedicata.

![](assets/message-duplicate-from-list.png)

Si applica lo stesso processo di conferma.
