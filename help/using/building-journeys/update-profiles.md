---
solution: Journey Optimizer
product: journey optimizer
title: Aggiornare il profilo
description: Scopri come utilizzare l’attività Aggiorna profilo in un percorso
feature: Journeys, Profiles, Activities
topic: Content Management
role: User
level: Intermediate
keywords: profilo, aggiornamento, percorso, attività
exl-id: 8b2b2d1e-9bd1-439d-a15e-acdbab387c4b
version: Journey Orchestration
source-git-commit: 0a2c384faea70dcbc9b99596740e375d85b2bc64
workflow-type: tm+mt
source-wordcount: '862'
ht-degree: 4%

---

# Aggiornare il profilo {#update-profile}

>[!CONTEXTUALHELP]
>id="ajo_journey_update_profiles"
>title="Attività Aggiorna profilo"
>abstract="L’attività Aggiorna profilo consente di aggiornare un profilo [!DNL Adobe Experience Platform] esistente con un valore specifico oppure con informazioni provenienti dall’evento o da un’origine dati."

Utilizzare l&#39;attività di azione **[!UICONTROL Aggiorna profilo]** per arricchire o correggere un profilo [!DNL Adobe Experience Platform] esistente durante l&#39;avanzamento di un cliente in un percorso. È possibile impostare i valori dei campi originati da un evento di percorso, un’origine dati configurata o un valore statico, consentendo di mantenere accurati e utilizzabili i dati del profilo senza uscire dall’area di lavoro del percorso. Prima di configurare questa attività, controlla le [protezioni e limitazioni](#guardrails) applicabili.

## Selezione set di dati {#dataset-selection}

L&#39;attività **[!UICONTROL Aggiorna profilo]** richiede un set di dati dedicato per archiviare gli aggiornamenti. Poiché questa attività aggiorna solo l&#39;[archivio profili](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html#profile-data-store){target="_blank"} (non Datalake), tutti gli aggiornamenti devono essere salvati in un [set di dati abilitato per il profilo](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/user-guide#enable-profile){target="_blank"} specificamente designato per le azioni **[!UICONTROL Aggiorna profilo]**.

>[!CAUTION]
>
>Non utilizzare un set di dati utilizzato anche per l’acquisizione in batch o in streaming. Altre esecuzioni dell&#39;acquisizione sovrascriveranno le modifiche apportate dall&#39;azione **[!UICONTROL Aggiorna profilo]**, causando la scomparsa degli attributi del profilo o il ripristino dei valori precedenti. Se osservi questo comportamento, verifica in Adobe Experience Platform che nessun’altra acquisizione stia scrivendo sullo stesso set di dati. Per informazioni sulla risoluzione dei problemi, vedere [Risoluzione degli errori di aggiornamento del profilo in Adobe Journey Optimizer](https://experienceleague.adobe.com/it/docs/experience-cloud-kcs/kbarticles/ka-26352){target="_blank"}.

Inoltre, la configurazione dell&#39;attività **[!UICONTROL Aggiorna profilo]** non richiede uno spazio dei nomi [Identity](https://experienceleague.adobe.com/it/docs/experience-platform/identity/features/namespaces){target="_blank"}. Di conseguenza, assicurati che il set di dati selezionato utilizzi lo stesso **[!UICONTROL spazio dei nomi identità]** utilizzato dall&#39;azione che ha avviato il percorso, in quanto questo spazio dei nomi verrà utilizzato da questi aggiornamenti. La mappa delle identità può essere utilizzata anche dal set di dati selezionato. Se non si seleziona un set di dati con lo spazio dei nomi identità corretto o uno che utilizza la mappa delle identità, l&#39;attività **[!UICONTROL Aggiorna profilo]** non riuscirà.

## Configurare l’attività di aggiornamento del profilo {#use-profile-update}

Segui i passaggi seguenti per configurare l&#39;attività **[!UICONTROL Aggiorna profilo]** nel tuo percorso.

1. Inizia a progettare il percorso. Ulteriori informazioni in [Creare il primo percorso](../building-journeys/journey-gs.md).

