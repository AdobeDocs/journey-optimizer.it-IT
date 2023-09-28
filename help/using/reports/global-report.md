---
solution: Journey Optimizer
product: journey optimizer
title: Rapporto globale
description: Scopri come utilizzare i dati del rapporto globale
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: ec15e700-7659-4dbf-8446-6534ea48c5c8
source-git-commit: 9a1eea69c47ace2ad9bbd1d4668007b8ea1796fc
workflow-type: tm+mt
source-wordcount: '531'
ht-degree: 0%

---

# Introduzione ai rapporti globali {#global-report}

>[!NOTE]
>
> Se vengono effettuate query personalizzate tramite API quando si utilizza Query Service, si prega di attendere un certo ritardo per i rapporti.

Utilizza il **[!UICONTROL Rapporto globale]** per misurare l’impatto di percorsi e consegne in un periodo di tempo selezionato.

* Se desideri eseguire il targeting di un percorso o di consegne nel contesto di un percorso, da **[!UICONTROL Percorsi]** , accedere al percorso e fare clic sul pulsante **[!UICONTROL Visualizza rapporto]** pulsante. Puoi quindi trovare i rapporti globali relativi a Percorso, e-mail, SMS e push.

  ![](assets/report_journey.png)

* Se desideri eseguire il targeting di una campagna, da **[!UICONTROL Campagne]** , accedi alla tua campagna e fai clic sul pulsante **[!UICONTROL Rapporti]** pulsante.

  ![](assets/report_campaign.png)

* Se si desidera passare dalla modalità **[!UICONTROL Rapporto live]** al **[!UICONTROL Rapporto globale]** per la consegna, fai clic su **[!UICONTROL Sempre]** dal selettore di tabulazione.

  ![](assets/report_5.png)

Per un elenco dettagliato di tutte le metriche disponibili in Adobe Journey Optimizer, consulta [questa pagina](#list-of-components-global)

## Personalizza dashboard {#modify-dashboard}

Ogni dashboard di reporting può essere modificato modificando il periodo di tempo e ridimensionando o rimuovendo i widget. La modifica dei widget ha effetto solo sul dashboard dell&#39;utente corrente. Gli altri utenti visualizzeranno le proprie dashboard o quelle impostate per impostazione predefinita.

1. Dal rapporto globale, seleziona un’ora di inizio e di fine per eseguire il targeting di dati specifici.

   ![](assets/report_modify_1.png)

1. Scegliere se si desidera escludere gli eventi di test dai rapporti con la barra di attivazione. Per ulteriori informazioni sugli eventi di test, consulta [questa pagina](../building-journeys/testing-the-journey.md).

   Tieni presente che **[!UICONTROL Escludere gli eventi di test]** L&#39;opzione è disponibile solo per i rapporti di Percorso.

   ![](assets/report_modify_2.png)

1. Clic **[!UICONTROL Modifica]** per iniziare a personalizzare la dashboard.

   ![](assets/report_modify_3.png)

1. Regolate le dimensioni dei widget trascinandone l&#39;angolo inferiore destro.

   ![](assets/report_modify_4.png)

1. Clic **[!UICONTROL Rimuovi]** per rimuovere i widget non necessari.

   ![](assets/report_modify_5.png)

1. Quando si è soddisfatti dell&#39;ordine di visualizzazione e delle dimensioni dei widget, fare clic su **[!UICONTROL Salva]**.

1. Per personalizzare la modalità di visualizzazione dei dati, puoi passare da diverse opzioni di visualizzazione, ad esempio grafici, tabelle e grafici ad anello.

   ![](assets/report_modify_10.png)

Il dashboard è ora salvato. Le diverse modifiche verranno riapplicate per un utilizzo successivo dei rapporti live. Se necessario, utilizza **[!UICONTROL Reimposta]** per ripristinare l&#39;ordine dei widget e dei widget predefiniti.

## Esportare i rapporti {#export-reports}

Puoi esportare facilmente i diversi rapporti in formato PDF o CSV, per condividerli o stamparli.

>[!BEGINTABS]

>[!TAB Esportare il report come file PDF]

1. Dal report, fai clic su **[!UICONTROL Esporta]** e seleziona **[!UICONTROL file PDF]**.

   ![](assets/export_2.png)

1. Nella finestra Stampa configurare il documento in base alle esigenze. Le opzioni possono variare a seconda del browser in uso.

1. Scegliere se stampare o salvare il report come PDF.

1. Individuare la cartella in cui si desidera salvare il file, rinominarlo, se necessario, e fare clic su Salva.

Il report è ora disponibile per la visualizzazione o la condivisione in un file pdf.

>[!TAB Esportare il rapporto come file CSV]

1. Dal report, fai clic su **[!UICONTROL Esporta]** e seleziona **[!UICONTROL File CSV]** per generare un file CSV a livello di report complessivo.

   ![](assets/export_1.png)

1. Puoi anche scegliere di esportare i dati da un widget specifico. Clic **[!UICONTROL Esporta dati widget in CSV]** accanto al widget selezionato.

   ![](assets/export_3.png)

1. Il file viene scaricato automaticamente e si trova nei file locali.

   Se hai generato il file a livello di report, contiene informazioni dettagliate per ciascun widget, inclusi il titolo e i dati.

   Se hai generato il file a livello di widget, fornisce specificamente i dati per il widget selezionato.

>[!ENDTABS]