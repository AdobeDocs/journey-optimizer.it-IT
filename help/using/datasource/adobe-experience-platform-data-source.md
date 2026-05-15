---
solution: Journey Optimizer
product: journey optimizer
title: Origine dati Adobe Experience Platform
description: Scopri come configurare l’origine dati di Adobe Experience Platform
feature: Journeys, Data Sources
topic: Administration
role: Developer, Admin
level: Intermediate, Experienced
keywords: integrato, sorgente, dati, piattaforma, integrazione
exl-id: 9083e355-15e3-4d1f-91ae-03095e08ad16
TQID: https://experienceleague.adobe.com/tvO8GjVADFHV1i6ff5krss2YyS-rtnQZ4BHcvvhG-t4
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: dd51b532-b93f-4bcf-8dbf-0d007f593aca
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 451
ht-degree: 27%

---

# Origine dati Adobe Experience Platform {#adobe-experience-platform-data-source}

>[!CONTEXTUALHELP]
>id="ajo_journey_data_source_built_in"
>title="Origine dati Adobe Experience Platform"
>abstract="L’origine dati di Adobe Experience Platform definisce la connessione ad Adobe Real-Time Customer Profile. Questa origine dati è incorporata e preconfigurata e non può essere eliminata. È progettata per recuperare e utilizzare i dati dal servizio Profilo cliente in tempo reale (ad esempio, controlla se la persona che ha effettuato l’accesso in un percorso è una donna)."

L’origine dati di Adobe Experience Platform definisce la connessione ad Adobe Real-Time Customer Profile. Questa origine dati è incorporata e preconfigurata e non può essere eliminata. Questa origine dati è progettata per recuperare e utilizzare i dati del servizio Profilo cliente in tempo reale (ad esempio, verificare se la persona che ha inserito un percorso è una donna). Per ulteriori informazioni su Adobe Real-time Customer Profile, consulta la [documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=it){target="_blank"}.

Per consentire la connessione al servizio Profilo cliente in tempo reale, è necessario utilizzare una chiave per identificare una persona e uno spazio dei nomi che la contestualizza. Di conseguenza, puoi utilizzare questa origine dati solo se i tuoi percorsi iniziano con un evento contenente una chiave e uno spazio dei nomi. [Ulteriori informazioni](../building-journeys/journey.md).

Puoi modificare il gruppo di campi preconfigurato denominato &quot;ProfileFieldGroup&quot;, aggiungerne di nuovi e rimuovere quelli che non sono utilizzati in alcun percorso in bozza o live. [Ulteriori informazioni](../datasource/configure-data-sources.md#define-field-groups).

>[!CAUTION]
>
>L’utilizzo di eventi di esperienza nelle espressioni/condizioni di percorso non è supportato. Se il caso d’uso richiede l’utilizzo di eventi esperienza, considera metodi alternativi. [Ulteriori informazioni](../building-journeys/exp-event-lookup.md)

Di seguito sono riportati i passaggi principali per aggiungere gruppi di campi all’origine dati incorporata:

1. Dall&#39;elenco delle origini dati, selezionare l&#39;origine dati predefinita **Adobe Experience Platform**.

   Sul lato destro dello schermo si apre il riquadro di configurazione dell’origine dati .

   ![](assets/journey23.png)

1. Selezionare **[!UICONTROL Aggiungi un nuovo gruppo di campi]** per definire una [nuova serie di campi da recuperare](../datasource/configure-data-sources.md#define-field-groups).

   ![](assets/journey24.png)

1. Selezionare uno schema dal menu a discesa **[!UICONTROL Schema]**. La creazione dello schema viene eseguita in Adobe Experience Platform, non in Adobe Journey Optimizer.

   >[!NOTE]
   >
   >Nella configurazione di Data Source [!DNL Journey Optimizer] sono supportati solo gli schemi basati su profili individuali XDM. Per ulteriori informazioni, vedere [Classe profilo individuale XDM](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/classes/individual-profile){target="_blank"}.

1. Seleziona i campi da utilizzare e salva le modifiche.

>[!TIP]
>
>Passa il puntatore del mouse sul nome di un gruppo di campi per visualizzare due icone a destra. Utilizzali per **duplicare** o **eliminare** il gruppo di campi. L&#39;icona **[!UICONTROL Elimina]** è disponibile solo se il gruppo di campi non è utilizzato in alcun percorso **Live**, **Bozza** o **Finished**. Fai riferimento al campo **[!UICONTROL Usato in]** per verificare se è così.
