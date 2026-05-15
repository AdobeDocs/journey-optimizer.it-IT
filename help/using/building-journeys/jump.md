---
solution: Journey Optimizer
product: journey optimizer
title: Passaggio da un percorso a un altro
description: Passaggio da un percorso a un altro
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: salto, attività, percorso, divisione, divisione
exl-id: 46d8950b-8b02-4160-89b4-1c492533c0e2
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/qCnWzqjO5YRbKO-WHUo950uoHS0skcZT6sdYyNJ4esE
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: d8353d85-5da7-453d-bd68-40ad33fa0ab7
  - id: fa683eda-48de-4558-af32-2673edcd44fe
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 1405
ht-degree: 6%

---

# Passaggio da un percorso a un altro {#jump}

>[!CONTEXTUALHELP]
>id="ajo_journey_jump"
>title="Attività Salta"
>abstract="L’azione Passa a consente di far passare singoli utenti da un percorso all’altro. Questa funzione semplifica la progettazione di percorsi molto complessi e consente di creare percorsi basati su modelli di percorso comuni e riutilizzabili."

L&#39;attività azione **[!UICONTROL Salta]** consente di inviare singoli utenti da un percorso all&#39;altro. Questa funzione consente di:

* semplificare la progettazione di percorsi molto complessi suddividendoli in diversi percorsi più semplici;
* creare percorsi basati su pattern di percorso comuni e riutilizzabili.

Nel percorso di origine, aggiungi un&#39;attività **[!UICONTROL Salta]** e seleziona un percorso di destinazione. Quando l&#39;utente accede al passaggio **[!UICONTROL Jump]**, viene inviato un evento interno al primo evento del percorso di destinazione. Se l&#39;azione **[!UICONTROL Salta]** ha esito positivo, l&#39;utente continua ad avanzare nel percorso. Il comportamento è simile ad altre azioni.

Nel percorso di destinazione, il primo evento attivato internamente dall&#39;attività **[!UICONTROL Jump]** crea il flusso individuale nel percorso.

## Ciclo di vita {#jump-lifecycle}

Si supponga di aver aggiunto un&#39;attività **[!UICONTROL Salta]** nel percorso A al percorso B. Il Percorso A è il **percorso di origine** e il percorso B è il **percorso di destinazione**.

Di seguito sono riportati i diversi passaggi del processo di esecuzione:

**Il Percorso A** è attivato da un evento esterno:

1. Il percorso A riceve un evento esterno correlato a un individuo.
1. Il singolo utente raggiunge il passaggio **[!UICONTROL Salta]**.
1. L&#39;utente viene inviato al percorso B e passa ai passaggi successivi nel percorso A, dopo il passaggio **[!UICONTROL Salta]**.

Nel percorso B, il primo evento viene attivato internamente tramite l&#39;attività **[!UICONTROL Jump]** dal percorso A:

1. Il percorso B riceve un evento interno dal percorso A.
1. L&#39;individuo inizia a fluire nel percorso B.

>[!NOTE]
>
>Il percorso B può essere attivato anche tramite un evento esterno.

### Comportamento del profilo durante un salto {#jump-profile-behavior}

Quando un profilo raggiunge il passaggio **[!UICONTROL Salta]**, continua a progredire nel percorso di origine (Percorso A) mentre entra simultaneamente nel percorso di destinazione (Percorso B). Il profilo è quindi attivo in entrambi i percorsi contemporaneamente.

Ciò significa che:

* Il profilo completa tutti i passaggi rimanenti nel Percorso A dopo l’attività Salta (ad esempio, un’azione di attesa di follow-up o di chiusura).
* Il profilo inizia anche a scorrere attraverso il Percorso B dal suo primo evento, indipendentemente dal Percorso A.
* Se il profilo è **già attivo** nel Percorso B al momento dell&#39;esecuzione del salto, **non** immetterà nuovamente il Percorso B. Il percorso A continua normalmente; non viene segnalato alcun errore.

