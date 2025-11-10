---
title: Guardrail e limitazioni per la funzione Decisioni
description: Ulteriori informazioni su Guardrail e limitazioni di Decisioning.
feature: Decisioning
role: User
level: Intermediate
exl-id: 73548973-ff8d-4d6c-b383-dd3679fa159a
version: Journey Orchestration
source-git-commit: 0b94bfeaf694e8eaf0dd85e3c67ee97bd9b56294
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 5%

---

# Guardrail e limitazioni per la funzione Decisioni {#decisioning-guardrails}

Per garantire un utilizzo ottimale delle decisioni, tieni presenti le seguenti protezioni e limitazioni.

L&#39;elenco completo dei guardrail e delle limitazioni di [!DNL Journey Optimizer] è disponibile in [questa sezione](../start/guardrails.md).

## Richieste di decisioni {#decision-requests}

|| Guardrail | Limite |
|| ------- | ------- |
|| Richiesta API di esperienza basata su codice con criteri decisionali utilizzando la segmentazione di Edge | 1500 |
|| Richiesta API di esperienza basata su codice con criterio di decisione che non utilizza la segmentazione di Edge | 5000 |
|| Numero massimo di URI di superficie per richiesta di Edge Decisioning | 30 |

## Raccolte elementi {#item-collections}

|| Guardrail | Limite |
|| ------- | ------- |
|| Raccolte elementi | 10K |
|| Totale elementi offerta per raccolta articoli | 500 |

## Criterio di decisione {#decision-policy}

|| Guardrail | Limite |
|| ------- | ------- |
|| Numero di strategie di selezione e di elementi manuali per criterio di decisione | 10 |
|| Numero massimo di elementi di offerta restituiti per criterio di decisione | 30 |

## Regole di idoneità {#eligibility-rules}

|| Guardrail | Limite |
|| ------- | ------- |
|| Regole di decisione totali e formule di classificazione | 10K combinati |
|| Numero massimo di attributi di profilo per regola | 25 |
|| Numero massimo di attributi di dati contestuali per regola | 30 |
|| Dimensione massima della regola Pql | 15K (UTF-8) |
|| Numero massimo di livelli di nidificazione | 30 |

## Formule di classificazione {#ranking-formulas}

|| Guardrail | Limite |
|| ------- | ------- |
|| Dimensione massima della formula di classificazione PQL | 8.000 (UTF-8) |
|| Numero massimo di attributi di profilo |25 |
|| Numero massimo di attributi di dati contestuali | 30 |
|| Numero massimo di livelli di nidificazione | 30 |

## Altre {#others}

|| Guardrail | Limite |
|| ------- | ------- |
|| Numero di attributi personalizzati per schema catalogo offerte | 100 |
|| Elementi offerta totali | 10K |
|| Posizionamenti totali | 1 K |
|| Modello di classificazione IA | 5 |
|| Regole di frequenza: numero massimo di regole di limite per offerta | 10 |

## Configurazioni  {#configurations}

Il numero totale di configurazioni supportate da Decisioning non può superare i 20.000.

Il conteggio di configurazione totale è il numero totale di [regole di limite](items.md#capping) esistenti nella sandbox.
