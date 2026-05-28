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
exl-id: ec1af88c-7b0a-4eaf-97e1-0d9676268fed
badge: label="Beta" type="Informative"
TQID: https://experienceleague.adobe.com/x-01SLf7JHabLWahy--Kbf8OQIDaUbu7r6YrM-vSs0o
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a9f73820-6899-47c2-a597-3fec28ab756aid: b49ca41f-eb7a-4f4b-abeb-a97c06fd0c04
subfeature_v2: id: d145add9-d5b9-481b-aa8a-e15e6bb7f813id: a7289281-9ae4-47b1-b8cf-4028b98af776id: b5afe8bf-bda6-41b5-ba06-922638872d63
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: bcc5edb5-84c3-4940-9f84-ed88b6c16274id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 481
ht-degree: 4%

---

# Rapporto globale della campagna {#objective-report}

Il report globale della campagna è accessibile direttamente dalla campagna con il pulsante **[!UICONTROL Visualizza report]**.

Il **[!UICONTROL report globale]** della campagna è suddiviso in diversi widget che descrivono il successo e gli errori della campagna. Ogni widget può essere ridimensionato ed eliminato, se necessario. Per ulteriori informazioni, fare riferimento a <!--[section](../reports/global-report.md#modify-dashboard)-->.

Per un elenco dettagliato di tutte le metriche disponibili in Adobe Journey Optimizer, fare riferimento a <!--[this page](global-report.md#list-of-components-global.md)-->

## Scheda Campagna {#campaign-global-objectives}

### Consegna {#delivery-global-objectives}

<!--
![](assets/campaign_report_global_1.png)
-->

Il widget Statistiche ]**della**[!UICONTROL  campagna descrive le informazioni principali relative alla campagna:

* **[!UICONTROL Profili immessi]**: numero di profili che hanno avviato il percorso.

* **[!UICONTROL Azioni consegnate]**: numero totale di volte in cui un&#39;azione nel percorso è stata consegnata.

* **[!UICONTROL Azioni non riuscite in %]**: numero totale di volte in cui un&#39;azione non è riuscita nel percorso rispetto al numero totale di volte in cui un&#39;azione è stata consegnata.

### Relazione sugli obiettivi {#objective-global}

>[!AVAILABILITY]
>
>La funzionalità **Report obiettivi** è attualmente disponibile solo per un set di organizzazioni (disponibilità limitata). Per ulteriori informazioni, contatta il tuo rappresentante Adobe.

![](assets/performance_report.gif)

La scheda **[!UICONTROL Obiettivi]** ti consente di ottimizzare i rapporti delle consegne eseguendo il targeting di una metrica specifica.

Gli **[!UICONTROL obiettivi]** elencati sono collegati a **[!UICONTROL Set di dati]** che definiscono una connessione a un sistema per il recupero di informazioni aggiuntive. È disponibile un elenco di **[!UICONTROL Obiettivi]** incorporati, ma puoi aggiungerne di nuovi aggiungendo un **[!UICONTROL Set di dati]**. Per la procedura dettagliata, consulta questa [sezione](../reports/reporting-configuration.md).

Dopo aver selezionato gli obiettivi per i quali desideri eseguire il targeting, i due widget **[!UICONTROL Panoramica delle prestazioni]** e **[!UICONTROL Obiettivo campagna]** forniranno un riepilogo dettagliato delle prestazioni della consegna.

Con il widget **[!UICONTROL Obiettivo campagna]**, puoi anche scegliere di confrontare l&#39;obiettivo principale con un&#39;altra metrica.

### Rapporto sulla sperimentazione {#experimentation-global-objectives}

<!--
![](assets/experimentation_report_3.png)
-->

La scheda **[!UICONTROL Sperimentazione]** fornisce informazioni chiave sulle prestazioni di ogni variante e identifica quella che ha avuto maggior successo.

La definizione dell&#39;esecutore migliore potrebbe richiedere un po&#39; di tempo, verrà rappresentata da questa icona ![](assets/experimentation_report_1.png).

+++Ulteriori informazioni sulle diverse metriche e widget disponibili per il rapporto Sperimentazione.

Il widget **[!UICONTROL Risultato esperimento]** descrive le prestazioni di ogni variante. Puoi modificare la linea di base selezionando uno dei trattamenti dal menu a discesa **[!UICONTROL Baseline]**. Il miglior trattamento sarà rappresentato da un’icona a forma di stella.

La tabella presenta le metriche seguenti:

* **[!UICONTROL Incremento rispetto al basale]**: misura del miglioramento percentuale del tasso di conversione di un determinato trattamento rispetto al basale.

* **[!UICONTROL Affidabilità]**: prova che un determinato trattamento è uguale al trattamento basale. [Ulteriori informazioni](../content-management/experiment-calculations.md#adobes-statistical-methodology-any-time-valid-confidence-sequences)

* **[!UICONTROL Clic in uscita univoci]**: numero totale di clic tra i canali in uscita.

* **[!UICONTROL Profili]**: numero di profili target per questo trattamento.

* **[!UICONTROL Clic/profili in uscita univoci]**: valore totale della metrica di successo, precedentemente selezionata durante la creazione degli esperimenti, diviso per il numero di profili.

Il grafico **[!UICONTROL Intervallo di affidabilità]** misura l&#39;incertezza sul miglioramento. Descrive la differenza percentuale nelle prestazioni tra la linea di base e il trattamento dalle prestazioni migliori. [Ulteriori informazioni](../content-management/experiment-calculations.md#adobes-statistical-methodology-any-time-valid-confidence-sequences).
+++

Per informazioni approfondite su questi risultati e su come interpretarli, consulta [questa pagina](../content-management/get-started-experiment.md#interpret-results).
