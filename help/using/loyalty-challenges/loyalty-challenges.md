---
solution: Journey Optimizer
product: journey optimizer
title: Sfide di fedeltà
description: Scopri come creare e gestire le sfide di fidelizzazione in Adobe Journey Optimizer per creare programmi di fidelizzazione coinvolgenti.
feature: Loyalty challenges
topic: Journeys
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta privata" type="Informative"
version: Journey Orchestration
source-git-commit: b68c2610cbaaa8dbd86deb677562185e08d517ea
workflow-type: tm+mt
source-wordcount: '5146'
ht-degree: 1%

---


# Sfide di fedeltà {#loyalty-challenges}

>[!AVAILABILITY]
>
>Questa funzionalità è attualmente in **versione beta privata** e potrebbe non essere disponibile nel tuo ambiente. Per ottenere l’accesso, contatta il tuo rappresentante Adobe.

Sfide di fidelizzazione consente di creare offerte di coinvolgimento personalizzate per i clienti, aiutandoti a orchestrare programmi fedeltà su larga scala. Puoi progettare le sfide con attività e obiettivi specifici, premiare i clienti per averli completati e fornire l’esperienza tramite i canali Adobe Journey Optimizer.

>[!BEGINSHADEBOX]
>
>**In questa guida:**
>
>* [Panoramica](#overview) - Comprendere le sfide della fedeltà
>* [Funzionamento](#how-it-works) - Flusso di lavoro dettagliato dalla configurazione al monitoraggio
>* [Prerequisiti](#prerequisites) - Configurare l&#39;acquisizione dei dati e le autorizzazioni
>* [Accedi alle sfide di fidelizzazione](#access) - Apri il menu e visualizza le sfide
>* [Crea sfide](#create-challenges) - Crea nuove sfide fedeltà
>* [Crea attività](#create-tasks) - Definisci cosa devono fare i clienti
>* [Gestire le sfide](#manage-challenges) - Modificare, monitorare e ottimizzare
>
>[!ENDSHADEBOX]

## Panoramica {#overview}

Sfide di fidelizzazione consente di progettare e distribuire offerte di coinvolgimento personalizzate che motivano i clienti a completare azioni specifiche e a ricevere premi. Questa funzione fornisce una soluzione completa per la creazione di programmi fedeltà su larga scala, dalla definizione di attività e attività cardine alla distribuzione di contenuti e al tracciamento delle prestazioni su tutti i canali. Puoi creare tre tipi di esperienze di sfida, configurare premi, inviare notifiche multicanale nelle fasi principali del ciclo di vita e monitorare le prestazioni tramite percorsi generati automaticamente, mantenendo al contempo l’integrazione con il sistema di gestione della fedeltà esterno.

## Come funziona {#how-it-works}

La creazione e il lancio di una sfida di fidelizzazione segue questo flusso di lavoro:

1. **Configura l&#39;acquisizione dei dati**. Configura i connettori di origine di Experience Platform (come Capillary) per acquisire i dati dell&#39;evento fedeltà che tengono traccia delle azioni dei clienti e dell&#39;avanzamento.

2. **Crea una sfida** - Definisci le proprietà della sfida di base, tra cui nome, tipo (Standard, Streak o Sequenziale), pubblico e intervallo di date.

3. **Aggiungi attività** - Definisci le azioni specifiche che i clienti devono completare, inclusi i tipi di attività (acquisto, spesa, visita, ecc.), le quantità, i filtri dei prodotti e i premi.

4. **Progetta schede di contenuto** - Crea la rappresentazione visiva della tua sfida utilizzando le schede di contenuto Journey Optimizer visualizzate sui dispositivi dei clienti.

5. **Configurazione della messaggistica** (facoltativo): configurazione di messaggi multicanale (in-app, e-mail, push) per le fasi chiave: avvio, in corso e completamento.

6. **Rivedi e pubblica** - Verifica la tua sfida con i profili di test, quindi pubblicala per renderla disponibile al pubblico di destinazione.

7. **percorso generato automaticamente** - Quando si pubblica, Journey Optimizer crea automaticamente un percorso che orchestra la consegna e la messaggistica delle schede di contenuto.

8. **Attiva percorso** - Il percorso generato automaticamente si attiva alla data di inizio della sfida e gestisce tutte le interazioni dei clienti.

9. **Monitora le prestazioni** - Tieni traccia della partecipazione, dei tassi di completamento, della distribuzione dei premi e del coinvolgimento nei messaggi tramite rapporti incorporati e l&#39;area di lavoro del percorso.

>[!NOTE]
>
>Il percorso generato automaticamente viene visualizzato nell&#39;inventario del percorso e, se necessario, può essere personalizzato. Tuttavia, le modifiche apportate direttamente al percorso non vengono sincronizzate con la configurazione di verifica.

## Funzionalità principali

Utilizzare le sfide di fidelizzazione per:

* **Creare tre tipi di problemi**:
   * **Standard**: i clienti completano un numero qualsiasi di attività per ottenere premi.
   * **Streak**: i clienti completano la stessa attività più volte.
   * **Sequenziale**: i clienti completano le attività in un ordine specifico.

* **Progetta contenuto sfida**: utilizza le schede di contenuto Journey Optimizer per creare la rappresentazione visiva della sfida sui dispositivi dei clienti. Le schede dei contenuti mostrano le informazioni sulla sfida, l’avanzamento e i premi sul dispositivo del cliente.

* **Imposta requisiti attività**: definisci cosa devono fare i clienti per ottenere premi, tra cui:
   * Tipi di attività (acquisto, importo spesa, visita, ecc.)
   * Quantità richiesta
   * Inclusioni/esclusioni di prodotti tramite SKU
   * Attributi e condizioni personalizzati

* **Configura premi**: definisci i premi che i clienti ottengono al completamento dell&#39;attività o dopo aver completato l&#39;intera sfida

* **Invia notifiche**: consegna di messaggi su più canali (in-app, e-mail, push) in fasi chiave:
   * **Lancio**: quando inizia la richiesta di verifica
   * **In corso**: quando i clienti sono tra di loro
   * **Completo**: quando i clienti finiscono la sfida

* **Tieni traccia delle prestazioni**: monitora i percorsi generati automaticamente e rivedi le prestazioni della verifica

### Limitazioni importanti {#limitations}

* **Nessun sistema di contabilità generale**: le sfide di fidelizzazione non tengono traccia dei valori monetari o dei saldi dei punti. Quando i clienti completano una sfida e ottengono un premio, Journey Optimizer chiama il sistema di gestione della fedeltà esterno per gestire l’allocazione di punti.

* **Solo selezione del pubblico**: puoi selezionare tipi di pubblico esistenti ma non puoi crearne di nuovi dall&#39;interfaccia utente Sfide fedeltà.

## Prerequisiti {#prerequisites}

Prima di utilizzare le sfide di fedeltà, assicurati di disporre di:

* Configurazione dell’acquisizione dati

  Le sfide relative alla fedeltà si basano sui dati acquisiti tramite i connettori di origine di Experience Platform per monitorare l’avanzamento dei clienti e il completamento delle attività.

   1. **Configurare un connettore di origine supportato**: attualmente il connettore Capillary è generalmente disponibile. Sono pianificati connettori aggiuntivi.

   2. **Convalida acquisizione dati**: assicurati che gli eventi fedeltà e i dati dei clienti vengano trasmessi ad Experience Platform e siano disponibili in Journey Optimizer.

  Per istruzioni dettagliate, consulta:

   * [Documentazione origini Experience Platform](https://experienceleague.adobe.com/it/docs/experience-platform/sources/home)
   * [Configurare i connettori di origine in Journey Optimizer](../start/get-started-sources.md)

* Autorizzazioni richieste {#required-permissions}

Per utilizzare le sfide di fidelizzazione, è necessario disporre delle autorizzazioni appropriate in Journey Optimizer. Se non riesci ad accedere alla funzione, contatta l’amministratore.

## Accedere alle sfide di fedeltà {#access}

Per accedere alle sfide di fedeltà:

1. In Adobe Journey Optimizer, seleziona **[!UICONTROL Sfide fedeltà]** nel menu di navigazione a sinistra.

   <!--![Loyalty challenges menu in left navigation](assets/loyalty-challenges-menu.png)-->

2. Nell&#39;inventario Sfide fedeltà vengono visualizzate tutte le sfide esistenti con informazioni quali:
   * Nome e descrizione della sfida
   * Stato (Bozza, Live, Arrestato, ecc.)
   * Tipo di sfida (Standard, Streak, Sequenziale)
   * Date di inizio e di fine
   * Data ultima modifica

   <!--![Loyalty challenges inventory showing list of challenges](assets/loyalty-challenges-inventory.png)-->

3. Seleziona **[!UICONTROL Crea sfida]** per iniziare a creare una nuova sfida.

### Problemi di ricerca e filtro {#search-filter}

Utilizza le funzionalità di ricerca e filtro per individuare rapidamente le problematiche specifiche:

#### Ricerca {#search}

Immetti il nome o le parole chiave della richiesta di verifica per trovare le richieste corrispondenti nel campo **[!UICONTROL Ricerca]**.

#### Filtra per stato {#filter-by-status}

Visualizza le sfide con stati specifici in **[!UICONTROL Filtra per stato]**:

* Bozza
* Pianificato
* Live
* Completato
* Interrotto
* Archiviato

#### Filtra per tipo {#filter-by-type}

Mostra solo le sfide Standard, Streak o Sequential utilizzando **[!UICONTROL Filtra per tipo]**.

#### Filtra per data {#filter-by-date}

Visualizza le sfide in un intervallo di date specifico utilizzando **[!UICONTROL Filtra per data]**.

#### Filtra per tag {#filter-by-tags}

Mostra le sfide con tag specifici applicati utilizzando **[!UICONTROL Filtra per tag]**.


**[!UICONTROL Sconto]**: fornisci un codice o un valore di sconto.

* Immettere il tipo di sconto (percentuale o importo fisso)
* Inserisci il valore dello sconto
* Facoltativamente, specifica il codice sconto o lascia che il sistema ne generi uno

**[!UICONTROL Elemento gratuito]**: concedere un prodotto o un servizio gratuito.

* Specifica l&#39;SKU o la descrizione dell&#39;articolo
* Indicare in che modo l&#39;articolo gratuito deve essere richiesto

**[!UICONTROL Premio personalizzato]**: definisci un tipo di premio personalizzato.

* Inserisci la descrizione del premio
* Indicare eventuali codici o identificatori pertinenti
* Configurare il modo in cui il premio viene consegnato o richiesto

#### Esempio di configurazione del premio {#reward-example}

**Sfida**: &quot;Sfida per gli amanti del caffè&quot;

**Attività 1**: Acquista 3 caffè

* Premio: 30 punti (10 punti per caffè)
* Tempistica: dopo il completamento dell’attività

**Attività 2**: provare 2 nuove bevande stagionali

* Premio: 50 punti
* Tempistica: dopo il completamento dell’attività

**Premio per il completamento della sfida**:

* Premio: caffè gratis + 100 punti bonus
* Tempistica: dopo il completamento di tutte le attività

**Premi totali possibili**: 180 punti + 1 caffè gratuito

### Attributi attività avanzati {#advanced-attributes}

Per i casi d’uso avanzati, puoi configurare attributi di attività aggiuntivi:

**[!UICONTROL Condizioni personalizzate]**: aggiungi una logica o condizioni personalizzate oltre i tipi di attività standard utilizzando i segmenti o le regole di Experience Platform.

**[!UICONTROL Geofencing]**: (per le attività Visita) richiede visite a posizioni specifiche definite da coordinate geografiche e raggio.

**[!UICONTROL Requisiti basati sul tempo]**: è necessario completare le attività in ore, giorni o intervalli di date specifici.

**[!UICONTROL Periodo di consolidamento]**: impostare un intervallo di tempo minimo tra il completamento dell&#39;attività per evitare azioni ripetute rapide.

**[!UICONTROL Dipendenze attività]**: (per le sfide sequenziali) definire i prerequisiti che devono essere completati prima che l&#39;attività diventi disponibile.

## Creare le sfide {#create-challenges}

Crea una sfida di fidelizzazione per definire l’offerta di coinvolgimento, configurare le schede di contenuto per la consegna, aggiungere attività, impostare premi e facoltativamente configurare la messaggistica tra i canali.

### Prima di iniziare {#before-you-start}

Prima di creare una sfida, assicurati di disporre di:

* Acquisizione dei dati configurata e convalidata tramite i connettori di origine
* Creazione di un pubblico richiesto in Experience Platform
* Risorse di contenuto preparate (immagini, testo, ecc.) per la sfida
* Definire le attività e i premi che si desidera offrire

### Crea una sfida {#create-a-challenge}

Per creare una nuova sfida di fedeltà:

1. In Journey Optimizer, seleziona **[!UICONTROL Sfide fedeltà]** nel menu di navigazione a sinistra.

2. Seleziona **[!UICONTROL Crea sfida]** nell&#39;angolo superiore destro.

   <!--![Create challenge button in loyalty challenges inventory](assets/create-challenge-button.png)-->

3. Nella schermata delle proprietà della sfida, configura quanto segue:

#### Proprietà di base {#basic-properties}

**[!UICONTROL Nome]**: immetti un nome descrittivo per la richiesta. Questo nome viene visualizzato nell&#39;inventario ed è incluso nel nome del percorso generato automaticamente.

**[!UICONTROL Descrizione]**: (facoltativo) aggiungi una descrizione per aiutare te e il tuo team a comprendere lo scopo e i dettagli di questa sfida.

**[!UICONTROL Tipo di sfida]**: selezionare il tipo di sfida che si desidera creare:

* **[!UICONTROL Standard]**: i clienti possono completare un numero qualsiasi di attività specificate per ottenere il premio. Esempio: &quot;Effettua 5 acquisti questo mese&quot;.

* **[!UICONTROL Streak]**: i clienti devono completare ripetutamente la stessa attività. Esempio: &quot;Visita il nostro negozio 10 volte di fila.&quot;

* **[!UICONTROL Sequenziale]**: i clienti devono completare le attività in un ordine specifico. Esempio: &quot;Prima fai un acquisto, poi scrivi una recensione, quindi fai riferimento a un amico.&quot;

<!--![Challenge type selection showing Standard, Streak, and Sequential options](assets/challenge-type-selection.png)-->

**[!UICONTROL Data di inizio]**: seleziona quando la sfida diventa attiva e disponibile per i clienti.

**[!UICONTROL Data di fine]**: seleziona quando scade la richiesta di verifica. I clienti che non hanno completato la sfida entro questa data non saranno più in grado di ottenere il premio.

#### Selezione del pubblico {#audience-selection}

**[!UICONTROL Seleziona pubblico]**: scegli il pubblico idoneo per questa sfida. Puoi selezionare solo i tipi di pubblico esistenti; non puoi creare nuovi tipi di pubblico dall’interfaccia utente Sfide fedeltà.

Per creare o perfezionare i tipi di pubblico, vedi [Creare tipi di pubblico in Journey Optimizer](../audience/about-audiences.md).

1. Seleziona **[!UICONTROL Salva come bozza]** per continuare a configurare la sfida.

## Creare le attività {#create-tasks}

Le attività definiscono le azioni o i milestone specifici che i clienti devono completare per ottenere premi in una sfida di fedeltà. Puoi configurare tipi di task, quantità, requisiti di prodotto e valori di ricompensa per creare esperienze di fidelizzazione coinvolgenti e personalizzate.

### Panoramica attività {#task-overview}

Ogni attività rappresenta un’azione misurabile che contribuisce al completamento della sfida. A seconda del tipo di sfida (Standard, Streak o Sequenziale), i clienti completano le attività in modo diverso:

* **Sfide standard**: i clienti completano un numero specificato di attività in qualsiasi ordine
* **Sfide**: i clienti completano la stessa attività più volte di seguito
* **Sfide sequenziali**: i clienti completano le attività in un ordine definito

### Aggiungi un&#39;attività {#add-task}

Per aggiungere un&#39;attività alla sfida:

1. Apri la sfida o creane una nuova.

2. Passa alla sezione **[!UICONTROL Attività]**.

   <!--![Tasks section in challenge creation interface](assets/tasks-section.png)-->

3. Seleziona **[!UICONTROL Aggiungi attività]** o **[!UICONTROL Crea nuova attività]**.

4. Nella schermata di creazione dell’attività, configura le seguenti proprietà.

### Proprietà attività {#task-properties}

#### Informazioni attività di base {#basic-info}

**[!UICONTROL Nome attività]**: immettere un nome descrittivo per l&#39;attività. Questo nome è visibile a te e al tuo team, ma potrebbe non essere mostrato ai clienti a seconda della progettazione della scheda di contenuto.

**[!UICONTROL Descrizione attività]**: (facoltativo) aggiungi dettagli sullo scopo o sui requisiti dell&#39;attività.

**[!UICONTROL Tipo di attività]**: selezionare il tipo di azione che i clienti devono eseguire. I tipi di attività disponibili includono:

* **[!UICONTROL Acquisto]**: il cliente effettua una transazione di acquisto
* **[!UICONTROL Importo spesa]**: il cliente spende un importo monetario specificato
* **[!UICONTROL Visita]**: il cliente visita una posizione fisica o una proprietà digitale
* **[!UICONTROL Coinvolgimento]**: il cliente è interessato al contenuto, ad esempio alla visualizzazione di un video o alla lettura di un articolo
* **[!UICONTROL Evento personalizzato]**: il cliente attiva un evento personalizzato tracciato attraverso l&#39;acquisizione dei dati

<!--![Task type selection dropdown showing available task types](assets/task-type-selection.png)-->

#### Quantità richiesta {#quantity-requirements}

**[!UICONTROL Quantità richiesta]**: specificare quante volte il cliente deve eseguire l&#39;attività per completarla.

Ad esempio:

* Per un task di acquisto: &quot;Acquista 2 articoli&quot; (quantità = 2)
* Per un&#39;attività Importo spesa: &quot;Spesa $50&quot; (quantità = 50)
* Per un&#39;attività Visita: &quot;Visita 5 volte&quot; (quantità = 5)

**[!UICONTROL Periodo di verifica]**: (facoltativo) definisci l&#39;intervallo di tempo per il completamento di questa attività:

* Durata per richiesta di verifica (impostazione predefinita)
* Al giorno
* Alla settimana
* Al mese
* Intervallo di date personalizzato

### Filtraggio di prodotti e SKU {#product-filtering}

Per i task Importo acquisti e Spesa, è possibile specificare i prodotti idonei per il completamento del task.

#### Inclusioni dei prodotti {#product-inclusions}

Definire quali prodotti o categorie contano per l&#39;attività:

1. Seleziona **[!UICONTROL Aggiungi criteri prodotto]**.

   <!--![Add product criteria button in task configuration](assets/add-product-criteria.png)-->

2. Scegliere come definire i prodotti qualificati:
   * **[!UICONTROL Per SKU]**: immettere codici SKU di prodotto specifici
   * **[!UICONTROL Per categoria]**: seleziona le categorie di prodotti dal catalogo
   * **[!UICONTROL Per attributo]**: filtra per attributi di prodotto quali marchio, dimensione, colore o attributi personalizzati

3. Inserire o selezionare gli identificatori del prodotto:

   **Esempio - Per SKU**:

   ```text
   SKU001, SKU002, SKU003
   ```

   **Esempio - Per categoria**:

   * Bevande > Caffè
   * Panetteria > Pasticceria

   **Esempio - Per attributo**:

   * Marchio = &quot;Marchio Premium&quot;
   * Categoria = &quot;Articoli stagionali&quot;
   * Prezzo > 20 $

4. Seleziona **[!UICONTROL Aggiungi]** per salvare i criteri del prodotto.

#### Esclusioni di prodotto {#product-exclusions}

È possibile escludere prodotti specifici dal conteggio per l&#39;attività:

1. Seleziona **[!UICONTROL Aggiungi esclusioni]**.

2. Utilizza gli stessi metodi di filtro delle inclusioni di prodotto per specificare quali prodotti escludere.

3. Scenari di esclusione comuni:

   * Articoli di vendita o sdoganamento
   * Biglietti regalo
   * Articoli promozionali o gratuiti
   * Marchi o categorie specifici

>[!NOTE]
>
>**Logica di inclusione ed esclusione**: quando sono definite sia le inclusioni che le esclusioni:
>
>* I prodotti devono soddisfare i criteri di inclusione
>* I prodotti che corrispondono ai criteri di esclusione vengono rimossi, anche se corrispondono alle inclusioni
>* Se non sono definite inclusioni, tutti i prodotti sono idonei ad eccezione di quelli esplicitamente esclusi

#### Esempi di filtraggio dei prodotti {#product-filtering-examples}

##### Esempio 1: Coffee Challenge {#example-1}

* Tipo di attività: Acquisto
* Quantità richiesta: 3
* Inclusioni: Categoria = &quot;Bevande > Caffè&quot;
* Risultato: il cliente deve acquistare 3 bevande a base di caffè

##### Esempio 2: spesa Premium {#example-2}

* Tipo di attività: importo spesa
* Quantità richiesta: $100
* Inclusioni: Marchio = &quot;Marchio Premium&quot;
* Esclusioni: Categoria = &quot;Gioco&quot;
* Risultato: il cliente deve spendere $ 100 per gli articoli Premium con marchio, esclusi gli articoli di cancellazione

##### Esempio 3: acquisto di prodotti specifici {#example-3}

* Tipo di attività: Acquisto
* Quantità richiesta: 1
* Inclusioni: SKU = &quot;NEWPRODUCT2024&quot;
* Risultato: il cliente deve acquistare il prodotto specifico con SKU &quot;NEWPRODUCT2024&quot;

### Configurare i premi {#configure-rewards}

Definire cosa guadagnano i clienti per il completamento delle attività. I premi possono essere concessi a livello di attività o a livello di sfida dopo il completamento di tutte le attività.

#### Tempistica premio {#reward-timing}

Scegli quando i clienti ricevono i premi:

**[!UICONTROL Dopo il completamento dell&#39;attività]**: i clienti ricevono un premio subito dopo aver completato questa attività specifica (detti anche &quot;premi progressivi&quot; o &quot;premi milestone&quot;).

**[!UICONTROL Dopo il completamento della sfida]**: i clienti ricevono un premio solo dopo aver completato tutte le attività richieste nella sfida (detti anche &quot;premi finali&quot; o &quot;premi speciali&quot;).

>[!TIP]
>
>È possibile combinare entrambi i tipi di premi in un&#39;unica sfida per mantenere il coinvolgimento in tutto il percorso del cliente. Ad esempio:
>
>* Assegna 10 punti dopo il completamento di ogni attività (premi progressivi)
>* Attribuisci altri 100 punti dopo aver completato l&#39;intera sfida (premio finale)

#### Tipi e valori di premi {#reward-types}

**[!UICONTROL Punti]**: punti fedeltà premio all&#39;account del cliente.

* Immetti il numero di punti (ad esempio, 100)
* I punti vengono comunicati al sistema di gestione della fedeltà esterno tramite API

## Configurare le schede di contenuto {#configure-content-cards}

Le schede di contenuto sono il modo principale in cui le sfide vengono visualizzate ai clienti sui loro dispositivi. Devi configurare una scheda di contenuto per la tua sfida.

1. In questa sfida, passa alla scheda **[!UICONTROL Contenuto]**.

2. Seleziona **[!UICONTROL Modifica contenuto]** per aprire l&#39;editor della scheda di contenuto.

   <!--![Content tab with Edit content button](assets/content-tab-edit.png)-->

3. Configura le proprietà della scheda di contenuto:

   **[!UICONTROL Nome configurazione]**: immettere un nome per la configurazione della scheda di contenuto.

   **[!UICONTROL Configurazione]**: selezionare o creare una configurazione della scheda di contenuto. Definisce le impostazioni tecniche per la modalità di distribuzione della scheda di contenuto.

4. Nell’editor delle schede di contenuto, progetta la tua scheda di sfida:

   * Aggiungi testo per descrivere la sfida, le attività e i premi
   * Includi immagini o altri elementi visivi
   * Utilizzare la personalizzazione per includere informazioni specifiche per il cliente
   * Visualizzare gli indicatori di avanzamento, se applicabili
   * Aggiungi pulsanti call-to-action

   L’editor delle schede di contenuto offre le stesse funzionalità degli altri canali di Journey Optimizer. Per istruzioni dettagliate, consulta [Progettare le schede di contenuto](../content-card/design-content-card.md).

5. Seleziona **[!UICONTROL Salva]** per salvare la configurazione della scheda di contenuto.

>[!NOTE]
>
>La scheda di contenuto viene distribuita tramite il percorso generato automaticamente. Viene visualizzato ai membri del pubblico idonei quando la sfida è attiva.

## Configurare la messaggistica {#configure-messaging}

Facoltativamente, puoi configurare i messaggi da inviare ai clienti nelle fasi chiave del ciclo di vita della sfida. La messaggistica è disponibile in tre fasi:

* **[!UICONTROL Lancio]**: invia un messaggio quando la richiesta di verifica diventa attiva
* **[!UICONTROL In corso]**: invia un messaggio quando i clienti sono parte della sfida
* **[!UICONTROL Completa]**: invia un messaggio quando i clienti completano la richiesta di verifica

### Aggiungere messaggi {#add-messages}

1. Nella tua sfida, passa alla scheda **[!UICONTROL Messaggistica]**.

   <!--![Messaging tab showing Launch, In progress, and Complete stages](assets/messaging-tab-stages.png)-->

2. Seleziona la fase in cui desideri aggiungere un messaggio: Avvio, In corso o Completo.

3. Seleziona **[!UICONTROL Aggiungi messaggio]**.

4. Scegli il canale per il messaggio:
   * **[!UICONTROL In-app]**: visualizza un messaggio nell&#39;applicazione
   * **[!UICONTROL E-mail]**: invia una notifica e-mail
   * **[!UICONTROL Push]**: invia una notifica push

5. Seleziona **[!UICONTROL Modifica contenuto]** per aprire l&#39;editor di contenuti per il canale selezionato.

6. Progetta il messaggio utilizzando l’editor di contenuto standard:
   * Aggiungere testo, immagini e altri elementi di contenuto
   * Utilizzare la personalizzazione per includere informazioni specifiche per il cliente
   * Includi dettagli della sfida come avanzamento o premi
   * Aggiungere contenuto dinamico in base agli attributi o ai comportamenti dei clienti

   Per informazioni specifiche sul canale, consulta:
   * [Creare messaggi in-app](../in-app/create-in-app.md)
   * [Creare le e-mail](../email/create-email.md)
   * [Creare notifiche push](../push/create-push.md)

7. Seleziona **[!UICONTROL Salva]** per salvare il messaggio.

8. Ripeti questi passaggi per aggiungere messaggi per altri stadi o canali in base alle esigenze.

>[!NOTE]
>
>Puoi aggiungere più messaggi per fase, per raggiungere i clienti su canali diversi. Ad esempio, puoi inviare sia un’e-mail che una notifica push all’avvio di una sfida.

### Tempistica dei messaggi e attivatori {#message-timing}

**Messaggi di avvio**: inviati quando la sfida diventa attiva per il pubblico idoneo.

**Messaggi in corso**: attivato quando i clienti raggiungono un punto di avanzamento specificato. Puoi configurare le condizioni di attivazione in base a:

* Numero di attività completate
* Percentuale di sfida completata
* Completamento attività specifica
* Tempo trascorso dall&#39;inizio della sfida

**Messaggi completi**: inviati quando i clienti completano tutte le attività richieste.

>[!TIP]
>
>**Best practice per la messaggistica**:
>
>* Messaggi concisi e focalizzati sulla sfida
>* Comunicare chiaramente il valore e i vantaggi
>* Utilizza tono e branding coerenti
>* Includi inviti all&#39;azione chiari
>* Verifica i messaggi prima di pubblicare la sfida

## Generare e personalizzare percorsi {#generate-journey}

Quando salvi una sfida con contenuti e messaggi configurati, Journey Optimizer genera automaticamente un percorso nel backend.

### Come funziona la generazione di percorsi {#journey-generation-process}

1. Quando si salva una sfida e si seleziona **[!UICONTROL Genera percorso]**, Journey Optimizer crea un nuovo percorso.

2. Il percorso viene automaticamente denominato in base al nome della richiesta di verifica (ad esempio, &quot;Richiesta di verifica: [Nome della richiesta di verifica]&quot;).

3. L’area di lavoro del percorso include:
   * **[!UICONTROL Attività Read audience]** con il pubblico selezionato
   * **Scheda contenuto** azione di consegna
   * **Attività messaggi** per tutti i messaggi configurati (Launch, In corso, Completato)
   * **Attendi** e **Condizione** le attività necessarie in base alla configurazione

   <!--![Auto-generated journey canvas showing content card and message activities](assets/generated-journey-canvas.png)-->

4. Il percorso viene visualizzato nell’inventario del percorso ed è visibile a tutti gli utenti con le autorizzazioni appropriate.

### Visualizza il percorso generato {#view-journey}

Per visualizzare il percorso generato automaticamente:

1. Passa a **[!UICONTROL Percorsi]** nel menu di navigazione a sinistra.

2. Cerca il percorso per nome della richiesta di verifica o, se li hai assegnati, filtra per tag.

3. Selezionare il percorso per visualizzarne l&#39;area di lavoro e la configurazione.

### Personalizzare il percorso {#customize-journey}

Puoi modificare il percorso generato automaticamente per aggiungere logica personalizzata, attività aggiuntive o configurazioni avanzate.

>[!IMPORTANT]
>
>**Considerazioni importanti durante la modifica dei percorsi**:
>
>* Le modifiche apportate all&#39;area di lavoro del percorso **non vengono sincronizzate** con l&#39;interfaccia utente Sfide fedeltà
>* La sfida rimane la fonte di verità per la definizione dell’esperienza di base
>* Journey Optimizer visualizza un avviso quando si entra in modalità di modifica personalizzata
>* Se devi apportare modifiche ad attività, premi o proprietà della sfida principale, modificale nell’interfaccia utente Sfide fedeltà, non nel percorso
>* Le modifiche di percorso personalizzate sono appropriate per la logica di routing, tempistica o integrazione avanzata

Per personalizzare il percorso:

1. Aprire il percorso generato dall&#39;inventario del percorso.

2. In Journey Optimizer viene visualizzato un avviso relativo alla modifica personalizzata. Legga attentamente l’avvertenza e la riconosca.

3. Apporta le modifiche desiderate utilizzando l’area di lavoro del percorso:
   * Aggiungi altre attività (attese, condizioni, azioni)
   * Configurare regole avanzate di frequenza o tempistica
   * Aggiungere azioni o integrazioni personalizzate
   * Modificare le condizioni di ingresso del pubblico

4. Verifica accuratamente le modifiche prima di pubblicarle.

5. Pubblica il percorso quando è pronto.

Per istruzioni dettagliate sulla modifica dei percorsi, consulta [Genera percorsi](../building-journeys/journey-gs.md).

### Considerazioni sull’area di lavoro del percorso {#journey-considerations}

Quando si lavora con percorsi generati automaticamente:

* **Impossibile modificare il pubblico nel percorso**: se è necessario modificare il pubblico, eseguirlo nell&#39;interfaccia utente Sfide fedeltà e rigenerare il percorso.

* **Aggiornamenti del contenuto dei messaggi**: per mantenere la coerenza, è necessario apportare modifiche al contenuto dei messaggi nell&#39;interfaccia utente Sfide fedeltà.

* **Stato Percorso**: lo stato del percorso (Bozza, Live, Interrotto) viene gestito indipendentemente dallo stato della richiesta di verifica.

* **Test**: verifica l&#39;intera esperienza di verifica, non solo il percorso, per garantire che tutti i componenti funzionino correttamente.

## Revisione e pubblicazione {#review-and-publish}

Prima di pubblicare la sfida:

1. **Controlla tutti i componenti**:
   * Proprietà e date della sfida
   * Attività e requisiti delle attività
   * Configurazione dei premi
   * Progettazione scheda di contenuto
   * Contenuto e tempistica dei messaggi
   * Struttura percorso generata

2. **Verifica l&#39;esperienza**:
   * Utilizzare i profili di test per convalidare il rendering del contenuto
   * Verifica che le attività si attivino correttamente in base ai dati di test
   * Verifica logica di allocazione premi
   * Verifica i messaggi su tutti i canali configurati
   * Rivedi l’esecuzione del percorso con i tipi di pubblico di test

3. **Pubblica la tua sfida**:
   * Al termine, seleziona **[!UICONTROL Pubblica]** dalle proprietà della richiesta di verifica
   * La sfida diventa attiva alla data di inizio specificata
   * Il percorso generato automaticamente è attivato
   * I membri del pubblico idonei possono vedere e partecipare alla sfida

## Gestire le sfide {#manage-challenges}

Dopo aver creato e pubblicato le sfide relative alla fidelizzazione, puoi visualizzarle, modificarle, monitorarle e ottimizzarle per garantire che forniscano i risultati desiderati per il programma fedeltà.

### Stati di sfida {#challenge-statuses}

Ogni sfida si sposta attraverso un ciclo di vita che si riflette sul suo stato:

**[!UICONTROL Bozza]**: è in corso la creazione o la modifica della sfida, ma non è ancora stata pubblicata. Puoi apportare qualsiasi modifica alle bozze delle sfide.

**[!UICONTROL Pianificato]**: la sfida è pubblicata e diventa attiva alla data di inizio. I clienti non possono ancora vedere le sfide pianificate né parteciparvi.

**[!UICONTROL Live]**: la sfida è attiva e i clienti del pubblico idoneo possono visualizzarla e parteciparvi. Questo stato viene visualizzato quando la data corrente è compresa tra le date di inizio e di fine.

**[!UICONTROL Completato]**: la sfida ha superato la data di fine oppure tutti gli obiettivi sono stati raggiunti. I clienti non possono più partecipare, ma è possibile visualizzare dati e risultati storici.

**[!UICONTROL Arrestato]**: la verifica è stata arrestata manualmente prima del completamento. I clienti non possono più partecipare. Per riattivare una sfida interrotta, devi duplicarla e creare una nuova versione.

**[!UICONTROL Archiviato]**: la sfida è stata archiviata per scopi organizzativi. Le sfide archiviate possono essere recuperate utilizzando i filtri, ma sono nascoste dalla vista predefinita.

### Visualizza dettagli della sfida {#view-details}

Per visualizzare informazioni dettagliate su una sfida:

1. Nell&#39;inventario, fai clic sul nome della sfida o seleziona il menu **[!UICONTROL Altre azioni]** (tre punti) e scegli **[!UICONTROL Visualizza dettagli]**.

   <!--![Challenge inventory with More actions menu highlighted](assets/challenge-more-actions.png)-->

2. Viene visualizzata la schermata dei dettagli della sfida:

   Scheda **[!UICONTROL Panoramica]**:
   * Proprietà di base (nome, descrizione, tipo, date)
   * Informazioni sullo stato attuale e sul ciclo di vita
   * Informazioni sul pubblico
   * Cronologia di creazione e modifica

   Scheda **[!UICONTROL Attività]**:
   * Elenco di tutte le attività della sfida
   * Tipi di task, requisiti e condizioni
   * Premi configurati per attività

   Scheda **[!UICONTROL Contenuto]**:
   * Configurazione e anteprima della scheda di contenuto
   * Rendering visivo della sfida per i clienti

   Scheda **[!UICONTROL Messaggistica]**:
   * Messaggi configurati per le fasi Launch, In corso e Completato
   * Assegnazioni dei canali e anteprime dei contenuti

   **[!UICONTROL Scheda Prestazioni]** (per le sfide Live e Completed):
   * Metriche di partecipazione
   * Percentuali di completamento
   * Distribuzione dei premi
   * Statistiche di coinvolgimento messaggi

### Modifica le sfide {#edit-challenges}

Puoi modificare le sfide in base al loro stato corrente.

#### Modifica bozza delle sfide {#edit-draft}

Per le sfide con stato **[!UICONTROL Bozza]**:

1. Fai clic sul nome della richiesta di verifica o seleziona **[!UICONTROL Modifica]** dal menu Azioni.

2. Modificate qualsiasi aspetto della sfida:
   * Proprietà di base
   * Attività e premi
   * Schede contenuto
   * Messaggistica
   * Selezione del pubblico

3. Seleziona **[!UICONTROL Salva come bozza]** per salvare le modifiche senza pubblicare, oppure **[!UICONTROL Pubblica]** per rendere attiva la richiesta.

#### Modifica le sfide pubblicate {#edit-published}

Per le sfide **[!UICONTROL Pianificate]** o **[!UICONTROL Live]**:

>[!IMPORTANT]
>
>**Impatto della modifica delle sfide live**: le modifiche alle sfide live possono interessare i clienti che già partecipano. Prima di apportare modifiche, considera quanto segue:
>
>* La modifica dei requisiti delle attività può invalidare l&#39;avanzamento del cliente
>* La modifica dei premi può creare incongruenze per i clienti che hanno già ottenuto premi
>* Le modifiche del pubblico possono escludere i clienti precedentemente idonei
>* Le modifiche ai contenuti vengono visualizzate immediatamente ai clienti
>
>Per modifiche significative, puoi interrompere la sfida corrente e creare una nuova versione.

**Modifica limitata per le sfide live**:

Puoi apportare queste modifiche alle sfide live senza fermarle:

* Aggiorna descrizione richiesta di verifica (interfaccia)
* Modificare gli elementi visivi e il testo delle schede di contenuto
* Aggiornare il contenuto dei messaggi
* Regola data di fine (solo estensione, non può essere abbreviata)
* Aggiungere o modificare i tag

**Modifiche che richiedono la duplicazione della richiesta**:

Per modificare queste proprietà, devi duplicare la richiesta e creare una nuova versione:

* Tipo di sfida (Standard, Streak, Sequenziale)
* Requisiti e condizioni delle attività
* Valori premio e regole di allocazione
* Data di inizio (per le sfide live)
* Pubblico (modifiche principali)

### Duplicare una sfida {#duplicate-challenge}

La duplicazione crea una copia di una sfida esistente che è possibile modificare e pubblicare come nuova sfida:

1. Nell&#39;inventario, seleziona il menu **[!UICONTROL Altre azioni]** (tre punti) per la sfida che desideri duplicare.

2. Seleziona **[!UICONTROL Duplica]**.

3. Nella finestra di dialogo di duplicazione:
   * Immetti un nuovo nome per la richiesta duplicata
   * È possibile modificare la descrizione
   * Scegli se copiare le impostazioni del pubblico
   * Scegli se copiare le configurazioni di messaggistica

4. Seleziona **[!UICONTROL Duplica]**.

5. La sfida duplicata si apre in modalità bozza, dove puoi apportare modifiche prima di pubblicarla.

**Scenari di duplicazione comuni**:

* Rieseguire una sfida di successo per un nuovo periodo di tempo
* Creare varianti di una sfida per tipi di pubblico diversi
* Aggiorna i requisiti delle attività o i premi per una nuova versione
* Riattivare una richiesta di verifica interrotta o completata

### Interrompere una sfida {#stop-challenge}

Per interrompere una sfida in tempo reale o pianificata prima della sua data di fine naturale:

1. Selezionare la sfida nell&#39;inventario.

2. Selezionare **[!UICONTROL Interrompi verifica]** dal menu Azioni.

3. Nella finestra di dialogo di conferma, esamina l’impatto:
   * I clienti che attualmente partecipano non possono più fare progressi
   * I clienti che hanno completato le attività ma non hanno completato la sfida non riceveranno i premi finali
   * Il percorso associato viene arrestato
   * Impossibile riavviare la verifica (duplicare per riutilizzarla)

4. Seleziona **[!UICONTROL Interrompi]** per confermare.

>[!NOTE]
>
>**Interruzione e completamento**: una richiesta di verifica interrotta termina prematuramente e non segue il normale processo di completamento. I clienti ricevono premi parziali già assegnati, ma non premi finali per il completamento della sfida. Prendere in considerazione la comunicazione di fascia precoce ai clienti interessati.

### Sfide relative all&#39;archiviazione {#archive}

Archiviare le sfide completate o interrotte per mantenere organizzato l&#39;inventario:

1. Seleziona il menu **[!UICONTROL Altre azioni]** (tre punti) per la sfida.

2. Seleziona **[!UICONTROL Archivia]**.

3. La sfida passa allo stato archiviato ed è nascosta dalla vista inventario predefinita.

Per visualizzare le problematiche archiviate:

1. Nell&#39;inventario, applica il filtro **[!UICONTROL Stato]**.

2. Seleziona **[!UICONTROL Archiviato]**.

3. Le problematiche archiviate vengono visualizzate con le stesse informazioni delle problematiche attive.

Per annullare l’archiviazione di una sfida:

1. Trova la sfida archiviata utilizzando i filtri.

2. Selezionare **[!UICONTROL Annulla archiviazione]** dal menu Azioni.

3. La sfida ritorna allo stato precedente (Completato o Interrotto).

### Eliminare le sfide {#delete}

Eliminare le sfide non più necessarie:

>[!IMPORTANT]
>
>**Eliminazione permanente**: impossibile recuperare le sfide eliminate. Elimina solo le sfide di cui sei sicuro di non aver bisogno in futuro. Anziché eliminare, è consigliabile archiviare per mantenere i record cronologici.

**Regole di eliminazione**:

* Puoi eliminare solo le sfide con stato **[!UICONTROL Bozza]**
* Impossibile eliminare le sfide pubblicate, pianificate, live o completate
* Per rimuovere una sfida pubblicata, devi prima arrestarla, quindi archiviarla

Per eliminare una bozza di richiesta di verifica:

1. Seleziona il menu **[!UICONTROL Altre azioni]** (tre punti) per la sfida.

2. Seleziona **[!UICONTROL Elimina]**.

3. Nella finestra di dialogo di conferma, conferma l’eliminazione.

## Monitorare le prestazioni {#monitor-performance}

Monitora in che modo i clienti si impegnano con le tue sfide utilizzando metriche delle prestazioni integrate.

### Metriche delle prestazioni {#performance-metrics}

La scheda Prestazioni mostra le metriche chiave per le sfide live e completate:

<!--![Performance metrics dashboard showing participation and completion data](assets/performance-metrics-dashboard.png)-->

**[!UICONTROL Metriche di partecipazione]**:

* **Totale clienti idonei**: numero di clienti nel pubblico di destinazione
* **Clienti iscritti**: numero di clienti che hanno visualizzato la richiesta o che si sono impegnati con essa
* **Tasso di iscrizione**: percentuale di clienti idonei iscritti
* **Partecipanti attivi**: numero di clienti attualmente in corso

**[!UICONTROL Metriche di completamento]**:

* **Clienti completati**: numero di clienti che hanno completato tutte le attività
* **Percentuale di completamento**: percentuale di clienti iscritti che hanno completato la sfida
* **Tempo medio di completamento**: tempo medio dall&#39;iscrizione al completamento
* **Attività completate**: numero totale di singole attività completate per tutti i clienti

**[!UICONTROL Metriche premio]**:

* **Premi totali distribuiti**: somma di tutti i premi allocati
* **Premi per tipo**: suddivisione per punti, sconti, articoli gratuiti e così via.
* **Premio medio per cliente**: valore del premio medio per i clienti partecipanti

**[!UICONTROL Metriche di coinvolgimento]**:

* **Impression scheda contenuto**: numero di volte in cui è stata visualizzata la richiesta di verifica
* **Clic sulla scheda dei contenuti**: numero di volte in cui i clienti hanno interagito con la scheda della sfida
* **Consegna messaggi**: numero di messaggi inviati per le fasi di avvio, in corso e completamento
* **Coinvolgimento messaggi**: percentuali di apertura e clic per messaggi per area di visualizzazione e canale

### Visualizzare i rapporti sulle prestazioni {#view-reports}

Per accedere a dati dettagliati sulle prestazioni:

1. Apri la sfida e passa alla scheda **[!UICONTROL Prestazioni]**.

2. Seleziona l’intervallo di date per il reporting (Oggi, Ultimi 7 giorni, Ultimi 30 giorni, Intervallo personalizzato).

3. Rivedi metriche per:
   * **Panoramica**: riepilogo di alto livello delle metriche chiave
   * **Timeline**: tendenze delle prestazioni nel tempo
   * **Raggruppamento**: metriche segmentate per attributi, canali o attività del cliente

4. Esporta i report utilizzando il pulsante **[!UICONTROL Esporta]** per ulteriori analisi.

### Monitorare il percorso generato {#monitor-journey}

Il percorso generato automaticamente contiene preziosi dati di esecuzione:

1. Dai dettagli della richiesta di verifica, selezionare **[!UICONTROL Visualizza percorso]** per aprire il percorso associato.

2. Nell’area di lavoro del percorso, rivedi:
   * **Rapporto Percorso**: statistiche generali di esecuzione
   * **Report attività**: prestazioni delle singole attività
   * **Metriche di entrata e di uscita**: quanti clienti sono entrati ed usciti
   * **Registri errori**: qualsiasi problema o errore di esecuzione

3. Utilizza il monitoraggio del percorso per identificare:
   * Strozzature in cui i clienti abbandonano
   * Problemi tecnici relativi alla consegna
   * Prestazioni dei messaggi per canale
   * Opportunità di ottimizzazione della tempistica

Per istruzioni dettagliate sul monitoraggio del percorso, consulta [Monitorare i percorsi](../building-journeys/report-journey.md).

### Ottimizzare le sfide {#optimize}

Utilizza i dati sulle prestazioni per migliorare le sfide attuali e future:

**[!UICONTROL Varianti di test]**: crea problemi duplicati con attività, premi o messaggi diversi per confrontare le prestazioni.

**[!UICONTROL Modifica tempistica]**: modifica la durata della sfida o le scadenze dell&#39;attività in base ai modelli di completamento.

**[!UICONTROL Perfeziona pubblico]**: espandi o restringi la selezione del pubblico in base ai tassi di coinvolgimento e completamento.

**[!UICONTROL Aggiorna contenuto]**: aggiorna le schede dei contenuti e i messaggi per mantenere l&#39;interesse e la chiarezza.

**[!UICONTROL Ottimizzazione premi]**: regola i valori dei premi per bilanciare costi e partecipazione.

**[!UICONTROL Difficoltà dell&#39;attività]**: modificare i requisiti dell&#39;attività se sono troppo semplici o troppo difficili in base ai dati di completamento.

## Convalida e test delle attività {#validation-testing}

Prima di pubblicare la richiesta di verifica, verifica che le attività siano configurate correttamente:

1. **Verifica logica attività**:
   * Verificare che i requisiti di quantità siano realistici
   * Verificare che i criteri di filtro del prodotto siano corretti
   * Conferma che i premi siano configurati correttamente

2. **Verifica con profili di test**:
   * Creare profili di test che rappresentano scenari cliente diversi
   * Inviare eventi di test tramite la pipeline di acquisizione dati
   * Verificare che le attività vengano attivate correttamente
   * Conferma i premi allocati come previsto

3. **Verifica mappatura dati**:
   * Assicurati che i dati dell’evento in arrivo siano mappati correttamente sui requisiti dell’attività
   * Verifica la corrispondenza di SKU, categorie e attributi tra il sistema di origine e Journey Optimizer
   * Casi limite del test (dati mancanti, valori non validi, ecc.)

## Best practice {#best-practices}

### Creazione di una sfida

**Inizia semplice**: per la prima sfida, inizia con una semplice sfida standard per acquisire familiarità con il processo.

**Verifica approfondita**: verifica sempre la tua sfida con profili di test e pubblico prima di pubblicarla nella tua base clienti completa.

**Cancella comunicazione**: assicurati che i clienti comprendano cosa devono fare, cosa guadagneranno e quando.

**Tempistica realistica**: imposta le date di inizio e di fine appropriate, lasciando ai clienti tempo sufficiente per completare la sfida.

**Premi interessanti**: premi preziosi e pertinenti per il tuo pubblico per stimolare la partecipazione.

### Configurazione attività

**Cancella requisiti**: rendi i requisiti dell&#39;attività chiari e realizzabili. Evita condizioni eccessivamente complesse.

**Difficoltà appropriata**: bilanciare la difficoltà dell&#39;attività con il valore della ricompensa. I compiti più difficili dovrebbero offrire maggiori premi.

**Precisione del filtro del prodotto**: controlla nuovamente SKU, categorie e attributi per garantire una corrispondenza accurata del prodotto.

**Premi progressivi**: utilizza i premi milestone (dopo il completamento dell&#39;attività) per mantenere il coinvolgimento del cliente durante l&#39;intera sfida.

**Flessibilità**: per le sfide standard, consenti flessibilità nel modo in cui i clienti completano le attività per adattarsi a comportamenti e preferenze diversi.

### Gestione e monitoraggio

**Monitoraggio regolare**: verifica le prestazioni della verifica almeno settimanalmente per individuare in tempo reale i problemi.

**Cancella denominazione**: utilizza nomi descrittivi che indicano lo scopo della sfida, il pubblico o il periodo di tempo per un&#39;organizzazione semplice.

**Usa tag**: applica tag coerenti per categorizzare le sfide in base a campagna, stagione, segmento di pubblico o altri attributi rilevanti.

**Modifiche al documento**: prendi nota del motivo per cui hai apportato modifiche alle sfide per riferimento e apprendimento futuri.

**Archiviazione coerente**: archiviazione regolare delle sfide completate per mantenere gestibile l&#39;inventario.

**Comunicazione delle modifiche**: se modifichi una sfida live, informa i clienti interessati delle modifiche che influiscono sulla loro partecipazione.

**Analizza dopo il completamento**: rivedi le prestazioni dopo il termine di ogni sfida per identificare gli insegnamenti appresi per le sfide future.

**Rollout graduale**: per nuovi tipi di sfida o modifiche significative, puoi iniziare con un pubblico più piccolo prima della distribuzione completa.

**Controllo della versione**: utilizza il controllo delle versioni non crittografate nei nomi delle sfide durante la creazione di iterazioni (ad esempio, &quot;Holiday Challenge 2024 - v2&quot;).

## Risoluzione dei problemi {#troubleshooting}

**La sfida non viene visualizzata ai clienti**:

* Verifica che la sfida sia nello stato Live
* Verifica che i clienti siano nel pubblico idoneo
* Conferma che la configurazione della scheda di contenuto sia corretta
* Esamina i registri di esecuzione del percorso per i problemi di consegna

**Bassa partecipazione**:

* Rivedi la visibilità della scheda dei contenuti e l’appello
* Verifica che la messaggistica comunichi chiaramente il valore
* Garantire l&#39;operatività e l&#39;attrattiva delle attività
* Verificare che il targeting del pubblico sia appropriato

**Attività non attivate**:

* Verifica che i dati vengano acquisiti correttamente dai connettori di origine
* Verificare che gli attributi dell&#39;evento corrispondano ai requisiti dell&#39;attività
* Verifica idoneità del pubblico

**Premi non allocati**:

* Conferma la corretta configurazione del premio
* Verificare la connessione al sistema di gestione della fedeltà esterno
* Verifica la presenza di errori nei registri di consegna dei premi

**Il filtro del prodotto non funziona**:

* Convalidare codici SKU e nomi di categoria
* Verificare che la mappatura degli attributi sia corretta
* Test con dati di acquisto di esempio

**Il Percorso non genera**:

* Conferma il completamento di tutta la configurazione richiesta
* Verifica la presenza di errori nella scheda Messaggistica
* Verifica che la scheda di contenuto sia configurata
* Esaminare i registri errori di sistema

**Dati prestazioni non visualizzati**:

* Consenti la propagazione dei dati (fino a 24 ore)
* Verificare che gli eventi vengano tracciati correttamente
* Controllare lo stato di acquisizione dei dati
* Assicurati che i clienti abbiano iniziato a partecipare

## Feedback su Beta {#beta-feedback}

Durante la fase beta, il tuo feedback è prezioso per aiutarci a migliorare le Sfide relative alla fedeltà. Condividi esperienze, domande e suggerimenti con il tuo rappresentante Adobe o tramite i canali di feedback beta forniti durante l’avvio.

## Argomenti correlati {#related-topics}

* [Creare tipi di pubblico in Journey Optimizer](../audience/about-audiences.md)
* [Progettare schede di contenuto](../content-card/design-content-card.md)
* [Creare messaggi in-app](../in-app/create-in-app.md)
* [Creare le e-mail](../email/create-email.md)
* [Creare notifiche push](../push/create-push.md)
* [Genera percorsi](../building-journeys/journey-gs.md)
* [Monitorare i percorsi](../building-journeys/report-journey.md)
* [Documentazione origini Experience Platform](https://experienceleague.adobe.com/it/docs/experience-platform/sources/home)
* [Configurare i connettori di origine in Journey Optimizer](../start/get-started-sources.md)
