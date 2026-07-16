---
title: Helper
description: Helper
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: b08dc0f8-c85f-4aca-85eb-92dc76b0e588
feature_v2:
  - id: fda7be7c-b81e-42c0-95a9-616e5b893c03
subfeature_v2: []
source-git-commit: cfd54ee08abb8ef6dbeaeb8ca079e0d19cd329a5
workflow-type: tm+mt
source-wordcount: 1188
ht-degree: 3%

---

# Helper {#gs-helpers}

## Valore di fallback predefinito{#default-value}

L&#39;helper `Default Fallback Value` viene utilizzato per restituire un valore di fallback predefinito se un attributo è vuoto o nullo. Questo meccanismo funziona per gli attributi del profilo e gli eventi di Percorso.

**Sintassi**

```sql
Hello {%=profile.personalEmail.name.firstName ?: "there" %}!
```

In questo esempio, il valore `there` viene visualizzato se l&#39;attributo `firstName` di questo profilo è vuoto o nullo.

## Condizioni{#if-function}

L&#39;helper `if` viene utilizzato per definire un blocco condizionale.
Se la valutazione dell’espressione restituisce true, il blocco viene renderizzato, altrimenti viene saltato.

**Sintassi**

```sql
{%#if contains(profile.personalEmail.address, ".edu")%}
<a href="https://www.adobe.com/academia">Check out this link</a>
```

Dopo l&#39;helper `if`, è possibile immettere un&#39;istruzione `else` per specificare un blocco di codice da eseguire, se la stessa condizione è false.
L&#39;istruzione `elseif` specificherà una nuova condizione da verificare se la prima istruzione restituisce false.


**Formato**

```sql
{
    {
        {%#if condition1%} element_1 
        {%else if condition2%} element_2 
        {%else%} default_element 
        {%/if%}
    }
}
```

**Esempi**

1. **Eseguire il rendering di collegamenti archivio diversi in base alle espressioni condizionali**

   ```sql
   {%#if profile.homeAddress.countryCode = "FR"%}
   <a href="https://www.somedomain.com/fr">Consultez notre catalogue</a>
   {%else%}
   <a href="https://www.somedomain.com/en">Checkout our catalog</a>
   {%/if%}
   ```

1. **Determinare l&#39;estensione dell&#39;indirizzo di posta elettronica**

   ```sql
   {%#if contains(profile.personalEmail.address, ".edu")%}
   <a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
   {%else if contains(profile.personalEmail.address, ".org")%}
   <a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
   {%else%}
   <a href="https://www.adobe.com/users">Checkout our page</a>
   {%/if%}
   ```

1. **Aggiungere un collegamento condizionale**

   La seguente operazione aggiungerà un collegamento al sito Web &quot;www.adobe.com/academia&#39;&quot; solo per i profili con indirizzi e-mail &quot;edu&quot;, al sito Web &quot;www.adobe.com/org&#39;&quot; per i profili con indirizzi e-mail &quot;org&quot; e all’URL predefinito &quot;www.adobe.com/users&#39;&quot; per tutti gli altri profili:

   ```sql
   {%#if contains(profile.personalEmail.address, ".edu")%}
   <a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
   {%else if contains(profile.personalEmail.address, ".org")%}
   <a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
   {%else%}
   <a href="https://www.adobe.com/users">Checkout our page</a>
   {%/if%}
   ```

1. **Contenuto condizionale basato sull&#39;appartenenza al pubblico**

   ```sql
   {%#if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8b").status = "existing"%}
   Hi! Esteemed gold member. <a href="https://www.somedomain.com/gold">Checkout your exclusive perks </a>
   {%else if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8c").status = "existing"%}
   Hi! Esteemed silver member. <a href="https://www.somedomain.com/silver">Checkout your exclusive perks </a>
   {%/if%}
   ```

>[!NOTE]
>
>Per ulteriori informazioni sui tipi di pubblico e sul servizio di segmentazione, consulta [questa sezione](../../audience/about-audiences.md).


