---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Introduzione all’esportazione del catalogo delle offerte
description: Scopri come esportare il catalogo delle offerte come set di dati
badge: label="Legacy" type="Informative"
feature: Decision Management, Datasets
topic: Integrations
role: User, Developer
level: Intermediate
exl-id: f30abea1-b204-4470-9836-75fae916bbb1
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/71W86v7R-wgsa7JDTE3d6Lddc71MOcTxrY5l0Ts600o
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
  - id: edbd1a0e-46c8-49da-8c10-dba9ec80bba9
feature_v2:
  - id: ed0d8d0e-04b9-4326-be72-a0fbca265377
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
  - id: fe96aceb-8194-4a8a-a6b0-75302d02804d
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 133
ht-degree: 100%

---

# Introduzione all’esportazione del catalogo delle offerte {#export-catalog}

>[!TIP]
>
>La funzione Decisioni, la nuova funzionalità decisionale di [!DNL Adobe Journey Optimizer], è ora disponibile tramite i canali e-mail e di esperienza basati su codice. [Ulteriori informazioni](../../experience-decisioning/gs-experience-decisioning.md)

Journey Optimizer consente di esportare automaticamente il catalogo delle offerte in Adobe Experience Platform.

L’esportazione crea un set di dati per ogni oggetto della Libreria di offerte (consulta [Accedere ai set di dati esportati](../export-catalog/access-dataset.md)). Include:

* Offerte personalizzate
* Offerte di fallback
* Posizionamenti
* Decisioni

Ogni volta che uno di questi oggetti viene modificato nella Libreria di offerte, viene eseguito automaticamente un nuovo processo di esportazione per aggiornare i set di dati.

>[!NOTE]
>
>Questa funzione è abilitata per impostazione predefinita. È possibile iniziare a utilizzarla senza ulteriori passaggi di attivazione. Una volta abilitata, i processi di esportazione verranno automatizzati e non sarà necessaria alcuna azione da parte tua.

<!--
>[!NOTE]
>
>This feature is not enabled by default. If you want to use it, reach out to your Adobe contact to have it activated for your catalog. Once it is enabled, export jobs will be automated and will require no action from your side.
-->
