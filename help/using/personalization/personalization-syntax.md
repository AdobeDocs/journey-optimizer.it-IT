---
solution: Journey Optimizer
product: journey optimizer
title: Sintassi di personalizzazione
description: Scopri come utilizzare la sintassi di personalizzazione.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: espressione, editor, sintassi, personalizzazione
exl-id: 5a562066-ece0-4a78-92a7-52bf3c3b2eea
source-git-commit: 8a1ec5acef067e3e1d971deaa4b10cffa6294d75
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 7%

---

# Sintassi di personalizzazione {#personalization-syntax}

Personalization in [!DNL Journey Optimizer] si basa sulla sintassi del modello Handlebars.
Per una descrizione completa della sintassi Handlebars, consulta la [documentazione HandlebarsJS](https://handlebarsjs.com/).

Utilizza un modello e un oggetto di input per generare HTML o altri formati di testo. I modelli Handlebars hanno l’aspetto di un testo normale con espressioni Handlebars incorporate.

Esempio di espressione semplice:

`{{profile.person.name}}`

dove:

* `profile` è uno spazio dei nomi.
* `person.name` è un token composto da attributi. La struttura degli attributi è definita in uno schema XDM di Adobe Experience Platform. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=it){target="_blank"}.

## Regole generali di sintassi {#general-rules}

Gli identificatori possono essere qualsiasi carattere Unicode ad eccezione dei seguenti:

