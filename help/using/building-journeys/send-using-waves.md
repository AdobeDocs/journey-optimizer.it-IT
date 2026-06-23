---
solution: Journey Optimizer
product: journey optimizer
title: Inviare utilizzando gli scaglioni nei percorsi
description: Pianifica messaggi di percorso in uscita da consegnare in batch controllati (scaglioni) nel tempo. L’invio ondata in percorsi di pubblico lettura consente di bilanciare il carico e supportare il recapito messaggi.
feature: Journeys, Activities, Audiences
topic: Content Management
role: User
level: Intermediate
mini-toc-levels: 1
keywords: ondate, batch, pianificazione, percorso, pubblico di lettura, recapito messaggi
exl-id: 1aaff17f-aa08-4f10-903c-8335a86ac6eb
feature_v2: []
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1554
ht-degree: 1%

---

# Inviare utilizzando gli scaglioni nei percorsi {#send-using-waves-journeys}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri come inviare messaggi in uscita da un percorso di pubblico di lettura in batch pianificati, denominati ondate, per bilanciare il carico, proteggere i sistemi a valle e supportare il recapito messaggi.

>[!ENDSHADEBOX]

È possibile recapitare i messaggi in uscita da un percorso in batch (ondate) nel tempo anziché tutti contemporaneamente. L’invio ondata consente di bilanciare il carico, evitare l’eccessiva sovraccarico dei sistemi a valle (come i call center o le pagine di destinazione) e supportare il recapito dei messaggi e la reputazione del mittente, in particolare per i percorsi di pubblico con elevato volume di letture.

<!--
>[!CAUTION]
>
>Wave sending is available for read audience journeys only and applies to **outbound** actions only (Email, SMS, Push, Direct mail).
-->

Puoi configurarlo a livello di percorso quando definisci il modo in cui il pubblico entra e come vengono pianificate le azioni. Puoi definire il numero di scaglioni, la loro dimensione (come percentuale del pubblico o come numeri assoluti) e quando viene eseguito ogni scaglione.

## Limitazioni e protezioni {#limitations-guardrails}

* L&#39;invio ondata è disponibile solo per percorsi di pubblico di lettura con i tipi di pianificazione **[!DNL As soon as possible]** e **[!UICONTROL Once]**. Ulteriori informazioni sulla [pianificazione dei percorsi](read-audience.md#schedule).
* L’invio ondata non è disponibile per percorsi ricorrenti, attivati da eventi, eventi di business, modalità di test o a esecuzione inattiva.
* È necessario definire almeno **2 scaglioni** e aggiungere fino a **10 scaglioni**.
* L&#39;intervallo minimo tra l&#39;inizio di due scaglioni è **30 minuti**.
* L&#39;inizio di un&#39;ondata non può precedere l&#39;inizio del percorso o essere nel passato.
* La suddivisione del pubblico in ondate può richiedere fino a 1 ora. I profili non possono entrare nel percorso fino a quel momento.
* All&#39;interno di una singola versione del percorso, due scaglioni non vengono mai eseguiti contemporaneamente. L&#39;ondata successiva inizia solo dopo la fine dell&#39;ondata precedente. Ad esempio, se le ondate sono programmate a 1 ora di distanza ma la prima ondata è in esecuzione per 2 ore, la seconda ondata inizia quando termina la prima ondata, non all&#39;ora programmata.
* L’avvio delle onde può essere ritardato quando la piattaforma applica limiti di quota o quando la capacità del sistema è soggetta a un carico elevato.

## Configurare l’invio ondata in un percorso {#configure-wave-sending}

1. Inizia il percorso con un&#39;attività [Read Audience](read-audience.md).

1. Fai doppio clic sull&#39;attività **[!UICONTROL Read Audience]** per aprirne le proprietà e seleziona l&#39;opzione **[!UICONTROL Consegna percorso a ondate]**.

   ![](assets/journey-wave-option.png){width="100%"}

1. Imposta il **numero di scaglioni** (ad esempio, 4).

   ![](assets/journey-wave-number.png){width="80%"}

   >[!NOTE]
   >
   >È necessario definire almeno 2 scaglioni e aggiungere fino a 10 scaglioni.

1. Scegliete come definire la dimensione e la tempistica dell&#39;onda come descritto di seguito.

### Onde uguali {#equal-waves}

Per impostazione predefinita, il pubblico è suddiviso in ondate di uguali dimensioni. Imposta un intervallo fisso tra l’inizio di ogni ondata (ad esempio, 2 ore).

![](assets/journey-equal-waves.png){width="70%"}

>[!NOTE]
>
>L&#39;intervallo minimo tra l&#39;inizio di due scaglioni è **30 minuti**.

Il sistema pianifica quindi automaticamente le ondate successive (ad esempio, la prima ondata alle ore 9:00, la seconda alle ore 11:00, la terza alle ore 1:00, la quarta alle ore 15:00).

