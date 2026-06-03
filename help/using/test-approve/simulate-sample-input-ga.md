---
solution: Journey Optimizer
product: journey optimizer
title: Simulare varianti di contenuto
description: Scopri come visualizzare in anteprima le varianti di contenuto, generare automaticamente le varianti con IA, gestire i profili di test e inviare bozze dall’esperienza Simula varianti di contenuto.
feature: Email, Email Rendering, Personalization, Preview, Proofs
topic: Content Management
role: User
level: Intermediate
hide: true
exl-id: 2744974b-62cc-4d25-acc3-edd4c53a9a58
TQID: https://experienceleague.adobe.com/Y8qsGW8XqSVqag4yqRinnem9w2PYJyKIDIWvuGqAchU
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: dc22c819-3f29-4e91-8b7d-5c6719831141
subfeature_v2: id: a5683ded-e5d5-4ec6-b9fd-e1b56a94ab96id: f8d2e9f0-69c9-40cd-890f-71336c8dfff7id: bf7a266e-e483-42c6-b5bc-09ca6e49900c
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: bcc5edb5-84c3-4940-9f84-ed88b6c16274id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: c5a6e06cc93e8ed03edc368f3d02eccd655a7461
workflow-type: tm+mt
source-wordcount: 1313
ht-degree: 1%

---

# Simulare varianti di contenuto {#custom-profiles}

>[!CONTEXTUALHELP]
>id="ajo_simulate_sample_profiles"
>title="Simulazione tramite input di esempio"
>abstract="In questa schermata, puoi testare le varianti di contenuto generandole automaticamente con IA, aggiungendo valori tramite un modello CSV o JSON, immettendole manualmente o utilizzando i profili di test."

Quando il contenuto include personalizzazione o logica condizionale, devi verificare che esegua correttamente il rendering per ogni tipo di destinatario prima di inviarlo.

L&#39;esperienza **[!UICONTROL Simula varianti di contenuto]** in [!DNL Journey Optimizer] risolve questo problema consentendo di testare più varianti di contenuto da una singola schermata, generate automaticamente con IA, immesse manualmente, importate da un file o basate su utenti simulati riutilizzabili. Puoi visualizzare in anteprima il rendering di ogni variante e inviare bozze, il tutto senza creare in precedenza profili persistenti in Adobe Experience Platform.

Dal contenuto, seleziona **[!UICONTROL Simula contenuto]** e quindi **[!UICONTROL Simula varianti di contenuto]** per aprire una singola esperienza in cui puoi:

* **Genera automaticamente varianti** utilizzando IA per coprire i rami di personalizzazione e condizionali
* **Aggiungi varianti manualmente** o da un file CSV o JSON
* **Utilizza utenti simulati** per visualizzare in anteprima e verificare i dati di test salvati e riutilizzabili
* **Anteprima** rendering e **invia bozze e-mail** per le varianti selezionate

Tutti gli attributi utilizzati nel contenuto per la personalizzazione vengono rilevati automaticamente. Una variante è una versione del contenuto con valori diversi per i relativi attributi.

>[!NOTE]
>
>Le varianti fungono solo da scopo di test per il contenuto corrente. Non vengono memorizzati in Adobe Experience Platform, ma nella sessione del browser utente, il che significa che non vengono visualizzati alla disconnessione o quando si lavora da un altro dispositivo.

## Guardrail e limitazioni {#limitations}

Prima di iniziare a testare il contenuto utilizzando dati di input di esempio, considera i seguenti guardrail e prerequisiti.

* **Canali** - La simulazione delle varianti di contenuto è disponibile per:

   * i canali di notifica e-mail, SMS e push;
   * tutti i canali in entrata (web, esperienza basata su codice, in-app, schede di contenuto).

* **Funzionalità supportate** - Le varianti di contenuto possono essere utilizzate con [!DNL Journey Optimizer] contenuti multilingue e funzionalità di sperimentazione dei contenuti. Questo consente di testare i messaggi in più lingue e di ottimizzare il contenuto attraverso la sperimentazione.

  Puoi anche sfruttare le varianti di contenuto per testare i modelli di contenuto.

  >[!NOTE]
  >
  >Per il momento, il rendering della casella in entrata e i rapporti di posta indesiderata non sono disponibili nell’esperienza corrente. Per utilizzare queste funzionalità, seleziona dal contenuto il pulsante **[!UICONTROL Simula contenuto]** per accedere all&#39;interfaccia utente precedente.

