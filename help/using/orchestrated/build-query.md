---
solution: Journey Optimizer
product: journey optimizer
title: Creare la prima regola
description: Scopri come creare regole per le campagne orchestrate
exl-id: 5e956a6a-0b89-4d78-8f16-fe9fceb25674
version: Campaign Orchestration
source-git-commit: 78fe305975ec97b45e73d60b1dcd66800f67d26e
workflow-type: tm+mt
source-wordcount: '1878'
ht-degree: 97%

---


# Creare la prima regola {#build-query}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_querymodeler_selectaudience"
>title="Selezionare il tipo di pubblico"
>abstract="Utilizzando l’opzione **Seleziona pubblico**, puoi scegliere il pubblico da utilizzare per filtrare la query."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_querymodeler_predefinedfilter"
>title="Filtro preimpostato"
>abstract="Con l’opzione **Filtro preimpostato** puoi selezionare un filtro preimpostato dall’elenco dei filtri personalizzati o dai preferiti."

I passaggi principali per creare regole per le campagne orchestrate sono i seguenti:

1. **Aggiungi condizioni**: crea condizioni personalizzate per filtrare la query creando la tua condizione personalizzata con gli attributi dal database e le espressioni avanzate.
1. **Combina condizioni**: dispone le condizioni nell’area di lavoro utilizzando gruppi e operatori logici.
1. **Verifica e convalida la regola**: prima di salvarla, controlla i dati risultanti dalla regola.

## Aggiungere una condizione {#conditions}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_querymodeler_customcondition"
>title="Condizione personalizzata"
>abstract="Le condizioni personalizzate sono componenti di filtraggio che consentono di filtrare la query creando la propria condizione con attributi provenienti dal database ed espressioni avanzate."

Per aggiungere condizioni nella query, segui questi passaggi:

1. Accedi al generatore di regole da un’attività **[!UICONTROL Crea pubblico]**.

1. Fai clic sul pulsante **Aggiungi condizione** per creare una prima condizione per la query.

   Puoi inoltre avviare la query utilizzando un filtro predefinito. A tale scopo, fai clic sul pulsante **[!UICONTROL Seleziona o salva filtro]** e scegli **[!UICONTROL Seleziona filtro predefinito]**.

   ![immagine che mostra il generatore di regole](assets/rule-builder-add.png)

1. Identifica l’attributo dal database da utilizzare come criterio per la condizione. L’icona “i” accanto a un attributo fornisce informazioni sulla tabella in cui è memorizzato e sul relativo tipo di dati.

   ![immagine che mostra la selezione di un attributo](assets/rule-builder-select-attribute.png)

   >[!NOTE]
   >
   >Il pulsante **Modifica espressione** consente di sfruttare l’editor di espressioni per definire manualmente un’espressione utilizzando i campi dal database e le funzioni helper. [Scopri come modificare le espressioni](../orchestrated/edit-expressions.md)

1. Fai clic sul pulsante ![ immagine che mostra il pulsante Altre azioni](assets/do-not-localize/rule-builder-icon-more.svg) accanto a un attributo per accedere a queste opzioni aggiuntive:

   +++ Distribuzione dei valori

   Analizza la distribuzione dei valori per un determinato attributo all’interno della tabella. Questa funzione è utile per comprendere i valori disponibili, i relativi conteggi e le percentuali. Consente inoltre di evitare problemi come l’utilizzo incoerente delle maiuscole o ortografia errata durante la creazione di query o di espressioni.

   Per gli attributi con un numero elevato di valori, lo strumento mostra solo i primi venti. In questi casi, viene visualizzata la notifica **[!UICONTROL Caricamento parziale]** per indicare questa limitazione. Puoi applicare filtri avanzati per perfezionare i risultati visualizzati e concentrarti su valori o sottoinsiemi di dati specifici.

   ![immagine che mostra l’interfaccia Distribuzione dei valori](assets/rule-builder-distribution-values.png)

   +++

   +++ Aggiungere ai preferiti

   L’aggiunta di attributi al menu dei preferiti consente di accedere rapidamente agli attributi utilizzati con maggiore frequenza. Puoi aggiungere fino a 20 attributi preferiti. Gli attributi preferiti e recenti sono associati a ogni utente all’interno di un’organizzazione, garantendo l’accessibilità tra computer diversi e fornendo un’esperienza fluida tra i dispositivi.

   Per accedere agli attributi preferiti, utilizza il menu **[!UICONTROL Preferiti e recenti]**. Per trovare più facilmente gli attributi necessari, sono elencati per primi gli attributi preferiti, seguiti da quelli utilizzati di recente. Per rimuovere un attributo dai preferiti, seleziona di nuovo l’icona a forma di stella.

   ![immagine che mostra l’interfaccia dei preferiti](assets/rule-builder-favorites.png)

   +++

