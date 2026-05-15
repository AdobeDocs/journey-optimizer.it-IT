---
solution: Journey Optimizer
product: journey optimizer
title: Informazioni sui tipi di pubblico di Adobe Experience Platform
description: Scopri come utilizzare i tipi di pubblico di Adobe Experience Platform
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: 71c652ba-f38f-452c-9c1b-dcd728307baf
TQID: https://experienceleague.adobe.com/HkybhydJwQDHVEXCKM5o16ZNeiBk-n9mogm-2pwFKus
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
subfeature_v2:
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 149
ht-degree: 10%

---

# Caricamento personalizzato {#custom-upload}

Adobe Experience Platform Audience Portal consente di importare un pubblico utilizzando un file CSV.

Durante il processo di caricamento personalizzato, specifica l’attributo CSV da utilizzare come identità e l’identità del profilo a cui è mappato. Questo stabilisce un collegamento tra i dati del pubblico e il profilo. Se il file CSV contiene un valore di identità non trovato nel profilo, viene creato un nuovo profilo con tale valore di identità.

>[!NOTE]
>
>Per i tipi di pubblico di caricamento personalizzati, se &quot;Lettura incrementale&quot; è abilitato in un percorso ricorrente, i profili vengono recuperati solo alla prima ricorrenza, in quanto questi tipi di pubblico sono fissi.

![](assets/import-audience.png)

Informazioni dettagliate su come importare tipi di pubblico sono disponibili nella [documentazione del servizio di segmentazione](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-portal#import-audience){target="_blank"} di Adobe Experience Platform.

Scopri come caricare i tipi di pubblico in formato CSV nel video:

>[!VIDEO](https://video.tv.adobe.com/v/3421714?quality=12)