1. Nella sezione **[!UICONTROL Azione]** della palette, rilascia l&#39;attività **[!UICONTROL Aggiorna profilo]** nell&#39;area di lavoro.

   ![Aggiorna l&#39;attività profilo nella palette percorso in Azioni](assets/profileupdate0.png)

1. Seleziona uno schema dall’elenco.

   >[!NOTE]
   >
   >Solo i campi già esistenti nello schema di profilo XDM selezionato sono disponibili per la selezione. Se il campo necessario non è elencato, aggiungilo prima allo schema in Adobe Experience Platform.

1. Fai clic su **[!UICONTROL Campo]** per selezionare il campo da aggiornare.

   ![Selezione del campo da aggiornare](assets/profileupdate2.png)

1. Seleziona un set di dati dall’elenco.

   >[!NOTE]
   >
   >L&#39;azione **[!UICONTROL Aggiorna profilo]** aggiorna i dati del profilo in tempo reale, ma non i set di dati. La selezione del set di dati è necessaria in quanto il profilo è un record correlato a un set di dati.

1. Fai clic sul campo **[!UICONTROL Valore]** per definire il valore da utilizzare:

   * Utilizzando l’editor di espressioni semplici, puoi selezionare un campo da un’origine dati o dall’evento in ingresso.

     ![Selettore di campi in modalità semplice per gli aggiornamenti degli attributi di profilo](assets/profileupdate4.png)

   * Se si desidera definire un valore specifico o sfruttare funzioni avanzate, selezionare [**[!UICONTROL Modalità avanzata]**](expression/expressionadvanced.md).

     ![Editor espressioni modalità avanzata per aggiornamenti di profilo complessi](assets/profileupdate3.png)

1. Per aggiornare attributi di profilo aggiuntivi nella stessa azione, fare clic su **[!UICONTROL Aggiorna un altro campo]** e ripetere la selezione del campo e del valore. È possibile aggiungere fino a cinque coppie campo/valore in una singola azione **[!UICONTROL Aggiorna profilo]**. Consulta [Guardrail e limitazioni](#guardrails).

L&#39;attività **[!UICONTROL Aggiorna profilo]** è ora configurata.

![Attività di aggiornamento profilo in un percorso con configurazione di più campi](assets/profileupdate1.png)


## Verificare l’aggiornamento del profilo {#using-the-test-mode}

Tieni presente che in [modalità di test](testing-the-journey.md) gli aggiornamenti del profilo hanno effetto immediato sul profilo di test e non sono simulati.

Solo i profili di test possono entrare in un percorso in modalità di test. È possibile creare un nuovo profilo di test o convertire un profilo esistente in un profilo di test. In [!DNL Adobe Experience Platform], gli attributi del profilo possono essere aggiornati tramite un&#39;importazione di file CSV o chiamate API. Un&#39;alternativa più rapida consiste nell&#39;utilizzare un&#39;attività **[!UICONTROL Aggiorna profilo]** all&#39;interno del percorso stesso per impostare il campo booleano del profilo di test su true.

Per ulteriori informazioni su come trasformare un profilo esistente in un profilo di test, consulta questa [sezione](../audience/creating-test-profiles.md#create-test-profiles-csv).

## Guardrail e limitazioni {#guardrails}

* L&#39;azione **[!UICONTROL Aggiorna profilo]** può essere utilizzata solo in percorsi con [spazio dei nomi](../event/about-creating.md#select-the-namespace).
* L’azione aggiorna solo i campi esistenti, non crea nuovi campi profilo.
* L’azione supporta solo tipi di campo semplici (stringa, numero, booleano). I campi XDM definiti come enumerazioni, valori suggeriti, array di oggetti o raccolte complesse (ad esempio, elenchi di prodotti) non sono supportati.
* Impossibile utilizzare l&#39;azione **[!UICONTROL Aggiorna profilo]** per generare [eventi esperienza](../event/about-events.md), ad esempio un acquisto.
* Come qualsiasi altra azione, puoi definire un percorso alternativo [in caso di errore o timeout](using-the-journey-designer.md#paths). Non è possibile eseguire due azioni in parallelo.
* Non è garantito che gli aggiornamenti del profilo siano immediatamente disponibili a valle nello stesso percorso. Evita di inserire un&#39;azione che legga un campo direttamente dopo l&#39;azione **[!UICONTROL Aggiorna profilo]** che lo scrive, poiché il valore aggiornato potrebbe non essere ancora riflesso.
* L&#39;attività **[!UICONTROL Aggiorna profilo]** aggiorna solo il [archivio profili](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html#profile-data-store){target="_blank"}, non il Data Lake.
* È possibile aggiornare fino a cinque coppie campo/valore in una singola azione **[!UICONTROL Aggiorna profilo]**. Utilizza il pulsante **[!UICONTROL Aggiorna un altro campo]** per aggiungere altre coppie.
* Per migliorare le prestazioni, raggruppare più aggiornamenti di attributi in un&#39;unica azione **[!UICONTROL Aggiorna profilo]** anziché utilizzare una sola azione per attributo.
