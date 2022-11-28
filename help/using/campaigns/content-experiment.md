---
solution: Journey Optimizer
product: journey optimizer
title: Creare un esperimento sui contenuti
description: Scopri come creare un esperimento sui contenuti nelle campagne
feature: A/B Testing
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: bd35ae19-8713-4571-80bc-5f40e642d121
source-git-commit: efea1bbd5154d378daf1f52315384156b6d23ae3
workflow-type: tm+mt
source-wordcount: '1000'
ht-degree: 4%

---

# Creare un esperimento sui contenuti {#content-experiment}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment"
>title="Esperimento sui contenuti"
>abstract="TBC"

>[!AVAILABILITY]
>
>La **Esperimento dei contenuti** al momento è disponibile solo per un set di organizzazioni (disponibilità limitata). Per ulteriori informazioni, contatta il tuo rappresentante Adobe.

Utilizza Journey Optimizer Content Experiment per definire più trattamenti di consegna. Il pubblico di interesse viene assegnato in modo casuale a ciascun trattamento al fine di determinare quale funziona meglio rispetto alla metrica di interesse. Puoi scegliere di variare il contenuto, l’oggetto o il mittente della consegna.

>[!NOTE]
>
>Prima di iniziare con Esperienza di contenuto, assicurati che la configurazione di reporting sia impostata per i set di dati personalizzati. Ulteriori informazioni in [questa sezione](reporting-configuration.md).

Nell’esempio seguente, il target di consegna è stato suddiviso in due gruppi, ognuno dei quali rappresenta il 45% della popolazione target e un gruppo di blocchi del 10%, che non riceverà la consegna.

Ogni persona nel pubblico di destinazione riceverà una versione di un’e-mail, con un oggetto che corrisponde a una delle due seguenti:

* uno che promuove direttamente un’offerta del 10% sulla nuova collezione e un’immagine.
* l&#39;altro pubblicizza solo un&#39;offerta speciale senza specificare il 10% di sconto senza alcuna immagine.

L’obiettivo è quello di vedere se i destinatari interagiranno con l’e-mail a seconda dell’esperimento ricevuto. Pertanto sceglieremo **[!UICONTROL Aperture e-mail]** come metrica di obiettivo principale in questo esperimento di contenuto.

![](assets/content_experiment.png)

## Creare la campagna {#campaign-experiment}

1. Da **[!UICONTROL Campagne]** pagina, fai clic su **[!UICONTROL Creare una campagna]**.

   ![](assets/content_experiment_1.png)

1. Seleziona il canale e quindi il **[!UICONTROL Superficie]** desideri utilizzare per questa consegna. Per ulteriori informazioni, consulta la sezione [Superfici dei canali](../configuration/channel-surfaces.md) pagina.

   ![](assets/content_experiment_2.png)

1. Fai clic su **[!UICONTROL Crea]**.

1. Imposta la **[!UICONTROL Proprietà]** della consegna:
   * **[!UICONTROL Titolo]**
   * **[!UICONTROL Descrizione]**
   * **[!UICONTROL Categoria]**: **[!UICONTROL Marketing]** / **[!UICONTROL Transazionale]**

1. Per avviare l’esperimento sui contenuti, attiva/disattiva la **[!UICONTROL Esperimento dei contenuti]** opzione . La **[!UICONTROL Esperimento dei contenuti]** viene visualizzato il menu .

   ![](assets/content_experiment_3.png)

