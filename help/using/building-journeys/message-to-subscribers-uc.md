---
title: Inviare un messaggio agli abbonati
description: Scopri come creare un percorso per inviare un messaggio agli abbonati di un elenco
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 2540938f-8ac7-43fa-83ff-fed59f6bc417
source-git-commit: 3c8c059e5e3953807b9fc2d8d0eded0d00e49003
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 5%

---

# Caso di utilizzo: inviare un messaggio agli abbonati di un elenco{#send-a-message-to-the-subscribers-of-a-list}

Lo scopo di questo caso d’uso è quello di creare un percorso per inviare un messaggio agli abbonati di un elenco.

In questo esempio, la **[!UICONTROL Consent and Preference Details]** gruppo di campi da [!DNL Adobe Experience Platform] viene utilizzato. Per trovare questo gruppo di campi, dal **[!UICONTROL Data Management]** menu, scegli **[!UICONTROL Schemas]**. Sulla **[!UICONTROL Field groups]** immettere il nome del gruppo di campi nel campo di ricerca.

![Questo gruppo di campi include l&#39;elemento subscriptions](../assets/consent-and-preference-details-field-group.png)

Per configurare questo percorso, effettua le seguenti operazioni:

1. Crea un percorso che inizia con un **[!UICONTROL Read]** attività. [Ulteriori informazioni](journey-gs.md).
1. Aggiungi un **[!UICONTROL Message]** attività , con un messaggio e-mail, al percorso. [Ulteriori informazioni](journeys-message.md).
1. In **[!UICONTROL Email parameters]** della sezione **[!UICONTROL Message]** impostazioni dell’attività, sostituisci l’indirizzo e-mail predefinito (`PersonalEmail.adress`) con l&#39;indirizzo e-mail degli abbonati all&#39;elenco:

   1. Fai clic sul pulsante **[!UICONTROL Enable parameter override]** a destra del **[!UICONTROL Address]** quindi fai clic sul campo **[!UICONTROL Edit]** icona.

      ![](../assets/message-to-subscribers-uc-1.png)

      Per poter modificare l’indirizzo e-mail, devi aver pubblicato il messaggio in precedenza.

   1. Nell’editor espressioni, immetti l’espressione per recuperare gli indirizzi e-mail degli abbonati. [Ulteriori informazioni](expression/expressionadvanced.md).

      Questo esempio mostra un&#39;espressione che include riferimenti ai campi di mappatura:

      ```json
      #{ExperiencePlatform.Subscriptions.profile.consents.marketing.email.subscriptions.entry('daily-email').subscribers.firstEntryKey()}
      ```

      In questo esempio vengono utilizzate le seguenti funzioni:

      | Funzione | Descrizione | Esempio |
      | --- | --- | --- |
      | `entry` | Fai riferimento a un elemento mappa in base allo spazio dei nomi selezionato | Fai riferimento a un elenco di abbonamenti specifico |
      | `firstEntryKey` | Recupera la prima chiave di ingresso di una mappa | Recupera il primo indirizzo e-mail degli abbonati |

      In questo esempio, l’elenco di sottoscrizioni è denominato `daily-email`. Gli indirizzi e-mail sono definiti come chiavi nel `subscribers` map, collegata alla mappa dell’elenco di abbonamenti.

      Ulteriori informazioni [riferimenti ai campi](expression/field-references.md) nelle espressioni.

      ![](../assets/message-to-subscribers-uc-2.png)

   1. In **[!UICONTROL Add an expression]** finestra di dialogo, fai clic su **[!UICONTROL Ok]**.

   ![](../assets/message-to-subscribers-uc-3.png)

1. Termina il percorso con un **[!UICONTROL End]** attività.
