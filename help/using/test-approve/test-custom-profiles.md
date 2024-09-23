---
solution: Journey Optimizer
product: journey optimizer
title: Verifica il contenuto utilizzando profili di esempio
description: Scopri come visualizzare in anteprima il contenuto delle e-mail e inviare bozze utilizzando i profili di esempio.
feature: Overview, Get Started
topic: Content Management
role: User
level: Intermediate
badge: label="Beta"
hide: true
hidefromtoc: true
source-git-commit: 6b3518645b9cbfbe6f728011b0889c28fa754496
workflow-type: tm+mt
source-wordcount: '779'
ht-degree: 0%

---


# Verifica il contenuto utilizzando profili di esempio {#custom-profiles}

>[!CONTEXTUALHELP]
>id="ajo_simulate_sample_profiles"
>title="Simulare utilizzando i profili di esempio"
>abstract="In questa schermata, puoi visualizzare in anteprima il contenuto delle e-mail e inviare bozze durante la rappresentazione di profili di esempio che puoi caricare da un file CSV o aggiungere manualmente direttamente da questa schermata."


<!--ATTENTE CONFIRMATION 

- nom (custom/sample)
- campaigns/journeys ou que campaigns

-->

>[!AVAILABILITY]
>
>Questa funzione è attualmente disponibile come versione beta solo per alcuni utenti.

Percorsi Optimizer consente di visualizzare in anteprima e testare il contenuto delle e-mail utilizzando profili di esempio che è possibile caricare da un file CSV o aggiungere manualmente direttamente durante la simulazione del contenuto. Questa funzione consente di selezionare profili di esempio da utilizzare per visualizzare in anteprima il contenuto e inviare bozze. Tutti gli attributi dei profili utilizzati nel contenuto per la personalizzazione vengono rilevati automaticamente dal sistema e possono essere utilizzati per i test.

Per accedere a questa esperienza, fai clic sul pulsante **[!UICONTROL Simula contenuto]** e scegli **[!UICONTROL Simula con CSV(Beta)]**.

![](assets/simulate-sample.png)


I passaggi principali per testare il contenuto sono i seguenti:

1. Aggiungi fino a 30 profili di esempio caricando un file CSV o aggiungendoli manualmente uno alla volta. [Scopri come aggiungere profili di esempio](#profiles)
1. Controlla l’anteprima del contenuto utilizzando i profili aggiunti. [Scopri come visualizzare in anteprima il tuo contenuto](#preview)
1. Invia fino a 10 bozze agli indirizzi e-mail impersonando i profili di esempio desiderati. [Scopri come inviare bozze](#proofs)


## Guardrail e limitazioni {#limitations}

Prima di iniziare a testare il contenuto utilizzando i profili di esempio, considera i seguenti guardrail e prerequisiti.

* Al momento, il test tramite profili di esempio è disponibile solo all’interno delle campagne e per il canale e-mail.
* Nell’esperienza corrente non sono disponibili le seguenti funzioni: rendering della casella in entrata, rapporti di posta indesiderata, contenuto multilingue ed esperimento sui contenuti. Per utilizzare queste funzionalità, seleziona dal contenuto il pulsante **[!UICONTROL Simula contenuto]** per accedere all&#39;interfaccia utente precedente.
* Al momento sono supportati solo gli attributi del profilo. Se nel contenuto vengono utilizzati attributi contestuali per la personalizzazione, non potrai testare il contenuto utilizzando questi attributi.
* Per l’immissione di dati per i profili di esempio sono supportati solo i seguenti tipi di dati: numero (intero e decimale), stringa, booleano e tipo data. Qualsiasi altro tipo di dati mostrerà un errore.

## Aggiungere profili di esempio {#profiles}

Puoi aggiungere fino a 30 profili di esempio per testare il contenuto utilizzando un file CSV o manualmente:

* Per caricare profili da un file CSV, fai clic sul collegamento **[!UICONTROL Scarica modello]** per recuperare un modello di file CSV. Questi modelli includono una colonna per ogni attributo di profilo utilizzato nel contenuto per la personalizzazione.

  Compila il file CSV, quindi fai clic su **[!UICONTROL Carica profili di esempio]** per caricarlo e verificare il contenuto.

* Per aggiungere un profilo manualmente, fare clic sul pulsante **[!UICONTROL Crea profilo di esempio]** e inserire le informazioni per il profilo. Viene visualizzato un campo per ogni attributo di profilo utilizzato nel contenuto per la personalizzazione.

  ![](assets/simulate-custom-add.png)

Una volta selezionati i profili, viene visualizzata una casella per ciascun profilo sul lato sinistro della schermata. Puoi utilizzare questi profili per visualizzare in anteprima il contenuto e inviare bozze.

>[!NOTE]
>
>I profili di esempio aggiunti fungono solo da scopo di test per il contenuto corrente. Gli elementi non vengono memorizzati in Adobe Experience Platform, ma nella sessione del browser utente, il che significa che non verranno visualizzati alla disconnessione o se si lavora da un altro dispositivo.

## Visualizzare l’anteprima dei contenuti utilizzando profili di esempio {#preview}

Per visualizzare l’anteprima del contenuto utilizzando uno dei profili, seleziona la casella pertinente per aggiornare l’anteprima del contenuto nella sezione a destra con le informazioni immesse per questo profilo.

Puoi rimuovere una casella in qualsiasi momento utilizzando il pulsante con i puntini di sospensione nell&#39;angolo superiore destro e selezionando **[!UICONTROL Rimuovi]**. Per modificare le informazioni di un profilo, fare clic sul pulsante con i puntini di sospensione e selezionare **[!UICONTROL Modifica]**.

![](assets/simulate-custom-boxes.png)

## Inviare bozze {#proofs}

Journey Optimizer ti consente di inviare bozze agli indirizzi e-mail impersonando uno o più profili di esempio aggiunti nella schermata di simulazione. I passaggi sono i seguenti:

1. Verifica che siano stati aggiunti profili di esempio per testare il contenuto e fai clic sul pulsante **[!UICONTROL Invia bozza]**.

1. Nel campo **[!UICONTROL Destinatari]**, inserisci l&#39;indirizzo e-mail a cui desideri inviare la bozza, quindi fai clic su **[!UICONTROL Aggiungi]**. Ripeti l’operazione per inviare la bozza ad altri indirizzi e-mail. Puoi aggiungere fino a 10 destinatari della bozza.

1. Nella sezione inferiore della schermata, seleziona i profili di esempio che desideri impersonare nella bozza. Puoi selezionare più profili, nel qual caso l’e-mail includerà tutte le bozze dei profili selezionati.

   Per ulteriori informazioni su un profilo, selezionare il collegamento **[!UICONTROL Visualizza dettagli profilo]**. Questo consente di visualizzare le informazioni immesse nella schermata precedente per i diversi attributi del profilo.

   ![](assets/simulate-custom-proofs.png)

1. Fare clic sul pulsante **[!UICONTROL Invia bozza]** per iniziare a inviare la bozza.

Puoi tenere traccia dell&#39;invio in qualsiasi momento facendo clic sul pulsante **[!UICONTROL Visualizza bozze]** nella schermata simula contenuto.

![](assets/simulate-custom-sent-proofs.png)
