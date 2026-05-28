---
solution: Journey Optimizer
product: journey optimizer
title: Integrazione fornitore
description: Utilizza le integrazioni Adobe Journey Optimizer con qualsiasi piattaforma esterna che espone un’API valida e i pattern di fornitori testati dagli ingegneri per garantirne l’affidabilità durante la progettazione della configurazione.
feature: Integrations
topic: Content Management
role: User
level: Intermediate
keywords: integrazione, fornitore, terze parti
subfeature_v2: []
feature_v2: id: fe96aceb-8194-4a8a-a6b0-75302d02804d
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 375
ht-degree: 0%

---


# Integrazione fornitori {#vendor-integration}

È possibile utilizzare **Integrazioni** in Adobe Journey Optimizer per chiamare **sistemi esterni tramite HTTP** quando ogni sistema espone un **endpoint API** adatto al tuo caso d&#39;uso ed è compatibile con il modo in cui le integrazioni emettono richieste e utilizzano risposte. Per un flusso di lavoro completo, vedi [Operazioni con le integrazioni](integrations.md).

L’elenco delle soluzioni di terze parti descritte è illustrativo, non esaustivo. Possono essere utilizzate altre piattaforme se soddisfano i requisiti del prodotto.

## Guardrail operativi {#operational-guardrails}

Applica quanto segue quando configuri un’integrazione in questa guida o in un fornitore simile:

* **Formato risposta:** le integrazioni mappano i campi delle **risposte JSON** o **risposte HTML**. Progetta le chiamate in modo che l’API restituisca JSON o HTML adatti per la mappatura al momento dell’authoring.
* **Payload e campi:** Richiedi e mappa solo gli attributi necessari. Risposte più piccole riducono la latenza e limitano l&#39;esposizione dei dati sensibili.
* **Forma endpoint:** preferire il recupero stabile **di risorse singole** (ad esempio una voce, un prodotto o un membro) rispetto agli endpoint di tipo elenco esteso o impaginazione quando il prodotto prevede ricerche mirate. Consulta [Limitazioni ed esclusioni](#limitations-exclusions) e [Operazioni con le integrazioni](integrations.md).
* **Volume e affidabilità:** Rispetta i **limiti di tariffa** del fornitore. Configura i criteri **timeout**, **riprova** e **cache** per il tuo canale (ad esempio e-mail batch e invii transazionali) e convalida sotto carico.
* **Sicurezza:** archivia e ruota i token, le chiavi API e le credenziali OAuth in base ai criteri della tua organizzazione. Non incorporare segreti nel contenuto del messaggio.


## Limitazioni ed esclusioni {#limitations-exclusions}

L&#39;elenco delle soluzioni di terze parti è **illustrativo**, non esaustivo. Le API fornitore, gli host, i limiti di tariffa e le forme di risposta JSON o HTML possono cambiare. Conferma gli endpoint, l’autenticazione e la mappatura dei campi con la documentazione corrente del fornitore e la tua sottoscrizione. I modelli qui presuppongono **chiamate orientate alla lettura** adatte alla personalizzazione. Le integrazioni supportano la mappatura solo dalle risposte **JSON** e **HTML**. **Write-back**, **esportazioni batch** e risposte in qualsiasi altro formato non supportati.

## Navigazione rapida {#quick-navigation}

Utilizza questi collegamenti raggruppati per passare rapidamente al modello del fornitore pertinente:

* **Sistema di gestione dei contenuti:** [Contentful](vendor-integration.md#contentful), [Sitecore](vendor-integration.md#sitecore), [Salsify](vendor-integration.md#salsify), [Contentstack](vendor-integration.md#contentstack), [Akeneo](vendor-integration.md#akeneo), [Magnolia](vendor-integration.md#magnolia)
* **Fedeltà e premi:** [Voucherify](vendor-integration.md#voucherify), [Talon.One](vendor-integration.md#talon-one), [Antavo](vendor-integration.md#antavo), [Fedeltà Salesforce](vendor-integration.md#salesforce-loyalty), [Capillare](vendor-integration.md#capillary)
* **Modelli, personalizzazione e consigli:** [Stensul](vendor-integration.md#stensul), [Marigold](vendor-integration.md#marigold), [Consigli di Adobe Target](vendor-integration.md#adobe-target-recommendations)
* **Dati, meteo e operazioni:** [AccuWeather](vendor-integration.md#accuweather), [ShipStation](vendor-integration.md#shipstation), [RevenueCat](vendor-integration.md#revenuecat), [Databricks](vendor-integration.md#databricks)
* **Recensioni, consenso e social:** [Bynder](vendor-integration.md#bynder), [Trustpilot](vendor-integration.md#trustpilot), [Bazaarvoice](vendor-integration.md#bazaarvoice), [OneTrust](vendor-integration.md#onetrust), [Meta](vendor-integration.md#meta), [Aprimo](vendor-integration.md#aprimo), [Epsilon (Epsilon3)](vendor-integration.md#epsilon)
