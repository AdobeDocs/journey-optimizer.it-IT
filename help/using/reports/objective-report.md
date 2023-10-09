---
solution: Journey Optimizer
product: journey optimizer
title: Rapporto globale della campagna
description: Scopri come utilizzare i dati del rapporto globale della campagna
feature: Reporting
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: ec1af88c-7b0a-4eaf-97e1-0d9676268fed
source-git-commit: c4ab97999d000d969f6f09f4d84be017d1288f94
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 3%

---

# Rapporto globale della campagna {#objective-report}

Il rapporto globale della campagna è accessibile direttamente dalla campagna con **[!UICONTROL Visualizza rapporto]** pulsante.

La campagna **[!UICONTROL Rapporto globale]** è diviso in diversi widget che descrivono nel dettaglio il successo e gli errori della campagna. Ogni widget può essere ridimensionato ed eliminato, se necessario. Per ulteriori informazioni, consulta questa [sezione](../reports/global-report.md#modify-dashboard).

Per un elenco dettagliato di tutte le metriche disponibili in Adobe Journey Optimizer, consulta [questa pagina](global-report.md#list-of-components-global.md)

## Scheda Campagna {#campaign-global-objectives}

### Distribuzione {#delivery-global-objectives}

![](assets/campaign_report_global_1.png)

Il **[!UICONTROL Statistiche della campagna]** widget fornisce dettagli sulle informazioni principali relative alla campagna:

* **[!UICONTROL Profili immessi]**: numero di profili che hanno avviato il percorso.

* **[!UICONTROL Azioni consegnate]**: numero totale di volte in cui è stata consegnata un’azione nel percorso.

* **[!UICONTROL Azioni non riuscite in %]**: numero totale di volte in cui un’azione non è riuscita nel percorso rispetto al numero totale di volte in cui è stata consegnata un’azione.

### Relazione sugli obiettivi {#objective-global}

>[!AVAILABILITY]
>
>Il **Relazione sugli obiettivi** Questa funzione è attualmente disponibile solo per un set di organizzazioni (disponibilità limitata). Per ulteriori informazioni, contatta il tuo rappresentante Adobe.

![](assets/performance_report.gif)

Il **[!UICONTROL Obiettivi]** Questa scheda ti consente di perfezionare meglio i rapporti delle consegne eseguendo il targeting di una metrica specifica.

Il **[!UICONTROL Obiettivi]** elencati sono collegati a **[!UICONTROL Set di dati]** che definiscono una connessione a un sistema per il recupero di informazioni aggiuntive. Elenco di elementi incorporati **[!UICONTROL Obiettivi]** è disponibile, ma puoi aggiungerne uno nuovo aggiungendo nuove **[!UICONTROL Set di dati]**. Per la procedura dettagliata, fare riferimento al seguente [sezione](../campaigns/reporting-configuration.md).

Dopo aver selezionato gli obiettivi di destinazione, i due **[!UICONTROL Panoramica delle prestazioni]** e **[!UICONTROL Finalità della campagna]** I widget forniranno un riepilogo dettagliato delle prestazioni di consegna.

Con il **[!UICONTROL Finalità della campagna]** widget, puoi anche scegliere di confrontare l’obiettivo principale con un’altra metrica.

### Rapporto sulla sperimentazione {#experimentation-global-objectives}

![](assets/experimentation_report_3.png)

Il **[!UICONTROL Sperimentazione]** fornisce informazioni chiave sulle prestazioni di ciascuna variante e identifica quella di maggior successo.

La definizione dell&#39;esecutore migliore potrebbe richiedere un po&#39; di tempo, sarà rappresentata da questa icona ![](assets/experimentation_report_1.png).

+++Ulteriori informazioni sulle diverse metriche e widget disponibili per il rapporto Sperimentazione.

Il **[!UICONTROL Risultato esperimento]** il widget descrive le prestazioni di ogni variante. È possibile modificare la linea di base selezionando uno dei trattamenti tra **[!UICONTROL Linea di base]** il menu a discesa. Il miglior trattamento sarà rappresentato da un’icona a forma di stella.

La tabella presenta le metriche seguenti:

* **[!UICONTROL Incremento rispetto alla linea di base]**: misura del miglioramento percentuale del tasso di conversione di un dato trattamento rispetto al basale.

* **[!UICONTROL Affidabilità]**: evidenza che un dato trattamento è uguale al trattamento di base. [Ulteriori informazioni](../campaigns/experiment-calculations.md#understand-confidence)

* **[!UICONTROL Clic in uscita univoci]**: numero totale di clic tra i canali in uscita.

* **[!UICONTROL Profili]**: numero di profili target per questo trattamento.

* **[!UICONTROL Clic/profili in uscita univoci]**: valore totale della metrica di successo, precedentemente selezionata durante la creazione degli esperimenti, diviso per il numero di profili.

Il **[!UICONTROL Intervallo di affidabilità]** Il grafico misura l’incertezza riguardo al miglioramento. Descrive la differenza percentuale nelle prestazioni tra la linea di base e il trattamento dalle prestazioni migliori. [Ulteriori informazioni](../campaigns/experiment-calculations.md#confidence-intervals).
+++

Per informazioni approfondite su questi risultati e su come interpretarli, consulta [questa pagina](../campaigns/get-started-experiment.md#interpret-results).
