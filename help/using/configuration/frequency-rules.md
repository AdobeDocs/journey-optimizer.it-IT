---
solution: Journey Optimizer
product: journey optimizer
title: Regole di frequenza
description: Scopri come definire le regole di frequenza
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 49248fb6-5a91-45b2-9de8-2f078d59c0fc
source-git-commit: 0ec122bbf134c41f95755a3b6f08eb7ef68506df
workflow-type: tm+mt
source-wordcount: '973'
ht-degree: 2%

---

# Regole di frequenza dei messaggi {#frequency-rules}

[!DNL Journey Optimizer] consente di controllare la frequenza con cui gli utenti ricevono un messaggio o accedono a un percorso impostando regole cross-channel che escludono automaticamente i profili sollecitati in eccesso dai messaggi e dalle azioni.

Ad esempio, non vuoi che il tuo marchio invii più di 3 messaggi di marketing al mese ai loro clienti.

A questo scopo, puoi utilizzare una regola di frequenza che limiti il numero di messaggi inviati in base a uno o più canali durante un periodo di calendario mensile.

>[!NOTE]
>
>Le regole di frequenza dei messaggi sono diverse dalla gestione della rinuncia, che consente agli utenti di annullare l’iscrizione alla ricezione di comunicazioni da un marchio. [Ulteriori informazioni](../privacy/opt-out.md#opt-out-management)

➡️ [Scopri questa funzione nel video](#video)

## Regole di accesso {#access-rules}

Le regole sono disponibili dal **[!UICONTROL Amministrazione]** > **[!UICONTROL Regole]** menu. Vengono elencate tutte le regole, ordinate per data di modifica.

Utilizza l’icona del filtro per filtrare in base alla categoria, allo stato e/o al canale. Puoi anche effettuare ricerche nell’etichetta del messaggio.

![](assets/message-rules-filter.png)

### Autorizzazioni{#permissions-frequency-rules}

Per accedere, creare, modificare o eliminare le regole di frequenza dei messaggi, devi disporre della **[!UICONTROL Gestire le regole di frequenza]** autorizzazione.

Utenti con **[!UICONTROL Visualizzare le regole di frequenza]** Le autorizzazioni sono in grado di visualizzare le regole, ma non di modificarle o eliminarle.

![](assets/message-rules-access.png)

Ulteriori informazioni sulle autorizzazioni in [questa sezione](../administration/high-low-permissions.md).

## Creare una regola {#create-new-rule}

>[!CONTEXTUALHELP]
>id="ajo_rules_category"
>title="Seleziona la categoria della regola del messaggio"
>abstract="Quando viene attivata e applicata a un messaggio, tutte le regole di frequenza che corrispondono alla categoria selezionata verranno applicate automaticamente a questo messaggio. Attualmente è disponibile solo la categoria Marketing."

>[!CONTEXTUALHELP]
>id="ajo_rules_capping"
>title="Imposta il limite per la regola"
>abstract="Specifica il numero massimo di messaggi inviati a un profilo cliente ogni mese. Il limite di frequenza sarà basato su un periodo di calendario mensile e verrà reimpostato all&#39;inizio di ogni mese."

>[!CONTEXTUALHELP]
>id="ajo_rules_channel"
>title="Definisci i canali a cui si applica la regola"
>abstract="Seleziona almeno un canale. L’applicazione dell’applicazione di limitazione viene applicata a tutti i canali come conteggio totale."

Per creare una nuova regola, segui i passaggi seguenti.

1. Accedere al **[!UICONTROL Regole di frequenza dei messaggi]** elenco, quindi fai clic su **[!UICONTROL Crea regola]**.

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

1. Seleziona il canale da utilizzare per questa regola: **[!UICONTROL E-mail]** o **[!UICONTROL Notifica push]**.

   ![](assets/message-rules-channels.png)

   >[!NOTE]
   >
   >Per poter creare la regola, devi selezionare almeno un canale.

1. Seleziona diversi canali se desideri applicare un limite a tutti i canali selezionati come conteggio totale.

   Ad esempio, imposta il limite a 15 e seleziona sia i canali e-mail che i canali push. Se un profilo ha già ricevuto 10 e-mail di marketing e 5 notifiche push di marketing, verrà escluso dalla consegna immediatamente successiva di qualsiasi e-mail di marketing o notifica push.

1. Fai clic su **[!UICONTROL Salva come bozza]** per confermare la creazione della regola. Il messaggio viene aggiunto all’elenco delle regole con **[!UICONTROL Bozza]** stato.

   ![](assets/message-rules-created.png)

## Attivare una regola {#activate-rule}

Una volta creata, una regola di frequenza del messaggio ha la **[!UICONTROL Bozza]** stato e non influisce ancora su alcun messaggio. Per abilitarlo, fai clic sui puntini di sospensione accanto alla regola e seleziona **[!UICONTROL Attiva]**.

![](assets/message-rules-activate.png)

L&#39;attivazione di una regola avrà un impatto sui messaggi a cui si applica alla loro successiva esecuzione. Scopri come [applicare una regola di frequenza a un messaggio](#apply-frequency-rule).

>[!NOTE]
>
>Per attivare completamente una regola possono essere necessari fino a 10 minuti. Non è necessario modificare i messaggi o ripubblicare i percorsi affinché una regola abbia effetto.

Per disattivare una regola di frequenza dei messaggi, fai clic sui puntini di sospensione accanto alla regola e seleziona **[!UICONTROL Disattiva]**.

![](assets/message-rules-deactivate.png)

Lo stato della regola cambierà in **[!UICONTROL Inattivo]** e la regola non verrà applicata alle esecuzioni di messaggi future. I messaggi attualmente in esecuzione non saranno interessati.

>[!NOTE]
>
>La disattivazione di una regola non influisce o reimposta alcun conteggio sui singoli profili.

## Applicare una regola di frequenza a un messaggio {#apply-frequency-rule}

Per applicare una regola di frequenza a un messaggio, segui la procedura seguente.

1. Durante la creazione di un [percorso](../building-journeys/journey-gs.md), aggiungi un messaggio selezionando uno dei canali definiti per la regola.

1. Seleziona la categoria definita per la [regola creata](#create-new-rule).

   ![](assets/journey-message-category.png)

   >[!NOTE]
   >
   >Attualmente solo il **[!UICONTROL Marketing]** categoria disponibile per le regole di frequenza dei messaggi.

1. Puoi fare clic su **[!UICONTROL Regola di frequenza]** per visualizzare la schermata delle regole di frequenza in una nuova scheda. [Ulteriori informazioni](#access-rules)

   Tutte le regole di frequenza che corrispondono alla categoria e al canale selezionati verranno applicate automaticamente a questo messaggio.

   >[!NOTE]
   >
   >Messaggi in cui è selezionata la categoria **[!UICONTROL Transazionale]** non verranno valutati in base alle regole di frequenza.

1. Puoi visualizzare il numero di profili esclusi dalla consegna nel [Report globale](../reports/global-report.md)e nella [Report live](../reports/live-report.md), dove le regole di frequenza saranno elencate come possibile motivo per cui gli utenti sono esclusi dalla consegna.

>[!NOTE]
>
>Puoi applicare diverse regole allo stesso canale, ma una volta raggiunto il limite inferiore, il profilo verrà escluso dalle consegne successive.

## Esempio: combinare diverse regole {#frequency-rule-example}

Puoi combinare diverse regole di frequenza dei messaggi, come descritto nell’esempio seguente.

1. [Creare una regola](#create-new-rule) chiamato *Limitazione totale di marketing*:

   * Seleziona Canali e-mail e push.
   * Impostare il limite a 12.

   ![](assets/message-rules-ex-overall-cap.png)

1. Per limitare ulteriormente il numero di notifiche push basate sul marketing inviate a un utente, crea una seconda regola chiamata *Limite di marketing push*:

   * Seleziona il canale push.
   * Impostare il limite a 4.

   ![](assets/message-rules-ex-push-cap.png)

1. Salva e [attivare](#activate-rule) la regola.

1. Crea un messaggio e-mail e seleziona la **[!UICONTROL Marketing]** categoria del messaggio. [Ulteriori informazioni](../email/create-email.md)

1. Crea una notifica push e seleziona la **[!UICONTROL Marketing]** categoria del messaggio. [Ulteriori informazioni](../push/create-push.md)

In questo scenario, un singolo profilo:
* può ricevere fino a 12 messaggi di marketing al mese;
* ma saranno escluse dalle notifiche push di marketing dopo aver ricevuto 4 notifiche push.

>[!NOTE]
>
>Quando si sottopongono a test le regole di frequenza, si consiglia di utilizzare una nuova [profilo di prova](../segment/creating-test-profiles.md), poiché una volta raggiunto il limite di frequenza di un profilo, non è possibile reimpostare il contatore fino al mese successivo. La disattivazione di una regola consentirà ai profili con limite massimo di ricevere i messaggi, ma non rimuoverà né eliminerà eventuali incrementi di contatore.

## Video introduttivo {#video}

Scopri come creare, attivare, testare e creare rapporti sulle regole di frequenza.

>[!VIDEO](https://video.tv.adobe.com/v/344451?quality=12)
