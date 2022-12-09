---
solution: Journey Optimizer
product: journey optimizer
title: Origine dati Adobe Experience Platform
description: Scopri come configurare l’origine dati di Adobe Experience Platform
feature: Data Sources
topic: Administration
role: Admin
level: Intermediate
exl-id: 9083e355-15e3-4d1f-91ae-03095e08ad16
source-git-commit: 69037a070f43fa89d0971cedc03adb577e1450d9
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 0%

---

# Origine dati Adobe Experience Platform {#adobe-experience-platform-data-source}

>[!CONTEXTUALHELP]
>id="ajo_journey_data_source_built_in"
>title="Origine dati Adobe Experience Platform"
>abstract="L’origine dati Adobe Experience Platform definisce la connessione al profilo cliente in tempo reale di Adobe. Questa origine dati è incorporata e preconfigurata e non può essere eliminata. È progettato per recuperare e utilizzare i dati dal Real-time Customer Profile Service (ad esempio, controlla se la persona che ha effettuato un percorso è una donna). Ti consente di utilizzare i dati Profilo e i dati Eventi esperienza."

L’origine dati Adobe Experience Platform definisce la connessione al profilo cliente in tempo reale di Adobe. Questa origine dati è incorporata e preconfigurata e non può essere eliminata. Questa origine dati è progettata per recuperare e utilizzare i dati dal servizio Profilo cliente in tempo reale (ad esempio, verifica se la persona che ha effettuato un percorso è una donna). Ti consente di utilizzare i dati Profilo e i dati Eventi esperienza. Per ulteriori informazioni sul profilo cliente in tempo reale di Adobe, consulta [Documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html){target=&quot;_blank&quot;}.


Per consentire la connessione al servizio Profilo cliente in tempo reale, è necessario utilizzare una chiave per identificare una persona e uno spazio dei nomi che contestualizza la chiave. Di conseguenza, puoi utilizzare questa origine dati solo se i tuoi percorsi iniziano con un evento contenente una chiave e uno spazio dei nomi. [Ulteriori informazioni](../building-journeys/journey.md).

Puoi modificare il gruppo di campi preconfigurato denominato &quot;ProfileFieldGroup&quot;, aggiungerne di nuovi e rimuovere quelli che non sono utilizzati in alcuna bozza o in percorsi live. [Ulteriori informazioni](../datasource/configure-data-sources.md#define-field-groups).


>[!NOTE]
>
>Puoi recuperare gli ultimi 1000 eventi di esperienza creati meno di un anno fa.

Di seguito sono riportati i passaggi principali per aggiungere gruppi di campi all’origine dati incorporata.

1. Dall’elenco delle origini dati, seleziona l’origine dati integrata di Adobe Experience Platform.

   Viene aperto il riquadro di configurazione dell’origine dati sul lato destro dello schermo.

   ![](assets/journey23.png)

1. Fai clic su **[!UICONTROL Add a New Field Group]** definire una nuova serie di campi da recuperare. [Ulteriori informazioni](../datasource/configure-data-sources.md#define-field-groups).

   ![](assets/journey24.png)

1. Seleziona uno schema dal **[!UICONTROL Schema]** a discesa. In questo campo sono elencati gli schemi di profili ed eventi di esperienza disponibili in Adobe Experience Platform. La creazione dello schema non viene eseguita in [!DNL Journey Optimizer]. Viene eseguito in Adobe Experience Platform.
1. Selezionare i campi da utilizzare.
1. Fai clic su **[!UICONTROL Save]**.

Quando si posiziona il cursore sul nome di un gruppo di campi, vengono visualizzate due icone a destra. Consentono di eliminare e duplicare il gruppo di campi. Tieni presente che **[!UICONTROL Delete]** l’icona è disponibile solo se il gruppo di campi non è utilizzato in alcun percorso live o di bozza (informazioni visualizzate nella **[!UICONTROL Used in]** (campo).
