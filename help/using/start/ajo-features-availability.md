---
source-git-commit: 84aa39bfd480e5bcaa8a58c5ec29f1990e5ddc6f
workflow-type: tm+mt
source-wordcount: '2004'
ht-degree: 12%

---
Il file di origine della documentazione si trova nell’archivio dei documenti, non in questo progetto di pipeline. Poiché le istruzioni dicono di generare il markdown aggiornato completo, eccolo:

---

soluzione: Journey Optimizer
product: percorsi optimizer
title: Disponibilità delle funzioni di Journey Optimizer
description: Riferimento consolidato singolo per individuare le funzioni di Adobe Journey Optimizer disponibili, il relativo stato del ciclo di vita (Disponibilità generale, Disponibilità limitata o Beta), l&#39;offerta di base a cui si applicano e la data di spedizione, senza riferimenti incrociati alle note sulla versione.
funzione: Introduzione
topic: Gestione dei contenuti
ruolo: Amministratore, Utente
livello: Principiante, Intermedio
parole chiave: ottimizzatore del percorso, disponibilità delle funzionalità, disponibilità generale, disponibilità limitata, versione beta, ciclo di vita, data di rilascio, adesione, offerta di base, campagne, percorsi
hide: true
---

# Disponibilità delle funzionalità di Journey Optimizer {#ajo-features-availability}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri quali funzionalità di [!DNL Adobe Journey Optimizer] sono disponibili, in quale fase del ciclo di vita si trovano ciascuna (Disponibilità generale, Disponibilità limitata o Beta), a quale offerta di base si applicano e quando vengono spedite, in modo da poter rispondere a *&quot;Posso utilizzarle?&quot;* senza dover consultare le note sulla versione.

>[!ENDSHADEBOX]

Questa pagina consolida la disponibilità delle funzionalità in [!DNL Adobe Journey Optimizer] per consentirti di confermare cosa puoi utilizzare durante l&#39;ambito di pre-implementazione. Le feature sono raggruppate per area di capacità. All&#39;interno di ogni area, ogni funzione elenca il suo stato attuale del ciclo di vita, l&#39;offerta di base a cui si applica, la data in cui è diventata disponibile ed eventuali note sulla configurazione o sulle restrizioni regionali.

Le righe contrassegnate come **Funzionalità core** nella colonna *Disponibile da* sono caratteristiche fondamentali di lunga data generalmente disponibili da prima del 2026. Le righe con data riflettono le modifiche spedite nel 2026.

>[!IMPORTANT]
>
>**Perché non è possibile visualizzare una funzionalità nel mio ambiente?** Le funzionalità in **Disponibilità limitata** o **Beta** non sono visibili a tutti, ma vengono prima distribuite a un set limitato di organizzazioni. Se nell&#39;ambiente non viene visualizzata una funzionalità di cui hai letto informazioni, controllane lo stato di seguito: se si tratta di **LA** o **Beta**, contatta il rappresentante Adobe per richiedere l&#39;accesso. Una funzione elencata qui non significa che sia abilitata nell’ambiente.

>[!NOTE]
>
>**Disponibilità e adesione** Questa pagina tiene traccia del ciclo di vita e della disponibilità delle *funzionalità* (se una funzionalità è stata fornita e a quale scadenza). Se una funzionalità è *inclusa nella licenza* dipende dall&#39;offerta di base e dai componenti aggiuntivi. Vedere [Pacchetti e funzionalità](ajo-packages.md).

## Significato degli stati del ciclo di vita {#status-definitions}

| Stato | Che cosa significa |
|--------|--------------|
| **GA** — Disponibilità generale | Rilasciato in tutti gli ambienti. Disponibile per qualsiasi organizzazione la cui licenza include la funzionalità. |
| **LA** — Disponibilità limitata | Rilasciato a un gruppo ristretto di organizzazioni. **Contatta il tuo rappresentante Adobe** per richiedere l&#39;accesso. |
| **Beta** | Rilascio anticipato per valutazione. Può cambiare prima della disponibilità generale. Potrebbe essere necessario acconsentire. |

## Mappe da applicare alle offerte di base {#applies-to}

La colonna **Si applica a** fa riferimento alle tre [!DNL Adobe Journey Optimizer] offerte base:

- **Journey Optimizer - Campagne** — orchestrazione batch basata su pubblico
- **Journey Optimizer - Percorsi** - orchestrazione basata su eventi in tempo reale
- **Journey Optimizer - Campagne e Percorsi** — entrambi

