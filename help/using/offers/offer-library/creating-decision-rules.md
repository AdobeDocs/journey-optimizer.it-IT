---
title: Creare regole di decisione
description: Scopri come creare regole di decisione per definire a chi visualizzare le offerte
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
exl-id: 401ce05b-412b-4fa0-a516-bf75727f6387
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 12%

---

# Creare regole di decisione {#create-decision-rules}

## Informazioni sulle regole di decisione {#about}

Puoi creare regole di decisione delle offerte basate sui dati disponibili in Adobe Experience Platform. Le regole di decisione determinano a chi può essere visualizzata un’offerta.

Ad esempio, puoi specificare che desideri che venga visualizzata solo “Offerta di abbigliamento invernale per le donne” quando (Genere = ‘Femmina’) e (Area geografica = ‘Nord Est’). 

➡️ [Scopri questa funzione nel video](#video)

Di seguito è riportato un elenco di limitazioni di cui tenere conto quando si lavora con le regole di decisione:

* Durante la creazione di una regola, puoi utilizzare eventi storici, ma esistono limitazioni su quando queste regole sono utilizzabili.
* Edge Decisioning utilizza il profilo Edge che non memorizza gli eventi, pertanto qualsiasi regola utilizzata in una decisione Edge non sarà valida.
* I percorsi che utilizzano le decisioni sulle offerte non esamineranno gli eventi storici, pertanto queste regole non saranno valide.
* Le richieste di decisione che utilizzano il profilo hub esamineranno gli ultimi 100 eventi di esperienza sul profilo per valutare le regole che fanno riferimento a eventi di esperienza storici.

## Creare una regola di decisione {#create}

L’elenco delle regole di decisione create è accessibile nel **[!UICONTROL Componenti]** menu.

![](../assets/decision_rules_list.png)

Per creare una regola di decisione, effettua le seguenti operazioni:

1. Vai a **[!UICONTROL Regole]** , quindi fai clic su **[!UICONTROL Crea regola]**.

   ![](../assets/offers_decision_rule_creation.png)

1. Denomina la regola e fornisci una descrizione, quindi configura la regola in base alle tue esigenze.

   A tale scopo, il Adobe Experience Platform **Generatore di segmenti** è disponibile per aiutarti a creare le condizioni della regola. [Scopri come creare le definizioni dei segmenti](../../audience/creating-a-segment-definition.md)

   <!--In this example, the rule will target customers that have the "Gold" loyalty level.-->

   ![](../assets/offers_decision_rule_creation_segment.png)

   >[!NOTE]
   >
   >Il Generatore di segmenti fornito per creare regole di decisione presenta alcune specificità rispetto a quello utilizzato con **[!UICONTROL Segmentazione]** servizio. Tuttavia, il processo globale descritto nel [Generatore di segmenti](../../audience/creating-a-segment-definition.md) La documentazione di è ancora valida per creare le regole di decisioni per le offerte. Ulteriori informazioni nella [documentazione del servizio di segmentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/segment-builder.html?lang=it).

1. Durante l’aggiunta e la configurazione di nuovi campi nell’area di lavoro, il **[!UICONTROL Proprietà del pubblico]** Questo riquadro mostra informazioni sui profili stimati appartenenti al pubblico. Clic **[!UICONTROL Aggiorna stima]** per aggiornare i dati.

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
