---
title: Introduzione alla recapitabilità delle offerte tramite API
description: Ulteriori informazioni sulle API disponibili per distribuire le offerte personalizzate.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 7bc1a4ec-113c-4af7-b549-ee17b843b818
source-git-commit: ccc3ad2b186a64b9859a5cc529fe0aefa736fc00
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 4%

---

# Introduzione alla recapitabilità delle offerte tramite API {#about-decisioning-apis}

Puoi distribuire le offerte utilizzando **Decisioning** o **Edge Decisioning** API. Inoltre, il **Batch Decisioning** API ti consente di distribuire offerte a tutti i profili in un determinato pubblico in una chiamata. Il contenuto dell’offerta per ogni profilo del pubblico viene inserito in un set di dati Adobe Experience Platform dove è disponibile per flussi di lavoro batch personalizzati.

In questa pagina trovi informazioni su funzionalità specifiche disponibili con **Decisioning** e **Edge Decisioning** API. Sebbene entrambi consentano di offrire offerte ai clienti, si consiglia di utilizzare **Edge Decisioning** Se possibile, API per casi di utilizzo in entrata e per garantire una migliore latenza e velocità effettiva sulla piattaforma.


Per ulteriori informazioni su come utilizzare le API, consulta le sezioni seguenti:
* [API Decisioning](decisioning-api.md)
* [API Edge Decisioning](edge-decisioning-api.md)
* [API Batch Decisioning](batch-decisioning-api.md)

## Funzionalità API di Edge Decisioning {#edge}

**Richiesta univoca per eventi di esperienza e richieste di decisioni**

Con l’API Edge Decisioning, puoi inviare in un’unica richiesta l’evento esperienza stesso insieme alla richiesta decisioning, anziché avere due richieste diverse.

Ad esempio, se un cliente visita il tuo sito web, la richiesta includerà l’evento esperienza (la visita del cliente alla pagina) e otterrà nuovamente un’offerta per popolare la pagina visitata.

**Archiviazione dei dati contestuali in Adobe Experience Platform**

I dati contestuali si riferiscono a dati che si conoscono solo al momento in cui si desidera che venga restituita un’offerta. Ad esempio, il colore dell’articolo acquistato, il tempo al momento dell’acquisto, ecc.

Quando si trasmettono dati contestuali con una richiesta API Edge Decisioning, i dati vengono memorizzati nel profilo di Adobe Experience Platform, consentendo un riutilizzo futuro.

>[!NOTE]
>
>Per memorizzare i dati contestuali, è necessario configurare uno schema XDM dedicato.

## Funzionalità API di decisioning {#decisioning}

Le funzionalità elencate di seguito sono disponibili solo con l’API Decisioning. Se devi sfruttarne una per soddisfare le tue esigenze, utilizza l’API Decisioning. In caso contrario, consigliamo di utilizzare le API Edge Decisioning.

* **Eventi esperienza**: sfrutta gli eventi di esperienza per creare regole decisionali.
* **Contenuto e caratteristiche dell’offerta**: puoi scegliere di non restituire il contenuto e le caratteristiche di un’offerta utilizzando un’opzione dedicata.
* **Metadati offerta**: abilita un’opzione per restituire i metadati di un’offerta.
* **Criterio di unione**: utilizza nella richiesta un criterio di unione diverso da quello associato alla sandbox.
* **Eventi decisionali e quota limite**: gli eventi di blocco delle decisioni non vengono conteggiati da alcun limite di frequenza che si verifica.
* **Proposte duplicate**: abilita un’opzione per non deduplicare le proposte.