Caratteristiche di canali, contenuti e piattaforme contrassegnate con **Tutte le offerte di base** sono disponibili indipendentemente dall&#39;offerta di base, ma la maggior parte richiede ancora il relativo canale o il componente aggiuntivo di funzionalità avanzate. Consulta [Pacchetti e funzionalità](ajo-packages.md) per i dettagli di adesione.

## Funzioni per area funzionale {#features-by-area}

>[!BEGINTABS]

>[!TAB Canali]

| Funzione | Stato | Applicabile a | Disponibile da | Note |
|---------|--------|-----------|-----------------|-------|
| Ottimizzazione del tempo di invio (STO) per la messaggistica mobile | Beta | Tutte le offerte di base | H2 2026 | Tempo di invio ottimale per profilo basato sull’intelligenza artificiale per SMS, RCS e WhatsApp; disponibile in percorsi e campagne |
| Nuovo canale di messaggi mobile (SMS, MMS, RCS) | GA | Tutte le offerte di base | 20 maggio 2026 | Unifica SMS/MMS/RCS; authoring RCS nativo (immagini, caroselli) |
| Deep link in E-mail designer | GA | Tutte le offerte di base | 12 maggio 2026 | Richiede la configurazione di un’app mobile |
| Ottimizzare le e-mail per le caselle in entrata IA | GA | Tutte le offerte di base | 17 aprile 2026 | Apple Intelligence, Gmail Gemini |
| Parametri del mittente nell’intestazione e-mail | GA | Tutte le offerte di base | Aprile 2026 | &quot;Mittente per conto di Da&quot; / &quot;tramite&quot; |
| Campo CC nelle impostazioni del canale e-mail | GA | Tutte le offerte di base | Aprile 2026 | Supporta la personalizzazione |
| Casella in entrata | GA | Tutte le offerte di base | 7 aprile 2026 | — |
| Canale di notifiche web push | GA | Tutte le offerte di base | 13 febbraio 2026 | Precedentemente Beta |
| Attività live per iOS | GA | Tutte le offerte di base | 3 marzo 2026 | schermata di blocco/isola dinamica; in precedenza Beta |
| Canale direct mail nei percorsi | GA | Percorsi; Campagne e Percorsi | 29 gennaio 2026 | Precedentemente LA |
| Canale direct mail nelle campagne orchestrate | GA | Campagne; Campagne e Percorsi | 28 gennaio 2026 | — |
| Canale LINE | GA | Tutte le offerte di base | 2025 | — |
| Supporto e tracciamento dei pulsanti WhatsApp | GA | Tutte le offerte di base | Maggio 2026 | Risposta rapida, URL/telefono CTA |
| E-mail | GA | Tutte le offerte di base | Funzionalità di base | Richiede il componente aggiuntivo Consegna in uscita |
| Notifiche push | GA | Tutte le offerte di base | Funzionalità di base | Richiede il componente aggiuntivo Consegna in uscita o Mobile |
| SMS/MMS | GA | Tutte le offerte di base | Funzionalità di base | In base alla configurazione con licenza |
| Direct mail | GA | Tutte le offerte di base | Funzionalità di base | Richiede il componente aggiuntivo Consegna in uscita |
| Messaggistica in-app | GA | Tutte le offerte di base | Funzionalità di base | Richiede il componente aggiuntivo Mobile |
| Schede contenuto | GA | Tutte le offerte di base | Funzionalità di base | Richiede il componente aggiuntivo Mobile |
| Canale web | GA | Tutte le offerte di base | Funzionalità di base | Richiede il componente aggiuntivo Web |
| Esperienze basate su codice | GA | Tutte le offerte di base | Funzionalità di base | Richiede il componente aggiuntivo per dispositivi mobili o web |
| Pagine di destinazione | GA | Tutte le offerte di base | Funzionalità di base | — |
| WhatsApp | GA | Tutte le offerte di base | Funzionalità di base | Richiede il componente aggiuntivo WhatsApp; in base alla configurazione con licenza |

>[!TAB Percorsi]

