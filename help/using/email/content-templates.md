---
solution: Journey Optimizer
product: journey optimizer
title: Creare modelli di contenuto
description: Scopri come creare modelli per riutilizzare i contenuti nelle campagne e nei percorsi Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
source-git-commit: 4df89a36705fb53984ba04ba1ae2f45554e47f77
workflow-type: tm+mt
source-wordcount: '604'
ht-degree: 2%

---

# Creare modelli di contenuto {#content-templates}

>[!CONTEXTUALHELP]
>id="ajo_content_templates"
>title="Creare modelli di contenuto"
>abstract="Crea modelli indipendenti per riutilizzare i contenuti tra percorsi e campagne."

Per un processo di progettazione più ampio e migliorato, è possibile creare modelli indipendenti per riutilizzare facilmente contenuti personalizzati in [!DNL Journey Optimizer] campagne e percorsi.

Questa funzionalità consente agli utenti orientati ai contenuti di lavorare su modelli esterni a campagne o percorsi. Gli utenti di marketing possono quindi riutilizzare e adattare questi modelli di contenuto indipendenti all’interno dei propri percorsi o campagne.

>[!CAUTION]
>
>Per creare, modificare ed eliminare modelli di contenuto, è necessario disporre dei **[!DNL Manage Library Items]** autorizzazione inclusa nel **[!DNL Content Library Manager]** profilo di prodotto. [Ulteriori informazioni](../administration/ootb-product-profiles.md#content-library-manager)

Ad esempio, un utente all’interno dell’azienda è responsabile solo del contenuto e pertanto non ha accesso a campagne o percorsi. Tuttavia, questo utente può creare un modello e-mail che gli addetti al marketing della tua organizzazione potranno selezionare per l’uso in tutte le e-mail come punto di partenza.

>[!NOTE]
>
>* Le modifiche apportate ai modelli di contenuto non vengono propagate a campagne o percorsi, siano essi in diretta o in bozza.
>
>* Allo stesso modo, quando i modelli vengono utilizzati in una campagna o in un percorso, le modifiche apportate al contenuto della campagna e del percorso non influiscono sul modello di contenuto utilizzato in precedenza.


➡️ [Scopri come creare e utilizzare i modelli in questo video](#video-templates)

Per creare un modello di contenuto, effettua le seguenti operazioni.

1. Per accedere all’elenco dei modelli di contenuto, seleziona **[!UICONTROL Gestione dei contenuti]** > **[!UICONTROL Modelli di contenuto]** dal menu a sinistra.

   ![](assets/content-template-list.png)

1. Tutti i modelli creati nella sandbox corrente, da un percorso, una campagna o dalla **[!UICONTROL Modelli di contenuto]** menu - vengono visualizzati.

   >[!NOTE]
   >
   >Puoi ordinare i modelli di contenuto per creazione o data di modifica.

1. Seleziona **[!UICONTROL Crea modello]**.

1. Compila i dettagli del modello.

   ![](assets/content-template-details.png)

   >[!NOTE]
   >
   >Attualmente solo il **E-mail** canale e **HTML** sono supportati.

1. Per assegnare etichette di utilizzo dati personalizzate o di base al modello, seleziona **[!UICONTROL Gestisci accesso]**. [Ulteriori informazioni su Object Level Access Control (OLAC)](../administration/object-based-access.md).

1. Fai clic su **[!UICONTROL Crea]** e scegli come desideri progettare il tuo messaggio e-mail dalle seguenti opzioni:

   * **[!UICONTROL Progettazione da zero]**
   * **[!UICONTROL Codice personalizzato]**
   * **[!UICONTROL Importa HTML]**
   * **[!UICONTROL Seleziona modello di progettazione]**

   ![](assets/content-template-design.png)

   >[!NOTE]
   >
   >Se selezioni un modello, puoi scegliere tra **[!UICONTROL Modelli di esempio]**, che sono modelli e-mail preconfigurati, e **[!UICONTROL Modelli salvati]**, ovvero quelli creati da un percorso, una campagna o da **[!UICONTROL Modelli di contenuto]** menu. [Ulteriori informazioni](email-templates.md#save-as-template)

1. Viene visualizzato E-mail Designer . Modifica il contenuto in base alle esigenze, nello stesso modo che faresti per qualsiasi e-mail all’interno di un percorso o di una campagna, in base all’opzione selezionata:

   * [Progettazione dell&#39;e-mail da zero](content-from-scratch.md) tramite l&#39;interfaccia del designer e sfruttando le immagini [Adobe Experience Manager Assets Essentials](assets-essentials.md).

   * [Codice o copia-incolla raw HTML](code-content.md) direttamente in E-mail Designer.

   * [Importare contenuto HTML esistente](existing-content.md) da un file o da una cartella .zip.

   * [Usa contenuto esistente](email-templates.md) da un elenco di modelli predefiniti o personalizzati.

   ![](assets/content-template-designer.png)

1. Fai clic su **[!UICONTROL Simula contenuto]** per controllare il rendering delle e-mail. È possibile scegliere la visualizzazione su desktop o dispositivo mobile. [Ulteriori informazioni](preview.md)

   >[!CAUTION]
   >
   >Per simulare il contenuto, è necessario disporre della **[!DNL Manage Simulate Content]** autorizzazione inclusa nel **[!DNL Content Library Manager]** profilo di prodotto. [Ulteriori informazioni](../administration/ootb-product-profiles.md#content-library-manager)

   ![](assets/content-template-stimulate.png)

1. Puoi inviare una bozza per testare il contenuto e farla approvare da alcuni utenti interni prima di utilizzarla in un percorso o in una campagna.

   * A tale scopo, fai clic sul pulsante **[!UICONTROL Invia bozza]** e segui i passaggi descritti in [questa sezione](preview.md#send-proofs).

   * Prima di inviare la bozza, devi selezionare la [superficie e-mail](../configuration/channel-surfaces.md) che verrà utilizzato per testare il contenuto.

      ![](assets/content-template-stimulate-proof-surface.png)

1. Una volta pronto il modello, fai clic su **[!UICONTROL Salva]**.

1. Se necessario, fai clic sulla freccia accanto al nome del modello per tornare al **[!UICONTROL Dettagli]** visualizza e modifica il modello.

   ![](assets/content-template-designer-back.png)

1. È ora possibile utilizzare questo modello di contenuto durante la creazione di qualsiasi [email](get-started-email-design.md) entro [!DNL Journey Optimizer]. Ulteriori informazioni su [utilizzo di un modello salvato](email-templates.md#use-saved-template).

   ![](assets/email_designer-saved-templates.png)

## Video introduttivo{#video-templates}

Scopri come creare, modificare e utilizzare modelli di contenuto in [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/3413743/?quality=12)