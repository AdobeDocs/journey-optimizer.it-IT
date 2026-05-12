---
solution: Journey Optimizer
product: journey optimizer
title: Tracciare i messaggi
description: Scopri come aggiungere collegamenti e tenere traccia dei messaggi inviati
feature: Email Design, Monitoring
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: collegamenti, tracciamento, monitoraggio, e-mail
exl-id: 689e630a-00ca-4893-8bf5-6d1ec60c52e7
TQID: https://experienceleague.adobe.com/mY-h-cTs9mlZH5XJNS9Yv3pxGVoRn-pBTHAh8TlBi8I
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: c6e980f5-2d4f-494f-beef-186b9ecf1513
  - id: ee5bb250-0884-4d71-86eb-d8489e8bcadd
  - id: f550d0f2-143d-4093-9463-467fbec95fcc
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: beb7a3c1-66ab-4786-b879-7621375b3c40
  - id: cc72dcf1-72e1-48cc-b434-e7c27d62d67c
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 2248fe8ed733afa359477cc3f4d80a3cf7732800
workflow-type: tm+mt
source-wordcount: 1461
ht-degree: 25%

---

# Aggiungere collegamenti e tracciare i messaggi {#tracking}

Utilizza [!DNL Journey Optimizer] per aggiungere collegamenti al contenuto e tenere traccia dei messaggi inviati per monitorare il comportamento dei destinatari.

>[!NOTE]
>
>I collegamenti inclusi nel contenuto scadono **25 mesi** dopo l&#39;invio del messaggio, ad eccezione dei collegamenti a una pagina mirror che scadono dopo **90 giorni**. Trascorso tale ritardo, i collegamenti non saranno più disponibili.

## Abilita tracciamento {#enable-tracking}

Puoi abilitare il tracciamento a livello di messaggio e-mail controllando **[!UICONTROL Aperture e-mail]** e/o **[!UICONTROL Fai clic sulle opzioni e-mail]** durante la creazione del messaggio all&#39;interno di un percorso o di una campagna, come mostrato nelle schede seguenti:

>[!BEGINTABS]

>[!TAB Attiva il tracciamento in un percorso]

![](assets/message-tracking-journey.png)

>[!TAB Abilitare il tracciamento in una campagna]

![](assets/message-tracking-campaign.png)

>[!ENDTABS]

>[!NOTE]
>
>Entrambe le opzioni sono abilitate per impostazione predefinita.

Quando sono abilitate, queste opzioni tengono traccia del comportamento dei destinatari dei messaggi:

* La metrica **[!UICONTROL Aperture e-mail]** controlla quanti messaggi sono stati aperti.
* La metrica **[!UICONTROL Clic su e-mail]** calcola il numero di clic sui collegamenti in un messaggio e-mail.

### Tracciare più e-mail {#track-across-multiple-emails}

Un identificatore di tracciamento univoco (urlID) viene generato solo quando sia l&#39;**URL** che la **label** sono univoci. I collegamenti che condividono lo stesso URL e hanno la stessa etichetta efficace (anche quando l’etichetta è vuota) riutilizzano lo stesso urlID, il che significa che non è possibile individuare il collegamento su cui è stato fatto clic.

Per tenere traccia dello stesso URL in più e-mail (o più volte in un messaggio e-mail), utilizza un&#39;etichetta univoca per ogni URL simile; in caso contrario, [!DNL Journey Optimizer] non sarà in grado di tenere traccia del collegamento su cui è stato fatto clic. È possibile impostare etichette distinte in E-mail Designer o, per HTML, tramite l&#39;attributo `data-label`.

| URL | Tag | Etichetta | comportamento urlID |
| --- | --- | --- | --- |
| `https://www.example.com` | Primo | (vuoto) | Ottiene un urlID (ad esempio A) |
| `https://www.example.com` | Second | (vuoto) | Riutilizza l’ID URL A — impossibile individuare il collegamento su cui è stato fatto clic |
| `https://www.example.com` | Terzo | Prima etichetta | Ottiene un urlID (ad esempio B) |
| `https://www.example.com` | Quarto | Seconda etichetta | Ottiene un urlID (esempio: C) |

