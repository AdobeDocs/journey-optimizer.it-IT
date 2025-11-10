---
title: Passaggi chiave per creare un’offerta
description: Scopri i passaggi chiave necessari per creare un’offerta
badge: label="Legacy" type="Informative"
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
exl-id: e375fd3a-b10d-45f4-a95b-ceb48116e841
version: Journey Orchestration
source-git-commit: 0b94bfeaf694e8eaf0dd85e3c67ee97bd9b56294
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 7%

---

# Passaggi chiave per creare e gestire le offerte {#key-steps-to-manage-offers}

Di seguito sono riportati i passaggi principali per creare, configurare e gestire le offerte, nonché per utilizzarle in una decisione.

![](../assets/offer-create-manage-process.png)

Per un esempio completo end-to-end che mostra come configurare le offerte, utilizzarle in una decisione e sfruttare questa decisione in un messaggio e-mail, vedi [questa pagina](../offers-e2e.md).

## Creare componenti {#create-components}

Prima di iniziare a creare le offerte, devi definire diversi componenti da utilizzare nelle offerte.

1. [Crea posizionamenti](creating-placements.md), che sono contenitori che verranno utilizzati per mostrare le offerte. Ad esempio, puoi creare un posizionamento dedicato alle offerte solo in formato immagine e posizionato nella parte superiore dei messaggi.

1. [Crea regole di decisione](creating-decision-rules.md) che specificheranno le condizioni in cui verranno presentate le offerte.

1. [Crea qualificatori di raccolta](creating-tags.md) (noti in precedenza come &quot;tag&quot;) che assocerai alle offerte, per organizzarle ed eseguirne facilmente la ricerca nella libreria.

1. Se desideri definire regole che determinano quale offerta deve essere presentata per prima per un determinato posizionamento (anziché tenere conto dei punteggi di priorità delle offerte), puoi [creare una formula di classificazione](../ranking/create-ranking-formulas.md).

<!--
<table style="table-layout:fixed">
<tr style="border: 0;">
<td>
<img src="../../assets/do-not-localize/icon-placement.svg" width="60px">
<div>
<a href="../offer-library/creating-placements.md">Create placements</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-rules.svg" width="60px">
<div>
<a href="../offer-library/creating-decision-rules.md">Create decision rules</a>
</div>
<p>
<td>
<img src="../../assets/do-not-localize/icon-tags.svg" width="60px">
<div>
<a href="../offer-library/creating-tags.md">Create collection qualifiers</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-ranking.svg" width="60px">
<div>
<a href="../ranking/create-ranking-formulas.md">Create ranking formulas</a>
</div>
<p>
</td>
</tr>
</table>
-->

## Creare e gestire le offerte {#create-and-manage-offers}

1. [Crea offerte](creating-personalized-offers.md) e configurane contenuto e proprietà.

1. [Crea offerte di fallback](creating-fallback-offers.md), che sono le offerte di ultima istanza da visualizzare se i clienti non sono idonei per nessuna delle offerte selezionate.

1. [Crea una raccolta](creating-collections.md) per includere le offerte personalizzate create e utilizzarle in una decisione.

<!--
<table style="table-layout:fixed">
<tr style="border: 0;">
<td>
<img src="../../assets/do-not-localize/icon-offer.svg" width="60px">
<div>
<a href="../offer-library/creating-personalized-offers.md">Create offers</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-fallback.svg" width="60px">
<div>
<a href="../offer-library/creating-fallback-offers.md">Create fallback offers</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-collection.svg" width="60px">
<div>
<a href="../offer-library/creating-collections.md">Create collections</a>
</div>
<p>
</td>
</tr>
</table>
-->

## Creare e configurare decisioni {#create-and-configure-decisions}

1. [Crea una decisione](../offer-activities/create-offer-activities.md) che combinerà i posizionamenti con le offerte personalizzate e le offerte di fallback. Questa combinazione verrà utilizzata dal motore decisionale per trovare l’offerta migliore per un profilo specifico.

1. [Configura la decisione](../offer-activities/create-offer-activities.md#add-decision-scopes). A questo scopo, seleziona i posizionamenti e, per ogni posizionamento, seleziona una raccolta e un fallback.

1. Se necessario, puoi [assegnare una formula di classificazione](../offer-activities/configure-offer-selection.md#assign-ranking-formula) o [classificazione IA](../offer-activities/configure-offer-selection.md#use-ranking-strategy) a un posizionamento durante la configurazione della decisione.

<!--
<table style="table-layout:fixed">
<tr style="border: 0;">
<td>
<img src="../../assets/do-not-localize/icon-decision.svg" width="60px">
<div>
<a href="../offer-activities/create-offer-activities.md">Create decisions</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-configure-decision.svg" width="60px">
<div>
<a href="../offer-activities/create-offer-activities.md#add-offers">Configure decisions</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-assign-ranking.svg" width="60px">
<div>
<a href="../offer-activities/configure-offer-selection.md#assign-ranking-formula">Assign ranking</a>
</div>
<p>
</td>
</tr>
</table>
-->