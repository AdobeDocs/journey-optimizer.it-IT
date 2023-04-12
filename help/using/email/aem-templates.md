---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare i modelli AEM
description: Scopri come creare modelli in AEM ed esportarli in Journey Optimizer
hide: true
hidefromtoc: true
feature: Overview
topic: Content Management
role: User
level: Beginner
badge: label="Beta" type="Informativo"
source-git-commit: 7a044f7c048ba797e7b857212f6d6b0cf2644b5d
workflow-type: tm+mt
source-wordcount: '769'
ht-degree: 1%

---

# Utilizzare i modelli di Adobe Experience Manager {#aem-templates}

>[!AVAILABILITY]
>
>L&#39;integrazione con Adobe Experience Manager è attualmente disponibile come versione beta solo per alcuni utenti.
> Come utente beta, utilizza [questo modulo](https://forms.office.com/pages/responsepage.aspx?id=Wht7-jR7h0OUrtLBeN7O4Wf0cbVTQ3tCpW_unE-w8-JUN1FaNlAzNkhPSUdaSkJXVFRCNTRJNVRFSy4u){target="_blank"} per condividere il feedback.

Con Adobe Journey Optimizer puoi creare messaggi personalizzati tramite i siti Adobe Experience Manager. Inizia progettando i modelli utilizzando le origini di contenuto di Adobe Experience Manager, quindi inviali a Adobe Journey Optimizer. Una volta condivisi, questi modelli sono accessibili in e-mail designer Adobe Journey Optimizer, semplificando il processo di creazione e invio di messaggi al pubblico desiderato.

## Prerequisiti {#prerequisites}

Prima di iniziare a utilizzare questa funzionalità, assicurati di essere allineato ai seguenti requisiti:

* **Impostazioni Experience Manager**

   Questa funzionalità è disponibile con [Adobe Experience Manager as a Cloud Service](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/overview/introduction.html){target="_blank"}.

   Come parte del programma beta, la configurazione del Cloud Service viene eseguita da Adobe in Adobe Experience Manager per la connessione a Adobe Journey Optimizer.

* **Autorizzazioni**

   Per creare, modificare ed eliminare modelli di contenuto in Adobe Journey Optimizer, è necessario disporre dei **[!DNL Manage Library Items]** autorizzazione inclusa nel **[!DNL Content Library Manager]** profilo di prodotto. [Ulteriori informazioni](../administration/ootb-product-profiles.md#content-library-manager)

## Guardrail e limitazioni{#aem-templates-limitations}

Per ottimizzare ulteriormente l’utilizzo di Adobe Experience Manager con Adobe Journey Optimizer, è importante conoscere le seguenti protezioni e limitazioni aggiuntive:

* Per rendere effettiva la personalizzazione nel modello di Experience Manager, è necessaria una sintassi Journey Optimizer corretta. [Ulteriori informazioni](../personalization/personalization-syntax.md)

* L’esportazione dei modelli di massa non è attualmente supportata. I modelli devono essere esportati singolarmente.

* La sincronizzazione tra Experience Manager e Journey Optimizer non è attualmente disponibile. Se dopo l’invio a Journey Optimizer vengono apportate modifiche a un modello di Experience Manager, l’utente dovrà riesportare il modello e inviarlo nuovamente a Journey Optimizer.

## Inviare un modello a Journey Optimizer{#aem-templates-send}

Per esportare un modello Adobe Experience Manager in Adobe Journey Optimizer, segui i passaggi seguenti:

1. Dalla home page di Adobe Experience Manager, seleziona la **[!UICONTROL Marketing in uscita]**.

   ![](assets/aem-outbound-menu.png)

1. Dalla libreria dei contenuti, puoi utilizzare modelli configurati in precedenza o crearne uno da zero. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/authoring/managing-pages.html?lang=en#creating-a-new-page)

1. Incorporando la sintassi di personalizzazione Journey Optimizer nel modello, puoi migliorarne le funzionalità di personalizzazione. [Ulteriori informazioni](../personalization/personalization-syntax.md)

   ![](assets/aem_ajo_4.png)

1. Seleziona il modello da esportare in Journey Optimizer e fai clic su **[!UICONTROL Invia a]** dal menu avanzato.

   ![](assets/aem-advanced-menu.png)

1. Inserisci il **[!UICONTROL Nome]** del modello Contenuto e seleziona la destinazione **[!UICONTROL Sandbox]**.

   ![](assets/aem-send-template-settings.png)

1. Dopo aver fatto clic su **[!UICONTROL Invia]** il processo di esportazione inizierà. Al termine dell’esportazione, nell’interfaccia utente viene visualizzato il seguente messaggio: &quot;Modello &quot;XX&quot; inviato correttamente ad AJO&quot;.

Il modello viene aggiunto ai modelli di contenuto Adobe Journey Optimizer della sandbox selezionata.

## Utilizzare e personalizzare un modello Adobe Experience Manager{#aem-templates-perso}

Una volta che il modello di Experience Manager è disponibile in Journey Optimizer come modello di contenuto, puoi identificare e incorporare il contenuto necessario per l’e-mail, inclusa la personalizzazione.

1. In Journey Optimizer, dal **[!UICONTROL Modello di contenuto]** accedere al modello importato.

   ![](assets/aem_ajo_1.png)

1. Facendo clic sul pulsante **[!UICONTROL Avviso]** è possibile verificare rapidamente se mancano impostazioni importanti. In questo modo potrai verificare che i messaggi siano configurati correttamente ed evitare potenziali errori o problemi.

   ![](assets/aem_ajo_2.png)

1. In **[!UICONTROL Proprietà del modello]** fai clic su **[!UICONTROL Gestisci accesso]** per assegnare etichette di utilizzo dati personalizzate o di base al modello. [Ulteriori informazioni su Object Level Access Control (OLAC)](../administration/object-based-access.md)

1. Per personalizzare ulteriormente il modello di Experience Manager e aggiungere una personalizzazione personalizzata al contenuto, fai clic su **[!UICONTROL Modifica contenuto]**. Questo ti consente di apportare facilmente modifiche e adattare il modello alle tue esigenze specifiche. [Ulteriori informazioni](get-started-email-design.md)

   >[!NOTE]
   >
   > Se desideri modificare e personalizzare il modello, puoi utilizzare solo la modalità di compatibilità .

1. Quando il modello di contenuto è pronto, [verificarlo e convalidarlo](content-templates.md#test-template).

1. Una volta definito il contenuto, puoi utilizzarlo durante la creazione di nuove e-mail sfogliando il **[!UICONTROL Modelli salvati]** raccolta. Quindi, seleziona **[!UICONTROL Utilizza questo modello]**.

   ![](assets/aem_ajo_3.png)

1. Ora puoi modificare e personalizzare il contenuto. Per ulteriori informazioni su come generare il contenuto delle e-mail, consulta questo [page](content-from-scratch.md).

   ![](assets/aem_ajo_5.png)

1. Se hai aggiunto contenuto personalizzato al modello di Experience Manager, fai clic su **[!UICONTROL Simula contenuto]** per visualizzare in anteprima come verrà visualizzato nel messaggio utilizzando i profili di test.

[Ulteriori informazioni sui profili di anteprima e di test](../email/preview.md)

   ![](assets/aem_ajo_6.png)

1. Quando visualizzi l’anteprima del messaggio, tutti gli elementi personalizzati vengono sostituiti automaticamente con i dati corrispondenti dal profilo di test selezionato.

   Se necessario, è possibile aggiungere ulteriori profili di test tramite la **[!UICONTROL Gestire i profili di test]** pulsante .

   ![](assets/aem_ajo_7.png)

Quando il tuo messaggio e-mail è pronto, completa la configurazione del tuo [percorso](../building-journeys/journey-gs.md) o [campagna](../campaigns/create-campaign.md), e attivalo per inviare il messaggio.
