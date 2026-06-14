---
solution: Journey Optimizer
product: journey optimizer
title: Testare e inviare un messaggio di direct mail
description: Scopri come controllare e inviare un messaggio di direct mailing in Journey Optimizer
feature: Direct Mail, Test Profiles, Preview
topic: Content Management
role: User
level: Beginner
keyword: direct, mail, configuration, direct-mail, provider
exl-id: 69a19190-d2e2-4858-a1df-ffd008226e2b
TQID: https://experienceleague.adobe.com/4GZKFKOx-D-RT1mssiV5vpmZQSJGVbGMro8Q-suhtPE
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: f8d2e9f0-69c9-40cd-890f-71336c8dfff7
  - id: cb1f1586-9fb4-4de2-8332-02cebb88d42d
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: e7702a4706509a8181ee39cccc510656c5230a16
workflow-type: tm+mt
source-wordcount: 605
ht-degree: 15%

---

# Testare e inviare un messaggio di direct mail {#direct-mail-test-send}

>[!BEGINSHADEBOX]

**In questa pagina:** Visualizza in anteprima il file di estrazione, convalida e attiva la campagna o il percorso e gestisci il consenso postale in modo che la direct mailing raggiunga con precisione i destinatari giusti.

>[!ENDSHADEBOX]

Scopri come visualizzare in anteprima il file di estrazione, convalidare e attivare la campagna o il percorso di direct mailing e gestire il consenso per la posta postale in Journey Optimizer.

## Prima di iniziare {#before-you-start}

Prima di testare e inviare un messaggio di direct mailing, [crea il messaggio e configura il file di estrazione](create-direct-mail.md). Assicurati anche di aver completato la [configurazione del canale direct mailing](direct-mail-configuration.md).

## Anteprima del file di estrazione {#preview-dm}

Una volta definito il contenuto del file di estrazione, visualizzalo in anteprima utilizzando uno dei due metodi di simulazione:

* Fai clic su **[!UICONTROL Simula contenuto]** per testare le varianti di contenuto con dati di input di esempio o con generazione automatica di IA. [Scopri come simulare varianti di contenuto](../test-approve/simulate-sample-input.md)
* Fai clic su **[!UICONTROL Simula contenuto]**, quindi seleziona **[!UICONTROL Simula contenuto (profili AEP)]** dal menu a discesa e aggiungi un profilo di test per verificare la modalità di rendering del file di estrazione.

Informazioni dettagliate su come visualizzare in anteprima e testare il contenuto sono disponibili nella sezione [Gestione dei contenuti](../content-management/preview-test.md).

![Simulare l&#39;anteprima del contenuto per un file di estrazione di direct mailing](assets/direct-mail-simulate.png){width="800" align="center"}

Quando il contenuto del file è pronto per essere inviato, chiudere la schermata di simulazione e fare clic sul pulsante **[!UICONTROL Controlla per attivare]**.

## Convalidare e attivare la campagna di direct mailing {#dm-validate}

>[!IMPORTANT]
>
> Se la campagna è soggetta a una policy di approvazione, dovrai richiedere l’approvazione per poter inviare la tua campagna Direct Mail. [Ulteriori informazioni](../test-approve/gs-approval.md)

Prima di attivare la campagna di direct mailing, assicurati che la campagna o il percorso e il file di estrazione siano configurati correttamente. A questo scopo, seleziona gli avvisi nella sezione superiore dell’editor. Alcuni sono semplici avvisi, altri possono impedirti di inviare il messaggio. Possono verificarsi due tipi di avvisi: avvisi ed errori.

* **Avvisi** fai riferimento a consigli e best practice. Ad esempio, se il messaggio SMS è vuoto, viene visualizzato un messaggio di avviso.

* **Gli errori** impediscono la pubblicazione della campagna, purché non vengano risolti. Ad esempio, un messaggio di errore ti avvisa quando manca la riga dell’oggetto.

![Rivedi e attiva la schermata che mostra gli avvisi di convalida delle campagne per direct mail](assets/direct-mail-review.png){width="800" align="center"}

Quando la tua campagna di direct mailing è pronta, completa la configurazione del [percorso](../building-journeys/journey-gs.md) o della [campagna](../campaigns/create-campaign.md) per inviarla.

>[!NOTE]
>
>Per impostazione predefinita, il file esportato termina con una nuova riga. Questo garantisce la compatibilità con gli strumenti standard di elaborazione dei dati.

Una volta inviato, puoi misurare l’impatto della campagna di direct mailing o del percorso all’interno dei rapporti. Per ulteriori informazioni sul reporting della direct mailing, consulta le sezioni seguenti:
* [Rapporto sulle campagne Direct mail](../reports/campaign-global-report-cja-direct.md)
* [Rapporto sul percorso direct mail](../reports/journey-global-report-cja-direct.md)

## Gestire il consenso per la direct mailing {#dm-consent-management}

In [!DNL Journey Optimizer], il consenso è gestito dallo [Schema di consenso](https://experienceleague.adobe.com/docs/experience-platform/xdm/field-groups/profile/consents.html?lang=it){target="_blank"} di Experience Platform. Per impostazione predefinita, il valore del campo di consenso è vuoto e viene trattato come consenso alla ricezione delle comunicazioni.

Se un profilo ha rinunciato alla ricezione di direct mailing, negli attributi di profilo di Experience Platform corrispondenti, il valore per `consents.marketing.postalMail.val` sarà `n` e il profilo corrispondente sarà escluso dalle consegne successive.

Per riattivarlo, è necessario ripristinare l&#39;attributo del profilo su `consents.marketing.postalMail.val` : `y`.

Per gestire gli attributi di un profilo, passa ad Experience Platform e accedi al profilo selezionando uno spazio dei nomi dell’identità e un valore di identità corrispondente. Per ulteriori informazioni, consulta la [documentazione di Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=it#getting-started){target="_blank"}.

Ulteriori informazioni sulla gestione della rinuncia in Journey Optimizer in [questa sezione](../privacy/opt-out.md).

## Argomenti correlati {#related-topics}

* [Introduzione alle direct mail](get-started-direct-mail.md)
* [Creare un messaggio direct mail](create-direct-mail.md)
* [Configurare il canale di direct mailing](direct-mail-configuration.md)
* [Anteprima e verifica del contenuto](../content-management/preview-test.md)

Per domande frequenti sulla direct mailing, consulta [Introduzione alla direct mailing](get-started-direct-mail.md).
