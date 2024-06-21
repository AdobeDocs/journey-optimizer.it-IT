---
solution: Journey Optimizer
product: journey optimizer
title: Creare un esperimento sui contenuti
description: Scopri come creare un esperimento sui contenuti nelle campagne
feature: Experimentation
topic: Content Management
role: User
level: Beginner
keywords: contenuto, esperimento, multiplo, pubblico, trattamento
exl-id: bd35ae19-8713-4571-80bc-5f40e642d121
source-git-commit: 59ecb9a5376e697061ddac4cc68f09dee68570c0
workflow-type: tm+mt
source-wordcount: '755'
ht-degree: 13%

---

# Creare un esperimento sui contenuti {#content-experiment}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment"
>title="Esperimento sui contenuti"
>abstract="Puoi scegliere di variare il contenuto, l’oggetto o il mittente del messaggio al fine di definire più trattamenti e determinare la combinazione migliore per i tipi dl pubblico."

>[!NOTE]
>
>Prima di iniziare con Content Experiment, assicurati che la configurazione del reporting sia impostata per i set di dati personalizzati. Ulteriori informazioni in [questa sezione](reporting-configuration.md).

L’esperimento sui contenuti di Journey Optimizer consente di definire più trattamenti di consegna per misurare quale offre le migliori prestazioni per il pubblico di destinazione. Puoi scegliere di variare il contenuto, l’oggetto o il mittente della consegna. Il pubblico di interesse viene allocato in modo casuale a ciascun trattamento per determinare quale funziona meglio in termini di metrica specificata.

![](../rn/assets/do-not-localize/experiment.gif)

Nell’esempio seguente, l’obiettivo di consegna è stato suddiviso in due gruppi, ciascuno dei quali rappresenta il 45% della popolazione target e un gruppo di riserva del 10%, che non riceverà la consegna.

Ogni persona nel pubblico di destinazione riceverà una versione di un’e-mail, con un oggetto che corrisponde a uno dei due seguenti:

* uno promuove direttamente un’offerta del 10% sulla nuova collezione e un’immagine.
* l&#39;altra si limita a pubblicizzare un&#39;offerta speciale senza specificare il 10% di sconto senza alcuna immagine.

L’obiettivo qui è vedere se i destinatari interagiscono con l’e-mail a seconda dell’esperimento ricevuto. Pertanto sceglieremo **[!UICONTROL Aperture e-mail]** come metrica di obiettivo principale in questo esperimento sui contenuti.

![](assets/content_experiment.png)

## Creare i contenuti {#campaign-experiment}

