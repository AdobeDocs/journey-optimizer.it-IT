---
solution: Journey Optimizer
product: journey optimizer
title: Creare modelli di contenuto
description: Scopri come creare modelli per riutilizzare i contenuti nelle campagne e nei percorsi Journey Optimizer
feature: Templates
topic: Content Management
role: User
level: Beginner
exl-id: a205539b-b7ea-4832-92b0-49637c4dac47
TQID: https://experienceleague.adobe.com/E9gFX9CtjkzhDBeVqcaOE-7kNWygH2CVIikDLZ3ZqR8
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a653cc2e-bc85-4353-a306-399e5b247978id: d998adac-2f81-400b-a669-d07bb196e4ebid: dc22c819-3f29-4e91-8b7d-5c6719831141id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2: id: d595a60b-bcf5-4a63-a189-66a0be755cc7id: ee5bb250-0884-4d71-86eb-d8489e8bcaddid: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 633
ht-degree: 12%

---

# Creare modelli di contenuto {#create-content-templates}

>[!CONTEXTUALHELP]
>id="ajo_create_template"
>title="Definire un modello di contenuto personalizzato"
>abstract="Crea da zero un modello personalizzato autonomo per rendere i contenuti riutilizzabili in più percorsi e campagne."

Esistono due modi per creare modelli di contenuto:

