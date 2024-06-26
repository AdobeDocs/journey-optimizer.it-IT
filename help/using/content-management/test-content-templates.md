---
solution: Journey Optimizer
product: journey optimizer
title: Test dei modelli di contenuto
description: Scopri come verificare il rendering di alcuni modelli di contenuto e-mail
feature: Templates
topic: Content Management
role: User
level: Beginner
source-git-commit: 59c675dd2ac94b6967cfb3a93f74b2016a090190
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 4%

---

# Test dei modelli di contenuto e-mail {#test-template}

Puoi testare il rendering di alcuni modelli e-mail, creati da zero o da un contenuto esistente. A questo scopo, segui i passaggi riportati qui sotto.

1. Accedere all’elenco dei modelli di contenuto tramite **[!UICONTROL Gestione dei contenuti]** > **[!UICONTROL Modelli di contenuto]** e seleziona un modello di e-mail.

1. Clic **[!UICONTROL Modifica contenuto]** dal **[!UICONTROL Proprietà modello]**.

1. Clic **[!UICONTROL Simula contenuto]** e seleziona un profilo di test per controllare il rendering. [Ulteriori informazioni](../content-management/preview-test.md)

   ![](assets/content-template-stimulate.png)

1. Puoi inviare una bozza per testare il contenuto e farla approvare da alcuni utenti interni prima di utilizzarla in un percorso o in una campagna.

   * A tale scopo, fare clic sul pulsante **[!UICONTROL Invia bozza]** e seguire i passaggi descritti in [questa sezione](../content-management/proofs.md).

   * Prima di inviare la bozza, è necessario selezionare [superficie e-mail](../configuration/channel-surfaces.md) che verranno utilizzati per testare il contenuto.

     ![](assets/content-template-stimulate-proof-surface.png)

>[!CAUTION]
>
>Il tracciamento attuale non è supportato durante il test dei modelli di contenuto e-mail, il che significa che gli eventi di tracciamento, i parametri UTM e i collegamenti alle pagine di destinazione non saranno efficaci nelle bozze inviate da un modello. Per verificare il tracciamento: [utilizzare il modello di contenuto](../email/use-email-templates.md) in un messaggio e-mail e [invia una bozza](../content-management/preview-test.md#send-proofs).
