---
solution: Journey Optimizer
product: journey optimizer
title: Integrazione di Adobe Analytics
description: Scopri come sfruttare i dati di Adobe Analytics
feature: Events
topic: Administration
role: Admin
level: Intermediate
keywords: analytics, integrazione, sdk web, piattaforma
exl-id: 9d842722-e5eb-4743-849d-b7ba9448062f
source-git-commit: c0afa3e2bc6dbcb0f2f2357eebc04285de8c5773
workflow-type: tm+mt
source-wordcount: '618'
ht-degree: 10%

---

# Integrazione di Adobe Analytics {#analytics-data}

## Utilizzo dei dati dell’SDK per web o Adobe Analytics {#leverage-analytics-data}

Puoi sfruttare tutti i dati dell’evento comportamentale web (tramite Adobe Analytics o SDK per web) già acquisiti e in streaming in Adobe Experience Platform per attivare percorsi e automatizzare le esperienze per i tuoi clienti.

>[!NOTE]
>
>Questa sezione si applica solo agli eventi basati su regole e ai clienti che devono utilizzare dati Adobe Analytics o WebSDK.

Affinché questo funzioni con Adobe Analytics, devi attivare in Adobe Experience Platform la suite di rapporti che desideri utilizzare. Per farlo, segui la procedura indicata di seguito:

1. Collegati a Adobe Experience Platform e cerca **[!UICONTROL Origini]**.

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

## Creare un percorso con un evento utilizzando i dati SDK per Adobe Analytics o Web {#event-analytics}

Dopo aver implementato l’integrazione con Adobe Analytics con [Origini Adobe Analytics](#leverage-analytics-data) o con [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=it), puoi creare un evento che può essere successivamente utilizzato in un percorso.

In questo esempio, per gli utenti che hanno aggiunto un prodotto ai carrelli verranno utilizzati:

* Se l’ordine è completato, riceveranno un’e-mail di follow-up due giorni dopo per richiedere feedback.
* Se l’ordine non è stato completato, riceverà un’e-mail per ricordargli di completare l’ordine.

1. Da Adobe Journey Optimizer, accedi al **[!UICONTROL Configurazione]** menu.

1. Quindi, seleziona **[!UICONTROL Gestisci]** dal **[!UICONTROL Eventi]** il Card.

   ![](assets/ajo-aa_5.png)

1. Fai clic su **[!UICONTROL Crea evento]**. Il riquadro di configurazione dell’evento si apre sul lato destro dello schermo.

1. Compila il **[!UICONTROL Evento]** parametri:

   * **[!UICONTROL Nome]**: Personalizza il nome della tua **[!UICONTROL Evento]**.
   * **[!UICONTROL Tipo]**: Scegli la **[!UICONTROL Unitario]** Digitare. [Ulteriori informazioni](../event/about-events.md)
   * **[!UICONTROL Tipo ID evento]**: Scegli la **[!UICONTROL Basato su regole]** Tipo ID evento. [Ulteriori informazioni](../event/about-events.md#event-id-type)
   * **[!UICONTROL Schema]**: Seleziona lo schema Analytics o WebSDK creato nella sezione precedente.
   * **[!UICONTROL Campi]**: Selezionare i campi Payload. [Ulteriori informazioni](../event/about-creating.md#define-the-payload-fields)
   * **[!UICONTROL Condizione ID evento]**: Definisci la condizione che verrà utilizzata dal sistema per identificare gli eventi che attiveranno il percorso.

      In questo caso, l’evento viene attivato quando i clienti aggiungono un elemento ai carrelli.
   * **[!UICONTROL Identificatore profilo]**: Scegli un campo dai campi del payload o definisci una formula per identificare la persona associata all’evento.

   ![](assets/ajo-aa_6.png)

1. Una volta configurato, seleziona **[!UICONTROL Salva]**. L’evento è ora pronto per essere utilizzato in un percorso.

1. Da **[!UICONTROL Percorsi]**, ora puoi iniziare a creare il percorso. Per ulteriori informazioni al riguardo, consulta [questa sezione](../building-journeys/journey-gs.md).

1. Aggiungi al percorso gli eventi di Analytics configurati in precedenza.

   ![](assets/ajo-aa_8.png)

1. Aggiungi un evento che verrà attivato se un ordine viene completato.

1. Dal tuo **[!UICONTROL Menu Evento]**, seleziona **[!UICONTROL Definire il timeout dell’evento]** e **[!UICONTROL Imposta un percorso di timeout]** opzioni.

   ![](assets/ajo-aa_9.png)

1. Dal percorso di timeout, aggiungi un **[!UICONTROL E-mail]** azione. Questo percorso verrà utilizzato per inviare un’e-mail ai clienti che non hanno completato un ordine per ricordare loro che i loro carrelli sono ancora disponibili.

1. Aggiungi un **[!UICONTROL Wait]** dopo il percorso principale e impostalo sulla durata necessaria.

   ![](assets/ajo-aa_10.png)

1. Quindi, aggiungi un **[!UICONTROL Azione e-mail]**. In questa e-mail, ai clienti verrà richiesto di fornire feedback sull’ordine inserito.

Ora puoi pubblicare il percorso dopo averne verificato la validità. [Ulteriori informazioni](../building-journeys/publishing-the-journey.md)

![](assets/ajo-aa_7.png)
