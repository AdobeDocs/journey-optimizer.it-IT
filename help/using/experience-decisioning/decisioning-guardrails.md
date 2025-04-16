---
title: Guardrail e limitazioni per la funzione Decisioni
description: Ulteriori informazioni su Guardrail e limitazioni di Decisioning.
feature: Decisioning
role: User
level: Intermediate
exl-id: 73548973-ff8d-4d6c-b383-dd3679fa159a
source-git-commit: e539d694e8fb91b6a8c7ba7ff5a2bb0905651f81
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 15%

---

# Guardrail e limitazioni per la funzione Decisioni {#decisioning-guardrails}

Per garantire un uso ottimale del processo decisionale, tieni presente i seguenti guardrail e limitazioni.

L&#39;elenco completo dei guardrail e delle [!DNL Journey Optimizer] limitazioni è disponibile in [questa sezione](../start/guardrails.md).

## Richieste di decisioni

| Guardrail | Limite |
| ------- | ------- |
| Richiesta API di esperienza basata su codice con criteri decisionali utilizzando la segmentazione di Edge | 1500 |
| Richiesta API di esperienza basata su codice con criterio di decisione che non utilizza la segmentazione di Edge | 5000 |

## Raccolte di elementi

| Guardavia | Limite |
| ------- | ------- |
| Raccolte di articoli | 10K |
| Totale elementi offerta per raccolta articoli | 500 |

## Criterio di decisione

| Guardrail | Limite |
| ------- | ------- |
| Numero di strategie di selezione e di elementi manuali per criterio di decisione | 10 |
| Numero massimo di articoli dell&#39;offerta restituiti per decisione regola | 30 |

## Eligibility rules (Regole di idoneità)

| Guardrail | Limite |
| ------- | ------- |
| Regole di decisione totali e formule di classificazione | 10K combinati |
| Numero massimo di attributi di profilo per regola | 25 |
| Numero massimo di attributi di dati contestuali per regola | 30 |
| Dimensione massima del regola pql | 15K (UTF-8) |
| Numero massimo di livelli di nidificazione | 30 |

## Formule di classificazione

| Guardrail | Limite |
| ------- | ------- |
| Dimensione massima della formula di classificazione PQL | 8.000 (UTF-8) |
| Numero massimo di attributi del profilo | 25 |
| Numero massimo di attributi di dati contestuali | 30 |
| Numero massimo di livelli di nidificazione | 30 |

## Altri

| Guardrail | Limite |
| ------- | ------- |
| Numero di attributi personalizzati per schema del catalogo delle offerte | 100 |
| Elementi offerta totali | 10K |
| Posizionamenti totali | 1 K |
| Modello di classificazione IA | 5 |
| Regole di frequenza: numero massimo di regole di limite per offerta | 10 |
