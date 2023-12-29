---
title: Passaggi chiave per creare un’offerta
description: Scopri i passaggi chiave necessari per creare un’offerta
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
exl-id: e375fd3a-b10d-45f4-a95b-ceb48116e841
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 11%

---

# Passaggi chiave per creare e gestire le offerte {#key-steps-to-manage-offers}

Di seguito sono riportati i passaggi principali per creare, configurare e gestire le offerte, nonché per utilizzarle in una decisione.

![](../assets/offer-create-manage-process.png)

Per un esempio completo end-to-end che mostra come configurare le offerte, utilizzarle in una decisione e sfruttare questa decisione in un messaggio e-mail, vedi [questa pagina](../offers-e2e.md).

## Creare componenti {#create-components}

Prima di iniziare a creare le offerte, devi definire diversi componenti da utilizzare nelle offerte.

1. **Creare posizionamenti**, che sono contenitori che verranno utilizzati per presentare le offerte. Ad esempio, puoi creare un posizionamento dedicato alle offerte solo in formato immagine e posizionato nella parte superiore dei messaggi.

1. **Creare regole di decisione** che specificherà le condizioni alle quali le offerte saranno presentate.

1. **Creare qualificatori di raccolta** (precedentemente noti come &quot;tag&quot;) che verranno associati alle offerte, per organizzarle ed eseguirne facilmente la ricerca nella libreria.

1. Se desideri definire regole che determinano quale offerta deve essere presentata per prima per un determinato posizionamento (anziché tenere conto dei punteggi di priorità delle offerte), puoi **creare una formula di classificazione**.

<table style="table-layout:fixed">
<tr style="border: 0;">
<td>
<img src="../../assets/do-not-localize/icon-placement.svg" width="60px">
<div>
<a href="../offer-library/creating-placements.md">Creare posizionamenti</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-rules.svg" width="60px">
<div>
<a href="../offer-library/creating-decision-rules.md">Creare regole di decisione</a>
</div>
<p>
<td>
<img src="../../assets/do-not-localize/icon-tags.svg" width="60px">
<div>
<a href="../offer-library/creating-tags.md">Creare i tag</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-ranking.svg" width="60px">
<div>
<a href="../ranking/create-ranking-formulas.md">Creare formule di classificazione</a>
</div>
<p>
</td>
</tr>
</table>

## Creare e gestire le offerte {#create-and-manage-offers}

1. **Creare le offerte** e configurarne contenuto e proprietà.

1. **Creare le offerte di fallback**, che sono le offerte di ultima istanza da mostrare se i clienti non sono idonei per nessuna delle offerte selezionate.

1. **Creare una raccolta** per includere le offerte personalizzate create e utilizzarle in una decisione.

<table style="table-layout:fixed">
<tr style="border: 0;">
<td>
<img src="../../assets/do-not-localize/icon-offer.svg" width="60px">
<div>
<a href="../offer-library/creating-personalized-offers.md">Creare le offerte</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-fallback.svg" width="60px">
<div>
<a href="../offer-library/creating-fallback-offers.md">Creare offerte di fallback</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-collection.svg" width="60px">
<div>
<a href="../offer-library/creating-collections.md">Creare raccolte</a>
</div>
<p>
</td>
</tr>
</table>

## Creare e configurare decisioni {#create-and-configure-decisions}

1. **Creare una decisione** che combinerà i posizionamenti con le offerte personalizzate e le offerte di fallback. Questa combinazione verrà utilizzata dal motore decisionale per trovare l’offerta migliore per un profilo specifico.

1. **Configurare la decisione**. A questo scopo, seleziona i posizionamenti e, per ogni posizionamento, seleziona una raccolta e un fallback.

1. Se necessario, puoi **assegna una formula di classificazione** in un posizionamento durante la configurazione della decisione.

<table style="table-layout:fixed">
<tr style="border: 0;">
<td>
<img src="../../assets/do-not-localize/icon-decision.svg" width="60px">
<div>
<a href="../offer-activities/create-offer-activities.md">Creare decisioni</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-configure-decision.svg" width="60px">
<div>
<a href="../offer-activities/create-offer-activities.md#add-offers">Configurare le decisioni</a>
</div>
<p>
</td>
<td>
<img src="../../assets/do-not-localize/icon-assign-ranking.svg" width="60px">
<div>
<a href="../offer-activities/configure-offer-selection.md#assign-ranking-formula">Assegna classificazione</a>
</div>
<p>
</td>
</tr>
</table>
