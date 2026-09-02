---
solution: Journey Optimizer
product: journey optimizer
title: Simulare varianti di contenuto
description: Scopri come visualizzare in anteprima tutte le varianti di contenuto una accanto all’altra, gestirle dalla barra delle azioni in basso e passare all’esperienza classica nell’esperienza riprogettata Simula varianti di contenuto.
feature: Email, Email Rendering, Personalization, Preview, Proofs
topic: Content Management
role: User
level: Intermediate
exl-id: d9f7e0a3-b8c2-4e5f-92a1-3c1d7e8a4f65
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
subfeature_v2:
  - id: f8d2e9f0-69c9-40cd-890f-71336c8dfff7
  - id: a5683ded-e5d5-4ec6-b9fd-e1b56a94ab96
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: bcc5edb5-84c3-4940-9f84-ed88b6c16274
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 0ea831b383982d312357e1d7893675818650325e
workflow-type: tm+mt
source-wordcount: 843
ht-degree: 1%

---


# Simulare varianti di contenuto {#simulate-content-variations}

>[!BEGINSHADEBOX]

**In questa pagina:** visualizza in anteprima tutte le varianti di contenuto in una griglia affiancata, gestiscele da una barra delle azioni inferiore consolidata e tornate all&#39;esperienza classica in qualsiasi momento.

>[!ENDSHADEBOX]

L&#39;esperienza **[!UICONTROL Simula varianti di contenuto]** è stata riprogettata per rendere più semplici e veloci i test e il confronto delle varianti. Tutte le varianti ora vengono riprodotte insieme in un&#39;unica griglia scorrevole e ogni controllo necessario è disponibile da una singola barra delle azioni inferiore.

Per accedere alla nuova esperienza, dal tuo contenuto fai clic su **[!UICONTROL Simula contenuto]** per aprire la schermata di simulazione del contenuto. Se sono già disponibili varianti, la griglia di anteprima viene visualizzata immediatamente. Se non ne esiste ancora alcuna, viene visualizzata una variante vuota e puoi iniziare a crearla utilizzando uno dei metodi descritti di seguito.