## Inserire i collegamenti {#insert-links}

Quando è abilitato il [tracciamento](#enable-tracking), vengono tracciati tutti i collegamenti inclusi nel contenuto del messaggio.

>[!NOTE]
>
>Vengono tracciati anche i collegamenti dai frammenti utilizzati in un messaggio e-mail. [Ulteriori informazioni sui frammenti](../content-management/fragments.md)

Per inserire collegamenti nel contenuto delle e-mail, segui la procedura seguente:

1. Selezionare un elemento (testo o immagine) e fare clic su **[!UICONTROL Inserisci collegamento]** nella barra degli strumenti contestuale.

   ![](assets/message-tracking-insert-link.png)

1. Scegli il tipo di collegamento da creare:

   * Seleziona **[!UICONTROL Collegamento esterno]** per inserire un collegamento a un URL esterno.

   * Seleziona **[!UICONTROL Pagina di destinazione]** per inserire un collegamento a una pagina di destinazione. [Ulteriori informazioni](../landing-pages/create-lp.md)

   * Seleziona **[!UICONTROL Rinuncia con un clic]** per inserire un collegamento che consenta agli utenti di annullare rapidamente l&#39;iscrizione alle comunicazioni senza dover confermare la rinuncia. [Ulteriori informazioni](email-opt-out.md#one-click-opt-out).

   * Seleziona **[!UICONTROL Consenso/Iscrizione esterno]** per inserire un collegamento per accettare la ricezione di comunicazioni dal tuo marchio.

   * Seleziona **[!UICONTROL Rinuncia/Annullamento iscrizione esterno]** per inserire un collegamento che consenta di annullare l&#39;iscrizione alla ricezione di comunicazioni dal tuo marchio. Ulteriori informazioni sulla gestione delle rinunce in [questa sezione](email-opt-out.md#email-opt-out).

   * Seleziona **[!UICONTROL Pagina mirror]** per aggiungere un collegamento alla pagina mirror della posta elettronica. [Ulteriori informazioni](#mirror-page)

   * Seleziona **[!UICONTROL Collegamento diretto]** per inserire un collegamento a un&#39;app mobile. In questo modo gli utenti vengono indirizzati direttamente al contenuto in-app corretto invece di essere reindirizzati a browser o app store, mantenendo il contesto e il coinvolgimento. [Ulteriori informazioni](deeplinks.md)

     >[!IMPORTANT]
     >
     >Prima di utilizzare il deep link, assicurati di aver completato i [passaggi di configurazione](deeplinks.md#configuration) corrispondenti in Journey Optimizer e di aver implementato la [gestione del deeplink](deeplinks.md#mobile-implementation) nella tua app mobile. Se non lo hai ancora fatto, il collegamento diretto non indirizzerà gli utenti al contenuto in-app desiderato.
     >
     >Inoltre, assicurati che il tracciamento dei collegamenti [&#x200B; sia abilitato](#enable-tracking) per il messaggio in modo che l&#39;URL venga riscritto tramite i sistemi Adobe.

1. Inserisci l’URL desiderato nel campo corrispondente, oppure seleziona una pagina di destinazione e definisci le impostazioni e gli stili del collegamento. [Ulteriori informazioni](#adjust-links)

   >[!NOTE]
   >
   >Per l&#39;interpretazione degli URL, [!DNL Journey Optimizer] è conforme alla sintassi URI ([RFC 3986 standard](https://datatracker.ietf.org/doc/html/rfc3986){target="_blank"}), che disabilita alcuni caratteri internazionali speciali negli URL. Quando tenti di inviare la bozza o l’e-mail, se ti viene restituito un errore relativo a un URL aggiunto al contenuto, puoi codificare l’URL della stringa come soluzione alternativa.

1. Puoi personalizzare i tuoi collegamenti. [Ulteriori informazioni](url-personalization.md)

1. Salva le modifiche.

1. Una volta creato il collegamento, puoi comunque modificarlo dai riquadri **[!UICONTROL Impostazioni]** e **[!UICONTROL Stili]** a destra.

   ![](assets/message-tracking-link-settings.png)

>[!NOTE]
>
>I messaggi e-mail di tipo Marketing devono includere un [collegamento di rinuncia](../privacy/opt-out.md#opt-out-decision-management), che non è necessario per i messaggi transazionali. La categoria del messaggio (**[!UICONTROL Marketing]** o **[!UICONTROL Transazionale]**) è definita nella [configurazione canale](email-settings.md#email-type) durante la creazione del messaggio.

Una volta inviato il messaggio, il periodo di conservazione per un collegamento è di **25 mesi**. Dopo questo ritardo, il collegamento non è più disponibile.

>[!CAUTION]
>
>Quando sia l&#39;**etichetta** che l&#39;**URL** di un pulsante sono resi modificabili in un [frammento personalizzabile](../content-management/customizable-fragments.md), nei report di tracciamento viene visualizzato l&#39;URL anziché l&#39;etichetta del pulsante.

## Collegare a una pagina mirror {#mirror-page}

La pagina mirror è una versione online della tua e-mail. L’aggiunta di un collegamento alla pagina speculare rappresenta una buona pratica di e-mail marketing. Gli utenti possono passare alla pagina mirror di un’e-mail, ad esempio se riscontrano problemi di rendering o immagini interrotte quando tentano di visualizzarla nella casella in entrata. Si consiglia inoltre di fornire una versione online per motivi di accessibilità o di incoraggiare la condivisione social.

La pagina speculare generata da Adobe Journey Optimizer contiene tutti i dati di personalizzazione.

Per aggiungere un collegamento a una pagina mirror nell&#39;e-mail, [inserisci un collegamento](#insert-links) e seleziona **[!UICONTROL Pagina mirror]** come tipo di collegamento.

![](assets/message-tracking-mirror-page.png)

La pagina mirror viene creata automaticamente. Una volta inviata l’e-mail, quando i destinatari fanno clic sul collegamento della pagina mirror, il contenuto dell’e-mail viene visualizzato nel browser web predefinito.

Il periodo di conservazione per una pagina mirror è di **90 giorni**. Trascorso tale periodo, la pagina mirror non è più disponibile.

>[!CAUTION]
>
>* I collegamenti alle pagine mirror vengono generati automaticamente e non possono essere modificati. Contengono tutti i dati personalizzati crittografati necessari per eseguire il rendering dell’e-mail originale. Di conseguenza, l’utilizzo di attributi personalizzati con valori elevati può generare URL di pagine mirror lunghi, che possono impedire il funzionamento del collegamento in browser web che hanno una lunghezza massima per gli URL.
>
>* Durante la creazione di e-mail che si basano fortemente sulla personalizzazione in fase di esecuzione (ad esempio, `#each` loop, oggetti nidificati, dati di payload di grandi dimensioni), gli URL delle pagine mirror possono diventare eccessivamente grandi, in particolare nelle campagne attivate dall’API che utilizzano dati contestuali estesi provenienti da payload. Questo può causare errori HTTP (404, 422, 502) nei browser o nei client di posta. Adobe consiglia di limitare l’ampiezza e la profondità dei campi dinamici, riducendo l’affidamento su frammenti complessi e appiattendo le strutture di personalizzazione per evitare errori di collegamento.
>
>* Nella [bozza](../content-management/proofs.md) inviata ai profili di test, il collegamento alla pagina mirror non è attivo. È attivo solo nei messaggi finali.

## Personalizzare l’aspetto e la destinazione del collegamento {#adjust-links}

È possibile apportare modifiche ai collegamenti, ad esempio sottolinearli, modificarne il colore o selezionare la destinazione.  Queste modifiche sono impostate nei riquadri **[!UICONTROL Impostazioni]** e **[!UICONTROL Stili]** nella sezione destra dell&#39;editor di contenuti.

### Target {#link-target}

L&#39;attributo **target** viene utilizzato per controllare la posizione di apertura di una pagina collegata. L’aggiunta di un attributo target in un tag di ancoraggio può specificare se il collegamento deve essere aperto in una nuova scheda, nella stessa scheda o in una cornice diversa.

Per definire la destinazione di un collegamento, effettua le seguenti operazioni:

1. In un componente **[!UICONTROL Testo]** in cui è stato inserito un collegamento, seleziona il collegamento.

1. Dalla scheda **[!UICONTROL Impostazioni]**, seleziona la posizione in cui si apre il collegamento nel menu a discesa **[!UICONTROL Target]**. I valori possibili sono elencati di seguito:

   * **[!UICONTROL Nessuno]**: il collegamento viene aperto nello stesso frame in cui è stato fatto clic (impostazione predefinita).
   * **[!UICONTROL Vuoto]**: il collegamento viene aperto in una nuova finestra o scheda.
   * **[!UICONTROL Stesso]**: il collegamento viene aperto nello stesso frame in cui è stato fatto clic.
   * **[!UICONTROL Principale]**: il collegamento viene aperto nel frame principale.
   * **[!UICONTROL Superiore]**: il collegamento viene aperto nel corpo completo della finestra.

   ![](assets/link_2.png)

1. Salva le modifiche.


### Sottolinea collegamento {#link-underline}

Seleziona l&#39;opzione **[!UICONTROL Sottolinea collegamento]** per sottolineare l&#39;etichetta del collegamento.

![](assets/link_1.png)

### Colore collegamento {#link-color}

Per cambiare il colore del collegamento, fai clic su **[!UICONTROL Colore collegamento]** dalla scheda **[!UICONTROL Stili]**.

![](assets/link_3.png)


## Gestire il tracciamento {#manage-tracking}

[E-mail Designer](content-from-scratch.md) consente di gestire gli URL tracciati, ad esempio modificando il tipo di tracciamento per ogni collegamento.

1. Fai clic sull&#39;icona **[!UICONTROL Collegamenti]** nel riquadro a sinistra per visualizzare l&#39;elenco di tutti gli URL del contenuto che verranno tracciati.

   Questo elenco consente di avere una visualizzazione centralizzata e di individuare ogni URL nel contenuto dell’e-mail.

1. Per modificare un collegamento, fai clic sull’icona a forma di matita corrispondente.

1. Se necessario, puoi modificare il **[!UICONTROL Tipo di tracciamento]**:

   ![](assets/message-tracking-edit-a-link.png)

   Per ogni URL tracciato, puoi impostare la modalità di tracciamento su uno dei seguenti valori:

   * **[!UICONTROL Tracciato]**: attiva il tracciamento su questo URL.
   * **[!UICONTROL Rinuncia]**: considera questo URL come un URL di rinuncia o di annullamento dell’iscrizione.
   * **[!UICONTROL Pagina mirror]**: considera questo URL come un URL della pagina mirror.
   * **[!UICONTROL Mai]**: non attiva mai il tracciamento di questo URL.

Il reporting sulle aperture e sui clic è disponibile nel [rapporto live](../reports/live-report.md) e nel [rapporto Customer Journey Analytics](../reports/report-gs-cja.md).

## Personalizzare il tracciamento URL {#url-tracking}

Per istruzioni dettagliate sulla personalizzazione degli URL (tra cui come personalizzare i parametri di tracciamento URL e come personalizzare un URL completo/di base), consulta [Personalizzazione URL](url-personalization.md).
