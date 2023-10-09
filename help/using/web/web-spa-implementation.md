---
title: Implementazione di un'applicazione a pagina singola
description: Scopri come implementare le visualizzazioni SPA in Journey Optimizer
feature: Web Channel
topic: Content Management
role: User
level: Intermediate
exl-id: c36d793d-0aa6-4a7a-94f2-dbfe6b644df8
source-git-commit: c4ab97999d000d969f6f09f4d84be017d1288f94
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 2%

---

# Implementare applicazioni a pagina singola (SPA) {#web-spa-implementation}

Adobe Experience Platform Web SDK offre funzioni avanzate che consentono di eseguire personalizzazioni su tecnologie lato client di nuova generazione, come le applicazioni a pagina singola (SPA).

I siti web tradizionali funzionano su modelli di navigazione &quot;da pagina a pagina&quot;, altrimenti noti come applicazioni a più pagine, in cui le progettazioni del sito web sono strettamente collegate a URL e le transizioni da una pagina web a un’altra richiedono un caricamento di pagina.

Le applicazioni web moderne, come le applicazioni a pagina singola (SPA), hanno invece adottato un modello che attiva rapidamente il rendering dell’interfaccia utente del browser, spesso indipendente dai ricaricamenti delle pagine. Queste esperienze possono essere attivate dalle interazioni dei clienti, ad esempio scorrimento, clic e movimenti del cursore. Con l’evoluzione dei paradigmi del web moderno, la rilevanza degli eventi generici tradizionali, come il caricamento di una pagina, per distribuire personalizzazione e sperimentazione non funziona più.

![](assets/web-spa-vs-traditional-lifecycle.png)

## Vantaggi di Adobe Experience Platform Web SDK per SPA {#web-spa-benefits}

Di seguito sono riportati alcuni vantaggi dell’utilizzo di Adobe Experience Platform Web SDK per le applicazioni a pagina singola:

* Capacità di memorizzare nella cache tutte le offerte al caricamento di pagina per ridurre più chiamate al server a una singola chiamata al server.
* Migliora enormemente l’esperienza utente sul sito, in quanto le offerte appaiono immediatamente tramite la cache senza il ritardo causato dalle chiamate al server tradizionali.
* La configurazione per sviluppatori una tantum consente agli esperti di marketing di creare ed eseguire attività di personalizzazione e sperimentazione tramite l’editor visivo web di Adobe Journey Optimizer sull’SPA.

## Visualizzazioni XDM e applicazioni a pagina singola {#web-spa-xdm}

L’Adobe **[!UICONTROL Journey Optimizer]** l’editor web sfrutta un concetto chiamato visualizzazioni: un gruppo logico di elementi visivi che insieme formano un’esperienza SPA. Un’applicazione a pagina singola può, pertanto, essere considerata come transizione attraverso le viste, anziché gli URL, in base alle interazioni dell’utente. In genere, una visualizzazione può rappresentare un intero sito, una singola pagina o elementi visivi raggruppati all’interno di una pagina.

Per spiegare ulteriormente le visualizzazioni, nell&#39;esempio seguente viene utilizzato un ipotetico sito di e-commerce online.

* Dopo aver visitato la home page, un’immagine protagonista promuove le raccolte stagionali e i diversi cataloghi di prodotti disponibili sul sito. In questo caso, è possibile definire una visualizzazione per l&#39;intera schermata iniziale. Questa visualizzazione potrebbe essere chiamata semplicemente &quot;home&quot;.

  ![](assets/web-spa-home.png)

* Quando il cliente diventa più interessato ai prodotti venduti dall’azienda, decide di fare clic sul pulsante **Uomini** collegamento. Simile alla home page, l&#39;intero **Uomini** può essere definita come visualizzazione. Questa visione potrebbe essere chiamata &quot;uomini&quot;.

  ![](assets/web-spa-men.png)

* Poiché una visualizzazione può essere definita come un intero sito o come un gruppo di elementi visivi in un sito, i quattro prodotti visualizzati nel sito dei prodotti possono essere raggruppati e considerati come una visualizzazione. Questa visualizzazione potrebbe essere denominata &quot;products&quot; (prodotti).

  ![](assets/web-spa-men-products.png)

* Quando il cliente decide di fare clic su **TUTTI I PRODOTTI DA UOMO** per esplorare altri prodotti sul sito, l’URL del sito web non cambia in questo caso, ma è possibile creare una visualizzazione qui per rappresentare solo la seconda riga di prodotti visualizzati. Il nome della visualizzazione potrebbe essere &quot;products-page-2&quot;.

