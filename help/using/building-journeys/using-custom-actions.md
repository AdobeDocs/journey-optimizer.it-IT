---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare azioni personalizzate
description: Scopri come utilizzare le azioni personalizzate
feature: Actions
topic: Content Management
role: User, Developer
level: Intermediate
keywords: azione, personalizzata, API, percorso, configurazione, servizio
exl-id: 2b1b3613-3096-43ec-a860-600dda1d83b2
source-git-commit: 803c9f9f05669fad0a9fdeeceef58652b6dccf70
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 25%

---

# Utilizzare azioni personalizzate {#use-custom-actions}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom"
>title="Azioni personalizzate"
>abstract="Le azioni personalizzate consentono di configurare la connessione di un sistema di terze parti per consentire l’invio di messaggi o chiamate API. Per ciascun provider è possibile configurare un’azione che può essere attivata tramite un’API REST con un payload in formato JSON."

Le azioni personalizzate consentono di configurare la connessione di un sistema di terze parti per consentire l’invio di messaggi o chiamate API. Per ciascun provider è possibile configurare un’azione che può essere attivata tramite un’API REST con un payload in formato JSON.

## Consenso e governance dei dati {#privacy}

In Journey Optimizer, puoi applicare i criteri di governance dei dati e di consenso alle azioni personalizzate per impedire l’esportazione di campi specifici in sistemi di terze parti o escludere i clienti che non hanno acconsentito a ricevere comunicazioni e-mail, push o SMS. Per ulteriori informazioni, consulta le pagine seguenti:

* [Governance dei dati](../action/action-privacy.md).
* [Consenso](../action/consent.md).

## Configurazione URL

Il riquadro di configurazione del **Azione personalizzata** attività mostra i parametri di configurazione dell’URL e i parametri di autenticazione configurati per l’azione personalizzata. Non puoi impostare la parte statica dell’URL nel percorso, ma nella configurazione globale dell’azione personalizzata. [Maggiori informazioni](../action/about-custom-action-configuration.md).

### Percorso dinamico

Se l’URL include un percorso dinamico, specifica il percorso nel **[!UICONTROL Percorso]** campo .

Per concatenare campi e stringhe di testo normale, utilizza le funzioni Stringa o il segno Più (+) nell’editor di espressioni avanzate. Racchiudere le stringhe di testo normale tra virgolette singole (&#39;) o tra virgolette doppie (&quot;). [Maggiori informazioni](expression/expressionadvanced.md).

Questa tabella mostra un esempio di configurazione:

| Campo | Valore |
| --- | --- |
| URL | `https://xxx.yyy.com:8080/somethingstatic/` |
| Percorso | `The id of marketingCampaign + '/messages'` |

L’URL concatenato ha questo modulo:

`https://xxx.yyy.com:8080/somethingstatic/`\&lt;campaign id=&quot;&quot;>`/messages`

![](assets/journey-custom-action-url.png)

### Intestazioni e parametri di query {#headers}

La **[!UICONTROL Configurazione URL]** la sezione mostra i campi dell&#39;intestazione dinamica e del parametro query, ma non i campi costanti. I campi dell’intestazione dinamica e dei parametri di query sono definiti come variabili nella schermata di configurazione dell’azione. [Ulteriori informazioni](../action/about-custom-action-configuration.md#url-configuration)

Per specificare il valore dei campi dell’intestazione dinamica e del parametro della query, fai clic all’interno del campo o sull’icona a forma di matita e seleziona il campo desiderato.

![](assets/journey-dynamicheaderfield.png)

## Parametri azione

In **[!UICONTROL Parametri azione]** vedrai i parametri del messaggio definiti come _&quot;Variabile&quot;_. Per questi parametri, puoi definire dove ottenere queste informazioni (ad esempio: eventi, origini dati), passa i valori manualmente o utilizza l’editor di espressioni avanzate per casi d’uso avanzati. I casi di utilizzo avanzati possono essere di manipolazione dati e di altro utilizzo di funzioni. Fai riferimento a questo [page](expression/expressionadvanced.md).

**Argomenti correlati**

[Configurare un’azione](../action/about-custom-action-configuration.md)