>[!NOTE]
>
>Il caso precedente, profilo già attivo nel Percorso B, genera un **salto invisibile all&#39;utente**: non viene generato alcun errore e il Percorso A continua normalmente. In altre situazioni, il Salto può **non riuscire** e il Percorso A applica la gestione standard degli errori di azione. Per l&#39;elenco completo dei casi, vedere [Errori di runtime](#jump-troubleshoot).

## Best practice e limitazioni {#jump-limitations}

Utilizza queste linee guida per mantenere il comportamento dell’attività Salta prevedibile e sicuro.

### Authoring {#jump-limitations-authoring}

* L&#39;attività **[!UICONTROL Jump]** è disponibile solo nei percorsi che utilizzano uno spazio dei nomi.
* È possibile passare solo a un percorso che utilizza lo stesso spazio dei nomi del percorso di origine.
* Non puoi passare a un percorso che inizia con un evento **Qualificazione del pubblico** o **Read Audience**.
* Non puoi avere un&#39;attività **[!UICONTROL Jump]** e un evento **Qualificazione del pubblico** o **Read Audience** nello stesso percorso.
* Puoi includere in un percorso tutte le **[!UICONTROL attività Salta]** necessarie. Dopo un **[!UICONTROL Salto]**, puoi aggiungere qualsiasi attività necessaria.
* Puoi avere tutti i livelli di salto necessari. Il percorso A, ad esempio, passa al percorso B, che passa al percorso C e così via.
* Il percorso di destinazione può inoltre includere tutte le **[!UICONTROL attività Salta]** necessarie.
* I pattern di loop non sono supportati. Non esiste un modo per collegare due o più percorsi, il che creerebbe un loop infinito. La schermata di configurazione dell&#39;attività **[!UICONTROL Jump]** non consente di eseguire questa operazione.

### Execution {#jump-limitations-exec}

* Quando l&#39;attività **[!UICONTROL Jump]** viene eseguita, viene attivata la versione più recente del percorso di destinazione.
* Un individuo univoco può essere presente solo una volta nello stesso percorso. Di conseguenza, se l’individuo inviato dal percorso di origine è già nel percorso target, non entrerà in tale percorso. Non verrà segnalato alcun errore nell&#39;attività **[!UICONTROL Jump]** perché si tratta di un comportamento normale.

## Strategia di progettazione: percorsi di dimensioni ridotte {#jump-strategy}

Percorsi di clienti complessi possono diventare rapidamente difficili da creare e mantenere, soprattutto con l’introduzione di canali o punti di contatto aggiuntivi. Anche un percorso con una manciata di milestone può esporre 20 o più percorsi univoci che un cliente può seguire, e tale complessità cresce in modo esponenziale con ogni aggiunta.

Un approccio pratico alla gestione di questo problema consiste nel suddividere percorsi di grandi dimensioni in percorsi secondari più piccoli e mirati, uno per ogni fase aziendale o attività cardine, e collegarli utilizzando l&#39;attività **[!UICONTROL Salta]**. In questo modo ogni percorso è leggibile, testabile e manutenibile in modo indipendente.

**Passaggio 1: visualizzare il percorso end-to-end**

Mappatura dell&#39;intero percorso di clienti e identificazione delle sue fasi di alto livello. Ad esempio, un percorso di onboarding del programma fedeltà potrebbe includere tre fasi distinte: scaricare l’app mobile, effettuare una prima transazione, effettuare una seconda transazione.

**Passaggio 2: annota le fasi e definisci i percorsi secondari**

Contrassegna il limite di ogni fase e definisci il relativo obiettivo aziendale. Ogni fase diventa un percorso secondario candidato con una chiara condizione di ingresso e un obiettivo.

**Passaggio 3: generare e connettere percorsi secondari**

Crea ogni fase come percorso separato in Journey Optimizer, quindi utilizza le attività **[!UICONTROL Jump]** per passare i profili da un percorso secondario all&#39;altro. Il risultato è una serie di percorsi più semplici e riutilizzabili che si combinano per produrre un&#39;esperienza end-to-end completa, riducendo i rischi di introdurre errori.