1. Fai clic su **[!UICONTROL Conferma]** per aggiungere l’attributo selezionato alla condizione.

1. Viene visualizzato un riquadro delle proprietà in cui è possibile configurare il valore desiderato per l’attributo.

   ![immagine che mostra il generatore di regole con una condizione aggiunta](assets/rule-builder-condition.png)

1. Seleziona l’**[!UICONTROL operatore]** da applicare dall’elenco a discesa. Sono disponibili diversi operatori da utilizzare. Gli operatori disponibili nell’elenco a discesa dipendono dal tipo di dati dell’attributo.

   +++Elenco degli operatori disponibili

   | Operatore | Scopo | Esempio |
   |---|---|---|
   | Uguale a | Restituisce un risultato identico ai dati immessi nella seconda colonna Valore. | Cognome (@lastName) uguale a “Jones”, restituirà solo i destinatari il cui cognome è Jones. |
   | Non uguale a | Restituisce tutti i valori non identici al valore inserito. | Lingua (@language) non uguale a “Inglese” |
   | Maggiore di | Restituisce un valore maggiore del valore immesso. | Età (@age) maggiore di 50 anni, restituirà tutti i valori maggiori di “50”, ovvero “51”, “52”, ecc. |
   | Minore di | Restituisce un valore minore del valore immesso. | Data di creazione (@created) prima di “DaysAgo(100)”, restituirà tutti i destinatari creati meno di 100 giorni fa. |
   | Maggiore o uguale a | Restituisce tutti i valori uguali o maggiori del valore immesso. | Età (@age) maggiore o uguale a “30”, restituirà tutti i destinatari con un’età pari o superiore ai 30 anni. |
   | Minore o uguale a | Restituisce tutti i valori uguali o inferiori al valore immesso. | Età (@age) minore o uguale a “60”, restituirà tutti i destinatari di età uguale o inferiore ai 60 anni. |
   | Incluso in | Restituisce i risultati inclusi nei valori indicati. Questi valori devono essere separati da una virgola. | La data di nascita (@birthDate) inclusa in “10/12/1979,10/12/1984” restituirà i destinatari nati nell’intervallo tra queste date. |
   | Non in | Funziona come l’operatore Incluso in. Qui, i destinatari vengono esclusi in base ai valori immessi. | La data di nascita (@birthDate) non è inclusa in “10/12/1979,10/12/1984”. I destinatari nati in queste date non verranno restituiti. |
   | È vuoto | Restituisce risultati che corrispondono a un valore vuoto nella seconda colonna Valore. | Cellulare (@mobilePhone) è vuoto restituisce tutti i destinatari che non hanno un numero di cellulare. |
   | Non è vuoto | Funziona in modo inverso rispetto all’operatore È vuoto. Non è necessario immettere dati nella seconda colonna Valore. | Il campo E-mail (@email) non è vuoto. |
   | Inizia con | Restituisce i risultati a partire dal valore immesso. | Account # (@account) inizia con “32010”. |
   | Non inizia con | Restituisce i risultati che non iniziano con il valore immesso | Account # (@account) non inizia con “20”. |
   | Contiene | Restituisce i risultati che contengono almeno il valore immesso. | Il dominio e-mail (@domain) che contiene “mail”, restituirà tutti i nomi di dominio che contengono “mail”, come “gmail.com”. |
   | Non contiene | Restituisce risultati che non contengono il valore immesso. | Il dominio e-mail (@domain) non contiene “vo”. I nomi di dominio contenenti “vo”, ad esempio “voilà.fr”, non verranno visualizzati nei risultati. |
   | Simile a | Simile all’operatore Contiene, consente di inserire un carattere jolly % nel valore. | Cognome (@lastName) simile a “Jon%s”. Il carattere jolly funge da “jolly” per trovare nomi come “Jones”. |
   | Diverso da | Simile all’operatore Contiene, consente di inserire un carattere jolly % nel valore. | Cognome (@lastName) diverso da “Smi%h”. I destinatari con il cognome “Smith” non verranno restituiti. |

   +++

