---
solution: Journey Optimizer
product: journey optimizer
title: Configurare l’azione della campagna
description: Scopri come configurare l’azione della campagna.
feature: Campaigns
topic: Content Management
role: User
level: Beginner
mini-toc-levels: 1
keywords: crea, ottimizzatore, campagna, superficie, messaggi
source-git-commit: 1bdba8c5c1a9238d351b159551f6d3924935b339
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 10%

---


# Configurare l’azione della campagna {#action-campaign-action}

Utilizza la scheda **[!UICONTROL Azioni]** per selezionare una configurazione di canale per il messaggio e configurare impostazioni aggiuntive, ad esempio il tracciamento, l&#39;esperimento sul contenuto o il contenuto multilingue.

1. **Scegli il canale**

   Passa alla scheda **[!UICONTROL Azioni]**, fai clic sul pulsante **[!UICONTROL Aggiungi azione]** e seleziona il canale di comunicazione.

   ![](assets/create-campaign-add-action.png)

   >[!NOTE]
   >
   >I canali disponibili variano in base al modello di licenza e ai componenti aggiuntivi.

1. **Seleziona una configurazione di canale**

   Configurazione definita da un [amministratore di sistema](../start/path/administrator.md). Contiene tutti i parametri tecnici per l’invio del messaggio, ad esempio parametri di intestazione, sottodominio, app mobili e così via. [Scopri come impostare le configurazioni dei canali](../configuration/channel-surfaces.md)

   ![](assets/create-campaign-action.png)

1. **Crea un esperimento sui contenuti**

   Utilizza la sezione **[!UICONTROL Esperimento sui contenuti]** per definire più trattamenti di consegna e misurare quale offre le migliori prestazioni per il tuo pubblico di destinazione. Fai clic sul pulsante **[!UICONTROL Crea esperimento]**, quindi segui i passaggi descritti in questa sezione: [Crea un esperimento sui contenuti](../content-management/content-experiment.md).

1. **Aggiungi contenuto multilingue**

   Utilizza la sezione **[!UICONTROL Lingue]** per creare contenuti in più lingue all&#39;interno della campagna. A tale scopo, fare clic sul pulsante **[!UICONTROL Aggiungi lingue]** e selezionare le **[!UICONTROL impostazioni lingua]** desiderate. Informazioni dettagliate su come impostare e utilizzare le funzionalità multilingue sono disponibili in questa sezione: [Introduzione ai contenuti multilingue](../content-management/multilingual-gs.md)

Sono disponibili impostazioni aggiuntive a seconda del canale di comunicazione selezionato. Per ulteriori informazioni, espandi le sezioni seguenti.

+++**Applica regole limite** (e-mail, direct mailing, push, SMS)

Nell&#39;elenco a discesa **[!UICONTROL Regole aziendali]**, seleziona un set di regole per applicare le regole di limitazione alla campagna. L’utilizzo dei set di regole di canale consente di impostare i limiti di frequenza per tipo di comunicazione per evitare di sovraccaricare i clienti con messaggi simili. [Scopri come utilizzare i set di regole](../conflict-prioritization/rule-sets.md)

+++

+++**Rileva coinvolgimento** (e-mail, SMS).

Utilizza la sezione **[!UICONTROL Tracciamento delle azioni]** per tenere traccia di come i destinatari reagiscono alle consegne e-mail o SMS. I risultati del tracciamento sono accessibili dal rapporto della campagna una volta eseguita la campagna. [Ulteriori informazioni sui report delle campagne](../reports/campaign-global-report-cja.md)

+++

+++**Attiva modalità Consegna rapida** (Push).

La modalità Consegna rapida è un componente aggiuntivo [!DNL Journey Optimizer] che consente l&#39;invio molto rapido di messaggi push in volumi elevati tramite campagne. La consegna rapida viene utilizzata quando il ritardo nella consegna dei messaggi è di importanza critica per l’azienda, quando si desidera inviare un avviso push urgente sui telefoni cellulari, ad esempio una notizia straordinaria agli utenti che hanno installato la tua app per il canale news. Per ulteriori informazioni sulle prestazioni quando si utilizza la modalità Consegna rapida, consultare [Descrizione del prodotto Adobe Journey Optimizer](https://helpx.adobe.com/it/legal/product-descriptions/adobe-journey-optimizer.html).

+++

+++**Assegna punteggi di priorità** (Web, In-app, basati su codice)

Assegnare un punteggio di priorità alla campagna ti consente di assegnare la priorità a una campagna in entrata e in uscita in presenza di un vincolo imposto, ad esempio un limite di frequenza. Immetti un valore numerico (da 0 a 100). Tieni presente che più alto è il numero, maggiore è la priorità. [Scopri come assegnare punteggi di priorità a percorsi e campagne](../conflict-prioritization/priority-scores.md)

+++

+++**Imposta regole di consegna aggiuntive** (schede contenuto)

Per le campagne basate su schede di contenuto, puoi abilitare regole di consegna aggiuntive per scegliere gli eventi e i criteri di attivazione del messaggio. [Scopri come creare le schede dei contenuti](../content-card/create-content-card.md)

+++

+++**Definisci trigger** (in-app)

Per i messaggi in-app, puoi utilizzare il pulsante **[!UICONTROL Modifica trigger]** per scegliere gli eventi e i criteri che attivano il messaggio. [Scopri come creare un messaggio in-app](../in-app/create-in-app.md)

+++

## Passaggi successivi {#next}

Quando l’azione della campagna è pronta, puoi progettarne il contenuto. [Ulteriori informazioni](campaign-content.md)
