---
solution: Journey Optimizer
product: journey optimizer
title: Gestione di utenti e profili di prodotto
description: Scopri come gestire utenti e profili di prodotto
exl-id: 85fd386a-45fa-4f9a-89d1-cecc0749b90d
feature: Access Management
topic: Administration
role: Admin
level: Intermediate
keywords: product, profiles, sandbox
source-git-commit: 16738786e4ebeef3417fd0f6e5be741b348c2744
workflow-type: tm+mt
source-wordcount: '838'
ht-degree: 8%

---

# Gestione di utenti e profili di prodotto {#manage-permissions}

>[!IMPORTANT]
>
> Ciascuna delle procedure descritte di seguito può essere eseguita soltanto da un **[!UICONTROL Prodotto]** o **[!UICONTROL Sistema]** amministratore. Per ulteriori informazioni, consulta [Documentazione di Admin Console](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/admin-roles.ug.html).

**[!UICONTROL Profili di prodotto]** sono set di utenti che condividono le stesse autorizzazioni e sandbox all’interno dell’organizzazione.

Il [!DNL Journey Optimizer] consente di scegliere tra diversi **[!UICONTROL Profili di prodotto]** con diversi livelli di autorizzazioni da assegnare agli utenti. Per ulteriori informazioni sulle **[!UICONTROL Profili di prodotto]**, fai riferimento a questo [pagina](ootb-product-profiles.md).

Ogni utente appartenente a un **[!UICONTROL Profili di prodotto]** ha diritto alle app e ai servizi di Adobe contenuti nel prodotto.

Puoi anche creare **[!UICONTROL Profili di prodotto]** se desideri ottimizzare l’accesso degli utenti a determinate funzionalità o oggetti nell’interfaccia.

## Assegnazione di un profilo di prodotto {#assigning-product-profile}

È possibile scegliere di assegnare un **[!UICONTROL Profilo di prodotto]** ai tuoi utenti.

L’elenco di tutti i profili di prodotto predefiniti con autorizzazioni assegnate è disponibile nella sezione [Profili di prodotto incorporati](ootb-product-profiles.md) sezione.

Per assegnare un **[!UICONTROL Profilo di prodotto]**:

1. In [!DNL Admin Console], dalla **[!UICONTROL Prodotti]** , seleziona la scheda **[!UICONTROL Experience Cloud: applicazioni basate su piattaforma]** prodotto.

1. Seleziona un **[!UICONTROL Profilo di prodotto]**.

   ![](assets/do-not-localize/access_control_2.png)

1. Dalla sezione **[!UICONTROL Utenti]** , fare clic su **[!UICONTROL Aggiungi utente]**.

   ![](assets/do-not-localize/access_control_3.png)

1. Digita il nome o l’indirizzo e-mail dell’utente e selezionalo.

   Se l&#39;utente non è stato creato in precedenza in [!DNL Admin Console], fare riferimento a [Aggiungi documentazione utenti](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html#add-users).

   ![](assets/do-not-localize/access_control_4.png)

1. Effettua gli stessi passaggi di cui sopra per aggiungere altri utenti al tuo **[!UICONTROL Profilo di prodotto]**. Quindi, fai clic su **[!UICONTROL Salva]**.

L’utente dovrebbe quindi ricevere un messaggio e-mail di reindirizzamento all’istanza.

Per ulteriori informazioni sulla gestione degli utenti, consulta [Documentazione di Admin Console](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html).

Quando accedi all’istanza, l’utente visualizzerà una visualizzazione specifica a seconda delle autorizzazioni assegnate nella sezione **[!UICONTROL Profilo di prodotto]**. Se l’utente non dispone del diritto di accesso a una funzione, viene visualizzato il seguente messaggio:

`You don't have permission to access this feature. Permission needed: XX.`

## Modifica di un profilo di prodotto esistente {#edit-product-profile}

Per preconfigurati o personalizzati **[!UICONTROL Profili di prodotto]**, puoi decidere in qualsiasi momento di aggiungere o eliminare le autorizzazioni.

In questo esempio, desideri aggiungere **[!UICONTROL Autorizzazioni]** relativo al **[!UICONTROL Percorsi]** funzionalità per gli utenti assegnati al visualizzatore Percorso **[!UICONTROL Profilo di prodotto]**. Gli utenti potranno quindi pubblicare i percorsi.

Tieni presente che se modifichi una **[!UICONTROL Profilo di prodotto]**, avrà un impatto su tutti gli utenti assegnati a questo **[!UICONTROL Profilo di prodotto]**.

1. In [!DNL Admin Console], dalla **[!UICONTROL Prodotti]** , seleziona la scheda **[!UICONTROL Experience Cloud: applicazioni basate su piattaforma]** prodotto.

1. Seleziona il visualizzatore di Percorso **[!UICONTROL Profilo di prodotto]**.

