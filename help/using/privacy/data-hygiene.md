---
solution: Journey Optimizer
product: journey optimizer
title: Eseguire operazioni relative al ciclo di vita dei dati
description: Scopri come eseguire operazioni relative al ciclo di vita dei dati
feature: Privacy, Monitoring
role: User
level: Intermediate
exl-id: 8045b559-bf5e-4b5f-9da4-accd44641a68
TQID: https://experienceleague.adobe.com/-zue9aNrWtfL3MGs7OjH-1CF436mzPh50fsru8OSEq8
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: aeebb91a-f216-4d5f-8da1-3a7e6f696ed0
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
subfeature_v2:
  - id: a9cf78bf-e9e4-4836-85a5-b6b3cf93bf56
  - id: f365ec33-2b99-4b7f-b4ee-c743dd7f615f
  - id: c8d5f2ce-ba44-43e9-a2bf-94a3d7d85ec3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 4e89993a998268ae2810c949d0669bf6dc458dd6
workflow-type: tm+mt
source-wordcount: 262
ht-degree: 89%

---

# Eseguire operazioni relative al ciclo di vita dei dati {#data-hygiene}

>[!BEGINSHADEBOX]

**In questa pagina:** Configura e pianifica le operazioni del ciclo di vita dei dati in modo da poter mantenere i record accurati, utilizzati come previsto ed eliminati in linea con i criteri organizzativi.

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Le funzionalità relative al ciclo di vita dei dati sono attualmente disponibili solo per le organizzazioni che hanno acquistato le offerte aggiuntive **Healthcare Shield** e **Privacy and Security Shield**.

Man mano che i dati vengono continuamente acquisiti in Adobe Experience Platform, diventa fondamentale assicurarsi che vengano utilizzati come previsto, aggiornati quando necessario ed eliminati in base ai criteri organizzativi.

Queste attività possono essere eseguite utilizzando il menu **[!UICONTROL Ciclo di vita dei dati]** che consente di configurare e pianificare le operazioni del ciclo di vita dei dati, per la corretta manutenzione dei record.

![](assets/data-hygiene.png)


## Consigli {#data-hygiene-recommendations}

Quando esegui operazioni di igiene dei dati (ad esempio l’eliminazione di identità o set di dati), tieni presente che gli eventi di consegna storici associati alle identità eliminate non verranno più visualizzati nei rapporti standard o nelle query di datalake. Questo può causare discrepanze tra il numero di e-mail segnalate come **Consegnate** e il numero di e-mail **Ricevute** nelle caselle in entrata dei destinatari, in particolare per i percorsi meno recenti.

Prima di eseguire eliminazioni su larga scala, convalida ed esporta tutti i dati di consegna o di reporting richiesti. Se è necessaria la riconciliazione dopo l’igiene dei dati, coordinati con il supporto Adobe per accedere ai registri archiviati o utilizzare le query del set di dati dell’Evento feedback dei messaggi per i dati recenti.

## Ulteriori informazioni {#data-hygiene-learn-more}

Per ulteriori informazioni su Privacy Service e su come seguire le operazioni relative al ciclo di vita dei dati, consulta la documentazione di Adobe Experience Platform:

* [Panoramica di Privacy Service](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=it)
* [Ciclo di vita dei dati in Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/hygiene/home.html?lang=it)
