---
solution: Journey Optimizer
product: journey optimizer
title: Inviare un messaggio agli iscritti
description: Scopri come creare un percorso per inviare un messaggio agli abbonati di un elenco
feature: Journeys, Use Cases, Subscriptions
topic: Content Management
role: User, Developer
level: Intermediate, Experienced
keywords: percorso, caso d’uso, messaggio, abbonati, elenco, lettura
exl-id: 2540938f-8ac7-43fa-83ff-fed59f6bc417
version: Journey Orchestration
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 17%

---

# Inviare un messaggio agli abbonati di un elenco {#send-a-message-to-the-subscribers-of-a-list}

Lo scopo di questo caso d’uso è la creazione di un percorso per inviare un messaggio agli abbonati di un elenco.

In questo esempio viene utilizzato il gruppo di campi **[!UICONTROL Dettagli consenso e preferenze]** di [!DNL Adobe Experience Platform]. Per trovare questo gruppo di campi, scegliere **[!UICONTROL Schemi]** dal menu **[!UICONTROL Gestione dati]**. Nella scheda **[!UICONTROL Gruppi di campi]** immettere il nome del gruppo di campi nel campo di ricerca.

![Questo gruppo di campi include l&#39;elemento subscriptions](assets/consent-and-preference-details-field-group.png)

Per configurare il percorso, eseguire la procedura seguente:

1. Crea un percorso che inizia con un&#39;attività **[!UICONTROL Leggi]**. [Ulteriori informazioni](journey-gs.md).
1. Aggiungi al percorso un&#39;attività di azione **[!UICONTROL E-mail]**. [Ulteriori informazioni](journeys-message.md).
1. Nella sezione **[!UICONTROL Parametri e-mail]** delle impostazioni dell&#39;attività **[!UICONTROL E-mail]**, sostituisci l&#39;indirizzo e-mail predefinito (`PersonalEmail.adress`) con l&#39;indirizzo e-mail degli iscritti all&#39;elenco:

   1. Fai clic sull&#39;icona **[!UICONTROL Abilita sostituzione parametro]** a destra del campo **[!UICONTROL Indirizzo]**, quindi fai clic sull&#39;icona **[!UICONTROL Modifica]**.

      ![](assets/message-to-subscribers-uc-1.png)

   1. Nell’editor espressioni, immetti l’espressione per recuperare gli indirizzi e-mail degli abbonati. [Ulteriori informazioni](expression/expressionadvanced.md).

      Questo esempio mostra un’espressione che include riferimenti ai campi mappa:

      ```json
      #{ExperiencePlatform.Subscriptions.profile.consents.marketing.email.subscriptions.entry('daily-email').subscribers.firstEntryKey()}
      ```

      In questo esempio vengono utilizzate le seguenti funzioni:

      | Funzione | Descrizione | Esempio |
      | --- | --- | --- |
      | `entry` | Fa riferimento a un elemento mappa in base allo spazio dei nomi selezionato | Fai riferimento a un elenco di iscrizioni specifico |
      | `firstEntryKey` | Recupera la prima chiave di ingresso di una mappa | Recupera il primo indirizzo e-mail degli abbonati |

      In questo esempio, l&#39;elenco iscrizioni è denominato `daily-email`. Gli indirizzi di posta elettronica sono definiti come chiavi nella mappa `subscribers`, collegata alla mappa dell&#39;elenco iscrizioni.

      Ulteriori informazioni su [riferimenti ai campi](expression/field-references.md) nelle espressioni.

      ![](assets/message-to-subscribers-uc-2.png)

   1. Nella finestra di dialogo **[!UICONTROL Aggiungi espressione]** fare clic su **[!UICONTROL Ok]**.

>[!CAUTION]
>
>La sostituzione dell’indirizzo e-mail deve essere utilizzata solo per casi d’uso specifici. Nella maggior parte dei casi, non è necessario modificare l’indirizzo e-mail perché il valore definito come indirizzo principale nei **[!UICONTROL campi di esecuzione]** è quello che deve essere utilizzato. [Ulteriori informazioni](../configuration/primary-email-addresses.md)