1. Fai clic sulla scheda **[!UICONTROL Autorizzazioni.]**

   Il **[!UICONTROL Autorizzazioni]** visualizza l’elenco delle funzionalità che si applicano al **[!UICONTROL Experience Cloud: applicazioni basate su piattaforma]** prodotto.

   ![](assets/do-not-localize/access_control_5.png)

1. Seleziona la **[!UICONTROL Percorsi]** funzionalità.

   ![](assets/do-not-localize/access_control_6.png)

1. Dalla sezione **[!UICONTROL Elementi di autorizzazione disponibili]** selezionare le autorizzazioni da assegnare al proprio **[!UICONTROL Profilo di prodotto]** facendo clic sull&#39;icona più (+).

   In questo caso, aggiungiamo **[!UICONTROL Pubblica Percorsi]** autorizzazione.

1. Se necessario, in **[!UICONTROL Elementi autorizzazione inclusi]**, fai clic sull’icona X accanto a rimuovere le autorizzazioni per il tuo profilo di prodotto.

1. Al termine, fai clic su **[!UICONTROL Salva]**.

Se necessario, puoi anche creare un nuovo profilo di prodotto con autorizzazioni specifiche. Per ulteriori informazioni, consulta [Creazione di un profilo di prodotto](#create-product-profile).

## Creazione di un profilo di prodotto {#create-product-profile}

[!DNL Journey Optimizer] consente di creare **[!UICONTROL Profili di prodotto]** e assegna un set di autorizzazioni e sandbox agli utenti. Con **[!UICONTROL Profili di prodotto]**, puoi autorizzare o negare l’accesso a determinate funzionalità o oggetti nell’interfaccia.

Per ulteriori informazioni sulla modalità di creazione e di gestione delle sandbox, consulta la [documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html?lang=it){target="_blank"}.

In questo esempio, creeremo un profilo di prodotto denominato **Percorsi di sola lettura** dove verranno concessi diritti di sola lettura per la funzione di Percorso. Gli utenti potranno solo accedere ai percorsi e visualizzarli e non potranno accedere ad altre funzioni, come **[!DNL  Decision management]** in [!DNL Journey Optimizer].

Per creare **Percorsi di sola lettura** **[!UICONTROL profili di prodotto]**:

1. Accedere a [!DNL Admin Console].

1. Dalla sezione **[!UICONTROL Prodotti]** , seleziona la scheda **[!UICONTROL Experience Cloud: applicazioni basate su piattaforma]** prodotto.

1. Fai clic su **[!UICONTROL Nuovo profilo]**.

   ![](assets/do-not-localize/access_control_9.png)

1. Aggiungi un **[!UICONTROL Nome profilo prodotto]**, **[!UICONTROL Nome visualizzato]** e **[!UICONTROL Descrizione]** per il tuo nuovo **[!UICONTROL profili di prodotto]**.

   ![](assets/do-not-localize/access_control_10.png)

1. In **[!UICONTROL Notifiche]** categoria, scegli se gli utenti riceveranno una notifica tramite e-mail quando vengono aggiunti o rimossi da questo profilo di prodotto.

1. Al termine, fai clic su **[!UICONTROL Salva]** e seleziona il nuovo **[!UICONTROL profili di prodotto]**.

1. Per aggiungere le autorizzazioni di accesso alle diverse funzioni per gli utenti, selezionare **[!UICONTROL Autorizzazioni]** scheda.

1. Scegli tra le diverse funzionalità, ad esempio **[!DNL Journeys]**, **[!DNL Segments]** o **[!DNL Decision management]** disponibile in [!DNL Journey Optimizer] nel menu a sinistra.

   In questo punto selezioniamo il **[!UICONTROL Percorsi]** funzionalità.

   ![](assets/do-not-localize/access_control_11.png)

1. Dalla sezione **[!UICONTROL Elementi di autorizzazione disponibili]** selezionare le autorizzazioni da assegnare al proprio **[!UICONTROL Profilo di prodotto]** facendo clic sull&#39;icona più (+).

   Qui selezioniamo **[!DNL View journeys]** e **[!DNL View journeys event, data sources, actions]**.

   ![](assets/do-not-localize/access_control_12.png)

1. Seleziona la **[!UICONTROL Accesso alla sandbox]** possibilità di scegliere le sandbox da assegnare al **[!UICONTROL Profilo di prodotto]**.

   ![](assets/do-not-localize/access_control_13.png)

1. Sotto **[!UICONTROL Elementi di autorizzazione disponibili]**, fai clic sull’icona più (+) per assegnare le sandbox al profilo. [Ulteriori informazioni sulle sandbox](sandboxes.md).

1. Al termine, fai clic su **[!UICONTROL Salva]**.

Il tuo **[!UICONTROL Profilo di prodotto]** viene ora creato e configurato. Ora devi assegnarla agli utenti.

Per ulteriori informazioni sulla creazione e la gestione del profilo di prodotto, consulta [Documentazione di Admin Console](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-product-profiles.ug.html).
