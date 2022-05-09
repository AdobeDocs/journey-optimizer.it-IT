---
title: Consegnare offerte tramite l’API Edge Decisioning
description: L’SDK per web di Adobe Experience Platform consente di recuperare ed eseguire il rendering delle offerte personalizzate create utilizzando le API o la Libreria offerte.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 4e2dc0d6-4610-4a2f-8388-bc58182b227f
source-git-commit: 79d3bd42c208d38aaebce742e70b247106c21587
workflow-type: tm+mt
source-wordcount: '1049'
ht-degree: 2%

---

# Consegnare offerte tramite l’API Edge Decisioning {#edge-decisioning-api}

## Guida introduttiva e prerequisiti {#edge-overview-and-prerequisites}

La [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html#video-overview) è una libreria JavaScript lato client che consente ai clienti Adobe Experience Cloud di interagire con i vari servizi dell’Experience Cloud tramite Experience Platform Edge Network.

L’SDK per web di Experience Platform supporta l’esecuzione di query sulle soluzioni di personalizzazione all’Adobe, inclusa la gestione delle decisioni, e consente di recuperare ed eseguire il rendering delle offerte personalizzate create utilizzando le API o la Libreria offerte. Per istruzioni più dettagliate, consulta la documentazione su [creazione di un’offerta](../../get-started/starting-offer-decisioning.md).

Esistono due modi per implementare l’Offer decisioning con il [SDK per web per Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html#video-overview). Un modo è rivolto agli sviluppatori e richiede la conoscenza dei siti web e la programmazione. L’altro modo consiste nell’utilizzare l’interfaccia utente di Adobe Experience Platform per configurare offerte che richiedono solo un riferimento a un piccolo script nell’intestazione della pagina HTML.

Consulta la documentazione su [offer decisioning](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/offer-decisioning/offer-decisioning-overview.html?lang=en#enabling-offer-decisioning) per ulteriori informazioni su come distribuire offerte personalizzate utilizzando l’SDK per web di Platform.

>[!NOTE]
>
>L’utilizzo di Gestione delle decisioni in Adobe Experience Platform Web SDK è attualmente disponibile in fase di accesso anticipato a determinati utenti. Questa funzionalità non è disponibile per tutte le organizzazioni.

## Adobe Experience Platform Web SDK {#aep-web-sdk}

Platform Web SDK sostituisce i seguenti SDK:

* Visitor.js
* AppMeasurement.js
* AT.js
* DIL.js

L&#39;SDK non ha combinato queste librerie ed è una nuova implementazione da zero. Per utilizzarlo, devi prima seguire questi passaggi:

1. Verifica che la tua organizzazione disponga delle autorizzazioni appropriate per utilizzare l&#39;SDK e che le autorizzazioni siano state configurate correttamente.

   <!-- For more detailed instructions, refer to the documentation on using the [Adobe Experience Platform Web SDK](). -->

1. [Configurare il datastream](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/datastreams.html?lang=en) nella scheda Raccolta dati del tuo account in Adobe Experience Cloud.

1. Installa l&#39;SDK. Esistono diversi metodi per farlo, che sono coperti [Installare la pagina SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=en). Questa pagina continuerà con ogni metodo di implementazione diverso.

Per usare l&#39;SDK, devi disporre di un [schema](../../../start/get-started-schemas.md) e [datastream](../../../start/get-started-datasets.md) definito.

<!-- ****TODO - Configure schema**** -->

Per personalizzare le offerte, devi configurare separatamente la personalizzazione/i profili.

<!-- Refer to the [doc](www.link.com) for detailed instructions.  -->

Per configurare l&#39;SDK, ad Offer decisioning, segui uno dei due passaggi seguenti:

## Opzione 1 - Installare l’estensione e l’implementazione del tag utilizzando Launch

Questa opzione è più semplice da usare per le persone che hanno meno esperienza di codifica.

1. [Creare una proprietà tag](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/companies-and-properties.html?lang=en)

1. [Aggiungere il codice di incorporamento ](https://experienceleague.adobe.com/docs/core-services-learn/implementing-in-websites-with-launch/configure-launch/launch-add-embed.html?lang=en)

1. Installa e configura l’estensione Platform Web SDK con il Datastream creato selezionando la configurazione dal menu a discesa &quot;Datastream&quot;. Consulta la documentazione su [estensioni](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/extensions/overview.html?lang=en).

   ![Adobe Experience Platform Web SDK](../../assets/installed-catalog-web-sdk.png)

   ![Configura estensione](../../assets/configure-sdk-extension.png)

1. Crea il necessario [Elementi dati](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/data-elements.html?lang=en). Come minimo, devi creare una mappa di identità web SDK per Platform e un elemento dati di oggetto XDM per l’SDK per web per Platform.

   ![Mappa delle identità](../../assets/sdk-identity-map.png)

   ![Oggetto XDM](../../assets/xdm-object.png)

1. Crea il tuo [Regole](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/rules.html?lang=en):

   Aggiungi un’azione Send Event dell’SDK per web di Platform e aggiungi gli ambiti decisionali rilevanti alla configurazione di quell’azione.

   ![Offerta di rendering](../../assets/rule-render-offer.png)

   ![Offerta di richiesta](../../assets/rule-request-offer.png)

1. [Creare e pubblicare](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/libraries.html?lang=en) una libreria contenente tutte le regole, gli elementi dati e le estensioni pertinenti che hai configurato.

## Opzione 2 - Implementazione manuale utilizzando la versione standalone predefinita

Di seguito sono riportati i passaggi necessari per utilizzare Offer Decisioning utilizzando l’installazione autonoma predefinita dell’SDK web. Questa guida presuppone che questa sia la prima volta che implementi l&#39;SDK, pertanto tutti i passaggi potrebbero non essere applicabili al tuo caso. Questa guida presuppone anche un’esperienza di sviluppo.

Includere il seguente frammento JavaScript dall&#39;opzione 2: Versione standalone integrata su [questa pagina](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=en) in `<head>` della pagina HTML.

```
javascript
    <script>
        !function(n,o){o.forEach(function(o){n[o]||((n.__alloyNS=n.__alloyNS||
        []).push(o),n[o]=function(){var u=arguments;return new Promise(
        function(i,l){n[o].q.push([i,l,u])})},n[o].q=[])})}
        (window,["alloy"]);
    </script>
    <script src="https://cdn1.adoberesources.net/alloy/2.6.4/alloy.js" async></script>
```

Per impostare la configurazione dell&#39;SDK, avrai bisogno di due ID dall&#39;interno dell&#39;account Adobe: il tuo edgeConfigId e il tuo orgId. edgeConfigId è lo stesso dell&#39;ID Datastream, che dovresti aver configurato nei prerequisiti.

Per trovare il tuo edgeConfigID/datastream ID, vai a Raccolta dati e seleziona il tuo Datastream. Per trovare il tuo orgId, vai al tuo profilo.

Configura l&#39;SDK in JavaScript seguendo le istruzioni presenti in questa pagina. Utilizzerai sempre il tuo edgeConfigId e orgId nella funzione di configurazione. La documentazione descrive anche i parametri facoltativi esistenti per la configurazione. La configurazione finale potrebbe essere simile alla seguente:

```
javascript
    alloy("configure", {
        "edgeConfigId": "12345678-0ABC-DEF-GHIJ-KLMNOPQRSTUV",                            
        "orgId":"ABCDEFGHIJKLMNOPQRSTUVW@AdobeOrg",
        "debugEnabled": true,
        "edgeDomain": "edge.adobedc.net",
        "clickCollectionEnabled": true,
        "idMigrationEnabled": true,
        "thirdPartyCookiesEnabled": true,
        "defaultConsent":"in"  
    });
```

Installa l’estensione Debugger Chrome da utilizzare con il debug. Si trova qui: <https://chrome.google.com/webstore/detail/adobe-experience-platform/bfnnokhpnncpkdmbokanobigaccjkpob>

Quindi, accedi al tuo account all&#39;interno del debugger. Quindi, vai a Registri e assicurati di essere connesso all&#39;area di lavoro corretta. Ora, copia la versione codificata base64 dell’ambito decisionale dalla tua offerta.

Durante la modifica del sito web, includi lo script con la configurazione e il `sendEvent` per inviare l&#39;ambito decisionale all&#39;Adobe.

**Esempio**:

```
javascript
    alloy("sendEvent", {
        "decisionScopes": 
        [
        "eyJ4ZG06YWN0aXZpdHlJZCI6Inhjb3JlOm9mZmVyLWFjdGl2aXR5OjE0ZWE4MDhhZjJjZDM1NzQiLCJ4ZG06cGxhY2VtZW50SWQiOiJ4Y29yZTpvZmZlci1wbGFjZW1lbnQ6MTRjNGFmZDI2OTXXXXXXXXXX"
        ]
    });
```

Per un esempio su come gestire la risposta, consulta quanto segue:

```
javascript
    alloy("sendEvent", {
        "decisionScopes":
        [
        "eyJ4ZG06YWN0aXZpdHlJZCI6Inhjb3JlOm9mZmVyLWFjdGl2aXR5OjE0ZWE4MDhhZjJjZDM1NzQiLCJ4ZG06cGxhY2VtZW50SWQiOiJ4Y29yZTpvZmZlci1wbGFjZW1lbnQ6MTRjNGFmZDI2OTXXXXXXXXXX"
        ]
    }).then(function(result) {
        Object.entries(result).forEach(([key, value]) => {
            console.log(key, value);
        });
    });
```

Puoi utilizzare il debugger per verificare di essere stato connesso correttamente alla rete Edge.

>[!NOTE]
>
>Se nei registri non viene visualizzata una connessione al bordo, potrebbe essere necessario disattivare il ad blocker.

Fai riferimento alla modalità di creazione dell’offerta e alla formattazione utilizzata. In base ai criteri soddisfatti nella decisione, ti verrà restituita un’offerta contenente le informazioni specificate al momento della creazione all’interno di Adobe Experience Platform.

In questo esempio, il JSON da restituire è:

```
json
{
   "name":"ABC Test",
   "description":"This is a test offer", 
   "link":"https://sampletesting.online/",
   "image":"https://sample-demo-URL.png"
}
```

Gestisci l&#39;oggetto di risposta e analizza i dati necessari. Poiché puoi inviare più ambiti decisionali in uno `sendEvent` call, la tua risposta potrebbe essere leggermente diversa.

```
json
    {
        "id": "abrxgl843d913",
        "scope": "eyJ4ZG06YWN0aXZpdHlJZCI6Inhjb3JlOm9mZmVyLWFjdGl2aXR5OjE0ZWE4MDhhZjJjZDM1NzQiLCJ4ZG06cGxhY2VtZW50SWQiOiJ4Y29yZTpvZmZlci1wbGFjZW1lbnQ6MTRjNGFmZDI2OTVlNWRmOSJ9",
        "items": 
        [
            {
                "id": "xcore:fallback-offer:14ea7f1ea26ebd0a",
                "etag": "1",
                "schema": "https://ns.adobe.com/experience/offer-management/content-component-json",
                "data": {
                    "id": "xcore:fallback-offer:14ea7f1ea26ebd0a",
                    "format": "application/json",
                    "language": [
                        "en-us"
                    ],
                    "content": "{\"name\":\"ABC Test\",\"description\":\"This is a test offer\", \"link\":\"https://sampletesting.online/\",\"image\":\"https://sample-demo-URL.png\"}"
                }
            }
        ]
    }
]
}
```

```
json
{
    "propositions": 
    [
    {
        "renderAttempted": false,
        "id": "e15ecb09-993e-4b66-93d8-0a4c77e3d913",
        "scope": "eyJ4ZG06YWN0aXZpdHlJZCI6Inhjb3JlOm9mZmVyLWFjdGl2aXR5OjE0ZWE4MDhhZjJjZDM1NzQiLCJ4ZG06cGxhY2VtZW50SWQiOiJ4Y29yZTpvZmZlci1wbGFjZW1lbnQ6MTRjNGFmZDI2OTVlNWRmOSJ9",
        "items": 
        [
            {
                "id": "xcore:fallback-offer:14ea7f1ea26ebd0a",
                "etag": "1",
                "schema": "https://ns.adobe.com/experience/offer-management/content-component-json",
                "data": {
                    "id": "xcore:fallback-offer:14ea7f1ea26ebd0a",
                    "format": "application/json",
                    "language": [
                        "en-us"
                    ],
                    "content": "{\"name\":\"Claire Hubacek Test\",\"description\":\"This is a test offer\", \"link\":\"https://sampletesting.online/\",\"image\":\"https://sample-demo-URL.png\"}"
                }
            }
        ]
    }
    ]
}
```

In questo esempio, il percorso necessario per gestire e utilizzare i dettagli specifici dell’offerta nella pagina web era: `result['decisions'][0]['items'][0]['data']['content']`

Per impostare le variabili JS:

```
javascript
const offer = JSON.parse(result['decisions'][0]['items'][0]['data']['content']);

let offerURL = offer['link'];
let offerDescription = offer['description'];
let offerImageURL = offer['image'];

document.getElementById("offerDescription").innerHTML = offerDescription;
document.getElementById('offerImage').src = offerImageURL;
```

## Limitazioni 

Alcuni vincoli di offerta non sono attualmente supportati con i flussi di lavoro Experience Edge per dispositivi mobili, ad esempio Limitazione di utilizzo. Il valore del campo Limitazione di utilizzo specifica il numero di volte in cui un’offerta può essere presentata a tutti gli utenti. Per ulteriori dettagli, consulta [Aggiungere vincoli a un’offerta](../../offer-library/add-constraints.md#capping).
