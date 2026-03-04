---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Guardrail e limitazioni per la gestione delle decisioni
description: Ulteriori informazioni sui guardrail e le limitazioni della gestione delle decisioni.
badge: label="Legacy" type="Informative"
feature: Decision Management
role: User
level: Intermediate
exl-id: d2872bd3-42f8-4744-bb5b-41c49340098a
version: Journey Orchestration
source-git-commit: 90b7d9bfe40e6d68e22a9f1aa8ef6d302a1035d9
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 11%

---

# Guardrail e limitazioni per la gestione delle decisioni {#decision-management-guardrails}

>[!IMPORTANT]
>
>In questa pagina sono illustrati i guardrail per la funzionalità precedente di **gestione delle decisioni**. Se utilizzi **Decisioning**, l&#39;attuale funzionalità di decisioning di [!DNL Adobe Journey Optimizer] disponibile tramite l&#39;esperienza basata sul codice e i canali e-mail, fai riferimento a [Guardrail e limitazioni di Decisioning](../experience-decisioning/decisioning-guardrails.md).
>
>Non sei sicuro di quale funzionalità stai utilizzando? [Informazioni su Decisioning](../experience-decisioning/gs-experience-decisioning.md).

Questa pagina si applica agli utenti che ancora lavorano con il sistema legacy di gestione delle decisioni. Per garantire un utilizzo ottimale, tieni presenti i seguenti guardrail e limitazioni.

L&#39;elenco completo dei guardrail e delle limitazioni di [!DNL Journey Optimizer] è disponibile in [questa sezione](../start/guardrails.md).

## Richieste di decisioni

La velocità effettiva di consegna corrisponde al numero di risposte alle decisioni che possono essere fornite dal servizio app di gestione delle decisioni in un determinato periodo di tempo.

| Guardrail | Limite |
| ------- | ------- |
| Decisioning delle richieste API al secondo | 500 per organizzazione |
| Richieste API di Edge Decisioning al secondo con segmentazione di Edge | 1.500 per organizzazione |
| Richieste API di Edge Decisioning al secondo senza segmentazione di Edge | 5.000 per organizzazione |
| Offerte restituite per risposta | Fino a 30 per ambito di decisione o 100 in totale |
| Numero massimo di regole di offerta interessate per richiesta | 100 |

## Decisioni

| Guardrail | Limite |
| ------- | ------- |
| Totale decisioni | 10K |
| Decisioni live | 1 K |
| Posizionamenti per decisione | 30 |

## Raccolte

| Guardrail | Limite |
| ------- | ------- |
| Offerte per raccolta | 500 |
| Raccolte | 10K |
| Raccolte per decisione | 30 |

## Qualificatori di raccolta

| Guardrail | Limite |
| ------- | ------- |
| Qualificatore raccolta per offerta o raccolta | 20 |
| Totale qualificatori raccolta | 1.000 |

## Offerte

| Guardrail | Limite |
| ------- | ------- |
| Offerte totali | 10K |
| Numero massimo di **offerte attive** per sandbox | 10K |
| Dimensione massima delle offerte, inclusi gli attributi (1 KB), fino a 30 attributi | 1KB |
| Dimensione massima della rappresentazione dell’offerta (totale per tutti i posizionamenti) | 1KB |

## Regole di idoneità

| Guardrail | Limite |
| ------- | ------- |
| Regole di decisione totali e formule di classificazione | 10K combinati |
| Numero massimo di attributi di profilo per regola | 25 |
| Numero massimo di attributi di dati contestuali per regola | 30 |
| Dimensione massima della regola PQL | 15K (UTF-8) |
| Numero massimo di livelli di nidificazione | 30 |

## Formule di ranking

| Guardrail | Limite |
| ------- | ------- |
| Dimensione massima della formula di classificazione PQL | 8.000 (UTF-8) |
| Numero massimo di attributi di profilo | 25 |
| Numero massimo di attributi di dati contestuali | 30 |
| Numero massimo di livelli di nidificazione | 30 |

## Altre

| Guardrail | Limite |
| ------- | ------- |
| Posizionamenti | 1000 |
| Modello di classificazione IA | 5 |
| Limite di frequenza: numero massimo di regole di limite per offerta | 10 |

## Configurazioni {#configurations}

Il numero totale di configurazioni supportate da Gestione decisioni non può superare i 20.000.

Il conteggio di configurazione totale è il numero totale di [regole di limite](offer-library/add-constraints.md#capping) esistenti nella sandbox. Per ogni regola di limite applicata a tutti i [posizionamenti](offer-library/creating-placements.md), la regola deve essere moltiplicata per tutti i posizionamenti associati all&#39;offerta specificata.
