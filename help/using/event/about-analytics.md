---
solution: Journey Optimizer
product: journey optimizer
title: Integrazione di Adobe Analytics
description: Scopri come sfruttare i dati di Adobe Analytics in Journey Optimizer
feature: Journeys, Events, Reporting, Integrations
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate, Experienced
keywords: analisi, integrazione, web sdk, piattaforma
exl-id: 9d842722-e5eb-4743-849d-b7ba9448062f
source-git-commit: 0be35e14dba32523a7f28aaaa28d41ee693d44ba
workflow-type: tm+mt
source-wordcount: '755'
ht-degree: 5%

---

# Utilizzare i dati di Adobe Analytics {#analytics-data}

Puoi sfruttare tutti i dati dell’evento comportamentale web che già acquisisci tramite Adobe Analytics o Web SDK e inviare in streaming a Adobe Experience Platform, per attivare percorsi e automatizzare le esperienze per i clienti.

Affinché questo funzioni con Adobe Analytics, devi:

1. Attiva la suite di rapporti che desideri utilizzare. [Ulteriori informazioni](#leverage-analytics-data)
1. Abilita Journey Optimizer per utilizzare la tua origine dati Adobe Analytics. [Ulteriori informazioni](#activate-analytics-data)
1. Aggiungi un evento specifico al tuo percorso. [Ulteriori informazioni](#event-analytic)

>[!NOTE]
>
>Questa sezione si applica solo agli eventi basati su regola e ai clienti che devono utilizzare dati Adobe Analytics o Web SDK.
> 
>Se utilizzi Customer Journey Analytics Adobe Systems, consulta [questa pagina](../reports/cja-ajo.md).
>

## Configurare dati Adobe Analytics o Web SDK {#leverage-analytics-data}

I dati provenienti da Adobe Analytics o Adobe Experience Platform Web SDK devono essere abilitati per essere utilizzati nei tuoi percorsi.

Per farlo, segui la procedura indicata di seguito:

1. Sfoglia al **[!UICONTROL menu Sorgenti]** .

1. Nella sezione Adobe Analytics selezionare **[!UICONTROL Aggiungi dati]**

   ![](assets/ajo-aa_1.png)

1. Dall&#39;elenco delle suite di rapporti Adobe Analytics disponibili, seleziona la suite ]**di**[!UICONTROL  rapporti da abilitare. Quindi fare clic su **[!UICONTROL Successivo]**.

   ![](assets/ajo-aa_2.png)

1. Scegli se desideri utilizzare uno schema predefinito o personalizzato.

1. Dalla schermata **[!UICONTROL Dettagli flusso di dati]**, scegli un **[!UICONTROL Nome flusso di dati]**.

1. Una volta completata la configurazione, fai clic su **[!UICONTROL Fine]**.

   ![](assets/ajo-aa_3.png)

In questo modo viene abilitato il connettore di origine Analytics per quella suite di rapporti. Ogni volta che i dati arrivano, vengono trasformati in un evento Esperienza e inviati in Adobe Experience Platform.

![](assets/ajo-aa_4.png)

Scopri ulteriori informazioni su Adobe Analytics connettore di origine in Adobe Experience Platform  [documentazione](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html){target="_blank"} e [esercitazione](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html){target="_blank"}.

## Attiva questa configurazione {#activate-analytics-data}

Al termine della configurazione, contatta Adobe per abilitare l’ambiente Journey Optimizer all’utilizzo di questa origine dati. Questo passaggio è necessario solo per le origini dati di Adobe Analytics. Per eseguire questa operazione:

1. Ottieni l’ID dell’origine dati. Queste informazioni sono disponibili nell&#39;interfaccia utente: passare all&#39;origine dati creata dalla scheda **Flussi dati** del menu **Origini**. Il modo più semplice per trovarlo è filtrare in base alle origini di Adobe Analytics.
1. Contatta l’Assistenza clienti Adobe con i seguenti dettagli:

   * Oggetto: Attivazione di eventi Adobe Analytics per i viaggi

   * Contenuto: abilitate il mio ambiente per l&#39;utilizzo degli eventi AA.

      * ID organizzazione: &quot;XXX@AdobeOrg&quot;

      * ID origine dati: &quot;ID: xxxxx&quot;

1. Una volta che hai una conferma che il tuo ambiente è pronto, puoi utilizzare Adobe Analytics dati nei tuoi percorsi.

## Crea un percorso con un evento utilizzando dati Adobe Analytics o Web SDK {#event-analytics}

Ora puoi creare un evento basato su dati Adobe Analytics o Adobe Experience Platform Web SDK da utilizzare in un percorso.

Nell&#39;esempio riportato di seguito, scopri come destinazione utenti che hanno aggiunto un prodotto al carrello:

* Se l&#39;ordine viene completato, gli utenti ricevono un&#39;e-mail seguire-up due giorni dopo per chiedere feedback.
* Se l&#39;ordine non viene completato, gli utenti ricevono un&#39;e-mail per ricordare loro di completare l&#39;ordine.

1. Da Adobe Systems Journey Optimizer accesso il **[!UICONTROL menu Configurazione]** .

1. Quindi, seleziona **[!UICONTROL Gestisci]** dalla scheda **[!UICONTROL Eventi]**.

   ![](assets/ajo-aa_5.png)

1. Fai clic su **[!UICONTROL Crea]** evento. Il riquadro di configurazione dell’evento si apre sul lato destro dello schermo.

1. Compila i parametri dell&#39;evento ****:

   * **[!UICONTROL Nome]**: personalizza il nome del tuo **[!UICONTROL evento]**.
   * **[!UICONTROL Tipo]**: scegliere il **[!UICONTROL tipo unitario]** . [Ulteriori informazioni](../event/about-events.md)
   * **[!UICONTROL Tipo di]** ID evento: scegli il tipo di ID evento basato su **** regola. [Ulteriori informazioni](../event/about-events.md#event-id-type)
   * **[!UICONTROL Schema]**: seleziona lo schema [Analytics o WebSDK creato in precedenza](#leverage-analytics-data).
   * **[!UICONTROL Campi]**: selezionare i campi payload. [Ulteriori informazioni](../event/about-creating.md#define-the-payload-fields)
   * **[!UICONTROL Condizione]** ID evento: definisci la condizione per identificare gli eventi che attiveranno il tuo viaggio.

     Qui, l&#39;evento viene attivato quando i clienti aggiungono un articolo al carrello.
   * **[!UICONTROL Identificatore]** profilo: scegli un campo dai campi payload o definisci una formula per identificare la persona associata all&#39;evento.

   ![](assets/ajo-aa_6.png)

1. Una volta configurato selezionare **[!UICONTROL Salva]**.

Ora che l&#39;evento è pronto, crea un percorso per utilizzarlo.

1. **[!UICONTROL Dal menu Percorsi]**, apri o crea un percorso. Per ulteriori informazioni al riguardo, consulta [questa sezione](../building-journeys/journey-gs.md).

1. Aggiungi al percorso l’evento Analytics configurato in precedenza.

   ![](assets/ajo-aa_8.png)

1. Aggiungi un evento che verrà attivato se un ordine è completato.

1. Dal **[!UICONTROL menu Evento]**, seleziona le opzioni **[!UICONTROL Definisci timeout evento]** e **[!UICONTROL Imposta un percorso di timeout]**.

   ![](assets/ajo-aa_9.png)

1. Aggiungi un&#39;azione **[!UICONTROL E-mail]** dal percorso di timeout. Questo percorso verrà utilizzato per inviare un&#39;e-mail ai clienti che non hanno completato un ordine per ricordare loro che i loro carrelli sono ancora disponibili.

1. Aggiungi un&#39;attività **[!UICONTROL di attesa]** dopo il percorso principale e impostala sulla durata necessaria.

   ![](assets/ajo-aa_10.png)

1. Quindi, aggiungi **[!UICONTROL Azione e-mail]**. In questa e-mail, ai clienti verrà richiesto di fornire feedback sull’ordine effettuato.

Ora puoi testare e pubblicare il percorso. [Ulteriori informazioni](../building-journeys/publishing-the-journey.md)

![](assets/ajo-aa_7.png)
