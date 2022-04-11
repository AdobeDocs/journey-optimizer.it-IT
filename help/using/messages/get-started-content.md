---
title: Introduzione ai messaggi
description: Scopri come creare messaggi in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 712dc172-6c0d-4ce8-ba16-de99d65fc641
source-git-commit: 1d0e28583c500d5eddf9f88250f279d188c4784a
workflow-type: tm+mt
source-wordcount: '647'
ht-degree: 97%

---

# Introduzione ai messaggi {#get-started-contents-messages}

Utilizza [!DNL Journey Optimizer] per sfruttare più elementi come risorse e contenuti in un’unica posizione, e per creare e pubblicare notifiche push e messaggi e-mail personalizzati.

* In [!DNL Journey Optimizer] utilizza le **funzionalità di progettazione delle e-mail** per creare o importare e-mail dinamiche.

* Utilizza **Adobe Experience Manager Assets Essentials** per creare un tuo database di risorse e arricchire le e-mail.

* Migliora l’esperienza dei clienti creando **messaggi push e-mail personalizzati** in base ai loro attributi di profilo.

* **Crea messaggi push ed e-mail** in base a questi contenuti, quindi pubblicali.

## Accedi ai messaggi {#access-messages}

I messaggi sono disponibili dalla **[!UICONTROL Messages]** scelta rapida nella navigazione a sinistra. Tutti i messaggi sono elencati, ordinati in base alla data di pubblicazione (per i messaggi pubblicati) o alla data di creazione (per le bozze dei messaggi).

>[!NOTE]
>
>Gli utenti possono accedere a, creare, modificare e/o pubblicare i messaggi in base al loro profilo di prodotto. Ulteriori informazioni sulle autorizzazioni per gli utenti [in questa sezione](../administration/permissions.md).

![](assets/messages-list.png)

* Utilizza l’interruttore **[!UICONTROL Show recents]** per aggiungere collegamenti diretti ai messaggi a cui hai effettuato l’accesso negli ultimi 5 giorni.

   ![](assets/show-recent-messages.png)

* Utilizza l’icona del filtro per visualizzare solo i messaggi di bozza, pubblicati o in corso di pubblicazione. Puoi anche eseguire ricerche sull’etichetta del messaggio, come segue:

   ![](assets/filter-messages.png)

* Puoi archiviare i messaggi non utilizzati per cancellare l’elenco dei messaggi utilizzando l’icona dedicata dal menu Azioni rapide.

   ![](assets/archive-message.png)

   Utilizza l’icona del filtro per visualizzare tutti i messaggi archiviati e fai clic sull’icona **[!UICONTROL Unarchive]** per rimuovere un elemento dall’elenco dei messaggi archiviati.

   >[!NOTE]
   >
   >Impossibile aprire un messaggio archiviato. Devi prima annullare l’archiviazione.

## Creare un nuovo messaggio {#create-new-message}

Per creare un nuovo messaggio, segui i passaggi seguenti:

1. Accedi all’elenco dei messaggi, quindi fai clic su **[!UICONTROL Create Message]**.

1. Definisci le proprietà del messaggio.

   ![](assets/create-message-properties.png)

   * Inserisci un **[!UICONTROL Title]** (obbligatorio) e **[!UICONTROL Description]**.

   * Seleziona la **[!UICONTROL Message category]**: Marketing o Transazionale.

   * Seleziona i canali da utilizzare per il messaggio: E-mail e/o notifica push. Per creare il messaggio, devi selezionare almeno un canale.

   * Seleziona la **[!UICONTROL Preset]** da utilizzare per il messaggio.

      I predefiniti includono tutti i parametri necessari per inviare una e-mail e/o una notifica push in base al marchio. [Ulteriori informazioni sui predefiniti](../configuration/message-presets.md).
   >[!CAUTION]
   >
   >Devi scegliere un predefinito di messaggio valido per la categoria e i canali selezionati.

   Puoi accedere e modificare il titolo, la descrizione e il predefinito del messaggio in qualsiasi momento utilizzando il pulsante **[!UICONTROL Properties]** nell’interfaccia dei messaggi.

1. Fai clic **[!UICONTROL Create]** per confermare la creazione del messaggio. Il messaggio viene aggiunto nell’elenco dei messaggi nello **[!UICONTROL Draft]** stato.

   È disponibile una scheda per ogni canale selezionato. Utilizza queste schede per configurare il contenuto per ogni canale. Per rimuovere una scheda, selezionala e fai clic sul pulsante **[!UICONTROL Delete channel]** a destra.

   ![](assets/create-messages-content.png)

   Ora puoi creare il contenuto del messaggio e adattare le impostazioni. Informazioni dettagliate sulla configurazione delle e-mail e delle notifiche push sono disponibili nelle sezioni seguenti:

   * [Creare un messaggio e-mail](create-email.md)
   * [Creare una notifica push](create-push.md)

   >[!NOTE]
   >   
   >Puoi personalizzare i messaggi utilizzando i dati dei profili utilizzando l’editor di espressioni. Per ulteriori informazioni sulla personalizzazione, consulta [questa sezione](../personalization/personalize.md).

1. Controlla il rendering dei messaggi e controlla le impostazioni di personalizzazione con i profili di test, utilizzando la sezione di anteprima sul lato sinistro. Per ulteriori informazioni al riguardo, consulta [questa sezione](../design/preview.md).

   ![](assets/messages-simple-preview.png)

1. Controlla gli avvisi nella sezione superiore dell’editor.  Alcuni sono semplici avvisi, altri possono impedire la pubblicazione del messaggio. Ulteriori informazioni in [questa sezione](alerts.md).

1. Per pubblicare il messaggio, fai clic sul pulsante **[!UICONTROL Publish]** oppure mantienilo come bozza e pubblicalo in un secondo momento. Per ulteriori informazioni su come pubblicare i messaggi, consulta [questa sezione](publish-manage-message.md).

## Duplica un messaggio {#duplicate-message}

Per creare un messaggio da uno esistente, segui i passaggi seguenti.

1. Apri il messaggio da copiare.

1. Utilizza il pulsante **[!UICONTROL Duplicate]** dall’interfaccia dei messaggi.

   ![](assets/message-duplicate.png)

   Tutte le impostazioni e la configurazione verranno copiate nel nuovo messaggio.

1. È possibile rinominare il messaggio prima di confermare la duplicazione.

   ![](assets/message-duplicate-confirm.png)

1. Una volta creato il nuovo messaggio, nella parte inferiore della finestra viene visualizzato un messaggio di conferma.

Puoi anche duplicare un messaggio dall’elenco dei messaggi, utilizzando l’icona dedicata dal menu Azioni rapide.

![](assets/message-duplicate-from-list.png)

Si applica lo stesso processo di conferma.

