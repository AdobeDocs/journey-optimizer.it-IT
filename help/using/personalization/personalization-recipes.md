---
title: Ricette Personalization
description: Pattern di personalizzazione comuni ed esempi reali per Adobe Journey Optimizer
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
source-git-commit: 04fca756923d53595639e221fb59d3f6a458ac4a
workflow-type: tm+mt
source-wordcount: '815'
ht-degree: 0%

---

# Ricette Personalization {#personalization-recipes}

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

