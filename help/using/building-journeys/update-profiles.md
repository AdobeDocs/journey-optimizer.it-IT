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
TQID: https://experienceleague.adobe.com/ifDBXoNDryXLKMkm59mVqT7-unQYG1JKTfMN7zAoWsA
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: cfba2953-2ce9-4b00-a00c-71cd338ae63f
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: b5d14f7b40933f110ff666db858e976e5de711db
workflow-type: tm+mt
source-wordcount: 1491
ht-degree: 4%

---

# Aggiornare il profilo {#update-profile}

>[!BEGINSHADEBOX]

**In questa pagina:** scopri come utilizzare l&#39;attività di azione Aggiorna profilo per arricchire o correggere un profilo Adobe Experience Platform esistente mentre un cliente procede attraverso un percorso.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_update_profiles"
>title="Attività Aggiorna profilo"
>abstract="L’attività Aggiorna profilo consente di aggiornare un profilo [!DNL Adobe Experience Platform] esistente con un valore specifico oppure con informazioni provenienti dall’evento o da un’origine dati."

Utilizzare l&#39;attività di azione **[!UICONTROL Aggiorna profilo]** per arricchire o correggere un profilo [!DNL Adobe Experience Platform] esistente durante l&#39;avanzamento di un cliente in un percorso. È possibile impostare i valori dei campi originati da un evento di percorso, un’origine dati configurata o un valore statico, consentendo di mantenere accurati e utilizzabili i dati del profilo senza uscire dall’area di lavoro del percorso. Prima di configurare questa attività, controlla le [protezioni e limitazioni](#guardrails) applicabili.

## Selezione set di dati {#dataset-selection}

L&#39;attività **[!UICONTROL Aggiorna profilo]** richiede un set di dati dedicato per archiviare gli aggiornamenti. Poiché questa attività aggiorna solo l&#39;[archivio profili](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=it#profile-data-store){target="_blank"} (non Datalake), tutti gli aggiornamenti devono essere salvati in un [set di dati abilitato per il profilo](https://experienceleague.adobe.com/it/docs/experience-platform/catalog/datasets/user-guide#enable-profile){target="_blank"} specificamente designato per le azioni **[!UICONTROL Aggiorna profilo]**.

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

Solo i profili di test possono accedere a un percorso in modalità di test. È possibile creare un nuovo profilo di test o convertire un profilo esistente in un profilo di test. In [!DNL Adobe Experience Platform], gli attributi del profilo possono essere aggiornati tramite un&#39;importazione di file CSV o chiamate API. Un&#39;alternativa più rapida consiste nell&#39;utilizzare un&#39;attività **[!UICONTROL Aggiorna profilo]** all&#39;interno del percorso stesso per impostare il campo booleano del profilo di test su true.

