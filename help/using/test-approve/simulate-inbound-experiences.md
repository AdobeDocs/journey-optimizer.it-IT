---
title: Simula azioni in entrata
description: Scopri come simulare esperienze in entrata nelle campagne di azione prima dell’attivazione.
feature: Campaigns, Preview
topic: Content Management
role: User
level: Beginner
badge: label="Beta privata" type="Informative"
hide: true
exl-tag: PrivateBeta
source-git-commit: 916b5875a96eae7b0a4aca86fe35022f21841dd8
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 2%
---

# Simulare esperienze in entrata {#simulate-inbound-experiences}

>[!BEGINSHADEBOX]

**In questa pagina:** convalida le esperienze della campagna di azioni in entrata con utenti simulati prima della pubblicazione, inclusi l&#39;anteprima di collegamenti e QR, il comportamento di simulazione e le limitazioni chiave.

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Questa funzionalità è attualmente disponibile in Private Beta. Per richiedere l’accesso, contatta il tuo rappresentante Adobe.

## Panoramica {#inbound-simulation-overview}

La simulazione dell&#39;esperienza in entrata consente di convalidare esperienze in entrata personalizzate per una **campagna di azioni** con utenti simulati prima che la campagna sia in esecuzione. Utilizzalo per verificare il targeting, le decisioni, i contenuti di cui è stato eseguito il rendering e il comportamento di risoluzione dei problemi tra i percorsi di anteprima web e mobili.

All&#39;avvio della modalità di simulazione, la campagna entra nello stato **[!UICONTROL Simulazione]**. Puoi spostarti e tornare in un secondo momento mentre la simulazione rimane attiva e il contenuto e la configurazione della campagna sono bloccati per la modifica (come avviene per lo stato pubblicato). Le esperienze simulate non sono esposte al pubblico di produzione.

Per l&#39;intero flusso di revisione della campagna, incluso il contesto di anteprima e simulazione del contenuto, vedere [Rivedere e attivare una campagna di azioni](../campaigns/review-activate-campaign.md).

## Attiva ed esegui modalità simulazione {#enter-simulation-mode}

Per accedere alla modalità di simulazione:

1. Nella campagna Azione, accedi a **[!UICONTROL Verifica per attivare]** l&#39;interfaccia, quindi seleziona la scheda **[!UICONTROL Simula azioni]**.

   ![](assets/simulation-mode-enter.png)

1. Selezionare gli utenti simulati che si desidera utilizzare per la simulazione utilizzando uno dei metodi disponibili:

   * **[!UICONTROL Sfoglia inventario]** - Seleziona gli utenti simulati creati in precedenza.
   * **[!UICONTROL Crea da modulo]** - Crea un campo utente simulato per campo.
   * **[!UICONTROL Crea da JSON]** - Importa un payload del profilo utente simulato per il file JSON.

   ![](assets/simulation-mode-ui.png)

   Per ulteriori dettagli sulla creazione e la gestione degli utenti simulati, consultare [Creare e gestire gli utenti simulati](../building-journeys/simulate-journey.md#test-users).

1. Una volta selezionati o creati gli utenti simulati, questi vengono visualizzati nel riquadro centrale. Per ogni utente è possibile visualizzare i dettagli, aggiornare le informazioni relative all&#39;utente o rimuovere l&#39;utente dall&#39;elenco di simulazione.

   ![](assets/simulation-mode-users.png)

1. Per generare l&#39;output simulato per ogni utente, fare clic sul pulsante **[!UICONTROL Genera collegamento]**. Questo genera:

   * URL condivisibile per visualizzare in anteprima l’esperienza in entrata sottoposta a rendering per l’utente selezionato.
   * Un codice QR per scenari di anteprima mobile.

1. Per ogni utente simulato, utilizza i controlli generati per convalidare l’esperienza:

   ![](assets/simulation-mode-generate.png)

   | Pulsante | Funzionamento |
   | --- | --- |
   | ![Apri pulsante collegamento](assets/simulation-action-open.png) | Apri il collegamento generato in un browser per visualizzare in anteprima l’esperienza in entrata per l’utente simulato. |
   | ![Pulsante Copia collegamento](assets/simulation-action-copy.png) | Copia il collegamento generato in modo da poterlo condividere o incollare in un altro browser o dispositivo. |
   | ![Pulsante codice QR](assets/simulation-action-qr.png) | Apri il codice QR (se disponibile per il canale), seleziona **[!UICONTROL iOS]** o **[!UICONTROL Android]**, analizza il codice con la fotocamera del dispositivo e, quando richiesto, immetti il codice visualizzato. |
   | ![Pulsante Altre azioni](assets/simulation-action-more.png) | Apri opzioni aggiuntive a **[!UICONTROL Apri sessione di verifica]** o **[!UICONTROL Nuova sessione di verifica]** e continua a risolvere i problemi nell&#39;interfaccia utente di Assurance. |

1. Puoi uscire dalla modalità di simulazione in qualsiasi momento facendo clic su **[!UICONTROL Interrompi simulazione]** nella barra delle azioni della campagna, ad esempio se devi tornare indietro e modificare la campagna.
