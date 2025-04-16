---
solution: Journey Optimizer
product: journey optimizer
title: Gestione delle sandbox
description: Scopri come gestire sandbox
feature: Sandboxes
topic: Administration
role: Admin, Architect, Developer
level: Experienced
keywords: sandbox, virtuali, ambienti, organizzazione, piattaforma
exl-id: 14f80d5d-0840-4b79-9922-6d557a7e1247
source-git-commit: 621f9bcb32d108490e7674778ce40385938af18e
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 52%

---

# Gestione delle sandbox {#sandboxes}

## Utilizzare le sandbox {#using-sandbox}

[!DNL Journey Optimizer] Consente di partizionare il istanza in ambienti virtuali separati denominati sandbox. Le sandbox vengono assegnate tramite ruoli in Autorizzazioni. [Scopri come assegnare le sandbox](permissions.md#create-product-profile).

[!DNL Journey Optimizer] riflette Adobe Experience Platform sandbox create per una determinata organizzazione. Le sandbox di Adobe Experience Platform possono essere create o reimpostate dall’istanza di Adobe Experience Platform. [Ulteriori informazioni sono disponibili nella guida utente sulle sandbox](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html?lang=it){target="_blank"}.

Puoi trovare il controllo sandbox switcher in alto a destra dello schermo accanto al nome della tua organizzazione. Per passare da una sandbox all’altra, fai clic sulla sandbox attualmente attiva nel commutatore e selezionane un’altra dall’elenco a discesa.

![](assets/sandbox_5.png)

➡️ [Scopri maggiori informazioni sulle sandbox in questo video](#video)

## Assegna sandbox {#assign-sandboxes}

>[!IMPORTANT]
>
> La gestione delle sandbox può essere eseguita solo da un **[!UICONTROL amministratore di prodotto]** o **[!UICONTROL di sistema]** .

Puoi scegliere di assegnare sandbox diverse a ruoli ]**predefiniti o personalizzati**[!UICONTROL .

Per assegnare le sandbox:

1. In [!DNL Permissions], selezionare un **[!UICONTROL ruolo dalla scheda**[!UICONTROL  Ruoli ]**]**.

   ![](assets/sandbox_1.png)

1. Fare clic su **[!UICONTROL Modifica]**.

1. Dall&#39;elenco a discesa delle **[!UICONTROL risorse Sandbox]** , seleziona la sandbox che verrà assegnata al tuo ruolo.

   ![](assets/sandbox_3.png)

1. Se necessario, fai clic sull&#39;icona X accanto per rimuovere le sandbox accesso al tuo **[!UICONTROL ruolo]**.

   ![](assets/sandbox_4.png)

1. Fai clic su **[!UICONTROL Salva]**.

## Accesso ai contenuti {#content-access}

Per configurare l’accessibilità dei contenuti, è necessario assegnare una cartella di contenuti condivisa a ciascuna delle sandbox. È possibile creare e configurare la **[!UICONTROL cartella condivisa nella scheda di archiviazione]** visualizzata nella [!DNL Admin Console] finestra per amministratori. Se hai accesso ad [!DNL Admin Console] come amministratore di sistema, puoi creare cartelle condivise e aggiungere delegati con diversi livelli di accesso alle cartelle condivise.

![](assets/do-not-localize/content_access.png)

Per sincronizzare i contenuti con la sandbox corretta, è necessario seguire la stessa sintassi della sandbox. Ad esempio, se la sandbox è denominata “sviluppo”, la cartella condivisa deve avere lo stesso nome.

[Scopri come gestire le cartelle condivise](https://helpx.adobe.com/it/enterprise/admin-guide.html/enterprise/using/manage-adobe-storage.ug.html){target="_blank"}.

## Video introduttivo{#video}

Scopri cosa sono le sandbox e come distinguere le sandbox di sviluppo da quelle di produzione. Scopri come creare, reimpostare ed eliminare le sandbox.

>[!VIDEO](https://video.tv.adobe.com/v/334355?quality=12)