1. Nel campo **Valore**, definisci il valore previsto. Puoi anche sfruttare l’editor di espressioni per definire manualmente un’espressione utilizzando i campi dal database e le funzioni helper. A tale scopo, fai clic sull’![immagine che mostra l’icona dell’editor di espressioni](assets/do-not-localize/rule-builder-icon-editor.svg). [Scopri come modificare le espressioni](../orchestrated/edit-expressions.md)

   Per gli attributi di tipo data, i valori predefiniti sono disponibili utilizzando l’opzione **[!UICONTROL Predefiniti]**.

   +++Vedi esempio

   ![immagine che mostra l’opzione predefinita](assets/rule-builder-attribute-preset.png)

   +++

### Condizioni personalizzate per tabelle collegate (collegamenti 1-1 e 1-N){#links}

Le condizioni personalizzate consentono di eseguire query sulle tabelle collegate alla tabella attualmente utilizzata dalla regola. Questo include tabelle con un collegamento di cardinalità 1-1 o tabelle di raccolta (collegamento 1-N).

Per un collegamento **1-1**, passa alla tabella collegata, seleziona l’attributo desiderato e definisci il valore previsto.

Puoi anche selezionare direttamente un collegamento alla tabella nel selettore **Valore** e confermare. In tal caso, i valori disponibili per la tabella selezionata devono essere selezionati utilizzando un selettore dedicato, come illustrato nell’esempio seguente.

+++Esempio di query

Qui, la query esegue il targeting dei brand la cui etichetta è “in esecuzione”.

1. Naviga nella tabella **Brand** e seleziona l’attributo **Etichetta**.

   ![Schermata della tabella dei brand](assets/rule-builder-1-1-attribute.png)

1. Definisci il valore previsto per l’attributo.

   ![Schermata della tabella dei brand](assets/rule-builder-1-1-attribute-value.png)

Di seguito è riportato un esempio di query in cui è stato selezionato direttamente un collegamento di tabella. I valori disponibili per questa tabella devono essere selezionati da un selettore dedicato.

![Schermata della tabella Brand](assets/rule-builder-1-1-attribute-table.png)

+++ 

Per un **collegamento 1-N**, puoi definire le condizioni secondarie per perfezionare la query, come illustrato nell’esempio seguente.

+++Esempio di query

In questo caso, la query ha come targeting destinatari che hanno effettuato acquisti relativi al prodotto BrewMaster, per un importo totale di almeno 100 $.

1. Seleziona la tabella **Acquisti** e conferma.

1. Fai clic su **[!UICONTROL Aggiungi condizione]** per definire le condizioni secondarie da applicare alla tabella selezionata.

   ![Schermata della tabella Acquisti](assets/rule-builder-1-n-purchase.png)

1. Aggiungi condizioni secondarie in base alle tue esigenze.

   ![Schermata della tabella Acquisti](assets/rule-builder-1-n-collection.png)

+++ 

### Condizioni personalizzate con dati aggregati {#aggregate}

Le condizioni personalizzate consentono di eseguire operazioni di aggregazione. A questo scopo, è necessario selezionare direttamente un attributo da una tabella di raccolta:

1. Spostati all’interno della tabella di raccolta desiderata e seleziona l’attributo sul quale desideri eseguire un’operazione di aggregazione.

1. Nel riquadro delle proprietà, attiva l’opzione **Aggrega dati** e seleziona la funzione di aggregazione desiderata.

   ![Schermata dell’opzione Aggrega dati](assets/rule-builder-aggregate.png)

## Combinare le condizioni utilizzando gli operatori {#operators}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_querymodeler_group"
>title="Gruppo"
>abstract="In questo riquadro, puoi modificare l’operatore utilizzato per collegare insieme più condizioni di filtro."

Ogni volta che aggiungi una nuova condizione alla regola, questa viene collegata automaticamente alla condizione esistente da un operatore **AND**. Ciò significa che i risultati delle due condizioni sono combinati.

Per cambiare l’operatore tra le condizioni, fai clic su di esso e seleziona l’operatore desiderato.

![Esempio di una query](assets/rule-builder-change-operator.png)

Gli operatori disponibili sono:

