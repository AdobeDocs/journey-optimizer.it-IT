---
solution: Journey Optimizer
product: journey optimizer
title: Configurare le impostazioni dell’archivio di AEM
description: Scopri come gli amministratori configurano archivi AEM, domini personalizzati, pubblicazione autenticata e accesso ai frammenti di contenuto solo per l’autore in Journey Optimizer.
feature: Integrations
topic: Administration
role: Admin
level: Experienced
keywords: AEM, Frammenti di contenuto, amministrazione, archivio, autenticazione, authoring, pubblicazione
feature_v2:
  - id: fe96aceb-8194-4a8a-a6b0-75302d02804d
subfeature_v2:
  - id: c7dc31c0-c4f7-42a7-8cf5-a8c5aeb0de74
source-git-commit: b7d613c888f67333a4baedfe1605c5ac4f32b18d
workflow-type: tm+mt
source-wordcount: 557
ht-degree: 0%

---

# Configurare l’accesso all’archivio Adobe Experience Manager {#aem-admin-settings}

>[!BEGINSHADEBOX]

**In questa pagina:** scopri come gli amministratori connettono una sandbox a un archivio Adobe Experience Manager, impostando l&#39;accesso in modalità solo autore o per pubblicazione, i domini personalizzati e l&#39;autenticazione in modo che gli addetti al marketing possano utilizzare i frammenti di contenuto AEM nei loro percorsi e campagne.

>[!ENDSHADEBOX]

Adobe Journey Optimizer si integra con **[!DNL Adobe Experience Manager as a Cloud Service]** e **[!DNL Adobe Experience Manager Managed Service]** in modo da poter utilizzare **Frammenti di contenuto** in Percorsi e campagne. **I frammenti di contenuto** vengono letti dall&#39;archivio di pubblicazione di Adobe Experience Manager per impostazione predefinita, gli amministratori possono passare all&#39;accesso di sola creazione o modificare l&#39;accesso di pubblicazione nel menu **[!UICONTROL Integrazione di AEM]**.

➡️ Quando l&#39;archivio è configurato, continuare con [Utilizzare i frammenti di contenuto di Experience Manager](../integrations/aem-fragments.md) per le attività di creazione e selezione in Journey Optimizer.

## Configurare gli archivi {#configure-ui}

>[!NOTE]
>
> **[!UICONTROL L&#39;integrazione di AEM]** salva le impostazioni del repository **per sandbox**. Ogni sandbox mantiene le proprie integrazioni e non si applicano tra le sandbox.

Journey Optimizer memorizza un’integrazione per organizzazione, sandbox e archivio Adobe Experience Manager. Se salvi una nuova integrazione per la stessa combinazione, questa sostituisce le impostazioni precedenti e viene mantenuta solo la configurazione più recente.

➡️ [Scopri questa funzionalità per Adobe Experience Manager Managed Service nel video](#video)

Per configurare l’archivio:

1. Accedi a **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]** > **[!UICONTROL Integrazione AEM]**.

1. Fare clic su **[!UICONTROL Crea configurazione]**.

   ![](assets/aem-admin-settings-1.png)

1. Scegli un metodo di configurazione:

   * Per il repository **[!DNL Adobe Experience Manager Managed Services]**, immettere un nome host del repository che termina con `adobecqms.net` nel campo **[!UICONTROL Nome host del repository AMS]**.

     ![](assets/aem-admin-settings-6.png)

   * Se si utilizza **[!DNL Adobe Experience as a Cloud Service]**, scegliere il repository da configurare e fare clic su **[!UICONTROL Avanti]**.

     Inoltre, puoi fare clic su **[!UICONTROL Visualizza]** per accedere a questo archivio.

     >[!IMPORTANT]
     >
     >Il salvataggio di una nuova configurazione per la stessa organizzazione, sandbox e repository **sostituisce** la configurazione predefinita, ovvero il repository **publish**.

     ![](assets/aem-admin-settings-2.png)

1. Immetti un **[!UICONTROL Nome]** e una **[!UICONTROL Descrizione]**.

1. Scegli la tua configurazione nel menu a discesa seguente:

   +++ Impostazione solo autore

   Selezionare **[!UICONTROL Configurazione solo autore]** quando Journey Optimizer deve leggere i frammenti di contenuto solo dall&#39;ambiente Adobe Experience Manager **Author**. La replica dagli aggiornamenti di authoring a quelli di pubblicazione e pubblicazione in tempo reale non è supportata.

   ![](assets/aem-admin-settings-3.png)

   +++

   </br>

   +++ Impostazione istanza di pubblicazione

   Per impostazione predefinita, ogni repository **[!DNL Adobe Experience Manager as a Cloud Service]** è configurato per l&#39;utilizzo dell&#39;istanza **publish**. Puoi continuare con il passaggio di prova Frammento di contenuto senza modificare queste impostazioni.

   Se l&#39;istanza di pubblicazione è **autenticata** o è necessario utilizzare un dominio di pubblicazione personalizzato, eseguire la procedura seguente.

   1. Seleziona **[!UICONTROL Impostazione istanza di pubblicazione]** per attivare le impostazioni dell&#39;istanza di pubblicazione.

      ![](assets/aem-admin-settings-4.png)

   1. Abilita **[!UICONTROL Invia token all&#39;istanza di pubblicazione]** in modo che le credenziali del servizio siano incluse nelle richieste all&#39;istanza di pubblicazione.

   1. Incolla un **[!UICONTROL JSON]** credenziali servizio valido per l&#39;autenticazione.

   1. Se necessario, fornisci un dominio personalizzato se l&#39;organizzazione non è in grado di raggiungere l&#39;host di pubblicazione predefinito di AEM (`publish-XX-XX.adobeaemcloud.com`) per recuperare il contenuto.

      ![](assets/aem-admin-settings-5.png)

   +++

1. Dopo aver completato la configurazione dell’istanza, scegli un frammento di contenuto per confermare il funzionamento dell’integrazione.

   ![](assets/aem-admin-settings-7.png)

1. Nella finestra **Contenuto verificato**, selezionare il frammento che si desidera verificare, quindi fare clic su **[!UICONTROL Seleziona]**.

1. Fai clic su **[!UICONTROL Salva]**.

1. Quando esegui il salvataggio con un frammento di contenuto di prova selezionato, la convalida viene eseguita automaticamente. Se la convalida non riesce, viene visualizzato un elenco di errori che consente di correggere la configurazione.

   ![](assets/aem-admin-settings-8.png)

1. Per modificare o disabilitare l&#39;integrazione del repository, accedere alla configurazione creata in precedenza dal menu **[!UICONTROL Integrazione AEM]**.

Quando salvi questa configurazione, Journey Optimizer la memorizza per tale archivio nella sandbox corrente. È quindi possibile utilizzare tale repository e le relative impostazioni durante la navigazione e la selezione del contenuto nel selettore **Contenuto verificato**.

## Video introduttivo {#video}

Scopri come gli amministratori configurano le impostazioni dell’archivio Managed Services di Adobe Experience Manager in Journey Optimizer in modo che gli addetti al marketing possano utilizzare i frammenti di contenuto in percorsi e campagne.

>[!VIDEO](https://video.tv.adobe.com/v/3492535?captions=ita&quality=12)
