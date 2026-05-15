---
solution: Journey Optimizer
product: journey optimizer
title: Frammenti di contenuto di AEM
description: Scopri come accedere e gestire i frammenti di contenuto di AEM
topic: Content Management
role: User
level: Beginner
exl-id: c36a53a4-c324-4082-838e-ed27bd3b2e90
TQID: https://experienceleague.adobe.com/GRQ3Wz7Y4YJ3545mTtju0R8en9BYiejyo8UoMx558nM
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
  - id: fe96aceb-8194-4a8a-a6b0-75302d02804d
subfeature_v2:
  - id: c6e980f5-2d4f-494f-beef-186b9ecf1513
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 269
ht-degree: 18%

---

# Introduzione ai frammenti di contenuto di Adobe Experience Manager {#aem-fragments}

>[!AVAILABILITY]
>
>Per i clienti del settore sanitario, l&#39;integrazione è abilitata solo dopo aver concesso in licenza le offerte aggiuntive Journey Optimizer Healthcare Shield e Adobe Experience Manager Enhanced Security.

Integrando Adobe Experience Manager as a Cloud Service con Adobe Journey Optimizer, ora puoi incorporare facilmente i frammenti di contenuto AEM nei contenuti Journey Optimizer. Questa connessione diretta facilita il processo di accesso e utilizzo dei contenuti AEM, consentendo la creazione di campagne e percorsi personalizzati e dinamici.

Per ulteriori informazioni sui frammenti di contenuto di AEM, consulta [Utilizzo dei frammenti di contenuto](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragments-with-journey-optimizer){target="_blank"} nella documentazione di Experience Manager.

## Ciclo di vita dei frammenti di contenuto

![](assets/do-not-localize/AEM_CF.png)

I frammenti di contenuto seguono diverse fasi del ciclo di vita a seconda del livello Adobe Experience Manager in cui esistono. [Ulteriori informazioni nella documentazione di Adobe Experience Manager](https://experienceleague.adobe.com/it/docs/experience-manager-cloud-service/content/sites/authoring/author-publish)

Il contenuto viene creato e gestito nel **livello di authoring**, dove i frammenti possono avere stati come Nuovo, Bozza, Pubblicato, Modificato o Non pubblicato. Questi stati sono validi solo per il **livello di authoring** e supportano la creazione e la revisione dei contenuti.

Quando viene pubblicato un frammento di contenuto, viene creata una copia nel **livello di pubblicazione** ed esposta tramite un endpoint pubblico non autenticato. Journey Optimizer si integra esclusivamente con questo **livello di pubblicazione**.

Di conseguenza, Journey Optimizer fa emergere solo frammenti di contenuto pubblicati o modificati e utilizza sempre l’ultima versione pubblicata. Eventuali modifiche apportate dopo la pubblicazione non vengono applicate in Journey Optimizer fino a quando il frammento di contenuto non viene ripubblicato.
