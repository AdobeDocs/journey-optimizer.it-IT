---
solution: Journey Optimizer
product: journey optimizer
title: Creare modelli di contenuto
description: Scopri come creare modelli da riutilizzare contenuto nelle campagne e nei percorsi di Journey Optimizer
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

Esistono due modi per creare contenuto modelli:

* Crea un modello contenuto da zero, utilizzando il menu barra **[!UICONTROL a sinistra Modelli di]** contenuto. [Scopri come](#create-template-from-scratch)

* Quando progetti la tua contenuto all&#39;interno di una campagna o di un percorso, salvala come modello. [Scopri come](#save-as-template)

Una volta salvato, il modello contenuto è disponibile per una campagna o un viaggio. Sia che sia stato creato da zero o da un contenuto precedente, ora puoi usare questo modello quando crei qualsiasi contenuto all&#39;interno di [!DNL Journey Optimizer]. [Scopri come](#use-content-templates)

>[!NOTE]
>
>* Le modifiche apportate ai modelli contenuto non vengono propagate alle campagne o ai percorsi, siano essi attivi o di bozza.
>
>* Analogamente, quando i modelli vengono utilizzati in una campagna o in un percorso, qualsiasi modifica apportata alla campagna e al contenuto di percorso non influisce sul modello contenuto utilizzato in precedenza.

## Crea modello da zero {#create-template-from-scratch}

Per creare un modello contenuto da zero, seguire i passaggi riportati di seguito.

1. Accedere all&#39;elenco dei modelli di contenuto tramite il menu a sinistra Gestione **** contenuti > **[!UICONTROL Modelli di]** contenuto.

1. Selezionare **[!UICONTROL Crea modello]**.

1. Inserisci i dettagli del modello e seleziona il canale desiderato.

   ![](assets/content-template-channels.png)

   >[!NOTE]
   >
   >Attualmente tutti i canali sono disponibili tranne Web.

1. Scegli un **[!UICONTROL tipo]** per il canale selezionato.

   ![](assets/content-template-type.png)

   * Per **[!UICONTROL E-mail]**, se si seleziona **[!UICONTROL Contenuto]**, è possibile definire la riga](../email/create-email.md#define-email-content) dell&#39;oggetto [come parte del modello. Se selezioni **[!UICONTROL HTML]**, puoi definire solo il contenuto del corpo del messaggio e-mail.

   * Per **[!UICONTROL SMS,]****[!UICONTROL Push]**, **[!UICONTROL In-app]** e **[!UICONTROL Direct Mail]**, è disponibile solo il tipo predefinito per il canale corrente. Devi ancora selezionarlo.

1. Seleziona o crea Adobe Experience Platform tag dal campo Tag ]**per categorizzare il modello e migliorare la**[!UICONTROL  ricerca. [Ulteriori informazioni](../start/search-filter-categorize.md#tags)

1. Per assegnare etichette di utilizzo dei dati personalizzate o di base al modello, puoi selezionare **[!UICONTROL Gestisci accesso]**. [Scopri ulteriori informazioni sul controllo di accesso a livello di oggetto (OLAC, Object Level Access Control).](../administration/object-based-access.md)

1. Fai clic **[!UICONTROL su Crea]** e progetta la tua contenuto in base alle esigenze, nello stesso modo in cui faresti per qualsiasi contenuto all&#39;interno di un viaggio o di una campagna, in base al canale selezionato.

   ![](assets/content-template-edition.png)

   Scopri come creare contenuto per i diversi canali nelle sezioni seguenti:
   * [Definire contenuto e-mail](../email/get-started-email-design.md)
   * [Definire i contenuto push](../push/design-push.md)
   * [Definire contenuto SMS](../sms/create-sms.md#sms-content)
   * [Definire direct mail contenuto](../direct-mail/create-direct-mail.md)
   * [Definire contenuto in-app](../in-app/design-in-app.md)

1. Se stai creando un **[!UICONTROL modello di e-mail]** con il **[!UICONTROL tipo HTML]** , puoi verificare il contenuto. [Scopri come](#test-template)

1. Una volta pronto il modello, fai clic su **[!UICONTROL Salva]**.

1. Fare clic sulla freccia accanto al nome del modello per tornare alla **[!UICONTROL schermata Dettagli]** .

   ![](assets/content-template-back.png)

Questo modello è ora pronto per essere utilizzato durante la creazione di qualsiasi contenuto all&#39;interno di [!DNL Journey Optimizer]. [Scopri come](#use-content-templates)

## Salva contenuto come modello contenuto {#save-as-template}

>[!CONTEXTUALHELP]
>id="ajo_messages_depecrated_inventory"
>title="Scopri come effettuare la migrazione dei messaggi"
>abstract="Il 25 luglio 2022 il menu Messaggi è stato rimosso e i messaggi vengono ora creati direttamente da un percorso. Per riutilizzare i messaggi precedenti nei percorsi, devi salvarli come modelli."

Quando progetti un contenuto in una campagna o in un percorso, puoi salvarlo per riutilizzarlo in futuro. Per farlo, segui la procedura indicata di seguito.

1. Nella schermata Modifica contenuto messaggio **[!UICONTROL , fate clic sulla pulsante Modello]** di ]****[!UICONTROL  contenuto.

1. Seleziona **[!UICONTROL Salva come modello di contenuto]** dal menu a discesa.

   ![](assets/content-template-button-save.png)

   Se ti trovi in [Email Designer](../email/get-started-email-design.md), puoi anche selezionare questa opzione dall&#39;elenco **[!UICONTROL a discesa Altro]** in alto a destra dello schermo.

   ![](assets/content-template-more-button-save.png)

1. Aggiungi un nome e una descrizione per questo modello.

   ![](assets/content-template-name.png)

   >[!NOTE]
   >
   >Il canale e il tipo correnti vengono compilati automaticamente e non possono essere modificati. Per i modelli di e-mail creati da Email Designer](../email/get-started-email-design.md), il [**[!UICONTROL tipo HTML]** viene selezionato automaticamente.

1. Seleziona o crea un Adobe Experience Platform tag dal campo Tag **per categorizzare il** modello. [Ulteriori informazioni](../start/search-filter-categorize.md#tags)

1. Per assegnare etichette di utilizzo dei dati personalizzate o di base al modello, puoi selezionare **[!UICONTROL Gestisci accesso]**. [Ulteriori informazioni](../administration/object-based-access.md).

1. Fai clic su **[!UICONTROL Salva]**.

1. Il modello viene salvato nell&#39;elenco **[!UICONTROL Content Templates]** , accessibile dal [!DNL Journey Optimizer] menu dedicato. Diventa un modello di contenuto autonomo a cui è possibile accedere, modificare ed eliminare come qualsiasi altro elemento in quella lista. [Ulteriori informazioni](#access-manage-templates)

È ora possibile utilizzare questo modello durante la creazione di qualsiasi contenuto all&#39;interno di [!DNL Journey Optimizer]. [Scopri come](#use-content-templates)

>[!NOTE]
>
>Qualsiasi modifica apportata al nuovo modello non viene propagata al contenuto da cui proviene. Analogamente, quando il contenuto originale viene modificato all&#39;interno di tale contenuto, il nuovo modello non viene modificato.
