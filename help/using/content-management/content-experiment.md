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
source-git-commit: d4dce7b31d898d86c330048e6d0a1587e87a617c
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
>Prima di iniziare con Content Experiment, assicurati che la configurazione del reporting sia impostata per i set di dati personalizzati. Ulteriori informazioni in [questa sezione](../reports/reporting-configuration.md).

L’esperimento sui contenuti di Journey Optimizer consente di definire più trattamenti di consegna per misurare quale offre le migliori prestazioni per il pubblico di destinazione. Puoi scegliere di variare il contenuto, l’oggetto o il mittente della consegna. Il pubblico di interesse viene allocato in modo casuale a ciascun trattamento per determinare quale funziona meglio in termini di metrica specificata.

![](../rn/assets/do-not-localize/experiment.gif)

Nell’esempio seguente, l’obiettivo di consegna è stato suddiviso in due gruppi, ciascuno dei quali rappresenta il 45% della popolazione target e un gruppo di riserva del 10%, che non riceverà la consegna.

Ogni persona nel pubblico di destinazione riceverà una versione di un’e-mail, con un oggetto che corrisponde a uno dei due seguenti:

* uno promuove direttamente un’offerta del 10% sulla nuova collezione e un’immagine.
* l&#39;altra si limita a pubblicizzare un&#39;offerta speciale senza specificare il 10% di sconto senza alcuna immagine.

L’obiettivo qui è vedere se i destinatari interagiscono con l’e-mail a seconda dell’esperimento ricevuto. Pertanto, sceglieremo **[!UICONTROL Aperture e-mail]** come metrica di obiettivo principale in questo esperimento sui contenuti.

![](assets/content_experiment.png)

## Creare i contenuti {#campaign-experiment}

1. Inizia creando e configurando la tua notifica e-mail, SMS o push [campagna](../campaigns/create-campaign.md) o [percorso](../building-journeys/journeys-message.md) in base alle tue esigenze.

   >[!AVAILABILITY]
   >
   >La sperimentazione in Percorso è attualmente disponibile solo per un set di organizzazioni (disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.

1. Dalla finestra **[!UICONTROL Modifica contenuto]**, inizia a personalizzare il trattamento A.

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

1. Quando il messaggio è personalizzato, dalla pagina di riepilogo della campagna, fai clic su **[!UICONTROL Crea esperimento]** per iniziare a configurare l&#39;esperimento sui contenuti.

   ![](assets/content_experiment_3.png)

1. Seleziona la **[!UICONTROL metrica di successo]** da impostare per l&#39;esperimento.

   Per questo esempio, seleziona **[!UICONTROL E-mail aperta]** per verificare se i profili aprono le e-mail se il codice promozionale è nella riga dell&#39;oggetto.

   ![](assets/content_experiment_11.png)

1. Quando si configura un esperimento utilizzando il canale in-app o Web e si sceglie **[!UICONTROL Clic in entrata]**, **[!UICONTROL Clic in entrata univoci]**, **[!UICONTROL Visualizzazioni pagina]** o **[!UICONTROL Metriche visualizzazioni pagina univoche]** , il menu a discesa **[!UICONTROL Azione clic]** consente di monitorare e tenere traccia con precisione di clic e visualizzazioni su pagine specifiche.

   ![](assets/content_experiment_20.png)

1. Fare clic su **[!UICONTROL Aggiungi trattamento]** per creare il numero di nuovi trattamenti necessario.

   ![](assets/content_experiment_8.png)

1. Modifica il **[!UICONTROL Titolo]** del trattamento per differenziarli meglio.

1. Scegli di aggiungere un gruppo **[!UICONTROL Holdout]** alla consegna. Questo gruppo non riceverà alcun contenuto da questa campagna.

   Se passi alla barra di attivazione, riceverai automaticamente il 10% della tua popolazione; se necessario puoi regolare questa percentuale.

   >[!IMPORTANT]
   >
   >Quando un gruppo di sospensione viene utilizzato in un&#39;azione per la sperimentazione di contenuti, l&#39;assegnazione di sospensione si applica solo a tale azione specifica. Al termine dell’azione, i profili nel percorso di sospensione continueranno a scorrere lungo il percorso e potranno ricevere messaggi da altre azioni. Di conseguenza, assicurati che tutti i messaggi successivi non dipendano dalla ricezione di un messaggio da parte di un profilo che potrebbe trovarsi in un gruppo di attesa. In tal caso, potrebbe essere necessario rimuovere l&#39;assegnazione di blocco.

   ![](assets/content_experiment_12.png)

1. Puoi quindi scegliere di allocare una percentuale precisa a ogni **[!UICONTROL Trattamento]** o semplicemente attivare la barra di selezione **[!UICONTROL Distribuisci uniformemente]**.

   ![](assets/content_experiment_13.png)

1. Fai clic su **[!UICONTROL Crea]** quando la configurazione è impostata.

## Progettare i trattamenti {#treatment-experiment}

1. Dalla finestra **[!UICONTROL Modifica contenuto]**, seleziona il trattamento B per modificare il contenuto.

   In questo caso, si sceglie di non specificare l&#39;offerta nella **[!UICONTROL riga oggetto]**.

   ![](assets/content_experiment_18.png)

1. Fai clic su **[!UICONTROL Modifica corpo dell&#39;e-mail]** per personalizzare ulteriormente il trattamento B.

   ![](assets/content_experiment_9.png)

1. Dopo aver progettato i trattamenti, fai clic su **[!UICONTROL Altre azioni]** per accedere alle opzioni relative ai trattamenti: **[!UICONTROL Rinomina]**, **[!UICONTROL Duplica]** e **[!UICONTROL Elimina]**.

   ![](assets/content_experiment_7.png)

1. Se necessario, accedi al menu **[!UICONTROL Impostazioni esperimento]** per modificare la configurazione dei trattamenti.

   ![](assets/content_experiment_19.png)

1. Una volta definito il contenuto del messaggio, fai clic sul pulsante **[!UICONTROL Simula contenuto]** per controllare il rendering della consegna e controlla le impostazioni di personalizzazione con i profili di test. [Ulteriori informazioni](../content-management/preview-test.md)

Dopo aver configurato la sperimentazione, puoi seguire il successo della consegna con il tuo rapporto. [Ulteriori informazioni](../reports/campaign-global-report.md#experimentation-report)
