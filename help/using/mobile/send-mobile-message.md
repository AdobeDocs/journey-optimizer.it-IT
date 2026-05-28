---
solution: Journey Optimizer
product: journey optimizer
title: Verifica e verifica i messaggi mobili
description: Scopri come controllare e inviare messaggi mobili in Journey Optimizer
feature: SMS
topic: Content Management
role: User
level: Beginner
exl-id: 31c9b080-e334-4a11-af33-4c6f115c70a4
TQID: https://experienceleague.adobe.com/JPjBxyZzo13tgSLo0dqd5bFOwn9C6MHkA-DjLzlAdEI
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: c41e8697-e629-4c38-96b3-564faaa17acf
  - id: f8d2e9f0-69c9-40cd-890f-71336c8dfff7
  - id: b3b09fe1-10f1-4793-9f6b-1ca0269eebe7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 537
ht-degree: 1%

---

# Verifica e invia il messaggio mobile {#send-sms}

## Anteprima del messaggio mobile {#preview-sms}

Una volta definito il contenuto del messaggio, puoi utilizzare profili di test o dati di input di esempio (caricati da un file CSV/JSON o aggiunti manualmente) per visualizzarne l’anteprima. Se hai inserito dei contenuti personalizzati, puoi controllare come questi contenuti vengono visualizzati nel messaggio.

A tale scopo, fai clic su **[!UICONTROL Simula contenuto]**, quindi controlla il messaggio utilizzando i dati del profilo di test.

![](assets/sms_preview_2.png)

Informazioni dettagliate su come visualizzare in anteprima e testare il contenuto sono disponibili nella sezione [Gestione dei contenuti](../content-management/preview-test.md).

### Codifica e limiti dei caratteri {#sms-character-limits}

Durante l&#39;accesso al menu **[!UICONTROL Simula contenuto]** viene visualizzato un conteggio di caratteri che facilita la pianificazione e la gestione dei messaggi mobili.

![](assets/sms_preview_3.png)

Journey Optimizer utilizza la codifica UTF-8 nel proprio editor SMS, che consente di digitare o incollare caratteri a doppio byte o Unicode. Questi caratteri vengono quindi trasmessi al fornitore di servizi per la consegna. La maggior parte dei provider SMS utilizza la codifica GSM a 7 bit per i messaggi standard con un limite di 160 caratteri e passa a UTF-16 (UCS-2) quando vengono rilevati caratteri non GSM con un limite di 70 caratteri.

Il conteggio dei caratteri non riflette le varianti introdotte dalla personalizzazione dinamica o dai caratteri speciali non GSM a 7 bit.

>[!IMPORTANT]
>
>Il reporting sulla consegna di SMS Journey Optimizer non tiene conto dei messaggi concatenati e della personalizzazione dinamica, pertanto potrebbe non riflettere il numero effettivo di messaggi inviati dal provider. Per informazioni dettagliate sull’utilizzo e sulla fatturazione, contatta il tuo rappresentante Adobe.
>
>Per informazioni sulle best practice per ridurre al minimo le interruzioni di fatturazione SMS, consulta [Best practice SMS per l&#39;ottimizzazione dei caratteri](mobile-cost-optimization.md).

## Convalidare il contenuto {#sms-validate}

>[!NOTE]
>
> Per migliorare il recapito messaggi, utilizza i numeri di telefono nei formati supportati dal provider. Ad esempio, Twilio e Sinch supportano solo i numeri di telefono in formato E.164.

È necessario controllare gli avvisi nella sezione superiore dell’editor. Alcuni sono semplici avvisi, altri possono impedirti di inviare il messaggio. Possono verificarsi due tipi di avvisi: avvisi ed errori.

![](assets/sms-alert-button.png)

* **Avvisi** fai riferimento a consigli e best practice. Ad esempio, viene visualizzato un messaggio di avviso se il messaggio Mobile è vuoto o se i limiti dei caratteri con il contenuto dinamico possono essere superati.

  **Limiti di caratteri:** 160 caratteri per segmento (GSM a 7 bit), 70 caratteri per Unicode/emojis, fino a un totale di 1500 caratteri.

* **Gli errori** impediscono di testare o attivare il percorso o di pubblicare la campagna, purché non siano risolti. Ad esempio, un messaggio di errore ti avvisa quando manca la riga dell’oggetto.

L&#39;avviso **&quot;Il limite di caratteri del testo SMS è stato superato&quot;** può essere visualizzato anche quando il messaggio simulato è più breve, perché la convalida calcola la **lunghezza massima possibile** valutando tutti i rami condizionali, i campi di personalizzazione e il contenuto dinamico al massimo.

La convalida calcola la lunghezza massima per tutti i dati di profilo possibili, mentre la simulazione mostra l’output effettivo per un profilo di test.

## Inviare messaggi da dispositivi mobili {#sms-send}

>[!IMPORTANT]
>
> Se la campagna è soggetta a una policy di approvazione, dovrai richiedere l’approvazione per poter inviare i messaggi da dispositivi mobili. [Ulteriori informazioni](../test-approve/gs-approval.md)

Quando il messaggio mobile è pronto, completa la configurazione del [percorso](../building-journeys/journey-gs.md) o [campagna](../campaigns/create-campaign.md) per inviarlo.

**Argomenti correlati**

* [Configurare il canale SMS](mobile-configuration.md)
* [Rapporti SMS/RCS/MMS](../reports/journey-global-report-cja-sms.md)
* [Creare un messaggio mobile](create-mobile-message.md)
* [Aggiungere un messaggio in un percorso](../building-journeys/journey-action.md)