Per ulteriori informazioni su come trasformare un profilo esistente in un profilo di test, consulta questa [sezione](../audience/creating-test-profiles.md#create-test-profiles-csv).

## Guardrail e limitazioni {#guardrails}

* L&#39;azione **[!UICONTROL Aggiorna profilo]** può essere utilizzata solo in percorsi con [spazio dei nomi](../event/about-creating.md#select-the-namespace).
* L’azione aggiorna solo i campi esistenti, non crea nuovi campi profilo.
* L’azione supporta solo tipi di campo semplici (stringa, numero, booleano). I campi XDM definiti come enumerazioni, valori suggeriti, array di oggetti o raccolte complesse (ad esempio, elenchi di prodotti) non sono supportati.
* Impossibile utilizzare l&#39;azione **[!UICONTROL Aggiorna profilo]** per generare [eventi esperienza](../event/about-events.md), ad esempio un acquisto.
* Come qualsiasi altra azione, puoi definire un percorso alternativo [in caso di errore o timeout](using-the-journey-designer.md#paths). Non è possibile eseguire due azioni in parallelo.
* Non è garantito che gli aggiornamenti del profilo siano immediatamente disponibili a valle nello stesso percorso. Evita di inserire un&#39;azione che legga un campo direttamente dopo l&#39;azione **[!UICONTROL Aggiorna profilo]** che lo scrive, poiché il valore aggiornato potrebbe non essere ancora riflesso.
* L&#39;attività **[!UICONTROL Aggiorna profilo]** aggiorna solo il [archivio profili](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=it#profile-data-store){target="_blank"}, non il Data Lake.
* È possibile aggiornare fino a cinque coppie campo/valore in una singola azione **[!UICONTROL Aggiorna profilo]**. Utilizza il pulsante **[!UICONTROL Aggiorna un altro campo]** per aggiungere altre coppie.
* Per migliorare le prestazioni, raggruppare più aggiornamenti di attributi in un&#39;unica azione **[!UICONTROL Aggiorna profilo]** anziché utilizzare una sola azione per attributo.

+++ Guida di riferimento della Knowledge Base di AI

Questa sezione contiene informazioni strutturate che supportano l&#39;interpretazione, il recupero e la risposta alle domande relative a questo argomento.

Per una comprensione completa, queste informazioni devono essere unite alla documentazione su questa pagina. Nessuna delle due origini è progettata per essere indipendente; la pagina descrive la funzione, mentre questa sezione fornisce un contesto aggiuntivo che aiuta a non ambiguare la terminologia, le finalità, l’applicabilità e i vincoli.

* **TL;DR:** In questa pagina viene illustrato come configurare l&#39;attività Aggiorna profilo per arricchire o correggere un profilo Adobe Experience Platform esistente con dati provenienti da eventi di percorso, origini dati o valori statici durante l&#39;avanzamento di un cliente in un percorso.

**Intenti:**

* Configurare l’attività Update Profile per modificare gli attributi di profilo esistenti durante un percorso
* Seleziona un set di dati abilitato per il profilo dedicato alle azioni Aggiorna profilo
* Mappa i valori dei campi da eventi di percorso, origini dati o valori statici agli attributi del profilo
* Aggiornare più attributi di profilo (fino a cinque) in una singola attività
* Aggiornamenti del profilo di test in modalità di test percorso

**Glossario:**

* **Aggiorna attività profilo**: attività di azione che scrive nuovi valori in campi esistenti in un profilo Adobe Experience Platform in tempo reale mentre un profilo si sposta attraverso un percorso *(specifico per prodotto)*
* **Archivio profili**: l&#39;archivio Adobe Experience Platform che contiene i dati del profilo cliente in tempo reale, distinto dal Data Lake *(specifico per prodotto)*
* **Spazio dei nomi identità**: etichetta che distingue i contesti di identità (ad esempio e-mail, ID CRM) utilizzati per far corrispondere il profilo da aggiornare *(specifico per prodotto)*
* **Set di dati abilitato per il profilo**: un set di dati Adobe Experience Platform configurato per contribuire con record al profilo unificato *(specifico per prodotto)*

**Guardrail:**

* L&#39;azione Aggiorna profilo può essere utilizzata solo nei percorsi in cui è definito uno spazio dei nomi.
* L’azione aggiorna solo i campi XDM esistenti; non può creare nuovi campi di profilo.
* Sono supportati solo i tipi di campo semplici (stringa, numero, booleano); non sono supportate enumerazioni, array di oggetti e raccolte complesse.
* L’azione non può generare eventi di esperienza come acquisti.
* È possibile aggiornare fino a cinque coppie campo/valore in una singola azione Aggiorna profilo.
* Non condividere il set di dati dedicato con i processi di acquisizione in batch o in streaming, in quanto altre esecuzioni di acquisizione sovrascriveranno le modifiche apportate al profilo di aggiornamento.
* Gli aggiornamenti del profilo potrebbero non essere immediatamente disponibili a valle nell’esecuzione dello stesso percorso.
* L’attività aggiorna solo l’archivio profili, non il Data Lake.

**Terminologia:**

* Nome canonico: Aggiorna profilo — Acronimo: none — Varianti: Aggiorna attività profilo, Azione Aggiorna profilo
* Sinonimi: &quot;Profile Store&quot; = &quot;Real-Time Customer Profile store&quot;
* Non confondere: &quot;Archivio profili&quot; (aggiornato da questa attività) ≠ &quot;Data Lake&quot; (non aggiornato da questa attività)

**Domande frequenti:**

* **Q: l&#39;attività Aggiorna profilo può creare nuovi campi del profilo?** — No, può solo aggiornare campi che esistono già nello schema profilo XDM selezionato.
* **Q: perché dovrei usare un set di dati dedicato per le azioni Aggiorna profilo?** — la condivisione del set di dati con l’acquisizione in batch o in streaming può causare la sovrascrittura delle modifiche apportate dall’attività Aggiorna profilo da parte di altre esecuzioni di acquisizione.
* **Q: gli aggiornamenti dei profili sono immediatamente visibili alle attività a valle nello stesso percorso?** — No, i valori aggiornati potrebbero non essere ancora riflessi se un&#39;azione legge lo stesso campo immediatamente dopo che è stato scritto dall&#39;attività Aggiorna profilo.
* **D: quanti campi posso aggiornare in una singola azione Aggiorna profilo?** — È possibile configurare fino a cinque coppie campo/valore in una singola attività utilizzando il pulsante &quot;Aggiorna un altro campo&quot;.
* **Q: gli aggiornamenti dei profili vengono applicati in modalità di test?** — Sì, in modalità di test gli aggiornamenti hanno effetto immediato sul profilo di test e non sono simulati.

+++
