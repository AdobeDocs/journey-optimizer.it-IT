---
title: Creare una notifica in-app
description: Scopri come creare un messaggio in-app in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: b3b79fe2-7db3-490d-9c3d-87267aa55eea
source-git-commit: 8d56e3060e78422b028ced17f415497789908ff9
workflow-type: tm+mt
source-wordcount: '543'
ht-degree: 0%

---

# Creare un messaggio in-app {#create-in-app}

## Creare una campagna e un messaggio in-app{#create-in-app-in-a-campaign}

Per creare un messaggio in-app, segui i passaggi seguenti:

1. Accedere al **[!UICONTROL Campaigns]** menu, quindi fai clic su **[!UICONTROL Create campaign]**.

1. In **[!UICONTROL Properties]** Specifica quando eseguire la campagna.

1. In **[!UICONTROL Actions]** scegli la sezione **[!UICONTROL In-app message]** e **[!UICONTROL App surface]** configurato in precedenza per il messaggio in-app. Quindi, fai clic su **[!UICONTROL Create]**.

   [Ulteriori informazioni sulla configurazione in-app](inapp-configuration.md).

   ![](assets/in_app_create_1.png)

1. Da **[!UICONTROL Properties]** , modifica la **[!UICONTROL Title]** e **[!UICONTROL Description]**.

1. Per assegnare etichette di utilizzo dati personalizzate o di base alla pagina di destinazione, seleziona **[!UICONTROL Manage access]**. [Ulteriori informazioni](../administration/object-based-access.md).

1. Fai clic sul pulsante **[!UICONTROL Select audience]** per definire il pubblico di cui eseguire il targeting dall’elenco dei segmenti Adobe Experience Platform disponibili. [Ulteriori informazioni](../segment/about-segments.md).

   ![](assets/in_app_create_2.png)

1. In **[!UICONTROL Identity namespace]** scegli lo spazio dei nomi da utilizzare per identificare gli individui del segmento selezionato. [Ulteriori informazioni](../event/about-creating.md#select-the-namespace).

1. Scegli la frequenza del trigger quando il messaggio in-app è attivo:

   * **[!UICONTROL Show every time]**: Mostra sempre il messaggio quando gli eventi selezionati nella **[!UICONTROL Mobile app trigger]** si verificano a discesa.
   * **[!UICONTROL Show once]**: Mostra questo messaggio solo la prima volta che gli eventi selezionati nel **[!UICONTROL Mobile app trigger]** si verificano a discesa.
   * **[!UICONTROL Show until click through]**: Mostra questo messaggio quando gli eventi selezionati nella **[!UICONTROL Mobile app trigger]** si verifica fino a quando un evento interattivo non viene inviato dall&#39;SDK con un&#39;azione di &quot;clic&quot;.

1. Da **[!UICONTROL Mobile app trigger]** a discesa, scegli gli eventi e i criteri che attiveranno il messaggio:

   1. Dall’elenco a discesa a sinistra, seleziona l’evento necessario per attivare il messaggio.
   1. Dall’elenco a discesa a destra, seleziona la convalida richiesta per l’evento selezionato.
   1. Fai clic sul pulsante **[!UICONTROL Add]** se desideri che il trigger consideri più eventi o criteri. Quindi, ripeti i passaggi precedenti.
   1. Seleziona il collegamento degli eventi, ad esempio scegli **[!UICONTROL And]** se vuoi **entrambi** trigger impostati su true per mostrare o scegliere un messaggio **[!UICONTROL Or]** se desideri che il messaggio venga visualizzato se **o** dei trigger sono true.

   ![](assets/in_app_create_3.png)

1. Scegli l’evento che attiva il messaggio dalla **[!UICONTROL Mobile app trigger]**
a discesa.

   Selezionando un trigger, scegli quale azione utente causa la visualizzazione del messaggio in-app.

   ![](assets/in_app_create_3.png)

1. Le campagne sono progettate per essere eseguite in una data specifica o su una frequenza ricorrente. Scopri come configurare il **[!UICONTROL Schedule]** della campagna in [questa sezione](../campaigns/create-campaign.md#schedule).

   ![](assets/in-app-schedule.png)

1. Ora puoi iniziare a progettare i contenuti con **[!UICONTROL Edit content]** pulsante .

   ![](assets/in_app_create_4.png)

## Inviare messaggi in-app{#in-app-send}

### Anteprima sul dispositivo {#preview-device}

Puoi visualizzare in anteprima la notifica in-app in un dispositivo specifico.

1. Fai clic su **[!UICONTROL Preview on device]**.

   ![](assets/in_app_create_6.png)

1. Da **[!UICONTROL Connect to device]** finestra, fai clic su **[!UICONTROL Start]**.

1. Digita nel **[!UICONTROL Base URL]** dell&#39;applicazione e fai clic su **[!UICONTROL Next]**.

   ![](assets/in_app_create_7.png)

1. Analizza il codice QR con il tuo dispositivo e inserisci il codice PIN visualizzato.

Il messaggio in-app può ora essere attivato direttamente sul dispositivo, consentendoti di visualizzare in anteprima e rivedere il messaggio su un dispositivo effettivo.

### Rivedi e attiva la notifica in-app{#in-app-review}

Una volta creato il messaggio in-app e il relativo contenuto definito e personalizzato, puoi rivederlo e attivarlo.

Per eseguire questa operazione, effettua le seguenti operazioni:

1. Utilizza la **[!UICONTROL Review to activate]** per visualizzare un riepilogo del messaggio.

   Il riepilogo consente di modificare la campagna se necessario e di verificare se è presente un parametro errato o mancante.

   ![](assets/in_app_create_5.png)

1. Verifica che la campagna sia configurata correttamente, quindi fai clic su **[!UICONTROL Activate]**.

La campagna è ora attivata. La notifica in-app configurata nella campagna viene inviata immediatamente o alla data specificata.

Dopo l’invio, puoi misurare l’impatto dei messaggi in-app nel rapporto Campaign. Per ulteriori informazioni sul reporting, consulta [questa sezione](inapp-report.md).

**Argomenti correlati:**

* [Progettare un messaggio in-app](design-in-app.md)
* [Rapporto in-app](inapp-report.md)
* [Configurazione in-app](inapp-configuration.md)
