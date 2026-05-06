---
solution: Journey Optimizer
product: journey optimizer
title: Personalizzazione degli URL nelle e-mail
description: Scopri le best practice e le limitazioni per la generazione dinamica di URL mantenendo al contempo affidabile il tracciamento
feature: Email Design, Monitoring
topic: Content Management
role: User
level: Intermediate, Experienced
keywords: URL, collegamento, personalizzazione, tracciamento, codifica, parentesi graffe
source-git-commit: 36fad8d6c200118210794249fa12263ae70e5422
workflow-type: tm+mt
source-wordcount: '760'
ht-degree: 1%

---

# Personalizzazione degli URL nelle e-mail {#url-personalization}

Gli URL personalizzati consentono di fornire esperienze contestuali attraverso i messaggi e-mail di [!DNL Journey Optimizer], ad esempio la generazione di collegamenti specifici per i destinatari o l&#39;aggiunta di parametri dinamici.

Portano i destinatari su pagine specifiche di un sito web o su un microsito personalizzato, a seconda degli attributi del profilo.

## Personalizzare un URL {#personalize-url}

Per personalizzare un URL, segui i passaggi indicati di seguito.

1. In E-mail Designer, seleziona un elemento nel contenuto e [inserisci un collegamento](message-tracking.md#insert-links) utilizzando la barra degli strumenti contestuale.

   >[!IMPORTANT]
   >
   >Personalization è disponibile solo per **[!UICONTROL Collegamento esterno]**, **[!UICONTROL Collegamento di annullamento sottoscrizione]** e **[!DNL Opt-Out]**. Assicurati di selezionare un tipo di collegamento appropriato.

1. Seleziona l’icona di personalizzazione.

   ![](assets/message-tracking-insert-link-perso.png)

1. Utilizza l’editor di personalizzazione per aggiungere gli attributi di profilo con cui desideri personalizzare l’URL.

1. Salva le modifiche.

Di seguito sono riportati alcuni esempi di URL personalizzati:

* `https://www.adobe.com/users/{{profile.person.name.lastName}}`
* `https://www.adobe.com/users?uid={{profile.person.name.firstName}}`
* `https://www.adobe.com/usera?uid={{context.journey.technicalProperties.journeyUID}}`
* `https://www.adobe.com/users?uid={{profile.person.crmid}}&token={{context.token}}`

>[!NOTE]
>
>Quando modifichi un URL personalizzato nell’editor di personalizzazione, le funzioni di assistenza e l’iscrizione a un pubblico vengono disabilitate per motivi di sicurezza.
>
>Gli spazi non sono supportati nei token di personalizzazione utilizzati negli URL.

Per un rendering e un tracciamento affidabili, segui le [best practice e guardrail](#best-practices) di seguito.

## Personalizzare un URL completo/di base {#personalize-complete-base-url}

Journey Optimizer supporta anche la personalizzazione dell&#39;**intero** URL o del **dominio base** di un URL, ad esempio:

```html
<a href="{{profile.social.link}}" />
<a href="{{profile.social.baseUrl}}/profile" />
<a href="https://{{profile.social.baseUrl}}/profile" />
```

>[!IMPORTANT]
>
>Per abilitare la personalizzazione URL completa o di base, contatta Adobe e fornisci l’elenco dei domini accettati. Questo è necessario per evitare reindirizzamenti non sicuri.

## Personalizzare i parametri di tracciamento URL {#personalize-url-tracking-parameters}

[Il tracciamento URL](url-tracking.md) è gestito a livello di configurazione del canale e si applica a tutti gli URL inclusi nel contenuto del messaggio. Puoi anche personalizzare i parametri di tracciamento URL per un singolo collegamento nel Designer e-mail. Questo ti consente di aggiungere un parametro specifico per il destinatario a un singolo collegamento (ad esempio, per passare un identificatore agli strumenti di analisi web).

A tale scopo, [inserisci un collegamento](message-tracking.md#insert-links), seleziona l&#39;icona di personalizzazione, aggiungi il parametro di tracciamento URL e seleziona l&#39;attributo di profilo desiderato dall&#39;[editor di personalizzazione](../personalization/personalization-build-expressions.md).

![](assets/message-tracking-perso-parameter.png)

Ripeti i passaggi precedenti per ogni collegamento a cui desideri aggiungere questo parametro di tracciamento.

Ora, quando l’e-mail viene inviata, questo parametro viene aggiunto automaticamente alla fine dell’URL. Puoi quindi acquisire questo parametro negli strumenti di analisi web o nei rapporti sulle prestazioni.

>[!NOTE]
>
>Per verificare l&#39;URL finale, puoi [inviare una bozza](../content-management/proofs.md) e fare clic sul collegamento nel contenuto dell&#39;e-mail una volta ricevuta la bozza. L’URL deve visualizzare il parametro di tracciamento. Ad esempio: <https://luma.enablementadobe.com/content/luma/us/en.html?utm_contact=profile.userAccount.contactDetails.homePhone.number>

## Best practice e guardrail {#best-practices}

Per mantenere i collegamenti validi, cliccabili e tracciabili, segui le best practice e le protezioni riportate di seguito.

### Parentesi graffe per gli URL dinamici {#use-braces}

Quando si inserisce un URL che contiene la personalizzazione, utilizzare tre parentesi graffe (`{{{ ... }}}`) per la parte dinamica dell&#39;URL. In questo modo si evita che l&#39;escape alteri caratteri speciali (ad esempio `/` e `+`) e si evitino URL interrotti, reindirizzamenti non corretti o problemi di tracciamento.

Ecco un esempio:

```html
<a href="https://example.com/path/{{{profile.person.customSlug}}}?ref={{{context.system.source.id}}}">View details</a>
```

>[!IMPORTANT]
>
>L&#39;utilizzo dell&#39;output non elaborato (`{{{ ... }}}`) indica che il valore è inserito così com&#39;è. Utilizzalo solo con valori considerati attendibili e destinati a essere sicuri per gli URL (ad esempio, valori generati o convalidati a monte).

### Correzione del tracciamento URL {#enable-url-tracking}

* Quando si utilizza la personalizzazione per generare l&#39;URL, assicurarsi che il valore risolto inizi con `http`/`https` per ogni destinatario. In caso contrario, il tracciamento potrebbe non essere applicato e il collegamento potrebbe non comportarsi come previsto.

* Non utilizzare la logica dinamica, ad esempio `let`, `each` o `if` istruzioni direttamente nel campo URL dell&#39;editor di personalizzazione. Questi sono disabilitati per motivi di sicurezza.

* Se lo scenario prevede una logica complessa per la generazione di URL personalizzati, evita di inserirla direttamente nel campo URL dell’editor di personalizzazione. Invece:
   * Aggiungi la logica e le istruzioni necessarie nel contenuto HTML sopra o vicino al campo URL.
   * Genera e archivia separatamente gli attributi personalizzati, quindi fai riferimento a essi nel contenuto dell’e-mail.

### Codifica e lunghezza URL {#encoding}

* Le regole di sintassi URI ([RFC 3986 standard](https://datatracker.ietf.org/doc/html/rfc3986){target="_blank"}) si applicano a tutti gli URL nel contenuto dell&#39;e-mail. Tuttavia, è più probabile che gli URL personalizzati presentino problemi di codifica, perché i valori specifici del destinatario possono introdurre caratteri riservati (ad esempio nei parametri di query). Assicurati pertanto che i valori dinamici siano codificati in URL (in particolare spazi, `&`, `#`, `%` e `+`) ed evita di utilizzare `+` per i valori di query.

* Gli URL molto lunghi possono essere troncati o rifiutati da browser, client di posta o sistemi a valle. Ad esempio, gli URL delle pagine mirror possono crescere in modo significativo quando la personalizzazione di runtime è pesante. Mantieni i payload personalizzati piccoli ed evita di incorporare oggetti di grandi dimensioni negli URL.

### Passaggi di convalida consigliati {#validation}

Prima di attivare un percorso o una campagna, segui le raccomandazioni seguenti:

* Invia una [bozza](../content-management/proofs.md) e fai clic sui collegamenti per confermare che l&#39;URL risolto inizi con `http`/`https` e mantenga la struttura prevista.
* Se i parametri di tracciamento vengono aggiunti alla fine, verifica che l’URL finale li includa (tramite il tracciamento URL a livello di configurazione o parametri di tracciamento per collegamento).

