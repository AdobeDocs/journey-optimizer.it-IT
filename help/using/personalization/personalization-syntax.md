---
title: Sintassi di personalizzazione
description: Scopri come utilizzare la sintassi di personalizzazione.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
exl-id: 5a562066-ece0-4a78-92a7-52bf3c3b2eea
source-git-commit: d3a22f223353dfa5d43acab400cea3d5c314662f
workflow-type: tm+mt
source-wordcount: '706'
ht-degree: 10%

---

# Sintassi di personalizzazione {#personalization-syntax}

Personalization in [!DNL Journey Optimizer] si basa sulla sintassi del modello denominata Handlebars.
Per una descrizione completa della sintassi Handlebars, fai riferimento a [Documentazione di HandlebarsJS](https://handlebarsjs.com/).

Utilizza un modello e un oggetto di input per generare HTML o altri formati di testo. I modelli Handlebars hanno un aspetto simile al testo normale con espressioni Handlebars incorporate.

Esempio di espressione semplice:

`{{profile.person.name}}`

Dove:

* `profile` è uno spazio dei nomi.
* `person.name` è un token composto da attributi. La struttura degli attributi è definita in uno schema XDM di Adobe Experience Platform. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=it){target=&quot;_blank&quot;}.

## Regole generali sulla sintassi {#general-rules}

Gli identificatori possono essere caratteri unicode, ad eccezione dei seguenti elementi:

```
Whitespace ! " # % & ' ( ) * + , . / ; < = > @ [ \ ] ^ ` { | } ~
```

La sintassi distingue tra maiuscole e minuscole.

Le parole **true**, **false**, **null** e **indefinito** sono consentiti solo nella prima parte di un&#39;espressione di percorso.

In Handlebars, i valori restituiti da {{expression}} sono **scampato a HTML**. Se l&#39;espressione contiene `&`, quindi l’output restituito in sequenza HTML viene generato come `&amp;`. Se non desideri che Handlebar eviti un valore, utilizza il &quot;triple-stash&quot;.

## Profilo

Questo spazio dei nomi ti consente di fare riferimento a tutti gli attributi definiti nello schema di profilo descritto in [Documentazione di Adobe Experience Platform Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html){target=&quot;_blank&quot;}.

Gli attributi devono essere definiti nello schema prima di essere referenziati in un [!DNL Journey Optimizer] blocco di personalizzazione.

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

## Segmenti{#perso-segments}

Scopri come sfruttare gli attributi del profilo nelle condizioni in [questa sezione](functions/helpers.md#if-function).

>[!NOTE]
>Per ulteriori informazioni sul servizio di segmentazione e segmentazione, consulta [questa sezione](../segment/about-segments.md).

## Offerte {#offers-syntax}

Questo spazio dei nomi ti consente di fare riferimento a decisioni esistenti sulle offerte.
Per fare riferimento a un’offerta è necessario dichiarare un percorso con le diverse informazioni che definiscono un’offerta.

Questo percorso ha la seguente struttura:

`offers.Type.[Placement Id].[Activity Id].Attribute`

Dove:

* `offers` identifica l&#39;espressione del percorso appartenente allo spazio dei nomi dell&#39;offerta
* `Type`  determina il tipo di rappresentazione dell’offerta. I valori possibili sono: `image`, `html` e `text`
* `Placement Id` e `Activity Id` sono identificatori di posizionamento e di attività
* `Attributes` sono attributi specifici dell’offerta che dipendono dal tipo di offerta. Esempio: `deliveryUrl` per immagini

Per ulteriori informazioni sull’API delle decisioni e sulla rappresentazione delle offerte, consulta [questa pagina](../offers/api-reference/offer-delivery-api/decisioning-api.md)

Tutti i riferimenti vengono convalidati rispetto allo schema delle offerte con un meccanismo di convalida descritto in [questa pagina](personalization-validation.md)

**Riferimenti di esempio:**

* Posizione in cui è ospitata l’immagine:

   `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].deliveryUrl`

* URL di destinazione quando fai clic sull’immagine:

   `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].linkUrl`

* Contenuto testo dell’offerta proveniente dal motore decisionale:

   `offers.text.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`

* Contenuto HTML dell’offerta proveniente dal motore decisionale:

   `offers.html.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`


## Assistenza{#helpers-all}

Un helper Handlebars è un identificatore semplice che può essere seguito da parametri.
Ogni parametro è un&#39;espressione Handlebars. È possibile accedere a questi helper da qualsiasi contesto in un modello.

Questi collaboratori di blocco sono identificati da un # che precede il nome dell&#39;helper e richiedono una chiusura / corrispondente, con lo stesso nome.
I blocchi sono espressioni con un blocco di apertura ({{# }}) e chiusura ({{/}}).


>[!NOTE]
>
>Le funzioni helper sono descritte in [questa sezione](functions/helpers.md).

## Tipi letterali {#literal-types}

[!DNL Adobe Journey Optimizer] supporta i seguenti tipi letterali:

| Letterale | Definizione |
| ------- | ---------- |
| Stringa | Tipo di dati composto da caratteri racchiusi tra virgolette doppie. <br>Esempi: `"prospect"`, `"jobs"`, `"articles"` |
| Booleano | Tipo di dati vero o falso. |
| Intero | Tipo di dati che rappresenta un numero intero. Può essere positivo, negativo o zero. <br>Esempi: `-201`, `0`, `412` |
| Array | Tipo di dati composto da un gruppo di altri valori letterali. Utilizza parentesi quadre per raggruppare e virgole per delimitare valori diversi. <br> **Nota:** Non è possibile accedere direttamente alle proprietà degli elementi all&#39;interno di una matrice. <br> Esempi: `[1, 4, 7]`, `["US", "FR"]` |

>[!CAUTION]
>
>L&#39;uso di **xEvent** non è disponibile nelle espressioni di personalizzazione. Qualsiasi riferimento a xEvent genererà errori di convalida.

## Personalizzazione URL{#perso-urls}

Gli URL personalizzati indirizzano i destinatari verso pagine specifiche di un sito web o verso un microsito personalizzato, a seconda degli attributi del profilo. In Adobe Journey Optimizer puoi aggiungere la personalizzazione agli URL nel contenuto del messaggio. La personalizzazione URL può essere applicata a testo e immagini e utilizzare dati di profilo o dati contestuali.

Journey Optimizer ti consente di personalizzare uno o più URL nel messaggio aggiungendo loro campi di personalizzazione. Per personalizzare un URL, effettua le seguenti operazioni:

1. Crea un collegamento nel contenuto del messaggio. [Ulteriori informazioni](../design/message-tracking.md#insert-links)
1. Seleziona gli attributi dall’icona di personalizzazione. L’icona di personalizzazione è disponibile solo per i seguenti tipi di collegamenti: **Collegamento esterno**, **Collegamento di annullamento dell’abbonamento** e **Rinuncia**.

![](assets/perso-url.png)

>[!NOTE]
>
>Nell’editor espressioni, quando modifichi un URL personalizzato, le funzioni helper e l’appartenenza ai segmenti sono disabilitate per motivi di sicurezza.

**URL personalizzati di esempio**

* `https://www.adobe.com/users/{{profile.person.name.lastName}}`
* `https://www.adobe.com/users?uid={{profile.person.name.firstName}}`
* `https://www.adobe.com/usera?uid={{context.journey.technicalProperties.journeyUID}}`
* `https://www.adobe.com/users?uid={{profile.person.crmid}}&token={{context.token}}`

>[!CAUTION]
>
>Gli spazi non sono supportati nei token di personalizzazione utilizzati all’interno degli url.
