---
solution: Journey Optimizer
product: journey optimizer
title: Informazioni sui tipi di pubblico di Adobe Experience Platform
description: Scopri come utilizzare i tipi di pubblico di Adobe Experience Platform
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: 10d2de34-23c1-4a5e-b868-700b462312eb
source-git-commit: cdcce470481393c821d1c5df95639602510a690a
workflow-type: tm+mt
source-wordcount: '991'
ht-degree: 44%

---

# Introduzione ai tipi di pubblico di Adobe Experience Platform {#about-segments}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_segment"
>title="Pubblico"
>abstract="Sfruttando i dati del servizio profilo cliente in tempo reale, Adobe Experience Platform consente di generare facilmente definizioni di segmento per creare tipi di pubblico mirati, che acquisiscono preferenze e comportamenti univoci dei clienti."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_audience"
>title="Selezionare il pubblico della campagna"
>abstract="Questo elenco mostra tutti i tipi di pubblico di Adobe Experience Platform disponibili. Seleziona il pubblico a cui destinare la campagna. Il messaggio configurato nella campagna verrà inviato a tutti i singoli utenti appartenenti al pubblico selezionato. [Ulteriori informazioni sul pubblico](../audience/about-audiences.md)"

Un pubblico è un insieme di persone che condividono comportamenti e/o caratteristiche simili. Ulteriori informazioni sui tipi di pubblico in [Documentazione del servizio di segmentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=it){target="_blank"}.

[!DNL Journey Optimizer] consente di creare tipi di pubblico di Adobe Experience Platform direttamente dal **[!UICONTROL Tipi di pubblico]** e sfruttarli nei tuoi percorsi o campagne.

I tipi di pubblico possono essere generati utilizzando diversi metodi:

