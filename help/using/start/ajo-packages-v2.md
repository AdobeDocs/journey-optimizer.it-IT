---
solution: Journey Optimizer
product: journey optimizer
title: Pacchetti e funzionalità di Journey Optimizer
description: Scopri come Adobe Journey Optimizer è confezionato e quali funzionalità sono disponibili in base all’offerta di base, ai componenti aggiuntivi per il canale e ai componenti aggiuntivi per funzionalità avanzate.
feature: Get Started
topic: Content Management
role: Admin, User
level: Beginner
keywords: Ottimizzatore percorso, pacchetto, licenza, campagne, percorsi, canali, decisioni, in uscita, mobile, web, modulare
hide: true
source-git-commit: 46a5a6dc0a3486633a1a71f8bba8a3cd53aaa618
workflow-type: tm+mt
source-wordcount: '974'
ht-degree: 2%

---


# Pacchetti e funzionalità di Adobe Journey Optimizer {#ajo-packages-v2}

>[!BEGINSHADEBOX]

**In questa pagina:** scopri come funziona il pacchetto modulare di Adobe Journey Optimizer tra le offerte di base, i componenti aggiuntivi per il canale e il componente aggiuntivo Decisioning, in modo da poter scegliere la combinazione che si adatta ai tuoi casi d&#39;uso del coinvolgimento e al budget.

>[!ENDSHADEBOX]

[!DNL Adobe Journey Optimizer] utilizza un modello di packaging modulare. Inizia con l’offerta di base che corrisponde al tuo caso d’uso principale, quindi aggiungi i canali e le funzionalità avanzate necessari.

>[!NOTE]
>
>La disponibilità del pacchetto e le funzionalità incluse possono variare in base al contratto, ai componenti aggiuntivi selezionati e alla disponibilità regionale. Contatta il tuo rappresentante Adobe per i dettagli specifici della tua organizzazione.

## Passaggio 1 — Scegliere l&#39;offerta di base {#base-offers}

Sono disponibili tre offerte base. Scegli quello che corrisponde al modo in cui coinvolgi principalmente i clienti.

| Offerta base | Ideale per | Comportamento di base |
|-----------|---------|--------------|
| **Journey Optimizer - Campagne** | Batch, attività pianificata dall’addetto al marketing | Orchestrazione pianificata basata sul pubblico. Flussi di lavoro per campagne in un solo passaggio o con più passaggi utilizzando l’archivio dati relazionale. |
| **Journey Optimizer - Percorsi** | Coinvolgimento dei clienti in tempo reale | Orchestrazione 1:1 basata su eventi. Supporta sia l&#39;elaborazione in streaming che quella in percorso batch. |
| **Journey Optimizer - Campagne e Percorsi** | Clienti che necessitano di entrambi | Combina l’orchestrazione delle campagne basata sul pubblico e l’orchestrazione del percorso in tempo reale. |

### Campagne e Percorsi: qual è la differenza? {#campaigns-vs-journeys}

| | Journey Optimizer - Campagne | JOURNEY OPTIMIZER - PERCORSI | Journey Optimizer - Campagne e Percorsi |
|--|:-----------------------------:|:----------------------------:|:----------------------------------------:|
| Orchestrazione batch basata sul pubblico | ✓ | Limitato ai casi d’uso del percorso | ✓ |
| Orchestrazione basata su eventi in tempo reale | — | ✓ | ✓ |
| Messaggistica transazionale (e-mail, push, SMS) | ✓ | ✓ | ✓ |
| Componenti aggiuntivi per il canale disponibili | ✓ | ✓ | ✓ |
| Componente aggiuntivo Decisioning disponibile | ✓ | ✓ | ✓ |

>[!NOTE]
>
>Il volume di dati totale è diverso: **Campagne** i clienti ricevono 15 KB per profilo indirizzabile; **Percorsi** e **Campagne e Percorsi** i clienti ricevono 75 KB per profilo indirizzabile.

## Passaggio 2 — Aggiungere i canali necessari {#channel-addons}

I canali non sono inclusi nell’offerta di base. Seleziona il componente aggiuntivo di canale o il bundle aggiuntivo che si adatta alla tua strategia di coinvolgimento.

>[!BEGINTABS]

>[!TAB Consegna in uscita]

Raggiungi il pubblico tramite i canali di messaggistica in uscita.

**Include:** e-mail, notifiche push, direct mail

**Casi d&#39;uso tipici:** e-mail promozionali, avvisi push transazionali, campagne e-mail fisiche

**Superfici supportate:** casella in entrata, schermata di blocco dispositivo mobile/vassoio di notifica, indirizzo postale

Include Deliverability Fundamentals per il supporto della preparazione IP nelle nuove istanze. [Informazioni sul recapito messaggi](../reports/deliverability.md)

>[!TAB Mobile]

Coinvolgi gli utenti dell’app con esperienze mobili persistenti e in sessione.

**Include:** messaggi in-app, notifiche push, schede di contenuto, canali basati su codice per superfici mobili

**Casi d&#39;uso tipici:** flussi di onboarding, annunci di funzionalità, spunti fedeltà, offerte in-app in tempo reale

**Superfici supportate:** schermi dell&#39;app mobile, barra delle notifiche, slot di contenuto persistente, superfici dell&#39;app personalizzata tramite SDK

>[!TAB Web]

Personalizza le esperienze web senza distribuire il codice.

**Include:** canale Web (editor visivo e non visivo), canali basati su codice per superfici Web

**Casi d&#39;uso tipici:** banner home page, personalizzazione della pagina di destinazione, test A/B, personalizzazione web headless tramite API

**Superfici supportate:** pagine browser, app a pagina singola (SPA), endpoint Web headless

