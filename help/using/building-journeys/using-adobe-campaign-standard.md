---
solution: Journey Optimizer
product: journey optimizer
title: Azioni di Adobe Campaign Standard
description: Scopri le azioni di Adobe Campaign Standard
feature: Journeys, Actions, Custom Actions
topic: Administration
role: User
level: Intermediate
keywords: percorso, integrazione, standard, campagna, ACS
exl-id: 50565cd9-7415-4c6a-9651-24fefeded3f5
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/spxxZT-JH5yzziL8-oSkJdBcKEppm-4ZzeLC2-laCaM
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: c2beecbb-b93e-4ae3-baa9-72adcdc06781
  - id: d8353d85-5da7-453d-bd68-40ad33fa0ab7
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1484
ht-degree: 5%

---

# Azioni di [!DNL Adobe Campaign] Standard {#using_campaign_action}

>[!BEGINSHADEBOX]

**In questa pagina:** scopri come utilizzare le attività di azione e-mail, push e SMS integrate di Adobe Campaign Standard nei tuoi percorsi utilizzando i modelli di messaggistica transazionale di Campaign Standard.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom_acs"
>title="Azioni personalizzate"
>abstract="È disponibile un’integrazione per [!DNL Adobe Campaign] Standard. Consente di inviare e-mail, notifiche push ed SMS utilizzando le funzionalità di messaggistica transazionale di [!DNL Adobe Campaign]."

Se disponi di [!DNL Adobe Campaign] Standard, sono disponibili le seguenti attività di azione integrate: **[!UICONTROL E-mail]**, **[!UICONTROL Invia]** e **[!UICONTROL SMS]**.

>[!NOTE]
>
>A questo scopo, devi configurare l’azione incorporata. Consulta [questa pagina](../action/acs-action.md).

