---
title: Testare e inviare un messaggio di direct mailing
description: Scopri come verificare e inviare un messaggio di direct mailing in Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
keyword: direct, mail, configuration, direct-mail, provider
source-git-commit: 246205d13c1dd30b4f4769780f69e5acdd388e66
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 2%

---

# Testare e inviare un messaggio di direct mailing {#direct-mail-test-send}

## Anteprima del file di estrazione {#preview-dm}

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
