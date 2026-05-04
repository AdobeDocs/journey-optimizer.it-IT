---
solution: Journey Optimizer
product: journey optimizer
title: Abilita integrazioni esterne
description: Integra integrazioni esterne nel processo di authoring dei canali per arricchire i contenuti con informazioni personalizzate e dinamiche
feature: Integrations
topic: Content Management
role: User
level: Beginner
keywords: integrazione
source-git-commit: 4cc3c959fe08c1d574a5d041bf7721441bc96f97
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 1%

---


# Utilizzo di integrazioni esterne per la personalizzazione {#integrations-personalization}

Prima di utilizzare le integrazioni esterne nel contenuto, verificare che un amministratore abbia **configurato e attivato** ogni integrazione (endpoint, autenticazione, criteri, payload di risposta e attivazione) come descritto in [Operazioni con le integrazioni](integrations.md).

Puoi aggiungere fino a **3** integrazioni per **[!UICONTROL Frammento]** e fino a **5** nel messaggio. Le integrazioni provenienti solo da frammenti non vengono conteggiate per **5**.

## Applicare la personalizzazione dell’integrazione al contenuto {#apply-integration-personalization}

In qualità di addetto marketing, puoi utilizzare integrazioni configurate per personalizzare il contenuto. Segui questi passaggi:

1. Accedi al contenuto della tua campagna e fai clic su **[!UICONTROL Aggiungi personalizzazione]** dal tuo **[!UICONTROL Componenti]** di testo o HTML.

   [Ulteriori informazioni sui componenti](../email/content-components.md)

   ![](assets/external-integration-content-1.png)

1. Passa alla sezione **[!UICONTROL Integrazioni]** e fai clic su **[!UICONTROL Apri integrazioni]** per visualizzare tutte le integrazioni attive.

   I **frammenti di Journey Optimizer** sono disponibili con le integrazioni ma supportano solo i canali in uscita. Dopo la pubblicazione di un frammento, l’aggiunta e il salvataggio di nuove integrazioni viene disattivato per evitare un impatto sui percorsi e sulle campagne esistenti.

   ![](assets/external-integration-content-2.png)

1. Seleziona un&#39;integrazione e fai clic su **[!UICONTROL Salva]**.

   ![](assets/external-integration-content-3.png)

1. Attiva la modalità **[!UICONTROL Pillole]** per sbloccare il menu di integrazione avanzato.

   ![](assets/external-integration-content-4.png)

1. Quando si crea la personalizzazione dell&#39;integrazione, l&#39;helper integrazioni include un campo **`required`** che definisce il modo in cui gli errori o i dati mancanti interagiscono con il contenuto predefinito:

   * **`required=true`** (impostazione predefinita): il rendering viene interrotto per il messaggio. L&#39;invio è escluso con **`ExternalDataLookupExclusion`** e tale esclusione è registrata nel **set di dati di feedback del messaggio**.
   * **`required=false`**: la variabile dei risultati è impostata su **`null`** e il rendering continua. Utilizza testo predefinito, fallback o logica condizionale nel modello, in modo che i profili non ricevano contenuto vuoto quando l’integrazione non restituisce dati.

     ![](assets/external-integration-content-8.png)

1. Per completare la configurazione dell&#39;integrazione, definire gli attributi di integrazione specificati in precedenza durante la [configurazione](integrations.md#configure).

   Puoi assegnare valori a questi attributi utilizzando valori statici, che rimangono costanti, o attributi di profilo, che estraggono informazioni in modo dinamico dai profili utente.

   ![](assets/external-integration-content-5.png)

1. Una volta definiti gli attributi di integrazione, puoi utilizzare i campi di integrazione nel contenuto per la messaggistica personalizzata facendo clic sull&#39;icona ![aggiungi](assets/do-not-localize/Smock_Add_18_N.svg).

   ![](assets/external-integration-content-6.png)

   >[!NOTE]
   >
   >I token nel modello devono utilizzare solo i campi esposti dall&#39;amministratore nella configurazione dell&#39;integrazione. Ad esempio, `{{weatherResponse.temperature}}` è valido quando `temperature` è esposto; `{{weatherResponse.humidity}}` è rifiutato nell&#39;editor se `humidity` non è stato esposto.

1. Fai clic su **[!UICONTROL Salva]**.

La personalizzazione dell’integrazione ora viene applicata correttamente al contenuto, garantendo a ogni destinatario un’esperienza personalizzata e rilevante in base agli attributi configurati.

![](assets/external-integration-content-7.png)

<!--

## Map one API call to another {#map-integration-chain}

You can **chain** integrations so that values returned by one active integration drive the inputs (path, headers, or query parameters) of another. That lets you build a real-time data flow in a single message without custom code.

Before you start, make sure that:

* An administrator has configured and activated every integration you need. See [Configure your Integration](integrations.md).
* Variable path placeholders, headers, and query parameters are set up in the integration configuration with marketer-facing labels.
* The administrator exposed the response fields you need in each integration's **[!UICONTROL Response payload]** so they appear when authoring.

In the below example, a reservation system integration returns a flight booking reference from the profile context. A separate flight-information integration expects that reference as a **path variable**. In the personalization editor, you map the second integration's variable to a field from the first integration's response, instead of a static value or profile attribute alone.

1. Open your message or fragment and place the cursor where you want personalized content (for example, a **[!UICONTROL Text]** field).

1. Open the personalization editor and go to **[!UICONTROL Integrations]** → **[!UICONTROL Open integrations]**.

1. Select the integration whose output will supply the downstream input (in the example, the reservation or profile API that returns the flight identifier).

1. Define that integration's inputs as usual—static values, profile attributes, or other allowed mappings—then save so its response is available for chaining.

    >[!NOTE]
    >
    > Fields must appear in the administrator-defined response payload for each integration. You cannot reference response properties that were not exposed in configuration.

1. Select the **second** integration (for example, the API that needs the flight number or booking reference on the URL path).

1. For each input that must come from the first call—often a **path variable** or **variable** header/query parameter—choose the mapping source that references the **first integration's response** (for example, the flight booking reference field from the reservation payload). Do not use a static test value if you need live, profile-specific data.

1. Insert the response tokens you need in the content (for example, destination name from the flight API, loyalty balance from a loyalty integration) using the ![add](assets/do-not-localize/Smock_Add_18_N.svg) control.

1. Save the personalization.

When you **simulate** or send, Journey Optimizer resolves integrations in order: the first call runs with the profile context you configured; its output is used to build the second request. Different integrations may run at simulation time and at send time according to your setup and channel behavior.

-->

## Video introduttivo {#video}

Questo video mostra come le **Integrazioni** collegano Adobe Journey Optimizer alle API esterne in modo da poter richiamare dati e contenuti live in **canali in uscita**, e-mail, SMS e push, per una personalizzazione più rilevante.

>[!VIDEO](https://video.tv.adobe.com/v/3484126/?captions=ita&learn=on)
