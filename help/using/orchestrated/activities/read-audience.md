---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare l’attività Leggi pubblico
description: Scopri come utilizzare l’attività Read audience in una campagna orchestrata
exl-id: ef8eba57-cd33-4746-8eb4-5214ef9cbe2f
source-git-commit: 3a44111345c1627610a6b026d7b19b281c4538d3
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 6%

---


# Leggi pubblico {#read-audience}


>[!CONTEXTUALHELP]
>id="ajo_orchestration_read_audience"
>title="Attività Crea pubblico"
>abstract="L&#39;attività **Read audience** ti consente di selezionare il pubblico che entrerà nella campagna orchestrata. Questo pubblico può essere un pubblico esistente di Adobe Experience Platform o uno estratto da un file CSV. Quando si inviano messaggi nel contesto di una campagna orchestrata, il pubblico del messaggio non è definito nell&#39;attività del canale, ma in un&#39;attività **Read audience** o **Build audience**."

L&#39;attività **[!UICONTROL Read audience]** consente di recuperare un pubblico esistente, salvato o importato in precedenza, e di riutilizzarlo all&#39;interno di una campagna orchestrata. Questa attività è particolarmente utile per il targeting di un set predefinito di profili senza la necessità di eseguire un nuovo processo di segmentazione.

Una volta caricato il pubblico, puoi facoltativamente perfezionarlo selezionando un campo di identità univoco e arricchendo il pubblico con attributi di profilo aggiuntivi a scopo di targeting, personalizzazione o reporting.

## Configurare l’attività Read audience {#read-audience-configuration}

Segui questi passaggi per configurare l&#39;attività **[!UICONTROL Read audience]**:

1. Prima di aggiungere l&#39;attività **[!UICONTROL Read audience]**, assicurati di selezionare un **[!UICONTROL criterio di unione]** nelle impostazioni di Campaign.

   ![](../assets/read-audience-6.png)

1. Aggiungi un&#39;attività **[!UICONTROL Read audience]** alla tua campagna orchestrata.

   ![](../assets/read-audience-1.png)

1. Immetti un&#39;etichetta **[!UICONTROL Label]** per l&#39;attività. Questa etichetta fungerà da nome del pubblico.

1. Fai clic su ![icona di ricerca cartella](../assets/do-not-localize/folder-search.svg) per selezionare il pubblico di destinazione della campagna orchestrata.

   ![](../assets/read-audience-2.png)

1. Scegli un&#39;entità **[!UICONTROL &#x200B;]** dalla dimensione di targeting della campagna. Questa impostazione definisce l’entità target e l’attributo utilizzati per riconciliare il pubblico con la dimensione target.

   ➡️ [Segui i passaggi descritti in questa pagina per creare la tua dimensione di targeting delle campagne](../target-dimension.md)

   ![](../assets/read-audience-3.png)

1. Seleziona [!UICONTROL Aggiungi attributo] per arricchire il pubblico selezionato con dati aggiuntivi. Questo passaggio ti consente di aggiungere attributi di profilo al pubblico, creando un elenco di destinatari migliorati con tali attributi.

1. Scegli gli **[!UICONTROL Attributi]** da aggiungere al pubblico. Il selettore di attributi visualizza i campi dello **schema profilo di unione**:

   * Per i tipi di pubblico basati su CSV, sono inclusi sia gli attributi **Profilo** che gli attributi personalizzati a livello di pubblico. Questi attributi si trovano nel seguente percorso dello schema:

     `<audienceid> > _ajobatchjourneystage > audienceEnrichment > CustomerAudienceUpload > <audienceid>`

   * Per i tipi di pubblico standard di AEP, sono disponibili solo gli attributi **Profilo**, in quanto non contengono campi incorporati specifici per il pubblico.

   >[!NOTE]
   >
   > Anche se alcuni attributi possono essere visualizzati nel selettore, la loro disponibilità in fase di esecuzione dipende dal fatto che i dati del pubblico siano stati correttamente riconciliati e uniti con il **profilo Adobe Experience Platform**.

   ![](../assets/read-audience-4.png)

Una volta creato, il pubblico è disponibile in sola lettura e non può più essere modificato. Può essere utilizzato solo dopo che il processo di creazione è stato completato.

## Esempio

Nell&#39;esempio seguente, l&#39;attività **[!UICONTROL Read audience]** viene utilizzata per recuperare un pubblico creato e salvato in precedenza dai profili abbonati alla newsletter. Il pubblico viene quindi arricchito con l&#39;attributo **Iscrizione fedeltà** per abilitare il targeting degli utenti che sono membri registrati del programma fedeltà.

![](../assets/read-audience-5.png)
