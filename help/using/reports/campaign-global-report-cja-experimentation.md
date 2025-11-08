---
solution: Journey Optimizer
product: journey optimizer
title: Rapporto campagna
description: Scopri come utilizzare i dati della sperimentazione dal rapporto della campagna
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 69742163-7378-49ab-929e-86213d6e65e3
source-git-commit: b8d56578aae90383092978446cb3614a4a033f80
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 9%

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

+++ Ulteriori informazioni sulle metriche dei KPI per la sperimentazione

* **[!UICONTROL Incremento]**: misura del miglioramento percentuale del tasso di conversione di un determinato trattamento rispetto al basale.

* **[!UICONTROL Affidabilità]**: prova che un determinato trattamento è uguale al trattamento basale. [Ulteriori informazioni](../content-management/experiment-calculations.md#adobes-statistical-methodology-any-time-valid-confidence-sequences)

+++

### Variante per metrica di successo {#variant-inbound}

![](assets/cja-experimentation-variants.png)

La tabella **Variante per metriche di successo** mostra le prestazioni di ogni variante in base alla metrica di successo selezionata durante l&#39;impostazione dell&#39;esperimento.
Per informazioni approfondite su questi risultati e su come interpretarli, consulta [questa pagina](../content-management/get-started-experiment.md#interpret-results).

+++ Ulteriori informazioni sulla variante per metrica di successo

* **[!UICONTROL Persone]**: numero di profili utente qualificati come profili target per i messaggi.

* **[!UICONTROL Clic in entrata]**: valore totale della metrica di successo, precedentemente selezionata durante la creazione degli esperimenti.

* **[!UICONTROL Tasso di conversione]**: valore totale della metrica di successo, precedentemente selezionata durante la creazione degli esperimenti, diviso per il numero di profili.

* **[!UICONTROL Incremento]**: misura del miglioramento percentuale del tasso di conversione di un determinato trattamento rispetto al basale.

* **[!UICONTROL Limite inferiore affidabilità]**: valore stimato più basso della differenza del tasso di conversione tra il trattamento e la linea di base, entro l&#39;intervallo di affidabilità scelto.

* **[!UICONTROL Affidabilità]**: prova che un determinato trattamento è uguale al trattamento basale. [Ulteriori informazioni](../content-management/experiment-calculations.md#adobes-statistical-methodology-any-time-valid-confidence-sequences)

* **[!UICONTROL Limite superiore affidabilità]**: valore massimo stimato della differenza del tasso di conversione tra il trattamento e la linea di base, entro l&#39;intervallo di affidabilità scelto.

+++

### Tasso di conversione per metrica di successo {#conversion-rate}

![](assets/cja-experimentation-conversion.png)


Il grafico **[!UICONTROL Intervallo di affidabilità]** mostra l&#39;intervallo di possibili miglioramenti, confrontando la linea di base con il trattamento dalle prestazioni migliori per la metrica di successo scelta. [Ulteriori informazioni](../content-management/experiment-calculations.md#adobes-statistical-methodology-any-time-valid-confidence-sequences).