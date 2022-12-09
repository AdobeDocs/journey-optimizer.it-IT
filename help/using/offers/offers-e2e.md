---
title: Utilizzare offerte personalizzate in un messaggio e-mail
description: Scopri un esempio end-to-end che mostra tutti i passaggi necessari per configurare le offerte e utilizzarle in un messaggio e-mail.
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 851d988a-2582-4c30-80f3-b881d90771be
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '1065'
ht-degree: 0%

---

# Caso di utilizzo: Configurare offerte personalizzate per utilizzarle in un messaggio e-mail {#configure-add-personalized-offers-email}

Questa sezione presenta un esempio end-to-end per mostrare come configurare le offerte e utilizzarle in un’e-mail, in base a una decisione creata in precedenza.

## Passaggi principali {#main-steps}

I passaggi chiave per configurare le offerte, includerle in una decisione e sfruttare questa decisione in un’e-mail sono elencati di seguito:

1. Prima di creare offerte, [definire i componenti](#define-components)

   * Creare posizionamenti
   * Creare regole decisionali
   * Creare tag
   * Creare classificazioni (facoltativo)

1. [Configurare le offerte](#configure-offers)

   * Creare offerte
   * Per ogni offerta:

      * Crea rappresentazioni e seleziona un posizionamento e una risorsa per ogni rappresentazione
      * Aggiungi una regola per ogni offerta
      * Definire una priorità per ogni offerta

1. [Creare un’offerta di fallback](#create-fallback)

1. [Creare una raccolta](#create-collection) per includere le offerte personalizzate create

1. [Configurare la decisione](#configure-decision)

   * Creare una decisione
   * Selezionare i posizionamenti creati
   * Per ogni posizionamento, seleziona la raccolta
   * Per ogni posizionamento, seleziona una classificazione (facoltativo)
   * Selezionare il fallback

1. [Inserire la decisione in un messaggio e-mail](#insert-decision-in-email)

   * Selezionare un posizionamento corrispondente alle offerte che si desidera visualizzare
   * Seleziona la decisione tra gli elementi compatibili con il posizionamento selezionato
   * Anteprima delle offerte

Il processo decisionale complessivo per l’utilizzo delle offerte in un messaggio e-mail può essere descritto come segue:

![](assets/offers-e2e-process.png)

## Definire i componenti {#define-components}

Prima di iniziare a creare le offerte, devi definire diversi componenti da utilizzare nelle offerte.

Li troverai sotto il **[!UICONTROL Decision Management]** > **[!UICONTROL Components menu]**.

1. Inizia creando **posizionamenti** per le offerte.

   Utilizzerai questi posizionamenti per definire dove verrà visualizzata l’offerta risultante durante la definizione della decisione di offerta.

   In questo esempio, crea tre posizionamenti con i seguenti tipi di canale e contenuto:

   * *Web - Immagine*
   * *E-mail - Immagine*
   * *Non digitale - Testo*

   ![](assets/offers-e2e-placements.png)

   I passaggi dettagliati per la creazione dei posizionamenti sono descritti in [questa sezione](../../using/offers/offer-library/creating-placements.md).

1. Crea **norme decisionali**.

   Le regole decisionali forniscono l’offerta migliore a un profilo in Adobe Experience Platform.

   Configura due semplici regole utilizzando la **[!UICONTROL XDM Individual Profile > Person > Gender]** attributo:

   * *Clienti Femminili*
   * *Clienti maschili*

   ![](assets/offers-e2e-rules.png)

   I passaggi dettagliati per la creazione delle regole sono descritti in [questa sezione](../../using/offers/offer-library/creating-decision-rules.md).

1. Puoi anche creare un **tag**.

   Potrai quindi associarlo alle offerte e utilizzare questo tag per raggruppare le offerte in una raccolta.

   In questo esempio, crea le *Yoga* tag .

   ![](assets/offers-e2e-tag.png)

   I passaggi dettagliati per la creazione dei tag sono descritti in [questa sezione](../../using/offers/offer-library/creating-tags.md).

1. Se desideri definire regole che determinino quale offerta deve essere presentata per prima per un determinato posizionamento (anziché tenere conto dei punteggi di priorità delle offerte), puoi creare un **formula di classificazione**.

   I passaggi dettagliati per la creazione di formule di classificazione sono descritti in [questa sezione](../../using/offers/ranking/create-ranking-formulas.md#create-ranking-formula).

   >[!NOTE]
   >
   >In questo esempio, utilizzeremo solo i punteggi di priorità. Ulteriori informazioni su [regole di idoneità e vincoli](../../using/offers/offer-library/creating-personalized-offers.md#eligibility).

## Configurare le offerte {#configure-offers}

Ora puoi creare e configurare le offerte. In questo esempio, creerai quattro offerte da visualizzare in base a ciascun profilo specifico.

1. Crea un’offerta. Ulteriori informazioni in [questa sezione](../../using/offers/offer-library/creating-personalized-offers.md#create-offer).

1. In questa offerta, crea tre rappresentazioni. Ogni rappresentazione deve essere una combinazione di un posizionamento creato in precedenza e di una risorsa:

   * Uno corrispondente al *Web - Immagine* placement
   * Uno corrispondente al *E-mail - Immagine* placement
   * Uno corrispondente al *Non digitale - Testo* placement

   >[!NOTE]
   >
   >Un’offerta può essere visualizzata in posizioni diverse all’interno di un messaggio per creare ulteriori opportunità di utilizzo in contesti di posizionamento diversi.

   Ulteriori informazioni sulle rappresentazioni in [questa sezione](../../using/offers/offer-library/creating-personalized-offers.md#representations).

1. Seleziona un’immagine appropriata per i primi due posizionamenti. Immetti un testo personalizzato per la *Non digitale - Testo* posizionamento.

   ![](assets/offers-e2e-representations.png)

1. In **[!UICONTROL Offer eligibility]** sezione , seleziona **[!UICONTROL By defined decision rule]** e trascina e rilascia la regola scelta.

   ![](assets/offers-e2e-eligibility.png)

1. Compila il **[!UICONTROL Priority]**. In questo esempio, aggiungi *25*.

1. Rivedi l’offerta, quindi fai clic su **[!UICONTROL Save and approve]**.

   ![](assets/offers-e2e-review.png)

1. In questo esempio, crea altre tre offerte con le stesse rappresentazioni, ma risorse diverse. Assegnali con regole e priorità diverse, ad esempio:

   * Prima offerta - Regola decisionale: *Clienti Femminili*, Priorità: *25*
   * Seconda offerta - Regola decisionale: *Clienti Femminili*, Priorità: *15*
   * Terza offerta - Regola decisionale: *Clienti maschili*, Priorità: *25*
   * Quarta offerta - Regola decisionale: *Clienti maschili*, Priorità: *15*

   ![](assets/offers-e2e-offers-created.png)

I passaggi dettagliati per la creazione e la configurazione delle offerte sono descritti in [questa sezione](../../using/offers/offer-library/creating-personalized-offers.md).

## Creare un’offerta di fallback {#create-fallback}

1. Crea un’offerta di fallback.

1. Definisci le stesse rappresentazioni delle offerte, con le risorse appropriate (devono essere diverse da quelle utilizzate nelle offerte).

   Ogni rappresentazione deve essere una combinazione di un posizionamento creato in precedenza e di una risorsa:

   * Uno corrispondente al *Web - Immagine* placement
   * Uno corrispondente al *E-mail - Immagine* placement
   * Uno corrispondente al *Non digitale - Testo* placement

   ![](assets/offers-e2e-fallback-representations.png)

1. Rivedi l’offerta di fallback, quindi fai clic su **[!UICONTROL Save and approve]**.

![](assets/offers-e2e-fallback.png)

L’offerta di fallback è ora pronta per essere utilizzata in una decisione.

I passaggi dettagliati per la creazione e la configurazione di un’offerta di fallback sono descritti in [questa sezione](../../using/offers/offer-library/creating-fallback-offers.md).

## Creare una raccolta {#create-collection}

Quando configuri la decisione, dovrai aggiungere le offerte personalizzate come parte di una raccolta.

1. Per accelerare il processo decisionale, crea una raccolta dinamica.

1. Utilizza la *Yoga* per selezionare le quattro offerte personalizzate create in precedenza.

   ![](assets/offers-e2e-collection-using-tag.png)

I passaggi dettagliati per la creazione di una raccolta sono descritti in [questa sezione](../../using/offers/offer-library/creating-collections.md).

## Configurare la decisione {#configure-decision}

Ora devi creare una decisione che combini i posizionamenti con le offerte personalizzate e l’offerta di fallback appena creata.

Questa combinazione verrà utilizzata dal motore decisionale per trovare l’offerta migliore per un profilo specifico: in questo esempio, si baserà sulla priorità e sulla regola decisionale che hai assegnato a ogni offerta.

Per creare e configurare una decisione di offerta, segui i passaggi principali seguenti:

1. Crea una decisione. Ulteriori informazioni in [questa sezione](../../using/offers/offer-activities/create-offer-activities.md#create-activity).

1. Seleziona la *Web - Immagine*, *E-mail - Immagine* e *Non digitale - Testo* posizionamenti.

   ![](assets/offers-e2e-decision-placements.png)

1. Per ogni posizionamento, aggiungi la raccolta creata.

   ![](assets/offers-e2e-decision-collection.png)

1. Se hai definito una classificazione quando [creazione di componenti](#define-components), puoi assegnarlo a un posizionamento nella decisione. Se più offerte sono idonee per essere presentate in questo posizionamento, la decisione utilizzerà questa formula per calcolare quale offerta distribuire per prima.

   I passaggi dettagliati per assegnare una formula di classificazione a un posizionamento sono descritti in [questa sezione](../../using/offers/offer-activities/configure-offer-selection.md#assign-ranking-formula).

1. Seleziona l’offerta di fallback creata. Sarà visualizzato come offerta di fallback disponibile per i tre posizionamenti selezionati.

   ![](assets/offers-e2e-decision-fallback.png)

1. Rivedi la tua decisione, quindi fai clic su **[!UICONTROL Save and approve]**.

   ![](assets/offers-e2e-review-decision.png)

La tua decisione è ora pronta per essere utilizzata per fornire offerte ottimizzate e personalizzate.

I passaggi dettagliati per la creazione e la configurazione di una decisione sono descritti in [questa sezione](../../using/offers/offer-activities/create-offer-activities.md).

## Inserire la decisione in un messaggio e-mail {#insert-decision-in-email}

Ora che la tua decisione è attiva, puoi inserirla in un messaggio e-mail. A tale scopo, segui i passaggi descritti in [questa pagina](../../using/email/add-offers-email.md).

![](assets/offers-e2e-offers-displayed.png)
