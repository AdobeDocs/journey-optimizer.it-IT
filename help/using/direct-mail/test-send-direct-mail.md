---
title: Verifica e invia un messaggio di direct mailing
description: Scopri come controllare e inviare un messaggio di direct mailing in Journey Optimizer
feature: Direct Mail, Test Profiles, Preview
topic: Content Management
role: User
level: Beginner
keyword: direct, mail, configuration, direct-mail, provider
exl-id: 69a19190-d2e2-4858-a1df-ffd008226e2b
source-git-commit: 27447578dad6bd2612989d79cd0dc8ddbe78d629
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 5%

---

# Verifica e invia un messaggio di direct mailing {#direct-mail-test-send}

## Anteprima del file di estrazione {#preview-dm}

Una volta definito il contenuto del file di estrazione, puoi utilizzare i profili di test per visualizzarlo in anteprima. Se hai incluso contenuti personalizzati, puoi verificare come questi vengono visualizzati nel messaggio utilizzando i dati del profilo di test.

A questo scopo, fai clic su **[!UICONTROL Simula contenuto]** quindi aggiungi un profilo di test per verificare come viene eseguito il rendering del file di estrazione utilizzando i dati del profilo di test.

![](assets/direct-mail-simulate.png){width="800" align="center"}

Informazioni dettagliate su come selezionare i profili di test e visualizzare in anteprima i contenuti sono disponibili nella sezione [Gestione dei contenuti](../content-management/preview-test.md) sezione.

Quando il contenuto del file è pronto per essere inviato, chiudi la schermata di simulazione e fai clic su **[!UICONTROL Controlla per attivare]** pulsante.

## Convalidare e attivare la campagna di direct mailing {#dm-validate}

Prima di attivare la campagna di direct mailing, assicurati che la campagna e il file di estrazione siano configurati correttamente. A questo scopo, seleziona gli avvisi nella sezione superiore dell’editor. Alcuni sono semplici avvisi, altri possono impedirti di inviare il messaggio. Possono verificarsi due tipi di avvisi: avvisi ed errori.

* **Avvisi** consulta consigli e best practice. Ad esempio, se il messaggio SMS è vuoto, viene visualizzato un messaggio di avviso.

* **Errori** impedisci la pubblicazione della campagna, purché non siano risolte. Ad esempio, un messaggio di errore ti avvisa quando manca la riga dell’oggetto.

![](assets/direct-mail-review.png){width="800" align="center"}

Quando la campagna di direct mailing è pronta, fai clic su **[!UICONTROL Attiva]** pulsante. All’avvio della campagna, il file di estrazione viene generato ed esportato automaticamente sul server specificato nella [configurazione di indirizzamento dei file](../direct-mail/direct-mail-configuration.md).

Una volta inviato, puoi misurare l’impatto della campagna di direct mailing all’interno dei rapporti della campagna. Per ulteriori informazioni sul reporting, consulta questa sezione.

## Gestire il consenso per la direct mailing {#dm-consent-management}

In entrata [!DNL Journey Optimizer], il consenso è gestito dall&#39;Experience Platform [Schema di consenso](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/profile/consents.html?lang=it){target="_blank"}. Per impostazione predefinita, il valore del campo di consenso è vuoto e viene trattato come consenso alla ricezione delle comunicazioni.

Se un profilo ha rinunciato alla ricezione di direct mailing, negli attributi di profilo di Experience Platform corrispondenti, il valore per `consents.marketing.postalMail.val` sarà `n` e il profilo corrispondente verrà escluso dalle consegne successive.

Per abilitarlo nuovamente, l’attributo di profilo deve essere modificato in `consents.marketing.postalMail.val` : `y`.

Per gestire gli attributi di un profilo, passa a Experience Platform e accedi al profilo selezionando uno spazio dei nomi dell’identità e un valore di identità corrispondente. Per ulteriori informazioni, consulta [Documentazione di Experienci Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=it#getting-started){target="_blank"}.

Ulteriori informazioni sulla gestione della rinuncia in Journey Optimizer in [questa sezione](../privacy/opt-out.md).
