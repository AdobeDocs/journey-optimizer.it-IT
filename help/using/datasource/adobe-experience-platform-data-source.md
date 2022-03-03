---
title: Origine dati Adobe Experience Platform
description: Scopri come configurare l’origine dati Adobe Experience Platform
feature: Data Sources
topic: Administration
role: Admin
level: Intermediate
exl-id: 9083e355-15e3-4d1f-91ae-03095e08ad16
source-git-commit: bd35bf2ec4c1b2898007d670fc20626f06cc3750
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 11%

---

# Origine dati Adobe Experience Platform {#adobe-experience-platform-data-source}

L’origine dati Adobe Experience Platform definisce la connessione al servizio Profilo cliente in tempo reale. Questa origine dati è incorporata e preconfigurata. Non può essere eliminato. Questa origine dati è progettata per recuperare e utilizzare i dati dal servizio Profilo cliente in tempo reale (ad esempio, controlla se la persona che ha inserito un percorso è una donna). It allows you to use Profile data and Experience Events data. For more information on the Real-time Customer Profile Service, refer to [Adobe Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=it){target=&quot;_blank&quot;}.

>[!NOTE]
>
>Puoi recuperare gli ultimi 1000 eventi di esperienza creati meno di un anno fa.

Per consentire la connessione al servizio Profilo cliente in tempo reale, è necessario utilizzare una chiave per identificare una persona e uno spazio dei nomi che contestualizza la chiave. Di conseguenza, puoi utilizzare questa origine dati solo se i percorsi iniziano con un evento contenente una chiave e uno spazio dei nomi. Consulta [questa pagina](../building-journeys/journey.md).

You can edit the pre-configured field group named “ProfileFieldGroup”, add new ones and remove the ones that are not used in any draft or live journeys. Consulta [questa pagina](../datasource/configure-data-sources.md#define-field-groups).

Di seguito sono riportati i passaggi principali per aggiungere gruppi di campi all’origine dati incorporata.

1. Dall’elenco delle origini dati, selezionare l’origine dati integrata di Adobe Experience Platform.

   Sul lato destro dello schermo si apre il riquadro di configurazione dell’origine dati .

   ![](assets/journey23.png)

1. Fai clic su **[!UICONTROL Add a New Field Group]** definire una nuova serie di campi da recuperare. Consulta [questa pagina](../datasource/configure-data-sources.md#define-field-groups).

   ![](assets/journey24.png)

1. Select a schema from the **[!UICONTROL Schema]** drop-down. In questo campo sono elencati gli schemi di profili ed eventi di esperienza disponibili in Adobe Experience Platform. La creazione dello schema non viene eseguita in [!DNL Journey Optimizer]. It’s performed in Adobe Experience Platform.
1. Selezionare i campi da utilizzare.
1. Click on **[!UICONTROL Save]**.

Quando si posiziona il cursore sul nome di un gruppo di campi, vengono visualizzate due icone a destra. Consentono di eliminare e duplicare il gruppo di campi. Note that the **[!UICONTROL Delete]** icon is only available if the field group is not used in any live or draft journey (information displayed in the **[!UICONTROL Used in]** field).