>[!TAB Tutti i canali]

Il componente aggiuntivo **Tutti i canali** raggruppa Consegna in uscita + Mobile + Web in un singolo acquisto.

Ideale per le organizzazioni che necessitano di una copertura omnicanale completa su superfici in uscita, app mobile e web.

>[!ENDTABS]

**WhatsApp** è disponibile come componente aggiuntivo separato per i clienti che devono inviare messaggi tramite WhatsApp Business. [Scopri come utilizzare WhatsApp](../whatsapp/get-started-whatsapp.md)

## Passaggio 3 — Aggiungere funzionalità avanzate {#advanced-addons}

### Funzione Decisioni {#decisioning-addon}

Il componente aggiuntivo **Decisioning** ti consente di definire, gestire e distribuire l&#39;offerta, l&#39;azione o l&#39;esperienza migliore per ogni profilo in tempo reale, su qualsiasi canale.

**Sblocco:**
- Selezione di offerte in tempo reale tramite regole di idoneità, logica di classificazione e vincoli
- Modelli di classificazione basati sull’intelligenza artificiale per ottimizzare automaticamente le prestazioni delle offerte
- Criteri di decisione utilizzabili in percorsi, campagne ed esperienze basate su codice

**Disponibile il:** tutte e tre le offerte base, in base al contratto di licenza. [Scopri come utilizzare il decisioning](../experience-decisioning/gs-experience-decisioning.md) | [Scopri i modelli AI](../offers/ranking/ai-models.md)

## Confronto immediato {#comparison-matrix}

| Funzionalità | Journey Optimizer - Campagne | JOURNEY OPTIMIZER - PERCORSI | Journey Optimizer - Campagne e Percorsi | Componente aggiuntivo richiesto |
|-----------|:-----------------------------:|:----------------------------:|:----------------------------------------:|:---------------:|
| Messaggistica transazionale (e-mail, push, SMS) | ✓ | ✓ | ✓ | — |
| Campagne batch | ✓ | — | ✓ | — |
| Campagne orchestrate _(solo e-mail, SMS, push, direct mail)_ | ✓ | — | ✓ | — |
| Percorsi automatizzati | — | ✓ | ✓ | — |
| Trigger di eventi in tempo reale | — | ✓ | ✓ | — |
| E-mail | ✓ | ✓ | ✓ | Consegna in uscita |
| Notifiche push | ✓ | ✓ | ✓ | Consegna in uscita |
| Direct mail | ✓ | ✓ | ✓ | Consegna in uscita |
| SMS/MMS | ✓ | ✓ | ✓ | Consegna in uscita |
| Messaggistica in-app | ✓ | ✓ | ✓ | Mobile |
| Schede contenuto | ✓ | ✓ | ✓ | Mobile |
| Canale web | ✓ | ✓ | ✓ | Web |
| Esperienze basate su codice | ✓ | ✓ | ✓ | Mobile o Web |
| WhatsApp | ✓ | ✓ | ✓ | WhatsApp |
| Funzione Decisioni | Dipende dalla licenza | Dipende dalla licenza | Dipende dalla licenza | Funzione Decisioni |
| Classificazione basata su AI | Dipende dalla licenza | Dipende dalla licenza | Dipende dalla licenza | Funzione Decisioni |

## Domande frequenti {#faq}

+++**Ogni offerta di base include ogni canale?**

No. [!DNL Adobe Journey Optimizer] utilizza un modello modulare: l&#39;offerta di base determina la capacità di orchestrazione (campagne, Percorsi o entrambi) e i componenti aggiuntivi del canale determinano le superfici di messaggistica che è possibile coinvolgere. È possibile scegliere la combinazione adatta al caso d’uso e al budget.

+++

+++**Qual è la differenza tra campagne e Percorsi?**

Le **campagne** sono basate su pubblico e pianificate dall&#39;addetto al marketing: puoi definire un pubblico, creare un messaggio e pianificarlo o attivarlo come invio batch. Sono ideali per l’utilizzo a scopo promozionale, le newsletter e i flussi di lavoro con più passaggi.

I **Percorsi** sono in tempo reale e basati su eventi: reagiscono al comportamento dei singoli clienti mentre si verifica e orchestrano 1:1 esperienze tra punti di contatto. Sono ideali per flussi di onboarding, sequenze post-acquisto e messaggi attivati in tempo reale.

**Campagne e Percorsi** offre entrambe le funzionalità in un&#39;unica licenza.

+++

+++**Quali canali sono supportati nelle campagne orchestrate?**

Le campagne orchestrate (flussi di lavoro di pubblico in più passaggi che utilizzano la funzione di orchestrazione delle campagne) supportano solo **e-mail, SMS, notifiche push e direct mail**. I canali web, in-app, basati su codice e schede di contenuto non sono supportati nei flussi di lavoro orchestrati per le campagne.

+++

+++**Decisioning è incluso in ogni configurazione?**

No. Decisioning è un componente aggiuntivo di funzionalità avanzato distinto e non è incluso in alcuna offerta di base per impostazione predefinita. Contatta il tuo rappresentante Adobe per aggiungere Decisioning alla configurazione.

+++

+++**Ho sentito parlare di Select, Prime o Ultimate. È ancora il modello di pacchetto corrente?**

[!DNL Adobe Journey Optimizer] è ora offerto tramite un modello di pacchetto modulare basato su offerte base (campagne, Percorsi, campagne e Percorsi) e componenti aggiuntivi. Se sei un cliente esistente che utilizza la terminologia Select, Prime o Ultimate e hai domande sulle adesioni correnti, contatta il rappresentante Adobe.

+++
