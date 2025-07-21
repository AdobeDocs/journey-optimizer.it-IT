---
solution: Journey Optimizer
product: journey optimizer
title: Configurare l’azione della campagna attivata dall’API
description: Scopri come configurare l’azione della campagna attivata dall’API.
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: campagne, attivate da API, REST, ottimizzatore, messaggi
source-git-commit: 1bdba8c5c1a9238d351b159551f6d3924935b339
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 7%

---


# Configurare l’azione della campagna attivata dall’API {#api-action}

Utilizza la scheda **[!UICONTROL Azioni]** per selezionare una configurazione di canale per il messaggio e configurare impostazioni aggiuntive, ad esempio il tracciamento, l&#39;esperimento sul contenuto o il contenuto multilingue.

1. **Scegliere il canale**.

   Passa alla scheda **[!UICONTROL Azioni]**, fai clic sul pulsante **[!UICONTROL Aggiungi azione]** e seleziona il canale di comunicazione.

   ![](assets/api-triggered-channel.png)

   >[!NOTE]
   >
   >I canali disponibili variano in base al modello di licenza e ai componenti aggiuntivi.
   >
   >Per le campagne attivate da API, sono disponibili solo i canali e-mail, SMS e di notifica push.

1. **Seleziona una configurazione di canale**

   Configurazione definita da un [amministratore di sistema](../start/path/administrator.md). Contiene tutti i parametri tecnici per l’invio del messaggio, ad esempio parametri di intestazione, sottodominio, app mobili e così via. [Scopri come impostare le configurazioni dei canali](../configuration/channel-surfaces.md)

   ![](assets/create-campaign-action.png)

1. **Crea un esperimento sui contenuti**

   Utilizza la sezione **[!UICONTROL Esperimento sui contenuti]** per definire più trattamenti di consegna e misurare quale offre le migliori prestazioni per il tuo pubblico di destinazione. Fai clic sul pulsante **[!UICONTROL Crea esperimento]**, quindi segui i passaggi descritti in questa sezione: [Crea un esperimento sui contenuti](../content-management/content-experiment.md).

1. **Aggiungi contenuto multilingue**

   Utilizza la sezione **[!UICONTROL Lingue]** per creare contenuti in più lingue all&#39;interno della campagna. A tale scopo, fare clic sul pulsante **[!UICONTROL Aggiungi lingue]** e selezionare le **[!UICONTROL impostazioni lingua]** desiderate. Informazioni dettagliate su come impostare e utilizzare le funzionalità multilingue sono disponibili in questa sezione: [Introduzione ai contenuti multilingue](../content-management/multilingual-gs.md)

Sono disponibili impostazioni aggiuntive a seconda del canale di comunicazione selezionato. Per ulteriori informazioni, espandi le sezioni seguenti.

+++**Applica regole limite** (e-mail, push, SMS)

Nell&#39;elenco a discesa **[!UICONTROL Regole aziendali]**, seleziona un set di regole per applicare le regole di limitazione alla campagna. L’utilizzo dei set di regole di canale consente di impostare i limiti di frequenza per tipo di comunicazione per evitare di sovraccaricare i clienti con messaggi simili. [Scopri come utilizzare i set di regole](../conflict-prioritization/rule-sets.md)

+++

+++**Rileva coinvolgimento** (e-mail, SMS).

Utilizza la sezione **[!UICONTROL Tracciamento delle azioni]** per tenere traccia di come i destinatari reagiscono alle consegne e-mail o SMS. I risultati del tracciamento sono accessibili dal rapporto della campagna una volta eseguita la campagna. [Ulteriori informazioni sui report delle campagne](../reports/campaign-global-report-cja.md)

+++

+++**Attiva modalità Consegna rapida** (Push).

La modalità Consegna rapida è un componente aggiuntivo [!DNL Journey Optimizer] che consente l&#39;invio molto rapido di messaggi push in volumi elevati tramite campagne. La consegna rapida viene utilizzata quando il ritardo nella consegna dei messaggi è di importanza critica per l’azienda, quando si desidera inviare un avviso push urgente sui telefoni cellulari, ad esempio una notizia straordinaria agli utenti che hanno installato la tua app per il canale news. Per ulteriori informazioni sulle prestazioni quando si utilizza la modalità Consegna rapida, consultare [Descrizione del prodotto Adobe Journey Optimizer](https://helpx.adobe.com/it/legal/product-descriptions/adobe-journey-optimizer.html).

+++

## Passaggi successivi {#next}

Una volta che la configurazione e il contenuto della campagna sono pronti, puoi progettarne il contenuto. [Ulteriori informazioni](api-triggered-campaign-content.md)