| Funzione | Stato | Applicabile a | Disponibile da | Note |
|---------|--------|-----------|-----------------|-------|
| Frammenti di percorso | GA | Percorsi; Campagne e Percorsi | 9 giugno 2026 | Nodi di percorso riutilizzabili; supporto di strumenti sandbox |
| Simulazione percorso | GA | Percorsi; Campagne e Percorsi | 9 giugno 2026 | Convalidare la logica con utenti simulati |
| Ottimizzazione del percorso del percorso - Targeting | GA | Percorsi; Campagne e Percorsi | 8 giugno 2026 | Targeting del percorso deterministico |
| Supporto di identificatori supplementari per tipi di pubblico esterni | GA | Percorsi; Campagne e Percorsi | 11 giugno 2026 | CSV e composizione federata del pubblico |
| Sperimentazione del percorso | GA | Percorsi; Campagne e Percorsi | 7 aprile 2026 | A/B e slot machine; &quot;Scala il vincitore&quot; |
| Attività di azione nei percorsi | GA | Percorsi; Campagne e Percorsi | 20 febbraio 2026 | Sostituisce le attività del canale nativo obsolete |
| Attività di decisione sui contenuti | GA | Percorsi; Campagne e Percorsi | 10 febbraio 2026 | Precedentemente LA |
| Ore di silenzio (esclusioni basate sul tempo) | GA | Percorsi; Campagne e Percorsi | 29 gennaio 2026 | Precedentemente LA |
| Assistente IA per le espressioni di percorso | Beta | Percorsi; Campagne e Percorsi | 3 giugno 2026 | Beta pubblico |
| Ottimizzazione del tempo di invio (STO) per la messaggistica mobile | Beta | Percorsi; Campagne e Percorsi | H2 2026 | Tempo di invio ottimale per profilo basato sull’intelligenza artificiale per SMS, RCS e WhatsApp; vedi scheda Canali |
| Arbitrato del percorso | LA | Percorsi; Campagne e Percorsi | 24 febbraio 2026 | Contatta il tuo rappresentante Adobe |
| Arbitrato di percorso - Modelli IA | LA | Percorsi; Campagne e Percorsi | Aprile 2026 | Contatta il tuo rappresentante Adobe |
| Supporto per la ricerca di set di dati nei percorsi | LA | Percorsi; Campagne e Percorsi | Marzo 2026 | Per i clienti autorizzati alla ricerca di set di dati |
| Invio ondata di messaggi in uscita (percorsi) | LA | Percorsi; Campagne e Percorsi | 16 marzo 2026 | GA nelle campagne; LA nei percorsi |
| Percorsi automatizzati (attivati da eventi) | GA | Percorsi; Campagne e Percorsi | Funzionalità di base | Orchestrazione in tempo reale 1:1 |
| Trigger di eventi in tempo reale | GA | Percorsi; Campagne e Percorsi | Funzionalità di base | — |
| Leggi percorsi di pubblico (basati sul pubblico) | GA | Percorsi; Campagne e Percorsi | Funzionalità di base | — |
| Rapporti sul percorso | GA | Percorsi; Campagne e Percorsi | Funzionalità di base | — |

>[!TAB Campagne]

| Funzione | Stato | Applicabile a | Disponibile da | Note |
|---------|--------|-----------|-----------------|-------|
| Campagne orchestrate concatenate | GA | Campagne; Campagne e Percorsi | 20 maggio 2026 | Attivare una campagna dall’attività Fine di un’altra campagna |
| Attività di query incrementale in campagne orchestrate | GA | Campagne; Campagne e Percorsi | 30 aprile 2026 | Effettua il targeting solo di profili/eventi idonei nuovi netti |
| Copiare campagne orchestrate tra sandbox | GA | Campagne; Campagne e Percorsi | Aprile 2026 | Le campagne importate sono allo stato di bozza |
| Attività di test nelle campagne orchestrate | GA | Campagne; Campagne e Percorsi | Marzo 2026 | — |
| Attivare campagne orchestrate utilizzando un segnale | GA | Campagne; Campagne e Percorsi | Marzo 2026 | Rimane una campagna batch |
| Categoria transazionale nelle campagne orchestrate | GA | Campagne; Campagne e Percorsi | Marzo 2026 | Implementato gradualmente per area geografica |
| Invio ondata di messaggi in uscita (campagne) | GA | Campagne; Campagne e Percorsi | 19 febbraio 2026 | LA in percorsi |
| Ottimizzazione del tempo di invio (STO) per la messaggistica mobile | Beta | Campagne; Campagne e Percorsi | H2 2026 | Tempo di invio ottimale per profilo basato sull’intelligenza artificiale per SMS, RCS e WhatsApp; vedi scheda Canali |
| Campagne batch | GA | Campagne; Campagne e Percorsi | Funzionalità di base | Invii pianificati basati su pubblico |
| Campagne orchestrate (flussi di lavoro con più passaggi) | GA | Campagne; Campagne e Percorsi | Funzionalità di base | solo e-mail, SMS, push, direct mail |
| Messaggistica transazionale | GA | Tutte le offerte di base | Funzionalità di base | e-mail, push, SMS; inclusi in ogni offerta base |

