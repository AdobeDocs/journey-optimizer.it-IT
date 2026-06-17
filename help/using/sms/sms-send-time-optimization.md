---
solution: Journey Optimizer
product: journey optimizer
title: Ottimizzazione del tempo di invio per la messaggistica mobile
description: Scopri come configurare e utilizzare l’ottimizzazione dell’ora di invio per la messaggistica mobile in Adobe Journey Optimizer.
feature: SMS
topic: Send Time Optimization
role: User
level: Intermediate
exl-id: 56ff1000-7799-40ff-8f03-2f5868d05e7b
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: f03a3a13-9e99-4c7c-a1ae-0f4d07ced35c
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b6b77c26-2a48-4a62-9ceb-5ae67f4dfde5
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 84aa39bfd480e5bcaa8a58c5ec29f1990e5ddc6f
workflow-type: tm+mt
source-wordcount: 1181
ht-degree: 1%

---


# Ottimizzazione del tempo di invio per la messaggistica mobile {#sms-send-time-optimization}

>[!AVAILABILITY]
>
>L’ottimizzazione dell’ora di invio per la messaggistica mobile (SMS, RCS e WhatsApp) è disponibile a partire da H2 2026 e si applica sia ai Percorsi che alle campagne.

## Panoramica {#overview}

L’ottimizzazione dell’ora di invio (STO) per la messaggistica mobile consente agli addetti al marketing di andare oltre la pianificazione &quot;batch and blast&quot; (batch e blast) utilizzando informazioni basate sull’intelligenza artificiale per determinare il tempo di consegna ottimale per ogni singolo profilo. Invece di inviare messaggi a tutto il pubblico contemporaneamente, Adobe Journey Optimizer analizza i pattern di coinvolgimento storici di ciascun profilo e prevede quando è più probabile che tale individuo apra, faccia clic o risponda a un messaggio SMS, RCS o WhatsApp.

Consentendo di inviare messaggi nel momento in cui si prevede il coinvolgimento più elevato, STO contribuisce ad aumentare i tassi di apertura, i tassi di click-through e il ROI complessivo della campagna, senza richiedere la segmentazione manuale del pubblico in base al fuso orario o alla coorte comportamentale. STO per la messaggistica mobile è supportato tra i canali SMS, RCS e WhatsApp ed è disponibile sia nel contesto di Percorso che in quello di esecuzione di Campaign.

## Prerequisiti {#prerequisites}

Prima di abilitare l’ottimizzazione dell’ora di invio per la messaggistica mobile, verifica quanto segue:

- L’organizzazione dispone del provisioning per Adobe Journey Optimizer e per almeno uno dei canali SMS, RCS o WhatsApp.
- Per il pubblico target in Adobe Experience Platform (AEP) esiste un volume sufficiente di dati storici sul coinvolgimento mobile, tra cui eventi di invio, aperture, clic sui collegamenti e risposte. Il modello di intelligenza artificiale richiede una cronologia delle interazioni precedente per generare previsioni affidabili per profilo.
- La superficie di canale rilevante (SMS, RCS o WhatsApp) è configurata e attiva nell’istanza di AJO. Per istruzioni di installazione, consulta [Configurare le superfici di canale SMS](../sms/sms-configuration.md).
- Per i casi d’uso basati sul Percorso, il Percorso deve essere progettato in modo che il nodo dell’azione del messaggio non sia vincolato dai nodi di attesa o evento a monte i cui timeout sono in conflitto con la finestra di consegna STO.

>[!NOTE]
>
>I profili con dati di coinvolgimento cronologici insufficienti tornano a un tempo di invio predefinito definito durante la configurazione. Le previsioni STO vengono generate e valutate a livello dei singoli profili.

## Come funziona {#how-it-works}

STO per la messaggistica mobile si basa su un modello di intelligenza artificiale specifico che elabora i segnali di coinvolgimento storici di ciascun profilo per prevedere la finestra di consegna ottimale. I passaggi seguenti descrivono il flusso end-to-end.

### &#x200B;1. Acquisizione dei dati e formazione sui modelli

Il modello AI acquisisce in modo continuo gli eventi di coinvolgimento mobile memorizzati in Adobe Experience Platform, inclusi i timestamp di apertura dei messaggi, gli eventi di clic dei collegamenti, i tempi di risposta e i record di consegna storici. Questi segnali formano i dati di formazione utilizzati per apprendere modelli comportamentali per ciascun profilo, come le ore di interazione preferite, le tendenze giornaliere della settimana e la reattività tra fusi orari. Il modello viene riqualificato su base continua per rimanere sensibile ai cambiamenti nel comportamento di coinvolgimento.

### &#x200B;2. Punteggio di previsione per profilo

Una volta eseguito il training, il modello classifica ogni profilo del pubblico target e produce una finestra di tempo di invio ottimale. Questa previsione viene scritta nuovamente nel profilo in AEP come attributo calcolato, rendendolo disponibile sia per i Percorsi che per le campagne in fase di esecuzione senza richiedere chiamate API aggiuntive o ricerche in tempo reale durante l’invio dei messaggi.

### &#x200B;3. Pianificazione runtime percorso