Per ciascuno di questi canali, selezionare un **modello** di messaggistica transazionale standard [!DNL Adobe Campaign]. Per i canali e-mail, SMS e push incorporati, ci affidiamo alla messaggistica transazionale per eseguire l’invio dei messaggi. Ciò significa che se si desidera utilizzare un determinato modello di messaggio nei percorsi, è necessario pubblicarlo in [!DNL Adobe Campaign] Standard. Per informazioni su come utilizzare questa funzione, consulta [questa pagina](https://experienceleague.adobe.com/docs/campaign-standard/using/communication-channels/transactional-messaging/getting-started-with-transactional-msg.html?lang=it).

>[!NOTE]
>
>Per poter essere utilizzato in Journey Optimizer, il messaggio transazionale di Campaign Standard e il relativo evento associato devono essere pubblicati. Se l’evento viene pubblicato ma il messaggio non lo è, non sarà visibile nell’interfaccia di Journey Optimizer. Se il messaggio viene pubblicato ma il relativo evento associato non lo è, sarà visibile nell’interfaccia di Journey Optimizer ma non sarà utilizzabile.

Configurazione azione standard ![[!DNL Adobe Campaign] nel percorso](assets/journey59.png)

Puoi utilizzare un evento (noto anche come modello di messaggistica transazionale di profilo in tempo reale).

>[!NOTE]
>
>Quando inviamo messaggi transazionali in tempo reale (rtEvent) o quando inviamo messaggi con un sistema di terze parti grazie a un’azione personalizzata, è necessaria una configurazione specifica per la gestione dell’affaticamento, dell’elenco Bloccati o dell’annullamento dell’abbonamento. Ad esempio, se un attributo &quot;unsubscribe&quot; è memorizzato in [!DNL Adobe Experience Platform] o in un sistema di terze parti, sarà necessario aggiungere una condizione prima dell&#39;invio del messaggio per verificare questa condizione.

Quando selezioni un modello, tutti i campi previsti nel payload del messaggio vengono visualizzati nel riquadro di configurazione dell&#39;attività in **[!UICONTROL Indirizzo]** e **[!UICONTROL Dati Personalization]**. Devi mappare ciascuno di questi campi con il campo che desideri utilizzare, dall’evento o dall’origine dati. È inoltre possibile utilizzare l’editor di espressioni avanzate per passare manualmente un valore, manipolare i dati sulle informazioni recuperate (ad esempio, convertire una stringa in maiuscolo) o utilizzare funzioni quali &quot;if, then, else&quot;. Consulta [questa pagina](expression/expressionadvanced.md).

![Interfaccia di selezione del modello di messaggio di Campaign Standard](assets/journey60.png)

## E-mail e SMS {#section_asc_51g_nhb}

Per **[!UICONTROL Email]** e **[!UICONTROL SMS]**, i parametri sono identici.

>[!NOTE]
>
>Quando si utilizza il modello transazionale di un profilo per l&#39;e-mail, il meccanismo di annullamento dell&#39;abbonamento viene gestito automaticamente da [!DNL Adobe Campaign] Standard.
>Includi un blocco di contenuto **[!UICONTROL Collegamento di annullamento sottoscrizione]** all&#39;interno di [modello di e-mail transazionale](https://experienceleague.adobe.com/docs/campaign-standard/using/communication-channels/transactional-messaging/getting-started-with-transactional-msg.html?lang=it).
>Se utilizzi un modello basato su eventi (rtEvent), incorpora nel messaggio un collegamento che trasmette l&#39;e-mail del destinatario come parametro URL e li indirizza a una pagina di destinazione per l&#39;annullamento dell&#39;abbonamento.
>Crea la pagina di destinazione e assicurati che la decisione di annullamento dell&#39;abbonamento del destinatario sia trasmessa ad Adobe.

Innanzitutto, devi scegliere un modello di messaggistica transazionale.

Sono disponibili due categorie: **[!UICONTROL Indirizzo]** e **[!UICONTROL Dati Personalization]**.

Puoi definire facilmente dove recuperare **[!UICONTROL Indirizzo]** o **[!UICONTROL Dati Personalization]** tramite l&#39;interfaccia. Puoi sfogliare gli eventi e i campi dell’origine dati disponibili. È inoltre possibile utilizzare l’editor di espressioni avanzate per casi di utilizzo più avanzati, ad esempio per utilizzare un’origine dati che richiede il passaggio di parametri o l’esecuzione di manipolazioni. Consulta [questa pagina](expression/expressionadvanced.md).

**[!UICONTROL Indirizzo]**

>[!NOTE]
>
>Questa categoria è visibile solo se selezioni un messaggio transazionale &quot;evento&quot;. Per i messaggi &quot;profile&quot;, il campo **[!UICONTROL Indirizzo]** viene recuperato automaticamente da [!DNL Adobe Campaign] Standard dal sistema.

Questi sono i campi necessari per sapere dove inviare il messaggio. Per un modello e-mail, si tratta dell’indirizzo e-mail. Per un SMS, è il numero del cellulare.

![Configurazione del parametro Message per l&#39;integrazione di Campaign Standard](assets/journey61.png)

**[!UICONTROL Dati Personalization]**

>[!NOTE]
>
>Non è possibile trasmettere una raccolta nei dati di personalizzazione. Se l’e-mail o l’SMS transazionale prevede delle raccolte, non funzioneranno. Inoltre, i dati di personalizzazione hanno un formato previsto (ad esempio, stringa, decimale e così via). Devi fare attenzione a rispettare questi formati previsti.

Questi sono i campi previsti dal messaggio di [!DNL Adobe Campaign] Standard. Questi campi possono essere utilizzati per personalizzare il messaggio, applicare la formattazione condizionale o scegliere una variante di messaggio specifica.

![Mappatura campi tra Journey Optimizer e Campaign Standard](assets/journey62.png)

## Push {#section_im3_hvf_nhb}

Prima di utilizzare l’attività push, è necessario configurare l’app mobile e Campaign Standard per inviare le notifiche push. Utilizza questo [articolo](https://helpx.adobe.com/it/campaign/kb/integrate-mobile-sdk.html) per eseguire i passaggi di implementazione necessari per Mobile.

Innanzitutto, devi scegliere un’app mobile dall’elenco a discesa e un messaggio transazionale.

![Editor di espressioni avanzate per la mappatura dei parametri di Campaign Standard](assets/journey62bis.png)

Sono disponibili due categorie: **[!UICONTROL Target]** e **[!UICONTROL Dati Personalization]**.

**[!UICONTROL Target]**

>[!NOTE]
>
>Questa categoria è visibile solo se selezioni un messaggio evento. Per i messaggi di profilo, i campi **[!UICONTROL Target]** vengono recuperati automaticamente dal sistema utilizzando la riconciliazione eseguita da [!DNL Adobe Campaign] Standard.

In questa sezione è necessario definire la **[!UICONTROL piattaforma push]**. L&#39;elenco a discesa consente di selezionare **[!UICONTROL Apple Push Notification Server]** (iOS) o **[!UICONTROL Firebase Cloud Messaging]** (Android). In alternativa, puoi selezionare un campo specifico da un evento o da un’origine dati oppure definire un’espressione avanzata.

È inoltre necessario definire il **[!UICONTROL Token di registrazione]**. L&#39;espressione dipende dalla modalità di definizione del token nel payload dell&#39;evento o in altre informazioni di [!DNL Journey Optimizer]. Può essere un campo semplice o un’espressione più complessa, nel caso in cui il token sia definito in una raccolta, ad esempio:

```
@event{Event_push._experience.campaign.message.profileSnapshot.pushNotificationTokens.first().token}
```

**[!UICONTROL Dati Personalization]**

>[!NOTE]
>
>Non è possibile trasmettere una raccolta nei dati di personalizzazione. Se il push transazionale prevede delle raccolte, non funzionerà. Inoltre, i dati di personalizzazione hanno un formato previsto (ad esempio, stringa, decimale e così via). Devi fare attenzione a rispettare questi formati previsti.

Questi sono i campi previsti dal modello transazionale utilizzato nel messaggio di [!DNL Adobe Campaign] Standard. Questi campi possono essere utilizzati per personalizzare il messaggio, applicare la formattazione condizionale o scegliere una variante di messaggio specifica.

+++ Guida di riferimento della Knowledge Base di AI

Questa sezione contiene informazioni strutturate che supportano l&#39;interpretazione, il recupero e la risposta alle domande relative a questo argomento.

Per una comprensione completa, queste informazioni devono essere unite alla documentazione su questa pagina. Nessuna delle due origini è progettata per essere indipendente; la pagina descrive la funzione, mentre questa sezione fornisce un contesto aggiuntivo che aiuta a non ambiguare la terminologia, le finalità, l’applicabilità e i vincoli.

* **TL;DR:** In questa pagina viene illustrato come utilizzare le attività predefinite di e-mail, SMS e azioni push di Adobe Campaign Standard nei percorsi Journey Optimizer tramite i modelli di messaggistica transazionale di Campaign.

**Intenti:**

* Configurare le attività di azione e-mail, SMS o push in un percorso utilizzando l’integrazione di Adobe Campaign Standard
* Selezionare e mappare un modello di messaggistica transazionale Campaign Standard ai campi del percorso
* Mappare i campi Indirizzo e Dati Personalization dagli eventi di percorso o dalle origini dati al payload del messaggio
* Gestire l’annullamento dell’abbonamento per i modelli e-mail transazionali basati su eventi e profili
* Configurare la piattaforma di destinazione per le notifiche push e il token di registrazione per le azioni push di Campaign Standard

**Glossario:**

* **Messaggistica transazionale**: funzionalità Adobe Campaign Standard per l&#39;invio di messaggi attivati in tempo reale (e-mail, SMS, push) basati su eventi *(specifici del prodotto)*
* **rtEvent**: modello di messaggio transazionale di evento in tempo reale in Adobe Campaign Standard, utilizzato per la messaggistica basata su eventi *(specifico per prodotto)*
* **Modello transazionale di profilo**: modello di messaggio transazionale di Campaign Standard che utilizza i dati di profilo per la risoluzione dei destinatari e la gestione dell&#39;annullamento dell&#39;abbonamento *(specifico per prodotto)*
* **Token di registrazione**: è necessario un identificatore a livello di dispositivo per indirizzare una notifica push a una specifica installazione di app mobili *(specifico per prodotto)*

**Guardrail:**

* L’azione incorporata deve essere configurata prima dell’uso; consulta la pagina di configurazione dell’azione.
* Affinché il modello sia utilizzabile in Journey Optimizer, è necessario pubblicare sia il messaggio transazionale di Campaign Standard che il relativo evento associato.
* Le raccolte non possono essere trasmesse nei campi dati di Personalization.
* Per i modelli basati su eventi (rtEvent), la gestione dell’annullamento dell’abbonamento deve essere gestita manualmente con una condizione prima dell’invio.
* Per i messaggi push basati su profilo, i campi di Target vengono recuperati automaticamente; la categoria Target è visibile solo per i messaggi evento.
* Per poter utilizzare l’attività push, l’app mobile deve essere configurata con Campaign Standard.

**Terminologia:**

* Nome canonico: Adobe Campaign Standard — Acronimo: ACS — varianti: Campaign Standard
* Sinonimi: &quot;messaggio transazionale di evento&quot; = &quot;rtEvent&quot;; &quot;messaggio transazionale in tempo reale&quot; = &quot;rtEvent&quot;
* Non confondere: &quot;modello transazionale di profilo&quot; (annullamento dell’abbonamento gestito automaticamente) ≠ &quot;modello transazionale di evento&quot; (l’annullamento dell’abbonamento deve essere gestito manualmente)

**Domande frequenti:**

* **D: quali canali sono disponibili tramite l&#39;integrazione Adobe Campaign Standard?** — I canali e-mail, SMS e di notifica push sono disponibili come attività di azione integrate.
* **D: è necessario pubblicare il messaggio transazionale in Campaign Standard prima di utilizzarlo in Journey Optimizer?** — Sì, è necessario pubblicare sia il messaggio transazionale che il relativo evento associato; un messaggio non pubblicato non sarà utilizzabile anche se visibile nell’interfaccia.
* **D: come viene gestita l&#39;annullamento dell&#39;abbonamento per i modelli e-mail basati su profili?** — L&#39;annullamento dell&#39;abbonamento viene gestito automaticamente da Adobe Campaign Standard quando si utilizza un modello transazionale di profilo; include nel modello un blocco di contenuto del collegamento di annullamento all&#39;abbonamento.
* **Q: posso passare una raccolta come dati di personalizzazione?** — No, non è possibile trasmettere le raccolte in Personalization Data; il messaggio transazionale non deve prevedere le raccolte.
* **D: dove posso mappare l&#39;indirizzo del destinatario per un&#39;e-mail basata su eventi?** — La categoria Indirizzo nel riquadro di configurazione dell&#39;attività è visibile solo per i messaggi transazionali di evento; per i messaggi di profilo l&#39;indirizzo viene recuperato automaticamente.

+++
