---
solution: Journey Optimizer
product: journey optimizer
title: Rapporto sull’esperimento percorso
description: Scopri come utilizzare i dati della sperimentazione dal rapporto sul Percorso
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: a2b4ef74-96a9-4907-ba70-7aee69e45f20
TQID: https://experienceleague.adobe.com/oN7VFQvhQlwNa2U5CmcAYkGbKb0Vnxc7yA5rCLDjQw4
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a9f73820-6899-47c2-a597-3fec28ab756a
  - id: b49ca41f-eb7a-4f4b-abeb-a97c06fd0c04
subfeature_v2:
  - id: d145add9-d5b9-481b-aa8a-e15e6bb7f813
  - id: a7289281-9ae4-47b1-b8cf-4028b98af776
  - id: b5afe8bf-bda6-41b5-ba06-922638872d63
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: bcc5edb5-84c3-4940-9f84-ed88b6c16274
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 7f28f19b11ead867b0851943fdd997dcc3af170b
workflow-type: tm+mt
source-wordcount: 407
ht-degree: 2%

---

# Rapporto sul percorso di sperimentazione {#campaign-global-report-cja-experimentation}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come leggere le metriche di sperimentazione nel rapporto percorso, inclusi i KPI dell&#39;esperimento, l&#39;incremento e l&#39;affidabilità e le prestazioni delle varianti in base alla metrica di successo per gli esperimenti su contenuti e percorsi.

>[!ENDSHADEBOX]

Il rapporto sul Percorso offre una visualizzazione completa delle prestazioni dell’esperimento, insieme alle metriche chiave necessarie per comprenderne l’impatto.

In Journey Optimizer, la sperimentazione di percorso è divisa in due tipi:

* [Esperimenti sui contenuti](../content-management/content-experiment.md)

  Tieni presente che le tabelle e i KPI dettagliati per l’esperimento sui contenuti sono gli stessi di un esperimento su percorsi. Se hai impostato un esperimento sui contenuti, consulta la [documentazione seguente](#experimentation).

* [Esperimenti di percorso](../building-journeys/optimize.md)

## Esperimento percorso {#experimentation}

### KPI della sperimentazione {#experimentation-kpis}

![](assets/journey-report-experiment-1.png)

Il riepilogo della **Sperimentazione** fornisce informazioni chiave sulle prestazioni dell&#39;esperimento e identifica quello più riuscito. Si noti che la definizione dell&#39;esecutore migliore potrebbe richiedere un po&#39; di tempo. Se l&#39;esperimento non ha esito positivo, verrà impostato su **Non conclusivo**.

I **indicatori di prestazioni chiave (KPI, Key Performance Indicators)** della sperimentazione fungono da dashboard completo e forniscono un&#39;analisi delle metriche essenziali associate alla sperimentazione.

+++ Ulteriori informazioni sulle metriche dei KPI per la sperimentazione

* **[!UICONTROL Incremento]**: misura del miglioramento percentuale del tasso di conversione di un determinato trattamento rispetto al basale.

* **[!UICONTROL Affidabilità]**: prova che un determinato trattamento è uguale al trattamento basale. [Ulteriori informazioni](../content-management/experiment-calculations.md#adobes-statistical-methodology-any-time-valid-confidence-sequences)

+++



### Variante per metriche di successo {#variant-inbound}

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
