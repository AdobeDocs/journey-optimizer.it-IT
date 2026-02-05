---
title: Configurazione schede di contenuto Web SDK
description: Configurare il supporto per le schede di contenuto in Web SDK
feature: Channel Configuration, Content Cards
topic: Content Management
role: Admin
level: Experienced
exl-id: bb67b55f-2eac-4775-a9f5-78288009477e
source-git-commit: 37862682a25843ce138c076e443f6d9b6229ece3
workflow-type: tm+mt
source-wordcount: '484'
ht-degree: 4%

---

# Configurare il supporto per le schede di contenuto in Web SDK {#content-card-configuration-sdk}

In questo esempio viene illustrato come recuperare le schede di contenuto da Adobe Journey Optimizer (AJO) tramite Adobe Experience Platform. Sfruttando [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/it/docs/experience-platform/web-sdk/home), il contenuto di personalizzazione viene recuperato e renderizzato interamente sul lato client.

Al caricamento della pagina iniziale, viene visualizzato lo stato predefinito della pagina. Tuttavia, se interagisci con i pulsanti **Fondi di deposito** o **Condividi sui social media**, verranno visualizzate schede di contenuto aggiuntive. Queste schede vengono attivate da condizioni lato client, garantendo che vengano visualizzate solo quando vengono intraprese azioni specifiche.

![](assets/content-card-web-1.png)

## Esecuzione dell’esempio {#run-sample}

>[!PREREQUISITES]
>
>È necessario installare node e npm. [Consulta questa documentazione](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm)


1. Imposta i certificati SSL locali per HTTPS. Questi esempi richiedono certificati SSL firmati localmente per distribuire il contenuto tramite HTTPS:

   1. Installa `mkcert` nel computer.

   1. Dopo l&#39;installazione, eseguire `mkcert -install` per installare il certificato `mkcert root`.

1. Clona l’archivio nel computer locale.

1. Apri un terminale e passa alla cartella dell’esempio.

1. Installare le dipendenze richieste eseguendo `npm install`.

1. Avviare l&#39;applicazione eseguendo `npm start`.

1. Apri il browser Web e passa a `https://localhost`.

## Come funziona {#setup}

