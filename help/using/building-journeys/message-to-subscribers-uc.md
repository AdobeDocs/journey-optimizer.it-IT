---
solution: Journey Optimizer
product: journey optimizer
title: Inviare un messaggio agli abbonati
description: Scopri come creare un percorso per inviare un messaggio agli abbonati di un elenco
feature: Journeys, Use Cases, Subscriptions
topic: Content Management
role: User, Data Engineer
level: Intermediate, Experienced
keywords: percorso, caso d’uso, messaggio, abbonati, elenco, lettura
exl-id: 2540938f-8ac7-43fa-83ff-fed59f6bc417
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 17%

---

# Caso d’uso: inviare un messaggio agli abbonati di un elenco{#send-a-message-to-the-subscribers-of-a-list}

Lo scopo di questo caso d’uso è la creazione di un percorso per inviare un messaggio agli abbonati di un elenco.

In questo esempio, la proprietà **[!UICONTROL Dettagli su consenso e preferenze]** gruppo di campi da [!DNL Adobe Experience Platform] viene utilizzato. Per trovare questo gruppo di campi, dal **[!UICONTROL Gestione dati]** menu, scegliere **[!UICONTROL Schemi]**. Il giorno **[!UICONTROL Gruppi di campi]** , immettere il nome del gruppo di campi nel campo di ricerca.

![Questo gruppo di campi include l&#39;elemento subscriptions](assets/consent-and-preference-details-field-group.png)

Per configurare il percorso, eseguire la procedura seguente:

1. Creare un percorso che inizia con **[!UICONTROL Letto]** attività. [Ulteriori informazioni](journey-gs.md).
1. Aggiungi un **[!UICONTROL E-mail]** attività al percorso. [Ulteriori informazioni](journeys-message.md).
1. In **[!UICONTROL Parametri e-mail]** sezione del **[!UICONTROL E-mail]** , sostituisci l&#39;indirizzo e-mail predefinito (`PersonalEmail.adress`) con l’indirizzo e-mail degli iscritti all’elenco:

   1. Fai clic su **[!UICONTROL Abilita sostituzione parametro]** a destra della **[!UICONTROL Indirizzo]** , quindi fare clic sul pulsante **[!UICONTROL Modifica]** icona.

      ![](assets/message-to-subscribers-uc-1.png)

   1. Nell’editor espressioni, immetti l’espressione per recuperare gli indirizzi e-mail degli abbonati. [Ulteriori informazioni](expression/expressionadvanced.md).

      Questo esempio mostra un’espressione che include riferimenti ai campi mappa:

      ```json
      #{ExperiencePlatform.Subscriptions.profile.consents.marketing.email.subscriptions.entry('daily-email').subscribers.firstEntryKey()}
      ```

      In questo esempio vengono utilizzate le seguenti funzioni:

      | Funzione | Descrizione | Esempio |
      | --- | --- | --- |
      | `entry` | Fai riferimento a un elemento mappa in base allo spazio dei nomi selezionato | Fai riferimento a un elenco di iscrizioni specifico |
      | `firstEntryKey` | Recuperare la prima chiave di ingresso di una mappa | Recupera il primo indirizzo e-mail degli abbonati |

      In questo esempio, l’elenco degli abbonamenti è denominato `daily-email`. Gli indirizzi e-mail sono definiti come chiavi nella `subscribers` mappa, collegata alla mappa dell’elenco di iscrizioni.

      Ulteriori informazioni su [riferimenti ai campi](expression/field-references.md) nelle espressioni.

      ![](assets/message-to-subscribers-uc-2.png)

   1. In **[!UICONTROL Aggiungi un’espressione]** , fare clic su **[!UICONTROL Ok]**.

>[!CAUTION]
>
>La sostituzione dell’indirizzo e-mail deve essere utilizzata solo per casi d’uso specifici. Nella maggior parte dei casi, non è necessario modificare l’indirizzo e-mail perché il valore definito come indirizzo principale nei **[!UICONTROL campi di esecuzione]** è quello che deve essere utilizzato. [Ulteriori informazioni](../configuration/primary-email-addresses.md)
