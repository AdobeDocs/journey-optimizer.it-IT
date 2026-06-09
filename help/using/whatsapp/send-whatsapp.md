---
solution: Journey Optimizer
product: journey optimizer
title: Verifica i messaggi WhatsApp
description: Scopri come controllare e inviare messaggi WhatsApp in Journey Optimizer
feature: Whatsapp
topic: Content Management
role: User
level: Beginner
exl-id: 31acb095-de90-495f-8e8c-43a78dedfa06
TQID: https://experienceleague.adobe.com/u2OevVu38fPdytpuTmHeSdEx3Wvpih7ifk-j88rhDFI
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: f8d2e9f0-69c9-40cd-890f-71336c8dfff7
  - id: b8df23d2-98a2-4406-86cc-2babe8728d36
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: a4e4f5ca5c3eb9dbfb5691cb5de420009ed7e5a5
workflow-type: tm+mt
source-wordcount: 414
ht-degree: 2%

---

# Verificare e inviare i messaggi WhatsApp {#send-whatsapp}

## Anteprima del messaggio WhatsApp {#preview-whatsapp}

Una volta definito il contenuto del messaggio, puoi visualizzarne l’anteprima utilizzando uno dei seguenti metodi di simulazione:

* Fai clic su **[!UICONTROL Simula contenuto]** per testare le varianti di contenuto con dati di input di esempio o con generazione automatica di IA. [Scopri come simulare varianti di contenuto](../test-approve/simulate-sample-input.md)
* Fai clic su **[!UICONTROL Simula contenuto]**, quindi seleziona **[!UICONTROL Simula contenuto (profili AEP)]** dal menu a discesa per visualizzare l&#39;anteprima con i profili di test.

Informazioni dettagliate su come visualizzare in anteprima e testare il contenuto sono disponibili nella sezione [Gestione dei contenuti](../content-management/preview-test.md).

## Convalidare il contenuto {#whatsapp-validate}

È necessario controllare gli avvisi nella sezione superiore dell’editor. Alcuni sono semplici avvisi, altri possono impedirti di inviare il messaggio. Possono verificarsi due tipi di avvisi: avvisi ed errori.

* **Avvisi** fai riferimento a consigli e best practice. Ad esempio, se il messaggio di testo è vuoto, viene visualizzato un messaggio di avviso.

* **Gli errori** impediscono di testare o attivare il percorso o di pubblicare la campagna, purché non siano risolti. Ad esempio, un messaggio di errore ti avvisa quando manca la riga dell’oggetto.

## Inviare i messaggi WhatsApp {#whatsapp-send}

>[!IMPORTANT]
>
> Se la campagna è soggetta a un criterio di approvazione, per poter inviare i messaggi di testo dovrai richiedere l’approvazione. [Ulteriori informazioni](../test-approve/gs-approval.md)

Quando il messaggio WhatsApp è pronto, completa la configurazione del [percorso](../building-journeys/publish-journey.md) o [campagna](../campaigns/review-activate-campaign.md) per inviarlo.

## Analizzare le interazioni WhatsApp {#whatsapp-channel-context}

Journey Optimizer acquisisce i dati di interazione aggiuntivi restituiti dal canale WhatsApp e li memorizza nel **AJO - Set di dati evento di tracciamento e-mail** nel gruppo di campi `whatsAppChannelContext`. Utilizza questi campi per generare [tipi di pubblico](../audience/about-audiences.md), eseguire [query](../data/get-started-queries.md) e analizzare il coinvolgimento WhatsApp. [Ulteriori informazioni sui set di dati di sistema](../data/get-started-datasets.md#system-datasets).

Vengono acquisiti i seguenti campi:

| Campo | Descrizione |
|-|-|
| `messageType` | Tipo di messaggio WhatsApp (ad esempio, `templateBased`, `response`). |
| `inboundMessage` | Contenuto della risposta in entrata (ad esempio, `stop`, `start`, `subscribe`). |
| `inboundNumber` | ID mittente in cui è stato ricevuto il messaggio in entrata. |
| `channelType` | Categoria canale (`Utility`, `Marketing` o `Promotional`). |
| `profileNumber` | Numero di telefono da cui è stato ricevuto il messaggio in entrata. |
| `origTimestamp` | Timestamp originale da Meta / WhatsApp. |
| `status` | Lo stato della consegna include il feedback standardizzato del provider (`sent`, `delivered`, `bounce`, `error`, `delay`, `duplicate`, `denylist`, `exclude` o `unknown`) e il messaggio di stato del provider non elaborato. |
| `reactionEvent` | Contenuto della risposta dell’utente: emoji per le reazioni o testo del messaggio per le risposte a un messaggio specifico. |
| `reactionMessageID` | ID del messaggio originale a cui si risponde. |
| `reactionActionName` | Tipo di azione di risposta (`react`, `unreact` o `reply`). |
| `interactiveSelectedTitle` | Titolo selezionato dall&#39;utente da un messaggio interattivo WhatsApp. |
| `interactiveType` | Tipo di messaggio interattivo (`list reply`, `button reply` o `button`). |
| `interactiveSelectedDescription` | Descrizione dell&#39;opzione interattiva WhatsApp selezionata. |
| `interactiveSelectedID` | ID dell’opzione selezionata da WhatsApp. |

Per eseguire query su questo set di dati, utilizzare la tabella `ajo_email_tracking_experience_event_dataset` in Query Service. Per i modelli di query e i casi d&#39;uso correlati, vedi [Esempi di query per set di dati](../data/datasets-query-examples.md).
