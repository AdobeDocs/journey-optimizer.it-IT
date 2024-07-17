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
source-git-commit: 75638e9b463278efab16b2b85ed2707640f088f2
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 11%

---

# Controllare e inviare il messaggio di testo (SMS/MMS){#send-sms}

## Anteprima del messaggio di testo {#preview-sms}

Una volta definito il contenuto del messaggio, puoi utilizzare i profili di test per visualizzarne l’anteprima. Se hai incluso contenuti personalizzati, puoi verificare come questi vengono visualizzati nel messaggio utilizzando i dati del profilo di test.

A questo scopo, fai clic su **[!UICONTROL Simula contenuto]**, quindi aggiungi un profilo di test per verificare il messaggio utilizzando i dati del profilo di test.

![](assets/sms_preview_2.png)

Informazioni dettagliate su come selezionare profili di test e visualizzare in anteprima il contenuto sono disponibili nella sezione [Gestione dei contenuti](../content-management/preview-test.md).

## Convalidare il contenuto {#sms-validate}

È necessario controllare gli avvisi nella sezione superiore dell’editor. Alcuni sono semplici avvisi, altri possono impedirti di inviare il messaggio. Possono verificarsi due tipi di avvisi: avvisi ed errori.

![](assets/sms-alert-button.png)

* **Avvisi** fai riferimento a consigli e best practice. Ad esempio, se il messaggio di testo è vuoto, viene visualizzato un messaggio di avviso.

* **Gli errori** impediscono di testare o attivare il percorso o di pubblicare la campagna, purché non siano risolti. Ad esempio, un messaggio di errore ti avvisa quando manca la riga dell’oggetto.


>[!NOTE]
>
> Per migliorare il recapito messaggi, utilizza i numeri di telefono nei formati supportati dal provider. Ad esempio, Twilio e Sinch supportano solo i numeri di telefono in formato E.164.

## Inviare i messaggi di testo {#sms-send}

Quando il messaggio di testo è pronto, completa la configurazione del [percorso](../building-journeys/journey-gs.md) o [campagna](../campaigns/create-campaign.md) per inviarlo.

**Argomenti correlati**

* [Configurare il canale SMS](sms-configuration.md)
* [Rapporti SMS/MMS](../reports/journey-global-report.md#sms-global)
* [Creare un messaggio SMS](create-sms.md)
* [Aggiungere un messaggio in un percorso](../building-journeys/journeys-message.md)
