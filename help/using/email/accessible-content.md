---
solution: Journey Optimizer
product: journey optimizer
title: Progettare contenuti accessibili
description: Scopri come progettare contenuti accessibili per le e-mail e le pagine di destinazione in Journey Optimizer
feature: Email Design
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: e-mail, progettazione, accessibilità
hide: true
hidefromtoc: true
source-git-commit: be87e47f7c3303575c2784af7ce76c138cb03154
workflow-type: tm+mt
source-wordcount: '1612'
ht-degree: 0%

---

# Progettare contenuti accessibili {#accessible-content}

L&#39;[atto europeo sull&#39;accessibilità](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX%3A32019L0882){target="_blank"} è una direttiva intesa a migliorare il mercato interno dei prodotti e dei servizi accessibili eliminando gli ostacoli causati da norme nazionali divergenti tra gli Stati membri.

Durante la creazione di contenuto per le **e-mail** e le **pagine di destinazione** in [!DNL Journey Optimizer], le best practice per l&#39;accessibilità per gli esperti di marketing e-mail elencati in questa pagina possono aiutarti a rispettare questa direttiva. Si basano sulle linee guida per l’accessibilità dei contenuti web (WCAG) 2.1, livello AA.

>[!NOTE]
>
>Le caratteristiche di accessibilità quando si utilizza l&#39;interfaccia [!DNL Journey Optimizer] sono descritte in dettaglio in [questa sezione](../start/accessibility.md).

L’atto europeo sull’accessibilità stabilisce che tutte le comunicazioni digitali, compresi e-mail, newsletter, PDF e contenuti scaricabili, devono essere accessibili. È quindi necessario seguire linee guida specifiche, ad esempio l’utilizzo di font accessibili e formati leggibili, e fornire testo alternativo per le immagini.

Il [!DNL Journey Optimizer] [Messaggio e-mail Designer](content-from-scratch.md), che consente agli addetti al marketing di creare contenuti sia per le e-mail che per le pagine di destinazione, ti consente di seguire facilmente queste linee guida. Di seguito sono elencate le procedure consigliate per la progettazione di contenuto accessibile con [!DNL Journey Optimizer].

<!--You can adjust a number of styling parameters and attributes from the Email Designer **[!UICONTROL Styles]** pane.-->
 
## Assicurare la leggibilità del testo {#text-readability}

