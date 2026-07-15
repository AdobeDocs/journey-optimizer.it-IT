---
title: Ricette di personalizzazione
description: Pattern di personalizzazione comuni ed esempi reali per Adobe Journey Optimizer
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
feature_v2:
  - id: fda7be7c-b81e-42c0-95a9-616e5b893c03
subfeature_v2:
  - id: cb09dcb7-3367-4b63-b02c-8a1356eb876e
  - id: ac5d9310-7772-40fb-9d78-864562e1bfd6
source-git-commit: f552e98f370f96e9a99d2f1d604f840ac6069d65
workflow-type: tm+mt
source-wordcount: 1524
ht-degree: 0%

---

# Ricette di personalizzazione {#personalization-recipes}

>[!BEGINSHADEBOX]

**In questa pagina:** Trova ricette di personalizzazione pronte all&#39;uso per date, array, stringhe, logica condizionale e casi edge di PQL che puoi copiare direttamente nel contenuto di Adobe Journey Optimizer.

>[!ENDSHADEBOX]

Questa pagina fornisce modelli di personalizzazione pronti all’uso per i casi d’uso più comuni in Adobe Journey Optimizer. Tutti gli esempi utilizzano la sintassi dell’editor di personalizzazione e possono essere copiati direttamente nei contenuti e-mail, SMS o push.

Per un riferimento completo delle funzioni disponibili, vedere [Funzioni helper](functions/helpers.md), [Funzioni data/ora](functions/dates.md), [Funzioni stringa](functions/string.md) e [Funzioni array](functions/arrays-list.md).

