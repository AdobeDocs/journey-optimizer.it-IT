---
title: Passaggi chiave per creare un’offerta
description: Scopri i passaggi chiave necessari per creare un’offerta.
feature: Offerte
topic: Integrazioni
role: User
level: Intermediate
source-git-commit: 5631a1937b854c3e14d1816df9e8d30690588303
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 11%

---

# Passaggi chiave per creare e gestire le offerte {#key-steps}

Di seguito sono descritti i passaggi principali per creare, configurare e gestire le offerte e per utilizzarle in una decisione.

![](../../assets/offer-create-manage-process.png)

Per un esempio completo e completo che mostri come configurare le offerte, utilizzale in una decisione e sfrutta questa decisione in un’e-mail, controlla [questa pagina](../offers-e2e.md).

## Creare componenti

Prima di iniziare a creare le offerte, devi definire diversi componenti da utilizzare nelle offerte.

1. **Crea posizionamenti**, ovvero contenitori che verranno utilizzati per mostrare le offerte. Ad esempio, puoi creare un posizionamento che sarà dedicato solo alle offerte in formato immagine e situato nella parte superiore dei messaggi.

1. **Creare** regole decisionali che specifichino le condizioni in cui verranno presentate le offerte.

1. **Crea** tag da associare alle offerte, consentendoti di organizzarli ed effettuare ricerche facilmente nella libreria.

1. Se desideri definire regole che determinino quale offerta presentare per prima per un determinato posizionamento (anziché tenere conto dei punteggi di priorità delle offerte), puoi **creare una formula di classificazione**.

<table>
<tr>
<td><img src="../../assets/do-not-localize/icon-placement.svg" width="60px"><p><a href="../offer-library/creating-placements.md">Creare posizionamenti</a></p></td>
<td><img src="../../assets/do-not-localize/icon-rules.svg" width="60px"><p><a href="../offer-library/creating-decision-rules.md">Creare regole di decisione</a></p></td>
<td><img src="../../assets/do-not-localize/icon-tags.svg" width="60px"><p><a href="../offer-library/creating-tags.md">Creare tag</a></p></td>
<td><img src="../../assets/do-not-localize/icon-ranking.svg" width="60px"><p><a href="../offer-library/create-ranking-formulas.md">Creare formule di classificazione</a></p></td>
</table>

## Creare e gestire le offerte

1. **Crea offerte** e configurane contenuto e proprietà.

1. **Crea offerte** di fallback, che sono le offerte di ultima risorsa da visualizzare se i clienti non sono idonei per nessuna delle offerte selezionate.

1. **Crea una** raccolta per includere le offerte personalizzate create e utilizzale in una decisione.

<table>
<tr>
<td><img src="../../assets/do-not-localize/icon-offer.svg" width="60px"><p><a href="../offer-library/creating-personalized-offers.md">Creare offerte</a></p></td>
<td><img src="../../assets/do-not-localize/icon-fallback.svg" width="60px"><p><a href="../offer-library/creating-fallback-offers.md">Creare offerte di fallback</a></p></td>
<td><img src="../../assets/do-not-localize/icon-collection.svg" width="60px"><p><a href="../offer-library/creating-collections.md">Creare raccolte</a></p></td></tr>
</table>

## Creare e configurare le decisioni

1. **Crea una** decisione che combini posizionamenti con offerte personalizzate e offerte di fallback. Questa combinazione verrà utilizzata dal motore di Offer decisioning per trovare l’offerta migliore per un profilo specifico.

1. **Configura la decisione**. A questo scopo, seleziona i posizionamenti e, per ogni posizionamento, seleziona una raccolta e un fallback.

1. Se necessario, è possibile **assegnare una formula di classificazione** a un posizionamento durante la configurazione della decisione.

<table>
<tr>
<td><img src="../../assets/do-not-localize/icon-decision.svg" width="60px"><p><a href="../offer-activities/create-offer-activities.md">Creare decisioni</a></p></td>
<td><img src="../../assets/do-not-localize/icon-configure-decision.svg" width="60px"><p><a href="../offer-activities/create-offer-activities.md#add-offers">Configurare le decisioni</a></p></td>
<td><img src="../../assets/do-not-localize/icon-assign-ranking.svg" width="60px"><p><a href="../offer-activities/configure-offer-selection.md#assign-ranking-formula">Assegna classificazione</a></p></td>
</tr>
</table>
