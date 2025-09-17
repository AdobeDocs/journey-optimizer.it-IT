---
title: Regole di decisione
description: Scopri come utilizzare le regole di decisione
feature: Decisioning
topic: Integrations
role: User
level: Intermediate
exl-id: 033a11b8-c848-4e4a-b6f0-62fa0a2152bf
source-git-commit: 58389860e5e0b07f32dd62b95a508e80579aaa73
workflow-type: tm+mt
source-wordcount: '549'
ht-degree: 25%

---

# Regole di decisione {#rules}

>[!CONTEXTUALHELP]
>id="ajo_exd_config_rules"
>title="Creare regole di decisione"
>abstract="Le regole di decisione consentono di definire il pubblico per gli elementi decisionali applicando vincoli, direttamente a livello dell’elemento decisionale o all’interno di una strategia di selezione specifica. Ciò consente di controllare con precisione quali elementi devono essere presentati a chi.<br/><br/>Seleziona **[!UICONTROL Crea regola con set di dati]** per utilizzare i dati di Adobe Experience Platform nelle regole di decisione. Questo ti consente di definire criteri di idoneità in base ad attributi esterni dinamici, in modo che vengano mostrati solo gli elementi decisionali pertinenti."

## Informazioni sulle regole di decisione {#about}

Le regole di decisione consentono di definire il pubblico per gli elementi decisionali applicando vincoli, direttamente a livello dell’elemento decisionale o all’interno di una strategia di selezione specifica. Ciò consente di controllare con precisione quali elementi devono essere presentati a chi.

Ad esempio, consideriamo uno scenario in cui si hanno elementi decisionali con prodotti relativi allo yoga progettati per le donne. Con le regole di decisione, puoi specificare che questi elementi devono essere visualizzati solo ai profili il cui genere è &quot;Femmina&quot; e che hanno indicato un &quot;Punto di interesse&quot; in &quot;Yoga&quot;.

>[!NOTE]
>
>Oltre alle regole di decisione a livello di articolo e di strategia di selezione, puoi anche definire il pubblico a cui rivolgerti a livello di campagna. [Ulteriori informazioni](../campaigns/create-campaign.md#audience)

L&#39;elenco delle regole di decisione è accessibile nel menu **[!UICONTROL Configurazione strategia]**.

![](assets/decision-rules-list.png)

## Creare una regola di decisione {#create}

Per creare una regola di decisione, effettua le seguenti operazioni:

1. Passa a **[!UICONTROL Configurazione strategia]** / **[!UICONTROL Regole di decisione]**, quindi fai clic sul pulsante **[!UICONTROL Crea regola]**.

   >[!NOTE]
   >
   >Puoi anche utilizzare i dati di Adobe Experience Platform per arricchire la logica decisionale con dati esterni. Questa funzione è particolarmente utile per gli attributi che cambiano frequentemente, ad esempio la disponibilità del prodotto o il prezzo in tempo reale. Questa funzionalità è disponibile per tutta la clientela come versione Beta pubblica. Se desideri accedervi, contatta il rappresentante del tuo account. [Scopri come utilizzare i dati di Adobe Experience Platform per prendere decisioni](../experience-decisioning/aep-data-exd.md)

1. Viene visualizzata la schermata di creazione delle regole di decisione. Denomina la regola e fornisci una descrizione.

1. Crea la regola di decisione in base alle tue esigenze utilizzando Adobe Experience Platform Segment Builder. A questo scopo, puoi sfruttare diverse origini dati, ad esempio:
   * Attributi del profilo e degli elementi decisionali,
   * Pubblico,
   * Dati contestuali provenienti da Adobe Experience Platform. [Scopri come sfruttare i dati contestuali](context-data.md)

   ![](assets/decision-rules-build.png)

   >[!NOTE]
   >
   >Il Generatore di segmenti fornito per creare regole di decisione presenta alcune specificità rispetto a quello utilizzato con il servizio di segmentazione di Adobe Experience Platform. Tuttavia, il processo globale descritto nella documentazione è ancora valido per creare regole di decisioni. [Scopri come creare le definizioni dei segmenti](../audience/creating-a-segment-definition.md)

1. Durante l&#39;aggiunta e la configurazione di nuovi campi nell&#39;area di lavoro, nel riquadro **[!UICONTROL Proprietà pubblico]** vengono visualizzate informazioni sui profili stimati appartenenti al pubblico. Fai clic su **[!UICONTROL Aggiorna stima]** per aggiornare i dati.

   >[!NOTE]
   >
   >Le stime del profilo non sono disponibili quando i parametri della regola includono dati non presenti nel profilo, come i dati contestuali.

1. Quando la regola di decisione è pronta, fai clic su **[!UICONTROL Salva]**. La regola creata viene visualizzata nell’elenco ed è disponibile per l’utilizzo in elementi di decisione e strategie di selezione per gestire la presentazione di elementi di decisione ai profili.

   >[!NOTE]
   >
   >La profondità di nidificazione in una regola di idoneità è limitata a 30 livelli. Questo viene misurato contando le `)` parentesi di chiusura nella stringa PQL. Una stringa di regola può avere dimensioni fino a 15 KB per caratteri con codifica UTF-8. Equivale a 15.000 caratteri ASCII (1 byte ciascuno) o 3.750-7.500 caratteri non ASCII (2-4 byte ciascuno). [Ulteriori informazioni su guardrail e limitazioni di Decisioning](gs-experience-decisioning.md#guardrails)
