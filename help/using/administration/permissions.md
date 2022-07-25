---
title: Gestione di utenti e profili di prodotto
description: Scopri come gestire le autorizzazioni.
exl-id: 85fd386a-45fa-4f9a-89d1-cecc0749b90d
feature: Access Management
topic: Administration
role: Admin
level: Intermediate
source-git-commit: 0e978d0eab570a28c187f3e7779c450437f16cfb
workflow-type: tm+mt
source-wordcount: '722'
ht-degree: 14%

---

# Gestione di utenti e profili di prodotto {#manage-permissions}

>[!IMPORTANT]
>
> Ognuna delle procedure descritte qui di seguito può essere eseguita solo da un **[!UICONTROL Product]** o **[!UICONTROL System]** amministratore. Per ulteriori informazioni, consulta la [Documentazione di Admin Console](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/admin-roles.ug.html).

**[!UICONTROL Product profiles]** sono set di utenti che condividono le stesse autorizzazioni e sandbox all’interno della tua organizzazione.

La [!DNL Journey Optimizer] product ti consente di scegliere tra diverse opzioni predefinite **[!UICONTROL Product profiles]** con diversi livelli di autorizzazioni da assegnare agli utenti. Per ulteriori informazioni sui **[!UICONTROL Product profiles]**, fai riferimento a [page](ootb-product-profiles.md).

Ogni utente appartenente a un **[!UICONTROL Product profiles]** ha diritto alle app e ai servizi di Adobe contenuti nel prodotto.

Puoi anche creare un tuo **[!UICONTROL Product profiles]** per ottimizzare l’accesso degli utenti a determinate funzionalità o oggetti dell’interfaccia.

## Assegnazione di un profilo di prodotto {#assigning-product-profile}

Puoi scegliere di assegnare un predefinito o personalizzato **[!UICONTROL Product profile]** agli utenti.

L’elenco di tutti i profili di prodotto predefiniti con autorizzazioni assegnate è disponibile nella sezione [Profili di prodotto incorporati](ootb-product-profiles.md) sezione .

Per assegnare un **[!UICONTROL Product profile]**:

1. In [!DNL Admin Console], dal **[!UICONTROL Products]** seleziona la scheda **[!UICONTROL Experience Cloud - Platform powered applications]** prodotto.

1. Seleziona un **[!UICONTROL Product profile]**.

   ![](assets/do-not-localize/access_control_2.png)

1. Dalla scheda **[!UICONTROL Users]**, fai clic su **[!UICONTROL Add user]**.

   ![](assets/do-not-localize/access_control_3.png)

1. Digita il nome o l’indirizzo e-mail dell’utente e seleziona l’utente.

   Se l&#39;utente non è stato creato in precedenza nel [!DNL Admin Console], fare riferimento alla [Aggiungere la documentazione degli utenti](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html#add-users).

   ![](assets/do-not-localize/access_control_4.png)

1. Esegui gli stessi passaggi di cui sopra per aggiungere altri utenti al tuo **[!UICONTROL Product profile]**. Quindi, fai clic su **[!UICONTROL Save]**.

L’utente dovrebbe quindi ricevere un messaggio e-mail di reindirizzamento all’istanza.

Per ulteriori informazioni sulla gestione degli utenti, consulta [Documentazione di Admin Console](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html).

Quando si accede all’istanza, l’utente visualizza una visualizzazione specifica a seconda delle autorizzazioni assegnate nel **[!UICONTROL Product profile]**. Se l’utente non ha il diritto di accesso a una funzione, verrà visualizzato il seguente messaggio:

`You don't have permission to access this feature. Permission needed: XX.`

## Modifica di un profilo di prodotto esistente {#edit-product-profile}

Per predefiniti o personalizzati **[!UICONTROL Product profiles]**, puoi decidere in qualsiasi momento di aggiungere o eliminare autorizzazioni.

In questo esempio, vogliamo aggiungere **[!UICONTROL Permissions]** relativa al **[!UICONTROL Journeys]** funzionalità per gli utenti assegnati al visualizzatore di Percorsi **[!UICONTROL Product profile]**. Gli utenti potranno quindi pubblicare percorsi.

Tieni presente che se modifichi un predefinito o personalizzato **[!UICONTROL Product profile]**, interesserà ogni utente assegnato a questo **[!UICONTROL Product profile]**.

1. In [!DNL Admin Console], dal **[!UICONTROL Products]** seleziona la scheda **[!UICONTROL Experience Cloud - Platform powered applications]** prodotto.

1. Selezionare il visualizzatore Percorso **[!UICONTROL Product profile]**.

