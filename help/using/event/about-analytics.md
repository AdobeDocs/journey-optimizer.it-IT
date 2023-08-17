---
solution: Journey Optimizer
product: journey optimizer
title: Integrazione di Adobe Analytics
description: Scopri come sfruttare i dati di Adobe Analytics in Journey Optimizer
feature: Events
topic: Administration
role: Admin
level: Intermediate
keywords: analytics, integrazione, web sdk, platform
exl-id: 9d842722-e5eb-4743-849d-b7ba9448062f
source-git-commit: 16752d94647b25b4a86c34b77bda0f72fcfaf169
workflow-type: tm+mt
source-wordcount: '768'
ht-degree: 7%

---

# Utilizzare i dati di Adobe Analytics {#analytics-data}

Puoi sfruttare tutti i dati dell’evento comportamentale web che già acquisisci tramite Adobe Analytics o Web SDK e lo streaming in Adobe Experience Platform, per attivare i percorsi e automatizzare le esperienze per i clienti.

Affinché questo funzioni con Adobe Analytics, devi:

1. Attiva la suite di rapporti che desideri utilizzare. [Ulteriori informazioni](#leverage-analytics-data)
1. Abilita Journey Optimizer per utilizzare la tua origine dati Adobe Analytics. [Ulteriori informazioni](#activate-analytics-data)
1. Aggiungi un evento specifico nel percorso. [Ulteriori informazioni](#event-analytic)

>[!NOTE]
>
>Questa sezione si applica solo per gli eventi basati su regole e i clienti che devono utilizzare dati Adobe Analytics o Web SDK.
> 
>Se utilizzi Adobe Customer Journey Analytics, consulta [questa pagina](../reports/cja-ajo.md).
>

## Configurare i dati di Adobe Analytics o Web SDK {#leverage-analytics-data}

Per poter essere utilizzati nei percorsi, i dati provenienti da Adobe Analytics o Adobe Experience Platform Web SDK devono essere abilitati.

Per farlo, segui la procedura indicata di seguito:

1. Accedi a **[!UICONTROL Sorgenti]** menu.

1. Nella sezione Adobe Analytics, seleziona **[!UICONTROL Aggiungi dati]**

   ![](assets/ajo-aa_1.png)

1. Dall’elenco delle suite di rapporti di Adobe Analytics disponibili, seleziona la **[!UICONTROL Suite di rapporti]** per attivare. Quindi, fai clic su **[!UICONTROL Successivo]**.

   ![](assets/ajo-aa_2.png)

1. Scegli se desideri utilizzare uno schema predefinito o personalizzato.

1. Dalla sezione **[!UICONTROL Dettagli del flusso di dati]** schermata, scegli una **[!UICONTROL Nome flusso di dati]**.

1. Una volta completata la configurazione, fai clic su **[!UICONTROL Fine]**.

   ![](assets/ajo-aa_3.png)

In questo modo viene attivato il connettore di origine di Analytics per quella suite di rapporti. Ogni volta che i dati vengono inseriti, vengono trasformati in un evento Experience e inviati in Adobe Experience Platform.

![](assets/ajo-aa_4.png)

Ulteriori informazioni sul connettore di origine di Adobe Analytics in  [Documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html?lang=it){target="_blank"} and [tutorial](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html?lang=it){target="_blank"}.

## Attiva questa configurazione {#activate-analytics-data}

Al termine della configurazione, contatta un Adobe per abilitare l’ambiente Journey Optimizer all’utilizzo di questa origine dati. Questo passaggio è necessario solo per le origini dati di Adobe Analytics. Per eseguire questa operazione:

1. Ottieni l’ID dell’origine dati. Queste informazioni sono disponibili nell’interfaccia utente: passa all’origine dati creata da **Flussi dati** scheda di **Sorgenti** menu. Il modo più semplice per trovarlo è filtrare in base alle origini di Adobe Analytics.
1. Contatta l’Assistenza clienti Adobe con i seguenti dettagli:

   * Oggetto: Abilitare gli eventi Adobe Analytics per i percorsi

   * Contenuto: abilita il mio ambiente per utilizzare gli eventi AA.

      * ID organizzazione: &quot;XXX@AdobeOrg&quot;

      * ID sorgente dati: &quot;ID: xxxxx&quot;

1. Una volta confermata la preparazione dell’ambiente, puoi utilizzare i dati di Adobe Analytics nei tuoi percorsi.

## Creare un percorso con un evento utilizzando i dati di Adobe Analytics o Web SDK {#event-analytics}

Ora puoi creare un evento basato sui dati di Adobe Analytics o Adobe Experience Platform Web SDK da utilizzare in un percorso.

Nell’esempio seguente, scopri come eseguire il targeting degli utenti che hanno aggiunto un prodotto ai loro carrelli:

* Se l’ordine è completato, due giorni dopo gli utenti ricevono un’e-mail di follow-up per richiedere un feedback.
* Se l’ordine non è completato, gli utenti ricevono un’e-mail per ricordarsi di completarlo.

1. Da Adobe Journey Optimizer, accedi a **[!UICONTROL Configurazione]** menu.

1. Quindi, seleziona **[!UICONTROL Gestisci]** dal **[!UICONTROL Eventi]** Card.

   ![](assets/ajo-aa_5.png)

1. Clic **[!UICONTROL Crea evento]**. Il riquadro di configurazione dell’evento si apre sul lato destro dello schermo.

1. Compila il **[!UICONTROL Evento]** parametri:

   * **[!UICONTROL Nome]**: personalizza il nome della tua **[!UICONTROL Evento]**.
   * **[!UICONTROL Tipo]**: scegli il **[!UICONTROL Unitario]** Digita. [Ulteriori informazioni](../event/about-events.md)
   * **[!UICONTROL Tipo ID evento]**: scegli il **[!UICONTROL Basato su regole]** Tipo ID evento. [Ulteriori informazioni](../event/about-events.md#event-id-type)
   * **[!UICONTROL Schema]**: seleziona lo schema Analytics o Web SDK [creato prima di](#leverage-analytics-data).
   * **[!UICONTROL Campi]**: seleziona i campi Payload. [Ulteriori informazioni](../event/about-creating.md#define-the-payload-fields)
   * **[!UICONTROL Condizione ID evento]**: definisci la condizione per identificare gli eventi che attiveranno il percorso.

     In questo caso, l’evento viene attivato quando i clienti aggiungono un articolo ai loro carrelli.
   * **[!UICONTROL Identificatore profilo]**: scegli un campo dai campi del payload, o definisci una formula, per identificare la persona associata all’evento.

   ![](assets/ajo-aa_6.png)

1. Una volta configurata, seleziona **[!UICONTROL Salva]**.

Ora che l’evento è pronto, crea un percorso per utilizzarlo.

1. Dalla sezione **[!UICONTROL Percorsi]** aprire o creare un percorso. Per ulteriori informazioni al riguardo, consulta [questa sezione](../building-journeys/journey-gs.md).

1. Aggiungi al percorso l’evento Analytics configurato in precedenza.

   ![](assets/ajo-aa_8.png)

1. Aggiungi un evento che verrà attivato se un ordine è completato.

1. Dal tuo **[!UICONTROL Menu Evento]**, seleziona la **[!UICONTROL Definire il timeout dell’evento]** e **[!UICONTROL Impostare un percorso di timeout]** opzioni.

   ![](assets/ajo-aa_9.png)

1. Dal percorso di timeout, aggiungi un **[!UICONTROL E-mail]** azione. Questo percorso verrà utilizzato per inviare un’e-mail ai clienti che non hanno completato un ordine per ricordare loro che i loro carrelli sono ancora disponibili.

1. Aggiungi un **[!UICONTROL Wait]** dopo il percorso principale e impostarlo sulla durata desiderata.

   ![](assets/ajo-aa_10.png)

1. Quindi, aggiungi un **[!UICONTROL Azione e-mail]**. In questa e-mail, ai clienti verrà richiesto di fornire feedback sull’ordine effettuato.

Ora puoi testare e pubblicare il percorso. [Ulteriori informazioni](../building-journeys/publishing-the-journey.md)

![](assets/ajo-aa_7.png)