1. Definisci il pubblico di cui eseguire il targeting. A questo scopo, fai clic sul pulsante **[!UICONTROL Selezionare il pubblico]** per visualizzare l’elenco dei segmenti Adobe Experience Platform disponibili. [Ulteriori informazioni sui segmenti](../segment/about-segments.md)

   In **[!UICONTROL Spazio dei nomi identità]** scegli lo spazio dei nomi da utilizzare per identificare gli individui del segmento selezionato. [Ulteriori informazioni](get-started-experiment.md#content-experiment-work)

1. Per eseguire la campagna in una data specifica o su una frequenza ricorrente, configura la sezione Pianificazione . [Ulteriori informazioni](create-campaign.md)

1. Fai clic su **[!UICONTROL Modifica contenuto]** per iniziare a personalizzare le diverse **[!UICONTROL Trattamenti]**.

   ![](assets/content_experiment_4.png)

## Crea i trattamenti {#treatment-experiment}

1. Da **[!UICONTROL Modifica contenuto]** finestra, inizia a personalizzare il tuo trattamento A.

   Per questo trattamento, specificheremo l&#39;offerta speciale direttamente nell&#39;oggetto.

   ![](assets/content_experiment_5.png)

1. Dopo aver progettato il tuo primo trattamento, dal **[!UICONTROL Altre azioni]** pulsante, fai clic su **[!UICONTROL Duplica]**.

   Puoi anche scegliere di iniziare un nuovo trattamento da zero cliccando sul **[!UICONTROL Esperimento dei contenuti]** pulsante ![](assets/content_experiment_16.png) per accedere alle opzioni avanzate **[!UICONTROL Aggiungi trattamento]**.

   ![](assets/content_experiment_7.png)

1. Modificare la **[!UICONTROL Titolo]** del tuo trattamento per differenziarli meglio.

   ![](assets/content_experiment_8.png)

1. Personalizza il tuo secondo trattamento in base alle esigenze.

   In questo caso, scegliamo di non specificare l’offerta nel **[!UICONTROL Linea oggetto]**.

   ![](assets/content_experiment_9.png)

Una volta personalizzati i trattamenti, puoi iniziare a configurare il tuo esperimento sui contenuti.

## Configurare l’esperimento sul contenuto {#configure-experiment}

1. Quando entrambe le consegne sono personalizzate, dalla **[!UICONTROL Modifica contenuto]** finestra, seleziona **[!UICONTROL Configurare un esperimento sul contenuto]**.

   ![](assets/content_experiment_10.png)

1. Seleziona gli obiettivi da impostare per l’esperimento.

   Per il nostro esperimento, selezioniamo **[!UICONTROL Apri e-mail]** per verificare se i destinatari aprono le loro e-mail se il codice promozionale si trova nella riga dell’oggetto.

   ![](assets/content_experiment_11.png)

1. Scegli di aggiungere un **[!UICONTROL Holdout]** creare un gruppo per la consegna. Questo gruppo non riceverà alcun contenuto da questa campagna.

   Se si attiva la barra di attivazione, la percentuale della popolazione sarà automaticamente pari al 10%. Se necessario, è possibile regolare questa percentuale.

   ![](assets/content_experiment_12.png)

1. È quindi possibile scegliere di allocare una percentuale precisa a ogni **[!UICONTROL Trattamento]** o semplicemente accendere **[!UICONTROL Distribuisci uniformemente]** barra di attivazione/disattivazione.

   ![](assets/content_experiment_13.png)

1. Fai clic su **[!UICONTROL Salva]** quando la configurazione è impostata.

1. Quando l’esperimento sul contenuto è pronto, puoi fare clic su **[!UICONTROL Rivedi per attivare]** per visualizzare un riepilogo della campagna. Gli avvisi vengono visualizzati se un parametro è errato o mancante.

   ![](assets/content_experiment_15.png)

1. Verifica che la campagna sia configurata correttamente, quindi fai clic su **[!UICONTROL Attiva]** per lanciarlo.

   ![](assets/content_experiment_14.png)

Dopo aver configurato la sperimentazione e la campagna, puoi seguire il successo della consegna con il rapporto Campaign.

## Relazione sugli obiettivi {#objectives-global}

>[!AVAILABILITY]
>
>La funzione di esperimento del contenuto è attualmente disponibile solo per un set di organizzazioni (disponibilità limitata). Per ulteriori informazioni, contatta il tuo rappresentante Adobe.

![](assets/performance_report.gif)

La **[!UICONTROL Obiettivi]** la scheda del rapporto Campaign ti consente di perfezionare meglio i rapporti delle consegne eseguendo il targeting di una metrica specifica.

La **[!UICONTROL Obiettivi]** sono collegati a **[!UICONTROL Set di dati]** che definiscono una connessione a un sistema per recuperare informazioni aggiuntive. Un elenco di elementi incorporati **[!UICONTROL Obiettivi]** è disponibile ma puoi aggiungerne una nuova **[!UICONTROL Set di dati]**. Per la procedura dettagliata, consulta [sezione](reporting-configuration.md).

Dopo aver selezionato gli obiettivi su cui eseguire il targeting, i due **[!UICONTROL Panoramica delle prestazioni]** e **[!UICONTROL Obiettivo della campagna]** I widget forniscono un riepilogo dettagliato delle prestazioni di consegna.

Con la **[!UICONTROL Obiettivo della campagna]** widget, puoi anche scegliere di confrontare il tuo obiettivo principale con un&#39;altra metrica.

Tieni presente che ogni widget può essere ridimensionato ed eliminato, se necessario. Per ulteriori informazioni, consulta questo [sezione](../reports/global-report.md#modify-dashboard).

## Rapporto di sperimentazione {#experimentation-global}

>[!AVAILABILITY]
>
>La funzione di esperimento del contenuto è attualmente disponibile solo per un set di organizzazioni (disponibilità limitata). Per ulteriori informazioni, contatta il tuo rappresentante Adobe.

![](assets/experimentation_report_3.png)

Dalla tua campagna **[!UICONTROL Report globale]**, **[!UICONTROL Sperimentazione]** scheda descrive le informazioni principali relative alle prestazioni di ogni variante e se è presente un performer migliore.

Tieni presente che la definizione dell’esecutore migliore potrebbe richiedere un po’ di tempo, sarà rappresentata da questa icona ![](assets/experimentation_report_1.png).

La **[!UICONTROL Risultato dell’esperimento]** Il widget descrive le prestazioni di ogni variante. È possibile modificare la linea di base selezionando uno dei trattamenti dal **[!UICONTROL Linea]** il menu a discesa. Il miglior trattamento sarà rappresentato da un&#39;icona a forma di stella.

La tabella presenta le metriche seguenti:

* **[!UICONTROL Profili]**: Numero di profili interessati da questo trattamento.

* **[!UICONTROL Clic in uscita univoci]**: Numero totale di clic tra canali in uscita.

* **[!UICONTROL Conteggio per profilo]**: Valore totale della metrica obiettivo Esperimento diviso per il numero di profili.

* **[!UICONTROL Intervallo di affidabilità]**: Differenza percentuale di prestazioni tra la linea di base e il trattamento più performante. [Ulteriori informazioni](../campaigns/experiment-calculations.md#confidence-intervals).

* **[!UICONTROL Incremento medio]**: Miglioramento percentuale del tasso di conversione di un dato trattamento rispetto alla linea di base. [Ulteriori informazioni](../campaigns/experiment-calculations.md#understand-lift)

* **[!UICONTROL Affidabilità]**: Prova che un dato trattamento è lo stesso del trattamento di base. [Ulteriori informazioni](../campaigns/experiment-calculations.md#understand-confidence)

Per informazioni approfondite su questi risultati e su come interpretarli, consulta [questa pagina](../campaigns/get-started-experiment.md#interpret-results).