Se preferisci il layout precedente, fai clic su **[!UICONTROL Passa all&#39;esperienza classica]** nella barra delle azioni inferiore in qualsiasi momento. La documentazione relativa all&#39;esperienza classica è disponibile all&#39;indirizzo [Simulare varianti di contenuto (esperienza classica)](simulate-sample-input.md).

## Creare e gestire le varianti {#manage-variants}

Le varianti possono essere create in diversi modi: manualmente una per una oppure importando un file, generandoli con IA o selezionando gli utenti simulati esistenti. Puoi aggiungere fino a 30 varianti manualmente o tramite caricamento di file. Quando si utilizza la generazione di IA, è possibile creare fino a 40 varianti a seconda della complessità del contenuto.

### Aggiungere varianti manualmente {#add-variants}

Per aggiungere manualmente una variante vuota, fare clic su **[!UICONTROL +]** nella barra delle azioni inferiore. Viene aggiunta una nuova variante vuota e puoi immettere direttamente i valori dell’attributo.

![](assets/simulate-variations-create.png)

È inoltre possibile utilizzare **[!UICONTROL ...]** > **Carica varianti** per importare un file CSV, JSON o JSONLINES in cui ogni riga o voce diventa una variante. Scarica il modello di file dalla finestra di dialogo di caricamento per utilizzare il formato corretto.

![](assets/simulate-variations-upload.png)

### Genera automaticamente varianti {#auto-generate}

Per generare automaticamente le varianti utilizzando l&#39;intelligenza artificiale, fai clic sul pulsante **[!UICONTROL Genera]** nella barra delle azioni inferiore. Il sistema analizza i contenuti, identifica i campi di personalizzazione e i rami condizionali e genera tutte le varianti necessarie per includerli in valori realistici. Le varianti generate da intelligenza artificiale possono essere identificate dall’icona a forma di scintilla visualizzata sulla scheda.

![](assets/simulate-variations-ai.png)

>[!CAUTION]
>
>Facendo clic su **[!UICONTROL Genera]**, vengono sostituite tutte le varianti esistenti, comprese quelle aggiunte manualmente o da un file.

### Seleziona varianti da utenti simulati {#simulated-users}

Puoi basare le varianti su **utenti simulati** che sono entità di test riutilizzabili, simili a profili, salvate in più sessioni e condivisibili con altri utenti. A differenza delle varianti immesse manualmente, gli utenti simulati persistono oltre la sessione corrente del browser.

Gli utenti simulati vengono creati e gestiti dalla funzionalità **[!UICONTROL Simulazione]** del percorso. Per informazioni sulla procedura completa, vedere [Creare e gestire utenti simulati](../building-journeys/simulate-journey.md#test-users).

Per utilizzare gli utenti simulati come varianti:

1. Fai clic su **[!UICONTROL Seleziona varianti]** nella barra delle azioni inferiore.
1. Selezionare dall&#39;elenco gli utenti simulati che si desidera utilizzare, quindi fare clic su **[!UICONTROL Seleziona]**.

![](assets/simulate-variations-select.png)

Gli utenti simulati selezionati vengono aggiunti come varianti. Puoi modificare localmente i valori degli attributi di una variante per il test, ma tali modifiche non vengono salvate nuovamente nel record utente simulato.

### Esporta varianti {#export-variants}

Puoi esportare in un file CSV tutte le varianti correnti, aggiunte manualmente, generate con IA o selezionate da utenti simulati. Fai clic su **[!UICONTROL ...]** nella barra delle azioni inferiore, quindi seleziona **[!UICONTROL Esporta varianti]**.

![](assets/simulate-variations-upload.png)

## Anteprima varianti {#preview-grid}

### Passare da una variante all’altra {#switch-variants}

In modalità anteprima, tutte le varianti vengono visualizzate una accanto all’altra con un indicatore numerato in alto. Per passare da una variante all&#39;altra, fai clic sul numero o utilizza i pulsanti di navigazione **&lt; >** nella barra delle azioni inferiore.

![](assets/simulate-variations-switch.png)

### Visualizzare le varianti in modalità anteprima o modifica {#edit-variants}

È possibile visualizzare le varianti in modalità anteprima o modifica, in cui è possibile modificare direttamente i valori del contenuto e degli attributi. Fai clic su **[!UICONTROL Anteprima]** o **[!UICONTROL Modifica]** nella barra delle azioni inferiore per passare tutte le anteprime contemporaneamente tra le due modalità.

![](assets/simulate-variations-mode.png)

Per attivare o disattivare una singola variante singolarmente, fare clic sul pulsante **[!UICONTROL Mostra anteprima]** o **[!UICONTROL Mostra dettagli variante]** nella parte superiore della scheda oppure premere a lungo il numero corrispondente nella barra delle azioni inferiore (oppure utilizzare Alt + Su/Giù).

![](assets/simulate-variations-unitary-switch.png)

### Modificare il layout {#change-layout}

Per modificare la modalità di visualizzazione delle varianti, utilizzare la **barra delle azioni inferiore** per alternare layout affiancati, sovrapposti verticalmente o a capo automatico.

![](assets/simulate-variations-layout.png)

### Passare da una visualizzazione desktop a una visualizzazione mobile {#switch-views}

Per visualizzare il rendering delle varianti su dispositivi diversi, fai clic sulle icone nella barra delle azioni inferiore per passare dalla vista desktop a quella mobile. La griglia di anteprima viene aggiornata per mostrare l’aspetto delle varianti sul dispositivo selezionato.

![](assets/simulate-variations-device.png)

## Funzionalità aggiuntive per il canale e-mail {#email-capabilities}

Durante la simulazione del contenuto delle e-mail, una barra superiore fornisce strumenti aggiuntivi specifici per le e-mail.

![](assets/simulate-variations-top-bar.png)

* **[!UICONTROL Rapporto spam]**: analizza il contenuto delle e-mail rispetto ai filtri spam e ottieni un punteggio di recapito messaggi. [Ulteriori informazioni](../content-management/spam-report.md)
* **[!UICONTROL Rendering e-mail]** - Anteprima del rendering del messaggio e-mail tra client e dispositivi e-mail più diffusi. [Ulteriori informazioni](../content-management/rendering.md)
* **[!UICONTROL Invia bozza]** - Invia una bozza di una o più varianti a un set di destinatari e-mail. Fai clic su **[!UICONTROL Invia bozza]**, aggiungi fino a 10 indirizzi di destinatari, seleziona le varianti da includere, quindi fai clic su **[!UICONTROL Invia bozza]** per confermare. Per rivedere le bozze inviate in precedenza, fare clic su **[!UICONTROL Visualizza bozze]**. [Ulteriori informazioni](../content-management/proofs.md)
* **[!UICONTROL Visualizza dettagli configurazione]** — controlla la configurazione del canale applicata a questo contenuto.
