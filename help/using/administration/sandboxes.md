---
title: Gestione delle sandbox
description: Scopri come gestire le sandbox
feature: Sandboxes
topic: Administration
role: Admin
level: Intermediate
exl-id: 14f80d5d-0840-4b79-9922-6d557a7e1247
source-git-commit: 7da910df3eda84884c7cda56af6ce5dcabc3a3db
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 66%

---

# Gestione delle sandbox {#sandboxes}

## Utilizzare le sandbox {#using-sandbox}

[!DNL Journey Optimizer] consente di suddividere l’istanza in ambienti virtuali separati, denominati sandbox.
Le sandbox vengono assegnate tramite i profili di prodotto nella Admin Console. [Scopri come assegnare le sandbox](permissions.md#create-product-profile).

[!DNL Journey Optimizer] presenta le sandbox di Adobe Experience Platform che sono state create per una determinata organizzazione.
Le sandbox di Adobe Experience Platform possono essere create o reimpostate dall’istanza di Adobe Experience Platform. [Ulteriori informazioni nella guida utente della sandbox](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html?lang=it){target=&quot;_blank&quot;}.

Puoi trovare il controllo del commutatore sandbox in alto a destra nella schermata accanto al nome della tua organizzazione. Per passare da una sandbox all’altra, fai clic sulla sandbox attualmente attiva nel commutatore e selezionane un’altra dall’elenco a discesa.

![](../assets/sandbox_5.png)

➡️ [Scopri questa funzione nel video](#video)

## Assegnare le sandbox {#assign-sandboxes}

>[!IMPORTANT]
>
> La gestione delle sandbox può essere eseguita solo da un **[!UICONTROL Product]** o **[!UICONTROL System]** amministratore. Per ulteriori informazioni, consulta la [Documentazione di Admin Console](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/admin-roles.ug.html){target=&quot;_blank&quot;}.

Puoi scegliere di assegnare diverse sandbox a preconfigurate o personalizzate **[!UICONTROL Product profiles]**.

Per assegnare le sandbox:

1. In [!DNL Admin Console], dal **[!UICONTROL Products]** seleziona la scheda **[!UICONTROL Adobe Experience Platform Apps]** prodotto.

1. Seleziona un **[!UICONTROL Product profile]**.

   ![](../assets/sandbox_1.png)

1. Seleziona la scheda **[!UICONTROL Permissions]**.

1. Seleziona la **[!UICONTROL Sandboxes]** funzionalità.

   ![](../assets/sandbox_2.png)

1. Nella sezione **[!UICONTROL Available Permissions Items]**, fai clic sull’icona più (+) per assegnare le sandbox al profilo. [Ulteriori informazioni sulle sandbox](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html?lang=it){target=&quot;_blank&quot;}.

   ![](../assets/sandbox_3.png)

1. Se necessario, in **[!UICONTROL Included Permission Items]**, fai clic sull’icona X accanto a per rimuovere l’accesso alle sandbox al tuo **[!UICONTROL Product profile]**.

   ![](../assets/sandbox_4.png)

1. Fai clic su **[!UICONTROL Save]**.

## Accesso al contenuto {#content-access}

Per configurare l’accessibilità dei contenuti, è necessario assegnare una cartella di contenuti condivisa a ciascuna delle sandbox. Puoi creare e configurare la cartella condivisa nella scheda **[!UICONTROL Storage]** visualizzata in [!DNL Admin Console] per gli amministratori. Se hai accesso ad [!DNL Admin Console] come amministratore di sistema, puoi creare cartelle condivise e aggiungere delegati con diversi livelli di accesso alle cartelle condivise.

![](../assets/do-not-localize/content_access.png)

Per sincronizzare i contenuti con la sandbox corretta, è necessario seguire la stessa sintassi della sandbox. Ad esempio, se la sandbox è denominata “sviluppo”, la cartella condivisa deve avere lo stesso nome.

[Scopri come gestire le cartelle condivise](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-adobe-storage.ug.html){target=&quot;_blank&quot;}.

## Video introduttivo{#video}

Scopri cosa sono le sandbox e come distinguere le sandbox di sviluppo da quelle di produzione. Scopri come creare, reimpostare ed eliminare le sandbox.

>[!VIDEO](https://video.tv.adobe.com/v/334355?quality=12)
