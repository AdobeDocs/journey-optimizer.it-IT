---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Introduzione ai dati contestuali
description: Scopri come sfruttare i dati contestuali nella gestione delle decisioni.
badge: label="Legacy" type="Informative"
feature: Decision Management
role: Developer
level: Experienced
exl-id: 4e736f9d-0f05-4a79-8ebf-ea22517d78a9
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/aVm2FFqkJWN-k1qngYsp94FgKIZWaLCMUneFd0rVNpA
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
  - id: edbd1a0e-46c8-49da-8c10-dba9ec80bba9
feature_v2:
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 229
ht-degree: 12%

---

# Introduzione ai dati contestuali {#context-data}

>[!TIP]
>
>La funzione Decisioni, la nuova funzionalità decisionale di [!DNL Adobe Journey Optimizer], è ora disponibile tramite i canali e-mail e di esperienza basati su codice. [Ulteriori informazioni](../experience-decisioning/gs-experience-decisioning.md)

I dati inviati come parte della richiesta di decisioni sono considerati dati contestuali. Puoi sfruttare i dati contestuali nel motore decisionale, ad esempio per progettare una regola di decisione che richiede che il tempo attuale sia di ≥80 gradi al momento della richiesta di decisione.

I dati contestuali sono definiti in modo diverso tra le richieste API **Decisioning** e **Edge Decisioning**. Per entrambi i tipi di richieste, i dati contestuali possono essere utilizzati nelle regole di idoneità o nelle formule di classificazione, ma solo le richieste API di Edge Decisioning possono utilizzare i dati contestuali per personalizzare il contenuto.

Prima di iniziare, controlla le seguenti protezioni e limitazioni:

* A causa della differenza nel modo di passare il contesto tra le chiamate Decisioning e Edge Decisioning, le regole di idoneità basate sul contesto e le formule di classificazione non sono intercambiabili tra le chiamate Decisioning e Edge Decisioning.
* Il test con il parametro `dryrun` è possibile solo con l&#39;API Decisioning. Non è disponibile con l’API Edge Decisioning. L&#39;impostazione di questo parametro su `true` con l&#39;API Decisioning non influisce sui limiti e sul numero di proposte.

Informazioni dettagliate su come utilizzare i dati contestuali in ogni API, consulta queste sezioni:

* [Utilizzare i dati contestuali nelle richieste di Edge Decisioning](context-data-edge.md)
* [Utilizzare i dati contestuali nelle richieste Decisioning](context-data-decisioning.md)
