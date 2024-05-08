---
title: Regole di decisione
description: Scopri come utilizzare le regole di decisione
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
badge: label="Disponibilità limitata"
exl-id: 033a11b8-c848-4e4a-b6f0-62fa0a2152bf
source-git-commit: 5ce388e5d86950e5cc6b173aab48225825f1c648
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 24%

---

# Regole di decisione {#rules}

>[!CONTEXTUALHELP]
>id="ajo_exd_config_rules"
>title="Creare regole di decisione"
>abstract="Le regole di decisione consentono di definire il pubblico per gli elementi decisionali applicando vincoli, direttamente a livello dell’elemento decisionale o all’interno di una strategia di selezione specifica. Ciò consente di controllare con precisione quali elementi devono essere presentati a chi."

## Informazioni sulle regole di decisione {#about}

Le regole di decisione consentono di definire il pubblico per gli elementi decisionali applicando vincoli, direttamente a livello dell’elemento decisionale o all’interno di una strategia di selezione specifica. Ciò consente di controllare con precisione quali elementi devono essere presentati a chi.

Ad esempio, consideriamo uno scenario in cui si hanno elementi decisionali con prodotti relativi allo yoga progettati per le donne. Con le regole di decisione, puoi specificare che questi elementi devono essere visualizzati solo ai profili il cui genere è &quot;Femmina&quot; e che hanno indicato un &quot;Punto di interesse&quot; in &quot;Yoga&quot;.

>[!NOTE]
>
>Oltre alle regole di decisione a livello di articolo e di strategia di selezione, puoi anche definire il pubblico a cui rivolgerti a livello di campagna. [Ulteriori informazioni](../campaigns/create-campaign.md#audience)

L’elenco delle regole di decisione è accessibile nella sezione **[!UICONTROL Impostazione strategia]** menu.

![](assets/decision-rules-list.png)

## Creare una regola di decisione {#create}

Per creare una regola di decisione, effettua le seguenti operazioni:

1. Accedi a **[!UICONTROL Impostazione strategia]** / **[!UICONTROL Regole di decisione]** quindi fai clic su **[!UICONTROL Crea regola]** pulsante.

1. Viene visualizzata la schermata di creazione delle regole di decisione. Denomina la regola e fornisci una descrizione.

1. Crea la regola di decisione in base alle tue esigenze utilizzando Adobe Experience Platform Segment Builder. A tal fine, puoi sfruttare diverse origini dati, come attributi di profilo, tipi di pubblico o dati contestuali provenienti da Adobe Experience Platform. [Scopri come sfruttare i dati contestuali](#context-data)

   ![](assets/decision-rules-build.png)

   >[!NOTE]
   >
   >Il Generatore di segmenti fornito per creare regole di decisione presenta alcune specificità rispetto a quello utilizzato con il servizio di segmentazione di Adobe Experience Platform.  Tuttavia, il processo globale descritto nella documentazione è ancora valido per creare regole di decisioni. [Scopri come creare le definizioni dei segmenti](../audience/creating-a-segment-definition.md)

1. Durante l’aggiunta e la configurazione di nuovi campi nell’area di lavoro, il **[!UICONTROL Proprietà del pubblico]** Questo riquadro mostra informazioni sui profili stimati appartenenti al pubblico. Clic **[!UICONTROL Aggiorna stima]** per aggiornare i dati.

   >[!NOTE]
   >
   >Le stime del profilo non sono disponibili quando i parametri della regola includono dati non presenti nel profilo, come i dati contestuali.

1. Quando la regola di decisione è pronta, fai clic su **[!UICONTROL Salva]**. La regola creata viene visualizzata nell’elenco ed è disponibile per l’utilizzo in elementi di decisione e strategie di selezione per gestire la presentazione di elementi di decisione ai profili.