* **Attributi** - Sono supportati sia gli attributi di profilo che quelli contestuali.

* **Tipi di dati** - Durante l&#39;immissione dei dati per le varianti sono supportati solo i tipi di dati seguenti: numero (intero e decimale), stringa, booleano e tipo di data. Qualsiasi altro tipo di dati mostrerà un errore.

* **Numero di varianti** - È possibile aggiungere fino a 30 varianti per testare il contenuto, utilizzando un file, manualmente o tramite generazione automatica.

## Crea varianti di contenuto

Per creare varianti per il contenuto, fai clic sul pulsante **[!UICONTROL Simula contenuto]** e scegli **[!UICONTROL Simula varianti di contenuto]**.

![Opzione Simula varianti di contenuto](assets/simulate-sample.png)

Puoi creare varianti nei seguenti modi:

* [Aggiungere varianti manualmente o da un file](#profiles).
* [Genera automaticamente le varianti](#auto-generate-variants) con IA.
* [Seleziona varianti da utenti simulati esistenti](#simulated-users).

Una volta create le varianti, puoi [visualizzare l&#39;anteprima del contenuto e inviare bozze](#preview-proofs).

### Aggiungere varianti manualmente o da un file {#profiles}

Quando accedi all’esperienza delle varianti di contenuto, tutti i campi di personalizzazione utilizzati nel contenuto vengono rilevati e visualizzati automaticamente in una variante vuota.

Ad esempio, se l’e-mail contiene due campi di personalizzazione &quot;Nome&quot; e &quot;Città&quot;, questi verranno visualizzati nell’elenco. Inizialmente non viene immesso alcun valore e nel riquadro di anteprima non viene visualizzato alcun contenuto personalizzato.

![Elenco delle varianti di input di esempio](assets/simulate-custom-variants-list.png)

Puoi aggiungere varianti manualmente o caricarle da un file.

+++ Aggiungere varianti manualmente

Per modificare il valore della variante predefinita, fai clic sul pulsante **[!UICONTROL Modifica]** per fornire valori personalizzati per ogni campo di personalizzazione. Il riquadro di anteprima viene aggiornato per mostrare il rendering del contenuto con i valori immessi.

Per aggiungere una nuova variante, fare clic sul pulsante **[!UICONTROL Crea campione]**. Viene visualizzata una nuova variante vuota, contenente tutti i campi di personalizzazione rilevati. Puoi modificare la nuova variante in base alle esigenze.

![Crea pulsante di input di esempio](assets/simulate-custom-add.png)

+++

+++ Aggiungere varianti da un file

Puoi caricare un file con varianti e valori predefiniti per accelerare il processo.

1. Fai clic sul pulsante **[!UICONTROL Carica dati]** per aprire la schermata di caricamento file.
1. Seleziona **[!UICONTROL Scarica esempio]** per scaricare un modello di file CSV, JSON o JSONLINES.
1. Apri il file modello e inserisci i valori desiderati per ciascun attributo di profilo. Il modello include una colonna per ogni attributo di profilo utilizzato nel contenuto per la personalizzazione.

   Esempio di sintassi JSON:

   ```json
   {
   "profile": {
       "attributes": {
       "person": {
           "name": {
               "lastName": "Doe",
               "firstName": "John"
               }
           }
       }
   }
   }
   ```

1. Quando il file è pronto, seleziona **[!UICONTROL Conferma]** per caricarlo. Dopo il caricamento, viene aggiunta una nuova variante all’elenco per ogni voce del file.

+++

### Genera automaticamente varianti di contenuto {#auto-generate-variants}

[!DNL Journey Optimizer] può utilizzare la simulazione basata sull&#39;intelligenza artificiale per generare automaticamente una variante di contenuto in modo da poter convalidare la logica di personalizzazione senza creare varianti manualmente. Durante il rendering del contenuto per la simulazione o la verifica, il sistema analizza il contenuto, identifica i campi di personalizzazione e li sostituisce con valori significativi per un’anteprima quasi realistica.

Per generare automaticamente una variante, fai clic sul pulsante **[!UICONTROL Genera]** e attendi che il sistema generi la variante. Esamina la variante generata nell’elenco delle varianti e il relativo rendering.

![Pulsante Genera varianti](assets/simulate-variants-generate.png)

>[!NOTE]
>
>La generazione produce una singola variante. Facendo clic su **[!UICONTROL Genera]** tutte le varianti di contenuto esistenti nell&#39;elenco, comprese quelle aggiunte manualmente o da un file, vengono sostituite con una variante generata.

### Seleziona varianti da utenti simulati {#simulated-users}

In **[!UICONTROL Simula varianti di contenuto]**, puoi basare le varianti su **utenti simulati**. Gli utenti simulati sono entità temporanee simili a profili create per il test senza utilizzare profili persistenti in Adobe Experience Platform. A differenza delle varianti aggiunte solo per la sessione corrente del browser, gli utenti simulati vengono salvati e possono essere riutilizzati in più percorsi e da altri utenti.

Gli utenti simulati vengono creati e gestiti dalla funzionalità **[!UICONTROL Simulazione]** del percorso. Per informazioni sulla procedura completa per la creazione, il salvataggio e il riutilizzo degli utenti, vedere [Creare e gestire utenti simulati](../building-journeys/simulate-journey.md#test-users).

Una volta creati gli utenti simulati, puoi utilizzarli per visualizzare l’anteprima del contenuto. Per farlo, segui questi passaggi:

1. Fai clic sul pulsante **[!UICONTROL Seleziona varianti]**.
1. Nell&#39;elenco degli utenti simulati esistenti, selezionare quelli che si desidera utilizzare, quindi fare clic su **[!UICONTROL Seleziona]**.

   ![Selezionare gli utenti simulati da utilizzare come varianti di contenuto](assets/simulate-custom-simulated.png)

1. Gli utenti simulati selezionati vengono aggiunti all’elenco delle varianti di contenuto, in cui puoi visualizzare l’anteprima del contenuto con i relativi valori di attributo. Puoi anche modificare manualmente i valori di una variante per il test, ma queste modifiche non vengono salvate nuovamente nell’utente simulato.

## Anteprima del contenuto e invio delle bozze {#preview-proofs}

Una volta aggiunte le varianti, puoi utilizzarle per visualizzare l’anteprima del contenuto nel riquadro a destra e per inviare bozze e-mail.

### Anteprima varianti di contenuto {#preview}

Per visualizzare l’anteprima del contenuto utilizzando una variante, seleziona la variante pertinente dall’elenco per aggiornare il contenuto nel riquadro di anteprima con le informazioni immesse per questa variante.

Nell’esempio seguente, sono state aggiunte due varianti per la riga dell’oggetto dell’e-mail:

| Selezione variante 1 | Selezione variante 2 |
|----------|-------------|
| ![Selezione variante 1](assets/simulate-custom-boxes.png) | ![Selezione variante 2](assets/simulate-custom-boxes2.png) |

<!--
For multilingual content and experimentation, a dropdown is available to switch between the different language variants or treatments.

![Language or treatment selector](assets/simulate-custom-experiment.png)
-->

### Inviare bozze {#proofs}

Journey Optimizer ti consente di inviare bozze agli indirizzi e-mail impersonando una o più varianti aggiunte nella schermata di simulazione. I passaggi sono i seguenti:

1. Verifica che siano state aggiunte varianti per verificare il contenuto e fai clic sul pulsante **[!UICONTROL Invia bozza]**.

1. Nel campo **[!UICONTROL Destinatari]**, inserisci l&#39;indirizzo e-mail a cui desideri inviare la bozza, quindi fai clic su **[!UICONTROL Aggiungi]**. Ripeti l’operazione per inviare la bozza ad altri indirizzi e-mail. Puoi aggiungere fino a 10 destinatari della bozza.

1. Nella sezione inferiore della schermata, seleziona la variante da utilizzare nella bozza. Puoi selezionare più varianti, nel qual caso l’e-mail includerà tante bozze quante sono le varianti selezionate.

   Per ulteriori informazioni su una variante, seleziona il collegamento **[!UICONTROL Visualizza dettagli profilo]**. Questo consente di visualizzare le informazioni immesse nella schermata precedente per le diverse varianti.

   ![Destinatari bozza e selezione variante](assets/simulate-custom-proofs.png)

1. Fare clic sul pulsante **[!UICONTROL Invia bozza]** per iniziare a inviare la bozza.

1. Per tenere traccia dell&#39;invio della bozza, fare clic sul pulsante **[!UICONTROL Visualizza bozze]** nella schermata Simula contenuto.

![Elenco bozze inviate](assets/simulate-custom-sent-proofs.png)