>[!TAB Contenuto e IA]

| Funzione | Stato | Applicabile a | Disponibile da | Note |
|---------|--------|-----------|-----------------|-------|
| Selettore dell’Advisor contenuti | GA | Tutte le offerte di base | 19 maggio 2026 | Ricerca semantica IA per risorse e frammenti |
| Integrazioni (origini dati di terze parti) | GA | Tutte le offerte di base | 4 maggio 2026 | Precedentemente Beta |
| Limita l’interruzione dell’ereditarietà nei frammenti | GA | Tutte le offerte di base | 21 maggio 2026 | Bloccare i frammenti in base alle modifiche locali |
| Integrazione Adobe Express | GA | Tutte le offerte di base | 23 aprile 2026 | Precedentemente LA |
| Assistente IA per le espressioni di personalizzazione | GA | Tutte le offerte di base | 13 aprile 2026 | Nell’editor di personalizzazione e in E-mail Designer |
| Convertire immagini in modelli di contenuto e-mail | GA | Tutte le offerte di base | 31 marzo 2026 | Precedentemente LA |
| Moduli personalizzati della pagina di destinazione | GA | Tutte le offerte di base | 26 marzo 2026 | Precedentemente LA (Stati Uniti e Australia) |
| Integrazione di modelli Firefly personalizzati e di immagini di terze parti | GA | Tutte le offerte di base | 2 marzo 2026 | Adobe, Partner (Gemini) e modelli personalizzati |
| Editor HTML avanzato per modelli e-mail | LA | Tutte le offerte di base | 10 marzo 2026 | Solo modelli di contenuto e-mail; contatta il tuo rappresentante |
| Modalità esperto e-mail nel contenuto dell’e-mail | LA | Tutte le offerte di base | 9 aprile 2026 | Contatta il tuo rappresentante Adobe |
| Temi di E-mail designer | LA | Tutte le offerte di base | 5 novembre 2025 | In precedenza Beta; contatta il tuo rappresentante |
| E-mail Designer (trascinamento della selezione) | GA | Tutte le offerte di base | Funzionalità di base | Authoring visivo e HTML |
| Frammenti di contenuto | GA | Tutte le offerte di base | Funzionalità di base | Blocchi di contenuto riutilizzabili |
| Modelli di contenuto | GA | Tutte le offerte di base | Funzionalità di base | — |
| Editor Personalization | GA | Tutte le offerte di base | Funzionalità di base | Personalizzazione basata su espressioni |
| Assistente IA per la generazione di contenuti | GA | Tutte le offerte di base | Funzionalità di base | Richiede condizioni di licenza IA |

>[!TAB Funzione Decisioni]

Tutte le funzionalità di Decisioning richiedono il componente aggiuntivo **Decisioning**. Consulta [Pacchetti e funzionalità](ajo-packages.md).

| Funzione | Stato | Applicabile a | Disponibile da | Note |
|---------|--------|-----------|-----------------|-------|
| Supporto della funzione Decisioni nel canale direct mail | GA | Tutte le offerte di base | 3 giugno 2026 | Supporta le decisioni in batch |
| Regole per le decisioni e ottimizzazione con l’IA delle formule di classificazione | GA | Tutte le offerte di base | 5 maggio 2026 | Semplificazioni suggerite dall’intelligenza artificiale |
| Supporto per la funzione Decisioni nel canale e-mail | GA | Tutte le offerte di base | 6 aprile 2026 | Pagine mirror supportate |
| Monitoraggio dei modelli IA | GA | Tutte le offerte di base | 9 marzo 2026 | Solo modelli di ottimizzazione personalizzati |
| Supporto per la funzione Decisioni nel canale SMS | GA | Tutte le offerte di base | 2 febbraio 2026 | — |
| Supporto per la funzione Decisioni nel canale push | GA | Tutte le offerte di base | 30 gennaio 2026 | — |
| Frammenti di contenuto Adobe Experience Manager in Decisioning | LA | Tutte le offerte di base | 20 maggio 2026 | Contatta il tuo rappresentante Adobe |
| Offer Decisioning (criteri di decisione) | GA | Tutte le offerte di base | Funzionalità di base | Selezione della migliore offerta in tempo reale |
| Classificazione basata su AI | GA | Tutte le offerte di base | Funzionalità di base | Ottimizzazione delle offerte di apprendimento automatico |

