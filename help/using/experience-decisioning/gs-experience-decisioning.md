---
title: Introduzione a Offer Decisioning
description: Ulteriori informazioni su Experience Decisioning
feature: Offers
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: 4c57dbf9-b2a4-42da-8aa3-5a1b3a475a32
source-git-commit: c4ab97999d000d969f6f09f4d84be017d1288f94
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 18%

---

# Introduzione a Offer Decisioning {#get-started-experience-decisioning}

>[!BEGINSHADEBOX]

Cosa troverai in questa documentazione:

* **[Introduzione a Offer Decisioning](gs-experience-decisioning.md)**
* Gestire gli elementi decisionali
   * [Configurare il catalogo degli elementi](catalogs.md)
   * [Creare elementi decisionali](items.md)
   * [Gestire le raccolte di elementi](collections.md)
* Configurare la selezione degli elementi
   * [Creare regole di decisione](rules.md)
   * [Creare metodi di classificazione](ranking.md)
* [Creare strategie di selezione](selection-strategies.md)
* [Creare criteri di decisione](create-decision.md)

>[!ENDSHADEBOX]

## Cos’è Experience Decisioning {#about}

>[!AVAILABILITY]
>
>La funzione Experience Decisioning è attualmente disponibile come versione beta solo per alcuni utenti. Per partecipare al programma beta, contatta l’Assistenza clienti Adobe.

Experience Decisioning semplifica la personalizzazione offrendo un catalogo centralizzato di offerte di marketing note come &quot;elementi decisionali&quot; e un motore decisionale sofisticato. Questo motore sfrutta le regole e i criteri di classificazione per selezionare e presentare a ogni individuo gli elementi decisionali più rilevanti.

Questi elementi decisionali vengono integrati direttamente in un’ampia gamma di superfici in entrata tramite il nuovo canale di esperienza basato su codice, ora accessibile nelle campagne Journey Optimizer.

**Limitazioni:**

* I criteri di decisione sono disponibili per l’utilizzo solo nelle campagne di esperienza basate su codice.
* Per il momento, la quota limite non è disponibile in Experience Decisioning.

## Passaggi chiave di Experience Decisioning {#steps}

I passaggi principali per lavorare con Experience Decisioning sono i seguenti:

1. **Configurare gli attributi personalizzati**: personalizza il catalogo degli elementi decisionali in base ai tuoi requisiti specifici impostando attributi personalizzati nello schema del catalogo.

1. **Creare elementi decisionali** per mostrarlo al pubblico di destinazione.

1. **Organizzare con le raccolte**: utilizza le raccolte per categorizzare gli elementi decisionali in base a regole basate su attributi. Incorpora le raccolte nelle strategie di selezione per determinare quale raccolta di elementi decisionali deve essere considerata.

1. **Creare regole di decisione**: le regole di decisione vengono utilizzate negli elementi di decisione e/o nelle strategie di selezione per determinare a chi può essere visualizzato un elemento di decisione.

1. **Implementare metodi di classificazione**: crea metodi di classificazione e applicali all’interno di strategie decisionali per determinare l’ordine prioritario per la selezione degli elementi decisionali.

1. **Creare strategie di selezione**: crea strategie di selezione che sfruttano raccolte, regole di decisione e metodi di classificazione per identificare gli elementi di decisione adatti per la visualizzazione nei profili.

1. **Incorporare un criterio di decisione nella campagna basata su codice**: i criteri di decisione combinano più strategie di selezione per determinare gli elementi di decisione idonei da visualizzare al pubblico previsto.
