---
solution: Journey Optimizer
product: journey optimizer
title: Informazioni sui tipi di pubblico di Adobe Experience Platform
description: Scopri come utilizzare i tipi di pubblico di Adobe Experience Platform
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
mini-toc-levels: 1
exl-id: 10d2de34-23c1-4a5e-b868-700b462312eb
source-git-commit: 8a1ec5acef067e3e1d971deaa4b10cffa6294d75
workflow-type: tm+mt
source-wordcount: '1855'
ht-degree: 17%

---

# Introduzione ai tipi di pubblico di Adobe Experience Platform {#about-segments}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_segment"
>title="Pubblico"
>abstract="Sfruttando i dati del servizio profilo cliente in tempo reale, Adobe Experience Platform consente di generare facilmente definizioni di segmento per creare tipi di pubblico mirati, che acquisiscono preferenze e comportamenti univoci dei clienti."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_audience"
>title="Selezionare il pubblico della campagna"
>abstract="Questo elenco mostra tutti i tipi di pubblico di Adobe Experience Platform disponibili. Seleziona il pubblico di destinazione della campagna. Il messaggio configurato nella campagna verrà inviato a tutti i singoli utenti appartenenti al pubblico selezionato. [Ulteriori informazioni sui tipi di pubblico](../audience/about-audiences.md)"

Un pubblico è un insieme di persone che condividono comportamenti e/o caratteristiche simili. Ulteriori informazioni sui tipi di pubblico in [Documentazione del servizio di segmentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=it){target="_blank"}.

[!DNL Journey Optimizer] consente di creare tipi di pubblico di Adobe Experience Platform direttamente dal **[!UICONTROL Tipi di pubblico]** e sfruttarli nei tuoi percorsi o campagne.

I tipi di pubblico possono essere generati utilizzando diversi metodi:

