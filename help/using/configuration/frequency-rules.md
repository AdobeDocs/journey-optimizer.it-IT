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
source-git-commit: 40c42303b8013c1d9f4dd214ab1acbec2942e094
workflow-type: tm+mt
source-wordcount: '602'
ht-degree: 0%

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

![](assets/message-rules-access.png)

<!--To access, create, edit or delete message frequency rules, you must have the message configuration permission. [Learn more](../administration/high-low-permissions.md#administration-permissions)-->

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

Per attivare una regola di frequenza dei messaggi, fai clic sui puntini di sospensione accanto alla regola e seleziona **[!UICONTROL Activate]**.

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

Per applicare una regola di frequenza a un messaggio, è sufficiente selezionare la categoria definita per questa regola quando [creazione del messaggio](../messages/get-started-content.md#create-new-message).

![](assets/message-rules-properties.png)

Selezionando la **[!UICONTROL Marketing]** categoria , tutte le regole di frequenza dei messaggi corrispondenti verranno applicate automaticamente a questo messaggio.

<!--Clicking the link out button next to the category selector will jump you over to the rules inventory screen to see which rules will be applied to the message.-->

Puoi visualizzare il numero di profili esclusi dalla consegna nel [Visualizzazioni live e globali](../reports/message-monitoring.md)e nella [rapporto e-mail Live](../reports/email-live-report.md), dove le regole di frequenza saranno elencate come possibile motivo per cui gli utenti sono esclusi dalla consegna.

## Esempio

Puoi combinare diverse regole di frequenza dei messaggi, come descritto nell’esempio seguente.

1. Creare una regola denominata *Limitazione totale di marketing*:

   * Seleziona tutti i canali (e-mail, push).
   * Impostare il limite a 12.

1. Per limitare ulteriormente il numero di notifiche push basate sul marketing inviate a un utente, crea una seconda regola chiamata *Limitare il push di marketing*:

   * Seleziona il canale push.
   * Impostare il limite a 4.

In questo scenario, un singolo profilo può ricevere fino a 12 messaggi di marketing al mese, ma sarà escluso dalle notifiche push di marketing dopo aver ricevuto 4 notifiche push.
