---
product: experience platform
solution: Experience Platform
title: Introduzione ai dati contestuali
description: Scopri come sfruttare i dati contestuali nella gestione delle decisioni.
badge: label="Legacy" type="Informative"
feature: Decision Management
role: Developer
level: Experienced
exl-id: 4e736f9d-0f05-4a79-8ebf-ea22517d78a9
version: Journey Orchestration
source-git-commit: 0b94bfeaf694e8eaf0dd85e3c67ee97bd9b56294
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 5%

---

# Introduzione ai dati contestuali {#context-data}

I dati inviati come parte della richiesta di decisioni sono considerati dati contestuali. Puoi sfruttare i dati contestuali nel motore decisionale, ad esempio per progettare una regola di decisione che richiede che il tempo attuale sia di ≥80 gradi al momento della richiesta di decisione.

I dati contestuali sono definiti in modo diverso tra le richieste API **Decisioning** e **Edge Decisioning**. Per entrambi i tipi di richieste, i dati contestuali possono essere utilizzati nelle regole di idoneità o nelle formule di classificazione, ma solo le richieste API di Edge Decisioning possono utilizzare i dati contestuali per personalizzare il contenuto.

Prima di iniziare, controlla le seguenti protezioni e limitazioni:

* A causa della differenza nel modo di passare il contesto tra le chiamate Decisioning e Edge Decisioning, le regole di idoneità basate sul contesto e le formule di classificazione non sono intercambiabili tra le chiamate Decisioning e Edge Decisioning.
* Il test con il parametro `dryrun` è possibile solo con l&#39;API Decisioning. Non è disponibile con l’API Edge Decisioning. L&#39;impostazione di questo parametro su `true` con l&#39;API Decisioning non influisce sui limiti e sul numero di proposte.

Informazioni dettagliate su come utilizzare i dati contestuali in ogni API, consulta queste sezioni:

* [Utilizzare i dati contestuali nelle richieste di Edge Decisioning](context-data-edge.md)
* [Utilizzare i dati contestuali nelle richieste Decisioning](context-data-decisioning.md)