Quando un Percorso contenente un nodo di azione SMS, RCS o WhatsApp abilitato dall’STO è attivo, il runtime del Percorso legge l’attributo del tempo di invio previsto di ciascun profilo qualificato mentre il profilo raggiunge il nodo di azione. Il messaggio viene mantenuto all’interno della finestra di ottimizzazione configurata e inviato quando arriva il tempo ottimale previsto. Se il tempo previsto è già trascorso o si trova all’esterno della finestra, viene applicato il comportamento di fallback configurato.

### &#x200B;4. Distribuzione invio campagna

Per le campagne, STO distribuisce l’invio tra il pubblico in base alle previsioni per profilo, anziché emettere un singolo invio in blocco. AJO sposta la consegna nella finestra di invio configurata della campagna, rispettando il tempo ottimale previsto di ciascun profilo e rimanendo all’interno dei limiti della finestra definiti.

>[!NOTE]
>
>Se il tempo ottimale previsto di un profilo non rientra nella finestra di invio configurata, il messaggio viene inviato al limite più vicino, all’inizio o alla fine della finestra, a seconda di quale dei due valori sia più vicino alla previsione.

## Configurare l’ottimizzazione dell’ora di invio {#configure}

### Abilitare l’opzione STO in una campagna {#configure-campaign}

1. In Journey Optimizer, passa a **Campagne** e crea una nuova campagna o apri una bozza esistente.
2. Seleziona **SMS**, **RCS** o **WhatsApp** come canale e completa i passaggi del contenuto di tipi di pubblico e messaggi.
3. Nella sezione **Pianificazione**, seleziona **Ottimizzazione dell&#39;ora di invio** invece di una data e un&#39;ora di invio fisse.
4. Utilizza l&#39;interruttore **Ottimizzazione ora di invio** per abilitare la funzione.
5. Configura la **finestra di invio**: imposta l&#39;ora di inizio e di fine entro le quali AJO può recapitare i messaggi. La finestra deve durare almeno un&#39;ora e può estendersi fino a 24 ore.
6. Definisci un **Tempo di invio fallback** per i profili che non hanno una cronologia di coinvolgimento sufficiente per generare una previsione. Puoi scegliere di inviare immediatamente all’apertura della finestra o a un orario fisso all’interno della finestra.
7. Completa i passaggi di quota limite, revisione e attivazione, quindi attiva la campagna.

### Attiva STO in un Percorso {#configure-journey}

1. Aprire o creare un Percorso nell&#39;area di lavoro del Percorso.
2. Aggiungi o seleziona un nodo azione **SMS**, **RCS** o **WhatsApp**.
3. Nel pannello di configurazione del nodo di azione, espandi le impostazioni di **Ora di invio**.
4. Attiva **Ottimizzazione ora di invio** per attivare lo stato.
5. Imposta la **finestra di ottimizzazione**: la durata massima (in ore) del messaggio che il runtime può contenere in attesa del tempo di consegna ottimale previsto. La finestra predefinita è di sei ore; il massimo è di 24 ore.
6. Configurare il **comportamento di fallback**, che può essere inviato immediatamente quando un profilo entra nel nodo oppure attendere la successiva finestra prevista disponibile, per i profili che non dispongono di dati di previsione.
7. Salva la configurazione del nodo e pubblica il Percorso.

>[!NOTE]
>
>Quando STO è attivo su un nodo di azione del Percorso, il tempo di consegna effettivo di un profilo può differire dal momento in cui il profilo entra nel nodo fino alla lunghezza completa della finestra di ottimizzazione configurata. Tenere conto di questo ritardo durante la progettazione di nodi di attesa a monte e l&#39;impostazione di timeout a livello di Percorso per evitare uscite di percorso premature.

## Guardrail e limitazioni {#guardrails}

- STO si applica solo ai messaggi SMS, RCS e WhatsApp in uscita. I flussi di risposta in entrata e le sessioni di messaggistica bidirezionale non sono soggetti alla pianificazione dell’STO.
- Ogni nodo di azione di Campaign o Percorso supporta una superficie di canale per ogni messaggio abilitato all’STO. La coordinazione STO tra canali diversi (ad esempio, SMS e WhatsApp all’interno di un singolo nodo) non è supportata.
- Per produrre una previsione, il modello di intelligenza artificiale richiede almeno 30 giorni di dati storici sul coinvolgimento mobile per profilo. I profili al di sotto di questa soglia utilizzano il tempo di invio di fallback configurato.
- STO interagisce con le regole di quota limite. Se la finestra di consegna prevista di un profilo con limite è in conflitto con un limite di limite, il messaggio viene soppresso in base alla regola di limite e non viene riprogrammato in una finestra successiva.
- I flag di consenso, i record di rinuncia e gli elenchi di soppressione globali vengono sempre applicati indipendentemente dalla pianificazione dell’STO. Un messaggio conservato per la consegna ottimizzata è ancora soggetto a controlli del consenso al momento della spedizione.
- STO non è disponibile per i messaggi transazionali in cui la consegna immediata è richiesta da requisiti aziendali o normativi.

## Argomenti correlati {#related-topics}

- [Guida introduttiva a SMS, RCS e WhatsApp in Journey Optimizer](../sms/create-sms.md)
- [Configurare le superfici di canale SMS](../sms/sms-configuration.md)
- [Ottimizzazione dell’ora di invio per le notifiche e-mail e push](../building-journeys/send-time-optimization.md)
- [Classificazione basata sull’intelligenza artificiale in Journey Optimizer](../offers/offer-activities/ai-ranking.md)
- [Note sulla versione di Journey Optimizer](../rn/release-notes.md)
