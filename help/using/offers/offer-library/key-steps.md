---
title: Passaggi chiave per creare un’offerta
description: Scopri i passaggi chiave necessari per creare un’offerta
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: e375fd3a-b10d-45f4-a95b-ceb48116e841
source-git-commit: c530905eacbdf6161f6449d7a0b39c8afaf3a321
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 13%

---

# Passaggi chiave per creare e gestire le offerte {#key-steps-to-manage-offers}

Di seguito sono descritti i passaggi principali per creare, configurare e gestire le offerte e per utilizzarle in una decisione.

![](../assets/offer-create-manage-process.png)

Per un esempio completo, completo e completo, che mostra come configurare le offerte, utilizzale in una decisione e sfrutta questa decisione in un’e-mail, consulta [questa pagina](../offers-e2e.md).

## Creare componenti {#create-components}

Prima di iniziare a creare le offerte, devi definire diversi componenti da utilizzare nelle offerte.

1. **Creare posizionamenti**, contenitori che verranno utilizzati per mostrare le offerte. Ad esempio, puoi creare un posizionamento che sarà dedicato solo alle offerte in formato immagine e situato nella parte superiore dei messaggi.

1. **Creare regole decisionali** che specifichi le condizioni alle quali verranno presentate le offerte.

1. **Creare tag** che verranno associate alle offerte, consentendoti di organizzarle facilmente e cercarle nella libreria.

1. Se desideri definire regole che determinino quale offerta deve essere presentata per prima per un determinato posizionamento (anziché tenere conto dei punteggi di priorità delle offerte), puoi **creare una formula di classificazione**.

<table>
<tr>
<td><img src="../../assets/do-not-localize/icon-placement.svg" width="60px"><p><a href="../offer-library/creating-placements.md">Creare posizionamenti</a></p></td>
<td><img src="../../assets/do-not-localize/icon-rules.svg" width="60px"><p><a href="../offer-library/creating-decision-rules.md">Creare regole di decisione</a></p></td>
<td><img src="../../assets/do-not-localize/icon-tags.svg" width="60px"><p><a href="../offer-library/creating-tags.md">Creare tag</a></p></td>
<td><img src="../../assets/do-not-localize/icon-ranking.svg" width="60px"><p><a href="../ranking/create-ranking-formulas.md">Creare formule di classificazione</a></p></td>
</table>

## Creare e gestire le offerte {#create-and-manage-offers}

1. **Creare offerte** e configurane il contenuto e le proprietà.

1. **Creare offerte di fallback**, che è l’ultima risorsa da visualizzare se i clienti non sono idonei per nessuna delle offerte selezionate.

1. **Creare una raccolta** per includere le offerte personalizzate create e utilizzarle in una decisione.

<table>
<tr>
<td><img src="../../assets/do-not-localize/icon-offer.svg" width="60px"><p><a href="../offer-library/creating-personalized-offers.md">Creare offerte</a></p></td>
<td><img src="../../assets/do-not-localize/icon-fallback.svg" width="60px"><p><a href="../offer-library/creating-fallback-offers.md">Creare offerte di fallback</a></p></td>
<td><img src="../../assets/do-not-localize/icon-collection.svg" width="60px"><p><a href="../offer-library/creating-collections.md">Creare raccolte</a></p></td></tr>
</table>

## Creare e configurare le decisioni {#create-and-configure-decisions}

1. **Creare una decisione** che combinerà posizionamenti con offerte personalizzate e offerte di fallback. Questa combinazione verrà utilizzata dal motore decisionale per trovare l’offerta migliore per un profilo specifico.

1. **Configurare la decisione**. A questo scopo, seleziona i posizionamenti e, per ogni posizionamento, seleziona una raccolta e un fallback.

1. Se necessario, puoi **assegnare una formula di classificazione** a un posizionamento durante la configurazione della decisione.

<table>
<tr>
<td><img src="../../assets/do-not-localize/icon-decision.svg" width="60px"><p><a href="../offer-activities/create-offer-activities.md">Creare decisioni</a></p></td>
<td><img src="../../assets/do-not-localize/icon-configure-decision.svg" width="60px"><p><a href="../offer-activities/create-offer-activities.md#add-offers">Configurare le decisioni</a></p></td>
<td><img src="../../assets/do-not-localize/icon-assign-ranking.svg" width="60px"><p><a href="../offer-activities/configure-offer-selection.md#assign-ranking-formula">Assegna classificazione</a></p></td>
</tr>
</table>
