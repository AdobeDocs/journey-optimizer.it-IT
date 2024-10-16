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
source-git-commit: 47482adb84e05fe41eb1c50479a8b50e00469ec4
workflow-type: tm+mt
source-wordcount: '873'
ht-degree: 28%

---

# Introduzione ai rapporti globali {#global-report}

>[!AVAILABILITY]
>
>L’esperienza di reporting corrente verrà ritirata a gennaio 2025. Dopo questa data, la nuova esperienza di reporting diventerà lo standard. Consigliamo di acquisire familiarità con le nuove funzioni e funzionalità per garantire una transizione senza problemi. [Introduzione alla nuova interfaccia di Journey Optimizer per la generazione di rapporti.](report-gs-cja.md)

>[!NOTE]
>
> Se vengono effettuate query personalizzate tramite API quando si utilizza Query Service, si prega di attendere un certo ritardo per i rapporti.

Utilizza il **[!UICONTROL Global report]** per misurare l&#39;impatto dei tuoi percorsi e delle tue consegne in un periodo di tempo selezionato.

* Se desideri eseguire il targeting di uno o più percorsi nel contesto di un percorso, dal menu **[!UICONTROL Percorsi]**, accedi al percorso e fai clic sul pulsante **[!UICONTROL Visualizza rapporto]**. Puoi quindi trovare i rapporti globali relativi a Percorso, e-mail, SMS e push.

  ![](assets/report_journey.png)

* Se desideri eseguire il targeting di una campagna, dal menu **[!UICONTROL Campagne]**, accedi alla campagna e fai clic sul pulsante **[!UICONTROL Rapporti]**.

  ![](assets/report_campaign.png)

* Se desideri passare dal **[!UICONTROL Rapporto live]** al **[!UICONTROL Rapporto globale]** per la consegna, fai clic su **[!UICONTROL Tutto il tempo]** nel cambio scheda.

  ![](assets/report_5.png)

