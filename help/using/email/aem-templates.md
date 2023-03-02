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
source-git-commit: a162f70dceb3bef635085840fc304e0da2c33eed
workflow-type: tm+mt
source-wordcount: '678'
ht-degree: 1%

---

# Utilizzare i modelli di Adobe Experience Manager {#aem-templates}

>[!AVAILABILITY]
>
>L’integrazione con Adobe Experience Manager è attualmente disponibile come versione beta solo per alcuni utenti.
> In qualità di utente beta, utilizza [questo modulo](https://forms.office.com/pages/responsepage.aspx?id=Wht7-jR7h0OUrtLBeN7O4Wf0cbVTQ3tCpW_unE-w8-JUN1FaNlAzNkhPSUdaSkJXVFRCNTRJNVRFSy4u){target="_blank"} per condividere feedback.

Con Adobe Journey Optimizer, puoi creare messaggi personalizzati tramite i siti Adobe Experience Manager. Inizia progettando i modelli utilizzando le origini di contenuto di Adobe Experience Manager, quindi inviali a Adobe Journey Optimizer. Una volta condivisi, questi modelli sono accessibili in E-mail designer di Adobe Journey Optimizer, semplificando il processo di creazione e invio di messaggi al pubblico desiderato.

## Prerequisiti {#prerequisites}

Prima di iniziare a utilizzare questa funzionalità, assicurati di essere in linea con i seguenti requisiti:

* **Impostazioni Experience Manager**

   Questa funzionalità è disponibile a partire da Adobe Experience Manager 6.5.14. Devi connetterti ad Adobe Experience Manager Sites nell’ambiente di authoring di Managed Services.

   Come parte del programma beta, la configurazione del Cloud Service è stata eseguita da Adobe in Adobe Experience Manager per connettersi a Adobe Journey Optimizer.

* **Autorizzazioni**

   Per creare, modificare ed eliminare modelli di contenuto in Adobe Journey Optimizer, è necessario disporre del **[!DNL Manage Library Items]** autorizzazione inclusa nel **[!DNL Content Library Manager]** profilo di prodotto. [Ulteriori informazioni](../administration/ootb-product-profiles.md#content-library-manager)


## Guardrail e limitazioni{#aem-templates-limitations}

Per ottimizzare ulteriormente l’utilizzo di Adobe Experience Manager con Adobe Journey Optimizer, è importante essere consapevoli delle seguenti protezioni e limitazioni aggiuntive:

* Il modello di Experience Manager non deve contenere personalizzazioni. La personalizzazione deve essere eseguita solo in Journey Optimizer.

* L’esportazione di modelli in blocco non è attualmente supportata, i modelli devono essere esportati singolarmente.

* La sincronizzazione tra Experience Manager e Journey Optimizer non è attualmente disponibile. Se vengono apportate modifiche a un modello di Experience Manager dopo che è stato inviato a Journey Optimizer, l’utente dovrà riesportare il modello e inviarlo di nuovo a Journey Optimizer.

## Inviare un modello a Journey Optimizer{#aem-templates-send}

Per esportare un modello di Adobe Experience Manager in Adobe Journey Optimizer, effettua le seguenti operazioni:

1. Dalla home page di Adobe Experience Manager, seleziona la **[!UICONTROL Marketing in uscita]**.

   ![](assets/aem-outbound-menu.png)

1. Accedi alla libreria dei contenuti e seleziona il modello da esportare in Journey Optimizer.

   Puoi anche creare una nuova pagina da zero. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/experience-manager-65/authoring/authoring/managing-pages.html?lang=en#creating-a-new-page)

   ![](assets/aem-send-template.png)

1. Dopo aver selezionato il modello, seleziona **[!UICONTROL Invia a]** dal menu avanzato.

   ![](assets/aem-advanced-menu.png)

1. Inserisci il **[!UICONTROL Nome]** del modello di contenuto e selezionare la destinazione **[!UICONTROL Sandbox]**.

   ![](assets/aem-send-template-settings.png)

1. Dopo aver fatto clic su **[!UICONTROL Invia]** , verrà avviato il processo di esportazione. Una volta completata l’esportazione, viene visualizzato il seguente messaggio nell’interfaccia utente: &quot;Modello &quot;XX&quot; inviato correttamente ad AJO&quot;.

Il modello viene aggiunto ai modelli di contenuto Adobe Journey Optimizer della sandbox selezionata.

## Utilizzare e personalizzare un modello di Adobe Experience Manager{#aem-templates-perso}

Una volta che il modello di Experience Manager è disponibile in Journey Optimizer come modello di contenuto, puoi identificare e incorporare il contenuto necessario per l’e-mail, inclusa la personalizzazione.

1. In Journey Optimizer, da **[!UICONTROL Modello di contenuto]** accedere al modello importato.

   ![](assets/aem_ajo_1.png)

1. Facendo clic su **[!UICONTROL Avviso]** , è possibile verificare rapidamente se mancano impostazioni importanti. In questo modo potrai verificare che i messaggi siano configurati correttamente e prevenire potenziali errori o problemi.

   ![](assets/aem_ajo_2.png)

1. In **[!UICONTROL Proprietà modello]** , fare clic sul pulsante **[!UICONTROL Gestisci accesso]** per assegnare etichette di utilizzo dei dati personalizzate o di base al modello. [Ulteriori informazioni su OLAC (Object Level Access Control)](../administration/object-based-access.md)

1. Per personalizzare ulteriormente il modello AEM e aggiungere una personalizzazione al contenuto, fai clic su **[!UICONTROL Modifica contenuto]**. In questo modo è possibile apportare facilmente modifiche e adattare il modello alle proprie esigenze specifiche. [Ulteriori informazioni](get-started-email-design.md)

   >[!NOTE]
   >
   > Se desideri modificare e personalizzare il modello, potrai utilizzare solo la modalità di compatibilità.

1. Quando il modello di contenuto è pronto, [testarlo e convalidarlo](content-templates.md#test-template).

1. Una volta definiti i contenuti, puoi utilizzarli durante la creazione di una nuova e-mail sfogliando il **[!UICONTROL Modelli salvati]** raccolta. Quindi, seleziona **[!UICONTROL Usa questo modello]**.

   Scopri come modificare e personalizzare un contenuto e-mail in [questa sezione](content-from-scratch.md).

   ![](assets/aem_ajo_3.png)

Quando l’e-mail è pronta, completa la configurazione del [percorso](../building-journeys/journey-gs.md) o [campagna](../campaigns/create-campaign.md)e attivarlo per inviare il messaggio.
