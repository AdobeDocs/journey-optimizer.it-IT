---
solution: Journey Optimizer
product: journey optimizer
title: Origine dati Adobe Experience Platform
description: Scopri come configurare l’origine dati Adobe Experience Platform
feature: Data Sources
topic: Administration
role: Admin, Developer
level: Intermediate
keywords: integrato, origine, dati, piattaforma, integrazione
exl-id: 9083e355-15e3-4d1f-91ae-03095e08ad16
source-git-commit: b8065a68ed73102cb2c9da2c2d2675ce8e5fbaad
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 32%

---

# Origine dati Adobe Experience Platform {#adobe-experience-platform-data-source}

>[!CONTEXTUALHELP]
>id="ajo_journey_data_source_built_in"
>title="Origine dati Adobe Experience Platform"
>abstract="L’origine dati di Adobe Experience Platform definisce la connessione ad Adobe Real-Time Customer Profile. Questa origine dati è integrata e preconfigurata e non può essere eliminata. È progettata per recuperare e utilizzare i dati dal servizio Real-Time Customer Profile (ad esempio, controlla se la persona che è entrata in un percorso è una donna). Consente di utilizzare i dati del Profilo e i dati di Eventi esperienza."

L’origine dati di Adobe Experience Platform definisce la connessione ad Adobe Real-Time Customer Profile. Questa origine dati è integrata e preconfigurata e non può essere eliminata. Questa origine dati è progettata per recuperare e utilizzare i dati dal servizio Profilo cliente in tempo reale (ad esempio, controlla se la persona che ha inserito un percorso è una donna). Consente di utilizzare i dati del Profilo e i dati di Eventi esperienza. Per ulteriori informazioni sull’Adobe Profilo cliente in tempo reale, consulta [Documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=it){target="_blank"}.


Per consentire la connessione al servizio Profilo cliente in tempo reale, è necessario utilizzare una chiave per identificare una persona e uno spazio dei nomi che contestualizza la chiave. Di conseguenza, puoi utilizzare questa origine dati solo se i percorsi iniziano con un evento contenente una chiave e uno spazio dei nomi. [Maggiori informazioni](../building-journeys/journey.md).

È possibile modificare il gruppo di campi preconfigurato denominato &quot;ProfileFieldGroup&quot;, aggiungerne di nuovi e rimuovere quelli che non sono utilizzati in alcuna bozza o percorso live. [Maggiori informazioni](../datasource/configure-data-sources.md#define-field-groups).


>[!NOTE]
>
>Puoi recuperare gli ultimi 1000 eventi di esperienza creati meno di un anno fa.

Di seguito sono riportati i passaggi principali per aggiungere gruppi di campi all’origine dati incorporata.

1. Dall’elenco delle origini dati, selezionare l’origine dati integrata di Adobe Experience Platform.

   Sul lato destro dello schermo si apre il riquadro di configurazione dell’origine dati .

   ![](assets/journey23.png)

1. Fai clic su **[!UICONTROL Aggiungi un nuovo gruppo di campi]** definire una nuova serie di campi da recuperare. [Maggiori informazioni](../datasource/configure-data-sources.md#define-field-groups).

   ![](assets/journey24.png)

1. Seleziona uno schema dal **[!UICONTROL Schema]** a discesa. In questo campo sono elencati gli schemi di profili ed eventi di esperienza disponibili in Adobe Experience Platform. La creazione dello schema non viene eseguita in [!DNL Journey Optimizer]. Viene eseguito in Adobe Experience Platform.
1. Selezionare i campi da utilizzare.
1. Fai clic su **[!UICONTROL Salva]**.

Quando si posiziona il cursore sul nome di un gruppo di campi, vengono visualizzate due icone a destra. Consentono di eliminare e duplicare il gruppo di campi. Tieni presente che **[!UICONTROL Elimina]** l’icona è disponibile solo se il gruppo di campi non è utilizzato in alcun percorso live o di bozza (informazioni visualizzate nel **[!UICONTROL Utilizzato in]** (campo).