* Il cliente decide di acquistare alcuni prodotti dal sito e procede alla schermata di pagamento. Lo schermo del carrello stesso può essere associato a una visualizzazione denominata &quot;carrello&quot;. Oppure puoi avere una visualizzazione diversa all&#39;interno della schermata di pagamento per gestire i prodotti consigliati di seguito.

  ![](assets/web-spa-cart.png)

Il concetto di visualizzazioni può essere esteso molto di più. Questi sono solo alcuni esempi di visualizzazioni che possono essere definite su un sito.

## Implementazione delle visualizzazioni XDM {#implement-xdm-views}

Le viste XDM possono essere utilizzate in Adobe Journey Optimizer per consentire agli addetti al marketing di eseguire campagne di personalizzazione web e sperimentazione sull’SPA tramite l’editor visivo web di Journey Optimizer.

Per completare la configurazione per sviluppatori una tantum, è necessario eseguire i passaggi seguenti:

1. Installa [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/installing-the-sdk.html?lang=it){target="_blank"} e controlla [prerequisiti per il canale web](web-prerequisites.md) pagina.

2. Determina tutte le viste XDM nell’applicazione a pagina singola che desideri personalizzare.

3. Dopo aver definito le viste XDM, per distribuire i contenuti a tali viste, devi implementare `sendEvent()` funzione con `renderDecisions` imposta su `true` e la vista XDM corrispondente nell’applicazione a pagina singola. La vista XDM deve essere trasmessa `xdm.web.webPageDetails.viewName`. Questo passaggio consente agli esperti di marketing di scoprire queste visualizzazioni all’interno dell’editor web di Journey Optimizer e di applicare loro le modifiche ai contenuti:

```
 alloy("sendEvent", {
  "renderDecisions": true,
  "xdm": {
   "web": {
    "webPageDetails": {
    "viewName":"home"
   }
  }
 }
});
```

>[!NOTE]
>
>Al primo `sendEvent()` chiamata, tutte le viste XDM di cui deve essere eseguito il rendering per l’utente finale verranno recuperate e memorizzate nella cache. Successivo `sendEvent()` le chiamate con viste XDM passate verranno lette dalla cache e sottoposte a rendering senza una chiamata al server.

## `sendEvent()` esempi di funzioni

Questa sezione illustra due esempi che mostrano come richiamare `sendEvent()` funzione in React per un ipotetico SPA di e-commerce.

### Esempio 1: home page per test A/B {#web-spa-sample-1}

Il team marketing desidera eseguire test A/B sull’intera home page.

![](assets/web-spa-home.png)

Per eseguire test A/B sull&#39;intero sito principale, `sendEvent()` deve essere richiamato con XDM `viewName` imposta su `home`:

```
function onViewChange() {

  var viewName = window.location.hash; // or use window.location.pathName if router works on path and not hash

  viewName = viewName || 'home'; // view name cannot be empty

  // Sanitize viewName to get rid of any trailing symbols derived from URL

  if (viewName.startsWith('#') || viewName.startsWith('/')) {
    viewName = viewName.substr(1);
  }

  alloy("sendEvent", {
    "renderDecisions": true,

    "xdm": {
      "web": {
        "webPageDetails": {
          "viewName":"home"
        }
      }
    }
  });
}

// react router v4

const history = syncHistoryWithStore(createBrowserHistory(), store);

history.listen(onViewChange);

// react router v3

<Router history={hashHistory} onUpdate={onViewChange} >
```

### Esempio 2: prodotti personalizzati {#web-spa-sample-2}

Il team marketing vuole personalizzare la seconda riga di prodotti cambiando il colore dell’etichetta del prezzo in rosso dopo che un utente fa clic per visualizzare tutti i prodotti da uomo.

![](assets/web-spa-men-products.png)

```
function onViewChange(viewName) {

  alloy("sendEvent", {
    "renderDecisions": true,
    "xdm": {
      "web": {
        "webPageDetails": {
          "viewName": viewName
        }
      }
    }
  });
}

class Products extends Component {

  render() {
    return (

        <button type="button" onClick={this.handleLoadMoreClicked}>All Men's Products</button>
    );
  }

  handleLoadMoreClicked() {
    var page = this.state.page + 1; // assuming page number is derived from component's state
    this.setState({page: page});
    onViewChange('PRODUCTS-PAGE-' + page);
  }

}
```
