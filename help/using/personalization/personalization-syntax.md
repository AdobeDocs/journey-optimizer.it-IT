---
title: Sintassi di personalizzazione
description: Scopri come utilizzare la sintassi di personalizzazione
translation-type: tm+mt
source-git-commit: e73b47ab6243b13f82aa1503bd8c751f976f29ee
workflow-type: tm+mt
source-wordcount: '718'
ht-degree: 2%

---

# Sintassi di personalizzazione {#personalization-syntax}

![](../assets/do-not-localize/badge.png)

## Introduzione

La personalizzazione in Journey Optimizer si basa sulla sintassi del modello denominata Handlebars.
Per una descrizione completa della sintassi Handlebars, consulta [HandlebarsJS](https://handlebarsjs.com/).

Utilizza un modello e un oggetto di input per generare HTML o altri formati di testo. I modelli Handlebars hanno un aspetto simile al testo normale con espressioni Handlebars incorporate.

Esempio di espressione semplice:

```
{{profile.person.name}}
```

dove:

* **** profilo è uno spazio dei nomi.
* **person.** name è un token composto da attributi. La struttura degli attributi è definita in uno schema XDM di Adobe Experience Platform. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=it).

## Regole generali sulla sintassi

Gli identificatori possono essere caratteri unicode, ad eccezione dei seguenti elementi:

