---
solution: Journey Optimizer
product: journey optimizer
title: Reporting
description: Introduzione alla generazione di rapporti
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: d2ff175a-8bca-4b62-931c-a909cfd9308d
source-git-commit: 881cae4638082f804a5e2a768dfa135193959191
workflow-type: tm+mt
source-wordcount: '1354'
ht-degree: 2%

---

# Gestire i rapporti {#channel-cja-manage}

## Analizzare in Customer Journey Analytics {#analyze}

>[!AVAILABILITY]
>
> La funzionalità **Analizza in CJA** è disponibile esclusivamente per gli utenti con una licenza [!DNL Customer Journey Analytics].

![](assets/cja-analyze.png)

Migliora la tua esperienza di analisi dei dati con la licenza di **[!DNL Customer Journey Analytics]** sfruttando la funzionalità **[!UICONTROL Analizza in CJA]** disponibile in tutti i report.

Questa potente opzione ti reindirizza direttamente al tuo ambiente **[!DNL Customer Journey Analytics]**, consentendoti di personalizzare estesamente i tuoi report. Puoi arricchire i tuoi widget con metriche Customer Journey Analytics specializzate, portando le tue informazioni a un livello completamente nuovo.

[Ulteriori informazioni sull&#39;interfaccia di Customer Journey Analytics.](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-getting-started)

## Definire il periodo del rapporto {#report-period}

![](assets/cja-time-period.png)

Quando accedi a un rapporto, puoi applicare un filtro per periodo di tempo, posizionato nell’angolo in alto a destra del rapporto.

Per impostazione predefinita, il periodo di filtro per una campagna o un percorso è impostato sulle relative date di inizio e fine. Se non è presente una data di fine, per impostazione predefinita il filtro utilizzerà la data corrente.

Per modificare il filtro, puoi selezionare una data e una durata di inizio personalizzate oppure scegliere tra opzioni predefinite, ad esempio l’ultima settimana o due mesi fa.

Il rapporto viene aggiornato automaticamente una volta applicato o modificato il filtro.

## Esportazione dei rapporti {#export-reports}

Puoi esportare facilmente i diversi rapporti in formato PDF o CSV, per condividerli o stamparli. I passaggi per esportare i rapporti sono descritti nelle schede seguenti.

>[!BEGINTABS]

>[!TAB Esporta il report come file CSV]

1. Dal tuo report, fai clic su **[!UICONTROL Condividi]** e seleziona **[!UICONTROL Scarica CSV]** per generare un file CSV a livello di report complessivo.

   ![](assets/export_cja_csv.png)

1. Il file viene scaricato automaticamente e si trova nei file locali.

   Se hai generato il file a livello di report, contiene informazioni dettagliate per ciascun widget, inclusi il titolo e i dati.

>[!TAB Esporta il report come file PDF]

1. Dal tuo report, fai clic su **[!UICONTROL Condividi]** e seleziona **[!UICONTROL Scarica PDF]**.

   ![](assets/export_cja_pdf.png)

1. Dopo aver richiesto il download, fare clic su **[!UICONTROL Scarica]**.

   ![](assets/export_cja_pdf_2.png)

1. Il file si aprirà automaticamente nel browser.

Il report è ora disponibile per la visualizzazione, il download o la condivisione in un file PDF.

>[!ENDTABS]


## Pianifica esportazioni {#schedule-export}

L&#39;**esportazione pianificata** ti consente di automatizzare la consegna di un massimo di 10 rapporti a intervalli settimanali, mensili o annuali. Puoi anche gestire facilmente i rapporti pianificati, con opzioni per aggiornare, modificare, annullare o eliminare una qualsiasi delle esportazioni pianificate.

1. Dal report, fai clic su **[!UICONTROL Condividi]** e seleziona **[!UICONTROL Pianifica esportazione]**.

   ![](assets/export-schedule-1.png)

1. Scegli il **[!UICONTROL tipo di file]** tra CSV e PDF.

1. Se necessario, puoi aggiungere una **[!UICONTROL Descrizione]** all&#39;esportazione.

1. Immetti il nome dei destinatari che riceveranno la consegna automatica.

   ![](assets/export-schedule-2.png)

1. Scegli la **[!UICONTROL frequenza]**.

1. In base alla frequenza selezionata, fornisci i dettagli di pianificazione pertinenti, ad esempio:

   * Date di inizio e di fine

   * Intervallo (ad esempio, ogni poche settimane)

   * Giorno specifico della settimana

   * Settimana nel mese

   * Giorno entro il mese

   * Mese dell’anno

1. Fai clic su **[!UICONTROL Invia secondo programma]**.

1. Per modificare l&#39;esportazione pianificata creata in precedenza, fare clic su **[!UICONTROL Condividi]** e selezionare **[!UICONTROL Gestisci pianificazioni]**.

   ![](assets/export-schedule-3.png)

1. Dall&#39;elenco delle esportazioni programmate, scegliere quella che si desidera aggiornare e apportare le modifiche necessarie.

1. Per eliminare un report pianificato, selezionarne uno dall&#39;elenco Pianificazioni gestite e fare clic su **[!UICONTROL Elimina]**.

   ![](assets/export-schedule-4.png)


## Creare una metrica semplice {#create-simple-metric}

Puoi creare metriche calcolate personalizzate direttamente all’interno dei rapporti. Puoi generare informazioni più personalizzate e analizzare meglio i dati combinando due metriche esistenti in modo che soddisfino le tue esigenze di reporting specifiche.

1. Per prima cosa, accedi al rapporto in cui desideri aggiungere una nuova metrica.

1. Nella tabella all&#39;interno del report, selezionare le metriche desiderate tenendo premuto il tasto `Shift` o `CTRL/CMD` mentre si fa clic su di esse. Quindi, fare clic con il pulsante destro del mouse e selezionare **[!UICONTROL Crea metrica da selezione]**.

   Se selezioni più di due metriche, nel generatore di metriche verranno utilizzate solo le prime due.

   ![](assets/cja-create-metric_2.png)

1. Dal generatore di metriche calcolate, assegna un nome alla nuova metrica digitando nel campo **[!UICONTROL Titolo]**. Puoi anche aggiungere una **[!UICONTROL Descrizione]**.

   >[!NOTE]
   >
   >Se possiedi Customer Journey Analytics, puoi personalizzare ulteriormente le metriche con opzioni aggiuntive. [Ulteriori informazioni](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-components/cja-calcmetrics/cm-workflow/cm-build-metrics#areas-of-the-calculated-metrics-builder)

1. Scegli le **[!UICONTROL Cifre decimali]** appropriate e seleziona un **[!UICONTROL Formato]** (Decimale, Ora, Percentuale o Valuta) in base alla modalità di visualizzazione della metrica.

1. Selezionare l&#39;operatore, ad esempio addizione, sottrazione, moltiplicazione o divisione, che determinerà la modalità di calcolo della metrica.

   ![](assets/cja-create-metric.png)

1. Se necessario, puoi riordinare i componenti.

1. Quando si è soddisfatti delle impostazioni, fare clic su **[!UICONTROL Applica]** per finalizzare la nuova metrica.

1. La nuova metrica verrà visualizzata accanto alle metriche originali nel rapporto.

   ![](assets/cja-create-metric_3.png)

La metrica appena creata verrà inclusa quando esporti il rapporto come PDF o CSV. Tuttavia, verrà rimosso dal report una volta chiuso.

## Esplorare i dati con Insight Builder {#exploratory}

Utilizza lo strumento Insight Builder per creare facilmente tabelle e visualizzazioni dalle **[!UICONTROL dimensioni]** e **[!UICONTROL metriche]** selezionate. Questo strumento semplifica l&#39;esplorazione dei dati, consentendo di personalizzare e analizzare le informazioni in modo semplice e automatico. Ulteriori informazioni sono disponibili in [questa documentazione](https://experienceleague.adobe.com/en/docs/analytics/analyze/analysis-workspace/panels/quickinsight).

1. Per prima cosa, accedi al rapporto nel punto in cui desideri utilizzare il generatore di Insight.

1. Seleziona il menu di Insight Builder dal menu della barra a sinistra.

   ![](assets/exploratory_analysis_1.png)

1. Crea una query scegliendo un **[!UICONTROL Dimension]** e una **[!UICONTROL Metrica]** utilizzando i menu a discesa. Se necessario, puoi anche selezionare un **[!UICONTROL segmento]**.

   ![](assets/exploratory_analysis_2.png)

1. Definisci l’intervallo di date per l’analisi in modo da specificare il periodo su cui desideri concentrarti. Per impostazione predefinita, l’intervallo di date viene impostato su quello utilizzato nel pannello del rapporto.

1. Utilizza le opzioni **[!UICONTROL Aggiungi suddivisione]** o **[!UICONTROL Aggiungi metrica]** per includere dimensioni aggiuntive, consentendo un raggruppamento dei dati più dettagliato.

   Puoi aggiungere fino a tre **[!UICONTROL Dimensioni]**, **[!UICONTROL Metriche]** e **[!UICONTROL Segmenti]**.

Ora puoi analizzare i dati utilizzando gli strumenti di tabella e visualizzazione personalizzati.

<!--## Create a down-funnel metric {#down-funnel}

1. Create a new journey or open an existing one. [Learn more about journey creation](../building-journeys/journey-gs.md)

1. On the canvas editor, select the option to "add a metric".

c. In the metric selector, choose whichever conversion metric seems appropriate and publish your journey

d. Open the report for the journey that you added the metric to and ensure that the metric has been added to the table alongside all the other pre-configured metrics.
-->

## Creare un pubblico dai dati di reporting {#create-audience}

>[!IMPORTANT]
>
>Ogni organizzazione è limitata a pubblicare 25 tipi di pubblico. Inoltre, gli utenti possono pubblicare fino a 5 tipi di pubblico all’ora e 20 al giorno.
>> I tipi di pubblico una tantum hanno una durata di 48 ore. Pertanto, se entro tale arco temporale vengono pubblicati 25 tipi di pubblico, è possibile pubblicare tali tipi di pubblico solo una volta trascorso il periodo di 48 ore.

Ora puoi selezionare dati specifici all’interno della tabella e creare direttamente un pubblico da queste selezioni, semplificando e semplificando il processo di creazione del pubblico.

1. Per prima cosa, accedi alla tabella del rapporto contenente i dati da trasformare in un pubblico.

1. Fare clic con il pulsante destro del mouse sulla cella desiderata e selezionare **[!UICONTROL Crea pubblico]**.

   In alternativa, puoi avviare la creazione di un pubblico dal widget **[!UICONTROL area di lavoro Percorsi]** selezionando un nodo e facendo clic con il pulsante destro del mouse su di esso.

1. Nella finestra **[!UICONTROL Crea pubblico]**, immetti un **[!UICONTROL Nome]** e imposta un **[!UICONTROL Intervallo di date occasionale]** per il pubblico che intendi pubblicare.

   >[!NOTE]
   >
   >Se possiedi Customer Journey Analytics, puoi personalizzare ulteriormente le metriche con opzioni aggiuntive. [Ulteriori informazioni](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-components/audiences/publish)

   ![](assets/audience_1.png)

1. Fai clic sul pulsante **[!UICONTROL Crea]** per finalizzare la creazione del pubblico. Tieni presente che il completamento di questo processo potrebbe richiedere del tempo.

Ora puoi continuare a utilizzare il pubblico appena creato con un Percorso o una campagna.

## Gestire i modelli {#cja-template}

>[!AVAILABILITY]
>
> La funzionalità **Modello** viene implementata progressivamente in più fasi, con disponibilità generale completa pianificata per la fine di gennaio e disponibile in esclusiva per gli utenti con una licenza [!DNL Customer Journey Analytics].

Ora puoi migliorare i rapporti di Journey Optimizer sfruttando i modelli di Customer Journey Analytics. [Ulteriori informazioni sul modello Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/templates/use-templates#use-reports)

Quando accedi ai tuoi report, puoi scegliere tra due tipi di modelli dal menu a discesa **[!UICONTROL Seleziona un modello]**:

* Modello predefinito fornito da Adobe
* Modelli generati dal cliente

![](assets/cja_template_5.png)

Se non è stato creato alcun modello, il menu a discesa **[!UICONTROL Seleziona modello]** non viene visualizzato nell&#39;interfaccia di reporting.

Per creare un modello, effettua le seguenti operazioni:

1. In [!DNL Customer Journey Analytics], passa al menu **[!UICONTROL Workspace]** e seleziona **[!UICONTROL Modelli Adobe]**. [Ulteriori informazioni sui modelli disponibili](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/templates/use-templates#available-templates)

1. Sfoglia i modelli predefiniti disponibili e fai clic su **[!UICONTROL Usa modello]** per selezionarne uno.

   ![](assets/cja_template_1.png)

1. Adatta il tuo report per soddisfare le tue esigenze. Consulta la [documentazione di Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/home).

1. Una volta completato il modello personalizzato, accedi al menu **[!UICONTROL Progetto]** e seleziona **[!UICONTROL Salva come modello]**.

   ![](assets/cja_template_2.png)

1. Fornisci i dettagli necessari per il modello. Per informazioni dettagliate, consulta la [documentazione di Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/templates/create-templates#edit-or-delete-a-template).

   >[!IMPORTANT]
   >
   > Assicurati di scegliere **Journey Optimizer** in **[!UICONTROL Casi d&#39;uso]** e di specificare il corrispondente **tipo di attività Journey Optimizer** e **attività**. Questo consente di visualizzare il rapporto in Journey Optimizer.

   ![](assets/cja_template_3.png)

1. In [!DNL Journey Optimizer], dal report, accedere al report e scegliere il modello creato in precedenza dal menu a discesa **[!UICONTROL Seleziona un modello]**.

   ![](assets/cja_template_4.png)

Per creare direttamente un modello dal report dell&#39;ottimizzatore di Percorso, è sufficiente accedere al report della campagna o del percorso, selezionare **[!UICONTROL Analizza in CJA]** e personalizzare il modello predefinito seguendo i passaggi descritti in precedenza.