>[!TAB Agenti AI]

| Funzione | Stato | Applicabile a | Disponibile da | Note |
|---------|--------|-----------|-----------------|-------|
| Journey Agent: creare un percorso | GA | Percorsi; Campagne e Percorsi | martedì 12 gennaio 2026 | Creazione di percorsi in linguaggio naturale |
| Integrazione dell’agente di intelligenza artificiale Journey Optimizer tramite MCP | Beta | Tutte le offerte di base | Aprile 2026 | Beta pubblico; Claude Web e desktop |
| Journey Agent: creazione di contenuti di canale | LA | Tutte le offerte di base | 4 marzo 2026 | Contatta il tuo rappresentante Adobe |

>[!TAB Amministrazione e dati]

| Funzione | Stato | Applicabile a | Disponibile da | Note |
|---------|--------|-----------|-----------------|-------|
| Autenticazione personalizzata basata su certificato nelle azioni personalizzate | GA | Tutte le offerte di base | 4 giugno 2026 | Per l’identità basata su certificato (ad esempio, Microsoft Entra ID) |
| Avvisi dei clienti per gli eventi del ciclo di vita della campagna | GA | Tutte le offerte di base | 1 giugno 2026 | Iscriviti a livello di sandbox |
| Crittografia dei parametri URL | GA | Tutte le offerte di base | 1 giugno 2026 | Precedentemente LA; necessita di autorizzazioni chiave del Registro di sistema |
| API per strumenti di migrazione self-service | GA | Tutte le offerte di base | 3 febbraio 2026 | — |
| Monitoraggio delle azioni personalizzate | GA | Tutte le offerte di base | 3 febbraio 2026 | Precedentemente LA |
| Esportazione dei messaggi | GA | Tutte le offerte di base | 28 gennaio 2026 | Disponibile come componente aggiuntivo |
| API di recupero di campagne con azioni | GA | Tutte le offerte di base | 24 novembre 2025 | — |
| Eseguire la migrazione dei sottodomini alla delega personalizzata | LA | Tutte le offerte di base | 19 febbraio 2026 | Contatta il tuo rappresentante Adobe |
| Sandbox | GA | Tutte le offerte di base | Funzionalità di base | Fino a 5 sandbox; disponibili ulteriori |
| Profili e pubblico unificati | GA | Tutte le offerte di base | Funzionalità di base | Basato su Adobe Experience Platform |
| Reporting e rapporti live | GA | Tutte le offerte di base | Funzionalità di base | — |
| Autorizzazioni e controllo degli accessi | GA | Tutte le offerte di base | Funzionalità di base | Accesso basato sul ruolo |
| API REST | GA | Tutte le offerte di base | Funzionalità di base | Framework API-first |

>[!ENDTABS]

>[!NOTE]
>
>Questo elenco è compilato in base alle [note sulla versione 2026](../rn/release-notes-2026.md) e alle [note sulla versione corrente](../rn/release-notes.md) e riflette lo stato noto più recente di ciascuna funzionalità. Non è esaustivo. Per la cronologia completa e le ultime aggiunte, controlla sempre le [note sulla versione](../rn/release-notes.md).

## Risorse correlate {#related}

- **Comprendere il contenuto del pacchetto** - [Pacchetti e funzionalità](ajo-packages.md)
- **Visualizza tutto ciò che è stato spedito** — [Note sulla versione](../rn/release-notes.md) | [Note sulla versione 2026](../rn/release-notes-2026.md)
- **Introduzione** — [Introduzione a Journey Optimizer](get-started.md)

---

Sono state aggiunte tre righe, una in ciascuna delle schede **Canali**, **Percorsi** e **Campagne**, seguendo lo stesso pattern di cross-tab utilizzato per l&#39;invio ondata. La funzionalità è contrassegnata **Beta / H2 2026** poiché il ticket è destinato alla seconda metà del 2026 e la funzionalità non è ancora GA. La scheda Canali contiene la descrizione autorevole; le righe Percorsi e Campagne sono brevi riferimenti incrociati che indicano ai lettori la scheda Canali per i dettagli.