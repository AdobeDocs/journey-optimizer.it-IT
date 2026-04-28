---
solution: Journey Optimizer
product: journey optimizer
title: Integrazione fornitore
description: Utilizza le integrazioni Adobe Journey Optimizer con qualsiasi piattaforma esterna che espone un’API valida e i pattern di fornitori testati dagli ingegneri per garantirne l’affidabilità durante la progettazione della configurazione.
feature: Integrations
topic: Content Management
role: User
level: Intermediate
hide: true
keywords: integrazione, fornitore, terze parti
source-git-commit: 16eb46843d0369ae14f004a5e0f9e743cad3170b
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 1%

---


# Integrazione fornitori {#vendor-integration}

>[!BEGINSHADEBOX]

Sommario:

* [Utilizzare le integrazioni](integrations.md)
* **[Introduzione all&#39;integrazione con i fornitori](vendor-integration-gs.md)**
* [Fornitori disponibili](vendor-integration.md)
* [Domande frequenti](vendor-integration-faq.md)

>[!ENDSHADEBOX]

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

* **Sistema di gestione dei contenuti:** [Contentful](#contentful), [Sitecore](#sitecore), [Salsify](#salsify), [Contentstack](#contentstack), [Akeneo](#akeneo), [Magnolia](#magnolia)
* **Fedeltà e premi:** [Voucherify](#voucherify), [Talon.One](#talon-one), [Antavo](#antavo), [Fedeltà Salesforce](#salesforce-loyalty), [Capillare](#capillary)
* **Modelli, personalizzazione e consigli:** [Stensul](#stensul), [Marigold](#marigold), [Consigli di Adobe Target](#adobe-target-recommendations)
* **Dati, meteo e operazioni:** [AccuWeather](#accuweather), [ShipStation](#shipstation), [RevenueCat](#revenuecat), [Databricks](#databricks)
* **Recensioni, consenso e social:** [Bynder](#bynder), [Trustpilot](#trustpilot), [Bazaarvoice](#bazaarvoice), [OneTrust](#onetrust), [Meta](#meta), [Aprimo](#aprimo), [Epsilon (Epsilon3)](#epsilon)
