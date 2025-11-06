---
title: Configurare il canale Web in-app
description: Scopri come configurare il canale Web in-app nella raccolta dati
feature: In App
topic: Content Management
role: User
level: Beginner
keywords: in-app, messaggio, creazione, inizio
exl-id: 5a67177e-a7cf-41a8-9e7d-37f7fe3d34dc
source-git-commit: efb943e5a6f27becc6e8b6128b776e46d6141823
workflow-type: tm+mt
source-wordcount: '634'
ht-degree: 7%

---

# Creare un messaggio in-app per il web {#create-in-app-web}

## Configurare il canale Web in-app {#configure-web-inapp}

Per configurare il tuo canale Web in-app, segui i passaggi seguenti:

* Installa l’estensione tag Web SDK per supportare la messaggistica in-app web. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration.html?lang=it){target="_blank"}

* Personalizza i trigger. La messaggistica Web in-app supporta due tipi di trigger: Inviati dati alla piattaforma e Manuali. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/experience-platform/edge/personalization/ajo/web-in-app-messaging.html?lang=it){target="_blank"}

* Crea la configurazione Web in-app. [Ulteriori informazioni](inapp-configuration.md)

## Creare la campagna di messaggi in-app Web {#create-inapp-web-campaign}

1. Accedi al menu **[!UICONTROL Campagne]**, quindi fai clic su **[!UICONTROL Crea campagna]**.

1. Scegli il tipo di esecuzione della campagna: Pianificato o Attivato da API. Ulteriori informazioni sui tipi di campagna in [questa pagina](../campaigns/create-campaign.md#campaigntype).

1. Dal menu a discesa **[!UICONTROL Azioni]**, scegli il **[!UICONTROL messaggio in-app]**.

   ![](assets/in_app_web_surface_1.png)

1. Scegli o crea la configurazione dell&#39;app. [Ulteriori informazioni](inapp-configuration.md#channel-prerequisites)

## Definire la campagna di messaggi in-app web {#configure-inapp}

1. Dalla sezione **[!UICONTROL Proprietà]**, immetti il **[!UICONTROL Titolo]** e la descrizione **[!UICONTROL Descrizione]**.

1. Per assegnare etichette di utilizzo dei dati personalizzate o di base al messaggio in-app, seleziona **[!UICONTROL Gestisci accesso]**. [Ulteriori informazioni](../administration/object-based-access.md).

1. Fai clic sul pulsante **[!UICONTROL Seleziona pubblico]** per definire il pubblico di destinazione dall&#39;elenco dei tipi di pubblico di Adobe Experience Platform disponibili. [Ulteriori informazioni](../audience/about-audiences.md).

   ![](assets/in_app_web_surface_5.png)

1. Nel campo **[!UICONTROL Spazio dei nomi identità]**, scegli lo spazio dei nomi da utilizzare per identificare i singoli utenti del pubblico selezionato. [Ulteriori informazioni](../event/about-creating.md#select-the-namespace).

1. Nel menu **[!UICONTROL Azione]**, puoi trovare le impostazioni configurate in precedenza come **[!UICONTROL Configurazione app]**. Se necessario, puoi apportare modifiche qui o aggiornare la regola facendo clic su **[!UICONTROL Modifica regola]**.

1. Fai clic su **[!UICONTROL Crea esperimento]** per iniziare a configurare l&#39;esperimento sui contenuti e creare trattamenti per misurarne le prestazioni e identificare l&#39;opzione migliore per il pubblico di destinazione. [Ulteriori informazioni](../content-management/content-experiment.md)

1. Fai clic su **[!UICONTROL Modifica trigger]** per scegliere gli eventi e i criteri che attiveranno il messaggio. I generatori di regole consentono agli utenti di specificare criteri e valori che, se soddisfatti, attivano un set di azioni, ad esempio l’invio di un messaggio in-app.

   1. Se necessario, fai clic sul menu a discesa evento per modificare il trigger.

      +++Consulta Triggers disponibili.

      | Pacchetto | Trigger | Definizione |
      |---|---|---|
      | Piattaforma | Dati inviati a Platform | Attivazione quando l’app mobile genera un evento di esperienza Edge per inviare dati a Adobe Experience Platform. Di solito la chiamata API [sendEvent](https://developer.adobe.com/client-sdks/documentation/edge-network/api-reference/#sendevent){target="_blank"} dall&#39;estensione AEP Edge. |
      | Manuale | Attivazione manuale | Due elementi dati associati: una chiave, che è una costante che definisce il set di dati (ad esempio, genere, colore, prezzo) e un valore, che è una variabile che appartiene al set (ad esempio, maschio/femmina, verde, 100). |

      +++

   1. Fare clic su **[!UICONTROL Aggiungi condizione]** se si desidera che il trigger consideri più eventi o criteri.

   1. Scegli la condizione **[!UICONTROL Or]** se desideri aggiungere altri **[!UICONTROL Triggers]** per espandere ulteriormente la regola.

      ![](assets/in_app_web_surface_8.png)

   1. Scegli la condizione **[!UICONTROL And]** se desideri aggiungere una **[!UICONTROL caratteristica]** personalizzata e perfezionare meglio la regola.

      +++Consulta Caratteristiche disponibili.

      | Pacchetto | Caratteristica | Definizione |
      |---|---|---|
      | Piattaforma | Tipo di evento XDM | Attivazione quando viene soddisfatto il tipo di evento specificato. |
      | Piattaforma | Valore XDM | Attivazione quando viene soddisfatto il valore XDM specificato. |

      +++

      ![](assets/in_app_web_surface_9.png)

   1. Fai clic su **[!UICONTROL Crea gruppo]** per raggruppare i trigger.

1. Scegli la frequenza del trigger quando il messaggio in-app è attivo. Sono disponibili le seguenti opzioni:

   * **[!UICONTROL Ogni volta]**: mostra sempre il messaggio quando si verificano gli eventi selezionati nel menu a discesa **[!UICONTROL Attivatore app mobile]**.
   * **[!UICONTROL Una volta]**: mostra questo messaggio solo la prima volta che si verificano gli eventi selezionati nel menu a discesa **[!UICONTROL Attivatore app mobile]**.
   * **[!UICONTROL Fino al click-through]**: visualizza questo messaggio quando gli eventi selezionati nel menu a discesa **[!UICONTROL Attivatore app mobile]** si verificano fino a quando un evento di interazione non viene inviato dal SDK con l&#39;azione &quot;cliccato&quot;.
   * **[!UICONTROL X volte]**: visualizza questo messaggio X volte.

1. Se necessario, scegli il **[!UICONTROL giorno della settimana]** o **[!UICONTROL ora del giorno]** in cui verrà visualizzato il messaggio in-app.

1. Le campagne sono progettate per essere eseguite in una data specifica o con una frequenza ricorrente. Scopri come configurare la **[!UICONTROL pianificazione]** della campagna in [questa sezione](../campaigns/create-campaign.md#schedule).

   ![](assets/in_app_web_surface_6.png)

1. Ora puoi iniziare a progettare il contenuto con il pulsante **[!UICONTROL Modifica contenuto]**. [Ulteriori informazioni](design-in-app.md)

   ![](assets/in_app_web_surface_7.png)

**Argomenti correlati:**

* [Testare e inviare il messaggio in-app](send-in-app.md)
* [Rapporto in-app](../reports/campaign-global-report-cja-inapp.md)
* [Configurazione in-app](inapp-configuration.md)