Per un elenco dettagliato di tutte le metriche disponibili in Adobe Journey Optimizer, consulta [questa pagina](#list-of-components-global)

## Personalizza dashboard {#modify-dashboard}

Ogni dashboard di reporting può essere modificato modificando il periodo di tempo e ridimensionando o rimuovendo i widget. La modifica dei widget ha effetto solo sul dashboard dell&#39;utente corrente. Gli altri utenti visualizzeranno le proprie dashboard o quelle impostate per impostazione predefinita.

1. Dal rapporto globale, seleziona un’ora di inizio e di fine per eseguire il targeting di dati specifici.

   ![](assets/report_modify_1.png)

1. Per i report di Percorso che coinvolgono più **[!UICONTROL Azioni]** configurate, scegli un **[!UICONTROL Azione]** specifico dal menu a discesa.

1. Se si desidera eseguire il targeting solo di uno o più messaggi ricorrenti, selezionarlo dal menu a discesa **[!UICONTROL Tempo di esecuzione]**.

   ![](assets/report_modify_12.png)

1. Scegliere se si desidera escludere gli eventi di test dai rapporti con la barra di attivazione. Per ulteriori informazioni sugli eventi di test, fare riferimento a [questa pagina](../building-journeys/testing-the-journey.md).

   L&#39;opzione **[!UICONTROL Escludi eventi di test]** è disponibile solo per i report di Percorso.

   ![](assets/report_modify_2.png)

1. Fai clic su **[!UICONTROL Modifica]** per iniziare a personalizzare il dashboard.

   ![](assets/report_modify_3.png)

1. Regolate le dimensioni dei widget trascinandone l&#39;angolo inferiore destro.

   ![](assets/report_modify_4.png)

1. Fai clic su **[!UICONTROL Rimuovi]** per rimuovere i widget non necessari.

   ![](assets/report_modify_5.png)

1. Una volta che sei soddisfatto dell&#39;ordine di visualizzazione e delle dimensioni dei widget, fai clic su **[!UICONTROL Salva]**.

1. Per personalizzare la modalità di visualizzazione dei dati, puoi passare da diverse opzioni di visualizzazione, ad esempio grafici, tabelle e grafici ad anello.

   ![](assets/report_modify_10.png)

Il dashboard è ora salvato. Le diverse modifiche verranno riapplicate per un utilizzo successivo dei rapporti live. Se necessario, utilizzare l&#39;opzione **[!UICONTROL Reimposta]** per ripristinare l&#39;ordine dei widget e dei widget predefiniti.

## Esportazione dei rapporti {#export-reports}

Puoi esportare facilmente i diversi rapporti in formato PDF o CSV, per condividerli o stamparli. I passaggi per esportare i rapporti sono descritti nelle schede seguenti.

➡️ [Scopri questa funzione nel video](#video-csv)


>[!BEGINTABS]

>[!TAB Esporta il report come file CSV]

1. Dal tuo report, fai clic su **[!UICONTROL Esporta]** e seleziona **[!UICONTROL File CSV]** per generare un file CSV a livello di report complessivo.

   ![](assets/export_1.png)

1. Puoi anche scegliere di esportare i dati da un widget specifico. Fai clic su **[!UICONTROL Esporta dati widget in CSV]** accanto al widget selezionato.

   ![](assets/export_3.png)

1. Il file viene scaricato automaticamente e si trova nei file locali.

   Se hai generato il file a livello di report, contiene informazioni dettagliate per ciascun widget, inclusi il titolo e i dati.

   Se hai generato il file a livello di widget, fornisce specificamente i dati per il widget selezionato.

>[!TAB Esporta il report come file PDF]

1. Dal report, fai clic su **[!UICONTROL Esporta]** e seleziona **[!UICONTROL File PDF]**.

   ![](assets/export_2.png)

1. Nella finestra Stampa configurare il documento in base alle esigenze. Le opzioni possono variare a seconda del browser in uso.

1. Scegliere se stampare o salvare il report come PDF.

1. Individuare la cartella in cui si desidera salvare il file, rinominarlo, se necessario, e fare clic su Salva.

Il report è ora disponibile per la visualizzazione o la condivisione in un file pdf.



>[!ENDTABS]


### Esportare i rapporti (video) {#video-csv}

Scopri come scaricare un rapporto CSV per un rapporto e per un singolo widget nel seguente video tutorial.

>[!VIDEO](https://video.tv.adobe.com/v/3424603?quality=12)



>[!CONTEXTUALHELP]
>id="ajo_report_campaign_ctr"
>title="Tasso di click-through"
>abstract="Widget tasso di click-through"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_clicks"
>title="Clic"
>abstract="Widget clic"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_delivered"
>title="Consegnate"
>abstract="Widget consegnati"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_overview"
>title="Panoramica della campagna"
>abstract="Widget panoramica della campagna"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_funnel"
>title="Risultati funnel della campagna"
>abstract="Widget risultati funnel della campagna"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_tracking_link"
>title="Etichette collegamenti tracciati"
>abstract="Widget etichette collegamenti tracciati"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_displays"
>title="Visualizzazioni"
>abstract="Widget visualizzazioni"

<!--campaign email-->

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_email_delivered_click"
>title="Tendenza consegnati e clic"
>abstract="Widget tendenza consegnati e clic"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_email_delivery_status"
>title="Stato consegna"
>abstract="Widget stato consegna"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_email_sending_statistics"
>title="Statistiche di invio"
>abstract="Widget statistiche di invio"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_email_tracking_statistics"
>title="Statistiche di tracciamento"
>abstract="Widget statistiche di tracciamento"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_email_domains"
>title="Domini e-mail"
>abstract="Widget domini e-mail"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_email_tracked_link"
>title="Etichette collegamenti tracciati"
>abstract="Widget etichette collegamenti tracciamenti"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_email_tracked_link_urls"
>title="URL collegamenti tracciati"
>abstract="Widget URL collegamenti tracciati"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_email_subjects"
>title="Oggetti e-mail"
>abstract="Widget oggetti e-mail"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_email_bounce_reasons"
>title="Motivi di mancato recapito"
>abstract="Widget motivi di mancato recapito"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_email_exclude"
>title="Motivi di esclusione"
>abstract="Widget motivi di esclusione"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_email_error"
>title="Motivi di errore"
>abstract="Widget motivi di errore"


<!--campaign push-->

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_push_sending_statistics"
>title="Statistiche di invio"
>abstract="Widget statistiche di invio"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_push_tracking_statistics"
>title="Statistiche di tracciamento"
>abstract="Widget statistiche di tracciamento"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_push_tracked_link"
>title="Etichette collegamenti tracciati"
>abstract="Widget etichette collegamenti tracciamenti"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_push_tracked_link_urls"
>title="URL collegamenti tracciati"
>abstract="Widget URL collegamenti tracciati"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_push_bounce_reasons"
>title="Motivi di mancato recapito"
>abstract="Widget motivi di mancato recapito"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_push_exclude"
>title="Motivi di esclusione"
>abstract="Widget motivi di esclusione"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_push_email_error"
>title="Motivi di errore"
>abstract="Widget motivi di errore"

<!--campaign inapp-->


>[!CONTEXTUALHELP]
>id="ajo_report_campaign_inapp_impression"
>title="Tendenza impression e clic"
>abstract="Widget tendenza impression e clic"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_inapp_clicks"
>title="Clic"
>abstract="Widget clic"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_inapp_displays"
>title="Visualizzazioni"
>abstract="Widget visualizzazioni"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_inapp_tracking_data"
>title="Dati di tracciamento"
>abstract="Widget dati di tracciamento"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_inapp_tracked_link"
>title="Etichette collegamenti tracciati"
>abstract="Widget etichette collegamenti tracciati"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_inapp_tracked_link_urls"
>title="URL collegamenti tracciati"
>abstract="Widget URL collegamenti tracciati"

<!--campaign sms-->


>[!CONTEXTUALHELP]
>id="ajo_report_campaign_sms_delivered_click"
>title="Tendenza consegnati e clic"
>abstract="Widget tendenza consegnati e clic"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_sms_delivery_status"
>title="Stato consegna"
>abstract="Widget stato consegna"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_sms_tracked_link"
>title="Etichette collegamenti tracciati"
>abstract="Widget etichette collegamenti tracciamenti"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_sms_tracked_link_urls"
>title="URL collegamenti tracciati"
>abstract="Widget URL collegamenti tracciati"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_sms_inbound"
>title="Messaggio SMS in entrata"
>abstract="Widget messaggio SMS in entrata"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_sms_message_type"
>title="Tipo di messaggio SMS"
>abstract="Widget tipo di messaggio SMS"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_sms_providers"
>title="Provider SMS"
>abstract="Widget provider SMS"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_sms_bounce"
>title="Motivi di mancato recapito"
>abstract="Widget motivi di mancato recapito"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_sms_exclude"
>title="Motivi di esclusione"
>abstract="Widget motivi di esclusione"

>[!CONTEXTUALHELP]
>id="ajo_report_campaign_sms_error"
>title="Motivi di errore"
>abstract="Widget motivi di errore"