## A meno che{#unless}

L&#39;helper `unless` viene utilizzato per definire un blocco condizionale. In opposizione all&#39;helper `if`, se la valutazione dell&#39;espressione restituisce false, viene eseguito il rendering del blocco.

**Sintassi**

```sql
{%#unless unlessCondition%} element_1 {%else%} default_element {%/unless%}
```

**Esempio**

Esegui il rendering di alcuni contenuti in base all’estensione dell’indirizzo e-mail:

```sql
{%#unless endsWith(profile.personalEmail.address, ".edu")%}
Some Normal Content
{%else%}
Some edu specific content
{%/unless%}
```

## Ogni{#each}

L&#39;helper `each` viene utilizzato per eseguire l&#39;iterazione su un array.
La sintassi dell&#39;helper è `{{#each ArrayName}}` YourContent `{{/each}}`.
È possibile fare riferimento ai singoli elementi array utilizzando la parola chiave **this** all&#39;interno del blocco. È possibile eseguire il rendering dell&#39;indice dell&#39;elemento dell&#39;array utilizzando `{{@index}}`.

**Sintassi**

```sql
{{#each profile.productsInCart}}
    <li>{{this.name}}</li>
{{/each}}
```

**Esempio**

```sql
{{#each profile.homeAddress.city}}
  {{@index}} : {{this}}<br>
{{/each}}
```

**Esempio**

Esegui il rendering di un elenco di prodotti che questo utente ha nel carrello:

```sql
{{#each profile.products as |product|}}
    <li>{{product.productName}} {{product.productRating}}</li>
{{/each}}
```

>[!NOTE]
>
>È inoltre possibile utilizzare l&#39;helper `each` per eseguire iterazioni sulle matrici restituite dalle risposte alle azioni personalizzate. Per un esempio di iterazione su array nidificati da una risposta di azione personalizzata, vedere [Utilizzo di risposte di azione personalizzate nei canali nativi](../../action/action-response.md#response-in-channels).

## Con{#with}

L&#39;helper `with` viene utilizzato per modificare il token di valutazione della parte modello.

**Sintassi**

```sql
{{#with profile.person.name}}
{{this.firstName}} {{this.lastName}}
{{/with}}
```

L&#39;helper `with` è utile anche per definire una variabile di collegamento.

**Esempio**

Da utilizzare con per l’aliasing di nomi di variabili lunghi a nomi più brevi:

```sql
{{#with profile.person.name as |name|}}
 Hi {{name.firstName}} {{name.lastName}}!
 Checkout our trending products for today!
{{/with}}
```

## Let{#let}

La funzione `let` consente di archiviare un&#39;espressione come variabile da utilizzare successivamente in una query.

**Sintassi**

```sql
{% let variable = expression %} {{variable}}
```

**Esempio**

L&#39;esempio seguente consente di calcolare la somma totale dei prezzi dei prodotti nel carrello con prezzi compresi tra 100 e 1000.

```sql
{% let sum = 0%}
    {{#each profile.productsInCart as |p|}}
        {%#if p.price>100 and p.price<1000%}
            {%let sum = sum + p.price %}
        {%/if%}
    {{/each}}
{{sum}}
```

## Url {#url}

L&#39;helper `url` viene utilizzato per tenere traccia dei collegamenti, ridurre gli URL e inserire [collegamenti profondi](../../email/deeplinks.md) nel contenuto dei messaggi SMS.

**Sintassi**

```sql
{{url originalUrl='<your_url>' type='<DEEPLINK>' action='CLICK'}}
```

**Parametri**

| Parametro | Descrizione |
|---|---|
| `originalUrl` | L’URL da ridurre. |
| `type` | Il tipo di collegamento. Utilizza `DEEPLINK` per aprire una schermata specifica in un&#39;app mobile. |
| `action` | Azione di tracciamento. Utilizza `CLICK` per tenere traccia dei clic sul collegamento. |

**Esempio**

