---
solution: Journey Optimizer
product: journey optimizer
title: Creare la dimensione di targeting
description: Scopri come mappare uno schema relazionale al profilo cliente
exl-id: 2479c109-cd6f-407e-8a53-77e4477dc36f
version: Campaign Orchestration
source-git-commit: aa075c1ca2feb3b6ef406089ab9fffd704fd95e2
workflow-type: tm+mt
source-wordcount: '742'
ht-degree: 0%

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

## Creare la dimensione di targeting {#targeting-dimension}

Per iniziare, imposta l’orchestrazione delle campagne mappando uno schema relazionale al profilo cliente.

1. Da **[!UICONTROL Amministrazione]**, accedere al menu **[!UICONTROL Configurazioni]** e selezionare **[!UICONTROL Dimension di destinazione di Campaign]**.

   ![](assets/target-dimension-1.png)

1. Fai clic su **[!UICONTROL Crea]** per iniziare a creare la **[!UICONTROL dimensione di targeting]**.

1. Scegli lo [schema configurato in precedenza](gs-schemas.md) &#x200B;dal menu a discesa.

   Anche se tutti gli schemi relazionali sono visibili, solo gli schemi con una relazione di identità diretta con il **Profilo** possono essere selezionati.

1. Selezionare il **[!UICONTROL valore identità]** che rappresenta l&#39;entità di destinazione.

   In questo esempio, il profilo cliente è collegato a più sottoscrizioni, ognuna rappresentata da un `crmID` univoco nello schema `Recipient`. Impostando lo schema **[!UICONTROL e la relativa identità]** per `Recipient`Dimension`crmID` di destinazione, è possibile inviare messaggi a livello di sottoscrizione anziché al profilo cliente principale, garantendo che ogni contratto o linea riceva il proprio messaggio personalizzato.

   [Ulteriori informazioni sono disponibili nella documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/it/docs/experience-platform/xdm/schema/composition#identity)

   ![](assets/target-dimension-2.png)

1. Fai clic su **[!UICONTROL Salva]** per completare l&#39;installazione. Una volta creata, una **[!UICONTROL dimensione di destinazione]** non può essere rimossa o modificata.

Dopo aver configurato il **[!UICONTROL Dimension di destinazione]**, procedere con la creazione e la configurazione della **[!UICONTROL Configurazione canale]** e definire i **[!UICONTROL Dettagli esecuzione]** corrispondenti.

## Configurazione del canale {#channel-configuration}

Dopo aver configurato il **[!UICONTROL Dimension di destinazione]**, è necessario configurare la **[!UICONTROL configurazione canale]** e definire i **[!UICONTROL dettagli di esecuzione]** appropriati. Questo consente di definire:

* **Livello di recapito dei messaggi**: ad esempio, l&#39;invio di un messaggio per destinatario, ad esempio una singola e-mail per singolo destinatario.

* **Indirizzo di esecuzione**: il campo del contatto specifico da utilizzare per l&#39;invio, ad esempio un indirizzo e-mail o un numero di telefono.

Per configurare la configurazione del canale:

1. Per iniziare, crea e configura la **[!UICONTROL configurazione canale]**.

   È inoltre possibile aggiornare una **[!UICONTROL configurazione canale]** esistente.

   ➡️ [Segui i passaggi descritti in questa pagina](../email/surface-personalization.md)

1. Dalla sezione **[!UICONTROL Dettagli esecuzione]** della **[!UICONTROL Configurazione canale]**, accedi alla scheda **[!UICONTROL Campagne orchestrate]**.

   ![](assets/target-dimension-3.png)

1. Fai clic su **[!UICONTROL Abilitato]** per renderlo compatibile con le campagne orchestrate.

1. Scegli il metodo di consegna:

   * **[!UICONTROL Dimension di destinazione]**: invia all&#39;entità principale, ad esempio destinatario.

   * **[!UICONTROL Destinazione + Dimension secondario]**: inviare utilizzando entità primarie e secondarie, ad esempio destinatario + contratto.

1. Seleziona dall&#39;elenco a discesa [Dimension di Target creato in precedenza](#targeting-dimension).

   ![](assets/target-dimension-4.png)

1. Se hai selezionato **[!UICONTROL Target + Dimension]** secondario come metodo di consegna, scegli un **[!UICONTROL Dimension secondario]** per definire il contesto per la consegna dei messaggi.

1. Nella sezione **[!UICONTROL Indirizzo di esecuzione]**, scegli quale **[!UICONTROL Source]** deve essere utilizzato per recuperare l&#39;indirizzo di consegna, ad esempio l&#39;indirizzo e-mail o il numero di telefono:

   * **[!UICONTROL Profilo]**: selezionare questa opzione se l&#39;indirizzo di consegna, ad esempio e-mail, è memorizzato direttamente nel profilo cliente principale.

     Utile quando si inviano messaggi al cliente principale, non a una specifica entità associata.

   * **[!UICONTROL Dimension di destinazione]**: scegliere questa opzione se l&#39;indirizzo di consegna è archiviato nell&#39;entità principale, ad esempio un destinatario.

     Utile quando ogni destinatario ha il proprio indirizzo di consegna, ad esempio un indirizzo e-mail o un numero di telefono diverso.

   * **[!UICONTROL Dimension secondario]**: quando si utilizza **[!UICONTROL Target + Dimension secondario]** come metodo di consegna, selezionare il **[!UICONTROL Dimension secondario]** pertinente configurato in precedenza.

     Ad esempio, se la dimensione secondaria rappresenta una prenotazione o un abbonamento, l’indirizzo di esecuzione, ad esempio un’e-mail, può essere preso da tale livello. Ciò è utile nei casi in cui i profili utilizzano un recapito diverso al momento della prenotazione o dell’abbonamento a un servizio.

1. Dal campo **[!UICONTROL Indirizzo di consegna]**, fai clic su ![icona di modifica](assets/do-not-localize/edit.svg) per scegliere il campo specifico da utilizzare per la consegna del messaggio.

   ![](assets/target-dimension-4.png)

1. Una volta configurata, fai clic su **[!UICONTROL Invia]**.

Il tuo canale è ora pronto per essere utilizzato con **Campagne orchestrate** e i messaggi verranno recapitati in base alla dimensione di destinazione selezionata.
