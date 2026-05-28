---
solution: Journey Optimizer
product: journey optimizer
title: Verifica i messaggi di testo
description: Scopri come controllare e inviare i messaggi LINE in Journey Optimizer
feature: Line
topic: Content Management
role: User
level: Beginner
exl-id: fd8437c6-0052-4116-af60-5624569bda65
TQID: https://experienceleague.adobe.com/Bfu4AL1axI4XUq0PKXuN0PnnxNvq4MB-O7Bzz66mtbU
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: f8d2e9f0-69c9-40cd-890f-71336c8dfff7
  - id: e09fc1e6-407c-418f-adc5-e2ffe8b8986e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 252
ht-degree: 0%

---

# Controllare e inviare il messaggio LINE {#send-line}

## Anteprima del messaggio di testo {#preview-line}

Una volta definito il contenuto del messaggio, puoi utilizzare profili di test o dati di input di esempio caricati da un file CSV/JSON, o aggiunti manualmente per visualizzarne l’anteprima. Se hai inserito dei contenuti personalizzati, puoi controllare come questi contenuti vengono visualizzati nel messaggio. [Scopri come verificare il contenuto utilizzando dati di input di esempio](../test-approve/simulate-sample-input.md)

A tale scopo, fai clic su **[!UICONTROL Simula contenuto]**, quindi controlla il messaggio utilizzando i dati del profilo di test.

Informazioni dettagliate su come visualizzare in anteprima e testare il contenuto sono disponibili nella sezione [Gestione dei contenuti](../content-management/preview-test.md).

## Convalidare il contenuto {#line-validate}

È necessario controllare gli avvisi nella sezione superiore dell’editor. Alcuni sono semplici avvisi, altri possono impedirti di inviare il messaggio. Possono verificarsi due tipi di avvisi: avvisi ed errori.

* **Avvisi** fai riferimento a consigli e best practice. Ad esempio, se il messaggio di testo è vuoto, viene visualizzato un messaggio di avviso.

* **Gli errori** impediscono di testare o attivare il percorso o di pubblicare la campagna, purché non siano risolti. Ad esempio, un messaggio di errore ti avvisa quando manca la riga dell’oggetto.

## Inviare i messaggi LINE {#line-send}

>[!IMPORTANT]
>
> Se la campagna è soggetta a un criterio di approvazione, per poter inviare i messaggi di testo dovrai richiedere l’approvazione. [Ulteriori informazioni](../test-approve/gs-approval.md)

Quando il messaggio LINE è pronto, completa la configurazione del [percorso](../building-journeys/journey-gs.md) o [campagna](../campaigns/create-campaign.md) per inviarlo.