```sql
  {{url originalUrl='https://www.mybusiness.com/offers/summer-sale' type='DEEPLINK' action='CLICK'}}
```

## Ricerca nei set di dati {#dataset-lookup}

>[!AVAILABILITY]
>
>Questa funzione è attualmente disponibile per tutti i clienti come versione a disponibilità limitata.
>
>Per il momento, la funzione helper `datasetLookup` può essere utilizzata all&#39;interno di frammenti di espressione per un gruppo limitato di clienti. Per potervi accedere, contatta il tuo rappresentante Adobe.

L&#39;helper `datasetLookup` recupera i dati dai set di dati dei record di Adobe Experience Platform durante la personalizzazione, in modo da poter utilizzare valori di campo non memorizzati nel profilo o nel payload dell&#39;evento.

**Sintassi**

```sql
{{datasetLookup datasetId="datasetId" id="key" result="store" required=false}}
```

Riferimento ai campi recuperati con `{{result.fieldId}}`, dove `result` è il valore passato al parametro `result`.

Per l&#39;abilitazione del set di dati, i dettagli dei parametri, gli esempi e i test, vedere [Utilizzare i dati di Adobe Experience Platform per la personalizzazione](../aep-data-perso.md).

## Metadati di esecuzione {#execution-metadata}

L&#39;helper `executionMetadata` consente di acquisire e archiviare in modo dinamico coppie chiave-valore personalizzate nel contesto di esecuzione del messaggio.

>[!NOTE]
>
>* La funzione dei metadati di esecuzione non è supportata da [azioni personalizzate](../../action/action.md) e nei canali in entrata (web, esperienza basata su codice, messaggi in-app, schede di contenuto).
>* La funzione Execution Metadata non è visibile quando viene visualizzato il contenuto stesso.

**Sintassi**

```
{{executionMetadata key="your_key" value="your_value"}}
```

In questa sintassi, `key` fa riferimento al nome dei metadati e `value` sono i metadati da mantenere.

**Caso d’uso**

Con questa funzione, puoi aggiungere informazioni contestuali a qualsiasi azione nativa delle campagne o dei percorsi. Questo consente di esportare i dati contestuali di consegna in tempo reale verso sistemi esterni per vari scopi come il tracciamento, l’analisi, la personalizzazione e l’elaborazione a valle.

Ad esempio, puoi utilizzare l’helper dei metadati di esecuzione per aggiungere un ID specifico a ciascuna consegna inviata a ciascun profilo. Queste informazioni vengono generate durante il runtime e i metadati di esecuzione arricchiti possono quindi essere esportati per la riconciliazione a valle con una piattaforma di reporting esterna.

**Come funziona**

Seleziona qualsiasi elemento dal contenuto del canale all&#39;interno di una campagna o di un percorso e, utilizzando l&#39;editor di personalizzazione, aggiungi l&#39;helper `executionMetadata` a questo elemento.


In fase di esecuzione, il valore dei metadati viene aggiunto al set di dati **[!UICONTROL Message Feedback Event]** esistente con la seguente aggiunta di schema:

```
"_experience": {
  "customerJourneyManagement": {
    "messageExecution": {
      "metadata": {
        "your_key": "your_value"
      }
    }
  }
}
```

>[!NOTE]
>
>Ulteriori informazioni sui set di dati in [questa sezione](../../data/get-started-datasets.md).

**Limitazioni**

* Puoi trasmettere un massimo di 50 coppie chiave-valore per azione.
* Il payload totale dei metadati è limitato a 2 KB per azione. Se viene superato il limite di 2 KB, il messaggio viene comunque recapitato, ma è possibile troncare qualsiasi coppia chiave-valore.
* I metadati non vengono acquisiti per i profili esclusi dall’azione. Quando un profilo viene escluso dalla ricezione di un messaggio, non viene creata alcuna voce di metadati per tale profilo nel set di dati.

**Esempio**

```
{{executionMetadata key="firstName" value=profile.person.name.firstName}}
```

