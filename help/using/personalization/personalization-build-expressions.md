---
solution: Journey Optimizer
product: journey optimizer
title: Aggiungere personalizzazione
description: Scopri come utilizzare l’editor di personalizzazione per aggiungere la personalizzazione.
feature: Personalization
topic: Personalization
role: Developer
level: Intermediate
mini-toc-levels: 1
keywords: espressione, editor, about, start
exl-id: 1ac2a376-a3a8-41ae-9b04-37886697f0fc
feature_v2: id: fda7be7c-b81e-42c0-95a9-616e5b893c03
subfeature_v2: id: e51e8901-97d9-4f7d-a835-503025a90e32id: ac5d9310-7772-40fb-9d78-864562e1bfd6
source-git-commit: f552e98f370f96e9a99d2f1d604f840ac6069d65
workflow-type: tm+mt
source-wordcount: 2328
ht-degree: 7%

---

# Aggiungere personalizzazione {#build-personalization-expressions}

>[!BEGINSHADEBOX]

**In questa pagina:** scopri come utilizzare l&#39;editor di personalizzazione per aggiungere, personalizzare e convalidare espressioni di personalizzazione da origini quali attributi di profilo, tipi di pubblico, decisioni sulle offerte e attributi contestuali.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_perso_editor"
>title="Informazioni sull’editor di personalizzazione"
>abstract="L’editor di personalizzazione consente di selezionare, disporre, personalizzare e convalidare tutti i dati per creare una personalizzazione dei contenuti."

L&#39;editor di personalizzazione è il fulcro della personalizzazione in [!DNL Journey Optimizer]. È disponibile in ogni contesto in cui è necessario definire la personalizzazione, ad esempio e-mail, push e offerte.

Nell’interfaccia dell’editor di personalizzazione puoi selezionare, disporre, personalizzare e convalidare tutti i dati per creare una personalizzazione personalizzata per il contenuto.

![](assets/perso_ee1.png)

## Dove posso aggiungere la personalizzazione {#where}

Puoi aggiungere la personalizzazione in **[!DNL Journey Optimizer]** in ogni campo con l&#39;icona ![aggiungi icona personalizzazione](assets/do-not-localize/add-perso-icon.svg). Per ulteriori informazioni, espandi le sezioni seguenti.

+++Messaggi

Nei messaggi, la personalizzazione può essere aggiunta in posizioni diverse nei messaggi, ad esempio il campo **[!UICONTROL Oggetto]**.

![](assets/perso_subject.png)

Può essere aggiunto anche in altre sezioni del contenuto. Ad esempio, per [notifiche push](../push/push-gs.md), è possibile aggiungere la personalizzazione nei campi **Titolo**, **Corpo**, **Audio personalizzato**, **Badge** e **Dati personalizzati**.

+++

+++E-mail designer

Durante la modifica del contenuto delle e-mail in [E-mail Designer](../email/get-started-email-design.md), puoi aggiungere la personalizzazione nella maggior parte degli elementi di testo utilizzando l&#39;icona nella barra degli strumenti contestuale.

![](assets/perso_insert.png)

+++

+++URL

Journey Optimizer consente inoltre di personalizzare **URL** nei messaggi. Gli URL personalizzati indirizzano i destinatari verso pagine specifiche di un sito web o verso un microsito personalizzato, a seconda degli attributi del profilo. [Ulteriori informazioni](../email/url-personalization.md)

![](assets/perso-url.png){width="50%"}

>[!NOTE]
>
>La personalizzazione URL è disponibile per i seguenti tipi di collegamenti: **Collegamento esterno**, **Collegamento per l&#39;annullamento dell&#39;abbonamento** e **Rinuncia**.

+++

+++Configurazione e-mail

Durante la creazione di una configurazione del canale e-mail, puoi definire valori personalizzati per sottodomini, intestazioni e parametri di tracciamento URL. [Ulteriori informazioni](../email/surface-personalization.md)

+++

+++Offerte

Puoi aggiungere la personalizzazione quando utilizzi contenuto di tipo testo nelle rappresentazioni delle **offerte**. [Scopri come creare le offerte personalizzate](../offers/offer-library/creating-personalized-offers.md)