* **Definizioni dei segmenti**: crea una nuova definizione di pubblico utilizzando il servizio di segmentazione di Adobe Experience Platform. [Scopri come creare le definizioni dei segmenti](creating-a-segment-definition.md)
* **Caricamento personalizzato**: importa un pubblico utilizzando un file CSV. Scopri come importare i tipi di pubblico in Adobe Experience Platform [Documentazione del servizio di segmentazione](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html#import-audience){target="_blank"}.
* **Composizione del pubblico**: crea un flusso di lavoro di composizione per combinare i tipi di pubblico di Adobe Experience Platform esistenti in un’area di lavoro visiva e sfruttare varie attività (suddivisione, esclusione...) per creare nuovi tipi di pubblico. [Introduzione alla composizione dei tipi di pubblico](get-started-audience-orchestration.md)

## Targeting dei tipi di pubblico in [!DNL Journey Optimizer] {#segments-in-journey-optimizer}

Nelle campagne e nei percorsi puoi selezionare qualsiasi pubblico generato utilizzando le definizioni dei segmenti, i flussi di lavoro di caricamento personalizzato o di composizione.

>[!AVAILABILITY]
>
>L’utilizzo di tipi di pubblico e attributi dalla composizione del pubblico e da tipi di pubblico con caricamento personalizzato (file CSV) non è attualmente disponibile per l’utilizzo con Healthcare Shield o Privacy and Security Shield. [Scopri come utilizzare gli attributi di arricchimento del pubblico in Journey Optimizer](../audience/about-audiences.md#enrichment)

Puoi sfruttare i tipi di pubblico in **[!DNL Journey Optimizer]** in modi diversi:

* Scegli un pubblico per una **campagna**: il messaggio viene inviato a tutti i singoli utenti appartenenti al pubblico selezionato. [Scopri come definire il pubblico di una campagna](../campaigns/create-campaign.md#define-the-audience-audience).

* Utilizza un **Read audience** attività di orchestrazione in un percorso per fare in modo che tutti i singoli utenti del pubblico entrino nel percorso e ricevano i messaggi inclusi nel percorso. Supponiamo che tu abbia un pubblico di tipo “cliente silver”. Con questa attività, puoi fare in modo che tutti i clienti silver entrino in un percorso e inviare loro una serie di messaggi personalizzati. [Scopri come configurare un’attività Leggi pubblico](../building-journeys/read-audience.md#configuring-segment-trigger-activity).

* Utilizza l’attività **Condizione** in un percorso per generare condizioni basate sull’iscrizione al pubblico. [Scopri come utilizzare i tipi di pubblico nelle condizioni](../building-journeys/condition-activity.md#using-a-segment).

* Utilizza il **Qualificazione del pubblico** attività evento in un percorso per consentire ai singoli utenti di entrare o proseguire nel percorso in base alle entrate e alle uscite del pubblico Adobe Experience Platform. Ad esempio, puoi fare in modo che tutti i nuovi clienti silver entrino in un percorso e inviare loro messaggi. Per ulteriori informazioni su come utilizzare questa attività, fai riferimento a [Scopri come configurare un’attività di qualificazione del pubblico](../building-journeys/audience-qualification-events.md).

  >[!NOTE]
  >
  >A causa della natura batch dei tipi di pubblico creati utilizzando flussi di lavoro di composizione e caricamento personalizzato, non puoi indirizzarli a un’attività &quot;Qualificazione del pubblico&quot;. Solo i tipi di pubblico creati utilizzando le definizioni dei segmenti possono essere utilizzati in questa attività.

## Utilizzare gli attributi di arricchimento del pubblico {#enrichment}

Quando esegui il targeting di un pubblico generato utilizzando i flussi di lavoro di composizione, puoi sfruttare gli attributi di arricchimento di questi tipi di pubblico per creare il percorso e personalizzare i messaggi.

Per utilizzare gli attributi di arricchimento in un Percorso, accertati che vengano aggiunti a un gruppo di campi nell’origine dati &quot;Experience Platform&quot;.

+++ Scopri come aggiungere attributi di arricchimento a un gruppo di campi

1. Passa a &quot;Amministrazione&quot; > &quot;Configurazione&quot; > &quot;Origini dati&quot;.
1. Selezionare &quot;Experience Platform&quot; e creare o modificare un gruppo di campi.
1. Apri il selettore di campi, individua gli attributi di arricchimento che desideri aggiungere e seleziona la casella di controllo accanto a essi.
1. Salva le modifiche.

Informazioni dettagliate sulle origini dei dati sono disponibili in queste sezioni:

* [Utilizzare l’origine dati Adobe Experience Platform](../datasource/adobe-experience-platform-data-source.md)
* [Configurare un’origine dati](../datasource/configure-data-sources.md)

+++

Una volta aggiunti gli attributi di arricchimento a un gruppo di campi, puoi sfruttarli in posizioni diverse in Journey Optimizer:

* **Creazione di più percorsi in un percorso** in base a regole che sfruttano gli attributi di arricchimento del pubblico di destinazione. A tal fine, esegui il targeting del pubblico utilizzando una [Read audience](../building-journeys/read-audience.md) attività, quindi crea regole in un [Condizione](../building-journeys/condition-activity.md) attività basata sugli attributi di arricchimento del pubblico.

  ![](assets/audience-enrichment-attribute-condition.png){width="70%" zoomable="yes"}

* **Personalizzare i messaggi** in percorsi o campagne aggiungendo attributi di arricchimento dal pubblico target nell’editor di personalizzazione. [Scopri come utilizzare l’editor di personalizzazione](../personalization/personalization-build-expressions.md)

  ![](assets/audience-enrichment-attribute-perso.png){width="70%" zoomable="yes"}

>[!AVAILABILITY]
>
>Gli attributi di arricchimento del caricamento personalizzati non sono ancora disponibili per l’utilizzo in Journey Optimizer.

## Metodi di valutazione del pubblico {#evaluation-method-in-journey-optimizer}

In Adobe Journey Optimizer, i tipi di pubblico vengono generati dalle definizioni dei segmenti utilizzando uno dei tre metodi di valutazione seguenti.

+++ Segmentazione in streaming

L’elenco dei profili per il pubblico viene tenuto aggiornato in tempo reale man mano che nuovi dati fluiscono nel sistema.

La segmentazione in streaming è un processo continuo di selezione di dati che aggiorna i tipi di pubblico in risposta all’attività dell’utente. Una volta generata la definizione di un segmento e salvato il pubblico risultante, la definizione del segmento viene applicata ai dati in entrata in Journey Optimizer. Ciò significa che gli individui vengono aggiunti o rimossi dal pubblico con la modifica dei dati del loro profilo, garantendo che il pubblico di destinazione sia sempre rilevante. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/streaming-segmentation.html?lang=it){target="_blank"}

>[!NOTE]
>
>Assicurati di utilizzare gli eventi giusti come criteri di segmentazione in streaming. [Ulteriori informazioni](#streaming-segmentation-events-guardrails)

+++

+++ Segmentazione batch

L’elenco dei profili per il pubblico viene valutato ogni 24 ore.

La segmentazione in batch è un’alternativa alla segmentazione in streaming che elabora tutti i dati di profilo contemporaneamente tramite le definizioni dei segmenti. In questo modo viene creata un’istantanea del pubblico, che è possibile salvare ed esportare per l’utilizzo. Tuttavia, a differenza della segmentazione in streaming, la segmentazione in batch non aggiorna continuamente l’elenco del pubblico in tempo reale e i nuovi dati che arrivano dopo il processo batch non verranno riflessi nel pubblico fino al successivo processo batch. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=it#batch){target="_blank"}

+++

+++ Segmentazione Edge

La segmentazione Edge consente di valutare i segmenti in Adobe Experience Platform istantaneamente [sul bordo](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html){target="_blank"}, abilitazione dei casi d’uso di personalizzazione della stessa pagina e della pagina successiva. Attualmente solo i tipi di query selezionati possono essere valutati con la segmentazione Edge. [Ulteriori informazioni](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/edge-segmentation.html#query-types){target="_blank"}

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

  Durante la creazione del pubblico, l’utilizzo di **Messaggio aperto** gli eventi di interazione sono diventati inaffidabili, perché non sono indicatori effettivi dell’attività dell’utente e possono influire negativamente sulle prestazioni di segmentazione. Scopri perché in questo [Post di blog Adobe](https://blog.adobe.com/en/publish/2021/06/24/what-apples-mail-privacy-protection-means-for-email-marketers){target="_blank"}. Pertanto, l’Adobe consiglia di non utilizzare **Messaggio aperto** eventi di interazione con segmentazione in streaming. Utilizza invece segnali reali di attività dell’utente come clic, acquisti o dati beacon.

* **Messaggio inviato** Evento stato feedback

  Il **Messaggio inviato** l’evento di feedback viene spesso utilizzato per il controllo della frequenza o dell’eliminazione prima dell’invio di un’e-mail. L&#39;Adobe consiglia di evitarlo in quanto mette pressione sulle prestazioni e può causare il degrado del sistema. Pertanto, per la logica di frequenza o eliminazione, utilizza le regole di business anziché **Messaggio inviato** eventi di feedback. Si noti che presto saranno disponibili limiti di frequenza giornalieri per i singoli profili, a complemento della frequenza mensile esistente per le regole aziendali.

>[!NOTE]
>
>È possibile utilizzare **Messaggio aperto** e **Messaggio inviato** eventi nella segmentazione batch senza problemi di prestazioni.


## Domande frequenti sulla composizione del pubblico e il caricamento personalizzato {#faq}

Nella sezione seguente sono elencate le domande frequenti sull’utilizzo in Journey Optimizer dei tipi di pubblico creati con flussi di lavoro di composizione e caricamento personalizzato (file CSV).

+++ Dove posso utilizzare i tipi di pubblico dalla composizione e dal caricamento personalizzato in Journey Optimizer?

I tipi di pubblico da composizione e caricamento personalizzati del pubblico possono essere targetizzati da campagne e percorsi. [Scopri come eseguire il targeting dei tipi di pubblico in [!DNL Journey Optimizer]](#segments-in-journey-optimizer)

* In entrata **Campagne**, questi tipi di pubblico vengono visualizzati nel selettore del pubblico dopo aver fatto clic sul pulsante &quot;Seleziona pubblico&quot;.

* In entrata **Percorsi**, è possibile utilizzare questi tipi di pubblico in un’attività &quot;Read Audience&quot; (Leggi pubblico) durante la selezione del pubblico e in un’attività &quot;Condition&quot; (Condizione) per i controlli di iscrizione al pubblico. Tuttavia, a causa della loro natura in batch, questi tipi di pubblico non vengono visualizzati nell’attività &quot;Qualificazione del pubblico&quot;.

  >[!NOTE]
  >
  >Per i tipi di pubblico di caricamento personalizzati, se &quot;Lettura incrementale&quot; è abilitato in un percorso ricorrente, i profili vengono recuperati solo alla prima ricorrenza, in quanto questi tipi di pubblico sono fissi.

Inoltre, questi tipi di pubblico sono disponibili per l’utilizzo nell’editor di personalizzazione per personalizzare i messaggi in percorsi e campagne. [Scopri come utilizzare l’editor di personalizzazione](../personalization/personalization-build-expressions.md)

+++

+++ Cosa sono gli attributi di arricchimento?

Gli attributi di arricchimento sono attributi aggiuntivi contestuali e specifici di un pubblico. Non sono associate al profilo e vengono generalmente utilizzate a scopo di personalizzazione.

Gli attributi di arricchimento sono collegati a un pubblico tramite un [Arricchire](composition-canvas.md#enrich) attività nella composizione del pubblico o attraverso il processo di caricamento personalizzato.

+++

+++ Dove posso utilizzare gli attributi di arricchimento in Journey Optimizer?

Gli attributi di arricchimento dalla composizione del pubblico possono essere utilizzati nelle seguenti aree. [Scopri come utilizzare gli attributi di arricchimento del pubblico](#enrichment)

* Attività condizione (Percorsi)
* Attributi azione personalizzati (Percorsi)
* Personalizzazione dei messaggi (Percorsi e campagne)

>[!AVAILABILITY]
>
>Gli attributi di arricchimento del caricamento personalizzati non sono ancora disponibili per l’utilizzo in Journey Optimizer.

+++

+++ Come si abilitano gli attributi di arricchimento nei Percorsi?

Per utilizzare gli attributi di arricchimento in un Percorso, accertati che vengano aggiunti a un gruppo di campi nell’origine dati &quot;Experience Platform&quot;. Le informazioni su come aggiungere attributi di arricchimento a un gruppo di campi sono disponibili in [questa sezione](#enrichment)

+++

+++ Quanto tempo dopo aver pubblicato un pubblico da una composizione di pubblico o da un caricamento personalizzato, posso utilizzarlo in Journey Optimizer?

* Tipi di pubblico da **composizione del pubblico** vengono eseguite ogni giorno, quindi potrebbe essere necessario attendere fino a 24 ore prima di utilizzarle in Journey Optimizer.
* Tipi di pubblico da **caricamento personalizzato** diventano disponibili in Journey Optimizer circa 2 ore dopo la pubblicazione.

+++

+++ I valori degli attributi di arricchimento vengono aggiornati dopo l’inizio di un percorso?

Attualmente no. Anche dopo i nodi di attesa o evento, i valori degli attributi di arricchimento rimangono invariati rispetto a quando il percorso è iniziato.

+++

+++ In che modo i tipi di pubblico di caricamento personalizzati si uniscono ai profili?

Durante il processo di caricamento personalizzato, specifica l’attributo CSV da utilizzare come identità e l’identità del profilo a cui è mappato. Questo stabilisce un collegamento tra i dati del pubblico e il profilo. Se il file CSV contiene un valore di identità non trovato nel profilo, viene creato un nuovo profilo con tale valore di identità.

Informazioni dettagliate sul processo di caricamento personalizzato sono disponibili in Adobe Experience Platform [Documentazione del servizio di segmentazione](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html#import-audience){target="_blank"}.

+++

+++ Quanto sono recenti i miei dati in Journey Optimizer?

I dati nei tipi di pubblico provenienti dalla composizione del pubblico e dal caricamento personalizzato vengono compilati dal servizio Esportazione pubblico (AES). AES legge gli attributi del profilo e l’iscrizione al pubblico, che rende disponibili a questi tipi di pubblico con le seguenti timeline:

* **Composizione del pubblico**: esportazione giornaliera (~24 ore)
* **Caricamento personalizzato**: processo di esportazione dedicato (circa 2 ore)

Qualsiasi percorso che utilizza un pubblico dalla composizione del pubblico o dal caricamento personalizzato nell’attività &quot;Read Audience&quot; (Leggi pubblico) avrà attributi di profilo aggiornati come l’ultima valutazione batch. Ciò include il consenso/la soppressione nel percorso.

Inoltre, gli attributi arricchiti nei tipi di pubblico di composizione del pubblico sono aggiornati quanto l’ultima esecuzione della composizione, che può durare fino a 24 ore nel passato.

+++

