---
solution: Journey Optimizer
product: journey optimizer
title: Elenchi seed
description: Scopri come utilizzare gli elenchi di seed in Journey Optimizer
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
keywords: elenco seed, elenco seed, seed, configurazione
source-git-commit: 49c283fc19d90b5ced896c5854325266d80e8bc2
workflow-type: tm+mt
source-wordcount: '912'
ht-degree: 2%

---

# Usa elenchi seed {#seed-lists}

Elenchi seed in [!DNL Journey Optimizer] consente di includere automaticamente indirizzi di seed specifici nelle consegne.

>[!CAUTION]
>
>Attualmente questa funzione si applica solo al canale e-mail.

Gli indirizzi di seed vengono utilizzati per eseguire il targeting di destinatari che non corrispondono ai criteri di target definiti. In questo modo, i destinatari che non rientrano nell’ambito di consegna possono ricevere la consegna, come farebbe qualsiasi altro destinatario.

Gli indirizzi di seed non sono profili reali né profili di test in quanto non includono dettagli di profilo. Sono solo destinatari appartenenti alle parti interessate interne memorizzate nel sistema. Se selezionati in una campagna o in un percorso specifico, vengono inclusi al momento dell’esecuzione della consegna, il che significa che riceveranno una copia della consegna a scopo di garanzia.

* Ricevendo le consegne contemporaneamente e nelle stesse condizioni dei clienti, gli elenchi di seed ti consentono di monitorare le copie e-mail inviate, per verificare che tutti i formati di visualizzazione, le immagini e i collegamenti siano corretti e di tenere traccia dei messaggi effettivi inviati ai destinatari.

  Ad esempio:

+++ Se sei un responsabile marketing:

  Si desidera che tutti i membri del gruppo ricevano copie dei messaggi inviati contemporaneamente ai clienti. In questo modo il tuo team può garantire che i messaggi vengano inviati con il layout previsto, gli URL attivi, il testo e le immagini corretti, come pianificato prima dell’esecuzione.

+++

+++ Se sei il proprietario di un prodotto:

  È necessario tenere traccia dei messaggi effettivi inviati ai clienti. Infatti, il tuo team e la tua leadership potrebbero essere interessati ad alcune campagne e dovranno essere aggiunti dati ad hoc per ricevere copie del messaggio al momento della consegna.

+++

* Un altro motivo per utilizzare gli elenchi di seed è la protezione della mailing list. L’inserimento di indirizzi di seed nella mailing list ti consente di notare se è utilizzato da una terza parte, in quanto gli indirizzi di seed in esso contenuti riceveranno le consegne inviate alla mailing list.

## Accedere agli elenchi di seed {#access-seed-lists}

Per accedere agli elenchi di seed già creati, vai a **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]** > **[!UICONTROL Configurazione e-mail]**, e seleziona **[!UICONTROL Elenco seed]**.

<!--
>[!CAUTION]
>
>Permissions to view, export and manage the seed lists are restricted to [Journey Administrators](../administration/ootb-product-profiles.md#journey-administrator). Learn more on managing [!DNL Journey Optimizer] users' access rights in [this section](../administration/permissions-overview.md).-->

>[!CAUTION]
>
>Per poter visualizzare, modificare e gestire gli elenchi di seed, è necessario disporre del **[!UICONTROL Gestisci elenco seed]** autorizzazione.

![](assets/seed-list-access.png)

Puoi cercare gli elenchi di seed per nome e/o filtro in base all’utente che ha creato l’elenco o alla data di creazione. Una volta selezionato, puoi cancellare il filtro visualizzato sopra l’elenco.

![](assets/seed-list-filtering.png)

Utilizza il **[!UICONTROL Elimina]** per rimuovere definitivamente una voce.

>[!CAUTION]
>
>Non è possibile eliminare un elenco di seed utilizzato in un [campagna](../campaigns/review-activate-campaign.md) o [percorso](../building-journeys/publishing-the-journey.md). È necessario disattivare la campagna/il percorso o modificarlo per utilizzare un&#39;altra superficie che non abbia selezionato l&#39;elenco di seed. [Ulteriori informazioni sull&#39;utilizzo di un elenco di seed](#use-seed-list)

È possibile fare clic sul nome di un elenco di seed per modificarlo. <!--Use the **[!UICONTROL Edit]** button to edit a seed list.-->

## Creare un elenco di seed {#create-seed-list}

>[!CONTEXTUALHELP]
>id="ajo_seed_list_details"
>title="Definire un elenco di seed"
>abstract="Utilizza un elenco di seed per aggiungere automaticamente indirizzi interni specifici al pubblico di consegna a scopo di garanzia. Gli elenchi di seed consentono di monitorare le copie dei messaggi inviate, per verificare che tutti gli elementi di visualizzazione siano corretti e per proteggere la mailing list. Attualmente questa funzione si applica solo al canale e-mail."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/seed-lists.html#use-seed-list" text="Cosa sono gli elenchi di seed?"

>[!CONTEXTUALHELP]
>id="ajo_seed_addresses"
>title="Compila l’elenco seed"
>abstract="Seleziona gli indirizzi che verranno inclusi al momento dell’esecuzione della consegna e riceveranno una copia esatta del messaggio. Puoi importare un file CSV o immettere manualmente gli indirizzi e-mail."

Per creare un elenco di seed, attieniti alla procedura seguente.

1. Accedere a **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]** > **[!UICONTROL Configurazione e-mail]** > **[!UICONTROL Elenco seed]** menu.

