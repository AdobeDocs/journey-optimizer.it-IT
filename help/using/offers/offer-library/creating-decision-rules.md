---
title: Creare regole di decisione
description: Scopri come creare regole di decisione per definire a chi visualizzare le offerte
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 401ce05b-412b-4fa0-a516-bf75727f6387
source-git-commit: 59499dec7d15dd4565c7910d7b454d82243ff011
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 13%

---

# Creare regole di decisione {#create-decision-rules}

Puoi creare regole di decisione delle offerte basate sui dati disponibili in Adobe Experience Platform. Le regole di decisione determinano a chi può essere visualizzata un’offerta.

Ad esempio, puoi specificare che desideri che venga visualizzata solo “Offerta di abbigliamento invernale per le donne” quando (Genere = ‘Femmina’) e (Area geografica = ‘Nord Est’). 

➡️ [Scopri questa funzione nel video](#video)

L’elenco delle regole di decisione create è accessibile nel **[!UICONTROL Componenti]** menu.

![](../assets/decision_rules_list.png)

Per creare una regola di decisione, effettua le seguenti operazioni:

1. Vai a **[!UICONTROL Regole]** , quindi fai clic su **[!UICONTROL Crea regola]**.

   ![](../assets/offers_decision_rule_creation.png)

1. Denomina la regola e fornisci una descrizione, quindi configura la regola in base alle tue esigenze.

   Per eseguire questa operazione, il **Generatore di segmenti** è disponibile per aiutarti a creare le condizioni della regola. [Ulteriori informazioni](../../segment/about-segments.md)

   <!--In this example, the rule will target customers that have the "Gold" loyalty level.-->

   ![](../assets/offers_decision_rule_creation_segment.png)

   >[!NOTE]
   >
   >Il Generatore di segmenti fornito per creare regole di decisione presenta alcune specificità rispetto a quello utilizzato con **[!UICONTROL Segmentazione]** servizio. Ad esempio, il **[!UICONTROL Segmenti]** non è disponibile. Tuttavia, il processo globale descritto nel [Generatore di segmenti](../../segment/about-segments.md) La documentazione di è ancora valida per creare le regole di decisioni per le offerte. Per ulteriori informazioni, consulta [Documentazione del servizio di segmentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=it).

1. Durante l’aggiunta e la configurazione di nuovi campi nell’area di lavoro, il **[!UICONTROL Proprietà segmento]** visualizza informazioni sui profili stimati appartenenti al segmento. Clic **[!UICONTROL Aggiorna stima]** per aggiornare i dati.

   ![](../assets/offers_decision_rule_creation_estimate.png)

   >[!NOTE]
   >
   >Le stime del profilo non sono disponibili quando i parametri della regola includono dati non presenti nel profilo, come i dati contestuali. Ad esempio, una regola di idoneità che richiede che il tempo corrente sia di ≥80 gradi.

1. Clic **[!UICONTROL Salva]** per confermare.

1. Una volta creata, la regola viene visualizzata nella **[!UICONTROL Regole]** elenco. Puoi selezionarlo per visualizzarne le proprietà e modificarlo o eliminarlo.

   ![](../assets/rule_created.png)

>[!CAUTION]
>
>Le offerte basate su eventi non sono attualmente supportate in [!DNL Journey Optimizer]. Se crei una regola di decisione basata su un [evento](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html#events){target="_blank"}, non potrai sfruttarlo in un’offerta.

## Video tutorial {#video}

>[!VIDEO](https://video.tv.adobe.com/v/329373?quality=12)
