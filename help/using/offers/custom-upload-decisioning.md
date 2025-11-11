---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Sfruttare i tipi di pubblico con caricamento personalizzato per la funzione Decisioni
description: Scopri come sfruttare i tipi di pubblico di caricamento personalizzati per prendere decisioni.
badge: label="Legacy" type="Informative"
feature: Decision Management
role: User
level: Intermediate
exl-id: bd950410-691b-49d8-8851-8c6c448c00fd
version: Journey Orchestration
source-git-commit: d6a9a8a392f0492aa6e4f059198ce77b6b2cd962
workflow-type: tm+mt
source-wordcount: '533'
ht-degree: 2%

---

# Sfruttare i tipi di pubblico con caricamento personalizzato per la funzione Decisioni {#custom-upload-decisioning}

Con Journey Optimizer puoi sfruttare i dati dei tipi di pubblico creati utilizzando il caricamento personalizzato (file CSV) in Adobe Experience Platform per supportare i flussi di lavoro di gestione delle decisioni. Ciò è particolarmente utile quando i dati non sono necessari sul profilo, ma sono ancora essenziali a fini decisionali.

I dati dei tipi di pubblico di caricamento personalizzati possono essere utilizzati in Gestione delle decisioni per:

1. Criteri di idoneità nelle offerte e nelle decisioni.
2. Personalizzazione del contenuto nelle rappresentazioni delle offerte.

Per ulteriori informazioni sui tipi di pubblico di caricamento personalizzati, consulta le sezioni:

* [Guida introduttiva a Audiences e Journey Optimizer](../audience/about-audiences.md)
* [Importazione di un pubblico in Adobe Experience Platform](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-portal#import-audience){target="_blank"}

## Da leggere {#must-read}

* Questa funzionalità è supportata solo in **Gestione delle decisioni**, non in Decisioning (precedentemente noto come &quot;Experience Decisioning&quot;).
* È disponibile esclusivamente tramite le richieste **Decisioning API (Hub)** e non è supportato da **Edge Decisioning API** o **batch decisioning**.

## Utilizzare un pubblico di caricamento personalizzato come criterio di idoneità {#eligibilty}

Puoi utilizzare un pubblico di caricamento personalizzato come criterio di idoneità a livello di offerta o decisione. Una volta aggiunti, questi criteri possono escludere offerte o raccolte di offerte dall’idoneità. Di seguito sono elencate le varie posizioni in cui puoi sfruttare i tipi di pubblico di caricamento personalizzati per perfezionare le offerte e l’idoneità alle decisioni:

* Creare una regola di decisione utilizzando un pubblico di caricamento personalizzato:

   1. Quando crei una regola, accedi alla scheda **Tipi di pubblico** e cerca il tuo pubblico CSV nell&#39;elenco. Trascina e rilascia il pubblico nell’area di lavoro della regola.
   1. Utilizza la scheda **Attributi** e passa agli schemi di arricchimento collegati al pubblico selezionato per accedere a tutti i dati dal file CSV e utilizzarli nella regola. Questo ti consente di utilizzare un campo del file CSV per perfezionare la regola. [Scopri come creare una regola di decisione](../offers/offer-library/creating-decision-rules.md)
   1. Salva la regola. Una volta creata, la regola può essere utilizzata a livello sia di offerta che di decisione per perfezionarne l’idoneità.

  ![](assets/csv-rule.png)

* Utilizza i tipi di pubblico di caricamento personalizzati come vincolo di offerta. [Scopri come aggiungere vincoli a un&#39;offerta](../offers/offer-library/add-constraints.md)

  Durante l&#39;authoring di un&#39;offerta, nel passaggio **Aggiungi vincoli** puoi effettuare le seguenti operazioni:

   * Utilizza il pubblico di caricamento personalizzato per definire l’idoneità dell’offerta,
   * Applica una regola che sfrutta il pubblico di caricamento personalizzato.

  ![](assets/csv-offer.png)

* Utilizza i tipi di pubblico di caricamento personalizzati a livello decisionale.

  Durante la configurazione di una decisione, nel passaggio **Aggiungi ambito decisione**, puoi utilizzare i tipi di pubblico per il caricamento personalizzati come criterio di valutazione per una raccolta di offerte. [Scopri come definire l’ambito della decisione](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)

  ![](assets/csv-decision.png)

## Utilizzare un pubblico di caricamento personalizzato per personalizzare le rappresentazioni delle offerte

I tipi di pubblico per caricamento personalizzati possono essere utilizzati anche per personalizzare il contenuto delle rappresentazioni delle offerte facendo riferimento ai dati del file CSV. [Scopri come aggiungere rappresentazioni a un&#39;offerta](../offers/offer-library/add-representations.md)

Per poter sfruttare gli attributi di personalizzazione di un pubblico di caricamento personalizzato, devi innanzitutto aggiungere il pubblico personalizzato come vincolo. A questo scopo, durante l&#39;authoring di un&#39;offerta, nel passaggio **Aggiungi vincoli**, aggiungi il pubblico come vincoli o seleziona una regola che sfrutta il pubblico di caricamento personalizzato.

![](assets/csv-offer.png)

Una volta aggiunto il pubblico come vincolo, puoi utilizzarne gli attributi per personalizzare il contenuto della rappresentazione. Per farlo, accedi alla scheda **Attributi del profilo** e cerca il pubblico di caricamento personalizzato. Seleziona gli attributi rilevanti dal pubblico per personalizzare il contenuto dell’offerta.

![](assets/csv-perso.png)