1. Seleziona la **[!UICONTROL Crea elenco seed]** pulsante.

   ![](assets/seed-list-create-button.png)

1. Compila i dettagli. Inizia aggiungendo un nome.

   ![](assets/seed-list-details.png)

   >[!NOTE]
   >
   >I nomi devono iniziare con una lettera (A-Z) e includere solo caratteri alfanumerici o caratteri speciali ( _, ., -).

1. Seleziona il canale. Attualmente è disponibile solo il canale e-mail.

1. Seleziona un profilo di test. Poiché gli indirizzi di seed non includono i dettagli del profilo, questo profilo di test verrà utilizzato solo per visualizzare i dati di personalizzazione nel messaggio inviato agli indirizzi di seed.

   >[!NOTE]
   >
   >È possibile selezionare un solo profilo di test alla volta.

1. Aggiungi gli indirizzi di seed a cui desideri inviare le consegne. Puoi importare un file CSV o immettere manualmente gli indirizzi e-mail.

   ![](assets/seed-list-email-addresses.png)

   >[!NOTE]
   >
   >È possibile combinare entrambe le opzioni, ma il numero totale di indirizzi in un elenco di seed non può superare i 50.

1. Clic **[!UICONTROL Crea]** per confermare. L’elenco dei valori iniziali appena creato viene visualizzato nel [Schermata Elenco seed](#access-seed-lists).

## Utilizzare un elenco di seed in una campagna o in un percorso {#use-seed-list}

Una volta creato l’elenco di seed, puoi utilizzarlo in qualsiasi campagna o percorso per includere gli indirizzi di seed corrispondenti nelle consegne. A questo scopo, segui i passaggi riportati qui sotto.

>[!CAUTION]
>
>I messaggi inviati agli indirizzi seed non sono inclusi nei rapporti.

1. Create una superficie e selezionate **[!UICONTROL E-mail]** canale. [Ulteriori informazioni](../email/email-settings.md)

1. Selezionare l&#39;elenco di seed desiderato nel [sezione corrispondente](../email/email-settings.md#seed-list).

   >[!NOTE]
   >
   >È possibile selezionare un solo elenco di seed alla volta.

   ![](assets/seed-list-surface.png)

1. Sottomettere la superficie.

1. Creare un [campagna](../campaigns/create-campaign.md) o un [percorso](../building-journeys/journey-gs.md).

1. Seleziona la **[!UICONTROL E-mail]** e seleziona la [superficie](channel-surfaces.md) incluso l’elenco di seed che è rilevante per te.

   ![](assets/seed-list-campaign-email.png)

1. Attiva [campagna](../campaigns/review-activate-campaign.md) o pubblicare [percorso](../building-journeys/publishing-the-journey.md).

Ora, ogni volta che un messaggio e-mail viene inviato ai clienti tramite tale campagna o percorso, anche gli indirizzi e-mail nell’elenco di seed selezionato lo riceveranno nelle stesse condizioni, contemporaneamente e con lo stesso contenuto dei destinatari target.

>[!NOTE]
>
>Per i percorsi la consegna e-mail viene inviata agli indirizzi seed solo il percorso della prima esecuzione.

