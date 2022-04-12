---
title: Regole di frequenza
description: Scopri come definire le regole di frequenza
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 49248fb6-5a91-45b2-9de8-2f078d59c0fc
source-git-commit: f1ac47a0cb405eaadc5428e7e5479eaf776d7abe
workflow-type: tm+mt
source-wordcount: '762'
ht-degree: 1%

---

# Regole di frequenza dei messaggi {#frequency-rules}

[!DNL Journey Optimizer] consente di controllare la frequenza con cui gli utenti ricevono un messaggio o accedono a un percorso impostando regole cross-channel che escludono automaticamente i profili sollecitati in eccesso dai messaggi e dalle azioni.

Ad esempio, non vuoi che il tuo marchio invii più di 3 messaggi di marketing al mese ai loro clienti.

A questo scopo, puoi utilizzare una regola di frequenza che limiti il numero di messaggi inviati in base a uno o più canali durante un periodo di calendario mensile.

>[!NOTE]
>
>Le regole di frequenza dei messaggi sono diverse dalla gestione della rinuncia, che consente agli utenti di annullare l’iscrizione alla ricezione di comunicazioni da un marchio. [Ulteriori informazioni](../messages/consent.md#opt-out-management)

## Regole di accesso {#access-rules}

Le regole sono disponibili dal **[!UICONTROL Administration]** > **[!UICONTROL Rules]** menu. Vengono elencate tutte le regole, ordinate per data di modifica.

>[!NOTE]
>
>Per accedere, creare, modificare o eliminare le regole di frequenza dei messaggi, devi disporre della [Gestire le regole di frequenza](../administration/high-low-permissions.md#manage-frequency-rules) autorizzazione.

![](assets/message-rules-access.png)

Utilizza l’icona del filtro per filtrare in base alla categoria, allo stato e/o al canale. Puoi anche effettuare ricerche nell’etichetta del messaggio.

![](assets/message-rules-filter.png)

## Creare una regola {#create-new-rule}

Per creare una nuova regola, segui i passaggi seguenti.

1. Accedere al **[!UICONTROL Message frequency rules]** elenco, quindi fai clic su **[!UICONTROL Create rule]**.

   ![](assets/message-rules-create.png)

1. Definisci il nome della regola.

   ![](assets/message-rules-details.png)

1. Seleziona la categoria della regola del messaggio.

   >[!NOTE]
   >
   >Attualmente solo il **[!UICONTROL Marketing]** categoria disponibile.

1. Imposta il limite per la regola, ovvero il numero massimo di messaggi che possono essere inviati a un singolo profilo utente ogni mese.

   ![](assets/message-rules-capping.png)

   >[!NOTE]
   >
   >Il limite di frequenza è basato su un periodo di calendario mensile. Viene reimpostato all&#39;inizio di ogni mese.

1. Seleziona il canale da utilizzare per questa regola: **[!UICONTROL Email]** o **[!UICONTROL Push notification]**.

   ![](assets/message-rules-channels.png)

   >[!NOTE]
   >
   >Per poter creare la regola, devi selezionare almeno un canale.

1. Seleziona diversi canali se desideri applicare un limite a tutti i canali selezionati come conteggio totale.

   Ad esempio, imposta il limite a 15 e seleziona sia i canali e-mail che i canali push. Se un profilo ha già ricevuto 10 e-mail di marketing e 5 notifiche push di marketing, verrà escluso dalla consegna immediatamente successiva di qualsiasi e-mail di marketing o notifica push.

1. Fai clic su **[!UICONTROL Save as draft]** per confermare la creazione della regola. Il messaggio viene aggiunto nell’elenco delle regole, con **[!UICONTROL Draft]** stato.

   ![](assets/message-rules-created.png)

## Attivare una regola {#activate-rule}

Una volta creata, una regola di frequenza del messaggio ha la **[!UICONTROL Draft]** stato e non influisce ancora su alcun messaggio. Per abilitarlo, fai clic sui puntini di sospensione accanto alla regola e seleziona **[!UICONTROL Activate]**.

![](assets/message-rules-activate.png)

L&#39;attivazione di una regola avrà un impatto sui messaggi a cui si applica alla loro successiva esecuzione. Scopri come [applicare una regola di frequenza a un messaggio](#apply-frequency-rule).

>[!NOTE]
>
>Non è necessario modificare o ripubblicare messaggi o percorsi affinché una regola abbia effetto.

Per disattivare una regola di frequenza dei messaggi, fai clic sui puntini di sospensione accanto alla regola e seleziona **[!UICONTROL Deactivate]**.

![](assets/message-rules-deactivate.png)

Lo stato della regola cambierà in **[!UICONTROL Inactive]** e la regola non verrà applicata alle esecuzioni di messaggi future. I messaggi attualmente in esecuzione non saranno interessati.

>[!NOTE]
>
>La disattivazione di una regola non influisce o reimposta alcun conteggio sui singoli profili.

## Applicare una regola di frequenza a un messaggio {#apply-frequency-rule}

Per applicare una regola di frequenza a un messaggio, segui la procedura seguente.

1. Crea un messaggio. [Ulteriori informazioni](../messages/get-started-content.md#create-new-message)

1. Seleziona la categoria definita per la [regola creata](#create-new-rule).

   ![](assets/message-rules-msg-properties.png)

   >[!NOTE]
   >
   >Attualmente solo il **[!UICONTROL Marketing]** categoria disponibile per le regole di frequenza dei messaggi.

1. Seleziona i canali desiderati per il messaggio.

   ![](assets/message-rules-msg-channels.png)

1. Puoi fare clic su **[!UICONTROL Frequency rule]** collegamento per visualizzare le regole di frequenza che verranno applicate per la categoria e i canali selezionati.

   ![](assets/message-rules-msg-link.png)

   Viene aperta una nuova scheda per visualizzare le regole di frequenza dei messaggi corrispondenti.

1. [Progettazione](../design/design-emails.md) e [pubblicare](../messages/publish-manage-message.md) il tuo messaggio.

Tutte le regole di frequenza che corrispondono alla categoria e al canale selezionati verranno applicate automaticamente a questo messaggio.

<!--Clicking the link out button next to the category selector will jump you over to the rules inventory screen to see which rules will be applied to the message.-->

Puoi visualizzare il numero di profili esclusi dalla consegna nel [Visualizzazioni live e globali](../reports/message-monitoring.md)e nella [rapporto e-mail Live](../reports/email-live-report.md), dove le regole di frequenza saranno elencate come possibile motivo per cui gli utenti sono esclusi dalla consegna.

>[!NOTE]
>
>Puoi applicare diverse regole allo stesso canale, ma una volta raggiunto il limite inferiore, il profilo verrà escluso dalle consegne successive.

## Esempio: combinare diverse regole {#frequency-rule-example}

Puoi combinare diverse regole di frequenza dei messaggi, come descritto nell’esempio seguente.

1. [Creare una regola](#create-new-rule) chiamato *Limitazione totale di marketing*:

   * Seleziona tutti i canali (e-mail, push).
   * Impostare il limite a 12.

   ![](assets/message-rules-ex-overall-cap.png)

1. Per limitare ulteriormente il numero di notifiche push basate sul marketing inviate a un utente, crea una seconda regola chiamata *Limite di marketing push*:

   * Seleziona il canale push.
   * Impostare il limite a 4.

   ![](assets/message-rules-ex-push-cap.png)

1. Salva e [attivare](#activate-rule) la regola.

1. Crea un messaggio. [Ulteriori informazioni](../messages/get-started-content.md#create-new-message)

1. Seleziona la **[!UICONTROL Marketing]** categoria.

   ![](assets/message-rules-ex-category-maktg.png)

1. Seleziona la **[!UICONTROL Email]** e **[!UICONTROL Push Notification]** canali.

   ![](assets/message-rules-ex-channels.png)

1. Puoi fare clic su **[!UICONTROL Frequency rule]** collegamento per visualizzare le regole di frequenza che verranno applicate per la categoria e i canali selezionati.

1. [Progettazione](../design/design-emails.md) e [pubblicare](../messages/publish-manage-message.md) il tuo messaggio.

In questo scenario, un singolo profilo:
* può ricevere fino a 12 messaggi di marketing al mese;
* ma saranno escluse dalle notifiche push di marketing dopo aver ricevuto 4 notifiche push.
