---
solution: Journey Optimizer
product: journey optimizer
title: Introduzione all’ottimizzazione dei contenuti
description: Scopri come utilizzare l’ottimizzazione dei contenuti per fornire contenuti personalizzati e ottimizzati nelle campagne e nei percorsi.
feature: Experimentation, Targeting
topic: Content Management
role: User
level: Beginner
keywords: ottimizzazione, targeting, sperimentazione, test A/B, campagne, percorsi, personalizzazione
exl-id: 0f563d61-7a9e-46bf-adfb-5a26e63505b9
source-git-commit: 27de3d2171e6f6575eb66ada20f951f6cb3abc98
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 8%

---

# Introduzione all’ottimizzazione dei contenuti {#message-optimization}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_optimization"
>title="Ottimizzazione dei contenuti"
>abstract="L’ottimizzazione dei contenuti in Journey Optimizer consente di testare diverse versioni dei contenuti e di determinare quale offre le prestazioni migliori. Puoi utilizzare il targeting per fornire contenuti personalizzati a segmenti specifici, la sperimentazione per testare più varianti o combinare entrambi gli approcci per sofisticate strategie di ottimizzazione."

L’ottimizzazione dei contenuti ti offre gli strumenti per inviare il messaggio giusto al pubblico giusto al momento giusto. Combinando informazioni basate sui dati con potenti funzionalità di personalizzazione, puoi massimizzare il coinvolgimento e le conversioni nelle campagne e nei percorsi.

L&#39;ottimizzazione dei contenuti è disponibile sia nelle [campagne](../campaigns/create-campaign.md) che nei [percorsi](../building-journeys/journey-gs.md), consentendo di applicare le stesse strategie di ottimizzazione in tutti i punti di contatto dei clienti.

