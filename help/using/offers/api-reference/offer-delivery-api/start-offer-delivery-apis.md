---
title: Introduzione alla recapitabilità delle offerte tramite API
description: Ulteriori informazioni sulle API disponibili per distribuire le offerte personalizzate.
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 7bc1a4ec-113c-4af7-b549-ee17b843b818
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '469'
ht-degree: 4%

---

# Introduzione alla recapitabilità delle offerte tramite API {#about-decisioning-apis}

Puoi distribuire le offerte utilizzando l&#39;API **Decisioning** o **Edge Decisioning**. Inoltre, l&#39;API **Batch Decisioning** ti consente di distribuire offerte a tutti i profili di un determinato pubblico in una chiamata. Il contenuto dell’offerta per ogni profilo del pubblico viene inserito in un set di dati Adobe Experience Platform dove è disponibile per flussi di lavoro batch personalizzati.

In questa pagina trovi informazioni su funzionalità specifiche disponibili con le API **Decisioning** e **Edge Decisioning**. Anche se entrambi consentono di distribuire offerte ai clienti, ti consigliamo di utilizzare l&#39;API **Edge Decisioning** ogni volta che è possibile per i casi di utilizzo in entrata e per garantire una latenza e una velocità effettiva migliori sulla piattaforma.

Per ulteriori informazioni su come utilizzare le API, consulta le sezioni seguenti:

* [API Decisioning](decisioning-api.md)
* [API Edge Decisioning](edge-decisioning-api.md)
* [API Batch Decisioning](batch-decisioning-api.md)

## Funzionalità API di Edge Decisioning {#edge}

**Richiesta univoca per eventi esperienza e richieste di decisioni**

Con l’API Edge Decisioning, puoi inviare una singola richiesta dell’evento esperienza insieme alla richiesta di decisione, anziché avere due richieste diverse.

Ad esempio, se un cliente visita il tuo sito web, la richiesta includerà l’evento esperienza (la visita del cliente alla pagina) e otterrà nuovamente un’offerta per popolare la pagina visitata.

**Archiviazione dati contestuali in Adobe Experience Platform**

I dati contestuali si riferiscono a dati che si conoscono solo al momento in cui si desidera che venga restituita un’offerta. Ad esempio, il colore dell’articolo acquistato, il tempo al momento dell’acquisto, ecc.

Quando si trasmettono dati contestuali con una richiesta API di Edge Decisioning, i dati vengono memorizzati nel profilo di Adobe Experience Platform, consentendo un riutilizzo futuro.

>[!NOTE]
>
>Per memorizzare i dati contestuali, è necessario configurare uno schema XDM dedicato.

**Aggiornamento contatore limite di frequenza**

Se per alcune offerte è stato abilitato il limite di frequenza per definire la frequenza con cui viene reimpostato il conteggio dei limiti, il contatore viene aggiornato e disponibile in una decisione API di Edge Decisioning in meno di 3 secondi. [Scopri come aggiungere vincoli a un&#39;offerta](../../offer-library/add-constraints.md)

## Funzionalità API di decisioning {#decisioning}

Le funzionalità elencate di seguito sono disponibili solo con l’API Decisioning. Se devi sfruttarne una per soddisfare le tue esigenze, utilizza l’API Decisioning. In caso contrario, consigliamo di utilizzare le API Edge Decisioning.

* **Contenuto e caratteristiche dell&#39;offerta**: puoi scegliere di non restituire il contenuto e le caratteristiche di un&#39;offerta utilizzando un&#39;opzione dedicata.
* **Metadati offerta**: abilita un&#39;opzione per restituire i metadati di un&#39;offerta.
* **Criterio di unione**: utilizza nella richiesta un criterio di unione diverso da quello associato alla sandbox.
* **Eventi decisionali e limiti di frequenza**: impediscono che gli eventi decisionali vengano conteggiati da qualsiasi limite di frequenza che si verifica.
* **Proposte duplicate**: abilita un&#39;opzione per non deduplicare le proposte.
