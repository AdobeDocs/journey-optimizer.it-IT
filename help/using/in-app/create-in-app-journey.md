---
title: Creare una notifica in-app in un Percorso
description: Scopri come creare un messaggio in-app in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: in-app, messaggio, creazione, avvio
hide: true
hidefromtoc: true
exl-id: b774e34f-8225-41a0-a2ec-b91d3a86cf2b
source-git-commit: 252011710574122c1f321a388b65bdafb7c666df
workflow-type: tm+mt
source-wordcount: '553'
ht-degree: 3%

---

# Creare un messaggio in-app in un Percorso {#create-in-app-journey}

>[!AVAILABILITY]
>
>L’attività in-app è attualmente disponibile come versione beta solo per alcuni utenti. Per partecipare al programma beta, contatta l’Assistenza clienti Adobe.

1. Apri il percorso, quindi trascina e rilascia una **[!UICONTROL In-app]** attività dal **[!UICONTROL Azioni]** della palette.

   Quando un profilo raggiunge la fine del percorso, tutti i messaggi in-app visualizzati scadranno automaticamente. Per questo motivo, dopo l’attività in-app viene aggiunta automaticamente un’attività Attendi per garantire la corretta tempistica.

   ![](assets/in_app_journey_1.png)

1. Inserisci un **[!UICONTROL Etichetta]** e **[!UICONTROL Descrizione]** per il tuo messaggio.

1. Scegli la [Superficie in-app](inapp-configuration.md) da utilizzare.

   ![](assets/in_app_journey_2.png)

1. Ora puoi iniziare a progettare i contenuti con **[!UICONTROL Modifica contenuto]** pulsante . [Ulteriori informazioni](design-in-app.md)

1. Fai clic su **[!UICONTROL Modifica trigger]** per configurare il trigger.

   ![](assets/in_app_journey_4.png)

1. Scegli la frequenza del trigger quando il messaggio in-app è attivo:

   * **[!UICONTROL Mostra ogni volta]**: Mostra sempre il messaggio quando gli eventi selezionati nella **[!UICONTROL Attivazione app mobile]** si verificano a discesa.
   * **[!UICONTROL Mostra una volta]**: Mostra questo messaggio solo la prima volta che gli eventi selezionati nel **[!UICONTROL Attivazione app mobile]** si verificano a discesa.
   * **[!UICONTROL Mostra fino a click-through]**: Mostra questo messaggio quando gli eventi selezionati nella **[!UICONTROL Attivazione app mobile]** si verifica fino a quando un evento interattivo non viene inviato dall&#39;SDK con un&#39;azione di &quot;clic&quot;.

1. Da **[!UICONTROL Attivazione app mobile]** a discesa, scegli gli eventi e i criteri che attiveranno il messaggio:

   1. Dall’elenco a discesa a sinistra, seleziona l’evento necessario per attivare il messaggio.
   1. Dall’elenco a discesa a destra, seleziona la convalida richiesta per l’evento selezionato.
   1. Fai clic sul pulsante **[!UICONTROL Aggiungi]** se desideri che il trigger consideri più eventi o criteri. Quindi, ripeti i passaggi precedenti.
   1. Seleziona il collegamento degli eventi, ad esempio scegli **[!UICONTROL E]** se vuoi **entrambi** trigger impostati su true per mostrare o scegliere un messaggio **[!UICONTROL Oppure]** se desideri che il messaggio venga visualizzato se **o** dei trigger sono true.
   1. Fai clic su **[!UICONTROL Salva]** quando i trigger sono stati configurati.

   ![](assets/in_app_journey_3.png)

1. Se necessario, completa il flusso di percorso trascinando e rilasciando azioni o eventi aggiuntivi. [Ulteriori informazioni](../building-journeys/about-journey-activities.md)

1. Quando il messaggio in-app è pronto, finalizza la configurazione e pubblica il percorso per attivarla.

Per ulteriori informazioni su come configurare un percorso, consulta [questa pagina](../building-journeys/journey-gs.md).

## Limitazioni delle attività in-app {#in-app-activity-limitations}

* Questa funzione non è attualmente disponibile per i clienti del settore medicale.

* La personalizzazione può contenere solo attributi di profilo.

* La visualizzazione in-app è legata alla durata del percorso, il che significa che quando il percorso termina per un profilo, tutti i messaggi in-app all’interno di quel percorso cesseranno di essere visualizzati per quel profilo.  Di conseguenza, non è possibile interrompere un messaggio in-app direttamente da un’attività del percorso. Al contrario, dovrai terminare l’intero percorso per impedire che i messaggi in-app vengano visualizzati nel profilo.

* In modalità di test, la visualizzazione in-app dipende dalla durata del percorso. Per evitare che il percorso si termini troppo presto durante il test, regolare la **[!UICONTROL Tempo di attesa]** valore per **[!UICONTROL Wait]** attività.

* **[!UICONTROL Reazione]** Le attività non possono essere utilizzate per reagire a un clic o apertura in-app.

* Si verifica un ritardo di attivazione tra il momento in cui un profilo utente raggiunge un’attività in-app nell’area di lavoro e il momento in cui inizia a vedere quel messaggio in-app. Questo ritardo può variare da 15 minuti a 1 ora.

**Argomenti correlati:**

* [Progettare un messaggio in-app](design-in-app.md)
* [Test e invio del messaggio in-app](send-in-app.md)
* [Rapporto in-app](../reports/campaign-global-report.md#inapp-report)
* [Configurazione in-app](inapp-configuration.md)
