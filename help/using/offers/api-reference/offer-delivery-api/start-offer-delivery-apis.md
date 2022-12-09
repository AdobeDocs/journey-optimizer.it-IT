---
title: Guida introduttiva alle API di consegna delle offerte
description: Ulteriori informazioni sulle API disponibili per distribuire offerte personalizzate.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 7bc1a4ec-113c-4af7-b549-ee17b843b818
source-git-commit: bf738ebac09d5c852872a8ea85f6532ad9d4222d
workflow-type: tm+mt
source-wordcount: '442'
ht-degree: 0%

---

# Guida introduttiva alle API di consegna delle offerte {#about-decisioning-apis}

Puoi fornire offerte utilizzando **Decisioni** o **Edge Decisioning** API. Inoltre, la **Decisioni in batch** L’API ti consente di offrire a tutti i profili in un dato segmento in una chiamata. Il contenuto dell’offerta per ogni profilo del segmento viene inserito in un set di dati di Adobe Experience Platform, dove è disponibile per flussi di lavoro batch personalizzati.

In questa pagina trovi informazioni su funzionalità specifiche disponibili con la **Decisioni** e **Edge Decisioning** API. Sebbene entrambi consentano di fornire offerte ai clienti, si consiglia di utilizzare **Edge Decisioning** API ogni volta che è possibile per i casi di utilizzo in entrata e per garantire una maggiore latenza e velocità effettiva sulla piattaforma.

|  | Richieste/sec | Latenza |
|---|---|---|
| Decisioning API | 2000 | &lt;500 ms |
| API di Edge Decisioning | 5000 | &lt;250 ms |

Per ulteriori informazioni su come utilizzare le API, consulta queste sezioni:
* [Decisioning API](decisioning-api.md)
* [API di Edge Decisioning](edge-decisioning-api.md)
* [API Batch Decisioning](batch-decisioning-api.md)

## Funzionalità API di Edge Decisioning {#edge}

**Richiesta univoca per eventi di esperienza e richieste di decisione**

Con l’API Edge Decisioning, puoi inviare una sola richiesta all’evento esperienza stesso insieme alla richiesta decisionale, anziché due richieste diverse.

Ad esempio, se un cliente visita il tuo sito web, la richiesta includerà l’evento esperienza (la visita del cliente alla pagina) e riceverà un’offerta per compilare nuovamente la pagina visitata.

**Archiviazione dei dati contestuali in Adobe Experience Platform**

I dati contestuali si riferiscono ai dati che conosci solo al momento in cui vuoi recuperare un’offerta. Ad esempio, il colore dell’articolo acquistato, il tempo al momento dell’acquisto, ecc.

Quando si trasmettono dati contestuali con una richiesta API di Edge Decisioning, questi vengono memorizzati nel profilo Adobe Experience Platform, consentendo un riutilizzo futuro.

>[!NOTE]
>
>Per memorizzare i dati contestuali, devi disporre di uno schema XDM dedicato.

## Decisioni delle funzionalità API {#decisioning}

Le funzionalità elencate di seguito sono disponibili solo con l’API Decisioning. Se devi sfruttare uno di questi per soddisfare i tuoi requisiti, utilizza l’API Decisioning. In caso contrario, si consiglia di utilizzare le API di Edge Decisioning.

* **Eventi di esperienza**: sfrutta gli eventi di esperienza per creare le regole decisionali.
* **Contenuto e caratteristiche dell’offerta**: puoi scegliere di non restituire il contenuto e le caratteristiche di un’offerta utilizzando un’opzione dedicata.
* **Metadati delle offerte**: abilita un’opzione per restituire i metadati di un’offerta.
* **Criteri di unione**: utilizza nella richiesta un criterio di unione diverso da quello associato alla sandbox.
* **Decisioni degli eventi e limiti di frequenza**: impedire che gli eventi decisionali vengano conteggiati da qualsiasi limite di frequenza che si verifica.
* **Proposte duplicate**: abilitare un&#39;opzione per non deduplicare le proposizioni.