```
Whitespace ! " # % & ' ( ) * + , . / ; < = > @ [ \ ] ^ ` { | } ~
```

La sintassi fa distinzione tra maiuscole e minuscole.

Le parole **true**, **false**, **null** e **undefined** sono consentite solo nella prima parte di un&#39;espressione di percorso.

In Handlebars, i valori restituiti da {{expression}} sono **con escape di HTML**. Se l&#39;espressione contiene `&`, l&#39;output con escape di HTML restituito verrà generato come `&amp;`. Se non desideri che Handlebars sfugga a un valore, utilizza il &quot;triplo-stash&quot;.

Per quanto riguarda gli argomenti delle funzioni letterali, il parser del linguaggio del modello non supporta una singola barra rovesciata senza escape (`\`). Questo carattere deve essere preceduto da una barra rovesciata (`\`). Esempio:

`{%= regexGroup("abc@xyz.com","@(\\w+)", 1)%}`

## Profilo

Questo spazio dei nomi consente di fare riferimento a tutti gli attributi definiti nello schema del profilo descritto nella [documentazione di Adobe Experience Platform Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=it){target="_blank"}.

Gli attributi devono essere definiti nello schema prima di essere referenziati in un blocco di personalizzazione [!DNL Journey Optimizer].

>[!NOTE]
>
>Scopri come sfruttare gli attributi del profilo nelle condizioni in [questa sezione](functions/helpers.md#if-function).

**Riferimenti di esempio:**

`{{profile.person.name.fullName}}`

`{{profile.person.name.firstName}}`

`{{profile.person.gender}}`

`{{profile.personalEmail.address}}`

`{{profile.mobilePhone.number}}`

`{{profile.homeAddress.city}}`

`{{profile.faxPhone.number}}`

## Tipi di pubblico{#perso-segments}

Scopri come sfruttare gli attributi del profilo nelle condizioni in [questa sezione](functions/helpers.md#if-function).

>[!NOTE]
>Per ulteriori informazioni sul servizio di segmentazione, consulta [questa documentazione](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=it){target="_blank"}.

## Offerte {#offers-syntax}

Questo spazio dei nomi consente di fare riferimento alle decisioni sulle offerte esistenti.
Per fare riferimento a un’offerta è necessario dichiarare un percorso con le diverse informazioni che definiscono un’offerta.

Questo percorso ha la seguente struttura:

`offers.Type.[Placement Id].[Activity Id].Attribute`

dove:

* `offers` identifica l&#39;espressione di percorso appartenente allo spazio dei nomi dell&#39;offerta
* `Type` determina il tipo di rappresentazione dell&#39;offerta. I valori possibili sono: `image`, `html` e `text`
* `Placement Id` e `Activity Id` sono identificatori di posizionamento e attività
* `Attributes` sono attributi specifici dell&#39;offerta che dipendono dal tipo di offerta. Esempio: `deliveryUrl` per le immagini

Per ulteriori informazioni sull&#39;API Decisions e su Offers Representation, consulta [questa pagina](../offers/api-reference/offer-delivery-api/decisioning-api.md)

Tutti i riferimenti vengono convalidati in base allo schema delle offerte con un meccanismo di convalida descritto in [questa pagina](personalization-validation.md)

**Riferimenti di esempio:**

* Posizione in cui è ospitata l’immagine:

  `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].deliveryUrl`

* URL di destinazione quando fai clic sull’immagine:

  `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].linkUrl`

* Contenuto del testo dell’offerta proveniente dal motore decisionale:

  `offers.text.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`

* Contenuto HTML dell’offerta proveniente dal motore decisionale:

  `offers.html.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`


## Helper{#helpers-all}

Un helper Handlebars è un semplice identificatore che può essere seguito da parametri.
Ogni parametro è un&#39;espressione Handlebars. È possibile accedere a questi helper da qualsiasi contesto in un modello.

Questi helper di blocco sono identificati da un # che precede il nome dell&#39;helper e richiedono un / di chiusura corrispondente, con lo stesso nome.
I blocchi sono espressioni con apertura di un blocco ({{# }}) and closing ({{/}}).


>[!NOTE]
>
>Le funzioni di supporto sono descritte in [questa sezione](functions/helpers.md).
>

## Tipi letterali {#literal-types}

[!DNL Adobe Journey Optimizer] supporta i seguenti tipi letterali:

| Letterale | Definizione |
| ------- | ---------- |
| Stringa | Tipo di dati costituito da caratteri racchiusi tra virgolette doppie. <br>Esempi: `"prospect"`, `"jobs"`, `"articles"` |
| Booleano | Tipo di dati true o false. |
| Intero | Tipo di dati che rappresenta un numero intero. Può essere positivo, negativo o zero. <br>Esempi: `-201`, `0`, `412` |
| Array | Tipo di dati composto da un gruppo di altri valori letterali. Utilizza parentesi quadre per raggruppare e virgole per delimitare tra valori diversi. <br> **Nota:** non è possibile accedere direttamente alle proprietà degli elementi all&#39;interno di un array. <br> Esempi: `[1, 4, 7]`, `["US", "FR"]` |

>[!CAUTION]
>
>L&#39;utilizzo della variabile **xEvent** non è disponibile nelle espressioni di personalizzazione. Qualsiasi riferimento a xEvent provocherà errori di convalida.

## URL PERSONALIZATION{#perso-urls}

Gli URL personalizzati indirizzano i destinatari verso pagine specifiche di un sito web o verso un microsito personalizzato, a seconda degli attributi del profilo. In Adobe Journey Optimizer, puoi aggiungere la personalizzazione agli URL nel contenuto del messaggio. La personalizzazione URL può essere applicata a testo e immagini e utilizzare dati di profilo o dati contestuali.

Journey Optimizer ti consente di personalizzare uno o più URL nel messaggio aggiungendo campi di personalizzazione. Per personalizzare un URL, effettua le seguenti operazioni:

1. Crea un collegamento nel contenuto del messaggio. [Ulteriori informazioni](../email/message-tracking.md#insert-links)
1. Dall’icona di personalizzazione, seleziona gli attributi. L&#39;icona di personalizzazione è disponibile solo per i seguenti tipi di collegamenti: **Collegamento esterno**, **Collegamento annullamento abbonamento** e **Rinuncia**.

   ![](assets/perso-url.png)

>[!NOTE]
>
>Nell’editor di personalizzazione, quando modifichi un URL personalizzato, le funzioni di assistenza e l’iscrizione ai tipi di pubblico vengono disabilitate per motivi di sicurezza.
>

**URL personalizzati di esempio**

* `https://www.adobe.com/users/{{profile.person.name.lastName}}`
* `https://www.adobe.com/users?uid={{profile.person.name.firstName}}`
* `https://www.adobe.com/usera?uid={{context.journey.technicalProperties.journeyUID}}`
* `https://www.adobe.com/users?uid={{profile.person.crmid}}&token={{context.token}}`

>[!CAUTION]
>
>Gli spazi non sono supportati nei token di personalizzazione utilizzati negli URL.
