---
solution: Journey Optimizer
product: journey optimizer
title: Creare problemi di fidelizzazione
description: Scopri come creare e configurare le sfide relative alla fedeltà in Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta privata" type="Informative"
source-git-commit: e98fe328b5a72a7091d48b5e2939a24e4ad6954c
workflow-type: tm+mt
source-wordcount: '1055'
ht-degree: 1%

---


# Creare le sfide {#create-challenges}

>[!BEGINSHADEBOX]

**Documentazione sulle sfide di fedeltà:**

* [Introduzione alle sfide di fidelizzazione](get-started.md) - Panoramica, flusso di lavoro, prerequisiti
* [Accedere alle sfide di fidelizzazione](access-loyalty-challenges.md) - Inventario e filtro
* **Crea problemi** ◀︎ **Sei qui** - Genera e configura problemi
* [Gestire le sfide](manage-challenges.md) - Modificare, monitorare, ottimizzare

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_loyalty_create_challenge"
>title="Creare una sfida di fidelizzazione"
>abstract="Crea una sfida di fidelizzazione per definire l’offerta di coinvolgimento, configurare le schede di contenuto per la consegna, aggiungere attività, impostare premi e facoltativamente configurare la messaggistica tra i canali."

## Prima di iniziare {#before-you-start}

Prima di creare una sfida, assicurati di disporre di:

* Acquisizione dei dati configurata e convalidata tramite i connettori di origine
* Creazione di un pubblico richiesto in Experience Platform
* Risorse di contenuto preparate (immagini, testo, ecc.) per la sfida
* Definire le attività e i premi che si desidera offrire

## Crea una sfida {#create-a-challenge}

Per i passaggi dettagliati sulla creazione di sfide, tra cui:
* Configurazione delle proprietà della sfida
* Tipi di sfida (Standard, Streak, Sequenziale)
* Selezione del pubblico
* Configurazione data

## Aggiungi attività {#add-tasks}

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

## Configurare le schede di contenuto {#configure-content-cards}

Per i passaggi dettagliati sulla configurazione delle schede di contenuto, tra cui:
* Configurazione scheda contenuto
* Progettazione e personalizzazione
* Anteprima e test

## Configurare la messaggistica {#configure-messaging}

Per i passaggi dettagliati sulla configurazione della messaggistica multicanale, tra cui:
* Canali dei messaggi (in-app, e-mail, push)
* Fasi del messaggio (lancio, in corso, completo)
* Tempistica dei messaggi e attivatori

## Revisione e pubblicazione {#review-and-publish}

Prima di pubblicare la sfida:

1. **Rivedi tutti i componenti**: verifica proprietà, attività, premi, contenuto, messaggi
2. **Verifica l&#39;esperienza**: utilizza i profili di test per convalidare il contenuto e i trigger delle attività
3. **Pubblicazione**: attiva la sfida per il pubblico di destinazione

Il percorso generato automaticamente si attiva alla data di inizio specificata.

## Passaggi successivi {#next-steps}

* [Gestire le sfide](manage-challenges.md) - Scopri come modificare, monitorare e ottimizzare le sfide
* [Comprendere le sfide relative alla fedeltà](get-started.md) - Rivedere le funzionalità
