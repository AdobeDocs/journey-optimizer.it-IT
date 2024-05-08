---
title: Sfruttare i dati contestuali in Experience Decisioning
description: Scopri come sfruttare i dati contestuali in Experience Decisioning
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
badge: label="Disponibilità limitata"
source-git-commit: 5ce388e5d86950e5cc6b173aab48225825f1c648
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 0%

---

# Sfruttare i dati contestuali in Experience Decisioning {#context}

Con Experience Decisioning puoi sfruttare qualsiasi informazione disponibile in Adobe Experience Platform per eseguire varie azioni, ad esempio la creazione di [regole di decisione](rules.md) o [formule di classificazione](ranking.md). Ad esempio, puoi progettare una regola di decisione che richiede che il tempo corrente sia di ≥80 gradi al momento della richiesta di decisione.

>[!NOTE]
>
>I dati contestuali sono definiti in Adobe Experience Platform e vengono inviati al momento di una richiesta di decisione. Non include dati storici.

Per utilizzare i dati contestuali, devi innanzitutto definire i dati che desideri rendere disponibili in Experience Decisioning. Al termine, questi dati si integrano perfettamente in Experience Decisioning in **[!UICONTROL Dati contestuali]** disponibile durante la creazione di una regola di decisione. Puoi anche sfruttare i dati quando modifichi una formula di classificazione.

![](assets/decision-rules-context.png)

I passaggi per alimentare Experience Decisioning con i dati di Adobe Experience Platform sono i seguenti:

1. Creare un **Schema Experience Event**  in Adobe Experience Platform e relativi **set di dati**. [Scopri come creare schemi](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/resources/schemas){target="_blank"}

1. Crea un nuovo flusso di dati Adobe Experience Platform:

   1. Accedi a **[!UICONTROL Flussi di dati]** menu e seleziona **[!UICONTROL Nuovo flusso di dati]**.

   1. In **[!UICONTROL Schema Evento]** , seleziona lo schema Experience Event creato in precedenza e fai clic su **[!UICONTROL Salva]**.

      ![](assets/decision-rule-context-datastream.png)

   1. Clic **[!UICONTROL Aggiungi servizio]** e selezionare &quot;Adobe Experience Platform&quot; come servizio. In **[!UICONTROL Set di dati evento]** , seleziona il set di dati evento creato in precedenza e abilita **[!UICONTROL Adobe Journey Optimizer]** opzione.

      ![](assets/decision-rules-context-datastream-service.png)

Una volta salvato lo stream di dati, le informazioni del set di dati selezionato vengono recuperate automaticamente e integrate in Experience Decisioning, diventando in genere disponibili entro circa 24 ore.

Per ulteriori informazioni su come lavorare con Adobe Experience Platform, consulta le risorse seguenti:

* [Schemi Experience Data Model (XDM)](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/composition){target="_blank"}
* [Set di dati](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/overview){target="_blank"}
* [Flussi di dati](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/overview){target="_blank"}
