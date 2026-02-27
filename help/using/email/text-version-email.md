---
solution: Journey Optimizer
product: journey optimizer
title: Gestire la versione testuale di un messaggio e-mail
description: Scopri come creare la versione testuale di un’e-mail
feature: Email Design
topic: Content Management
role: User
level: Intermediate
keywords: testo, e-mail, versione, normale, editor
exl-id: 4bb36810-65fb-4a9b-9bea-e56ed2c1eea3
source-git-commit: 1a5ce1bf2d98a5de31f1245dee96d24984cb28d9
workflow-type: tm+mt
source-wordcount: '1141'
ht-degree: 8%

---

# Gestire la versione testuale di un messaggio e-mail {#text-version-email}

Si consiglia di creare una versione testuale del corpo dell’e-mail, che viene utilizzata quando non è possibile visualizzare il contenuto HTML.

Dal punto di vista della sicurezza, offrire una versione in testo normale è importante perché le e-mail di HTML possono comportare rischi come script dannosi, pixel di tracciamento o tentativi di phishing che si basano su formattazione e collegamenti avanzati. Il testo normale riduce la superficie di attacco ed è spesso preferito dai destinatari attenti alla sicurezza o dai sistemi e-mail aziendali che limitano o eliminano HTML. La disponibilità di entrambe le versioni consente ai destinatari di scegliere il formato adatto ai propri requisiti di sicurezza e privacy.

## Accedere alla versione di testo predefinita {#plain-text-default}

Per impostazione predefinita, E-mail Designer crea una versione **[!UICONTROL Testo normale]** del messaggio e-mail, compresi i campi di personalizzazione. Questa versione viene generata automaticamente e sincronizzata con la versione HTML del contenuto.

Per accedere alla versione di testo predefinita, seleziona l&#39;icona **[!UICONTROL Testo normale]** dal contenuto dell&#39;e-mail.

![](assets/text_version_3.png)

## Utilizza una versione di testo personalizzata {#plain-text-default-custom}

Se preferisci utilizzare un contenuto diverso per la versione di testo normale, segui la procedura seguente:

1. Dall&#39;e-mail, seleziona l&#39;icona **[!UICONTROL Testo normale]**.

1. Utilizza l&#39;interruttore **[!UICONTROL Sincronizza con HTML]** per disabilitare la sincronizzazione. Fai clic sul segno di spunta per confermare la scelta.

   ![](assets/text_version_2.png)

1. Puoi quindi modificare la versione di testo normale personalizzata in base alle tue esigenze.

>[!CAUTION]
>
> * Quando la sincronizzazione è disabilitata, le modifiche apportate nella visualizzazione **[!UICONTROL Testo normale]** non vengono applicate alla visualizzazione HTML.
>
> * Se riattivi l&#39;opzione **[!UICONTROL Sincronizza con HTML]** dopo aver aggiornato il contenuto di testo normale, le modifiche andranno perse e verranno sostituite con il contenuto di testo generato dalla versione di HTML.

## Quando utilizzare versioni di testo normale personalizzate {#when-to-use}

Sapere quando creare una versione di testo normale personalizzata anziché utilizzare la sincronizzazione automatica consente di garantire una consegna e una leggibilità ottimali delle e-mail.

### Utilizza testo normale personalizzato (disabilita sincronizzazione) quando:

* **Layout HTML complessi** - L&#39;e-mail HTML include layout a più colonne, tabelle o CSS complessi che non si traducono correttamente in testo normale.
* **Contenuto visivo** - Il tuo indirizzo e-mail si basa in larga misura sulle immagini e desideri fornire alternative testuali descrittive per i client disabilitati per le immagini.
* **Diversa struttura di messaggistica** - Si desidera fornire una struttura di messaggi semplificata o riorganizzata ottimizzata per i lettori di testo normale.
* **Requisiti di accessibilità** - È necessaria una formattazione di testo normale specifica per soddisfare gli standard di accessibilità.
* **Client e-mail legacy** - Il pubblico include gli utenti di client e-mail precedenti (ad esempio, Outlook 2003, client mobili di solo testo) che necessitano di contenuti con formattazione speciale.
* **Formattazione ASCII** - Si desidera includere una formattazione di testo normale specifica, ad esempio ASCII art, tabelle o interruzioni di riga specifiche.

