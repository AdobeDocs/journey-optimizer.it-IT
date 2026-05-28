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
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: fe96aceb-8194-4a8a-a6b0-75302d02804d
subfeature_v2: id: c7dc31c0-c4f7-42a7-8cf5-a8c5aeb0de74
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: c1579802-ddd4-4214-8a91-97b2066abe11id: d095671a-1355-40aa-8b5f-06c33c68080bid: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 269
ht-degree: 18%

---

# Introduzione ai frammenti di contenuto di Adobe Experience Manager {#aem-fragments}

>[!AVAILABILITY]
>
>Per i clienti del settore sanitario, l&#39;integrazione è abilitata solo dopo aver concesso in licenza le offerte aggiuntive Journey Optimizer Healthcare Shield e Adobe Experience Manager Enhanced Security.

Integrando Adobe Experience Manager as a Cloud Service con Adobe Journey Optimizer, ora puoi incorporare facilmente i frammenti di contenuto AEM nei contenuti Journey Optimizer. Questa connessione diretta facilita il processo di accesso e utilizzo dei contenuti AEM, consentendo la creazione di campagne e percorsi personalizzati e dinamici.

Per ulteriori informazioni sui frammenti di contenuto di AEM, consulta [Utilizzo dei frammenti di contenuto](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragments-with-journey-optimizer){target="_blank"} nella documentazione di Experience Manager.

## Ciclo di vita dei frammenti di contenuto

![](assets/do-not-localize/AEM_CF.png)

I frammenti di contenuto seguono diverse fasi del ciclo di vita a seconda del livello Adobe Experience Manager in cui esistono. [Ulteriori informazioni nella documentazione di Adobe Experience Manager](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/author-publish)

Il contenuto viene creato e gestito nel **livello di authoring**, dove i frammenti possono avere stati come Nuovo, Bozza, Pubblicato, Modificato o Non pubblicato. Questi stati sono validi solo per il **livello di authoring** e supportano la creazione e la revisione dei contenuti.

Quando viene pubblicato un frammento di contenuto, viene creata una copia nel **livello di pubblicazione** ed esposta tramite un endpoint pubblico non autenticato. Journey Optimizer si integra esclusivamente con questo **livello di pubblicazione**.

Di conseguenza, Journey Optimizer fa emergere solo frammenti di contenuto pubblicati o modificati e utilizza sempre l’ultima versione pubblicata. Eventuali modifiche apportate dopo la pubblicazione non vengono applicate in Journey Optimizer fino a quando il frammento di contenuto non viene ripubblicato.