+++

## Origini Personalization {#sources}

Il riquadro di navigazione consente di selezionare l’origine per la personalizzazione. Le origini disponibili sono:

* **[!UICONTROL Attributi profilo]** : elenca tutti i riferimenti associati allo schema profilo descritto nella [documentazione di Adobe Experience Platform Data Model (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=it){target="_blank"}.
* **[!UICONTROL Attributi di destinazione]**: questa cartella è specifica per le campagne orchestrate. Contiene attributi calcolati direttamente nell’area di lavoro della campagna. [Scopri come aggiungere la personalizzazione nelle campagne orchestrate](../orchestrated/add-personalization.md)
* **[!UICONTROL Tipi di pubblico]**: elenca tutti i tipi di pubblico creati nel servizio di segmentazione di Adobe Experience Platform. Ulteriori informazioni sono disponibili nella [documentazione sulla segmentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=it){target="_blank"}.
* **[!UICONTROL Decisioni di offerta]** : elenca tutte le offerte associate a un posizionamento specifico. Seleziona il posizionamento e inserisci le offerte nel contenuto. Per una documentazione completa su come gestire le offerte, consulta [questa sezione](../offers/get-started/starting-offer-decisioning.md).
* **[!UICONTROL Attributi contestuali]**: quando un&#39;attività di azione canale (e-mail, push, SMS) viene utilizzata in un percorso o in una campagna, gli attributi contestuali relativi a eventi e proprietà sono disponibili per la personalizzazione. Un esempio di personalizzazione che sfrutta gli attributi contestuali è presentato in [questa sezione](personalization-use-case.md). Inoltre, le risposte alle azioni personalizzate possono essere utilizzate per la personalizzazione. [Scopri come utilizzare le risposte alle azioni personalizzate nei canali nativi](../action/action-response.md#response-in-channels).

>[!NOTE]
>
>Se esegui il targeting di un pubblico con attributi di arricchimento generati utilizzando un flusso di lavoro di composizione, puoi sfruttare questi attributi di arricchimento per personalizzare il messaggio. [Scopri come utilizzare gli attributi di arricchimento del pubblico](../audience/about-audiences.md#enrichment)

## Aggiungere personalizzazione {#add}

>[!CONTEXTUALHELP]
>id="ajo_perso_editor_autocomplete"
>title="Completamento automatico"
>abstract="L’attivazione di questa opzione consente al sistema di suggerire e completare automaticamente il codice durante la digitazione. Questa funzione è disponibile solo per i formati HTML e Testo e supporta gli attributi di Profilo e Contesto. Se viene disabilitata tramite l’apposito pulsante di attivazione, il completamento automatico del codice HTML nativo verrà eseguito dall’editor."

Nell’area di lavoro centrale puoi creare la sintassi di personalizzazione. Per utilizzare un attributo per personalizzare il messaggio, individuarlo nel riquadro di spostamento a sinistra e fare clic sul pulsante `+` per aggiungerlo all&#39;espressione.

![](assets/personalization-add-attribute.png)

Il menu con i puntini di sospensione accanto all&#39;icona `+` consente di ottenere ulteriori dettagli per ciascun attributo e di aggiungere gli attributi utilizzati più di frequente ai preferiti. Gli attributi aggiunti ai preferiti sono accessibili dal menu **[!UICONTROL Preferiti]** nel riquadro di spostamento.

>[!NOTE]
>
>Per impostazione predefinita, nel riquadro degli attributi vengono visualizzati solo gli attributi compilati. Per visualizzare tutti gli attributi, selezionare il pulsante ![](assets/do-not-localize/settings-icon.svg) situato sopra il campo di ricerca e disattivare l&#39;opzione **[!UICONTROL Mostra solo attributi popolati]**.

Inoltre, puoi definire il testo di fallback predefinito che verrà visualizzato se un attributo di profilo di tipo stringa è vuoto. A tale scopo, fare clic sul pulsante con i puntini di sospensione accanto all&#39;attributo e selezionare **[!UICONTROL Inserisci con testo di fallback]**. Scrivere il testo da visualizzare per impostazione predefinita se il valore dell&#39;attributo è vuoto per un profilo, quindi fare clic su **[!UICONTROL Aggiungi]**.

![](assets/attribute-details.png)

Nell’esempio seguente, l’editor di personalizzazione ti consente di selezionare i profili che hanno il compleanno oggi e quindi di completare la personalizzazione inserendo un’offerta specifica corrispondente a quel giorno.

![](assets/perso_ee2.png)

## Opzioni per la modifica delle espressioni {#options}

L’area di lavoro centrale fornisce vari strumenti per aiutarti a scrivere la tua espressione di personalizzazione.

![](assets/perso-workspace.png)

Le opzioni disponibili sono:

1. **[!UICONTROL Trova]** / **[!UICONTROL Trova e sostituisci]**: cerca nell&#39;espressione e sostituisci automaticamente parti di codice.
1. **[!UICONTROL Annulla]** / **[!UICONTROL Ripristina]**: annulla/ripristina l&#39;ultima operazione.
1. **[!UICONTROL Completamento automatico]**: suggerisce e completa automaticamente il codice durante la digitazione. Questa funzione è disponibile solo per i formati HTML e Testo e supporta gli attributi di Profilo e Contesto. Se viene disabilitata tramite l’apposito pulsante di attivazione, il completamento automatico del codice HTML nativo verrà eseguito dall’editor.

   ![](assets/perso-complete.png){width="70%" align="center" zoomable="yes"}

1. **[!UICONTROL HTML]** / **[!UICONTROL JSON]** / **[!UICONTROL Testo]**: identifica il formato del codice. Questo consente al sistema di adattare la convalida e la funzione di completamento automatico in base alla lingua selezionata.
1. **[!UICONTROL Convalida]**: verifica la sintassi dell&#39;espressione. Ulteriori informazioni in [questa sezione](../personalization/personalization-build-expressions.md).
1. **[!UICONTROL Salva come frammento]**: salva l&#39;espressione come frammento di espressione. [Ulteriori informazioni](../content-management/save-fragments.md#save-as-expression-fragment)
1. **[!UICONTROL Dimensione font]**: regola la dimensione font per i contenuti all&#39;interno dell&#39;editor per migliorarne la leggibilità.
1. **[!UICONTROL Parola a capo]**: attiva o disattiva il ritorno a capo automatico, consentendo la visualizzazione di espressioni lunghe su una singola riga o racchiuse nell&#39;editor. Le opzioni includono:
   * **Disattivato** (impostazione predefinita) - Nessun ritorno a capo automatico. Le linee lunghe si estendono oltre la vista dell’editor e richiedono uno scorrimento orizzontale.
   * **Il** - Dispone le righe alla larghezza dell&#39;editor.
   * **Colonna a capo automatico** - Dispone le righe quando i caratteri di una riga raggiungono gli 80 caratteri.
   * **Limitato** - Dispone le righe alla larghezza dell&#39;editor o a 80 caratteri, a seconda di quale dei due valori è più basso.
1. **[!UICONTROL Pillole]**: visualizza gli attributi come &quot;pillole&quot; compatte per migliorare la leggibilità nascondendo i percorsi degli attributi lunghi. Fare clic su un attributo per visualizzarne il percorso completo.

   >[!NOTE]
   >
   >Questa opzione è disponibile solo per gli attributi di profilo, gli attributi contestuali e gli elementi multimediali dinamici.

Nel riquadro di navigazione sono disponibili funzioni aggiuntive per aiutarti a creare la tua espressione di personalizzazione.

![](assets/perso-features.png)

* **[!UICONTROL Funzioni helper]** - Le funzioni helper consentono di eseguire operazioni sui dati, ad esempio calcoli, formattazione o conversioni di dati, condizioni e di manipolarli nel contesto della personalizzazione. [Ulteriori informazioni sulle funzioni helper disponibili](functions/functions.md)

* **[!UICONTROL Preferiti]** - Gli attributi aggiunti ai preferiti vengono visualizzati in questo elenco. Questo consente di accedere rapidamente agli elementi utilizzati con maggiore frequenza. Per aggiungere un attributo ai preferiti, fai clic sul menu con i puntini di sospensione e scegli **[!UICONTROL Aggiungi ai preferiti]**.

* **[!UICONTROL Condizioni]** - Sfrutta le regole condizionali create nella libreria per aggiungere contenuto dinamico ai messaggi. Questo consente di creare più varianti del messaggio in base alle condizioni. [Scopri come creare contenuti dinamici](../personalization/get-started-dynamic-content.md)

* **[!UICONTROL Frammenti]** - Sfrutta i frammenti di espressione creati o salvati nella sandbox corrente. Un frammento è un componente riutilizzabile a cui è possibile fare riferimento in [!DNL Journey Optimizer] campagne e percorsi. Questa funzionalità consente di precreare più blocchi di contenuto personalizzati che possono essere utilizzati dagli utenti di marketing per assemblare rapidamente i contenuti in un processo di progettazione migliorato. [Scopri come utilizzare i frammenti di espressione per la personalizzazione](../personalization/use-expression-fragments.md)

>[!TIP]
>
>Cerchi espressioni pronte all’uso? La pagina **[ricette Personalization](personalization-recipes.md)** fornisce modelli di copia e incolla per i casi d&#39;uso più comuni: formattazione della data, timer di conto alla rovescia, fallback condizionali, visualizzazione solo temporale e altro ancora.

Una volta che l’espressione di personalizzazione è pronta, devi farla convalidare dall’editor di personalizzazione. Ulteriori informazioni in [questa sezione](../personalization/personalization-build-expressions.md).

## Meccanismi di convalida {#validation-mechanisms}

La convalida dell&#39;espressione viene eseguita automaticamente quando si fa clic sul pulsante **Aggiungi** per chiudere la finestra dell&#39;editor. Puoi anche usare il pulsante **Convalida** per controllare la sintassi di personalizzazione.

![](assets/perso_validation1.png)

Espandi la sezione seguente per visualizzare gli errori più comuni che possono verificarsi durante la convalida della personalizzazione.

+++Errori comuni

* **Percorso &quot;XYZ&quot; non trovato**

Quando tenti di fare riferimento a un campo non definito nello schema.

In questo caso **firstName1** non è definito come attributo nello schema del profilo:

```
{{profile.person.name.firstName1}}
```

* **Tipo non corrispondente per la variabile &quot;XYZ&quot;. Previsto array. Trovata stringa.**

Quando si tenta di eseguire l’iterazione su una stringa anziché su un array.

In questo caso **product** non è un array:

```
{{each profile.person.name.firstName as |product|}}
 {{product.productName}}
{{/each}}
```

* **Sintassi Handlebars non valida. Trovato`'[XYZ}}'`**

Se viene utilizzata una sintassi Handlebars non valida.

Le espressioni Handlebars sono circondate da **{{expression}}**

```
   {{[profile.person.name.firstName}}
```

* **Definizione segmento non valida**

```
No segment definition found for 988afe9f0-d4ae-42c8-a0be-8d90e66e151
```

+++

Per le offerte, possono verificarsi errori specifici. Per ulteriori informazioni, espandi la sezione seguente:

+++ Errori specifici relativi alle offerte

Gli errori relativi all’integrazione delle offerte in un messaggio e-mail o push hanno il seguente pattern:

```
Offer.<offerType>.[PlacementID].[ActivityID].<offer-attribute>
```

La convalida viene eseguita durante la convalida del contenuto di personalizzazione nell’editor di personalizzazione.

<table> 
 <thead> 
  <tr> 
   <th> Titolo errore<br /> </th> 
   <th> Convalida/risoluzione <br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>Risorsa con ID placementID e tipo OfferPlacement non trovata <br/>
Risorsa con ID activityID e tipo OfferActivity non trovata<br/></td> 
   <td>Controlla se ActivityID e/o PlacementID sono disponibili</td> 
  </tr> 
   <tr> 
   <td>Impossibile convalidare la risorsa.</td> 
   <td>Il componentType nel posizionamento deve corrispondere all’offerta offerType</td> 
  </tr> 
   <tr> 
   <td>L’URL pubblico non è presente in offerId.</td> 
   <td>Le offerte di immagini (tutte le offerte personalizzate e di fallback associate alla coppia decisione-posizionamento) devono avere un URL pubblico popolato (deliveryURL non deve essere vuoto).</td> 
  </tr> 
  <tr> 
   <td>La decisione contiene attributi non di profilo.</td> 
   <td>Offerte L’utilizzo del modello deve contenere solo gli attributi del profilo.</td> 
  </tr> 
  <tr> 
   <td>Si è verificato un errore durante il recupero dell’utilizzo della decisione.</td> 
   <td>Questo errore può verificarsi quando l’API tenta di recuperare il modello di offerta.</td> 
  </tr>
  <tr> 
   <td>Attributo offerta attributo offerta non valido.</td> 
   <td>Verifica se l’attributo dell’offerta a cui si fa riferimento nel pacchetto di offerta è valido. Di seguito sono riportati gli attributi validi: <br/>
Immagine: deliveryURL, linkURL<br/>
Testo: contenuto<br/>
HTML: content<br/></td> 
  </tr> 
 </tbody> 
</table>

+++

## Riferimento rapido {#quick-reference}

Questa sezione contiene informazioni strutturate che supportano l&#39;interpretazione, il recupero e la risposta alle domande relative a questo argomento.

Per una comprensione completa, queste informazioni devono essere unite alla documentazione su questa pagina. Nessuna delle due origini è progettata per essere indipendente; la pagina descrive la funzione, mentre questa sezione fornisce un contesto aggiuntivo che aiuta a non ambiguare la terminologia, le finalità, l’applicabilità e i vincoli.

>[!BEGINTABS]

>[!TAB Panoramica]

**TL;DR**

Questa pagina spiega come utilizzare l’editor di personalizzazione di Journey Optimizer per selezionare, generare, personalizzare e convalidare le espressioni di personalizzazione da origini quali attributi di profilo, tipi di pubblico, decisioni sulle offerte e attributi contestuali.

**Intenti**

* Scopri dove è possibile aggiungere la personalizzazione in Journey Optimizer (messaggi, e-mail Designer, URL, configurazione e-mail, offerte)
* Seleziona l’origine di personalizzazione appropriata per un’espressione
* Aggiungere attributi ed espressioni di build nell’area di lavoro dell’editor
* Utilizza gli strumenti dell’editor: Trova/Sostituisci, Completamento automatico, Convalida, Pillole, Salva come frammento
* Utilizza le funzioni del riquadro di navigazione: Funzioni helper, Preferiti, Condizioni, Frammenti
* Convalidare espressioni e risolvere errori comuni

>[!TAB Glossario]

* **Editor Personalization**: lo strumento dell&#39;interfaccia utente centrale di Journey Optimizer per la creazione, la personalizzazione e la convalida delle espressioni di personalizzazione, disponibile ovunque sia possibile definire la personalizzazione. *(specifico per prodotto)*
* **Origini Personalization**: le categorie di dati disponibili per la creazione di espressioni: attributi di profilo, attributi di destinazione, tipi di pubblico, decisioni di offerta e attributi contestuali.
* **Attributi contestuali**: dati specifici del Percorso o della campagna (eventi, proprietà, risposte ad azioni personalizzate) disponibili per la personalizzazione solo quando un&#39;azione del canale viene utilizzata in un percorso o in una campagna. *(specifico per prodotto)*
* **Pillole**: modalità di visualizzazione dell&#39;editor di personalizzazione che rende i percorsi di attributi lunghi come token compatti e cliccabili per migliorarne la leggibilità. Disponibile solo per attributi di profilo, attributi contestuali e elementi multimediali dinamici. *(specifico per prodotto)*
* **Completamento automatico**: funzionalità dell&#39;editor che suggerisce e completa automaticamente il codice durante la digitazione. Disponibile solo per i formati HTML e Text, supporta solo gli attributi Profile e Context. *(specifico per prodotto)*
* **Frammento di espressione**: componente di espressione di personalizzazione riutilizzabile a cui è possibile fare riferimento in più campagne e percorsi. *(specifico per prodotto)*
* **Testo di fallback**: stringa predefinita visualizzata quando un attributo di profilo di tipo stringa è vuoto per un determinato profilo; configurato per attributo tramite &quot;Inserisci con testo di fallback&quot;.

>[!TAB Terminologia]

* **Nome canonico:** editor di personalizzazione
* **Non confondere:** l&#39;editor di Personalization (utilizzato per creare espressioni di contenuto nei messaggi, nelle e-mail, nelle notifiche push e nelle offerte; supporta sia Handlebars che la sintassi PQL) ≠ l&#39;editor di espressioni avanzate (utilizzato nel percorso per condizioni sulle origini dati e informazioni sugli eventi, attività di attesa personalizzate e mappatura dei parametri delle azioni) fornisce funzioni e operatori incorporati che differiscono da quelli dell&#39;editor di personalizzazione
* **Non confondere:** Attributi di profilo (basati su schema XDM, disponibili in tutti i contesti) ≠ Attributi contestuali (specifici del percorso/della campagna, disponibili solo in tale contesto) ≠ Attributi di destinazione (solo per campagne orchestrate)
* **Non confondere:** Completamento automatico per HTML/Text (suggerisce il completamento degli attributi di personalizzazione) ≠ completamento automatico del codice nativo di HTML (impostazione predefinita dell&#39;editor quando l&#39;opzione è disabilitata)

>[!TAB Guardrail e limitazioni]

* Il completamento automatico è disponibile solo per i formati HTML e Text; supporta solo gli attributi Profile e Context.
* La modalità di visualizzazione delle pillole è disponibile solo per gli attributi di profilo, gli attributi contestuali e gli elementi multimediali dinamici.
* La personalizzazione URL è disponibile solo per i tipi di collegamento External, Unsubscription link e Opt-out.
* Per impostazione predefinita, il riquadro degli attributi mostra solo gli attributi popolati; disattiva &quot;Mostra solo attributi popolati&quot; per visualizzare tutti gli attributi dello schema.
* L’utilizzo del modello di offerte deve contenere solo attributi di profilo; gli attributi non di profilo in una decisione causano un errore di convalida.

>[!TAB Domande frequenti]

**Q: dove è possibile aggiungere la personalizzazione in Journey Optimizer?**

In qualsiasi campo con l’icona Aggiungi personalizzazione, inclusa la riga dell’oggetto e-mail, i campi di notifica push (Titolo, Corpo, Audio personalizzato, Badge, Dati personalizzati), gli elementi di testo E-mail Designer, gli URL (Collegamento esterno, Collegamento di annullamento dell’abbonamento, Rinuncia), i sottodomini/intestazioni/parametri di tracciamento URL della configurazione e-mail e le rappresentazioni di tipo testo dell’offerta.

**D: Quali sono le origini di personalizzazione disponibili?**

Attributi del profilo, attributi di Target (solo campagne orchestrate), tipi di pubblico, decisioni di offerta e attributi contestuali (eventi di percorso/campagna e risposte alle azioni personalizzate).

**Q: Come viene convalidata un&#39;espressione?**

La convalida viene eseguita automaticamente quando si fa clic su Aggiungi per chiudere l&#39;editor. Puoi anche attivarla manualmente con il pulsante Convalida. Gli errori più comuni includono: percorso non trovato (campo non incluso nello schema), tipo non corrispondente (iterazione di una stringa come array), sintassi Handlebars non valida e definizione di segmento non valida.

**D: cosa fa l&#39;opzione Pillole?**

I lunghi percorsi di attributi vengono riprodotti come token compatti e cliccabili per una migliore leggibilità nell’editor. Disponibile solo per attributi di profilo, attributi contestuali e elementi multimediali dinamici.

**D: perché nel riquadro degli attributi sono presenti solo alcuni attributi?**

Per impostazione predefinita, il riquadro mostra solo gli attributi compilati. Seleziona l’icona delle impostazioni sopra il campo di ricerca e disattiva &quot;Mostra solo attributi popolati&quot; per visualizzare tutti gli attributi dello schema.

>[!ENDTABS]

<!-- ai-section-version: 1 | source-hash: 54973b31 -->
