---
solution: Journey Optimizer
product: journey optimizer
title: Anteprima, convalida e invio del messaggio LINE
description: Scopri come visualizzare in anteprima e convalidare un messaggio LINE, risolvere avvisi ed errori, richiedere l’approvazione quando necessario e attivarlo o pubblicarlo in un percorso o in una campagna
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
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: f8d2e9f0-69c9-40cd-890f-71336c8dfff7
  - id: e09fc1e6-407c-418f-adc5-e2ffe8b8986e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: 94a7cd6e4e89b2c8a4a09cfb4fbfc173ca76c391
workflow-type: tm+mt
source-wordcount: 400
ht-degree: 2%

---


# Anteprima, convalida e invio del messaggio LINE {#send-line}

>[!BEGINSHADEBOX]

**In questa pagina:** Visualizzare in anteprima e convalidare il messaggio LINE, risolvere gli avvisi e gli errori, richiedere l&#39;approvazione quando necessario e completare la configurazione del percorso o della campagna per inviare il messaggio.

>[!ENDSHADEBOX]

## Prima di iniziare {#before-you-start}

Prima di iniziare, assicurati che:

* LINE è abilitato per la tua organizzazione. Se LINE non è disponibile, contatta il rappresentante Adobe per richiedere l’attivazione.
* In Journey Optimizer è disponibile una configurazione del canale LINE. Vedere [Configurare il canale LINE](./line-configuration.md).
* Hai aggiunto un’azione LINE a un percorso o a una campagna e definito il contenuto del messaggio. Vedere [Creare un messaggio LINE](./create-line.md).

## Anteprima del messaggio LINE {#preview-line}

Dopo aver definito il contenuto del messaggio, utilizzare **[!UICONTROL Simula contenuto]** per visualizzare l&#39;anteprima del messaggio prima di inviarlo.

È possibile utilizzare una delle seguenti opzioni:

| Opzione simulazione | Utilizzala per |
| --- | --- |
| **[!UICONTROL Simula contenuto]** | Test delle varianti di contenuto con dati di input di esempio o generazione automatica di IA. |
| **[!UICONTROL Simula contenuto]** > **[!UICONTROL Simula contenuto (profili AEP)]** | Visualizza l’anteprima del messaggio con i profili di test. |

Esamina ogni variante e verifica che il contenuto del messaggio e i valori personalizzati siano visualizzati come previsto.

Per informazioni dettagliate sull&#39;anteprima e sulla verifica del contenuto, vedere [Anteprima e verifica del contenuto](../content-management/preview-test.md).

## Convalidare il contenuto {#line-validate}

Prima di continuare, controlla gli avvisi visualizzati nella parte superiore dell’editor dei messaggi.

In Journey Optimizer vengono visualizzati due tipi di avvisi:

* **Gli avvisi** sono consigli o suggerimenti sulle best practice. Non ti impediscono di testare o inviare il messaggio.
* **Gli errori** identificano i problemi che devono essere risolti prima di poter testare o attivare il percorso o pubblicare la campagna.

Risolvi tutti gli errori prima di continuare. Rispondi agli avvisi quando indicano che il messaggio potrebbe non fornire l’esperienza del cliente prevista.

## Richiedi approvazione quando richiesto {#line-approval}

Se la campagna è soggetta a una policy di approvazione, richiedi l’approvazione prima di inviare il messaggio.

Consulta [Scopri come richiedere l&#39;approvazione](../test-approve/gs-approval.md).

## Inviare il messaggio LINE {#line-send}

Quando il messaggio è pronto, torna al percorso o alla campagna che contiene l’azione LINE e completa la configurazione:

* **Percorso:** Completare la configurazione del percorso, quindi attivare il percorso.
* **Campagna:** Completa la configurazione della campagna, quindi pubblica la campagna.

Se non riesci ad attivare il percorso o a pubblicare la campagna, torna all’editor dei messaggi e risolvi gli eventuali errori rimanenti.

## Attività correlate {#related-tasks}

* [Introduzione a LINE](./get-started-line.md)
* [Creare un messaggio LINE](./create-line.md)
* [Configurare il canale LINE](./line-configuration.md)

{{$include /help/_includes/do-not-localize/line/ai-augmented-send-line.md}}
