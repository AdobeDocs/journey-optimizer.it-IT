---
solution: Journey Optimizer
product: journey optimizer
title: Componente aggiuntivo prestazioni per velocità effettiva - (push) unitario - Consegna messaggi
description: Scopri come configurare e utilizzare il componente aggiuntivo Performance per la velocità effettiva (push) unitaria e la consegna dei messaggi in Adobe Journey Optimizer.
feature: Push
topic: Content Management
role: User
level: Intermediate
exl-id: 2d0677ad-41c8-4299-a7c8-0e4f8a1716f7
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2: id: c96d2aa5-76a2-443d-8d23-5de95577c909
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b6b77c26-2a48-4a62-9ceb-5ae67f4dfde5
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 4aebdb06094628cfe7393c7f7b41e5fe0ee9df13
workflow-type: tm+mt
source-wordcount: 252
ht-degree: 3%

---


# Componente aggiuntivo prestazioni per velocità effettiva - (push) unitario - Consegna messaggi {#performance-add-on-for-throughput-push-unitary-mes}

>[!AVAILABILITY]
>
>Questa funzionalità è disponibile da **AJO26.7** (2026-07-27).

## Panoramica {#overview}

Adobe Journey Optimizer presenta **il componente aggiuntivo Performance per la velocità effettiva - (Push) Unitario - Consegna messaggi**, consentendo alle organizzazioni di fornire ai clienti esperienze personalizzate più rilevanti tra i canali push.

Questa pagina spiega come configurare e utilizzare questa funzione nelle campagne e nei percorsi.

## Prerequisiti {#prerequisites}

Prima di iniziare:

* Hai accesso a Adobe Journey Optimizer con le autorizzazioni **Push** richieste.
* È configurata una superficie di canale push. Consulta [Configurare il canale push](../configuration/channel-surfaces.md).

## Come funziona {#how-it-works}

Componente aggiuntivo delle prestazioni per la velocità effettiva (push) unitaria: la distribuzione dei messaggi si integra direttamente con il motore di esecuzione di AJO. Quando un profilo raggiunge un’azione push in un percorso o in una campagna, la funzione applica i parametri configurati al momento dell’invio.

Funzionalità principali:

* **Personalizzazione a livello di profilo**: le impostazioni si adattano per destinatario utilizzando gli attributi di profilo e contesto.
* Supporto per **Percorso e campagna**: funziona sia in percorsi orchestrati che in campagne singole.
* **Metriche in tempo reale**. I risultati verranno visualizzati nei [report push](../reports/push-report.md).

## Configurare il componente aggiuntivo Performance per la velocità effettiva {#configure}

1. Nel menu a sinistra di AJO, passa a **Canali** > **Configurazioni push**.
1. Seleziona o crea una configurazione di canale.
1. Nella sezione **Componente aggiuntivo prestazioni per**, abilitare la funzionalità.
1. Imposta i parametri richiesti.
1. Fai clic su **Salva**.

>[!NOTE]
>
>Le modifiche alla configurazione vengono applicate alle nuove esecuzioni del percorso. I percorsi in corso non subiscono modifiche.

## Argomenti correlati {#related-topics}

* [Introduzione alla funzione push](get-started-push.md)
* [Creare una notifica push](create-push.md)
* [Note sulla versione di AJO26.7](../rn/release-notes.md)
