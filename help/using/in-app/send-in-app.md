---
title: Verifica e invio della notifica in-app
description: Scopri come controllare e inviare un messaggio in-app in Journey Optimizer
feature: In App
topic: Content Management
role: User
level: Beginner
keywords: in-app, messaggio, creazione, inizio
exl-id: 9e9c235a-b78c-4669-af82-822b6f1e6fca
TQID: https://experienceleague.adobe.com/lInGr6DN0-ED3ouErpV09-9ovLvOL1oHiSZEO-NBA7c
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: f8d2e9f0-69c9-40cd-890f-71336c8dfff7
  - id: cc5c44e2-54a1-4927-b794-442cd87d8f74
  - id: c96d2aa5-76a2-443d-8d23-5de95577c909
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 686aa52541f2790d6d9853f31dd2a5c1b22c4b16
workflow-type: tm+mt
source-wordcount: 436
ht-degree: 12%

---

# Verificare e inviare una notifica in-app {#create-in-app}

>[!BEGINSHADEBOX]

**In questa pagina:** scopri come visualizzare in anteprima, testare, rivedere e attivare il messaggio in-app in Adobe Journey Optimizer prima di inviarlo al tuo pubblico.

>[!ENDSHADEBOX]

## Anteprima su dispositivo {#preview-device}

Se desideri visualizzare un’anteprima della notifica in-app prima che venga pubblicata per tutti gli utenti, puoi visualizzarla su un dispositivo specifico. Questa funzionalità ti consente di garantire che la notifica si presenti e funzioni come previsto sul dispositivo scelto, fornendo un’esperienza utente migliore per il pubblico.

Per farlo, segui la procedura indicata di seguito:

1. Fare clic su **[!UICONTROL Anteprima sul dispositivo]**.

   ![](assets/in_app_create_6.png)

1. Dalla finestra **[!UICONTROL Connetti al dispositivo]**, fare clic su **[!UICONTROL Avvia]**.

1. Immetti l&#39;**[!UICONTROL URL di base]** dell&#39;applicazione e fai clic su **[!UICONTROL Avanti]**.

   ![](assets/in_app_create_7.png)

1. Analizzare il codice QR con il dispositivo e immettere il codice PIN visualizzato.

Ora il messaggio in-app può essere attivato direttamente sul dispositivo, consentendoti di visualizzare l’anteprima e rivedere il messaggio su un dispositivo effettivo.

## Anteprima con profili di test {#simulate}

Una volta definito il messaggio in-app, puoi visualizzarne l’anteprima utilizzando uno dei seguenti metodi di simulazione:

* Fai clic su **[!UICONTROL Simula contenuto]** per testare le varianti di contenuto con dati di input di esempio o con generazione automatica di IA. [Scopri come simulare varianti di contenuto](../test-approve/simulate-sample-input.md)
* Fai clic su **[!UICONTROL Simula contenuto]**, quindi seleziona **[!UICONTROL Simula contenuto (profili AEP)]** dal menu a discesa per visualizzare in anteprima i profili di test e aggiungere un profilo di test per controllare il messaggio.

Informazioni dettagliate su come selezionare profili di test e visualizzare in anteprima il contenuto sono disponibili nella sezione [Gestione dei contenuti](../content-management/preview-test.md).

## Rivedere e attivare la notifica in-app{#in-app-review}

>[!IMPORTANT]
>
> Se la campagna è soggetta a un criterio di approvazione, per poter inviare la notifica in-app dovrai richiedere l’approvazione. [Ulteriori informazioni](../test-approve/gs-approval.md)

Una volta creato il messaggio in-app e definito e personalizzato il relativo contenuto, puoi rivederlo e attivarlo.

Per farlo, segui la procedura indicata di seguito:

1. Utilizza il pulsante **[!UICONTROL Rivedi per attivare]** per visualizzare un riepilogo del messaggio.

   Il riepilogo ti consente di modificare la campagna, se necessario, e di verificare se un parametro è errato o mancante.

   ![](assets/in_app_create_5.png)

1. Verifica che la tua campagna sia configurata correttamente, quindi fai clic su **[!UICONTROL Attiva]**.

La campagna è ora attivata. La notifica in-app configurata nella campagna viene inviata immediatamente o alla data specificata.

Una volta inviati, puoi misurare l’impatto dei messaggi in-app nei rapporti della campagna o del Percorso. Per ulteriori informazioni sul reporting, consulta [questa sezione](../reports/campaign-global-report-cja-inapp.md).

**Argomenti correlati:**

* [Creare un messaggio in-app](create-in-app.md)
* [Progettare un messaggio in-app](design-in-app.md)
* [Rapporto in-app](../reports/campaign-global-report-cja-inapp.md)
* [Configurazione in-app](inapp-configuration.md)
