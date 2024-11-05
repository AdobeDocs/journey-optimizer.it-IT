---
solution: Journey Optimizer
product: journey optimizer
title: Rapporto campagna
description: Scopri come utilizzare i dati della sperimentazione dal rapporto della campagna
feature: Reporting
topic: Content Management
role: User
level: Intermediate
source-git-commit: 47482adb84e05fe41eb1c50479a8b50e00469ec4
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 11%

---

# Rapporto sulla sperimentazione della campagna {#campaign-global-report-cja-experimentation}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_click"
>title="Metrica di successo"
>abstract="Valore totale della metrica Successo, precedentemente selezionata durante la creazione degli esperimenti, diviso per il numero di profili."

## Sperimentazione {#experimentation}

La scheda **[!UICONTROL Sperimentazione]** fornisce informazioni chiave sulle prestazioni di ogni variante e identifica quella che ha avuto maggior successo.

Si noti che la definizione dell&#39;esecutore migliore potrebbe richiedere un po&#39; di tempo. Se l&#39;esperimento non ha esito positivo, verrà impostato su **Non conclusivo**.

![](assets/cja-experimentation-1.png)

### KPI della sperimentazione {#experimentation-kpis}

![](assets/cja-experimentation-kpis.png)

I **[!UICONTROL Indicatori prestazioni chiave (KPI, Key Performance Indicators) della sperimentazione]** funzionano come dashboard completo che fornisce un&#39;analisi delle metriche essenziali associate alla sperimentazione.

+++ Ulteriori informazioni sulle metriche dei KPI nella sperimentazione

* **[!UICONTROL Incremento]**: misura del miglioramento percentuale del tasso di conversione di un determinato trattamento rispetto al basale.

* **[!UICONTROL Affidabilità]**: prova che un determinato trattamento è uguale al trattamento basale. [Ulteriori informazioni](../content-management/experiment-calculations.md#understand-confidence)

+++

### Variante per clic in entrata {#variant-inbound}

![](assets/cja-experimentation-variants.png)

Il widget **[!UICONTROL Variante per clic in entrata]** descrive le prestazioni di ogni variante.
Per informazioni approfondite su questi risultati e su come interpretarli, consulta [questa pagina](../content-management/get-started-experiment.md#interpret-results).

+++ Ulteriori informazioni sulla variante per metriche di clic in entrata

* **[!UICONTROL Persone]**: numero di profili utente qualificati come profili target per i messaggi.

* **[!UICONTROL Clic in entrata]**: numero totale di clic tra i canali in uscita.

* **[!UICONTROL Tasso di conversione]**: valore totale della metrica di successo, precedentemente selezionata durante la creazione degli esperimenti, diviso per il numero di profili.

* **[!UICONTROL Incremento]**: misura del miglioramento percentuale del tasso di conversione di un determinato trattamento rispetto al basale.

* **[!UICONTROL Affidabilità]**: prova che un determinato trattamento è uguale al trattamento basale. [Ulteriori informazioni](../content-management/experiment-calculations.md#understand-confidence)

<!--
* **[!UICONTROL Confidence Upper bound]**:

* **[!UICONTROL Confidence Lower bound]**:
-->
+++

### Tasso di conversione per i clic in entrata {#conversion-rate}

![](assets/cja-experimentation-conversion.png)

Il grafico **[!UICONTROL Intervallo di affidabilità]** misura l&#39;incertezza sul miglioramento. Descrive la differenza percentuale nelle prestazioni tra la linea di base e il trattamento dalle prestazioni migliori. [Ulteriori informazioni](../content-management/experiment-calculations.md#confidence-intervals).
