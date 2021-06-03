---
title: Delega sottodomini
description: Scopri come delegare i sottodomini
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
source-git-commit: 068ee9c8966e5968a488c12b2a48fa2ba2ab5245
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 11%

---


# Delega un sottodominio

Journey Optimizer ti consente di delegare completamente i sottodomini ad Adobe. In questo modo, Adobe sarà in grado di inviare messaggi come servizio gestito controllando e mantenendo tutti gli aspetti del DNS necessari per la consegna, il rendering e il tracciamento delle campagne e-mail.

>[!NOTE]
>
>Per impostazione predefinita, il contratto di licenza [!DNL Journey Optimizer] ti consente di delegare fino a 10 sottodomini. Contatta il tuo contatto Adobe se desideri aumentare questa limitazione.
>
>L’utilizzo di CNAME per la delega dei sottodomini non è attualmente supportato da Journey Optimizer.

Per delegare un nuovo sottodominio, effettua le seguenti operazioni:

1. Accedi al menu **[!UICONTROL Channels]** / **[!UICONTROL Subdomains]**, quindi fai clic su **[!UICONTROL Delegate subdomain]**.

   ![](../assets/subdomain-delegate.png)

1. Specifica il nome del sottodominio da delegare.

   ![](../assets/subdomain-name.png)

1. Viene visualizzato l’elenco dei record da inserire nei server DNS. Copia questi record, uno per uno, o scaricando un file CSV, quindi accedi alla soluzione di hosting del tuo dominio per generare i record DNS corrispondenti.

   Assicurati che tutti i record DNS siano stati generati nella tua soluzione di hosting del dominio. Se tutto è configurato correttamente, seleziona la casella &quot;Confermo..&quot;, quindi fai clic su **[!UICONTROL Submit]**.

   ![](../assets/subdomain-submit.png)

   >[!NOTE]
   >
   >Puoi creare i record e inviare la configurazione del sottodominio in un secondo momento utilizzando il pulsante **[!UICONTROL Save as draft]** . Potrai quindi riprendere la delega del sottodominio aprendola dall’elenco dei sottodomini.

1. Una volta inviata la delega del sottodominio, il sottodominio viene visualizzato nell’elenco con lo stato **[!UICONTROL Processing]** . Per ulteriori informazioni sugli stati dei sottodomini, consulta [questa sezione](access-subdomains.md).

   I controlli e le azioni seguenti vengono eseguiti fino a quando il sottodominio non viene verificato e possono essere utilizzati per inviare messaggi.

   Questo passaggio viene eseguito per Adobe e può richiedere fino a 3 ore.

   1. Controllare se il sottodominio è stato delegato ad Adobe DNS (record NS, record SOA, configurazione zona, record di proprietà),
   1. Configura il DNS per il dominio,
   1. Creare URL di tracciamento e mirror,
   1. Provisioning di CDN Cloud Front,
   1. Creare, convalidare e allegare il certificato SSL CDN,
   1. Crea DNS avanti,
   1. Crea record PTR.

   ![](../assets/subdomain-processing.png)

1. Una volta completati i controlli, il sottodominio ottiene lo stato **[!UICONTROL Success]** . È pronto per essere utilizzato per inviare messaggi.

   <!-- later on, users will be notified in Pulse -->

   ![](../assets/subdomain-notification.png)


