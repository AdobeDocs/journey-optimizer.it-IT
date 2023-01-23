---
solution: Journey Optimizer
product: journey optimizer
title: Inviare un messaggio agli abbonati
description: Scopri come creare un percorso per inviare un messaggio agli abbonati di un elenco
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: percorso, caso d'uso, messaggio, abbonati, elenco, lettura
exl-id: 2540938f-8ac7-43fa-83ff-fed59f6bc417
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 4%

---

# Caso di utilizzo: inviare un messaggio agli abbonati di un elenco{#send-a-message-to-the-subscribers-of-a-list}

Lo scopo di questo caso d’uso è quello di creare un percorso per inviare un messaggio agli abbonati di un elenco.

In questo esempio, la **[!UICONTROL Dettagli su consenso e preferenza]** gruppo di campi da [!DNL Adobe Experience Platform] viene utilizzato. Per trovare questo gruppo di campi, dal **[!UICONTROL Gestione dati]** menu, scegli **[!UICONTROL Schemi]**. Sulla **[!UICONTROL Gruppi di campi]** immettere il nome del gruppo di campi nel campo di ricerca.

![Questo gruppo di campi include l&#39;elemento subscriptions](assets/consent-and-preference-details-field-group.png)

Per configurare questo percorso, effettua le seguenti operazioni:

1. Crea un percorso che inizia con un **[!UICONTROL Leggi]** attività. [Ulteriori informazioni](journey-gs.md).
1. Aggiungi un **[!UICONTROL E-mail]** attività di azione al percorso. [Ulteriori informazioni](journeys-message.md).
1. In **[!UICONTROL Parametri e-mail]** della sezione **[!UICONTROL E-mail]** impostazioni dell’attività, sostituisci l’indirizzo e-mail predefinito (`PersonalEmail.adress`) con l&#39;indirizzo e-mail degli abbonati all&#39;elenco:

   1. Fai clic sul pulsante **[!UICONTROL Abilita sostituzione parametro]** a destra del **[!UICONTROL Indirizzo]** quindi fai clic sul campo **[!UICONTROL Modifica]** icona.

      ![](assets/message-to-subscribers-uc-1.png)

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

      ![](assets/message-to-subscribers-uc-2.png)

   1. In **[!UICONTROL Aggiungi un’espressione]** finestra di dialogo, fai clic su **[!UICONTROL Ok]**.
