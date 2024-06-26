---
solution: Journey Optimizer
product: journey optimizer
title: Creare modelli di contenuto
description: Scopri come creare modelli per riutilizzare i contenuti nelle campagne e nei percorsi Journey Optimizer
feature: Templates
topic: Content Management
role: User
level: Beginner
source-git-commit: 59c675dd2ac94b6967cfb3a93f74b2016a090190
workflow-type: tm+mt
source-wordcount: '699'
ht-degree: 15%

---


# Creare modelli di contenuto {#create-content-templates}

>[!CONTEXTUALHELP]
>id="ajo_create_template"
>title="Definire un modello di contenuto personalizzato"
>abstract="Crea da zero un modello personalizzato autonomo per rendere i contenuti riutilizzabili in più percorsi e campagne."

Esistono due modi per creare modelli di contenuto:

* Creare un modello di contenuto da zero utilizzando la barra a sinistra **[!UICONTROL Modelli di contenuto]** menu. [Scopri come](#create-template-from-scratch)

* Quando progetti il contenuto all’interno di una campagna o di un percorso, salvalo come modello. [Scopri come](#save-as-template)

Una volta salvato, il modello di contenuto è disponibile per l’utilizzo in una campagna o in un percorso. Creato da zero o da un contenuto precedente, ora puoi utilizzare questo modello per creare qualsiasi contenuto in [!DNL Journey Optimizer]. [Scopri come](#use-content-templates)

>[!NOTE]
>
>* Le modifiche apportate ai modelli di contenuto non vengono propagate a campagne o percorsi, sia che siano live o bozze.
>
>* Allo stesso modo, quando i modelli vengono utilizzati in una campagna o in un percorso, eventuali modifiche apportate al contenuto della campagna e del percorso non influiscono sul modello di contenuto utilizzato in precedenza.

## Crea modello da zero {#create-template-from-scratch}

Per creare un modello di contenuto da zero, effettua le seguenti operazioni.

1. Accedere all’elenco dei modelli di contenuto tramite **[!UICONTROL Gestione dei contenuti]** > **[!UICONTROL Modelli di contenuto]** menu a sinistra.

1. Seleziona **[!UICONTROL Crea modello]**.

1. Inserisci i dettagli del modello e seleziona il canale desiderato.

   ![](assets/content-template-channels.png)

   >[!NOTE]
   >
   >Attualmente sono disponibili tutti i canali eccetto Web.

1. Scegli un **[!UICONTROL Tipo]** per il canale selezionato.

   ![](assets/content-template-type.png)

   * Per **[!UICONTROL E-mail]**, se selezioni **[!UICONTROL Contenuto]**, è possibile definire [Oggetto](../email/create-email.md#define-email-content) come parte del modello. Se si seleziona **[!UICONTROL HTML]**, è possibile definire solo il contenuto del corpo dell’e-mail.

   * Per **[!UICONTROL SMS]**, **[!UICONTROL Push]**, **[!UICONTROL In-app]** e **[!UICONTROL Direct mailing]**, per il canale corrente è disponibile solo il tipo predefinito. È comunque necessario selezionarlo.

1. Seleziona o crea tag Adobe Experience Platform da **[!UICONTROL Tag]** per categorizzare il modello e migliorare la ricerca. [Ulteriori informazioni](../start/search-filter-categorize.md#tags)

1. Per assegnare al modello etichette di utilizzo dei dati personalizzate o di base, puoi selezionare **[!UICONTROL Gestisci accesso]**. [Ulteriori informazioni su OLAC (Object Level Access Control)](../administration/object-based-access.md).

1. Clic **[!UICONTROL Crea]** e progettare i contenuti in base alle esigenze, nello stesso modo in cui si farebbe per qualsiasi contenuto all’interno di un percorso o di una campagna, in base al canale selezionato.

   ![](assets/content-template-edition.png)

   Scopri come creare contenuti per i diversi canali nelle sezioni seguenti:
   * [Definire il contenuto delle e-mail](../email/get-started-email-design.md)
   * [Definire il contenuto push](../push/design-push.md)
   * [Definire il contenuto degli SMS](../sms/create-sms.md#sms-content)
   * [Definire il contenuto della direct mailing](../direct-mail/create-direct-mail.md)
   * [Definire il contenuto in-app](../in-app/design-in-app.md)

1. Se stai creando un’ **[!UICONTROL E-mail]** modello con **[!UICONTROL HTML]** testo, puoi verificare il contenuto. [Scopri come](#test-template)

1. Quando il modello è pronto, fai clic su **[!UICONTROL Salva]**.

1. Fai clic sulla freccia accanto al nome del modello per tornare al **[!UICONTROL Dettagli]** schermo.

   ![](assets/content-template-back.png)

Questo modello è ora pronto per essere utilizzato quando si crea qualsiasi contenuto in [!DNL Journey Optimizer]. [Scopri come](#use-content-templates)

## Salva contenuto come modello di contenuto {#save-as-template}

>[!CONTEXTUALHELP]
>id="ajo_messages_depecrated_inventory"
>title="Scopri come effettuare la migrazione dei messaggi"
>abstract="Il 25 luglio 2022 il menu Messaggi è stato rimosso e i messaggi vengono ora creati direttamente da un percorso. Per riutilizzare i messaggi precedenti nei percorsi, devi salvarli come modelli."

Durante la progettazione di qualsiasi contenuto in una campagna o in un percorso, puoi salvarlo per un riutilizzo futuro. Per farlo, segui la procedura indicata di seguito.

1. Dal messaggio **[!UICONTROL Modifica contenuto]** , fare clic su **[!UICONTROL Modello di contenuto]** pulsante.

1. Seleziona **[!UICONTROL Salva come modello di contenuto]** dal menu a discesa.

   ![](assets/content-template-button-save.png)

   Se si è nel [E-mail Designer](../email/get-started-email-design.md), è inoltre possibile selezionare questa opzione dal menu **[!UICONTROL Altro]** in alto a destra.

   ![](assets/content-template-more-button-save.png)

1. Aggiungi un nome e una descrizione per questo modello.

   ![](assets/content-template-name.png)

   >[!NOTE]
   >
   >Il canale e il tipo correnti vengono compilati automaticamente e non possono essere modificati. Per i modelli e-mail creati da [E-mail Designer](../email/get-started-email-design.md), il **[!UICONTROL HTML]** viene selezionato automaticamente.

1. Seleziona o crea un tag Adobe Experience Platform da **Tag** per categorizzare il modello. [Ulteriori informazioni](../start/search-filter-categorize.md#tags)

1. Per assegnare al modello etichette di utilizzo dei dati personalizzate o di base, puoi selezionare **[!UICONTROL Gestisci accesso]**. [Ulteriori informazioni](../administration/object-based-access.md).

1. Fai clic su **[!UICONTROL Salva]**.

1. Il modello viene salvato in **[!UICONTROL Modelli di contenuto]** , accessibile dalla [!DNL Journey Optimizer] menu dedicato. Diventa un modello di contenuto autonomo accessibile, modificato ed eliminato come qualsiasi altro elemento dell’elenco. [Ulteriori informazioni](#access-manage-templates)

Ora puoi utilizzare questo modello per creare qualsiasi contenuto in [!DNL Journey Optimizer]. [Scopri come](#use-content-templates)

>[!NOTE]
>
>Qualsiasi modifica apportata a tale nuovo modello non viene propagata al contenuto da cui proviene. Analogamente, quando il contenuto originale viene modificato all’interno di tale contenuto, il nuovo modello non viene modificato.
