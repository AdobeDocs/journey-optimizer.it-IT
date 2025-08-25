---
solution: Journey Optimizer
product: journey optimizer
title: Esportazione di messaggi in Journey Optimizer
description: Scopri come esportare i messaggi
feature: Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: esportazione, messaggi, HIPAA, e-mail, SMS, configurazione
badge: label="Disponibilità limitata" type="Informative"
hide: true
hidefromtoc: true
exl-id: 7b50c933-9738-4b1b-acae-08f0a8d41dab
source-git-commit: c62653af3c1eacaaf55dcf181d33f2253521e33d
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 13%

---

# Esportare il contenuto del messaggio {#message-export}

>[!CONTEXTUALHELP]
>id="ajo_admin_msg_export"
>title="Conservare ed esportare i contenuti inviati"
>abstract="Seleziona questa opzione per scrivere i contenuti dei messaggi e-mail o SMS inviati utilizzando questa configurazione in un set di dati [!DNL Experience Platform]. I record vengono conservati per 3 giorni di calendario, durante i quali puoi esportarli nella tua archiviazione."

>[!AVAILABILITY]
>
>Questa funzione è attualmente disponibile solo per un set di organizzazioni (disponibilità limitata). Per ulteriori informazioni, contatta il tuo rappresentante Adobe.

**Esportazione messaggi** consente di trasferire il contenuto dei messaggi e-mail e SMS inviati da [!DNL Journey Optimizer] al proprio archivio tramite [!DNL Adobe Experience Platform] destinazioni, che consentono di inviare dati da [!DNL Experience Platform] agli endpoint esterni. [Ulteriori informazioni](https://experienceleague.adobe.com/it/docs/experience-platform/destinations/home){target="_blank"}

Con questa funzione, il contenuto dei messaggi e-mail e SMS inviati tramite [!DNL Journey Optimizer] che sono stati contrassegnati per l&#39;esportazione viene scritto nel [!DNL Experience Platform] **set di dati di esportazione messaggi di AJO**.

I record vengono quindi conservati nel **set di dati di esportazione messaggi di AJO** per tre giorni di calendario, durante i quali è possibile esportarli nel sistema esterno desiderato.
<!--
## Terminology

* **[!DNL Experience Platform] destinations** - Framework to deliver data out of Experience Platform into external endpoints. [Learn more](https://experienceleague.adobe.com/it/docs/experience-platform/destinations/home){target="_blank"}
* **AJO Message Export Dataset** - An [!DNL Experience Platform] dataset which stores the message content of email and SMS messages sent via [!DNL Journey Optimizer] which have been marked for export.
* **Retention**: Records in the AJO Message Export Dataset are retained for 3 calendar days from ingestion.-->

## Guardrail

* Questa funzione supporta solo i canali E-mail e SMS.
* I record nel set di dati di esportazione dei messaggi di AJO vengono conservati per tre giorni di calendario dall’acquisizione.
* Il backfill non è supportato per i messaggi inviati prima di abilitare l’esportazione dei messaggi come descritto di seguito.

## Abilita esportazione messaggi {#enable-message-export}

Il processo di onboarding per la funzione Esportazione messaggi è costituito da due passaggi:

1. [Imposta il flusso di dati di esportazione](#set-up-export-dataflow) in [!DNL Experience Platform];
1. [Abilita esportazione messaggi](#config-message-export) nella configurazione del canale in [!DNL Journey Optimizer].

>[!WARNING]
>
>Verranno visualizzati solo i nuovi record dopo l’abilitazione delle esportazioni e l’invio dei messaggi. I backfill per il contenuto prima di impostare il processo di esportazione e di abilitare l’opzione Esporta messaggio non sono supportati.

### Configurare il flusso di dati di esportazione {#set-up-export-dataflow}

Prima di poter esportare i dati, è necessario impostare il processo di esportazione definendo la destinazione [!DNL Experience Platform] e il set di dati che verrà utilizzato. Segui i passaggi seguenti.

>[!NOTE]
>
>Questa configurazione deve essere configurata per ogni sandbox.

1. Scegli un tipo di destinazione [Experience Platform](https://experienceleague.adobe.com/it/docs/experience-platform/destinations/destination-types){target="_blank"}. Un elenco delle piattaforme di destinazione disponibili pronte per la ricezione dei dati è disponibile in [questa pagina](https://experienceleague.adobe.com/it/docs/experience-platform/destinations/catalog/overview){target="_blank"}.

1. In [!DNL Experience Platform], configura la destinazione definendo credenziali, bucket/contenitore, prefisso percorso e opzioni di sicurezza. [Scopri come](https://experienceleague.adobe.com/it/docs/experience-platform/destinations/ui/activate/export-datasets){target="_blank"}

1. Crea un flusso di esportazione di set di dati utilizzando i seguenti dati:

   * Set di dati di Source: seleziona **Set di dati esportazione messaggi di AJO**.
   * Formato file: seleziona JSON o Parquet (scegli uno in base agli strumenti a valle).
   * Pianificazione: assicurati che venga eseguito entro l’intervallo di conservazione di 3 giorni.

### Abilitare l’esportazione dei messaggi nella configurazione del canale {#config-message-export}

Per applicare l’esportazione dei messaggi alle campagne e ai percorsi, devi abilitare l’opzione dedicata a livello di configurazione del canale. Segui i passaggi seguenti.

1. In [!DNL Journey Optimizer], modificare o creare la configurazione del [canale](channel-surfaces.md#create-channel-surface) e-mail o SMS desiderata.

1. Selezionare l&#39;opzione **[!UICONTROL Abilita esportazione messaggi]**.

   ![](assets/config-message-export.png)

1. Salva le modifiche e invia la configurazione del canale.

I messaggi e-mail e SMS inviati tramite campagne o percorsi utilizzando questa configurazione di canale vengono scritti nel **set di dati di esportazione messaggi di AJO**. I record vengono quindi esportati nella destinazione di archiviazione selezionata in base al flusso di dati di esportazione definito.

Se si disabilita l&#39;opzione **[!UICONTROL Abilita esportazione messaggi]**, i nuovi record per questa configurazione del canale non verranno acquisiti nel set di dati. I record esistenti rimangono fino alla scadenza della conservazione.