* Crea un modello di contenuto da zero utilizzando la barra a sinistra del menu **[!UICONTROL Modelli di contenuto]**. [Scopri come](#create-template-from-scratch)

* Quando progetti il contenuto all’interno di una campagna o di un percorso, salvalo come modello. [Scopri come](#save-as-template)

Una volta salvato, il modello di contenuto è disponibile per l’utilizzo in una campagna o in un percorso. Indipendentemente dal fatto che sia stato creato da zero o da contenuto precedente, è possibile utilizzare questo modello per creare qualsiasi contenuto in [!DNL Journey Optimizer]. [Scopri come](#use-content-templates)

>[!NOTE]
>
>* Le modifiche apportate ai modelli di contenuto non vengono propagate a campagne o percorsi, sia che siano live o bozze.
>
>* Allo stesso modo, quando i modelli vengono utilizzati in una campagna o in un percorso, eventuali modifiche apportate al contenuto della campagna e del percorso non influiscono sul modello di contenuto utilizzato in precedenza.

## Crea modello da zero {#create-template-from-scratch}

>[!NOTE]
>
>A partire da marzo 2025, i modelli di contenuto di tipo HTML sono diventati obsoleti. È comunque possibile utilizzare i modelli di contenuto HTML esistenti creati in precedenza in [!DNL Journey Optimizer].

Per creare un modello di contenuto da zero, effettua le seguenti operazioni.

1. Accedi all&#39;elenco dei modelli di contenuto tramite il menu a sinistra **[!UICONTROL Gestione contenuto]** > **[!UICONTROL Modelli di contenuto]**.

1. Seleziona **[!UICONTROL Crea modello]**.

1. Inserisci i dettagli del modello e seleziona il canale desiderato.

   ![](assets/content-template-channels.png)

   >[!NOTE]
   >
   >Attualmente sono disponibili tutti i canali eccetto Web.

1. Seleziona o crea tag Adobe Experience Platform dal campo **[!UICONTROL Tag]** per categorizzare il modello ai fini di una ricerca migliorata. [Ulteriori informazioni](../start/search-filter-categorize.md#tags)

1. Per assegnare etichette di utilizzo dei dati personalizzate o di base al modello, selezionare **[!UICONTROL Gestisci accesso]**. [Ulteriori informazioni sul controllo degli accessi a livello di oggetto](../administration/object-based-access.md).

1. Fai clic su **[!UICONTROL Crea]** e progetta il contenuto in base alle esigenze, nello stesso modo in cui crei qualsiasi contenuto all&#39;interno di un percorso o di una campagna, in base al canale selezionato.

   ![](assets/content-template-edition.png)

   Scopri come creare contenuti per i diversi canali nelle sezioni seguenti:
   * [Definire il contenuto delle e-mail](../email/get-started-email-design.md)
   * [Definire il contenuto push](../push/design-push.md)
   * [Definire il contenuto degli SMS](../sms/create-sms.md#sms-content)
   * [Definire il contenuto della direct mailing](../direct-mail/create-direct-mail.md)
   * [Definire il contenuto in-app](../in-app/design-in-app.md)
   * [Definisci contenuto Web](../web/create-web.md#edit-web-content)
   * [Definire contenuti di esperienza basati su codice](../code-based/create-code-based.md)

     >[!NOTE]
     >
     >Puoi aggiungere criteri di decisione a modelli di contenuto di esperienze basati su codice. [Ulteriori informazioni](../experience-decisioning/create-decision.md#create-decision)

1. Puoi verificare il contenuto. [Scopri come](#test-template)

1. Quando il modello è pronto, fai clic su **[!UICONTROL Salva]**.

1. Fai clic sulla freccia accanto al nome del modello per tornare alla schermata **[!UICONTROL Dettagli]**.

   ![](assets/content-template-back.png)

Questo modello è ora pronto per essere utilizzato quando si crea qualsiasi contenuto in [!DNL Journey Optimizer]. [Scopri come](#use-content-templates)

>[!NOTE]
>
>Quando crei un modello di contenuto e-mail, puoi applicare rapidamente uno stile specifico che si adatta al tuo marchio e design applicando un tema al contenuto. [Ulteriori informazioni](../email/apply-email-themes.md)

## Salvare il contenuto come modello di contenuto {#save-as-template}

Durante la progettazione di qualsiasi contenuto in una campagna o in un percorso, puoi salvarlo per un riutilizzo futuro. Per farlo, segui la procedura indicata di seguito.

1. Dalla schermata **[!UICONTROL Modifica contenuto]** del messaggio, fare clic sul pulsante **[!UICONTROL Modello contenuto]**.

1. Seleziona **[!UICONTROL Salva come modello di contenuto]** dal menu a discesa.

   ![](assets/content-template-button-save.png)

   Se ti trovi in [E-mail Designer](../email/get-started-email-design.md), puoi anche selezionare questa opzione dall&#39;elenco a discesa **[!UICONTROL Altro]** nell&#39;angolo in alto a destra dello schermo.

   ![](assets/content-template-more-button-save.png)

1. Aggiungi un nome e una descrizione per questo modello.

   ![](assets/content-template-name.png)

   >[!NOTE]
   >
   >Il canale corrente viene compilato automaticamente e non può essere modificato.

1. Seleziona o crea un tag Adobe Experience Platform dal campo **Tag** per categorizzare il modello. [Ulteriori informazioni](../start/search-filter-categorize.md#tags)

1. Per assegnare etichette di utilizzo dei dati personalizzate o di base al modello, selezionare **[!UICONTROL Gestisci accesso]**. [Ulteriori informazioni](../administration/object-based-access.md).

1. Fai clic su **[!UICONTROL Salva]**.

1. Il modello viene salvato nell&#39;elenco **[!UICONTROL Modelli di contenuto]**, accessibile dal menu dedicato [!DNL Journey Optimizer]. Diventa un modello di contenuto autonomo accessibile, modificato ed eliminato come qualsiasi altro elemento dell’elenco. [Ulteriori informazioni](#access-manage-templates)

È ora possibile utilizzare questo modello per creare qualsiasi contenuto in [!DNL Journey Optimizer]. [Scopri come](#use-content-templates)

>[!NOTE]
>
>Qualsiasi modifica apportata al nuovo modello non viene propagata al contenuto da cui proviene. Analogamente, quando si modifica il contenuto originale, il nuovo modello non viene modificato.

