---
solution: Journey Optimizer
product: journey optimizer
title: Verifica i messaggi di testo
description: Scopri come controllare e inviare messaggi di testo in Journey Optimizer
feature: SMS
topic: Content Management
role: User
level: Beginner
exl-id: 31c9b080-e334-4a11-af33-4c6f115c70a4
source-git-commit: f275820c3f79bb4c9aca8593c2c761ccd4283795
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 11%

---

# Controllare e inviare il messaggio di testo {#send-sms}

## Anteprima del messaggio di testo {#preview-sms}

Una volta definito il contenuto del messaggio, puoi utilizzare i profili di test per visualizzarne l’anteprima. Se hai incluso contenuti personalizzati, puoi verificare come questi vengono visualizzati nel messaggio utilizzando i dati del profilo di test.

A questo scopo, fai clic su **[!UICONTROL Simula contenuto]** quindi aggiungi un profilo di test per controllare il messaggio utilizzando i dati del profilo di test.

![](assets/sms_preview_2.png)

Informazioni dettagliate su come selezionare i profili di test e visualizzare in anteprima i contenuti sono disponibili nella sezione [Gestione dei contenuti](../content-management/preview-test.md) sezione.

## Convalidare il contenuto {#sms-validate}

È necessario controllare gli avvisi nella sezione superiore dell’editor. Alcuni sono semplici avvisi, altri possono impedirti di inviare il messaggio. Possono verificarsi due tipi di avvisi: avvisi ed errori.

![](assets/sms-alert-button.png)

* **Avvisi** consulta consigli e best practice. Ad esempio, se il messaggio di testo è vuoto, viene visualizzato un messaggio di avviso.

* **Errori** impedisci di testare o attivare il percorso o di pubblicare la campagna, purché non siano risolti. Ad esempio, un messaggio di errore ti avvisa quando manca la riga dell’oggetto.


>[!NOTE]
>
> Per migliorare il recapito messaggi, utilizza i numeri di telefono nei formati supportati dal provider. Ad esempio, Twilio e Sinch supportano solo i numeri di telefono in formato E.164.

## Inviare i messaggi di testo {#sms-send}

Quando il messaggio di testo è pronto, completa la configurazione del [percorso](../building-journeys/journey-gs.md) o [campagna](../campaigns/create-campaign.md) per inviarlo.

**Argomenti correlati**

* [Configurare il canale SMS](sms-configuration.md)
* [Rapporti SMSS](../reports/journey-global-report.md#sms-global)
* [Creare un messaggio SMS](create-sms.md)
* [Aggiungere un messaggio in un percorso](../building-journeys/journeys-message.md)