➡️ [Scopri come sfruttare l&#39;ottimizzazione dei contenuti in una campagna in questo video](#video)

## Funzionalità di ottimizzazione {#capabilities}

Con l’ottimizzazione dei contenuti in Journey Optimizer, puoi:

* [Utilizza il targeting](optimization-targeting.md) per fornire contenuti personalizzati a segmenti di pubblico specifici in base agli attributi del profilo, ai dati contestuali o all&#39;iscrizione al pubblico.

* [Esegui esperimenti](optimization-experimentation.md) per testare più varianti di contenuto e identificare quale funziona meglio in base alle metriche di successo.

* [Combina entrambi gli approcci](optimization-combination.md) per creare strategie di ottimizzazione sofisticate in cui testare diverse varianti per ciascun segmento di destinazione.

## Targeting e sperimentazione {#targeting-vs-experimentation}

Comprendere la differenza tra targeting e sperimentazione ti aiuta a scegliere l’approccio di ottimizzazione corretto per i tuoi obiettivi.

**Il targeting** utilizza regole deterministiche per distribuire contenuti personalizzati a segmenti specifici in base ad attributi di profilo noti, contesto o appartenenza a un pubblico. In questo modo il messaggio giusto arriva al pubblico giusto.

**La sperimentazione** utilizza l&#39;assegnazione casuale per testare più varianti di contenuto e individuare le migliori prestazioni. Ti aiuta a scoprire cosa risuona di più con il tuo pubblico attraverso test basati sui dati.

La tabella seguente riassume le principali differenze:

| Funzionalità | Targeting | Sperimentazione |
|--------|-----------|-----------------|
| **Metodo di assegnazione** | Deterministico - basato su regole | Casuale: in base all’allocazione del traffico |
| **Basato su** | Attributi di profilo, contesto, pubblico | Distribuzione casuale |
| **Caso d’uso** | Distribuire contenuti rilevanti a segmenti noti | Scopri quale contenuto offre le prestazioni migliori |
| **Esempio** | Mostra diverse promozioni per posizione | Prova 2 righe dell’oggetto per vedere quale si apre di più |
| **Ottimo per** | Personalization su larga scala | Ottimizzazione e apprendimento |

![](../campaigns/assets/msg-optimization-experiment-vs-targeting.png){width="110%" zoomable="yes"}

## Casi d’uso comuni {#use-cases}

Di seguito sono riportati alcuni scenari tipici in cui l’ottimizzazione dei contenuti può aiutarti a ottenere risultati migliori:

Targeting:

* **Geotargeting**: invia offerte specifiche per la posizione in base alla posizione in cui si trovano i clienti. Ad esempio, promuovere cappotti invernali nelle regioni più fredde e costumi da bagno nei climi più caldi.

* **Ottimizzazione del dispositivo** - Distribuisci contenuti specifici per il dispositivo, ad esempio layout ottimizzati per il desktop per gli utenti desktop e layout ottimizzati per dispositivi mobili per gli utenti di smartphone.

Sperimentazione:

* **Test A/B** - Verifica diverse righe dell&#39;oggetto dell&#39;e-mail, pulsanti di call-to-action o offerte promozionali per scoprire quale è il motore della maggior parte delle conversioni.

* **Lifecycle marketing**: verifica diversi messaggi di onboarding per i nuovi clienti rispetto alle offerte di fidelizzazione per i clienti esistenti.

Combinazione

* **Segmentazione avanzata**: esegui il targeting dei clienti per livello fedeltà e testa diversi messaggi di ricompensa all&#39;interno di ciascun livello per massimizzare il coinvolgimento in tutti i segmenti.

## Introduzione {#get-started}

Per iniziare a ottimizzare il contenuto:

1. **Crea una campagna o un percorso**: configura la [campagna](../campaigns/create-campaign.md) o il [percorso](../building-journeys/journey-gs.md) e aggiungi almeno un&#39;azione.

1. **Scegli il tuo approccio di ottimizzazione**:
   * [Utilizza il targeting](optimization-targeting.md) per personalizzare il contenuto per segmenti specifici.
   * [Utilizza la sperimentazione](optimization-experimentation.md) per testare più varianti.
   * [Combina entrambi](optimization-combination.md) per l&#39;ottimizzazione avanzata.

1. **Definisci il contenuto**: crea diverse varianti di contenuto per la strategia di ottimizzazione.

1. **Attiva e monitora**: avvia la campagna o il percorso ottimizzato e tieni traccia delle prestazioni nei [rapporti](../reports/campaign-global-report-cja.md).

## Come funziona {#how-it-works}

Una volta che il percorso o la campagna è attiva, i profili vengono valutati in base ai criteri definiti. In base a queste valutazioni, ogni profilo riceve la versione di contenuto più appropriata:

1. **Valutazione profilo** - Quando un profilo entra nella campagna o nel percorso, Journey Optimizer ne valuta gli attributi e il contesto.

1. **Assegnazione contenuto** - In base alla configurazione di ottimizzazione:
   * Per il **targeting**, i profili che corrispondono a criteri specifici ricevono il contenuto personalizzato corrispondente.
   * Per **sperimentazione**, i profili vengono assegnati in modo casuale a diverse varianti di contenuto in base alle impostazioni di allocazione del traffico.
   * Per **combinazioni**, i profili prima corrispondono a una regola di targeting, quindi vengono assegnati in modo casuale a una delle varianti dell&#39;esperimento per quel segmento.

1. **Tracciamento delle prestazioni** - Journey Optimizer tiene traccia automaticamente delle metriche di coinvolgimento e dei dati di conversione per identificare il contenuto con le prestazioni migliori.

## Video dimostrativo {#video}

Scopri come sfruttare l’ottimizzazione dei contenuti nelle campagne attivate da azioni o API. Scoprirai come eseguire il targeting dei tipi di pubblico secondari, creare varianti di messaggio per posizione, abilitare il contenuto di fallback ed eseguire più esperimenti all’interno di una singola campagna. Questo tutorial illustra anche come gestire le campagne multicanale mantenendo al contempo la coerenza dei messaggi.

>[!VIDEO](https://video.tv.adobe.com/v/3470376?captions=ita&quality=12)

**Argomenti correlati**

* [Creare una campagna](../campaigns/create-campaign.md)
* [Creare un percorso](../building-journeys/journey-gs.md)
* [Esperimento contenuti](../content-management/get-started-experiment.md)
