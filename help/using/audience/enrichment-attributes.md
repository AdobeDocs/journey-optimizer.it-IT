---
solution: Journey Optimizer
product: journey optimizer
title: Informazioni sui tipi di pubblico di Adobe Experience Platform
description: Scopri come utilizzare i tipi di pubblico di Adobe Experience Platform
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: 3ec496ba-7555-49e2-992c-403c33302a90
source-git-commit: f99ba639b5d47fa334741b7e55e7bce83697626d
workflow-type: tm+mt
source-wordcount: '519'
ht-degree: 3%

---

# Utilizzare gli attributi di arricchimento del pubblico {#enrichment}

Quando esegui il targeting di un pubblico generato utilizzando flussi di lavoro di composizione, un pubblico personalizzato (file CSV) o una composizione di pubblico federato, puoi sfruttare gli attributi di arricchimento di questi tipi di pubblico per creare il percorso e personalizzare i messaggi.

>[!NOTE]
>
>I tipi di pubblico creati tramite il caricamento personalizzato di file CSV prima del 1° ottobre 2024 non sono idonei alla personalizzazione. Per utilizzare gli attributi di questi tipi di pubblico e sfruttare appieno questa funzione, ricreare e caricare nuovamente eventuali tipi di pubblico CSV esterno importati prima di questa data.
>
>I criteri di consenso non supportano gli attributi di arricchimento. Pertanto, eventuali regole dei criteri di consenso devono essere basate solo sugli attributi presenti nel profilo.

Di seguito sono elencate le azioni che puoi eseguire utilizzando gli attributi di arricchimento dei tipi di pubblico:

* **Crea più percorsi in un percorso** in base a regole che sfruttano gli attributi di arricchimento del pubblico di destinazione. A questo scopo, esegui il targeting del pubblico utilizzando un&#39;attività [Read audience](../building-journeys/read-audience.md), quindi crea regole in un&#39;attività [Condition](../building-journeys/condition-activity.md) in base agli attributi di arricchimento del pubblico.

  ![](assets/audience-enrichment-attribute-condition.png){width="70%" zoomable="yes"}

* **Personalizza i messaggi** in percorsi o campagne aggiungendo attributi di arricchimento dal pubblico di destinazione nell&#39;editor di personalizzazione. [Scopri come utilizzare l&#39;editor di personalizzazione](../personalization/personalization-build-expressions.md)

  ![](assets/audience-enrichment-attribute-perso.png){width="70%" zoomable="yes"}

>[!IMPORTANT]
>
>Per utilizzare gli attributi di arricchimento dei tipi di pubblico creati con flussi di lavoro di composizione, accertati che vengano aggiunti a un gruppo di campi nel Data Source di &quot;Experience Platform&quot;.
>
+++ Scopri come aggiungere attributi di arricchimento a un gruppo di campi>
>
1. Passa a &quot;Amministrazione&quot; > &quot;Configurazione&quot; > &quot;Origini dati&quot;.
1. Selezionare &quot;Experience Platform&quot; e creare o modificare un gruppo di campi.
1. Nel selettore schema, seleziona lo schema appropriato. Il nome dello schema sarà nel seguente formato: &quot;Schema per audienceId:&quot; + l’ID del pubblico. Puoi trovare l’ID del pubblico nella schermata dei dettagli del pubblico nell’inventario del pubblico.
1. Apri il selettore di campi, individua gli attributi di arricchimento che desideri aggiungere e seleziona la casella di controllo accanto a essi.
1. Salva le modifiche.
1. Una volta aggiunti gli attributi di arricchimento a un gruppo di campi, puoi sfruttarli in Journey Optimizer nelle posizioni elencate in precedenza.
>
Informazioni dettagliate sulle origini dei dati sono disponibili in queste sezioni:
>
* [Utilizzare l&#39;origine dati di Adobe Experience Platform](../datasource/adobe-experience-platform-data-source.md)
* [Configurare un&#39;origine dati](../datasource/configure-data-sources.md)
>
+++







+++ Cosa sono gli attributi di arricchimento?

Gli attributi di arricchimento sono attributi aggiuntivi contestuali e specifici di un pubblico. Non sono associate al profilo e vengono generalmente utilizzate a scopo di personalizzazione.

Gli attributi di arricchimento sono collegati a un pubblico tramite un’attività Arricchisci nella composizione del pubblico o tramite il processo di caricamento personalizzato.

+++

+++ Dove posso utilizzare gli attributi di arricchimento in Journey Optimizer?

Gli attributi di arricchimento dalla composizione del pubblico possono essere utilizzati nelle seguenti aree. [Scopri come utilizzare gli attributi di arricchimento del pubblico](#enrichment)

* Attività condizione (Percorsi)
* Attributi azione personalizzati (Percorsi)
* Personalizzazione dei messaggi (Percorsi e campagne)

+++

+++ Come si abilitano gli attributi di arricchimento nei Percorsi?

Per utilizzare gli attributi di arricchimento dei tipi di pubblico creati con flussi di lavoro di composizione, assicurati che vengano aggiunti a un gruppo di campi nel Data Source di &quot;Experience Platform&quot;. Le informazioni su come aggiungere attributi di arricchimento a un gruppo di campi sono disponibili in [questa sezione](#enrichment)

+++

+++ I valori degli attributi di arricchimento vengono aggiornati dopo l’inizio di un percorso?

Attualmente no. Anche dopo i nodi di attesa o evento, i valori degli attributi di arricchimento rimangono invariati rispetto a quando il percorso è iniziato.

+++
