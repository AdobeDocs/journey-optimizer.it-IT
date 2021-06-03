---
title: Gestione delle sandbox
description: Scopri come gestire le sandbox
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
exl-id: null
source-git-commit: e4f69cd209665e7f13a0c21e92453cd5cdce45a1
workflow-type: tm+mt
source-wordcount: '324'
ht-degree: 27%

---

# Gestione delle sandbox {#sandboxes}

![](../assets/do-not-localize/badge.png)

## Utilizzare le sandbox {#using-sandbox}

[!DNL Journey Optimizer] consente di suddividere l’istanza in ambienti virtuali separati, denominati sandbox.
Le sandbox vengono assegnate tramite i profili di prodotto nella Admin Console. [Scopri come assegnare le sandbox](permissions.md#create-product-profile).

[!DNL Journey Optimizer] riflette le sandbox Adobe Experience Platform create per una determinata organizzazione.
Le sandbox di Adobe Experience Platform possono essere create o reimpostate dall’istanza Adobe Experience Platform. [Ulteriori informazioni sono disponibili nella guida utente della sandbox](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html).

Il controllo del commutatore sandbox è disponibile in alto a sinistra sullo schermo. Per passare da una sandbox all’altra, fai clic sulla sandbox attualmente attiva nel commutatore e selezionane un’altra dall’elenco a discesa.

## Assegnare le sandbox {#assign-sandboxes}

>[!IMPORTANT]
>
> La gestione delle sandbox può essere eseguita solo da un amministratore **[!UICONTROL Product]** o **[!UICONTROL System]**. Per ulteriori informazioni, consulta la [documentazione di Admin Console](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/admin-roles.ug.html).

Puoi scegliere di assegnare diverse sandbox a preconfigurate o personalizzate **[!UICONTROL Product profiles]**.

Per assegnare le sandbox:

1. Nella scheda [!DNL Admin Console] , seleziona il prodotto **[!UICONTROL Adobe Experience Platform Apps]** dalla scheda **[!UICONTROL Products]** .

1. Seleziona un **[!UICONTROL Product profile]**.

1. Seleziona la scheda **[!UICONTROL Permissions]**.

1. Seleziona la funzionalità **[!UICONTROL Sandbox access]** .

1. Nella sezione **[!UICONTROL Available Permissions Items]**, fai clic sull’icona più (+) per assegnare le sandbox al profilo. [Ulteriori informazioni sulle sandbox](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html).

1. Se necessario, in **[!UICONTROL Included Permission Items]**, fai clic sull’icona X accanto a per rimuovere l’accesso alle sandbox al tuo **[!UICONTROL Product profile]**.

1. Fai clic su **[!UICONTROL Save]**.

## Accesso al contenuto {#content-access}

Per configurare l’accessibilità dei contenuti, è necessario assegnare una cartella condivisa del contenuto a ciascuna delle sandbox. Puoi creare e configurare la cartella condivisa nella scheda **[!UICONTROL Storage]** visualizzata in [!DNL Admin Console] per gli amministratori. Se hai accesso a [!DNL Admin Console] come amministratore di sistema, puoi creare cartelle condivise e aggiungere delegati con diverso livello di accesso alle cartelle condivise.

![](../assets/do-not-localize/content_access.png)

Per sincronizzare il contenuto con la sandbox corretta, è necessario seguire la stessa sintassi della sandbox; ad esempio, se la sandbox è denominata sviluppo, la cartella condivisa deve avere lo stesso nome.

[Scopri come gestire le cartelle](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-adobe-storage.ug.html) condivise.