### Distribuzione personalizzata {#custom-distribution}

Seleziona l&#39;opzione **[!UICONTROL Distribuzione personalizzata]** per definire la dimensione di ogni ondata come percentuale del pubblico totale (ad esempio, 15%, 20%, 25%, 40%).

![](assets/journey-wave-percentage.png){width="70%"}

Seleziona **[!UICONTROL Numeri]** per definire la dimensione di ogni ondata come numero assoluto di profili (ad esempio, 10.000; 50.000).

![](assets/journey-wave-numbers.png){width="70%"}

>[!NOTE]
>* Quando si utilizzano le percentuali, il totale di tutte le ondate deve essere 100%. In caso contrario, viene visualizzato un avviso.
>* Quando si utilizzano i numeri, il sistema non convalida la copertura e assicura che le dimensioni dell&#39;onda coprano il pubblico previsto. [Ulteriori informazioni](#faq)

### Pianificazione personalizzata {#custom-schedule}

Seleziona **[!UICONTROL Pianifica ogni scaglione]** per definire una data e un&#39;ora di inizio specifiche per ogni scaglione. Non è necessario che le onde siano equidistanti (ad esempio, 9:00 AM, 11:00 AM, 5:00 PM, 8:30 PM).

![](assets/journey-wave-custom-schedule.png){width="70%"}

>[!NOTE]
>
>L&#39;intervallo minimo tra l&#39;inizio di due scaglioni è **30 minuti**.

## Casi d’uso {#use-cases}

L’invio ondata consente di controllare quando e quanti messaggi vengono inviati, migliorando il recapito messaggi, proteggendo la reputazione del mittente e allineando gli invii con la capacità operativa. Considera l’utilizzo delle onde in questi scenari:

* **Gestione call center o risposta:** limitare il numero di messaggi inviati al giorno o all&#39;ora in modo che i team a valle (ad esempio, l&#39;assistenza clienti) possano gestire le risposte. Ad esempio, invia 20 messaggi al giorno per far corrispondere la capacità del call center.

  ![](assets/journey-waves-ex-call-center.png){width="55%"}

* **Volume elevato e recapito messaggi:** Evita di inviare un percorso molto grande in un&#39;unica ripresa. Distribuisci la consegna nel tempo per contribuire a mantenere la reputazione del mittente e ridurre il rischio di essere segnalato come spam.

  ![](assets/journey-waves-ex-high-volume.png){width="55%"}

* **Incremento:** Quando si utilizza una nuova piattaforma o un nuovo indirizzo IP, aumentare progressivamente il volume (ad esempio, 10% nella prima ondata, quindi 15%, 20% e così via) per creare la reputazione gradualmente.

  ![](assets/journey-waves-ex-ramp-up.png){width="55%"}

## Domande frequenti {#faq}

+++ Cosa succede se la somma delle dimensioni delle onde non è uguale al pubblico totale?

* Se la somma delle dimensioni dell&#39;ondata **supera** il pubblico (ad esempio, pianifichi 100.000 nella prima ondata per un pubblico di 100.000), la prima ondata verrà inviata al pubblico completo e le ondate rimanenti non avranno più nessuno a cui inviare, non verranno eseguite.
* Se la somma **è inferiore** rispetto al pubblico (ad esempio, si definiscono quattro ondate per un totale di 40.000 profili per un pubblico di 100.000), solo i profili inclusi in tali ondate riceveranno il messaggio. Il resto del pubblico non riceverà la comunicazione e non verrà ritentato nelle ondate successive.

+++

+++ Posso assegnare segmenti o criteri diversi a singole ondate?

È possibile definire solo la dimensione e la tempistica delle onde. Lo stesso pubblico attraversa il percorso; non è possibile assegnare segmenti o criteri diversi a singole ondate.

+++

## Vedi anche {#see-also}

* [Utilizza un pubblico in un percorso](read-audience.md): configura l&#39;attività Read audience.

+++ Guida di riferimento della Knowledge Base di AI

Questa sezione contiene informazioni strutturate che supportano l&#39;interpretazione, il recupero e la risposta alle domande relative a questo argomento.

Per una comprensione completa, queste informazioni devono essere unite alla documentazione su questa pagina. Nessuna delle due origini è progettata per essere indipendente; la pagina descrive la funzione, mentre questa sezione fornisce un contesto aggiuntivo che aiuta a non ambiguare la terminologia, le finalità, l’applicabilità e i vincoli.

* **TL;DR:** In questa pagina viene illustrato come configurare l&#39;invio di messaggi wave in percorsi di lettura pubblico di Adobe Journey Optimizer per inviare messaggi in uscita in batch controllati nel tempo, migliorando il recapito messaggi e proteggendo la reputazione del mittente.

