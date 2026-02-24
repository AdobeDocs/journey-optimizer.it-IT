---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare e assegnare sandbox
description: Scopri come gestire le sandbox
feature: Sandboxes
topic: Administration
role: Admin, Developer
level: Experienced
keywords: sandbox, virtuale, ambienti, organizzazione, piattaforma
exl-id: 14f80d5d-0840-4b79-9922-6d557a7e1247
source-git-commit: 56faee8badff99ff9a39cfd85a78c1ed272cd2ca
workflow-type: tm+mt
source-wordcount: '406'
ht-degree: 22%

---

# Utilizzare e assegnare sandbox {#sandboxes}

Le **Sandbox** sono ambienti virtuali che suddividono l&#39;istanza di Adobe Journey Optimizer in aree di lavoro separate e isolate, per lo sviluppo, il test o la produzione. La gestione della sandbox si trova in **Amministrazione** > **Canali** > **Connetti i sistemi e gli ambienti** (o tramite il selettore sandbox in alto a destra nell&#39;interfaccia). Le sandbox consentono di sperimentare in modo sicuro, assegnare un accesso diverso per ruolo e mantenere il contenuto organizzato. In questa pagina viene illustrato come utilizzare e assegnare sandbox, configurare l&#39;accesso al contenuto e, nell&#39;articolo [Esportare oggetti in un&#39;altra sandbox](../configuration/copy-objects-to-sandbox.md), come copiare percorsi e modelli tra sandbox.

## Utilizzare le sandbox {#using-sandbox}

[!DNL Journey Optimizer] consente di suddividere l&#39;istanza in ambienti virtuali separati denominati sandbox. Le sandbox vengono assegnate tramite i ruoli in Autorizzazioni. [Scopri come assegnare le sandbox](permissions.md#create-product-profile).

[!DNL Journey Optimizer] riflette le sandbox di Adobe Experience Platform create per una determinata organizzazione. Le sandbox di Adobe Experience Platform possono essere create o reimpostate dall’istanza di Adobe Experience Platform. [Ulteriori informazioni sono disponibili nella guida utente sulle sandbox](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html?lang=it){target="_blank"}.

Puoi trovare il controllo del commutatore sandbox in alto a destra dello schermo, accanto al nome della tua organizzazione. Per passare da una sandbox all’altra, fai clic sulla sandbox attualmente attiva nel commutatore e selezionane un’altra dall’elenco a discesa.

![](assets/sandbox_5.png)

➡️ [Ulteriori informazioni sulle sandbox in questo video](#video)

## Assegna sandbox {#assign-sandboxes}

>[!IMPORTANT]
>
> La gestione delle sandbox può essere eseguita solo da un amministratore **[!UICONTROL Product]** o **[!UICONTROL System]**.

Puoi scegliere di assegnare sandbox diverse a **[!UICONTROL Ruoli]** predefiniti o personalizzati.

Per assegnare le sandbox:

1. In [!DNL Permissions], dalla scheda **[!UICONTROL Ruoli]**, selezionare un **[!UICONTROL Ruolo]**.

   ![](assets/sandbox_1.png)

1. Fai clic su **[!UICONTROL Modifica]**.

1. Dall&#39;elenco a discesa delle risorse **[!UICONTROL Sandbox]**, seleziona la sandbox che verrà assegnata al tuo ruolo.

   ![](assets/sandbox_3.png)

1. Se necessario, fai clic sull&#39;icona X accanto ad essa per rimuovere l&#39;accesso alla sandbox dal tuo **[!UICONTROL Ruolo]**.

   ![](assets/sandbox_4.png)

1. Fai clic su **[!UICONTROL Salva]**.

## Accesso al contenuto {#content-access}

Per configurare l’accessibilità dei contenuti, assegna una cartella condivisa di contenuto a ciascuna sandbox. Puoi creare e configurare le cartelle condivise nella scheda **[!UICONTROL Archiviazione]** visualizzata in [!DNL Admin Console] per gli amministratori. Se hai accesso a [!DNL Admin Console] come amministratore di sistema, puoi creare cartelle condivise e aggiungere delegati con diversi livelli di accesso alle cartelle condivise.

![](assets/do-not-localize/content_access.png)

Per sincronizzare i contenuti con la sandbox corretta, è necessario seguire la stessa sintassi della sandbox. Ad esempio, se la sandbox è denominata &quot;sviluppo&quot;, la cartella condivisa deve avere lo stesso nome.

[Scopri come gestire le cartelle condivise](https://helpx.adobe.com/it/enterprise/admin-guide.html/enterprise/using/manage-adobe-storage.ug.html){target="_blank"}.

## Video introduttivo{#video}

Scopri cosa sono le sandbox e come distinguere le sandbox di sviluppo da quelle di produzione. Scopri come creare, reimpostare ed eliminare le sandbox.

>[!VIDEO](https://video.tv.adobe.com/v/334355?quality=12)