---
solution: Journey Optimizer
product: journey optimizer
title: Azioni di Adobe Campaign Standard
description: Informazioni sulle azioni di Adobe Campaign Standard
feature: Actions
topic: Administration
role: Admin
level: Intermediate
exl-id: 50565cd9-7415-4c6a-9651-24fefeded3f5
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '920'
ht-degree: 4%

---

# Azioni di Adobe Campaign Standard {#using_campaign_action}

Se disponi di Adobe Campaign Standard, sono disponibili le seguenti attività di azione integrate: **[!UICONTROL E-mail]**, **[!UICONTROL Push]** e **[!UICONTROL SMS]**.

>[!NOTE]
>
>A questo scopo, devi configurare l’azione incorporata. Consulta [questa pagina](../action/acs-action.md).

Per ciascuno di questi canali, seleziona una messaggistica transazionale Adobe Campaign Standard **template**. Per i canali e-mail, SMS e push incorporati, ci affidiamo alla messaggistica transazionale per eseguire l’invio dei messaggi. Significa che se desideri utilizzare un determinato modello di messaggio nei tuoi percorsi, devi pubblicarlo in Adobe Campaign Standard. Fai riferimento a [questa pagina](https://experienceleague.adobe.com/docs/campaign-standard/using/communication-channels/transactional-messaging/getting-started-with-transactional-msg.html?lang=it) per scoprire come utilizzare questa funzione.

>[!NOTE]
>
>Per poter essere utilizzato in Journey Optimizer, è necessario pubblicare il messaggio transazionale di Campaign Standard e il relativo evento associato. Se l’evento è pubblicato ma il messaggio non lo è, non sarà visibile nell’interfaccia di Journey Optimizer. Se il messaggio viene pubblicato ma l’evento associato non lo è, sarà visibile nell’interfaccia di Journey Optimizer ma non sarà utilizzabile.

![](assets/journey59.png)

Puoi utilizzare un evento (noto anche come in tempo reale) o un modello di messaggistica transazionale di profilo.

>[!NOTE]
>
>Quando inviamo messaggi transazionali in tempo reale (rtEvent) o quando inviamo messaggi con un sistema di terze parti tramite un’azione personalizzata, è necessaria una configurazione specifica per la gestione dell’affaticamento, dell’elenco Bloccati o dell’annullamento dell’abbonamento. Ad esempio, se un attributo &quot;Annulla sottoscrizione&quot; è memorizzato in Adobe Experience Platform o in un sistema di terze parti, prima che il messaggio di invio verifichi questa condizione sarà necessario aggiungere una condizione.

Quando selezioni un modello, tutti i campi previsti nel payload del messaggio vengono visualizzati nel riquadro di configurazione dell’attività in **[!UICONTROL Indirizzo]** e **[!UICONTROL Dati di personalizzazione]**. Devi mappare ciascuno di questi campi con il campo che desideri utilizzare, dall’evento o dall’origine dati. È inoltre possibile utilizzare l’editor di espressioni avanzate per passare manualmente un valore, eseguire la manipolazione dei dati sulle informazioni recuperate (ad esempio convertire una stringa in maiuscolo) o utilizzare funzioni come &quot;if, then, else&quot;. Consulta [questa pagina](expression/expressionadvanced.md).

![](assets/journey60.png)

## E-mail e SMS {#section_asc_51g_nhb}

Per **[!UICONTROL E-mail]** e **[!UICONTROL SMS]**, i parametri sono identici.

>[!NOTE]
>
>Per l’e-mail, se utilizzi un modello transazionale di profili, il meccanismo di annullamento dell’abbonamento viene gestito da Campaign Standard. Aggiungi semplicemente un **[!UICONTROL Collegamento di annullamento dell’abbonamento]** blocco di contenuto nel modello ([ulteriori informazioni](https://experienceleague.adobe.com/docs/campaign-standard/using/communication-channels/transactional-messaging/getting-started-with-transactional-msg.html?lang=it)). Se utilizzi un modello basato su eventi (rtEvent), devi aggiungere nel messaggio un collegamento che passa l’e-mail della persona nel parametro URL e punta a una pagina di destinazione per l’annullamento dell’abbonamento. Devi creare questa pagina di destinazione e accertarti che la decisione dell’utente di annullare l’iscrizione sia trasmessa all’Adobe.

Innanzitutto, devi scegliere un modello di messaggistica transazionale.

Sono disponibili due categorie: **[!UICONTROL Indirizzo]** e **[!UICONTROL Dati di personalizzazione]**.

Puoi definire facilmente dove recuperare il **[!UICONTROL Indirizzo]** o **[!UICONTROL Dati di personalizzazione]** utilizzando l’interfaccia . È possibile sfogliare gli eventi e i campi dell’origine dati disponibili. Puoi inoltre utilizzare l’editor di espressioni avanzate per casi d’uso più avanzati, ad esempio per utilizzare un’origine dati che richiede il passaggio di parametri o l’esecuzione di manipolazioni. Consulta [questa pagina](expression/expressionadvanced.md).

**[!UICONTROL Indirizzo]**

>[!NOTE]
>
>Questa categoria è visibile solo se selezioni un messaggio transazionale &quot;evento&quot;. Per i messaggi &quot;profile&quot;, la **[!UICONTROL Indirizzo]** Il campo viene recuperato automaticamente da Adobe Campaign Standard dal sistema.

Questi sono i campi necessari al sistema per sapere dove inviare il messaggio. Per un modello e-mail, si tratta dell’indirizzo e-mail. Per un SMS, è il numero di telefono cellulare.

![](assets/journey61.png)

**[!UICONTROL Dati di personalizzazione]**

>[!NOTE]
>
>Non puoi passare una raccolta nei dati di personalizzazione. Se l’e-mail o l’SMS sulle transazioni prevede delle raccolte, non funzionerà. Tieni presente anche che i dati di personalizzazione hanno un formato previsto (ad esempio: (stringa, decimale, ecc.). Devi fare attenzione a rispettare questi formati previsti.

Questi sono i campi previsti dal messaggio Adobe Campaign Standard. Questi campi possono essere utilizzati per personalizzare il messaggio, applicare la formattazione condizionale o scegliere una specifica variante del messaggio.

![](assets/journey62.png)

## Push {#section_im3_hvf_nhb}

Prima di utilizzare l’attività push, è necessario configurare la tua app mobile insieme a Campaign Standard per l’invio di notifiche push. Utilizza questo [articolo](https://helpx.adobe.com/it/campaign/kb/integrate-mobile-sdk.html) adottare le misure di implementazione necessarie per mobile.

Innanzitutto, devi scegliere un’app mobile dall’elenco a discesa e un messaggio transazionale.

![](assets/journey62bis.png)

Sono disponibili due categorie: **[!UICONTROL Target]** e **[!UICONTROL Dati di personalizzazione]**.

**[!UICONTROL Target]**

>[!NOTE]
>
>Questa categoria è visibile solo se selezioni un messaggio evento. Per i messaggi di profilo, la **[!UICONTROL Target]** i campi vengono recuperati automaticamente dal sistema utilizzando la riconciliazione eseguita da Adobe Campaign Standard.

In questa sezione, devi definire le **[!UICONTROL Piattaforma push]**. L’elenco a discesa ti consente di selezionare **[!UICONTROL Server di notifica push Apple]** (iOS) o **[!UICONTROL Messaggistica Firebase Cloud]** (Android). In alternativa, puoi selezionare un campo specifico da un evento o un’origine dati oppure definire un’espressione avanzata.

È inoltre necessario definire le **[!UICONTROL Token di registrazione]**. L’espressione dipende dalla modalità di definizione del token nel payload dell’evento o in un altro [!DNL Journey Optimizer] informazioni. Può essere un campo semplice o un’espressione più complessa nel caso in cui il token sia definito in una raccolta, ad esempio:

```
@{Event_push._experience.campaign.message.profileSnapshot.pushNotificationTokens.first().token}
```

**[!UICONTROL Dati di personalizzazione]**

>[!NOTE]
>
>Non puoi passare una raccolta nei dati di personalizzazione. Se il push transazionale prevede raccolte, non funzionerà. Tieni presente anche che i dati di personalizzazione hanno un formato previsto (ad esempio: (stringa, decimale, ecc.). Devi fare attenzione a rispettare questi formati previsti.

Questi sono i campi previsti dal modello transazionale utilizzato nel messaggio Adobe Campaign Standard. Questi campi possono essere utilizzati per personalizzare il messaggio, applicare la formattazione condizionale o scegliere una specifica variante del messaggio.