```
Whitespace ! " # % & ' ( ) * + , . / ; < = > @ [ \ ] ^ ` { | } ~
```

La sintassi distingue tra maiuscole e minuscole.

Le parole **true**, **false**, **null** e **undefined** sono consentite solo nella prima parte di un&#39;espressione di percorso.

In Handlebars, i valori restituiti da {{expression}} sono **HTML-escape**. Se l&#39;espressione contiene &amp;, l&#39;output HTML restituito viene generato come &amp;. Se non desideri che Handlebar eviti un valore, utilizza il &quot;triple-stash&quot;.

## Profilo

Questo spazio dei nomi ti consente di fare riferimento a tutti gli attributi definiti nello schema del profilo descritto nella documentazione [Adobe Experience Platform Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html).

Gli attributi devono essere definiti nello schema prima di essere referenziati in un blocco di personalizzazione Journey Optimizer.

Tutti i riferimenti vengono convalidati rispetto allo schema di profilo con un meccanismo di convalida descritto [qui](personalization-validation.md).

**Riferimenti di esempio:**

* ```{{profile.person.name.fullName}}```
* ```{{profile.person.name.firstName}}```
* ```{{profile.person.gender}}```
* ```{{profile.personalEmail.address}}```
* ```{{profile.mobilePhone.number}}```
* ```{{profile.homeAddress.city}}```
* ```{{profile.faxPhone.number}}```

**Determina estensione** indirizzo e-mail:

```
{%#if contains(profile.personalEmail.address, ".edu")%}
<a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
{%else if contains(profile.personalEmail.address, ".org")%}
<a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
{%else%}
<a href="https://www.adobe.com/users">Checkout our page</a>
{%/if%}
```

## Segmenti

Per ulteriori informazioni sul servizio di segmentazione e segmentazione, consulta questa [sezione](../segment/about-segments.md).

**Eseguire il rendering di contenuti diversi in base all’appartenenza** al segmento:

```
{%#if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8b").status = "existing"%}
  Hi! Esteemed gold member. <a href="https://www.somedomain.com/gold">Checkout your exclusive perks </a>
{%else%} if 'profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8c").status = "existing"'%}
  Hi! Esteemed silver member. <a href="https://www.somedomain.com/silver">Checkout your exclusive perks </a>
{%/if%}
```

**Determina se un profilo è già un membro**:

```
{%#if profile.segmentMembership.get(segments.`123e4567-e89b-12d3-a456-426614174000`.id)%}
    You're a member!
{%else%}
    You should be a member! Sign up now!
{%/if%}
```

## Offerte

Questo spazio dei nomi ti consente di fare riferimento a decisioni esistenti sulle offerte.
Per fare riferimento a un’offerta è necessario dichiarare un percorso con le diverse informazioni che definiscono un’offerta.

Questo percorso ha la seguente struttura:
0 - &quot;offerte&quot; : identifica l&#39;espressione del percorso appartenente allo spazio dei nomi dell&#39;offerta
1 - Tipo : determina il tipo di rappresentazione dell’offerta. I valori validi sono &quot;image&quot;, &quot;html&quot; e &quot;text&quot;
2 - Id Posizionamento
3 - ID attività
4 - Attributi specifici dell&#39;offerta. A seconda del tipo di offerta è possibile utilizzare gli attributi supportati. Ad esempio, per le immagini `deliveryUrl`.

Per ulteriori informazioni sull&#39;API di Decisioni, consulta questa [pagina](https://experienceleague.adobe.com/docs/offer-decisioning/using/api-reference/offer-delivery/deliver-offers.html?lang=en#deliver-offers-using-the-decisions-api).

Per ulteriori informazioni sulla rappresentazione delle offerte, consulta questa [pagina](https://experienceleague.adobe.com/docs/offer-decisioning/using/api-reference/offer-delivery/deliver-offers.html?lang=en#accept-and-content-type-headers).

Tutti i riferimenti vengono convalidati rispetto allo schema delle offerte con un meccanismo di convalida descritto [qui](personalization-validation.md).

**Riferimenti di esempio:**

* Posizione in cui è ospitata l’immagine:

```offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].deliveryUrl```

* URL di destinazione quando fai clic sull’immagine:

```offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].linkUrl```

* Contenuto testuale dell’offerta proveniente dal motore decisionale:

```offers.text.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content```

* Contenuto HTML dell’offerta proveniente dal motore decisionale:

```offers.html.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content```


## Helper

Un helper Handlebars è un identificatore semplice che può essere seguito da parametri.
Ogni parametro è un&#39;espressione Handlebars. È possibile accedere a questi helper da qualsiasi contesto in un modello.

Questi collaboratori di blocco sono identificati da un # che precede il nome dell&#39;helper e richiedono una chiusura / corrispondente, con lo stesso nome.
I blocchi sono espressioni con un blocco di apertura ({{# }}) e chiusura ({/}}).

### Se

L’helper **if** viene utilizzato per definire un blocco condizionale.
Se la valutazione dell’espressione restituisce true, il blocco viene sottoposto a rendering in caso contrario viene ignorato.

```
{%#if contains(profile.personalEmail.address, ".edu")%}
<a href="https://www.adobe.com/academia">Check out this link</a>
```

Seguendo l&#39;helper **if**, è possibile immettere un&#39;istruzione **else** per specificare un blocco di codice da eseguire, se la stessa condizione è falsa.
L&#39;istruzione **else if** specifica una nuova condizione per verificare se la prima istruzione restituisce false.

**Eseguire il rendering di diversi collegamenti all’archivio in base alle espressioni** condizionali:

```
{%#if profile.homeAddress.countryCode = "FR"%}
  <a href="https://www.somedomain.com/fr">Consultez notre catalogue</a>
{%else%}
  <a href="https://www.somedomain.com/en">Checkout our catalogue</a>
{%/if%}
```

### A meno che

**Per definire un blocco condizionale viene utilizzato #** unless helper. In opposizione all&#39;helper **#if**, se la valutazione dell&#39;espressione restituisce false, viene eseguito il rendering del blocco.

**Esegui il rendering di alcuni contenuti in base all’estensione** dell’indirizzo e-mail:

```
{%#unless endsWith(profile.personalEmail.address, ".edu")%}
Some Normal Content
{%else%}
Some edu specific content Content
{%/unless%}
```

### Ogni

L&#39;helper **each** viene utilizzato per eseguire iterazioni su un array.
La sintassi dell&#39;helper è ```{{#each ArrayName}}``` YourContent {{/each}}
Possiamo fare riferimento ai singoli elementi dell&#39;array utilizzando la parola chiave **this** all&#39;interno del blocco. È possibile eseguire il rendering dell&#39;indice dell&#39;elemento dell&#39;array utilizzando {{@index}}.

Esempio:

```
{{#each profile.productsInCart}}
    <li>{{this.name}}</li>
    </br>
{{/each}}
```

```
{{#each profile.homeAddress.city}}
  {{@index}} : {{this}}<br>
{{/each}}
```

**Esegui il rendering di un elenco di prodotti di cui dispone questo utente nel carrello**:

```
{{#each profile.products as |product|}}
    <li>{{product.productName}} {{product.productRating}}</li>
   </br>
{{/each}}
```

### Con

L’ **#with** helper viene utilizzato per modificare il token di valutazione della parte modello.

Esempio:

```
{{#with profile.person.name}}
{{this.firstName}} {{this.lastName}}
{{/with}}
```

L’ **#with** helper è utile per definire anche una variabile di scelta rapida.

**Utilizzare con per assegnare i nomi di variabili lunghe a nomi** più brevi:

```
{{#with profile.person.name as |name|}}
 Hi {{name.firstName}} {{name.lastName}}!
 Checkout our trending products for today!
{{/with}}
```


## Limitazioni 

* L’utilizzo della variabile **xEvent** non è disponibile nelle espressioni di personalizzazione. Qualsiasi riferimento a xEvent genererà errori di convalida.
