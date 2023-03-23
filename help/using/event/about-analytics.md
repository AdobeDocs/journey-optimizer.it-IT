---
solution: Journey Optimizer
product: journey optimizer
title: Integrazione di Adobe Analytics
description: Scopri come sfruttare i dati di Adobe Analytics in Journey Optimizer
feature: Events
topic: Administration
role: Admin
level: Intermediate
keywords: analytics, integrazione, sdk web, piattaforma
exl-id: 9d842722-e5eb-4743-849d-b7ba9448062f
source-git-commit: 16752d94647b25b4a86c34b77bda0f72fcfaf169
workflow-type: tm+mt
source-wordcount: '768'
ht-degree: 7%

---

# Utilizzare i dati di Adobe Analytics {#analytics-data}

Puoi sfruttare tutti i dati dell’evento comportamentale web già acquisiti tramite Adobe Analytics o SDK per web e lo streaming in Adobe Experience Platform, al fine di attivare percorsi e automatizzare le esperienze per i tuoi clienti.

Affinché questo funzioni con Adobe Analytics, devi:

1. Attiva la suite di rapporti che desideri utilizzare. [Ulteriori informazioni](#leverage-analytics-data)
1. Abilita Journey Optimizer all’utilizzo della tua origine dati Adobe Analytics. [Ulteriori informazioni](#activate-analytics-data)
1. Aggiungi un evento specifico nel percorso. [Ulteriori informazioni](#event-analytic)

>[!NOTE]
>
>Questa sezione si applica solo agli eventi basati su regole e ai clienti che devono utilizzare i dati Adobe Analytics o SDK web.
> 
>Se utilizzi Adobe Customer Journey Analytics, consulta [questa pagina](../reports/cja-ajo.md).

## Configurare i dati Adobe Analytics o SDK per web {#leverage-analytics-data}

Per poter essere utilizzati nei tuoi percorsi, devi abilitare i dati provenienti da Adobe Analytics o Adobe Experience Platform Web SDK.

Per farlo, segui la procedura indicata di seguito:

1. Sfoglia il **[!UICONTROL Origini]** menu.

1. Nella sezione Adobe Analytics, seleziona **[!UICONTROL Aggiungi dati]**

   ![](assets/ajo-aa_1.png)

1. Dall’elenco delle suite di rapporti Adobe Analytics disponibili, seleziona la **[!UICONTROL Suite di rapporti]** per abilitare. Quindi, fai clic su **[!UICONTROL Successivo]**.

   ![](assets/ajo-aa_2.png)

1. Scegliere se si desidera utilizzare uno schema predefinito o personalizzato.

1. Da **[!UICONTROL Dettaglio flusso di dati]** schermata, scegli una **[!UICONTROL Nome flusso di dati]**.

1. Al termine della configurazione, fai clic su **[!UICONTROL Fine]**.

   ![](assets/ajo-aa_3.png)

Questo abilita il connettore di origine Analytics per la suite di rapporti. Ogni volta che i dati entrano, vengono trasformati in un evento Experience e inviati ad Adobe Experience Platform.

![](assets/ajo-aa_4.png)

Ulteriori informazioni sul connettore sorgente Adobe Analytics in  [Documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html?lang=it){target="_blank"} and [tutorial](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html?lang=it){target="_blank"}.

## Attiva questa configurazione {#activate-analytics-data}

Al termine della configurazione, contatta l’Adobe per abilitare l’utilizzo di questa origine dati nell’ambiente Journey Optimizer. Questo passaggio è necessario solo per le origini dati Adobe Analytics. Per eseguire questa operazione:

1. Ottieni l&#39;ID dell&#39;origine dati. Queste informazioni sono disponibili nell’interfaccia utente di : individuare l&#39;origine dati creata dalla **Flussi di dati** della scheda **Origini** menu. Il modo più semplice per trovarlo è filtrare sulle sorgenti Adobe Analytics.
1. Contatta l’Assistenza clienti di Adobe con i seguenti dettagli:

   * Oggetto: Abilita eventi Adobe Analytics per percorsi

   * Contenuto: Abilita il mio ambiente per l’utilizzo di eventi AA.

      * ID organizzazione: &quot;XXX@AdobeOrg&quot;

      * ID origine dati: &quot;ID: xxxxx&quot;

1. Una volta ottenuta la conferma che l’ambiente è pronto, puoi utilizzare i dati di Adobe Analytics nei tuoi percorsi.

## Creare un percorso con un evento utilizzando i dati SDK per Adobe Analytics o Web {#event-analytics}

È ora possibile creare un evento basato sui dati dell’SDK Web di Adobe Analytics o Adobe Experience Platform da utilizzare in un percorso.

Nell’esempio seguente, scopri come eseguire il targeting degli utenti che hanno aggiunto un prodotto ai loro carrelli:

* Se l’ordine è completato, gli utenti ricevono un’e-mail di follow-up due giorni dopo per richiedere feedback.
* Se l’ordine non è completato, gli utenti ricevono un messaggio e-mail per ricordare loro di completare l’ordine.

1. Da Adobe Journey Optimizer, accedi al **[!UICONTROL Configurazione]** menu.

1. Quindi, seleziona **[!UICONTROL Gestisci]** dal **[!UICONTROL Eventi]** il Card.

   ![](assets/ajo-aa_5.png)

1. Fai clic su **[!UICONTROL Crea evento]**. Il riquadro di configurazione dell’evento si apre sul lato destro dello schermo.

1. Compila il **[!UICONTROL Evento]** parametri:

   * **[!UICONTROL Nome]**: Personalizza il nome della tua **[!UICONTROL Evento]**.
   * **[!UICONTROL Tipo]**: Scegli la **[!UICONTROL Unitario]** Digitare. [Ulteriori informazioni](../event/about-events.md)
   * **[!UICONTROL Tipo ID evento]**: Scegli la **[!UICONTROL Basato su regole]** Tipo ID evento. [Ulteriori informazioni](../event/about-events.md#event-id-type)
   * **[!UICONTROL Schema]**: Selezionare lo schema Analytics o WebSDK [creato prima](#leverage-analytics-data).
   * **[!UICONTROL Campi]**: Selezionare i campi Payload. [Ulteriori informazioni](../event/about-creating.md#define-the-payload-fields)
   * **[!UICONTROL Condizione ID evento]**: Definisci la condizione per identificare gli eventi che attiveranno il percorso.

      In questo caso, l’evento viene attivato quando i clienti aggiungono un elemento ai carrelli.
   * **[!UICONTROL Identificatore profilo]**: Scegli un campo dai campi del payload o definisci una formula per identificare la persona associata all’evento.

   ![](assets/ajo-aa_6.png)

1. Una volta configurato, seleziona **[!UICONTROL Salva]**.

Ora che l’evento è pronto, crea un percorso per utilizzarlo.

1. Da **[!UICONTROL Percorsi]** aprire o creare un percorso. Per ulteriori informazioni al riguardo, consulta [questa sezione](../building-journeys/journey-gs.md).

1. Aggiungi l’evento Analytics configurato in precedenza al percorso.

   ![](assets/ajo-aa_8.png)

1. Aggiungi un evento che verrà attivato se un ordine viene completato.

1. Dal tuo **[!UICONTROL Menu Evento]**, seleziona **[!UICONTROL Definire il timeout dell’evento]** e **[!UICONTROL Imposta un percorso di timeout]** opzioni.

   ![](assets/ajo-aa_9.png)

1. Dal percorso di timeout, aggiungi un **[!UICONTROL E-mail]** azione. Questo percorso verrà utilizzato per inviare un’e-mail ai clienti che non hanno completato un ordine per ricordare loro che i loro carrelli sono ancora disponibili.

1. Aggiungi un **[!UICONTROL Wait]** dopo il percorso principale e impostalo sulla durata necessaria.

   ![](assets/ajo-aa_10.png)

1. Quindi, aggiungi un **[!UICONTROL Azione e-mail]**. In questa e-mail, ai clienti verrà richiesto di fornire feedback sull’ordine inserito.

Ora puoi testare e pubblicare il tuo percorso. [Ulteriori informazioni](../building-journeys/publishing-the-journey.md)

![](assets/ajo-aa_7.png)
