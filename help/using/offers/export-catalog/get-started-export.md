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
source-git-commit: d6a9a8a392f0492aa6e4f059198ce77b6b2cd962
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 100%

---

# Introduzione all’esportazione del catalogo delle offerte {#export-catalog}

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
