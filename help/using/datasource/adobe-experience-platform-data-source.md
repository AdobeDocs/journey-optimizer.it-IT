---
solution: Journey Optimizer
product: journey optimizer
title: Origine dati Adobe Experience Platform
description: Scopri come configurare l’origine dati di Adobe Experience Platform
feature: Journeys, Data Sources
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate, Experienced
keywords: integrato, sorgente, dati, piattaforma, integrazione
exl-id: 9083e355-15e3-4d1f-91ae-03095e08ad16
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 31%

---

# Origine dati Adobe Experience Platform {#adobe-experience-platform-data-source}

>[!CONTEXTUALHELP]
>id="ajo_journey_data_source_built_in"
>title="Origine dati Adobe Experience Platform"
>abstract="L’origine dati di Adobe Experience Platform definisce la connessione ad Adobe Real-Time Customer Profile. Questa origine dati è integrata e preconfigurata e non può essere eliminata. È progettata per recuperare e utilizzare i dati dal servizio Real-Time Customer Profile (ad esempio, controlla se la persona che è entrata in un percorso è una donna). Consente di utilizzare i dati del profilo e i dati di eventi esperienza."

L’origine dati di Adobe Experience Platform definisce la connessione ad Adobe Real-Time Customer Profile. Questa origine dati è integrata e preconfigurata e non può essere eliminata. Questa origine dati è progettata per recuperare e utilizzare i dati del servizio Profilo cliente in tempo reale (ad esempio, verificare se la persona che ha inserito un percorso è una donna). Consente di utilizzare i dati del Profilo e i dati di Eventi esperienza. Per ulteriori informazioni su Adobe Real-time Customer Profile, consulta [Documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=it){target="_blank"}.


Per consentire la connessione al servizio Profilo cliente in tempo reale, è necessario utilizzare una chiave per identificare una persona e uno spazio dei nomi che la contestualizza. Di conseguenza, puoi utilizzare questa origine dati solo se i tuoi percorsi iniziano con un evento contenente una chiave e uno spazio dei nomi. [Ulteriori informazioni](../building-journeys/journey.md).

Puoi modificare il gruppo di campi preconfigurato denominato &quot;ProfileFieldGroup&quot;, aggiungerne di nuovi e rimuovere quelli che non sono utilizzati in alcun percorso in bozza o live. [Ulteriori informazioni](../datasource/configure-data-sources.md#define-field-groups).


>[!NOTE]
>
>Puoi recuperare i 1000 eventi di esperienza più recenti creati meno di un anno fa.

Di seguito sono riportati i passaggi principali per aggiungere gruppi di campi all’origine dati incorporata.

1. Dall’elenco delle origini dati, seleziona l’origine dati integrata di Adobe Experience Platform.

   Sul lato destro dello schermo si apre il riquadro di configurazione dell’origine dati .

   ![](assets/journey23.png)

1. Clic **[!UICONTROL Aggiungi un nuovo gruppo di campi]** per definire una nuova serie di campi da recuperare. [Ulteriori informazioni](../datasource/configure-data-sources.md#define-field-groups).

   ![](assets/journey24.png)

1. Seleziona uno schema da **[!UICONTROL Schema]** a discesa. Questo campo elenca gli schemi Profilo ed Eventi esperienza disponibili in Adobe Experience Platform. La creazione dello schema non viene eseguita in [!DNL Journey Optimizer]. Viene eseguito in Adobe Experience Platform.
1. Selezionare i campi da utilizzare.
1. Fai clic su **[!UICONTROL Salva]**.

Quando posizioni il cursore sul nome di un gruppo di campi, a destra vengono visualizzate due icone. Ti consentono di eliminare e duplicare il gruppo di campi. Tieni presente che **[!UICONTROL Elimina]** è disponibile solo se il gruppo di campi non viene utilizzato in alcun percorso live o bozza (le informazioni visualizzate **[!UICONTROL Utilizzato in]** ).
