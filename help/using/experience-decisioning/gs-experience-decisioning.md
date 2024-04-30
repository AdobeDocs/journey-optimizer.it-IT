---
title: Introduzione a Experience Decisioning
description: Ulteriori informazioni su Experience Decisioning
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta"
exl-id: 4c57dbf9-b2a4-42da-8aa3-5a1b3a475a32
source-git-commit: 98e3e770530facac6f9c69a72e77fc663ef5ed0c
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 27%

---

# Introduzione a Experience Decisioning {#get-started-experience-decisioning}

>[!BEGINSHADEBOX &quot;Cosa troverai in questa guida alla documentazione&quot;]

* **[Introduzione a Experience Decisioning](gs-experience-decisioning.md)**
* Gestire gli elementi decisionali: [Configurare il catalogo articoli](catalogs.md) - [Creare elementi decisionali](items.md) - [Gestire le raccolte elementi](collections.md)
* Configura la selezione degli elementi: [Creare regole di decisione](rules.md) - [Creare metodi di classificazione](ranking.md)
* [Creare strategie di selezione](selection-strategies.md)
* [Creare criteri di decisione](create-decision.md)

>[!ENDSHADEBOX]

## Cos’è Experience Decisioning {#about}

>[!AVAILABILITY]
>
>La funzione Experience Decisioning è attualmente disponibile come versione beta solo per alcuni utenti. Per partecipare al programma beta, contatta l’Assistenza clienti Adobe.
>
>I criteri di decisione sono disponibili per l’utilizzo solo nelle campagne di esperienza basate su codice.

La funzione Decisioni per le esperienze semplifica la personalizzazione proponendo un catalogo centralizzato di offerte di marketing note come “elementi decisionali” e un motore decisionale sofisticato. Questo motore sfrutta le regole e i criteri di classificazione per selezionare e presentare a ogni persona gli elementi decisionali più rilevanti.

Gli elementi decisionali sono integrati direttamente in un’ampia gamma di superfici in entrata tramite il nuovo canale di esperienza basato su codice, ora accessibile nelle campagne Journey Optimizer.

## Passaggi chiave di Experience Decisioning {#steps}

I passaggi principali per lavorare con Experience Decisioning sono i seguenti:

1. **Configurare gli attributi personalizzati**: personalizza il catalogo degli elementi decisionali in base ai tuoi requisiti specifici impostando attributi personalizzati nello schema del catalogo.

1. **Creare elementi decisionali** per mostrarlo al pubblico di destinazione.

1. **Organizzare con le raccolte**: utilizza le raccolte per categorizzare gli elementi decisionali in base a regole basate su attributi. Incorpora le raccolte nelle strategie di selezione per determinare quale raccolta di elementi decisionali deve essere considerata.

1. **Creare regole di decisione**: le regole di decisione vengono utilizzate negli elementi di decisione e/o nelle strategie di selezione per determinare a chi può essere visualizzato un elemento di decisione.

1. **Implementare metodi di classificazione**: crea metodi di classificazione e applicali all’interno di strategie decisionali per determinare l’ordine prioritario per la selezione degli elementi decisionali.

1. **Creare strategie di selezione**: crea strategie di selezione che sfruttano raccolte, regole di decisione e metodi di classificazione per identificare gli elementi di decisione adatti per la visualizzazione nei profili.

1. **Incorporare un criterio di decisione nella campagna basata su codice**: i criteri di decisione combinano più strategie di selezione per determinare gli elementi di decisione idonei da visualizzare al pubblico previsto.
