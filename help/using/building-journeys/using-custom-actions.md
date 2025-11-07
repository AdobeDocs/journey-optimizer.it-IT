---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare azioni personalizzate
description: Scopri come utilizzare le azioni personalizzate
feature: Journeys, Actions, Custom Actions
topic: Content Management
role: User, Developer
level: Intermediate
keywords: azione, personalizzato, API, percorso, configurazione, servizio
exl-id: 2b1b3613-3096-43ec-a860-600dda1d83b2
version: Journey Orchestration
source-git-commit: 221368c7766e942143639fcd554b32f9de5ab0c9
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 20%

---

# Utilizzare azioni personalizzate {#use-custom-actions}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom"
>title="Azioni personalizzate"
>abstract="Le azioni personalizzate consentono di configurare la connessione di un sistema di terze parti per consentire l’invio di messaggi o chiamate API. Per ciascun provider è possibile configurare un’azione che può essere attivata tramite un’API REST con un payload in formato JSON."

Utilizza le azioni personalizzate per abilitare la connessione a un sistema di terze parti per l’invio di messaggi o chiamate API. Per ciascun provider è possibile configurare un’azione che può essere attivata tramite un’API REST con un payload in formato JSON.

Ulteriori informazioni sulle azioni personalizzate in [questa sezione](../action/action.md).

Scopri come creare e configurare un&#39;azione personalizzata in [questa pagina](../action/about-custom-action-configuration.md).

Scopri come utilizzare le risposte alle chiamate API da azioni personalizzate per la personalizzazione in [questa pagina](../action/action-response.md).

## Consenso e governance dei dati {#privacy}

In Journey Optimizer, puoi applicare la governance dei dati e i criteri di consenso alle azioni personalizzate per impedire l’esportazione di campi specifici in sistemi di terze parti o escludere clienti che non hanno acconsentito a ricevere comunicazioni e-mail, push o SMS. Per ulteriori informazioni, consulta le pagine seguenti:

* [Governance dei dati](../action/action-privacy.md).
* [Consenso](../action/consent.md).

## Configurazione URL

Nel riquadro di configurazione dell&#39;attività **Azione personalizzata** sono visualizzati i parametri di configurazione URL e i parametri di autenticazione configurati per l&#39;azione personalizzata. Non è possibile impostare la parte statica dell’URL nel percorso, ma nella configurazione globale dell’azione personalizzata. [Ulteriori informazioni](../action/about-custom-action-configuration.md).

### Percorso dinamico

Se l&#39;URL include un percorso dinamico, specificare il percorso nel campo **[!UICONTROL Percorso]**.

Per concatenare campi e stringhe di testo normale, utilizza le funzioni Stringa o il segno più (+) nell’editor di espressioni avanzate. Racchiudere le stringhe di testo normale tra virgolette singole (&#39;) o doppie (&quot;). [Ulteriori informazioni](expression/expressionadvanced.md).

Questa tabella mostra un esempio di configurazione:

| Campo | Valore |
| --- | --- |
| URL | `https://xxx.yyy.com:8080/somethingstatic/` |
| Percorso | `The _id + '/messages'` |

L’URL concatenato ha il seguente modulo:

`https://xxx.yyy.com:8080/somethingstatic/`\&lt;ID>`/messages`

![](assets/journey-custom-action-url.png)

### Intestazioni e parametri di query {#headers}

La sezione **[!UICONTROL Configurazione URL]** mostra i campi intestazione dinamica e parametro di query, ma non i campi costanti. I campi dell’intestazione dinamica e dei parametri di query sono definiti come variabili nella schermata di configurazione dell’azione. [Ulteriori informazioni](../action/about-custom-action-configuration.md#url-configuration)

Per specificare il valore dei campi con intestazione dinamica e parametri di query, fai clic all’interno del campo o sull’icona a forma di matita e seleziona il campo desiderato.

![](assets/journey-dynamicheaderfield.png)

## Parametri azione

Nella sezione **[!UICONTROL Parametri azione]** verranno visualizzati i parametri del messaggio definiti come _&quot;Variabile&quot;_. Per questi parametri, puoi definire dove ottenere queste informazioni (ad esempio: eventi, origini dati), passare i valori manualmente o utilizzare l’editor di espressioni avanzate per casi d’uso avanzati. I casi d’uso avanzati possono essere la manipolazione dei dati e altro utilizzo di funzioni. Consulta [questa pagina](expression/expressionadvanced.md).

