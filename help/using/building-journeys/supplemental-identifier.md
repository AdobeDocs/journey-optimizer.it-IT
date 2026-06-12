---
title: Utilizzare identificatori supplementari nei percorsi
description: Scopri come utilizzare gli identificatori supplementari nei percorsi.
exl-id: f6ebd706-4402-448a-a538-e9a4c2cf0f8b
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/ABOlJ-ZF0a3xLNY-hH6jjFqu53ph4PynNalGkgQ6P8k
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: d08afb72-92f6-4856-88e3-11ec34313c2f
  - id: fa683eda-48de-4558-af32-2673edcd44fe
topic_v2:
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 02ce60020012083981c5599789b9e86804190627
workflow-type: tm+mt
source-wordcount: 2009
ht-degree: 2%

---

# Utilizzare identificatori supplementari nei percorsi {#supplemental-id}

>[!CONTEXTUALHELP]
>id="ajo_journey_parameters_supplemental_identifier"
>title="Usare un identificatore supplementare"
>abstract="L’identificatore supplementare è un identificatore secondario che fornisce contesto aggiuntivo per l’esecuzione di un percorso. Per definirlo, seleziona qualsiasi attributo non di identità (o identità non di persona) dal pubblico o dall’evento da utilizzare come identificatore supplementare."

<table style="border-collapse: collapse; width: 100%;">
  <tr>
    <td style="vertical-align: top; padding-right: 20px; border: none;">
      <p>Per impostazione predefinita, i percorsi vengono eseguiti nel contesto di un <b>ID profilo</b>. Questo significa che, se il profilo è attivo in un dato percorso, non potrà rientrare in un altro percorso. Per evitare questo problema, Journey Optimizer consente di acquisire un <b>identificatore supplementare</b>, ad esempio un ID ordine, un ID abbonamento, un ID prescrizione, oltre all'ID profilo.  
      <p>In questo esempio, è stato aggiunto un <b>ID prenotazione</b> come identificatore supplementare.</p>
      <p>In questo modo, i percorsi vengono eseguiti nel contesto dell’ID profilo associato all’identificatore supplementare (in questo caso, l’ID prenotazione). Viene eseguita un’istanza del percorso per ogni iterazione dell’identificatore supplementare. Questo consente più ingressi dello stesso ID profilo nei percorsi se sono state effettuate prenotazioni diverse.</p>
      <p>Inoltre, Journey Optimizer consente di sfruttare gli attributi dell’identificatore supplementare (ad esempio, numero di prenotazione, data di rinnovo della prescrizione, tipo di prodotto) per la personalizzazione dei messaggi, garantendo comunicazioni altamente pertinenti.</p>
    </td>
    <td style="vertical-align: top; border: none; text-align: center; width: 40%;">
      <img src="assets/event-supplemental-id.png" alt="Esempio di identificatore supplementare" style="max-width:100%;" />
    </td>
  </tr>
</table>