Utilizza la scheda **[!UICONTROL Stili]** del componente **[!UICONTROL Testo]** per garantire che il testo sia leggibile, ad esempio utilizzando un contrasto di colore appropriato e font semplici. [Ulteriori informazioni](content-components.md#text)

![](assets/accessible-text-styles.png){width="80%"}

Per i font e il testo, attenetevi alle seguenti linee guida:

**Selezione carattere**

* Utilizza font sans-serif come Arial, Verdana, Tahoma, Helvetica o Open Sans.
* Evita font serif, corsivi o decorativi nel contenuto del corpo.
* Attenersi a un set di caratteri limitato per coerenza e fallback (ad esempio: `font-family: Arial, Helvetica, sans-serif;`).

**Dimensione font**

* Assicurati che la dimensione minima del font per il corpo del testo sia 16 px.
* Utilizza la gerarchia corretta per le intestazioni.

**Contrasto colore**

* Mantenere un rapporto di contrasto di almeno 4,5:1 tra testo e sfondo.
* Per il testo di grandi dimensioni (≥24 px o 18 px in grassetto), assicurati di ottenere un contrasto di almeno 3:1.
* Evitare il testo grigio chiaro o pastello su sfondi bianchi.
* Non fare affidamento solo sul colore per trasmettere il significato, ma utilizzare invece sottolineature, icone, ecc.

**Accessibilità testo**

* Evitare il testo nelle immagini.
* Non utilizzare tutte le maiuscole nel corpo del testo.
* Assicurati che il testo possa essere ingrandito fino al 200% senza interrompere il layout.

## Garantire l’accessibilità visiva {#visual-accessibility}

Per assicurarti che il contenuto sia accessibile visivamente, segui le best practice riportate di seguito:

* Evitare di utilizzare indicatori di solo colore per informazioni importanti.
* Utilizza etichette di testo o icone per assicurarne la chiarezza.
* Ottimizza la progettazione per layout mobili e reattivi, garantendo pulsanti grandi e spaziati correttamente.
* Esegui regolarmente test tra dispositivi e dimensioni dello schermo per mantenere l’accessibilità.

In [!DNL Journey Optimizer], le dimensioni e la spaziatura dei diversi elementi del contenuto possono essere ulteriormente migliorate utilizzando i parametri e gli attributi di stile del riquadro **[!UICONTROL Stili]** di E-mail Designer. [Ulteriori informazioni](get-started-email-style.md)

È ad esempio possibile aggiornare lo [sfondo](backgrounds.md) o modificare i margini, la spaziatura interna e l&#39;allineamento per migliorare l&#39;accessibilità visiva del contenuto. [Ulteriori informazioni](alignment-and-padding.md)

![](assets/accessible-styles.png){width="80%"}

Inoltre, il Designer e-mail di [!DNL Journey Optimizer] consente di visualizzare in anteprima e ottimizzare la progettazione per diversi dispositivi e dimensioni dello schermo. In qualsiasi momento puoi **[!UICONTROL Passare alla visualizzazione live]** per verificare come il contenuto potrebbe essere riprodotto su dispositivi di varie dimensioni.

![](assets/accessible-live-view.png){width="70%"}

>[!CAUTION]
>
>La visualizzazione live è un’anteprima generica progettata per confrontare l’aspetto del rendering tra le varie dimensioni dei dispositivi. Il rendering finale può variare a seconda del client e-mail del destinatario.

## Usa testo alternativo per le immagini {#alt-text}

Utilizza il componente **[!UICONTROL Immagine]** per fornire testo alternativo per le immagini. [Ulteriori informazioni](content-components.md#image)

![](assets/accessible-alt-text.png){width="90%"}

Per un testo alternativo efficace nei prodotti digitali, attieniti alle linee guida seguenti:

* Descrivi lo scopo dell’immagine in modo conciso e contestuale.
* Evita frasi ridondanti come &quot;Immagine di ...&quot; e utilizza testo alternativo vuoto per le immagini decorative.
* Per le icone con significato, fornisci etichette significative e per le immagini complesse, utilizza un breve testo alternativo più una descrizione più lunga altrove.

## Usa formato leggibile {#readable-format}

Utilizza la struttura rilevante di E-mail Designer e i [componenti di contenuto](content-components.md), nonché le opzioni nel riquadro **[!UICONTROL Stili]**, per organizzare il contenuto in modo chiaro, logico e conciso, accessibile a tutti.

![](assets/accessible-components.png){width="1000%"}

* Utilizza HTML semantico e strutturato con intestazioni, paragrafi, elenchi e tabelle corretti.
* Assicurati che il contenuto segua un flusso logico da sinistra a destra e dall’alto al basso.
* Utilizza un linguaggio chiaro e conciso.
* Fornire formati alternativi per PDF e infografiche.
* Consenti il ridimensionamento e il riversamento del testo e assicurati che la composizione tipografica sia leggibile con un contrasto del colore adeguato in tutti i formati.

## Garantire la leggibilità dei contenuti {#readability}

Per essere leggibile, il contenuto deve essere chiaro, ben strutturato e utilizzabile da tutti, comprese le persone con difficoltà visive, cognitive o di lettura e quelle che utilizzano tecnologie per l’accessibilità. Alcuni punti da considerare durante la creazione di contenuto accessibile includono:

* Mantenere le frasi a un massimo di 20 parole.
* Modifica la copia in modo che sia diretta e diretta.
* Utilizza la voce attiva per semplificare la struttura della frase.
* Evita di usare parole gergali, gergali o regionali che alcuni potrebbero non conoscere.

Per valutare la leggibilità delle e-mail, puoi utilizzare il popolare [test di facilità di lettura Flesch](https://support.microsoft.com/en-us/office/get-your-document-s-readability-and-level-statistics-85b4969e-e80a-4777-8dd3-f7fc3c8b3fd2){target="_blank"}, disponibile in Microsoft Word, che calcola la facilità di lettura dei contenuti su una scala da 0 a 100.

## Verifica il contenuto {#test}

Per verificare l&#39;accessibilità del contenuto, è possibile utilizzare le funzionalità di test fornite da [!DNL Journey Optimizer]. Non sono progettate specificamente per verificare se il contenuto è completamente accessibile, ma possono fornire un primo livello di verifica.

* Visualizza l’anteprima del contenuto utilizzando i profili di test. [Scopri come](../content-management/preview.md)

* Utilizza l&#39;opzione [Rendering di e-mail](../content-management/rendering.md) che sfrutta Litmus per simulare le progettazioni tra i principali client e-mail (Apple Mail, Gmail, Outlook) e vedere se testo, colori e immagini rendono accessibili i contenuti. <!--Litmus includes accessibility testing-->

* Invia bozze per testare il rendering del contenuto prima di inviarlo al pubblico reale. [Scopri come](../content-management/proofs.md)

![](assets/accessible-simulate.png){width="90%"}

Per eseguire il check-in in modo più coerente se il contenuto è accessibile in modo affidabile, cerca strumenti esterni specifici come:

* Lo strumento di verifica del contrasto [WebAim](https://webaim.org/resources/contrastchecker/){target="_blank"} e lo strumento di valutazione dell&#39;accessibilità Web [WAVE](https://wave.webaim.org/){target="_blank"} per valutare il contrasto e la conformità.

* Tecnologie per l&#39;accessibilità, come gli assistenti vocali (ad esempio: [NVDA](https://www.nvaccess.org/download/){target="_blank"} o [VoiceOver](https://support.apple.com/en-ie/guide/iphone/iph3e2e415f/ios){target="_blank"} su iPhone), per visualizzare le e-mail dal punto di vista degli utenti ipovedenti.

## Usa modalità scura {#dark-mode}

<!--TO PUBLISH WHEN DARK MODE IS RELEASED-->

La modalità scura migliora l&#39;accessibilità visiva per gli utenti con sensibilità alla luce o disturbi visivi, offrendo un&#39;esperienza di visualizzazione migliore.

![](assets/accessible-dark-mode.png){width="90%"}

Tra le best practice per la progettazione di contenuti in modalità scura, puoi utilizzare PNG o SVG trasparenti, impostare metatag e CSS appropriati e fornire uno stile di fallback accessibile se la modalità scura non è supportata. Infine, assicurati che le e-mail vengano riprodotte correttamente in modalità scura, testando tutti i contenuti e gli elementi dell’interfaccia utente sia in modalità chiara che in modalità scura.

Le best practice dettagliate specifiche della modalità scura, incluse le linee guida per garantire l&#39;accessibilità, sono elencate in [questa sezione](dark-mode.md#best-practices). <!--KEEP dark mode accessibility best practices IN ONE SINGLE LOCATION - for now listed on the Dark mode page.-->

## Usa attributi specifici per e-mail accessibili {#attributes}

### Attributi `lang` e `dir`

Durante la creazione di e-mail accessibili, includi gli attributi `lang` (lingua) e `dir` (direzione del testo) nel corpo dell&#39;e-mail. Questi attributi consentono alle tecnologie per l’accessibilità, come gli assistenti vocali, di interpretare e presentare il contenuto in modo appropriato.

* L&#39;attributo `lang` indica la lingua dell&#39;e-mail per le tecnologie per l&#39;accessibilità, garantendo che le parole vengano pronunciate correttamente.

  +++Esempi

  Esempio di inglese:

  ```
  <body lang="en">
  ```

  Esempio di francese:

  ```
  <body lang="fr">
  ```

  +++

* L&#39;attributo `dir` specifica la direzione del testo. La maggior parte delle lingue, tra cui l&#39;inglese e il francese, sono lette da sinistra a destra (ltr), mentre le lingue come l&#39;arabo e l&#39;ebraico sono lette da destra a sinistra (rtl).

  +++Esempi

  Esempio di inglese (da sinistra a destra):

  ```
  <body lang="en" dir="ltr">
  ```

  Esempio di arabo (da destra a sinistra):

  ```
  <body lang="ar" dir="rtl">
  ```

  +++

Gli assistenti vocali si basano sull&#39;attributo `lang` per applicare le regole di pronuncia corrette, mentre la direzione del testo garantisce un flusso di contenuto naturale per le lingue da sinistra a destra o da destra a sinistra. Senza questi attributi, gli utenti potrebbero riscontrare un ordine di lettura confuso o una pronuncia errata. Di conseguenza, racchiudi sempre il corpo dell&#39;e-mail con gli attributi `lang` e `dir` appropriati.

>[!TIP]
>
>Se l&#39;e-mail contiene più lingue, assegnare gli attributi della lingua appropriati a sezioni specifiche (ad esempio `<table>` o `<td>` blocchi) per garantire la corretta lettura di ogni parte.

### Tabelle layout e `role="presentation"`

Nelle e-mail di HTML, le tabelle vengono spesso utilizzate per il layout. Per impostazione predefinita, gli assistenti vocali trattano ogni `<table>` come una tabella dati, annunciando righe, colonne e struttura. Questo può creare confusione se la tabella viene utilizzata solo per la formattazione.

Aggiungi `role="presentation"` (o `role="none"`) alle tabelle layout per garantire che le tecnologie per l&#39;accessibilità saltino la struttura e si concentrino solo sul contenuto effettivo.

+++Esempio - Tabella layout (con role=&quot;presentazione&quot;): 

```
<table role="presentation" border="0" cellpadding="0" cellspacing="0" width="100%"> 

  <tr> 

    <td align="center"> 

      <h1>Hello World</h1> 

      <p>Welcome to our newsletter</p> 

    </td> 

  </tr> 

</table>
```

Gli assistenti vocali leggono:
&quot;Hello World. Benvenuto nella nostra newsletter.&quot; *(Nessuna menzione di righe, colonne o tabelle)*

+++

+++Esempio - Tabella dati (senza role=&quot;presentation&quot;): 

```
<table border="1" cellpadding="5" cellspacing="0"> 

  <tr> 

    <th scope="col">Name</th> 

    <th scope="col">Score</th> 

  </tr> 

  <tr> 

    <td>Alice</td> 

    <td>95</td> 

  </tr> 

  <tr> 

    <td>Bob</td> 

    <td>88</td> 

  </tr> 

</table> 
```

Gli assistenti vocali leggono:
&quot;Tabella con 2 colonne e 3 righe.&quot;

&quot;Nome, Alice.&quot;

&quot;Punteggio, 95&quot;.

&quot;Nome, Bob.&quot;

&quot;Punteggio, 88&quot;.

+++

>[!TIP]
>
>Utilizza `role="presentation"` esclusivamente per le tabelle layout. Per le tabelle dati, mantenere la struttura semantica`<table>` in modo che gli assistenti vocali possano annunciare correttamente le intestazioni e le relazioni.

### Testo riconoscibile e descrittivo per i collegamenti

Gli assistenti vocali leggono i collegamenti utilizzando il testo. Se un collegamento è etichettato solo come &quot;Fai clic qui&quot; o &quot;Ulteriori informazioni&quot;, gli utenti delle tecnologie per l’accessibilità non conosceranno la destinazione.

Per garantire l’accessibilità, scrivi un testo descrittivo che indichi chiaramente la destinazione o l’azione. Utilizza E-mail Designer per [aggiungere un collegamento](message-tracking.md#insert-links) al contenuto e modificare l&#39;etichetta in modo che sia distinguibile (visibile) e descrittiva (non crittografata). Evita etichette vaghe come &quot;qui&quot; o &quot;altro&quot;.

![](assets/accessible-link.png){width="70%"}

+++Esempio - Collegamento valido (descrittivo): 

```
<p>Learn more in the  

<a href="https://adobe.com/release-notes">August release notes</a>. 

</p>
```

Gli assistenti vocali leggono:
&quot;Link, note sulla versione di agosto&quot;.

+++

+++Esempio - Collegamento non valido (non descrittivo): 

```
<p>Learn more about our new features.  

  <a href="https://adobe.com/release-notes">Click here</a>. 

</p>
```

Gli assistenti vocali leggono:
&quot;Link, fai clic qui.&quot; *(Non fornisce contesto fuori ordine di lettura.)*

+++

<!--
>[!TIP]
>
>Always ensure link text is discernible (visible) and descriptive (clear about purpose). Avoid vague labels like 'here' or 'more'.-->

## Supporto per la navigazione da tastiera e la messa a fuoco {#keyboard}

<!--for landing pages-->

Il supporto per la navigazione da tastiera e l&#39;attivazione della tastiera consente agli utenti che non possono utilizzare il mouse di accedere e interagire completamente con il contenuto. Inoltre, migliora l’usabilità complessiva offrendo a tutti gli utenti un modo chiaro e coerente di passare alle informazioni.

* Attivazione della messa a fuoco tramite tastiera (tasti TAB/freccia)

   * Assicurarsi che tutti gli elementi interattivi (ad esempio pulsanti, caselle di controllo e collegamenti) abbiano `tabindex="0"`, in modo che vengano inclusi nell&#39;ordine di tabulazione naturale.

   * Consenti la navigazione utilizzando i tasti TAB e freccia (↑ ↓ ← →), che dovrebbero evidenziare visibilmente l’elemento attivo.

* Stile di messa a fuoco personalizzato

   * Applica stili chiari e distinguibili per concentrarti sugli elementi utilizzabili:

     +++Esempio (CSS):

     ```
     [tabindex="0"] : focus { 
     
     outline: 2px solid #00AEEF;  /* Cyan border */ 
     
     background-color: #20CEFF;   /* Optional background */ 
     
     }
     ```

     +++

   * Assicurati che gli indicatori di focus soddisfino gli standard WCAG 2.2 per l’aspetto del focus, tra cui:

      * Area minima: 2 linee di spessore pixel CSS.

      * Rapporto di contrasto: ≥ 3:1 tra stato attivo e non attivo.

* Supporto per l&#39;attivazione della tastiera

   * Assicurarsi che le caselle di controllo e i pulsanti rispondano ai tasti Invio e Spazio.

   * Convalidare l’interazione utilizzando solo la tastiera:

      * Immettere o Spazio per attivare/disattivare le caselle di controllo.

      * I pulsanti Invio o Spazio devono essere attivati.