### Usa sincronizzazione automatica (impostazione predefinita) quando:

* **Semplice progettazione HTML** - La tua e-mail HTML ha una struttura semplice e lineare che si traduce bene in testo normale.
* **Contenuto coerente** - Desideri mantenere l&#39;esatta coerenza tra le versioni di HTML e testo normale.
* **Aggiornamenti frequenti** - Aggiorna regolarmente il contenuto delle e-mail e vuoi evitare duplicazioni manuali.
* **Personalization funziona correttamente** - I campi di personalizzazione funzionano correttamente in entrambi i formati.
* **Vincoli di tempo** - È necessario avviare rapidamente le e-mail senza ulteriore personalizzazione del testo normale.

## Esempi pratici {#practical-examples}

Gli esempi seguenti illustrano scenari reali per aiutarti a decidere se utilizzare il testo normale personalizzato o la sincronizzazione automatica. Ogni esempio spiega il contesto, l’approccio consigliato e la motivazione alla base della decisione.

+++Esempio 1: newsletter marketing con layout complesso

**Scenario:** newsletter a più colonne con immagini, pulsanti con stili e sezioni codificate con colori.

![](assets/text_version_ex1.png)

**Consiglio:** Utilizzare testo normale personalizzato (disabilita sincronizzazione).

**Motivo per il testo normale personalizzato:** La versione di HTML utilizza un layout griglia a tre colonne con immagini di banner, pulsanti con stili e sezioni con codici colore. Questi elementi visivi non si traducono bene in testo normale tramite sincronizzazione automatica, con conseguente contenuto disordinato e difficile da leggere. Una versione di testo normale personalizzata consente di ristrutturare il contenuto in un formato lineare e facile da scansionare con intestazioni di sezione chiare e collegamenti formattati correttamente.

**Esempio di testo normale personalizzato:**

```
================================================
YOUR BRAND - MONTHLY NEWSLETTER
December 2025
================================================

🌟 FEATURED ARTICLE
"10 Ways to Optimize Your Customer Journeys"
Read more: https://example.com/articles/optimize-journeys

📢 UPCOMING WEBINAR
"Mastering Email Personalization"
December 15, 2025 at 2:00 PM EST
Register: https://example.com/webinar/register

📦 NEW PRODUCTS
- Winter Collection: https://example.com/winter
- Holiday Gift Guide: https://example.com/gifts

================================================
Website: https://example.com
Unsubscribe: https://example.com/unsubscribe
================================================
```

+++

+++Esempio 2: conferma di un ordine transazionale

**Scenario:** conferma ordine con dati strutturati (numero ordine, articoli, prezzi, dettagli spedizione).

![](assets/text_version_ex2.png)

**Consiglio:** Utilizzare la sincronizzazione automatica.

**Perché funziona la sincronizzazione automatica:** Le conferme d&#39;ordine hanno una struttura semplice e lineare che si traduce naturalmente da HTML a testo normale. I flussi di informazioni sono logici (dettagli → articoli → totali → spedizione) e i campi di personalizzazione come numeri di ordine e nomi dei clienti funzionano in modo identico in entrambi i formati. I dati strutturati e tabulari vengono convertiti in modo chiaro senza richiedere regolazioni manuali, risparmiando tempo e mantenendo la chiarezza.

+++

+++Esempio 3: invito ad un evento con rich media

**Scenario:** invito ad eventi con immagini di sfondo, video incorporati ed elementi interattivi.

![](assets/text_version_ex3.png)

**Consiglio:** Utilizzare testo normale personalizzato (disabilita sincronizzazione).

**Perché usare testo normale personalizzato:** la versione di HTML si basa sull&#39;impatto visivo: immagini di sfondo, video incorporati e pulsanti RSVP interattivi. La sincronizzazione automatica eliminerebbe questi elementi, lasciando una versione del testo confusa con riferimenti interrotti. Una versione di testo normale personalizzata consente di fornire dettagli chiari sull’evento, informazioni sugli oratori e collegamenti di registrazione diretti in un formato ben organizzato che funziona senza elementi visivi.

**Esempio di testo normale personalizzato:**

