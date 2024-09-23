---
solution: Journey Optimizer
product: journey optimizer
title: Verifica i contenuti utilizzando profili personalizzati
description: Scopri come visualizzare in anteprima i contenuti e inviare bozze utilizzando profili personalizzati.
feature: Overview, Get Started
topic: Content Management
role: User
level: Intermediate
badge: label="Beta"
hide: true
hidefromtoc: true
source-git-commit: 6229f295b961b0535139b64928216e40c3759947
workflow-type: tm+mt
source-wordcount: '599'
ht-degree: 0%

---


# Verifica i contenuti utilizzando profili personalizzati {#custom-profiles}

>[!CONTEXTUALHELP]
>id="ajo_simulate_sample_profiles"
>title="Simulare utilizzando profili personalizzati"
>abstract="In questa schermata, puoi visualizzare in anteprima i contenuti e inviare bozze durante la rappresentazione di profili personalizzati che puoi caricare da un file CSV o aggiungere manualmente direttamente da questa schermata."

>[!AVAILABILITY]
>
>Questa funzione è attualmente disponibile come versione beta solo per alcuni utenti.
>
>Il rendering della casella in entrata e i rapporti di posta indesiderata non sono disponibili nell’esperienza corrente. Per utilizzare queste funzionalità, seleziona dal contenuto il pulsante **[!UICONTROL Simula contenuto]** per accedere all&#39;interfaccia utente legacy.

Percorsi Optimizer consente di visualizzare in anteprima e testare il contenuto utilizzando profili personalizzati che è possibile caricare da un file CSV o aggiungere manualmente direttamente durante la simulazione del contenuto.

Per accedere a questa esperienza, fai clic sul pulsante **[!UICONTROL Simula contenuto]** e scegli **[!UICONTROL Simula con CSV(Beta)]**.

Questa schermata consente di selezionare i profili da utilizzare per visualizzare in anteprima il contenuto e inviare bozze. Tutti gli attributi utilizzati nel contenuto per la personalizzazione vengono rilevati automaticamente dal sistema e possono essere utilizzati per i test.

I passaggi principali per testare il contenuto sono i seguenti:

1. Aggiungi profili personalizzati caricando un file CSV o aggiungendoli manualmente uno alla volta. [Scopri come aggiungere profili personalizzati](#profiles)
1. Controlla l’anteprima del contenuto utilizzando i profili aggiunti. [Scopri come visualizzare in anteprima il tuo contenuto](#preview)
1. Invia fino a 10 bozze agli indirizzi e-mail impersonando i profili personalizzati desiderati. [Scopri come inviare bozze](#proofs)


## Aggiungere profili personalizzati {#profiles}

Puoi aggiungere profili personalizzati per testare il contenuto utilizzando un file CSV o manualmente:

* Per caricare profili da un file CSV, fai clic sul collegamento **[!UICONTROL Scarica modello]** per recuperare un modello di file CSV. Questi modelli includono una colonna per ogni attributo di personalizzazione utilizzato nel contenuto.

  Compila il file CSV, quindi fai clic su **[!UICONTROL Carica profili di esempio]** per caricarlo e verificare il contenuto.

* Per aggiungere un profilo manualmente, fare clic sul pulsante **[!UICONTROL Crea profilo di esempio]** e inserire le informazioni per il profilo. Viene visualizzato un campo per ogni attributo di personalizzazione utilizzato nel contenuto.

  ![](assets/simulate-custom-add.png)

Una volta selezionati i profili, viene visualizzata una casella per ciascun profilo sul lato sinistro della schermata. Puoi utilizzare questi profili per visualizzare in anteprima il contenuto e inviare bozze.

## Visualizzare l’anteprima dei contenuti utilizzando profili personalizzati {#preview}

Per visualizzare l’anteprima del contenuto utilizzando uno dei profili, seleziona la casella pertinente per aggiornare l’anteprima del contenuto nella sezione a destra con le informazioni immesse per questo profilo.

Puoi rimuovere una casella in qualsiasi momento utilizzando il pulsante con i puntini di sospensione nell&#39;angolo superiore destro e selezionando **[!UICONTROL Rimuovi]**. Per modificare le informazioni di un profilo, fare clic sul pulsante con i puntini di sospensione e selezionare **[!UICONTROL Modifica]**.

![](assets/simulate-custom-boxes.png)

## Inviare bozze {#proofs}

Journey Optimizer ti consente di inviare bozze agli indirizzi e-mail impersonando uno o più profili personalizzati aggiunti nella schermata di simulazione. I passaggi sono i seguenti:

1. Verifica che siano stati aggiunti profili personalizzati per testare il contenuto e fai clic sul pulsante **[!UICONTROL Invia bozza]**.

1. Nel campo **[!UICONTROL Destinatari]**, inserisci l&#39;indirizzo e-mail a cui desideri inviare la bozza, quindi fai clic su **[!UICONTROL Aggiungi]**. Ripeti l’operazione per inviare la bozza ad altri indirizzi e-mail. Puoi aggiungere fino a 10 destinatari della bozza.

1. Nella sezione inferiore della schermata, seleziona i profili personalizzati che desideri rappresentare nella bozza. Puoi selezionare più profili, nel qual caso l’e-mail includerà tutte le bozze dei profili selezionati.

   ![](assets/simulate-custom-proofs.png)

1. Fare clic sul pulsante **[!UICONTROL Invia bozza]** per iniziare a inviare la bozza.

Puoi tenere traccia dell&#39;invio in qualsiasi momento facendo clic sul pulsante **[!UICONTROL Visualizza bozze]** nella schermata simula contenuto.

![](assets/simulate-custom-sent-proofs.png)