1. Includi e configura il [Web SDK](https://experienceleague.adobe.com/it/docs/experience-platform/web-sdk/home) nella pagina utilizzando le impostazioni del file `.env` nella cartella di esempio.

   ```
   <script src="https://cdn1.adoberesources.net/alloy/2.18.0/alloy.min.js" async></script>
   alloy("configure", {
       defaultConsent: "in",
       edgeDomain: "{{edgeDomain}}",
       edgeConfigId: "{{edgeConfigId}}",
       orgId:"{{orgId}}",
       debugEnabled: false,
       personalizationStorageEnabled: true,
       thirdPartyCookiesEnabled: false
   });
   ```

1. Utilizza il comando `sendEvent` per recuperare il contenuto personalizzato.

   ```
   alloy("sendEvent", {
       renderDecisions: true,
       personalization: {
           surfaces: ["web://alloy-samples.adobe.com/#content-cards-sample"],
       },
   });
   ```

1. Sottoscrivere le schede di contenuto per una superficie specifica utilizzando il comando `subscribeRulesetItems`. Ogni volta che vengono valutati i set di regole, gestisci l&#39;oggetto risultato nel callback, che conterrà `propositions` con i dati della scheda contenuto.

   ```
   const contentCardManager = createContentCardManager("content-cards");
   
   alloy("subscribeRulesetItems", {
       surfaces: ["web://alloy-samples.adobe.com/#content-cards-sample"],
       schemas: ["https://ns.adobe.com/personalization/message/content-card"],
       callback: (result, collectEvent) => {
           const { propositions = [] } = result;
           contentCardManager.refresh(propositions, collectEvent);
       },
   });
   ```

1. Gestisci il rendering delle schede di contenuto e invia `interact` e `display` eventi utilizzando l&#39;oggetto `contentCardsManager` trovato in `script.js`. Estrai, ordina ed elabora schede di contenuto dalle proposte ricevute.

   ```
   const createContentCard = (proposition, item) => {
       const { data = {}, id } = item;
       const {
           content = {},
           meta = {},
           publishedDate,
           qualifiedDate,
           displayedDate,
       } = data;
   
       return {
           id,
           ...content,
           meta,
           qualifiedDate,
           displayedDate,
           publishedDate,
           getProposition: () => proposition,
       };
   };
   
   const extractContentCards = (propositions) =>
       propositions
           .reduce((allItems, proposition) => {
           const { items = [] } = proposition;
   
           return [
               ...allItems,
               ...items.map((item) => createContentCard(proposition, item)),
           ];
       }, [])
       .sort(
           (a, b) =>
               b.qualifiedDate - a.qualifiedDate || b.publishedDate - a.publishedDate
       );
   
   const contentCards = extractContentCards(propositions);
   ```

1. Esegui il rendering delle schede di contenuto in base ai dettagli definiti per ciascuna campagna. Ogni scheda include `title`, `body`, `imageUrl` e altri valori di dati personalizzati.

   ```
   const renderContentCards = () => {
       const contentCardsContainer = document.getElementById(containerElementId);
       contentCardsContainer.addEventListener("click", handleContentCardClick);
   
       let contents = "";
   
       contentCards.forEach((card) => {
           const { id, title, body, imageUrl, meta = {} } = card;
           const { buttonLabel = "" } = meta;
   
           contents += `
               <div class="col">
                   <div data-id="${id}" class="card h-100">
                       <img src="${imageUrl}" class="card-img-top" alt="...">
                       <div class="card-body d-flex flex-column">
                           <h5 class="card-title">${title}</h5>
                           <p class="card-text">${body}</p>
                           <a href="#" class="mt-auto btn btn-primary">${buttonLabel}</a>
                       </div>
                   </div>
                </div>
            `;
       });
   
       contentCardsContainer.innerHTML = contents;
       collectEvent(
           "display",
           contentCards.map((card) => card.getProposition())
        );
   };
   ```

1. Quando viene richiamato il callback `subscribeRulesetItems`, viene fornita anche una funzione di convenienza denominata `collectEvent`. Questa funzione viene utilizzata per inviare eventi Experience Edge per monitorare interazioni, visualizzazioni e altre azioni dell’utente. In questo esempio, collectEvent tiene traccia di quando si fa clic su una scheda di contenuto. Inoltre, se fai clic sul pulsante sulla scheda dei contenuti, il browser viene indirizzato a `actionUrl` specificato dalla campagna.

   ```
   const handleContentCardClick = (evt) => {
       const cardEl = evt.target.closest(".card");
   
       if (!cardEl) {
           return;
       }
   
       const isAnchor = evt.target.nodeName === "A";
       const card = contentCards.find((card) => card.id === cardEl.dataset.id);
   
       if (!card) {
           return;
       }
   
       collectEvent("interact", [card.getProposition()]);
   
       if (isAnchor) {
           evt.preventDefault();
           evt.stopImmediatePropagation();
           const { actionUrl } = card;
           if (actionUrl && actionUrl.length > 0) {
               window.location.href = actionUrl;
           }
       }
   };
   ```

## Osservazioni chiave {#key-observations}

### personalizationStorageEnabled

Opzione `personalizationStorageEnabled` impostata su `true` nel comando `configure`. In questo modo, le schede di contenuto precedentemente qualificate vengono memorizzate e continuano a essere visualizzate nelle diverse sessioni utente.

### Trigger

Le schede di contenuto supportano trigger personalizzati valutati sul lato client. Quando viene soddisfatta una regola di attivazione, vengono visualizzate schede di contenuto aggiuntive. In questo esempio vengono utilizzate quattro campagne diverse, una per ogni scheda di contenuto, che condividono tutte la stessa superficie: `web://alloy-samples.adobe.com/#content-cards-sample`. La tabella seguente illustra le regole di attivazione per ogni campagna e come soddisfarle.

<table>
    <tr>
        <th>Regola di attivazione</th>
        <th>Scheda</th>
        <th>Come soddisfare la regola di attivazione</th>
    </tr>
    <tr>
        <td>Nessuna</td>
        <td><img src="assets/content-card-web-2.png"></td>
        <td>comando sendEvent. Nessuna regola lato client da soddisfare.</td>
    </tr>
    <tr>
        <td>Nessuna</td>
        <td><img src="assets/content-card-web-3.png"></td>
        <td>comando sendEvent. Nessuna regola lato client da soddisfare.</td>
    </tr>
    <tr>
        <td><img src="assets/content-card-web-4.png"></td>
        <td><img src="assets/content-card-web-5.png"></td>
        <td><img src="assets/content-card-web-6.png"></td>
    </tr>
    <tr>
        <td><img src="assets/content-card-web-7.png"></td>
        <td><img src="assets/content-card-web-8.png"></td>
        <td><img src="assets/content-card-web-9.png"></td>
    </tr>
</table>

Il comando `evaluateRulesets` viene attivato quando si fa clic sui pulsanti &quot;Fondi di deposito&quot; e &quot;Condividi sui social media&quot;. Ogni pulsante specifica il `decisionContext` pertinente per soddisfare le regole definite per le rispettive campagne.

```
document.getElementById("action-button-1").addEventListener("click", () => {
    alloy("evaluateRulesets", {
        renderDecisions: true,
        personalization: {
            decisionContext: {
                action: "deposit-funds",
            },
        },
    });
});

document.getElementById("action-button-2").addEventListener("click", () => {
    alloy("evaluateRulesets", {
        renderDecisions: true,
        personalization: {
            decisionContext: {
                action: "social-media",
            },
        },
    });
});
```
