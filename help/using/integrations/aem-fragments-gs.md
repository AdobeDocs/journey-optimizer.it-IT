---
solution: Journey Optimizer
product: journey optimizer
title: Frammenti di contenuto di AEM
description: Scopri come accedere e gestire i frammenti di contenuto di AEM
topic: Content Management
role: User
level: Beginner
source-git-commit: 4f7e36a6cc19e4138e867950e34c5a5e6452b364
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 20%

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
