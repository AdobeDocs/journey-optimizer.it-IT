---
title: Creare regole di decisione
description: Scopri come creare regole decisionali per definire a chi visualizzare le offerte
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 401ce05b-412b-4fa0-a516-bf75727f6387
source-git-commit: 1213a65c8a22a326e8294c51db53efb6e23fd6f9
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 13%

---

# Creare regole di decisione {#create-decision-rules}

Puoi creare regole decisionali per le offerte in base ai dati disponibili in Adobe Experience Platform. Le regole decisionali determinano a chi visualizzare un’offerta.

Ad esempio, puoi specificare che desideri che venga visualizzata solo “Offerta di abbigliamento invernale per le donne” quando (Genere = ‘Femmina’) e (Area geografica = ‘Nord Est’). 

➡️ [Scopri questa funzione nel video](#video)

L&#39;elenco delle regole decisionali create è accessibile nella **[!UICONTROL Componenti]** menu.

![](../assets/decision_rules_list.png)

Per creare una regola decisionale, effettua le seguenti operazioni:

1. Vai a **[!UICONTROL Regole]** scheda , quindi fai clic su **[!UICONTROL Crea regola]**.

   ![](../assets/offers_decision_rule_creation.png)

1. Denomina la regola e fornisci una descrizione, quindi configura la regola in base alle tue esigenze.

   Per eseguire questa operazione, **Generatore di segmenti** è disponibile per creare le condizioni della regola. [Ulteriori informazioni](../../segment/about-segments.md)

   <!--In this example, the rule will target customers that have the "Gold" loyalty level.-->

   ![](../assets/offers_decision_rule_creation_segment.png)

   >[!NOTE]
   >
   >Il Generatore di segmenti fornito per creare regole decisionali presenta alcune specificità rispetto a quella utilizzata con il **[!UICONTROL Segmentazione]** servizio. Ad esempio, il **[!UICONTROL Segmenti]** scheda non disponibile per l’uso. Tuttavia, il processo globale descritto nel [Generatore di segmenti](../../segment/about-segments.md) la documentazione è ancora valida per generare le regole decisionali delle offerte. Ulteriori informazioni nel [Documentazione del servizio di segmentazione Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=it).

1. Durante l’aggiunta e la configurazione di nuovi campi nell’area di lavoro, la **[!UICONTROL Proprietà del segmento]** visualizza informazioni sui profili stimati appartenenti al segmento. Fai clic su **[!UICONTROL Aggiorna stima]** per aggiornare i dati.

   ![](../assets/offers_decision_rule_creation_estimate.png)

   >[!NOTE]
   >
   >Le stime del profilo non sono disponibili quando i parametri delle regole includono dati non presenti nel profilo, ad esempio dati contestuali. Ad esempio, una regola di idoneità che richiede che il tempo corrente sia ≥ 80 gradi.

1. Fai clic su **[!UICONTROL Salva]** per confermare.

1. Una volta creata la regola, questa viene visualizzata nella **[!UICONTROL Regole]** elenco. È possibile selezionarlo per visualizzarne le proprietà e modificarlo o eliminarlo.

   ![](../assets/rule_created.png)

>[!CAUTION]
>
>Le offerte basate su eventi non sono attualmente supportate in [!DNL Journey Optimizer]. Se crei una regola decisionale basata su un [event](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=en#events){target="_blank"}, non potrai sfruttarlo in un’offerta.

## Video tutorial {#video}

>[!VIDEO](https://video.tv.adobe.com/v/329373?quality=12)
