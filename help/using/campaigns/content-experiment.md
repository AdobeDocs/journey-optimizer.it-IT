---
title: Creazione di un esperimento sul contenuto
description: Scopri come creare un esperimento sui contenuti nelle campagne
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: bd35ae19-8713-4571-80bc-5f40e642d121
source-git-commit: 0fb54571ea7620c981e746f8ac240b675e2f0d64
workflow-type: tm+mt
source-wordcount: '574'
ht-degree: 1%

---

# Creazione di un esperimento sul contenuto {#content-experiment}

>[!AVAILABILITY]
>
>La funzione di esperimento del contenuto è attualmente disponibile solo per un set di organizzazioni (disponibilità limitata). Per ulteriori informazioni, contatta il tuo rappresentante Adobe.

La funzione di esperimento dei contenuti ti consente di definire più trattamenti di consegna. Il pubblico di interesse viene assegnato in modo casuale a ciascun trattamento al fine di determinare quale funziona meglio rispetto alla metrica di interesse. Puoi scegliere di variare il contenuto, l’oggetto o il mittente dell’e-mail.

Nell’esempio seguente, il target di consegna è stato suddiviso in due gruppi, ognuno dei quali rappresenta il 45% della popolazione target e un gruppo di blocchi del 10%, che non riceverà la consegna.

Ogni persona nel pubblico di destinazione riceverà una versione dell’e-mail, con un oggetto che corrisponde a una delle due seguenti:

* uno che promuove direttamente un’offerta del 10% sulla nuova collezione e un’immagine.
* l&#39;altro pubblicizza solo un&#39;offerta speciale senza specificare il 10% di sconto senza alcuna immagine.

L’obiettivo è quello di vedere se i destinatari interagiranno con l’e-mail a seconda dell’esperimento ricevuto. Pertanto sceglieremo **[!UICONTROL Email Opens]** come metrica di obiettivo principale in questo esperimento di contenuto.

![](assets/content_experiment.png)

## Creare una campagna {#campaign-experiment}

1. Da **[!UICONTROL Campaigns]** pagina, fai clic su **[!UICONTROL Create Campaign]**.

   ![](assets/content_experiment_1.png)

1. Seleziona **[!UICONTROL Email]** quindi il **[!UICONTROL Surface]** desideri utilizzare per questa consegna. Per ulteriori informazioni, consulta la sezione [Superfici dei canali](../configuration/channel-surfaces.md) pagina.

   ![](assets/content_experiment_2.png)

1. Fai clic su **[!UICONTROL Create]**.

1. Imposta la **[!UICONTROL Properties]** della consegna:
   * **[!UICONTROL Title]**
   * **[!UICONTROL Description]**
   * **[!UICONTROL Category]**: **[!UICONTROL Marketing]** / **[!UICONTROL Transactional]**

1. Per avviare l’esperimento sui contenuti, attiva/disattiva la **[!UICONTROL Content experiment]** opzione . La **[!UICONTROL Content experiment]** apparirà il menu .

   ![](assets/content_experiment_3.png)

1. Imposta la **[!UICONTROL Audience]** e **[!UICONTROL Schedule]** Parametri per le consegne. [Ulteriori informazioni](create-campaign.md)

1. Fai clic su **[!UICONTROL Edit content]** per iniziare a personalizzare le diverse **[!UICONTROL Treatments]**.

   ![](assets/content_experiment_4.png)

## Crea i trattamenti {#treatment-experiment}

1. Da **[!UICONTROL Edit content]** aggiungi **[!UICONTROL Subject line]** per il tuo trattamento A email e clicca **[!UICONTROL Save]**.

   Per questo trattamento, specifichiamo l&#39;offerta direttamente nella riga dell&#39;oggetto.

   ![](assets/content_experiment_5.png)

1. Fai clic su **[!UICONTROL Email designer]** per iniziare a personalizzare le consegne.

   ![](assets/content_experiment_6.png)

1. Dopo aver progettato l’e-mail, fai clic su **[!UICONTROL Save]** e torna al **[!UICONTROL Edit content]** finestra per creare il Trattamento B.

1. Da **[!UICONTROL More actions]** pulsante, fai clic su **[!UICONTROL Duplicate]**.

   Puoi anche scegliere di iniziare un nuovo trattamento da zero cliccando sul **[!UICONTROL Content experiment]** per accedere alle opzioni avanzate **[!UICONTROL Add treatment]**.

   ![](assets/content_experiment_7.png)

1. Modificare la **[!UICONTROL Title]** del tuo trattamento per differenziarli meglio.

   ![](assets/content_experiment_8.png)

1. Seleziona la consegna e-mail collegata al tuo nuovo **[!UICONTROL Treatment]**.

1. Aggiungi il **[!UICONTROL Subject line]** per la consegna.

   Per questo trattamento, scegliamo di non specificare l’offerta nel **[!UICONTROL Subject line]**.

   ![](assets/content_experiment_9.png)

1. Fai clic su **[!UICONTROL Email designer]** personalizzare ulteriormente il Trattamento B consegna, se necessario.

Una volta personalizzati i trattamenti, puoi iniziare a configurare l’esperimento sui contenuti.

## Configurare l’esperimento sul contenuto {#configure-experiment}

1. Quando entrambe le consegne sono personalizzate, dalla **[!UICONTROL Edit content]** finestra, seleziona **[!UICONTROL Configure content experiment]**.

   ![](assets/content_experiment_10.png)

1. Seleziona gli obiettivi da impostare per l’esperimento.

   Per il nostro esperimento, selezioniamo **[!UICONTROL Email open]** per verificare se i destinatari aprono le loro e-mail se il codice promozionale si trova nella riga dell’oggetto.

   ![](assets/content_experiment_11.png)

1. Scegli di aggiungere un **[!UICONTROL Holdout]** creare un gruppo per la consegna. Questo gruppo non riceverà alcun contenuto da questa campagna.

   Se si attiva la barra di attivazione, la percentuale della popolazione sarà automaticamente pari al 10%. Se necessario, è possibile regolare questa percentuale.

   ![](assets/content_experiment_12.png)

1. È quindi possibile scegliere di allocare una percentuale precisa a ogni **[!UICONTROL Treatment]** o semplicemente accendere **[!UICONTROL Distribute evenly]** barra di attivazione/disattivazione.

   ![](assets/content_experiment_13.png)

1. Fai clic su **[!UICONTROL Save]** quando la configurazione è impostata.

1. Quando l’esperimento sul contenuto è pronto, puoi fare clic su **[!UICONTROL Review to activate]** per visualizzare un riepilogo della campagna. Gli avvisi vengono visualizzati se un parametro è errato o mancante.

   ![](assets/content_experiment_15.png)

1. Verifica che la campagna sia configurata correttamente, quindi fai clic su **[!UICONTROL Activate]** per lanciarlo.

   ![](assets/content_experiment_14.png)

## Rapporto di sperimentazione {#experimentation-report}

![](assets/experimentation_report_3.png)

Dalla tua campagna **[!UICONTROL Global report]**, **[!UICONTROL Experimentation]** scheda descrive le informazioni principali relative alle prestazioni di ogni variante e se durante il test è stato ottenuto un risultato migliore.

Per ulteriori dettagli su questo rapporto, consulta [Report globale della campagna](../campaigns/content-experiment.md#experimentation-report) pagina.