**Intenti:**
* Abilitare l’invio ondata in un percorso Read Audience per inviare messaggi in batch
* Configurare le onde uguali con un intervallo fisso tra ogni ondata
* Definire le dimensioni delle ondate personalizzate come percentuali o conteggi assoluti dei profili
* Pianifica ogni scaglione con una data e un’ora di inizio specifiche utilizzando una pianificazione personalizzata
* Controllare il volume di consegna per proteggere la reputazione del mittente o allinearlo alla capacità operativa

**Glossario:**
* **Invio ondata**: modalità di consegna che divide il pubblico di lettura in batch (ondate) e invia messaggi a ogni batch a intervalli pianificati anziché a tutti contemporaneamente *(specifico per prodotto)*
* **Onde uguali**: configurazione ondata in cui il pubblico viene suddiviso in porzioni di uguali dimensioni con intervallo fisso tra le ondate che iniziano *(specifico per prodotto)*
* **Distribuzione personalizzata**: configurazione ondata in cui la dimensione di ogni ondata viene definita manualmente come percentuale o numero assoluto di profili *(specifici del prodotto)*
* **Pianificazione personalizzata**: configurazione ondata in cui ogni ondata ha una data e un&#39;ora di inizio specifiche, che consentono una spaziatura non uniforme *(specifica del prodotto)*

**Guardrail:**
* L’invio ondata è disponibile solo per i percorsi Read Audience con i tipi di pianificazione &quot;As soon as possible&quot; (Appena possibile) e &quot;Once&quot; (Una volta); non è disponibile per i percorsi ricorrenti, attivati da eventi, eventi di business, modalità di test o a esecuzione inattiva.
* È necessario definire un minimo di due scaglioni e un massimo di dieci scaglioni.
* L&#39;intervallo minimo tra l&#39;inizio di due scaglioni consecutivi è di 30 minuti.
* L&#39;ora di inizio di un&#39;ondata non può precedere l&#39;inizio del percorso o essere nel passato.
* La suddivisione del pubblico in ondate può richiedere fino a 1 ora; i profili non possono entrare fino ad allora.
* All&#39;interno di una singola versione del percorso, due scaglioni non vengono mai eseguiti contemporaneamente; l&#39;onda successiva inizia solo dopo il termine di quella precedente.
* L&#39;avvio delle onde può essere ritardato dai limiti di quota della piattaforma o dal carico pesante del sistema.
* Quando si utilizza la distribuzione personalizzata basata su percentuale, il totale di tutte le scaglioni deve essere pari al 100%.
* Quando si utilizza la distribuzione personalizzata basata sul numero, il sistema non convalida la copertura totale; l’utente deve assicurarsi che le dimensioni delle onde coprano il pubblico previsto.
* Se le dimensioni delle onde superano il pubblico, la prima ondata viene inviata al pubblico completo e le onde rimanenti non vengono eseguite.
* Se il totale delle dimensioni delle ondate è inferiore al pubblico, solo i profili nelle ondate definite ricevono il messaggio; gli altri non vengono ritentati.

**Terminologia:**
* Nome canonico: Invio ondata — Acronimo: none — varianti: consegna in batch, consegna basata su ondata, invio graduale
* Sinonimi: &quot;ondate&quot; = &quot;batch&quot; = &quot;fasi di consegna&quot;
* Non confondere: &quot;Invio ondata&quot; ≠ &quot;percorso ricorrente&quot; (l’invio ondata divide un singolo pubblico letto in batch temporizzati; i percorsi ricorrenti rileggono il pubblico secondo una pianificazione)

**Domande frequenti:**
* **Q: l&#39;invio ondata può essere utilizzato in percorsi ricorrenti?** — No; l&#39;invio wave è disponibile solo per percorsi Read Audience con il tipo di pianificazione &quot;As soon as possible&quot; (Appena possibile) o &quot;Once&quot; (Una volta).
* **Q: qual è il tempo minimo tra due scaglioni?** — 30 minuti tra l&#39;inizio di due ondate consecutive.
* **D: cosa succede se le mie dimensioni d&#39;onda totali superano il pubblico?** — La prima ondata invia al pubblico completo e le ondate successive non hanno più profili da inviare a; non vengono eseguite.
* **D: posso assegnare contenuti o segmenti diversi a singole ondate?** — No; tutte le scaglioni utilizzano lo stesso pubblico e lo stesso contenuto di percorso. È possibile personalizzare solo la dimensione e la tempistica per ondata.
* **Q: quante scaglioni posso configurare?** — Tra 2 e 10 onde al percorso.
* **Q: quando dovrei usare l&#39;invio ondata?** protezione della reputazione del mittente per invii di volumi elevati, allineamento della consegna con la capacità del team a valle (ad esempio, call center) o aumento progressivo del volume su un nuovo IP o piattaforma.

+++