* **AND (intersezione)**: combina i risultati che corrispondono a tutti i componenti di filtraggio nelle transizioni in uscita.
* **OR (Unione)**: include i risultati che corrispondono ad almeno uno dei componenti di filtraggio nelle transizioni in uscita.
* **EXCEPT (Esclusione)**: esclude i risultati che corrispondono a tutti i componenti di filtro nella transizione in uscita.

## Gestire le condizioni {#manipulate}

La barra degli strumenti dell’area di lavoro del generatore di regole fornisce opzioni per gestire facilmente le condizioni all’interno della regola:

| Icona barra degli strumenti | Descrizione |
|--- |--- |
| ![Icona Sposta in alto la selezione](assets/do-not-localize/rule-builder-icon-up.svg) | Sposta il componente in alto di una riga. |
| ![Icona Sposta in basso la selezione](assets/do-not-localize/rule-builder-icon-down.svg) | Sposta il componente in basso di una riga. |
| ![Icona Raggruppa la selezione](assets/do-not-localize/rule-builder-icon-group.svg) | Inserisce due componenti in un gruppo. |
| ![Icona Separa la selezione](assets/do-not-localize/rule-builder-icon-ungroup.svg) | Separa i componenti di un singolo gruppo. |
| ![Icona Espandi tutto](assets/do-not-localize/rule-builder-icon-expand.svg) | Espande tutti i gruppi. |
| ![Icona Comprimi tutto](assets/do-not-localize/rule-builder-icon-collapse.svg) | Comprime tutti i gruppi. |
| ![Icona Rimuovi tutto](assets/do-not-localize/rule-builder-icon-delete.svg) | Rimuove tutti i gruppi e i componenti. |

A seconda delle esigenze, potrebbe essere necessario creare gruppi intermedi di componenti raggruppando i componenti in uno stesso gruppo e collegandoli tra loro.

* Per raggruppare due condizioni esistenti, seleziona una delle due condizioni e fai clic sul pulsante ![Icona Sposta in alto la selezione](assets/do-not-localize/rule-builder-icon-up.svg) o ![Icona Sposta in basso la selezione](assets/do-not-localize/rule-builder-icon-down.svg) per raggrupparla con la condizione precedente o successiva.

* Per raggruppare una condizione esistente con una nuova, selezionala, fai clic su ![immagine che mostra il pulsante Altre azioni](assets/do-not-localize/rule-builder-icon-more.svg) e seleziona **[!UICONTROL Aggiungi gruppo]**. Seleziona il nuovo attributo da aggiungere al gruppo, quindi conferma.

  ![](assets/rule-builder-edit-groups.png)

Nell’esempio seguente, è stato creato un gruppo intermedio per il targeting di clienti che hanno acquistato il prodotto BrewMaster o VanillaVelvet.

![](assets/rule-builder-groups.png)

## Controllare e convalidare la query

>[!CONTEXTUALHELP]
>id="ajo_orchestration_querymodeler_ruleproperties"
>title="Proprietà regola"
>abstract="Dopo aver creato la query nell’area di lavoro, puoi verificarla utilizzando il riquadro **Proprietà delle regole** sul lato destro.<br/>Questo riquadro consente di visualizzare i dati risultanti, recuperare una versione del codice SQL della query e verificare il numero di record target.<br/>Utilizza il pulsante **Seleziona o salva il filtro** per salvare la query come filtro preimpostato o sostituisci il contenuto dell’area di lavoro con un filtro esistente."

Dopo aver creato la query nell’area di lavoro, puoi verificarla utilizzando il riquadro **Proprietà della regola**. Le operazioni disponibili sono:

* **Visualizza risultati:** visualizza i dati risultanti dalla query.
* **Vista codice**: visualizza una versione della query basata su codice in SQL.
* **Calcola**: aggiorna e visualizza il numero di record interessati dalla regola.
* **Seleziona o salva il filtro**: scegli un filtro preimpostato esistente da utilizzare nell’area di lavoro oppure salva la query come filtro preimpostato per riutilizzarla in futuro.

<br/>

Quando la regola è pronta, fai clic sul pulsante **[!UICONTROL Conferma]** per salvarla.

>[!IMPORTANT]
>
>Se si seleziona un filtro predefinito dal riquadro Proprietà regola, la regola creata nell’area di lavoro viene sostituita con il filtro selezionato.