In questo esempio, supponendo `profile.person.name.firstName` = &quot;Alex&quot;, l&#39;entità risultante è:

```
{
  "key": "firstName",
  "value": "Alex"
}
```

## Crittografa {#url-parameter-encryption-helper}

>[!AVAILABILITY]
>
>Questa funzionalità è attualmente disponibile solo per il canale e-mail.

La funzione `Encrypt` consente di crittografare qualsiasi valore di espressione al momento del rendering, in genere un attributo di profilo, un token o persino una struttura JSON stratificata creata nell&#39;espressione, prima che venga scritto in un parametro di query nei collegamenti di tracciamento o nelle pagine di destinazione.

I valori che appaiono come testo normale nell’URL (inclusi dati PII o altri dati sensibili) non sono leggibili quando il collegamento viene ispezionato o inoltrato. Solo i valori racchiusi con questo helper sono crittografati; il resto dell’URL rimane invariato.

**Caso d’uso**

Questo helper consente di proteggere i dati di profilo sensibili (PII) prima di includerli nell’output di rendering.

**Prerequisito**

Un amministratore deve creare almeno una chiave attiva nel registro delle chiavi a livello di sandbox. [Scopri come creare e gestire le chiavi](../url-parameter-encryption.md#create-keys)

>[!NOTE]
>
>L’utilizzo di una chiave revocata o altrimenti non attiva dovrebbe causare un errore di personalizzazione in fase di rendering, pertanto un messaggio non viene inviato con una chiave non valida.

**Sintassi**

```text
{{encrypt dataPath keyName="keyName" version="version" result="variableName"}}
```

**Utilizzo**

Questo helper crittografa i dati sensibili e memorizza il risultato in una variabile di modello. <!--The encryption is performed using the AES-256-GCM algorithm.-->

Puoi applicare l’helper a uno, più o tutti i parametri di un collegamento, a seconda della progettazione dell’URL e dei vincoli di lunghezza.

* **Input**: `dataPath` (riferimento dati che deve essere risolto in una stringa), `keyName` (identificatore chiave di crittografia), `version` (versione chiave opzionale), `result` (nome variabile per output crittografato)
* **Output**: rende disponibile il valore crittografato nella variabile `result` specificata.
* **Formato risultato**: la variabile risultato contiene una stringa separata da punti: `keyName.version.nonce.authTag.cipherText` (tutti i segmenti tranne `keyName` e `version` sono codificati con URL Base64 senza spaziatura interna).
* **Requisiti chiave statica**: `keyName` e `version` devono essere valori letterali stringa statici (i riferimenti dinamici non sono supportati).
* **Versione predefinita**: il parametro `version` è facoltativo. Se omesso, il servizio della chiave di crittografia risolve la versione predefinita

**Esempi**

| Espressione di esempio | Risultato |
| --- | --- |
| `{{encrypt profile.person.email keyName="email-key" version="1" result="enc"}}{{enc}}` | `email-key.1.RkFrZU5vbmNlQUJD.T3V0cHV0QXV0aFRhZ0Fh.am9obkBleGFtcGxlLmNvbQ` |
| `{{encrypt profile.person.name.firstName keyName="pii-key" version="2" result="encName"}}{{encName}}` | `pii-key.2.U29tZVJhbmRvbUlW.QXV0aGVudGljYXRpb25UYQ.Sm9obg` |

**Guardrail**

* La decrittografia viene gestita all&#39;esterno di [!DNL Journey Optimizer] nelle pagine di destinazione, nelle app o nelle API. Pianifica il ciclo di vita e la rotazione delle chiavi con il team di sicurezza, in modo che i payload storici possano essere decrittografati laddove necessario.

* Le chiavi revocate non devono essere utilizzate per la nuova crittografia. Seguire i criteri di sicurezza per la rotazione e lo smantellamento.

* Il processo di crittografia richiede molte risorse e l&#39;utilizzo della funzione `Encrypt` può influire sulla velocità effettiva al momento del rendering.

