---
solution: Journey Optimizer
product: journey optimizer
title: Monitorare le prestazioni della sfida fedeltà
description: Scopri come utilizzare le dashboard di reporting Sfide di fedeltà per monitorare le prestazioni e le informazioni sulle sfide in Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
badge: label="Beta privata" type="Informative"
mini-toc-levels: 1
exl-id: a1b2c3d4-e5f6-7890-abcd-ef1234567890
feature_v2: []
subfeature_v2: []
source-git-commit: 61005da7b43e9b21ab720bbb1ef86317345137cd
workflow-type: tm+mt
source-wordcount: 586
ht-degree: 4%

---

# Monitorare le prestazioni della sfida fedeltà {#loyalty-reporting}

>[!BEGINSHADEBOX]

**Sommario**

[Introduzione alle sfide di fedeltà](get-started.md)

<table style="table-layout:fixed">
<tr style="border: 0;">
<td style="vertical-align:top;">

**Crea e gestisci le sfide**

* [Accesso e gestione di sfide e attività](access-loyalty-challenges.md)
* [Creare le sfide](create-challenges.md)
* [Creare le attività](create-tasks.md)
* **Monitora le prestazioni della sfida fedeltà** ◀︎ **Sei qui**

</td>
<td style="vertical-align:top;">

**Configura e integra**

* [Configurare le sfide relative alla fedeltà](loyalty-admin.md)
* [Dati e set di dati sulla fedeltà](loyalty-data-and-datasets.md)
* [Riferimento API per le sfide di fedeltà](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

</td>
</tr>
</table>

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Questa funzionalità è attualmente in **versione beta privata**. Per informazioni dettagliate sul ciclo di rilascio e sulle fasi di disponibilità, consulta [Ciclo di rilascio di Journey Optimizer](../rn/releases.md).

Utilizza il reporting sulle sfide di fidelizzazione per vedere come stanno andando le tue sfide. Controlla chi si iscrive, chi sta completando le sfide e quanti ricavi genera il programma, il tutto in un’unica posizione. I dati provengono da Adobe Customer Journey Analytics.

Per aprire le dashboard di reporting, vai a **[!UICONTROL Sfide fedeltà (Beta)]** in Journey Optimizer e seleziona **[!UICONTROL Rapporti fedeltà]** nella navigazione a sinistra.

L’interfaccia di reporting dispone di due schede:

* **[Rapporti](#reports-view)**: numeri e grafici per le sfide.
* **[Approfondimenti](#insights-cards)**: schede che evidenziano ciò che merita la tua attenzione in questo momento.

## Visualizzazione Rapporti {#reports-view}

La scheda **Rapporti** offre una panoramica delle prestazioni del programma per il periodo selezionato. Utilizza il selettore data nella parte superiore della pagina e seleziona il pulsante **[!UICONTROL Applica filtro]** per modificare il periodo di reporting e visualizzare numeri e grafici aggiornati.

![](assets/reporting-challenge-key.png)

Nell&#39;area **Metriche chiave** sono visualizzati quattro numeri. Ogni metrica mostra anche una variazione percentuale rispetto al periodo precedente.

* **Membri fedeltà**: quanti membri fedeltà erano attivi durante il periodo.
* **Iscrizioni alle sfide**: quante volte i membri sono stati iscritti a una sfida.
* **Ricavi**: ricavi totali associati all&#39;attività di verifica.
* **Tasso medio di completamento**: percentuale di membri iscritti che hanno completato almeno una verifica.

Il pannello **Informazioni più recenti** a destra mostra le informazioni generate dall&#39;intelligenza artificiale più recenti del programma. Seleziona **[!UICONTROL Visualizza tutto]** per aprire la scheda **Informazioni** completa.

Sotto le metriche chiave, la sezione **Sfide** offre due visualizzazioni dell&#39;attività di sfida.

![](assets/reporting-challenge-challenges.png)

* **Impegno sfida**: una sequenza temporale che mostra quanti membri hanno iniziato, sono in corso e hanno completato le sfide nel periodo.
* **Report sulle sfide**: tabella di tutte le sfide con dettagli quali tipo, attività, stato e numeri di iscrizione. Utilizza la barra di ricerca per trovare una sfida specifica. Seleziona una sfida per visualizzarne il rapporto completo con le tendenze di coinvolgimento e i dettagli delle prestazioni.

  +++Esempio di rapporto sulla sfida

  ![](assets/reporting-challenge-report.png)

  +++

## Scheda Approfondimenti {#insights-cards}

La scheda **Insights** presenta schede generate dall&#39;intelligenza artificiale che segnalano anomalie, tendenze e opportunità nel programma fedeltà. Ogni scheda rappresenta una singola osservazione e viene classificata in base alla sua importanza rispetto ai dati del programma corrente.

![](assets/reporting-insights.png)

Una marca temporale **Ultimo scansionato** in alto a destra mostra quando il motore di insight ha elaborato i dati del programma per l&#39;ultima volta.

### Azioni della carta {#insight-card-actions}

Ogni scheda ha un menu ![](assets/do-not-localize/Smock_More_18_N.svg) con due azioni:

* **Ignora**: rimuove definitivamente la scheda dall&#39;elenco delle informazioni.
* **Posponi**: nasconde temporaneamente la scheda. Scegli di posporre per **1 giorno**, **3 giorni** o **7 giorni**. La scheda viene visualizzata nuovamente al termine del periodo di Posponi.

<!--
### Priority badges {#insight-badges}

Each card has a priority badge — **High**, **Medium**, or **Low** — based on how significant the underlying signal is relative to your current program data. These levels are relative: there are always a few **High** cards, even in a quiet week. **High** means "most relevant right now", not that a fixed threshold was crossed.
-->

### Tag categoria {#insight-category-tags}

Ogni scheda contiene un **tag di categoria** che identifica la parte del programma a cui si riferisce insight.

| Categoria | Cosa copre |
| --- | --- |
| **A livello di programma** | Stato generale e prestazioni del programma fedeltà |
| **Livello** | Guadagna tassi, spostamento e distribuzione tra i livelli membro |
| **Sfida** | Attività, tassi di completamento e anomalie per una sfida specifica o per più sfide |
| **Prodotto** | Prestazioni del catalogo dei prodotti, comprese visualizzazioni, rimborsi e tendenze a livello di catalogo |
| **Ciclo di vita membro** | Modalità di avanzamento dei membri nelle fasi di iscrizione, coinvolgimento e abbandono |
| **Tendenza** | Modelli basati sul tempo come cicli settimanali, picchi stagionali o inversioni di tendenza |