>[!TIP]
>
>Prima di copiare gli esempi, controlla le [best practice per Personalization](personalization-syntax.md#best-practices) per evitare gli errori di sintassi più comuni.

## Ricette data e ora {#date-time-recipes}

### Ricetta 1 - Visualizza la data corrente in un formato leggibile {#recipe-current-date}

Utilizza `formatDate` con `getCurrentZonedDateTime()` per eseguire il rendering della data odierna in qualsiasi formato:

```sql
{%= formatDate(getCurrentZonedDateTime(), "MMMM dd, yyyy") %}
```

Output (esempio): `April 11, 2026`

**Modelli di formato comuni:**

| Pattern | Esempio di output |
|---------|---------------|
| `"dd/MM/yyyy"` | `11/04/2026` |
| `"MM/dd/yyyy"` | `04/11/2026` |
| `"EEEE, MMMM dd"` | `Saturday, April 11` |
| `"yyyy-MM-dd"` | `2026-04-11` |

>[!NOTE]
>
>Utilizzare `y` minuscolo (anno di calendario) anziché `Y` (anno basato su settimane) per evitare risultati imprevisti ai limiti dell&#39;anno. Vedi [caratteri pattern](functions/dates.md#pattern-characters) per il riferimento completo.

### Ricetta 2: conto alla rovescia per una data di scadenza o evento {#recipe-countdown}

Utilizzare `dateDiff` per calcolare il numero di giorni rimanenti fino a un attributo di data profilo, quindi eseguirne il rendering in modo dinamico:

```handlebars
{% let daysLeft = dateDiff(getCurrentZonedDateTime(), stringToDate(profile.loyalty.expiryDate)) %}
{%#if daysLeft > 0%}
Your reward points expire in {{daysLeft}} day{%#if daysLeft > 1%}s{%/if%}. Use them before they're gone!
{%else%}
Your reward points have expired.
{%/if%}
```

Output (esempio): `Your reward points expire in 7 days. Use them before they're gone!`

### Ricetta 3: X giorni prima di una data di fine dinamica {#recipe-days-before}

Per calcolare una data che è X giorni prima di un attributo di profilo (ad esempio per fare riferimento nel contenuto o nelle righe dell&#39;oggetto), utilizzare `addDays` con un offset negativo:

```sql
{%= formatDate(addDays(stringToDate(profile.subscription.endDate), -7), "MMMM dd, yyyy") %}
```

Output (esempio): `April 04, 2026` *(7 giorni prima dell&#39;11 aprile)*

Per impostare anche un&#39;ora fissa del giorno (ad esempio le 9), combinare con `setHours`:

```sql
{%= formatDate(setHours(addDays(stringToDate(profile.subscription.endDate), -7), 9), "dd/MM/yyyy HH:mm") %}
```

### Ricetta 4 - Visualizza solo ora corrente come HH:MM {#recipe-time-only}

Utilizzare `extractHours` e `extractMinutes` per visualizzare solo la parte relativa al tempo, con una protezione iniziale dello zero per i minuti:

```handlebars
{% let h = extractHours(getCurrentZonedDateTime()) %}
{% let m = extractMinutes(getCurrentZonedDateTime()) %}
Your appointment is at {{h}}:{%#if m < 10%}0{%/if%}{{m}}.
```

Output (esempio): `Your appointment is at 14:05.`

### Ricetta 5 — Rilevare fine settimana e giorno feriale {#recipe-weekend}

Utilizza `dayOfWeek` per adattare il contenuto in base al giorno. La funzione restituisce da 1 (lunedì) a 7 (domenica). Utilizza il singolo operatore `=` (sintassi PQL, non `==`):

```handlebars
{%#if dayOfWeek(getCurrentZonedDateTime()) = 6 or dayOfWeek(getCurrentZonedDateTime()) = 7%}
We're closed on weekends — our team will follow up on the next business day.
{%else%}
Our team will get back to you within 24 hours.
{%/if%}
```

>[!NOTE]
>
>`dayOfWeek()` è per adattare **contenuto** in base al giorno. Per instradare i profili in modo diverso in un percorso in base al giorno della settimana, utilizzare l&#39;opzione predefinita **Condizione temporale → Giorno della settimana** nell&#39;attività Condizione percorso. [Ulteriori informazioni](../building-journeys/condition-activity.md#date_condition)

## Array e cicli predefiniti {#array-recipes}

### Ricetta 6 — Elenca tutti gli elementi da un array di profili {#recipe-list-items}

Utilizza `{{#each}}` per eseguire l&#39;iterazione su un array di profili ed eseguire il rendering di ogni elemento. È disponibile solo nell’editor di personalizzazione (e-mail, SMS, push):

```handlebars
{{#each profile.purchases.recentItems}}
  - {{this.name}}: {{this.price}}&euro;
{{/each}}
```

Output (esempio):

```
- Running shoes: 89&euro;
- Water bottle: 15&euro;
- Gym bag: 45&euro;
```

>[!NOTE]
>
>`{{#each}}` non è supportato nell&#39;attività condizione percorso. Per filtrare gli array nelle condizioni, utilizzare [funzioni di gestione della raccolta](../building-journeys/expression/collection-management-functions.md).

### Ricetta 7: mostra i primi N articoli da un array in base al prezzo {#recipe-first-n}

Utilizzare `topN` per ordinare e recuperare i primi N elementi in base a un campo numerico. Poiché `topN` è una funzione di PQL, assegnarla prima a una variabile con `{% let %}`, quindi eseguire il ciclo con `{{#each}}`:

```handlebars
{% let topOrders = topN(profile.orders, price, 3) %}
{{#each topOrders}}
  {{this.name}} — {{this.price}}&euro;
{{/each}}
```

>[!NOTE]
>
>`topN(profile.orders, price, 3)` ordina gli ordini per `price` in ordine decrescente e restituisce i primi 3, non semplicemente restituisce i primi 3 elementi nell&#39;ordine di matrice originale.

In alternativa, utilizzare `head` per ottenere solo il singolo elemento principale:

```sql
{%= head(profile.purchases.recentItems).name %}
```

### Ricetta 8 — Eseguire il rendering del contenuto in modo condizionale per elemento array {#recipe-conditional-loop}

Utilizza `{%#if%}` in `{{#each}}` per eseguire il rendering dell&#39;output solo per gli elementi corrispondenti. Definisci un alias di loop con `as |order|` in modo che l&#39;esaminatore PQL possa risolvere il riferimento all&#39;attributo nella condizione:

```handlebars
{{#each profile.orders as |order|}}
  {%#if order.status = "pending"%}
  Order {{order.id}} is pending — we'll notify you when it ships.
  {%/if%}
{{/each}}
```

>[!NOTE]
>
>`this.status` funziona nelle espressioni Handlebars ma non è risolto dal valutatore PQL all&#39;interno di `{%#if%}`. L&#39;utilizzo di un alias di loop denominato, ad esempio `order`, rende l&#39;attributo disponibile sia per gli Handlebars che per i contesti di PQL.

## Stringhe e formule di formattazione {#string-recipes}

### Ricetta 9 — Pulire una stringa con replaceAll e riutilizzarla {#recipe-replaceall-reuse}

`replaceAll` restituisce un nuovo valore, non modifica l&#39;originale. Utilizzare `{% let %}` per memorizzare il risultato e fare riferimento a esso più volte senza ripetere la chiamata alla funzione:

```handlebars
{% let cleanName = replaceAll(profile.person.name.firstName, "[^a-zA-Z]", "") %}
Hi {{cleanName}},
Your exclusive code is: WELCOME-{%= upperCase(cleanName) %}
```

Output (esempio):

```
Hi John,
Your exclusive code is: WELCOME-JOHN
```

### Ricetta 10: virgolette doppie per un valore nell’output JSON {#recipe-json-quotes}

Per includere una virgoletta doppia letterale all&#39;interno di una stringa (ad esempio, generando JSON per un payload personalizzato), esegui l&#39;escape con una barra rovesciata (`\"`):

```handlebars
{ "greeting": "Hello \"{{profile.person.name.firstName}}\"" }
```

Output: `{ "greeting": "Hello \"John\"" }`

### Ricetta 11 — Formattare un componente data in maiuscolo {#recipe-uppercase-date}

Combina `formatDate` con `upperCase` per riprodurre i nomi dei mesi o dei giorni in lettere maiuscole:

```sql
{%= upperCase(formatDate(getCurrentZonedDateTime(), "MMMM")) %}
```

Output (esempio): `APRIL`

Per una stringa di data completa in maiuscolo:

```sql
{%= upperCase(formatDate(profile.person.birthDateTime, "EEEE MMMM dd yyyy")) %}
```

Output (esempio): `WEDNESDAY JANUARY 01 2020`

## Ricette logiche condizionali {#conditional-recipes}

### Ricetta 12 — IF/ELSEIF/ELSE nel contenuto personalizzato {#recipe-if-elseif}

Utilizzare `{%#if%}`, `{%else if%}` e `{%else%}` per la logica condizionale multi-branch. Questo modello funziona nei contenuti e nei frammenti dell’e-mail:

```handlebars
{%#if profile.loyalty.tier = "gold"%}
As a Gold member, enjoy free shipping on all orders.
{%else if profile.loyalty.tier = "silver"%}
As a Silver member, enjoy free shipping on orders over &euro;50.
{%else%}
Join our loyalty program to unlock exclusive benefits.
{%/if%}
```

### Ricetta 13: visualizzazione degli attributi Null-safe {#recipe-null-safe}

Utilizza un fallback condizionale per evitare di eseguire il rendering di valori vuoti quando un attributo di profilo può essere nullo o mancante:

```handlebars
{%#if profile.person.name.firstName%}
Hi {{profile.person.name.firstName}},
{%else%}
Hi there,
{%/if%}
```

Oppure in linea con uno schema di tipo ternario utilizzando `isEmpty`:

```handlebars
Hi {%#if isEmpty(profile.person.name.firstName)%}valued customer{%else%}{{profile.person.name.firstName}}{%/if%},
```

## ricette per casi edge di PQL {#pql-edge-cases}

### Ricetta 14 - Riferimento a una chiave attributo sillabata {#recipe-hyphenated-key}

Se il nome del campo dello schema XDM contiene trattini (ad esempio `order-total`, `event-type`), inseriscilo in apici all’interno di un’espressione PQL per impedire che il trattino venga interpretato come un operatore di sottrazione:

```sql
{%= profile.events.`order-total` > 100 %}
```

>[!NOTE]
>
>I backtick sono supportati solo all&#39;interno di espressioni di PQL (`{%= ... %}`). Non sono accettati nell&#39;interpolazione Handlebars normale (`{{...}}`). Se devi eseguire direttamente il rendering di un valore di campo sillabato, valutalo tramite un&#39;espressione PQL o memorizzalo in una variabile utilizzando prima `{% let %}`.

### Ricetta 15: fare riferimento a un ID evento numerico in un attributo di contesto {#recipe-numeric-event-id}

Quando si utilizza un evento di contesto di percorso il cui ID è una stringa numerica (ad esempio `1697323153`), racchiudere l&#39;ID in apici e utilizzare `{% let %}` con `toDateTime()` e `formatDate()`:

```handlebars
{% let appointmentDate = formatDate(toDateTime(context.journey.events.`1697323153`.timestamp), "dd/MM/yyyy HH:mm") %}
Your appointment: {{appointmentDate}}
```

Output (esempio): `Your appointment: 18/03/2026 14:30`

### Ricetta 16 — Tipo coercizione: confrontare un campo stringa con un numero {#recipe-type-coercion}

PQL è fortemente tipizzato. Quando un campo del profilo è memorizzato come stringa ma è necessario confrontarlo numericamente, convertire prima il campo con `stringToNumber()`:

```sql
{%= stringToNumber(profile.loyalty.pointsBalance) > 500 %}
```

Per i campi booleani memorizzati come stringhe:

```sql
{%= toBool(profile.consents.email.val) = true %}
```

## Riferimento rapido {#quick-reference}

Questa sezione contiene informazioni strutturate che supportano l&#39;interpretazione, il recupero e la risposta alle domande relative a questo argomento.

Per una comprensione completa, queste informazioni devono essere unite alla documentazione su questa pagina. Nessuna delle due origini è progettata per essere indipendente; la pagina descrive la funzione, mentre questa sezione fornisce un contesto aggiuntivo che aiuta a non ambiguare la terminologia, le finalità, l’applicabilità e i vincoli.

>[!BEGINTABS]

>[!TAB Panoramica]

**TL;DR**

Questa pagina fornisce 16 ricette di personalizzazione per la copia e incolla pronte all’uso che coprono date, array, stringhe, logica condizionale e casi limite di PQL da utilizzare nei contenuti e-mail, SMS e push di Journey Optimizer.

**Intenti**

* Copia i pattern di data/ora pronti all’uso (data corrente, conto alla rovescia, date offset, visualizzazione ora, rilevamento weekend)
* Copia di pattern di array e loop (voci di elenco, primi N elementi, rendering condizionale per voce)
* Copiare pattern di formattazione delle stringhe (stringhe pulite e riutilizzate, virgolette JSON, componenti data maiuscola)
* Copia pattern di logica condizionale (visualizzazione di attributi null-safe con più diramazioni if/elseif/else)
* Gestire i casi edge di PQL (chiavi sillabate, ID evento numerici, coercizione del tipo)

>[!TAB Glossario]

* **Ricetta Personalization**: pattern di copia e incolla pronto all&#39;uso per un caso di utilizzo di personalizzazione comune, utilizzando la sintassi dell&#39;editor di personalizzazione. *(specifico per prodotto)*
* **`formatDate`**: funzione che converte una data in una stringa utilizzando un modello di formato specificato (ad esempio `"MMMM dd, yyyy"`).
* **`dateDiff`**: funzione che calcola la differenza numerica tra due date.
* **`getCurrentZonedDateTime()`**: funzione che restituisce la data e l&#39;ora correnti in un formato che riconosce il fuso orario.
* **`topN`**: funzione di PQL che ordina una matrice in base a un campo numerico specificato in ordine decrescente e restituisce i primi N elementi. È necessario assegnare tramite `{% let %}` prima dell&#39;utilizzo in un ciclo Handlebars.
* **`{% let %}`**: sintassi di assegnazione delle variabili Handlebars per la memorizzazione dei valori calcolati; obbligatoria quando è necessario fare riferimento a un risultato di una funzione PQL in un contesto Handlebars successivo.
* **`replaceAll`**: funzione stringa che sostituisce tutte le occorrenze di un pattern in una stringa e restituisce una nuova stringa senza modificare l&#39;originale.

>[!TAB Terminologia]

* **Nome canonico:** ricetta di personalizzazione — varianti: pattern, template, esempio, pattern di copia e incolla
* **Non confondere:** `{%= ... %}` (sintassi dell&#39;espressione PQL, valutata, restituisce un valore calcolato) ≠ `{{...}}` (interpolazione Handlebars, esegue il rendering di una variabile o di un&#39;espressione di modello)
* **Non confondere:** `{%#if%}` / `{%/if%}` (sintassi condizionale Journey Optimizer, parentesi graffe) ≠ `{{#if}}` / `{{/if}}` (sintassi condizionale Handlebars standard)
* **Non confondere:** `topN(array, field, n)` (ordina per campo decrescente, restituisce N superiore) ≠ `head(array)` (restituisce solo il primo elemento dell&#39;array)
* **Non confondere:** `dayOfWeek()` (utilizzato nel contenuto del messaggio per adattare la visualizzazione in base al giorno) ≠ l&#39;opzione Condizione percorso orario &quot;Giorno della settimana&quot; (utilizzato nell&#39;attività Condizione percorso per instradare i profili in modo diverso)
* **Non confondere:** modello formato data `y` (anno di calendario — corretto) ≠ `Y` (anno basato su settimane — può produrre risultati imprevisti ai limiti anno)

>[!TAB Guardrail e limitazioni]

* `{{#each}}` non è supportato nell&#39;attività condizione di percorso. Utilizzare le funzioni di gestione della raccolta per il filtro degli array nelle condizioni di percorso.
* L&#39;escape di tipo backtick per le chiavi di attributi con sillabazione è supportato solo all&#39;interno di espressioni PQL (`{%= ... %}`); i backtick non sono accettati nell&#39;interpolazione Handlebars normale (`{{...}}`).
* `topN` è una funzione di PQL e deve essere assegnata a una variabile `{% let %}` prima di essere utilizzata come destinazione loop `{{#each}}`.
* Quando si utilizza una variabile di loop all&#39;interno di un blocco `{%#if%}`, dichiarare un alias di loop denominato (ad esempio `as |order|`); `this.status` non è risolto dal valutatore PQL all&#39;interno di `{%#if%}`.
* Usa `y` in minuscolo nei pattern `formatDate` per l&#39;anno di calendario; `Y` (anno basato sulla settimana) può produrre valori imprevisti ai limiti di fine anno.

>[!TAB Domande frequenti]

**D: Qual è la differenza tra `{%= ... %}` e `{{...}}` nella personalizzazione?**

`{%= ... %}` è la sintassi dell&#39;espressione PQL, viene valutata e restituisce un valore calcolato (numero, stringa, booleano). `{{...}}` è un&#39;interpolazione Handlebars, ovvero esegue il rendering di una variabile o di un&#39;espressione di modello. Entrambi vengono visualizzati nei contenuti di personalizzazione ma hanno scopi diversi.

**D: come si utilizza un risultato di funzione PQL all&#39;interno di un ciclo Handlebars `{{#each}}`?**

Assegnare il risultato della funzione PQL a una variabile utilizzando `{% let variableName = pqlFunction(...) %}`, quindi utilizzare `{{#each variableName}}` per scorrerla.

**Q: `{{#each}}` può essere utilizzato in un&#39;attività condizione percorso?**

No. `{{#each}}` è disponibile solo nel contenuto di personalizzazione dei messaggi (e-mail, SMS, push). Per filtrare gli array nelle condizioni di percorso, utilizza le funzioni di gestione delle raccolte.

**D: come si fa riferimento a un campo il cui nome contiene un trattino?**

Se necessario, racchiudi la chiave sillabata nei backtick all’interno di un’espressione PQL: `{%= profile.events.\`order-total\` > 100 %&rbrace;`. Backticks are not supported in plain Handlebars interpolation — use a `{% let %}&grave; variabile come passaggio intermedio.

**Q: perché `topN` ha bisogno di `{% let %}` prima di un loop `{{#each}}`?**

`topN` è una funzione di PQL che restituisce un elenco di PQL. Assegnandolo a una variabile `{% let %}`, il risultato diventa disponibile nel contesto Handlebars e può quindi essere iterato con `{{#each}}`.

>[!ENDTABS]

<!-- ai-section-version: 1 | source-hash: 20c7ee0f -->