```
YOU'RE INVITED!
Annual Customer Summit 2025

📅 When: March 15-17, 2025
📍 Where: San Francisco Convention Center
         123 Market Street, San Francisco, CA

KEYNOTE SPEAKERS
- Jane Smith, CEO TechCorp: "The Future of Digital Marketing"
- John Doe, Chief Innovation Officer: "AI and Customer Experience"

REGISTER NOW: https://example.com/summit/register
Early bird discount ends February 1st

Full agenda: https://example.com/summit/agenda
Questions: events@example.com | 1-800-555-0123
```

+++

## Casi d’uso comuni {#common-use-cases}

I seguenti casi d’uso illustrano situazioni in cui è utile creare una versione di testo normale personalizzata (disattivando la sincronizzazione). Ogni esempio mostra la sfida posta dalla versione di HTML e come una soluzione di testo normale personalizzata la affronta.

+++Caso d’uso 1: e-mail sul catalogo dei prodotti

**Sfida:** in HTML viene visualizzata una griglia di prodotti con immagini, prezzi e pulsanti di acquisto

**Soluzione di testo normale:** creare un elenco strutturato con nomi di prodotto, prezzi e collegamenti diretti chiari

```
FEATURED PRODUCTS
=================

1. Premium Leather Wallet
   Price: $89.99
   View product: https://example.com/product/wallet
   
2. Designer Sunglasses
   Price: $129.99
   View product: https://example.com/product/sunglasses
```

+++

+++Caso d’uso 2: benvenuto alla serie e-mail

**Sfida:** e-mail di benvenuto con marchio con logo aziendale e formattazione dello stile

**Soluzione testo normale:** Utilizzare la formattazione ASCII art o text per creare una gerarchia visiva

```
***************************************************
*                                                 *
*     WELCOME TO [BRAND NAME]                    *
*     We're thrilled to have you!                *
*                                                 *
***************************************************
```

+++

+++Caso d’uso 3: sondaggio o richiesta di feedback

**Sfida:** HTML include pulsanti con stili ed elementi modulo

**Soluzione testo normale:** fornire collegamenti di testo non crittografato con istruzioni

```
We'd love your feedback!
------------------------

Please take 2 minutes to complete our survey:
https://example.com/survey/customer-feedback

Your input helps us improve our service.
```

+++

## Domande frequenti {#faq}

**I campi di personalizzazione funzioneranno in testo normale?**\
Sì, i campi di personalizzazione come `{{profile.firstName}}` funzionano in modo identico in entrambe le versioni HTML e testo normale.

**Come si verifica la versione in testo normale?**
* Passa alla visualizzazione **[!UICONTROL Testo normale]** nel Designer e-mail. [Scopri come](#text-version-email)
* Invia e-mail di prova a client e-mail di solo testo come versioni precedenti di Pine o app e-mail di base per dispositivi mobili.

**Cosa succede se dimentico di creare una versione in testo normale?**\
Il sistema genera automaticamente una versione in testo normale dal HTML, che potrebbe non essere formattata in modo ottimale ma che garantirà la consegna ai client di solo testo.

**Posso utilizzare una personalizzazione diversa in HTML rispetto al testo normale?**\
Sì, una volta disattivata la sincronizzazione, puoi personalizzare ogni versione in modo indipendente, anche utilizzando campi di personalizzazione o contenuti diversi.

**Quali client di posta elettronica supportano solo il testo normale?**\
Pochissimi client moderni sono di solo testo, ma alcuni criteri e-mail aziendali, strumenti di accessibilità e dispositivi mobili meno recenti possono visualizzare del testo normale. Si tratta anche di un fallback quando il rendering HTML non riesce.

**Con quale frequenza devo aggiornare la versione in testo normale?**\
Aggiornalo ogni volta che apporti modifiche significative al contenuto HTML. Modifiche minori apportate a HTML potrebbero non richiedere aggiornamenti di testo normale se il messaggio principale rimane lo stesso.

**Posso includere collegamenti nelle e-mail in testo normale?**\
Sì! Includi URL completi (ad esempio, https://example.com/page) e la maggior parte dei client e-mail li renderà automaticamente cliccabili.

**Includere immagini in testo normale?**\
No, il testo normale non supporta le immagini. Descrivi invece ciò che viene visualizzato nell’immagine o fornisci un collegamento per visualizzarlo online.
