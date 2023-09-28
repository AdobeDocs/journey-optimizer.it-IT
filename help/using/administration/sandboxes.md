---
solution: Journey Optimizer
product: journey optimizer
title: Gestione delle sandbox
description: Scopri come gestire le sandbox
feature: Sandboxes
topic: Administration
role: Admin, Architect, Developer
level: Experienced
keywords: sandbox, virtuale, ambienti, organizzazione, piattaforma
exl-id: 14f80d5d-0840-4b79-9922-6d557a7e1247
source-git-commit: 9f43387ff63c3d2c2849fad1ca6a98310b3915b3
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 61%

---

# Gestione delle sandbox {#sandboxes}

## Utilizzare le sandbox {#using-sandbox}

[!DNL Journey Optimizer] consente di suddividere l’istanza in ambienti virtuali separati, denominati sandbox.
Le sandbox vengono assegnate tramite i ruoli in Autorizzazioni. [Scopri come assegnare le sandbox](permissions.md#create-product-profile).

[!DNL Journey Optimizer] presenta le sandbox di Adobe Experience Platform che sono state create per una determinata organizzazione.
Le sandbox di Adobe Experience Platform possono essere create o reimpostate dall’istanza di Adobe Experience Platform. [Ulteriori informazioni sono disponibili nella guida utente sulle sandbox](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html?lang=it){target="_blank"}.

Puoi trovare il controllo del commutatore sandbox in alto a destra dello schermo accanto al nome della tua organizzazione. Per passare da una sandbox all’altra, fai clic sulla sandbox attualmente attiva nel commutatore e selezionane un’altra dall’elenco a discesa.

![](assets/sandbox_5.png)

➡️ [Ulteriori informazioni sulle sandbox in questo video](#video)

## Assegna sandbox {#assign-sandboxes}

>[!IMPORTANT]
>
> La gestione delle sandbox può essere eseguita solo da un **[!UICONTROL Prodotto]** o **[!UICONTROL Sistema]** amministratore.

Puoi scegliere di assegnare sandbox diverse a sandbox predefinite o personalizzate **[!UICONTROL Ruoli]**.

Per assegnare le sandbox:

1. In entrata [!DNL Permissions], dalla **[!UICONTROL Ruoli]** , seleziona una **[!UICONTROL Ruolo]**.

   ![](assets/sandbox_1.png)

1. Clic **[!UICONTROL Modifica]**.

1. Dalla sezione **[!UICONTROL Sandbox]** dall&#39;elenco a discesa delle risorse, seleziona la sandbox che verrà assegnata al tuo ruolo.

   ![](assets/sandbox_3.png)

1. Se necessario, fai clic sull’icona X accanto a rimuovere le sandbox per accedere al **[!UICONTROL Ruolo]**.

   ![](assets/sandbox_4.png)

1. Fai clic su **[!UICONTROL Salva]**.

## Accesso al contenuto {#content-access}

Per configurare l’accessibilità dei contenuti, è necessario assegnare una cartella di contenuti condivisa a ciascuna delle sandbox. Puoi creare e configurare la cartella condivisa in **[!UICONTROL Storage]** scheda visualizzata in [!DNL Admin Console] per gli amministratori. Se hai accesso ad [!DNL Admin Console] come amministratore di sistema, puoi creare cartelle condivise e aggiungere delegati con diversi livelli di accesso alle cartelle condivise.

![](assets/do-not-localize/content_access.png)

Per sincronizzare i contenuti con la sandbox corretta, è necessario seguire la stessa sintassi della sandbox. Ad esempio, se la sandbox è denominata “sviluppo”, la cartella condivisa deve avere lo stesso nome.

[Scopri come gestire le cartelle condivise](https://helpx.adobe.com/it/enterprise/admin-guide.html/enterprise/using/manage-adobe-storage.ug.html){target="_blank"}.

## Video introduttivo{#video}

Scopri cosa sono le sandbox e come distinguere le sandbox di sviluppo da quelle di produzione. Scopri come creare, reimpostare ed eliminare le sandbox.

>[!VIDEO](https://video.tv.adobe.com/v/334355?quality=12)