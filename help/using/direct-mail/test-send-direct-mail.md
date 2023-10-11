---
title: Testare e inviare un messaggio di direct mail
description: Scopri come verificare e inviare un messaggio di direct mailing in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
keyword: direct, mail, configuration, direct-mail, provider
exl-id: 69a19190-d2e2-4858-a1df-ffd008226e2b
source-git-commit: 804ff95d2a19601d036e739bb1d5a629930247b9
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 14%

---

# Testare e inviare un messaggio di direct mail {#direct-mail-test-send}

## Anteprima del file di estrazione {#preview-dm}

>[!CONTEXTUALHELP]
>id="ajo_direct_mail_preview"
>title="Anteprima file di estrazione"
>abstract="In questo riquadro puoi visualizzare in anteprima il modo in cui il file di estrazione viene visualizzato per ciascun profilo di test selezionato nel riquadro a sinistra. Se hai inserito dei contenuti personalizzati, puoi verificare come vengono visualizzati utilizzando i dati del profilo di test."

Una volta definito il contenuto del file di estrazione, puoi utilizzare i profili di test per visualizzarlo in anteprima. Se hai inserito dei contenuti personalizzati, puoi verificare come vengono visualizzati nel messaggio, utilizzando i dati del profilo di test.

1. Nella schermata di configurazione del contenuto del file di estrazione, fai clic su **[!UICONTROL Simula contenuto]**.

   ![](assets/direct-mail-simulate-button.png){width="800" align="center"}

1. Clic **[!UICONTROL Gestire i profili di test]** per aggiungere un profilo di test.

1. Trova il tuo profilo di test con **[!UICONTROL Spazio dei nomi dell’identità]** e **[!UICONTROL Valore identità]** campi. Quindi, fai clic su **[!UICONTROL Aggiungi profilo]**.

   ![](assets/direct-mail-test-profile.png){width="800" align="center"}

1. Dopo aver selezionato il profilo di test, puoi chiudere **[!UICONTROL Aggiungi profilo di test]** finestra.

1. Dalla sezione **Anteprima e prova** finestra, i dati del profilo di test vengono aggiunti al contenuto del file di estrazione, consentendo di visualizzare in anteprima come verrà eseguito il rendering del file.

   ![](assets/direct-mail-simulate.png){width="800" align="center"}

Quando il contenuto del file è pronto per essere inviato, chiudi la schermata di simulazione e fai clic su **[!UICONTROL Controlla per attivare]** pulsante.

## Convalidare e attivare la campagna di direct mailing {#dm-validate}

Prima di attivare la campagna di direct mailing, assicurati che la campagna e il file di estrazione siano configurati correttamente. A questo scopo, seleziona gli avvisi nella sezione superiore dell’editor. Alcuni sono semplici avvisi, altri possono impedirti di inviare il messaggio. Possono verificarsi due tipi di avvisi: avvisi ed errori.

* **Avvisi** consulta consigli e best practice. Ad esempio, se il messaggio SMS è vuoto, viene visualizzato un messaggio di avviso.

* **Errori** impedisci la pubblicazione della campagna, purché non siano risolte. Ad esempio, un messaggio di errore ti avvisa quando manca la riga dell’oggetto.

![](assets/direct-mail-review.png){width="800" align="center"}

Quando la campagna di direct mailing è pronta, fai clic su **[!UICONTROL Attiva]** pulsante. All’avvio della campagna, il file di estrazione viene generato ed esportato automaticamente sul server specificato nella [configurazione di indirizzamento dei file](../direct-mail/direct-mail-configuration.md).

Una volta inviato, puoi misurare l’impatto della campagna di direct mailing all’interno dei rapporti della campagna. Per ulteriori informazioni sul reporting, consulta questa sezione.

## Gestire il consenso per la direct mailing {#dm-consent-management}

In [!DNL Journey Optimizer], il consenso è gestito dallo [Schema di consenso](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/profile/consents.html?lang=it){target="_blank"} di Experience Platform. Per impostazione predefinita, il valore del campo di consenso è vuoto e viene trattato come consenso alla ricezione delle comunicazioni.

Se un profilo ha rinunciato alla ricezione di direct mailing, negli attributi di profilo di Experience Platform corrispondenti, il valore per `consents.marketing.postalMail.val` sarà `n` e il profilo corrispondente verrà escluso dalle consegne successive.

Per abilitarlo nuovamente, l’attributo di profilo deve essere modificato in `consents.marketing.postalMail.val` : `y`.

Per gestire gli attributi di un profilo, passa a Experience Platform e accedi al profilo selezionando uno spazio dei nomi dell’identità e un valore di identità corrispondente. Per ulteriori informazioni, consulta la [documentazione di Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=it#getting-started){target="_blank"}.

Ulteriori informazioni sulla gestione della rinuncia in Journey Optimizer in [questa sezione](../privacy/opt-out.md).