1. Per iniziare, crea e configura le notifiche e-mail, SMS o push [campagna](../campaigns/create-campaign.md) o [percorso](../building-journeys/journeys-message.md) in base alle tue esigenze.

   >[!AVAILABILITY]
   >
   >La sperimentazione in Percorso è attualmente disponibile solo per un set di organizzazioni (disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.

1. Dalla sezione **[!UICONTROL Modifica contenuto]** finestra, iniziare a personalizzare il trattamento A.

   Per questo trattamento, specificheremo l’offerta speciale direttamente nell’oggetto e aggiungeremo la personalizzazione.

   ![](assets/content_experiment_5.png)

1. Crea o importa il contenuto originale e personalizzalo in base alle esigenze.

## Configurare l’esperimento sui contenuti {#configure-experiment}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_dimension"
>title="Dimensione"
>abstract="Scegli la dimensione da monitorare per l’esperimento, ad esempio clic o visualizzazioni specifici di pagine specifiche."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_success_metric"
>title="Metrica di successo"
>abstract="La metrica di successo viene utilizzata per monitorare e valutare il trattamento dalle prestazioni migliori in un esperimento. Assicurati di impostare il set di dati per determinate metriche prima di utilizzarlo."

1. Quando il messaggio è personalizzato, dalla pagina di riepilogo della campagna fai clic su **[!UICONTROL Crea esperimento]** per iniziare a configurare l’esperimento sui contenuti.

   ![](assets/content_experiment_3.png)

1. Seleziona la **[!UICONTROL Metrica di successo]** desideri impostare per l’esperimento.

   Per questo esempio, seleziona **[!UICONTROL E-mail aperta]** per verificare se i profili aprono le e-mail se il codice promozionale è nella riga dell’oggetto.

   ![](assets/content_experiment_11.png)

1. Quando si imposta un esperimento utilizzando il canale in-app o web e si sceglie **[!UICONTROL Clic in entrata]**, **[!UICONTROL Clic univoci in entrata]** , **[!UICONTROL Visualizzazioni pagina]** , o **[!UICONTROL Metriche delle visualizzazioni di pagina univoche]** , il **[!UICONTROL Azione clic]**  a discesa consente di monitorare e tenere traccia con precisione dei clic e delle visualizzazioni su pagine specifiche.

   ![](assets/content_experiment_20.png)

1. Clic **[!UICONTROL Aggiungi trattamento]** per creare il maggior numero di nuovi trattamenti necessario.

   ![](assets/content_experiment_8.png)

1. Modificare il **[!UICONTROL Titolo]** del trattamento per differenziarli meglio.

1. Scegli di aggiungere una **[!UICONTROL Blocco]** raggruppa per la consegna. Questo gruppo non riceverà alcun contenuto da questa campagna.

   Se passi alla barra di attivazione, riceverai automaticamente il 10% della tua popolazione; se necessario puoi regolare questa percentuale.

   >[!IMPORTANT]
   >
   >Quando un gruppo di sospensione viene utilizzato in un&#39;azione per la sperimentazione di contenuti, l&#39;assegnazione di sospensione si applica solo a tale azione specifica. Al termine dell’azione, i profili nel percorso di sospensione continueranno a scorrere lungo il percorso e potranno ricevere messaggi da altre azioni. Di conseguenza, assicurati che tutti i messaggi successivi non dipendano dalla ricezione di un messaggio da parte di un profilo che potrebbe trovarsi in un gruppo di attesa. In tal caso, potrebbe essere necessario rimuovere l&#39;assegnazione di blocco.

   ![](assets/content_experiment_12.png)

1. Puoi quindi scegliere di allocare una percentuale precisa a ciascuno **[!UICONTROL Trattamento]** o semplicemente accendere il **[!UICONTROL Distribuisci uniformemente]** barra di selezione.

   ![](assets/content_experiment_13.png)

1. Clic **[!UICONTROL Crea]** quando la configurazione è impostata.

## Progettare i trattamenti {#treatment-experiment}

1. Dalla sezione **[!UICONTROL Modifica contenuto]** finestra, selezionare il trattamento B per modificare il contenuto.

   In questo caso, scegliamo di non specificare l’offerta nel **[!UICONTROL Oggetto]**.

   ![](assets/content_experiment_18.png)

1. Clic **[!UICONTROL Modifica corpo dell’e-mail]** per personalizzare ulteriormente il trattamento B.

   ![](assets/content_experiment_9.png)

1. Dopo aver progettato i trattamenti, fai clic su **[!UICONTROL Altre azioni]** per accedere alle opzioni relative ai trattamenti: **[!UICONTROL Rinomina]**, **[!UICONTROL Duplica]** e **[!UICONTROL Elimina]**.

   ![](assets/content_experiment_7.png)

1. Se necessario, accedi a **[!UICONTROL Impostazioni esperimento]** per modificare la configurazione dei trattamenti.

   ![](assets/content_experiment_19.png)

1. Una volta definito il contenuto del messaggio, fai clic su **[!UICONTROL Simula contenuto]** per controllare il rendering della consegna e controllare le impostazioni di personalizzazione con i profili di test. [Ulteriori informazioni](../content-management/preview-test.md)

Dopo aver configurato la sperimentazione, puoi seguire il successo della consegna con il tuo rapporto. [Ulteriori informazioni](../reports/campaign-global-report.md#experimentation-report)
