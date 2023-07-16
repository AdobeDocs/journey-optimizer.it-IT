---
solution: Journey Optimizer
product: journey optimizer
title: Azioni di Adobe Campaign Standard
description: Scopri le azioni di Adobe Campaign Standard
feature: Actions
topic: Administration
role: Admin
level: Intermediate
keywords: percorso, integrazione, standard, campagna, ACS
exl-id: 50565cd9-7415-4c6a-9651-24fefeded3f5
source-git-commit: 417eea2a52d4fb38ae96cf74f90658f87694be5a
workflow-type: tm+mt
source-wordcount: '933'
ht-degree: 4%

---

# Azioni di Adobe Campaign Standard {#using_campaign_action}

Se disponi di Adobe Campaign Standard, sono disponibili le seguenti attività di azione integrate: **[!UICONTROL E-mail]**, **[!UICONTROL Push]** e **[!UICONTROL SMS]**.

>[!NOTE]
>
>A questo scopo, devi configurare l’azione incorporata. Consulta [questa pagina](../action/acs-action.md).

Per ciascuno di questi canali, seleziona una funzione di messaggistica transazionale di Adobe Campaign Standard **modello**. Per i canali e-mail, SMS e push incorporati, ci affidiamo alla messaggistica transazionale per eseguire l’invio dei messaggi. Ciò significa che se desideri utilizzare un determinato modello di messaggio nei tuoi percorsi, devi pubblicarlo in Adobe Campaign Standard. Fai riferimento a [questa pagina](https://experienceleague.adobe.com/docs/campaign-standard/using/communication-channels/transactional-messaging/getting-started-with-transactional-msg.html?lang=it) per scoprire come utilizzare questa funzione.

>[!NOTE]
>
>Per poter essere utilizzato in Journey Optimizer, il messaggio transazionale di Campaign Standard e il relativo evento associato devono essere pubblicati. Se l’evento viene pubblicato ma il messaggio non lo è, non sarà visibile nell’interfaccia di Journey Optimizer. Se il messaggio viene pubblicato ma il relativo evento associato non lo è, sarà visibile nell’interfaccia di Journey Optimizer ma non sarà utilizzabile.

![](assets/journey59.png)

Puoi utilizzare un evento (noto anche come modello di messaggistica transazionale di profilo in tempo reale).

>[!NOTE]
>
>Quando inviamo messaggi transazionali in tempo reale (rtEvent) o quando inviamo messaggi con un sistema di terze parti grazie a un’azione personalizzata, è necessaria una configurazione specifica per la gestione dell’affaticamento, dell’elenco Bloccati o dell’annullamento dell’abbonamento. Ad esempio, se un attributo &quot;unsubscribe&quot; è memorizzato in Adobe Experience Platform o in un sistema di terze parti, sarà necessario aggiungere una condizione prima dell’invio del messaggio per verificare questa condizione.

Quando selezioni un modello, tutti i campi previsti nel payload del messaggio vengono visualizzati nel riquadro di configurazione dell’attività in **[!UICONTROL Indirizzo]** e **[!UICONTROL Dati di personalizzazione]**. Devi mappare ciascuno di questi campi con il campo che desideri utilizzare, dall’evento o dall’origine dati. È inoltre possibile utilizzare l’editor di espressioni avanzate per passare manualmente un valore, manipolare i dati sulle informazioni recuperate (ad esempio, convertire una stringa in maiuscolo) o utilizzare funzioni quali &quot;if, then, else&quot;. Consulta [questa pagina](expression/expressionadvanced.md).

![](assets/journey60.png)

## E-mail e SMS {#section_asc_51g_nhb}

Per **[!UICONTROL E-mail]** e **[!UICONTROL SMS]**, i parametri sono identici.

>[!NOTE]
>
>Quando si utilizza il modello transazionale di un profilo per le e-mail, il meccanismo di annullamento dell’abbonamento viene gestito automaticamente da Adobe Campaign Standard. Per implementare questa, puoi includere facilmente un’ **[!UICONTROL Collegamento per annullare l’iscrizione]** blocco di contenuto all’interno di [il modello e-mail transazionale](https://experienceleague.adobe.com/docs/campaign-standard/using/communication-channels/transactional-messaging/getting-started-with-transactional-msg.html?lang=it). Tuttavia, se utilizzi un modello basato su eventi (rtEvent), devi incorporare nel messaggio un collegamento che trasmetta l’e-mail del destinatario come parametro URL e li indirizzi a una pagina di destinazione per l’annullamento dell’abbonamento. È necessario creare questa pagina di destinazione e garantire che la decisione del destinatario di annullare l’abbonamento sia effettivamente trasmessa ad Adobe.

Innanzitutto, devi scegliere un modello di messaggistica transazionale.

Sono disponibili due categorie: **[!UICONTROL Indirizzo]** e **[!UICONTROL Dati di personalizzazione]**.

È possibile definire facilmente dove recuperare **[!UICONTROL Indirizzo]** o **[!UICONTROL Dati di personalizzazione]** tramite l’interfaccia di. Puoi sfogliare gli eventi e i campi dell’origine dati disponibili. È inoltre possibile utilizzare l’editor di espressioni avanzate per casi di utilizzo più avanzati, ad esempio per utilizzare un’origine dati che richiede il passaggio di parametri o l’esecuzione di manipolazioni. Consulta [questa pagina](expression/expressionadvanced.md).

**[!UICONTROL Indirizzo]**

>[!NOTE]
>
>Questa categoria è visibile solo se selezioni un messaggio transazionale &quot;evento&quot;. Per i messaggi di &quot;profilo&quot;, la **[!UICONTROL Indirizzo]** viene recuperato automaticamente da Adobe Campaign Standard.

Questi sono i campi necessari per sapere dove inviare il messaggio. Per un modello e-mail, si tratta dell’indirizzo e-mail. Per un SMS, è il numero del cellulare.

![](assets/journey61.png)

**[!UICONTROL Dati di personalizzazione]**

>[!NOTE]
>
>Non è possibile trasmettere una raccolta nei dati di personalizzazione. Se l’e-mail o l’SMS transazionale prevede delle raccolte, non funzioneranno. Inoltre, i dati di personalizzazione hanno un formato previsto (ad esempio, stringa, decimale e così via). Devi fare attenzione a rispettare questi formati previsti.

Questi sono i campi previsti dal messaggio di Adobe Campaign Standard. Questi campi possono essere utilizzati per personalizzare il messaggio, applicare la formattazione condizionale o scegliere una variante di messaggio specifica.

![](assets/journey62.png)

## Push {#section_im3_hvf_nhb}

Prima di utilizzare l’attività push, è necessario configurare l’app mobile e Campaign Standard per inviare le notifiche push. Usa questo [articolo](https://helpx.adobe.com/it/campaign/kb/integrate-mobile-sdk.html) per adottare le misure di implementazione necessarie per mobile.

Innanzitutto, devi scegliere un’app mobile dall’elenco a discesa e un messaggio transazionale.

![](assets/journey62bis.png)

Sono disponibili due categorie: **[!UICONTROL Target]** e **[!UICONTROL Dati di personalizzazione]**.

**[!UICONTROL Target]**

>[!NOTE]
>
>Questa categoria è visibile solo se selezioni un messaggio evento. Per i messaggi di profilo, **[!UICONTROL Target]** I campi vengono recuperati automaticamente dal sistema utilizzando la riconciliazione eseguita da Adobe Campaign Standard.

In questa sezione devi definire **[!UICONTROL Piattaforma push]**. L’elenco a discesa consente di selezionare **[!UICONTROL Server notifiche push Apple]** (iOS) oppure **[!UICONTROL Firebase Cloud Messaging]** (Android) In alternativa, puoi selezionare un campo specifico da un evento o da un’origine dati oppure definire un’espressione avanzata.

È inoltre necessario definire **[!UICONTROL Token di registrazione]**. L’espressione dipende da come viene definito il token nel payload dell’evento o in altri [!DNL Journey Optimizer] informazioni. Può essere un campo semplice o un’espressione più complessa, nel caso in cui il token sia definito in una raccolta, ad esempio:

```
@{Event_push._experience.campaign.message.profileSnapshot.pushNotificationTokens.first().token}
```

**[!UICONTROL Dati di personalizzazione]**

>[!NOTE]
>
>Non è possibile trasmettere una raccolta nei dati di personalizzazione. Se il push transazionale prevede delle raccolte, non funzionerà. Inoltre, i dati di personalizzazione hanno un formato previsto (ad esempio, stringa, decimale e così via). Devi fare attenzione a rispettare questi formati previsti.

Questi sono i campi previsti dal modello transazionale utilizzato nel messaggio di Adobe Campaign Standard. Questi campi possono essere utilizzati per personalizzare il messaggio, applicare la formattazione condizionale o scegliere una variante di messaggio specifica.
