---
solution: Journey Optimizer
product: journey optimizer
title: Creare la dimensione di targeting
description: Scopri come mappare uno schema relazionale al profilo cliente
exl-id: 2479c109-cd6f-407e-8a53-77e4477dc36f
version: Campaign Orchestration
source-git-commit: 9003668674302c576ed9738c803446c476877e47
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 1%

---


# Configurare una dimensione di targeting {#configuration}

Con **[!UICONTROL Campagne orchestrate]**, puoi progettare e distribuire comunicazioni mirate a livello di entità, sfruttando le funzionalità dello schema relazionale di Adobe Experience Platform. Experience Platform utilizza gli schemi per descrivere la struttura dei dati in modo coerente e riutilizzabile. Quando i dati vengono acquisiti in Experience Platform, sono strutturati in base a uno schema XDM.

Anche se la segmentazione per **[!UICONTROL Campagne orchestrate]** opera principalmente su schemi relazionali, la consegna effettiva dei messaggi avviene sempre al livello **Profilo**.

Durante la configurazione del targeting, puoi definire due aspetti chiave:

* **Schemi di destinazione**

  Puoi specificare quali schemi relazionali sono idonei per il targeting. Per impostazione predefinita, viene utilizzato lo schema denominato `Recipient`, ma è possibile configurare alternative quali `Visitors`, `Customers` e così via.

  >[!IMPORTANT]
  >
  > Lo schema di destinazione deve avere una relazione 1:1 con lo schema `Profile`. Ad esempio, non è possibile utilizzare `Purchases` come schema di destinazione, poiché in genere rappresenta una relazione uno-a-molti.

* **Collegamento profilo**

  Il sistema deve capire come lo schema di destinazione viene mappato allo schema `Profile`. Ciò si ottiene tramite un campo di identità condiviso, esistente sia nello schema di destinazione che nello schema `Profile`, configurato come spazio dei nomi dell&#39;identità.

➡️ [Ulteriori informazioni sugli schemi relazionali nella documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/it/docs/experience-platform/xdm/schema/relational#how-relational-schemas-differ-from-standard-xdm-schemas)

## Creare la dimensione di targeting {#targeting-dimension}

Per iniziare, imposta l’orchestrazione delle campagne mappando uno schema relazionale al profilo cliente.

1. Da **[!UICONTROL Amministrazione]**, accedere al menu **[!UICONTROL Configurazioni]** e selezionare **[!UICONTROL Dimension di destinazione di Campaign]**.

   ![](assets/target-dimension-1.png)

1. Fai clic su **[!UICONTROL Crea]** per iniziare a creare la **[!UICONTROL dimensione di targeting]**.

1. Scegli lo [schema configurato in precedenza](gs-schemas.md) &#x200B;dal menu a discesa.

   Mentre vengono visualizzati tutti gli schemi relazionali, solo quelli con una relazione di identità diretta con **Profilo** sono idonei per la selezione. Evita di scegliere schemi non people, ad esempio acquisti, e seleziona uno schema direttamente associato a un profilo.

1. Selezionare il **[!UICONTROL valore identità]** che rappresenta l&#39;entità di destinazione.

   In questo esempio, il profilo cliente è collegato a più sottoscrizioni, ognuna rappresentata da un `crmID` univoco nello schema `Recipient`. Impostando lo schema **[!UICONTROL e la relativa identità]** per `Recipient`Dimension`crmID` di destinazione, è possibile inviare messaggi a livello di sottoscrizione anziché al profilo cliente principale, garantendo che ogni contratto o linea riceva il proprio messaggio personalizzato.

   [Ulteriori informazioni sono disponibili nella documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/it/docs/experience-platform/xdm/schema/composition#identity)

   ![](assets/target-dimension-2.png)

1. Fai clic su **[!UICONTROL Salva]** per completare l&#39;installazione. Una volta creata, una **[!UICONTROL dimensione di destinazione]** non può essere rimossa o modificata.

Dopo aver configurato il **[!UICONTROL Dimension di destinazione]**, procedere con la creazione e la configurazione della **[!UICONTROL Configurazione canale]** e definire i **[!UICONTROL Dettagli esecuzione]** corrispondenti.