➡️ [Scopri questa funzione nel video](#video)

## Guardrail e limitazioni {#guardrails}

* **percorsi supportati**: sono supportati identificatori supplementari per **percorsi attivati da eventi** e **di pubblico di lettura**. Sono **non supportati** per i percorsi di qualificazione del pubblico (ovvero, percorsi che iniziano con un&#39;attività di qualificazione del pubblico).

* **Azioni in entrata**: gli identificatori supplementari non sono attualmente supportati per le azioni in entrata, ad esempio in-app e web.

* **Limiti di istanze simultanee**: i profili non possono avere più di 10 istanze di percorso simultanee.

* **Tipo di dati e struttura dello schema**: l&#39;identificatore supplementare deve essere di tipo `string`. Può essere un attributo di stringa indipendente oppure un attributo di stringa all&#39;interno di una matrice di oggetti. L&#39;attributo di stringa indipendente darà luogo a una singola istanza di percorso, mentre l&#39;attributo di stringa all&#39;interno di una matrice di oggetti darà luogo a un&#39;istanza di percorso univoca per iterazione della matrice di oggetti. Gli array di stringhe e le mappe non sono supportati.

* **Rientro Percorso**

  Il comportamento di rientro percorso con identificatori supplementari segue la politica di rientro esistente:

   * Se il percorso non è un rientro, la stessa combinazione di ID profilo + ID supplementare non può rientrare nel percorso.
   * Se il percorso è rientro con una finestra temporale, la stessa combinazione di ID profilo + ID supplementare può essere reinserita dopo la finestra temporale definita.

* **Etichettatura e applicazione uso dati (DULE)** - Nessun controllo di convalida DULE eseguito sull&#39;ID supplementare. Questo significa che questo attributo non verrà considerato quando il percorso cerca violazioni dei criteri di governance dei dati.

* **Configurazione eventi downstream**

  Se utilizzi un altro evento a valle nel percorso, questo deve utilizzare lo stesso ID supplementare e avere lo stesso ID spazio dei nomi.

* **Leggi percorsi di pubblico**

   * **Eventi di business**: l&#39;ID supplementare è disabilitato se si utilizza un evento di business.
   * **Campi evento e contesto**: l&#39;identificatore supplementare non deve provenire da un campo contesto evento o percorso.
   * **Selezione attributo**: qualsiasi attributo non di identità (o identità non di persona) può essere utilizzato come ID supplementare, per tutti i tipi di pubblico (Servizio profilo unificato, importazione CSV e Composizione pubblico federato). Gli attributi di identità basati su persona non sono consentiti. Per i tipi di pubblico esterni, vedi [Identificatori supplementari con tipi di pubblico esterni](#external-audiences) per i modelli di dati supportati e i requisiti di configurazione.
   * **Frequenza di lettura**: per percorsi di pubblico di lettura che utilizzano un campo ID supplementare di tipo array, la frequenza di lettura dell&#39;attività Read audience è limitata a un massimo di 500 profili al secondo.

## Comportamento dei criteri di uscita con ID supplementari {#exit-criteria}

Precondizione: Percorso abilitato per l’ID supplementare (tramite attività evento unitario o attività di lettura del pubblico)

La tabella seguente spiega il comportamento dei profili in un percorso supplementare abilitato per gli ID quando è configurato il criterio di uscita:

| Configurazione criteri di uscita | Comportamento quando vengono soddisfatti i criteri di uscita |
| ---------------------------- | ---------------------------------- |
| Basato su un evento ID non supplementare | Tutte le istanze del profilo corrispondente nel percorso sono chiuse. |
| In base a un evento ID supplementare <br/>*Nota: lo spazio dei nomi ID supplementare deve corrispondere a quello del nodo iniziale.* | Viene chiusa solo l’istanza di profilo + ID supplementare corrispondente. |
| In base a un pubblico | Tutte le istanze del profilo corrispondente nel percorso sono chiuse. |

## Aggiungere un identificatore supplementare e sfruttarlo in un percorso {#add}

>[!BEGINTABS]

>[!TAB percorso attivato da eventi]

Per utilizzare un identificatore supplementare in un percorso attivato da un evento, effettua le seguenti operazioni:

1. **Aggiungi l&#39;ID supplementare all&#39;evento**

   1. Crea o modifica l’evento desiderato. [Scopri come configurare un evento unitario](../event/about-creating.md)

   1. Nella schermata di configurazione dell&#39;evento, selezionare l&#39;opzione **[!UICONTROL Usa identificatore supplementare]**.

      ![Configurazione evento con opzione identificatore supplementare](assets/supplemental-ID-event.png)

   1. Utilizza l’editor espressioni per selezionare il campo da utilizzare come ID supplementare (ad esempio, ID prenotazione, ID abbonamento).

      >[!NOTE]
      >
      >Assicurarsi di utilizzare l&#39;editor espressioni in **[!UICONTROL modalità avanzata]** per selezionare l&#39;attributo.

1. **Aggiungi l&#39;evento al percorso**

   Trascina l’evento configurato nell’area di lavoro del percorso. Attiva la voce percorso in base sia all’ID profilo che all’ID supplementare.

   ![Percorso con identificatore supplementare per attivazione evento](assets/supplemental-ID-journey.png)

>[!TAB Leggi percorso di destinatari]

Per utilizzare un identificatore supplementare in un percorso Read audience, effettua le seguenti operazioni:

1. **Aggiungi e configura un&#39;attività Read audience nel percorso**

   1. Trascina nel percorso un&#39;attività **[!UICONTROL Read audience]**.

   1. Nel riquadro delle proprietà dell&#39;attività attivare l&#39;opzione **[!UICONTROL Usa identificatore supplementare]**.

      ![Attività di lettura del pubblico con configurazione dell&#39;identificatore supplementare](assets/supplemental-ID-read-audience.png)

   1. Nel campo **[!UICONTROL Identificatore supplementare]**, utilizzare l&#39;editor espressioni per selezionare l&#39;attributo dell&#39;identificatore supplementare.

   Per i tipi di pubblico [importati da un file CSV](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html?lang=it#import-audience){target="_blank"}, se il pubblico CSV contiene più righe per ID profilo, assicurati che Attivazione rapida sia prima abilitata. Consulta [Identificatori supplementari con tipi di pubblico esterni](#external-audiences).

       >[!NOTE]
       >
       >Assicurati di utilizzare l&#39;editor espressioni in **[!UICONTROL Modalità avanzata]** per selezionare l&#39;attributo.
   
>[!ENDTABS]

## Utilizzo degli attributi ID supplementari

Utilizza l’editor di espressioni e l’editor di personalizzazione per fare riferimento agli attributi dell’identificatore supplementare per la personalizzazione o la logica condizionale. Gli attributi sono accessibili dal menu **[!UICONTROL Attributi contestuali]**.

![Editor Personalization che mostra i campi dell&#39;identificatore supplementare per il contenuto](assets/supplemental-ID-perso.png)

Per i percorsi attivati da eventi se si utilizzano array (ad esempio, più prescrizioni o criteri), utilizzare una formula per estrarre elementi specifici.

+++ Vedi esempi

In un array di oggetti con ID supplementare come `bookingNum` e un attributo allo stesso livello denominato `bookingCountry`, il percorso eseguirà un&#39;iterazione nell&#39;oggetto array in base al bookingNum e creerà un&#39;istanza di percorso per ogni oggetto.

* L&#39;espressione seguente nell&#39;attività condizione eseguirà un&#39;iterazione nella matrice di oggetti e verificherà se il valore di `bookingCountry` è uguale a &quot;FR&quot;:

  ```
  @event{<event_name>.<object_path>.<object_array_name>.all(currentEventField.<attribute_path>.bookingNum==${supplementalId}).at(0).<attribute_path>.bookingCountry}=="FR"
  ```

* L&#39;espressione seguente nell&#39;editor di personalizzazione e-mail eseguirà un&#39;iterazione nell&#39;array di oggetti, estrae `bookingCountry` applicabile all&#39;istanza di percorso corrente e lo visualizza nel contenuto:

  ```
  {{#each context.journey.events.<event_ID>.<object_path>.<object_array_name> as |l|}} 
  
  {%#if l.<attribute_path>.bookingNum = context.journey.technicalProperties.supplementalId%} {{l.<attribute_path>.bookingCountry}}  {%/if%}
  
  {{/each}}
  ```

* Esempio dell’evento utilizzato per attivare il percorso:

  ```
  "bookingList": [
        {
            "bookingInfo": {
                "bookingNum": "x1",
                      "bookingCountry": "US"
            }
        },
        {
            "bookingInfo": {
                "bookingNum": "x2",
                "bookingCountry": "FR"
            }
        }
    ]
  ```

+++

## ID supplementare e arbitrato di percorso {#arbitration}

L&#39;arbitrato di percorso (inclusi i limiti di concorrenza e il conteggio delle voci all&#39;interno dei set di regole) funziona a livello di ID profilo, non a livello di coppia (ID profilo, ID supplementare). Ciò significa che un limite di concorrenza pari a 1 può bloccare una seconda istanza di percorso per lo stesso profilo anche quando presenta un diverso valore ID supplementare.

Contatta il tuo rappresentante Adobe per indicazioni sul comportamento di arbitrato prima di affidarti a specifiche impostazioni di arbitrato in produzione.

**Documentazione correlata:**

* [Limitazione del percorso e arbitrato](../conflict-prioritization/journey-capping.md)
* [Utilizzare i set di regole](../conflict-prioritization/rule-sets.md)
* [Gestione dei conflitti e assegnazione delle priorità](../conflict-prioritization/gs-conflict-prioritization.md)

## Identificatori supplementari con pubblico esterno {#external-audiences}

L&#39;ID supplementare è supportato per i tipi di pubblico esterni, inclusi i tipi di pubblico [importati da un file CSV](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html?lang=it#import-audience){target="_blank"} e quelli creati con [Federated Audience Composition](../audience/get-started-audience-orchestration.md). Quando configuri un percorso che legge da un pubblico di tipo CSV o Federated Audience Composition, puoi designare qualsiasi attributo non di identità in tale pubblico come ID supplementare. Journey Optimizer crea quindi un’istanza di percorso separata per ogni combinazione di profilo univoco + ID supplementare.

* Caso d’uso 1: una riga per profilo univoco + coppia di ID supplementare

  Questo è il caso d’uso principale per i tipi di pubblico CSV e Federated Audience Composition. Il pubblico contiene più righe in cui ogni riga rappresenta una combinazione univoca di un profilo (ad esempio, un cliente) e un ID supplementare (ad esempio, un account o un ID ordine). Ogni riga viene considerata come record di attivazione indipendente.

  | profile_id | account_id *(ID supplementare)* | other_attributes |
  | --- | --- | --- |
  | customer_001 | ACC-1001 | ... |
  | customer_001 | ACC-1002 | ... |
  | customer_002 | ACC-2001 | ... |

  In questo esempio, `customer_001` ha due account. Journey Optimizer crea un&#39;istanza di percorso separata per ogni coppia univoca di profilo + `account_id`.

* Caso d’uso 2: una riga per profilo con un array di ID supplementari

  Questo caso d’uso è disponibile per i tipi di pubblico che supportano gli array. Una singola riga del pubblico contiene un profilo con un attributo array contenente più valori ID supplementari. Journey Optimizer crea un’istanza di percorso per valore nell’array.

  | profile_id | account_ids *(array, ID supplementare)* | other_attributes |
  | --- | --- | --- |
  | customer_001 | [ACC-1001, ACC-1002] | ... |
  | customer_002 | [ACC-2001] | ... |

  In questo esempio, Journey Optimizer genera due istanze di percorso per `customer_001` (una per ID account) e una per `customer_002`. Questo si comporta in modo coerente con il funzionamento dell’ID supplementare per i tipi di pubblico del servizio Unified Profile.

### Come configurare {#external-configuration}

Per i tipi di pubblico CSV che utilizzano il caso d’uso 1 (in cui il pubblico contiene intenzionalmente più righe per lo stesso ID profilo) è necessario abilitare la funzione Attivazione rapida prima di configurare il percorso. Consulta i prerequisiti di seguito. Per tutti gli altri casi, configura direttamente il percorso.

+++ Prerequisito: abilitare l’attivazione rapida sui tipi di pubblico CSV tramite API

>[!IMPORTANT]
>
>Questo prerequisito si applica solo ai tipi di pubblico CSV in cui il pubblico contiene intenzionalmente più righe per lo stesso ID profilo (Caso d’uso 1). I tipi di pubblico con Composizione del pubblico federato hanno l’attivazione rapida abilitata per impostazione predefinita e non richiedono questo passaggio. L&#39;interfaccia utente di Audience Portal non supporta l&#39;impostazione di `expressActivation`. È necessario utilizzare l&#39;API del pubblico esterno.

Abilitare `expressActivation` sul pubblico al momento della creazione. Questo comunica a Journey Optimizer di attivare ogni record in modo indipendente, senza deduplicazione per ID profilo. Questo flag non può essere modificato dopo la creazione del pubblico.

Utilizza la seguente chiamata API durante la creazione del pubblico:

Endpoint:

```http
POST https://platform.adobe.io/data/core/ais/external-audience
```

Intestazioni richieste:

```http
Authorization: Bearer {ACCESS_TOKEN}
Content-Type: application/json
x-api-key: {API_KEY}
x-gw-ims-org-id: {IMS_ORG}
x-sandbox-name: {SANDBOX_NAME}
```

Corpo della richiesta (set `expressActivation: true`):

```json
{
  "name": "my_audience_name",
  "fields": [ ... ],
  "sourceSpec": { ... },
  "audienceType": "people",
  "namespace": "CustomerAudienceUpload",
  "expressActivation": true
}
```

>[!NOTE]
>
>`expressActivation` utilizza `false` per impostazione predefinita. Deve essere impostato al momento della creazione del pubblico e non può essere modificato dopo la creazione. Per impostazione predefinita, per tutti i tipi di pubblico di Federated Audience Composition è abilitata l’attivazione rapida e non è necessario questo flag.

Consulta la [documentazione di creazione API per pubblico esterno](https://experienceleague.adobe.com/it/docs/experience-platform/segmentation/tutorials/create-external-audience#create){target="_blank"} per il riferimento completo.

+++

Per configurare il percorso:

1. Aprire o creare un percorso con un nodo **[!UICONTROL Read audience]**.
1. Nelle impostazioni del nodo **[!UICONTROL Read audience]**, seleziona il pubblico CSV o Federated Audience Composition.
1. Attiva l&#39;opzione **[!UICONTROL Usa identificatore supplementare]**, quindi nel campo **[!UICONTROL Identificatore supplementare]** utilizza l&#39;editor espressioni in **[!UICONTROL Modalità avanzata]** per scegliere l&#39;attributo da utilizzare come identificatore secondario (ad esempio, `account_id`, `order_number`).
1. L’attributo selezionato viene trattato come ID supplementare per il percorso; non è richiesta alcuna registrazione di identità.

### Comportamento di deduplicazione {#external-dedup}

Quando per un pubblico è abilitata l’attivazione rapida (sempre true per Federated Audience Composition, deve essere impostata in modo esplicito per CSV), Journey Optimizer gestisce la deduplicazione in base alla configurazione del percorso:

| Scenario | Esempio di righe di pubblico | Comportamento |
| --- | --- | --- |
| **Percorso con ID supplementare — nessuna coppia duplicata (ID profilo, ID supplementare)** | (P1, S1), (P1, S2) | Caso d’uso previsto. Journey Optimizer crea un’istanza di percorso separata per ogni combinazione di profilo univoco + ID supplementare. Tutte le righe sono ammesse. |
| **Percorso con ID supplementare. Sono presenti coppie duplicate (ID profilo, ID supplementare)** | (P1, S1), (P1, S1), (P1, S2) | Le righe che condividono la stessa combinazione (ID profilo, ID supplementare) vengono escluse dalla normale logica di rientro del percorso. È ammessa solo la prima riga corrispondente per combinazione univoca. |
| **Percorso senza ID supplementare configurato** | (P1, S1), (P1, S2) | Senza un ID supplementare, Journey Optimizer tratta tutte le righe per lo stesso ID profilo come se si trattasse dello stesso profilo. È ammessa una sola istanza di percorso per ID profilo; le righe aggiuntive per lo stesso profilo vengono eliminate. |

## Casi d’uso di esempio

Questi esempi mostrano come gli identificatori supplementari supportano più record correlati.

### **Notifiche di rinnovo dei criteri**

* **Scenario**: un provider di assicurazioni invia promemoria di rinnovo per ogni polizza attiva detenuta da un cliente.
* **Esecuzione**:
   * Voce principale: John.
   * ID supplementari: `"AutoPolicy123", "HomePolicy456"`.
   * Il percorso viene eseguito separatamente per ogni criterio, con date di rinnovo personalizzate, dettagli sulla copertura e informazioni sui premi.

### **Gestione abbonamenti**

* **Scenario**: un servizio di sottoscrizione invia messaggi personalizzati per ogni sottoscrizione quando viene attivato un evento per tale sottoscrizione.
* **Esecuzione**:
   * Voce principale: Jane.
   * ID supplementari: `"Luma Yoga Program ", "Luma Fitness Program"`.
   * Ogni evento include un ID abbonamento e i dettagli relativi a tale abbonamento. Il percorso viene eseguito separatamente per ogni evento/abbonamento, consentendo offerte di rinnovo personalizzate per abbonamento.

### **Consigli di prodotto**

* **Scenario**: una piattaforma di e-commerce invia consigli basati su prodotti specifici acquistati da un cliente.
* **Esecuzione**:
   * Voce principale: Alex.
   * ID supplementari: `"productID1234", "productID5678"`.
   * Il percorso viene eseguito separatamente per ciascun prodotto, con opportunità di upselling personalizzate.

## Video introduttivo {#video}

Scopri come abilitare e applicare un identificatore supplementare in [!DNL Adobe Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/3464792?quality=12)
