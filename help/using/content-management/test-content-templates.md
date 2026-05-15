---
solution: Journey Optimizer
product: journey optimizer
title: Testare modelli di contenuto
description: Scopri come verificare il rendering di alcuni modelli di contenuto e-mail
feature: Templates
topic: Content Management
role: User
level: Beginner
exl-id: 01726ab6-f581-4d19-aedd-2541bc0f27c6
TQID: https://experienceleague.adobe.com/CC56E9rV4TImjLBbm-fsq2a4JKLnEA4wJB2DVLgOAfM
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d556b755-390a-43f0-be32-a08cf6236126id: dc22c819-3f29-4e91-8b7d-5c6719831141id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2: id: a5683ded-e5d5-4ec6-b9fd-e1b56a94ab96id: d595a60b-bcf5-4a63-a189-66a0be755cc7id: f8d2e9f0-69c9-40cd-890f-71336c8dfff7id: fae48155-b23f-40d2-a252-a25bce350b4did: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 252
ht-degree: 4%

---

# Test dei modelli di contenuto e-mail {#test-template}

Puoi testare il rendering di alcuni modelli e-mail, creati da zero o da un contenuto esistente. A questo scopo, segui i passaggi riportati qui sotto.

1. Accedi all&#39;elenco dei modelli di contenuto tramite il menu **[!UICONTROL Gestione contenuto]** > **[!UICONTROL Modelli di contenuto]** e seleziona un modello di e-mail.

1. Fai clic su **[!UICONTROL Modifica contenuto]** dalle **[!UICONTROL proprietà modello]**.

1. Fai clic su **[!UICONTROL Simula contenuto]** e seleziona un profilo di test per verificare il rendering. [Ulteriori informazioni](../content-management/preview-test.md)

   ![](assets/content-template-stimulate.png)

   >[!NOTE]
   >
   >[!DNL Journey optimizer] consente inoltre di testare diverse varianti dei modelli di contenuto visualizzandoli in anteprima e inviando bozze utilizzando dati di input di esempio caricati da un file CSV / JSON o aggiunti manualmente. [Scopri come simulare varianti di contenuto](../test-approve/simulate-sample-input.md)

1. Puoi inviare una bozza per testare il contenuto e farla approvare da alcuni utenti interni prima di utilizzarla in un percorso o in una campagna.

   * A tale scopo, fare clic sul pulsante **[!UICONTROL Invia bozza]** e seguire i passaggi descritti in [questa sezione](../content-management/proofs.md).

   * Prima di inviare la bozza, è necessario selezionare la [configurazione e-mail](../configuration/channel-surfaces.md) che verrà utilizzata per verificare il contenuto.

     ![](assets/content-template-stimulate-proof-surface.png)

>[!CAUTION]
>
>Il tracciamento attuale non è supportato durante il test dei modelli di contenuto e-mail, il che significa che gli eventi di tracciamento, i parametri UTM e i collegamenti alle pagine di destinazione non saranno efficaci nelle bozze inviate da un modello. Per verificare il tracciamento, [utilizza il modello di contenuto](../email/use-email-templates.md) in un messaggio e-mail e invia una bozza utilizzando i profili di test, oppure dati di input di esempio caricati da un file CSV/JSON o aggiunti manualmente. [Scopri come visualizzare in anteprima e verificare il contenuto](../content-management/preview-test.md)
