---
solution: Journey Optimizer
product: journey optimizer
title: Anteprima e verifica del messaggio SMS
description: Scopri come visualizzare in anteprima e testare il messaggio SMS in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 31c9b080-e334-4a11-af33-4c6f115c70a4
source-git-commit: 81ab92022329788c1feea24c7a621ef154d33422
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 12%

---

# Anteprima e verifica del messaggio SMS {#send-sms}

## Anteprima SMS {#preview-sms}

Una volta definito il contenuto del messaggio, puoi utilizzare i profili di test per visualizzarlo in anteprima e testarlo. Se hai inserito dei contenuti personalizzati, puoi verificare come vengono visualizzati nel messaggio, utilizzando i dati del profilo di test.

1. Clic **[!UICONTROL Simula contenuto]**.

1. Clic **[!UICONTROL Gestire i profili di test]** per aggiungere un profilo di test.

1. Trova il tuo profilo di test con **[!UICONTROL Spazio dei nomi dell’identità]** e **[!UICONTROL Valore identità]** campi. Quindi, fai clic su **[!UICONTROL Aggiungi profilo]**.

   ![](assets/sms_preview_3.png)

1. Dopo aver selezionato il profilo di test, puoi chiudere **[!UICONTROL Aggiungi profilo di test]** finestra.

1. Dalla sezione **Anteprima e prova** I dati del profilo di test vengono aggiunti al contenuto del messaggio.

   ![](assets/sms_preview_2.png)


## Convalidare l’SMS{#sms-validate}

È necessario controllare gli avvisi nella sezione superiore dell’editor. Alcuni sono semplici avvisi, altri possono impedirti di inviare il messaggio. Possono verificarsi due tipi di avvisi: avvisi ed errori.

* **Avvisi** consulta consigli e best practice. Ad esempio, se il messaggio SMS è vuoto, viene visualizzato un messaggio di avviso.

* **Errori** impedisci di testare o attivare il percorso o di pubblicare la campagna, purché non siano risolti. Ad esempio, un messaggio di errore ti avvisa quando manca la riga dell’oggetto.

![](assets/sms-alert-button.png)

>[!NOTE]
>
> Per migliorare il recapito messaggi, utilizza i numeri di telefono nei formati supportati dal provider. Ad esempio, Twilio e Sinch supportano solo i numeri di telefono in formato E.164.

## Inviare l’SMS{#sms-send}

Quando il messaggio SMS è pronto, completa la configurazione del [percorso](../building-journeys/journey-gs.md) o [campagna](../campaigns/create-campaign.md) per inviarlo.

**Argomenti correlati**

* [Configurare il canale SMS](sms-configuration.md)
* [Rapporto SMS](../reports/journey-global-report.md#sms-global)
* [Creare un messaggio SMS](create-sms.md)
* [Aggiungere un messaggio in un percorso](../building-journeys/journeys-message.md)