* **Definizioni dei segmenti**: crea una nuova definizione di pubblico utilizzando il servizio di segmentazione di Adobe Experience Platform. [Scopri come creare le definizioni dei segmenti](creating-a-segment-definition.md)
* **Importazione file CSV**: importa un pubblico utilizzando un file CSV. Scopri come importare i tipi di pubblico in Adobe Experience Platform [Documentazione del servizio di segmentazione](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html#import-audience){target="_blank"}.
* **Composizione del pubblico**: crea un flusso di lavoro di composizione per combinare i tipi di pubblico di Adobe Experience Platform esistenti in un’area di lavoro visiva e sfruttare varie attività (suddivisione, esclusione...) per creare nuovi tipi di pubblico. [Introduzione alla composizione dei tipi di pubblico](get-started-audience-orchestration.md)

## Targeting dei tipi di pubblico in [!DNL Journey Optimizer] {#segments-in-journey-optimizer}

Puoi selezionare nelle campagne e nei percorsi qualsiasi pubblico Adobe Experience Platform generato utilizzando [definizioni dei segmenti](../audience/creating-a-segment-definition.md).

>[!NOTE]
>
>Per il momento, i tipi di pubblico derivanti da [composizioni di pubblico](../audience/get-started-audience-orchestration.md) può essere impostato come destinazione solo nelle campagne. Questa funzionalità è disponibile come versione beta privata per i percorsi.
>
>L&#39;utilizzo del pubblico [caricato da un file CSV](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html#import-audience){target="_blank"} in campagne e percorsi è attualmente disponibile come versione beta privata.
>
>Per ulteriori informazioni, contatta il tuo rappresentante Adobe.

Puoi sfruttare i tipi di pubblico in **[!DNL Journey Optimizer]** in modi diversi:

* Scegli un pubblico per una **campagna**: il messaggio viene inviato a tutti i singoli utenti appartenenti al pubblico selezionato. [Scopri come definire il pubblico di una campagna](../campaigns/create-campaign.md#define-the-audience-audience).

* Utilizza un’attività di orchestrazione **Leggi pubblico** in un percorso per fare in modo che tutti i singoli utenti del pubblico entrino nel percorso e ricevano i messaggi inclusi nel percorso.

  Supponiamo che tu abbia un pubblico di tipo “cliente silver”. Con questa attività, puoi fare in modo che tutti i clienti silver entrino in un percorso e inviare loro una serie di messaggi personalizzati. [Scopri come configurare un’attività Leggi pubblico](../building-journeys/read-audience.md#configuring-segment-trigger-activity).

* Utilizza l’attività di evento **Qualificazione del pubblico** in un percorso per consentire a singoli utenti di entrare o proseguire nel percorso, sulla base degli ingressi e delle uscite del pubblico di Adobe Experience Platform.

  Ad esempio, puoi fare in modo che tutti i nuovi clienti silver entrino in un percorso e inviare loro messaggi. Per ulteriori informazioni su come utilizzare questa attività, fai riferimento a [Scopri come configurare un’attività di qualificazione del pubblico](../building-journeys/audience-qualification-events.md).

* Utilizza l’attività **Condizione** in un percorso per generare condizioni basate sull’iscrizione al pubblico. [Scopri come utilizzare i tipi di pubblico nelle condizioni](../building-journeys/condition-activity.md#using-a-segment).

## Metodi di valutazione del pubblico {#evaluation-method-in-journey-optimizer}

In Adobe Journey Optimizer, i tipi di pubblico vengono generati dalle definizioni dei segmenti utilizzando uno dei tre metodi di valutazione seguenti.

+++ Segmentazione in streaming

L’elenco dei profili per il pubblico viene tenuto aggiornato in tempo reale man mano che nuovi dati fluiscono nel sistema.

La segmentazione in streaming è un processo continuo di selezione di dati che aggiorna i tipi di pubblico in risposta all’attività dell’utente. Una volta generata la definizione di un segmento e salvato il pubblico risultante, la definizione del segmento viene applicata ai dati in entrata in Journey Optimizer. Ciò significa che gli individui vengono aggiunti o rimossi dal pubblico con la modifica dei dati del loro profilo, garantendo che il pubblico di destinazione sia sempre rilevante. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/streaming-segmentation.html){target="_blank"}

>[!NOTE]
>
>Assicurati di utilizzare gli eventi giusti come criteri di segmentazione in streaming. [Ulteriori informazioni](#streaming-segmentation-events-guardrails)

+++

+++ Segmentazione in batch

L’elenco dei profili per il pubblico viene valutato ogni 24 ore.

La segmentazione in batch è un’alternativa alla segmentazione in streaming che elabora tutti i dati di profilo contemporaneamente tramite le definizioni dei segmenti. In questo modo viene creata un’istantanea del pubblico, che è possibile salvare ed esportare per l’utilizzo. Tuttavia, a differenza della segmentazione in streaming, la segmentazione in batch non aggiorna continuamente l’elenco del pubblico in tempo reale e i nuovi dati che arrivano dopo il processo batch non verranno riflessi nel pubblico fino al successivo processo batch. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html#batch){target="_blank"}

+++

+++ Segmentazione Edge

La segmentazione Edge consente di valutare i segmenti in Adobe Experience Platform istantaneamente [sul bordo](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=it){target="_blank"}, enabling same-page and next-page personalization use cases. Currently only select query types can be evaluated with edge segmentation. [Learn more](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/edge-segmentation.html#query-types){target="_blank"}

+++

Se si conosce il metodo di valutazione da utilizzare, selezionarlo utilizzando l&#39;elenco a discesa. Per visualizzare un elenco dei metodi di valutazione delle definizioni dei segmenti disponibili, puoi anche fare clic sull’icona Sfoglia icona cartella con una lente di ingrandimento. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html#segment-properties){target="_blank"}

![](assets/evaluation-methods.png)

<!--The determination between batch segmentation and streaming segmentation is made by the system for each audience, based on the complexity and the cost of evaluating the segment definition rule. You can view the evaluation method for each audience in the **[!UICONTROL Evaluation method]** column of the audience list.
    
![](assets/evaluation-method.png)

>[!NOTE]
>
>If the **[!UICONTROL Evaluation method]** column does not display, you  need to add it using configuration button on the top right of the list.-->

Dopo aver definito per la prima volta un pubblico, vengono aggiunti i profili quando idonei.

Il recupero del pubblico dai dati precedenti può richiedere fino a 24 ore. Dopo il recupero, il pubblico viene aggionato costantemente ed è sempre pronto per il targeting.

### Utilizzo degli eventi con segmentazione in streaming {#streaming-segmentation-events-guardrails}

La segmentazione in streaming è utile per la personalizzazione in tempo reale con casi d’uso di alto valore. Tuttavia, è importante scegliere il diritto [Eventi](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html#events){target="_blank"} da utilizzare come criteri di segmentazione.

Di conseguenza, per prestazioni ottimali di segmentazione in streaming, evita di utilizzare i seguenti eventi:

* **Messaggio aperto** Evento tipo di interazione

  Durante la creazione del pubblico, l’utilizzo di **Messaggio aperto** gli eventi di interazione sono diventati inaffidabili, perché non sono indicatori effettivi dell’attività dell’utente e possono influire negativamente sulle prestazioni di segmentazione. Scopri perché in questo [Post di blog Adobe](https://blog.adobe.com/en/publish/2021/06/24/what-apples-mail-privacy-protection-means-for-email-marketers){target="_blank"}.

  Pertanto, l’Adobe consiglia di non utilizzare **Messaggio aperto** eventi di interazione con segmentazione in streaming. Utilizza invece segnali reali di attività dell’utente come clic, acquisti o dati beacon.

* **Messaggio inviato** Evento stato feedback

  Il **Messaggio inviato** l’evento di feedback viene spesso utilizzato per il controllo della frequenza o dell’eliminazione prima dell’invio di un’e-mail. L&#39;Adobe consiglia di evitarlo in quanto mette pressione sulle prestazioni e può causare il degrado del sistema.

  Pertanto, per la logica di frequenza o eliminazione, utilizza le regole di business anziché **Messaggio inviato** eventi di feedback. Si noti che presto saranno disponibili limiti di frequenza giornalieri per i singoli profili, a complemento della frequenza mensile esistente per le regole aziendali.

>[!NOTE]
>
>È possibile utilizzare **Messaggio aperto** e **Messaggio inviato** eventi nella segmentazione batch senza problemi di prestazioni.