1. Seleziona la scheda **[!UICONTROL Permissions]**.

   La **[!UICONTROL Permissions]** visualizza l’elenco delle funzionalità applicabili al **[!UICONTROL Experience Cloud - Platform powered applications]** prodotto.

   ![](assets/do-not-localize/access_control_5.png)

1. Seleziona la **[!UICONTROL Journeys]** funzionalità.

   ![](assets/do-not-localize/access_control_6.png)

1. Da **[!UICONTROL Available Permission Items]** selezionare le autorizzazioni da assegnare al **[!UICONTROL Product profile]** facendo clic sull’icona più (+).

   Qui, aggiungiamo la **[!UICONTROL Publish Journeys]** autorizzazione.

1. Se necessario, in **[!UICONTROL Included Permission Items]**, fai clic sull’icona X adiacente alla rimozione delle autorizzazioni dal tuo profilo di prodotto.

1. Al termine, fai clic su **[!UICONTROL Save]**.

Se necessario, puoi anche creare un nuovo profilo di prodotto con autorizzazioni specifiche. Per ulteriori informazioni, consulta [Creazione di un profilo di prodotto](#create-product-profile).

## Creazione di un profilo di prodotto {#create-product-profile}

[!DNL Journey Optimizer] consente di creare **[!UICONTROL Product profiles]** e assegna agli utenti un set di autorizzazioni e sandbox. Con **[!UICONTROL Product profiles]**, puoi autorizzare o negare l’accesso a determinate funzionalità o oggetti nell’interfaccia.

Per ulteriori informazioni su come creare e gestire le sandbox, consulta [Documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html?lang=it){target=&quot;_blank&quot;}.

In questo esempio, creeremo un profilo di prodotto denominato **Percorsi in sola lettura** in cui concederemo diritti di sola lettura alla funzione Percorso. Gli utenti potranno accedere e visualizzare solo i percorsi e non potranno accedere ad altre funzioni quali **[!DNL  Decision management]** in [!DNL Journey Optimizer].

Per creare la nostra **Percorsi in sola lettura** **[!UICONTROL product profiles]**:

1. Accedere al [!DNL Admin Console].

1. Da **[!UICONTROL Products]** seleziona la scheda **[!UICONTROL Experience Cloud - Platform powered applications]** prodotto.

1. Fai clic su **[!UICONTROL New Profile]**.

   ![](assets/do-not-localize/access_control_9.png)

1. Aggiungi un **[!UICONTROL Product Profile Name]**, **[!UICONTROL Display Name]** e **[!UICONTROL Description]** per il tuo nuovo **[!UICONTROL product profiles]**.

   ![](assets/do-not-localize/access_control_10.png)

1. Nella categoria **[!UICONTROL Notifications]**, scegli di informare gli utenti via e-mail, quando verranno aggiunti o rimossi da questo profilo di prodotto.

1. Al termine, fai clic su **[!UICONTROL Save]** e seleziona la nuova **[!UICONTROL product profiles]**.

1. Per aggiungere le autorizzazioni per gli utenti per accedere a funzioni diverse, seleziona la **[!UICONTROL Permissions]** scheda .

1. Selezionare tra le diverse funzionalità, ad esempio **[!DNL Journeys]**, **[!DNL Segments]** o **[!DNL Decision management]** disponibile in [!DNL Journey Optimizer] elencati nel menu a sinistra.

   Qui selezioniamo il **[!UICONTROL Journeys]** funzionalità.

   ![](assets/do-not-localize/access_control_11.png)

1. Da **[!UICONTROL Available Permission Items]** selezionare le autorizzazioni da assegnare al **[!UICONTROL Product profile]** facendo clic sull’icona più (+).

   Qui selezioniamo **[!DNL View journeys]** e **[!DNL View journeys event, data sources, actions]**.

   ![](assets/do-not-localize/access_control_12.png)

1. Seleziona la **[!UICONTROL Sandbox access]** capacità di scegliere quali sandbox assegnare al **[!UICONTROL Product profile]**.

   ![](assets/do-not-localize/access_control_13.png)

1. Nella sezione **[!UICONTROL Available Permissions Items]**, fai clic sull’icona più (+) per assegnare le sandbox al profilo. [Ulteriori informazioni sulle sandbox](sandboxes.md).

1. Al termine, fai clic su **[!UICONTROL Save]**.

Le **[!UICONTROL Product profile]** viene ora creato e configurato. Ora devi assegnarlo agli utenti.

Per ulteriori informazioni sulla creazione e la gestione del profilo di prodotto, consulta [Documentazione di Admin Console](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-product-profiles.ug.html).
