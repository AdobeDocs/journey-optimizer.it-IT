---
solution: Journey Optimizer
product: journey optimizer
title: Ore non interattive
description: Scopri come evitare l’invio di comunicazioni in periodi specifici utilizzando le regole dell’orario non interattivo
feature: Campaigns
topic: Content Management
role: User
level: Intermediate
keywords: ore non interattive, esclusioni di tempo, regole aziendali, set di regole, pianificazione, campagne
exl-id: [TO BE GENERATED]
hide: yes
hidefromtoc: yes
source-git-commit: 11bccd63afa1bf5aafcd1dff70c8193ea754d256
workflow-type: tm+mt
source-wordcount: 980
ht-degree: 9%

---

# Ore non interattive {#quiet-hours}

>[!AVAILABILITY]
>
>Le ore di silenzio sono attualmente disponibili solo per un set di organizzazioni (disponibilità limitata). Per essere aggiunti alla lista d’attesa, contatta il tuo rappresentante Adobe.

Le ore di silenzio consentono di definire esclusioni basate sul tempo per i canali E-mail, SMS, Push e WhatsApp. Garantiscono che non vengano inviati messaggi in specifici periodi di tempo, aiutandoti a rispettare le preferenze dei clienti e i requisiti di conformità.

Puoi applicare ore di silenzio tramite set di regole, che possono essere assegnate a singole azioni in campagne o percorsi per un controllo preciso.

## Perché utilizzare le Ore non interattive {#why-quiet-hours}

Le ore di pausa consentono di migliorare la customer experience e mantenere la conformità in diversi modi:

* **Rispetta le preferenze del cliente**: evita di inviare messaggi in orari scomodi (ad esempio, tarda notte o prima mattina), che possono avere un impatto negativo sulla reputazione del marchio e sulla fedeltà dei clienti.

* **Migliora il coinvolgimento**: inviando messaggi quando i clienti hanno più probabilità di visualizzarli e agire di conseguenza, si aumenta l&#39;efficacia delle comunicazioni.

* **Conformità legale**: alcuni stati e aree geografiche vietano l&#39;invio di messaggi SMS di marketing in ore specifiche. Le ore di silenzio consentono di rispettare le normative, come il TCPA e le leggi SMS specifiche per ogni stato.

* **Ottimizza tempistica**: se è trascorso troppo tempo dalla pianificazione di un messaggio, potrebbe non essere più rilevante. Le ore di pausa consentono di eliminare i messaggi obsoleti o di mantenerli in sospeso fino a un momento appropriato.

## Come funzionano le ore di pausa {#how-quiet-hours-work}

Le ore non interattive vengono implementate tramite le regole aziendali che crei e applichi alle campagne e ai percorsi utilizzando i set di regole.

Quando è pianificato l&#39;invio di un messaggio durante un periodo di inattività, [!DNL Adobe Journey Optimizer] esegue una delle due azioni in base alla configurazione:

* **Ignora**: il messaggio viene eliminato definitivamente e non viene mai inviato.
* **Coda**: il messaggio viene trattenuto e inviato automaticamente al termine del periodo di inattività.

Il sistema valuta le ore non interattive in base al fuso orario del destinatario, che può essere:

* Il fuso orario specificato nel profilo del cliente
* Fuso orario dedotto basato su altri dati di profilo ed eventi
* Fuso orario fisso specificato nella regola

>[!NOTE]
>
>Finestra di pre-soppressione: il sistema inizia l&#39;eliminazione delle comunicazioni 30 minuti prima dell&#39;inizio delle ore di sospensione, in modo che non venga inviato alcun messaggio all&#39;inizio del periodo di sospensione.

## Creare una regola Ore non interattive {#create-quiet-hours-rule}

Per creare una regola relativa alle ore non interattive:

1. Passa a **[!UICONTROL Amministrazione]** > **[!UICONTROL Regole aziendali]**.

1. Nella sezione **[!UICONTROL Set di regole]**, crea un nuovo set di regole o selezionane uno esistente a cui aggiungere la regola relativa alle ore non interattive.

1. Fai clic su **[!UICONTROL Crea regola]** e seleziona **[!UICONTROL Ore non interattive]** come tipo di regola.