>[!TIP]
>
>Per un esempio di utilizzo di un programma di fidelizzazione multifase, vedere [percorso di fidelizzazione multifase](journeys-uc.md#multi-phase-loyalty).

## Configurazione dell’attività Salta {#jump-configure}

1. Progetta il tuo **percorso di origine**.

   ![Attività Salta nella palette percorsi per la transizione tra percorsi](assets/jump1.png)

1. In qualsiasi passaggio del percorso, aggiungi un&#39;attività **[!UICONTROL Jump]** dalla categoria **[!UICONTROL ACTIONS]**. Aggiungi un’etichetta e una descrizione.

   ![Menu a discesa per la selezione del percorso di destinazione nella configurazione delle attività di salto](assets/jump2.png)

1. Fai clic nel campo **percorso di destinazione**.
L’elenco mostra tutte le versioni del percorso che sono bozza, live o in modalità di test. I percorsi che utilizzano uno spazio dei nomi diverso o che iniziano con un evento **Qualificazione del pubblico** non sono disponibili. Anche i percorsi target che creerebbero un pattern di loop vengono filtrati.

   ![Attività Salta che mostra il percorso di destinazione e i parametri delle azioni](assets/jump3.png)

   >[!NOTE]
   >
   >Puoi fare clic sull&#39;icona **Apri percorso di destinazione**, a destra, per aprire il percorso di destinazione in una nuova scheda.

1. Selezionare il percorso di destinazione in cui si desidera passare.
Il campo **Primo evento** è precompilato con il nome del primo evento del percorso di destinazione. Se il percorso di destinazione include più eventi, il **[!UICONTROL Salto]** è consentito solo sul primo evento.

   ![Configurazione mappatura parametri per attività di salto con editor espressioni](assets/jump4.png)

1. La sezione **Parametri azione** visualizza tutti i campi dell&#39;evento di destinazione. Mappa ogni campo con i campi dell’evento di origine o dell’origine dati, come con altri tipi di azioni. Queste informazioni verranno passate al percorso target in fase di runtime.
1. Aggiungi le attività successive per completare il percorso di origine.

   ![Interfaccia della modalità di test per testare l&#39;attività di salto tra percorsi](assets/jump5.png)


   >[!NOTE]
   >
   >L’identità dell’individuo viene mappata automaticamente. Queste informazioni non sono visibili nell’interfaccia.

L&#39;attività **[!UICONTROL Jump]** è configurata. Non appena il percorso è attivo o in modalità di test, gli utenti che raggiungono il passaggio **[!UICONTROL Salta]** verranno inviati al percorso di destinazione.

Quando un&#39;attività **[!UICONTROL Jump]** è configurata in un percorso, viene aggiunta automaticamente un&#39;icona di voce **[!UICONTROL Jump]** all&#39;inizio del percorso di destinazione. Questo consente di identificare che il percorso può essere attivato esternamente ma anche internamente da un&#39;attività **[!UICONTROL Jump]**.

![Flusso Percorso che mostra il salto dal percorso di origine al percorso di destinazione](assets/jump7.png)

## Risoluzione dei problemi {#jump-troubleshoot}

### Errori di configurazione

I seguenti problemi impediscono il corretto funzionamento del Salto e vengono visualizzati come errori nell’area di lavoro del percorso:

* Il percorso di destinazione non esiste più.
* Il percorso di destinazione è bozza, chiuso o interrotto.
* Il primo evento del percorso target è stato modificato e la mappatura è interrotta.

![Analisi dei Percorsi che mostra le metriche di esecuzione delle attività di salto](assets/jump6.png)

### Errori di runtime

Nei casi seguenti, il passaggio di salto viene trattato come **azione non riuscita** nel Percorso A. Il Percorso A applica la gestione standard degli errori di azione e continua:

* L&#39;istanza del percorso di destinazione esistente è stata terminata e il percorso di destinazione non è un nuovo partecipante.
* Nel percorso di destinazione è configurato un periodo di rientro. Anche se il reinserimento è consentito in linea di principio, il profilo non può rientrare finché non è trascorso il periodo (il salto non riesce con lo stato &quot;non rientro per il periodo&quot;).
* La versione del percorso di destinazione non può essere individuata, è stata eliminata, è terminata o è stata interrotta.