1. Configurare le impostazioni relative alle ore non interattive:

   * **Nome regola**: assegna alla regola un nome descrittivo.

   * **Periodo di tempo**: definire quando applicare le ore non interattive:
      * **Ore del giorno**: imposta ore specifiche (ad esempio, dalle 20:00 alle 08:03:00):00:00
      * **Giorni della settimana**: seleziona giorni specifici (ad esempio, fine settimana)
      * **Date personalizzate**: scegli date di calendario specifiche (ad esempio, festività)

   * **Fuso orario**: selezionare la modalità di determinazione del fuso orario:
      * **Fuso orario locale dell&#39;utente**: utilizza il fuso orario del profilo di ciascun destinatario
      * **Fuso orario specifico**: applica un fuso orario fisso (ad esempio, orientale, centrale)

   * **Azione**: scegli cosa succede ai messaggi nelle ore non interattive:
      * **Ignora**: i messaggi vengono eliminati definitivamente
      * **Coda**: i messaggi vengono conservati e inviati al termine delle ore non interattive

1. Fai clic su **[!UICONTROL Salva]** per creare la regola.

## Applicare ore di pausa a campagne e percorsi {#apply-quiet-hours}

Dopo aver creato una regola relativa alle ore non interattive, devi applicarla alle campagne o ai percorsi:

1. Apri la campagna o il percorso in cui desideri applicare le ore non interattive.

1. Passa all’azione (e-mail, SMS, push o WhatsApp) che desideri controllare.

1. Nella configurazione dell&#39;azione, individua la sezione **[!UICONTROL Set di regole]**.

1. Selezionare il set di regole contenente la regola relativa alle ore non interattive.

1. Salva le modifiche.

La regola relativa alle ore non interattive verrà ora applicata a tale azione specifica. Tutti i messaggi inviati tramite questa azione rispetteranno la configurazione delle ore non interattive.

>[!NOTE]
>
>Le regole relative alle ore non interattive si applicano sia alle comunicazioni pianificate che a quelle attivate da eventi. Assicurati che il set di regole sia configurato correttamente per gestire il caso d’uso.

## Considerazioni sul fuso orario {#timezone-considerations}

Quando si utilizza l&#39;opzione **Fuso orario locale dell&#39;utente**, [!DNL Adobe Journey Optimizer] cerca le informazioni sul fuso orario nell&#39;ordine seguente:

1. **Attributo fuso orario profilo**: il fuso orario specificato in modo esplicito nel profilo del cliente
2. **Fuso orario dedotto**: fuso orario calcolato in base ad altri dati di profilo e segnali comportamentali

Se nessuna delle due opzioni è disponibile, il sistema potrebbe non applicare correttamente le ore non interattive. Per risultati ottimali, assicurati che i profili dei clienti includano informazioni sul fuso orario.

Quando si utilizza un **fuso orario specifico**, tutti i destinatari ricevono (o non ricevono) messaggi in base a tale singolo fuso orario, indipendentemente dalla loro posizione effettiva.

## Guardrail e limitazioni {#guardrails-limitations}

Quando si utilizzano ore non interattive, tenere presente quanto segue:

* **Tempo di attivazione**: possono essere necessari fino a 20 minuti per attivare completamente una regola o un set di regole. Pianifica di conseguenza durante la creazione o la modifica delle regole.

* **Ritardo attivazione campagna**: dopo aver associato le regole business, attendi almeno 10 minuti prima di attivare un percorso o di inviare una campagna per verificare che le regole siano applicate correttamente.

* **Limiti set di regole**: al momento, è possibile avere fino a 3 set di regole attivi per il dominio del canale e 5 per il dominio del percorso.

* **Frequenza di rilascio dei messaggi**: quando vengono rilasciati messaggi in coda e di fine orario non intermittente, l&#39;invio avviene a una velocità massima di 5.000 messaggi al secondo per organizzazione.

* **Non supportato in**: le regole delle ore non interattive non sono attualmente disponibili per l&#39;orchestrazione delle campagne.

* **Esecuzione in prova**: le regole delle ore non interattive non vengono valutate durante le esecuzioni in prova del percorso.

## Reporting {#reporting}

Puoi tenere traccia dell’impatto delle ore non interattive su campagne e percorsi tramite le funzioni di reporting standard:

* **Rapporto di tutti i tempi**: la sezione &quot;Motivi di esclusione&quot; mostra il volume di clienti che non hanno ricevuto comunicazioni a causa di regole di orario non interattivo, insieme al nome specifico del set di regole.

* **Report live**: (se disponibile) mostra statistiche in tempo reale sui profili attualmente in attesa a causa di ore non interattive o scartati a causa di ore non interattive.

## Passaggi successivi {#next-steps}

Una volta configurate e applicate le regole dell’orario non interattivo, puoi:

* Esamina la campagna o il percorso per assicurarti che le regole siano correttamente associate
* Attivare la campagna o il percorso
* Monitorare l’impatto delle ore non interattive nei rapporti

