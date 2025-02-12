---
solution: Journey Optimizer
product: journey optimizer
title: Configurare i sottodomini web
description: Scopri come impostare i sottodomini web con Journey Optimizer
role: Admin
feature: Web Channel, Subdomains
level: Experienced
keywords: web, sottodomini, configurazione
exl-id: 6e00466d-4ce5-4d80-89ff-c7331a5ab158
source-git-commit: ccfc0870a8d59d16c7f5b6b02856785aa28dd307
workflow-type: tm+mt
source-wordcount: '894'
ht-degree: 24%

---

# Configurare i sottodomini web {#web-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_web_header"
>title="Delegare un sottodominio web"
>abstract="Devi configurare il sottodominio da utilizzare per il canale web. Puoi utilizzare un sottodominio già delegato ad Adobe o configurarne un altro."

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_web"
>title="Delegare un sottodominio web"
>abstract="Se aggiungi contenuti provenienti da Adobe Experience Manager Assets alle esperienze web, devi configurare il sottodominio che verrà utilizzato per pubblicare tali contenuti. Seleziona tra i sottodomini già delegati ad Adobe o configura un nuovo sottodominio."

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_web_default"
>title="Impostare un sottodominio web"
>abstract="Seleziona un sottodominio dall’elenco dei sottodomini delegati ad Adobe. È possibile impostare questo sottodominio web come predefinito, ma è possibile utilizzare un solo sottodominio predefinito alla volta."

Durante l&#39;authoring delle esperienze Web, se si aggiungono contenuti provenienti dalla libreria [Adobe Experience Manager Assets](../integrations/assets.md), è necessario impostare il sottodominio che verrà utilizzato per pubblicare tali contenuti.

Puoi utilizzare un sottodominio già delegato ad Adobe oppure configurare un altro sottodominio. Ulteriori informazioni sulla delega dei sottodomini ad Adobe sono disponibili in [questa sezione](../configuration/delegate-subdomain.md).

>[!CAUTION]
>
>La configurazione del sottodominio web è comune a tutti gli ambienti. Pertanto:
>
>* Per accedere e modificare i sottodomini Web, devi disporre dell&#39;autorizzazione **[!UICONTROL Gestisci sottodomini Web]** nella sandbox di produzione.
>
> * Qualsiasi modifica a un sottodominio web influirà anche sulle sandbox di produzione.

Puoi creare diversi sottodomini web, ma verrà utilizzato solo il sottodominio **default**. Puoi modificare il sottodominio web predefinito, ma è possibile utilizzarne solo uno alla volta.

## Accesso e gestione dei sottodomini web {#access-web-subdomains}

1. Vai al menu **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]**, quindi seleziona **[!UICONTROL Impostazioni Web]** > **[!UICONTROL Sottodomini Web]**. Vengono visualizzati tutti i sottodomini configurati con la sandbox corrente.

   ![](assets/web-access-subdomains.png)

1. Puoi filtrare in base all&#39;utente che ha delegato ogni sottodominio o uno dei due stati di delega (**[!UICONTROL Bozza]**, **[!UICONTROL Elaborazione]**, **[!UICONTROL Operazione completata]** o **[!UICONTROL Non riuscita]**).

   ![](assets/web-filter-subdomains.png)

1. Il badge **[!UICONTROL Default]** viene visualizzato accanto al sottodominio attualmente utilizzato come predefinito. Per modificare il sottodominio predefinito, seleziona **[!UICONTROL Imposta come predefinito]** dal pulsante **[!UICONTROL Altre azioni]** accanto al sottodominio desiderato.

   ![](assets/web-subdomain-default.png)

   >[!NOTE]
   >
   >Puoi modificare il sottodominio web predefinito, ma è possibile utilizzarne solo uno alla volta.

## Usa un sottodominio esistente {#web-use-existing-subdomain}

Per utilizzare un sottodominio già delegato ad Adobe, segui i passaggi seguenti.

1. Accedi al menu **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]**, quindi seleziona **[!UICONTROL Impostazioni Web]** > **[!UICONTROL Sottodomini Web]**.

1. Fare clic su **[!UICONTROL Configura sottodominio]**.

1. Seleziona l&#39;opzione **[!UICONTROL Usa sottodominio delegato]** dalla sezione **[!UICONTROL Tipo di configurazione]** e scegli un sottodominio delegato dall&#39;elenco.

   ![](assets/web-subdomain-details.png)

   >[!NOTE]
   >
   >Non puoi selezionare un sottodominio già utilizzato come sottodominio web.

1. Il prefisso che verrà visualizzato nell’URL web viene aggiunto automaticamente. Non puoi cambiarlo.

1. Per impostare questo sottodominio come predefinito, seleziona l’opzione corrispondente.

   ![](assets/web-subdomain-details-default.png)

   >[!NOTE]
   >
   >Verrà utilizzato solo il sottodominio **default**.

1. Fai clic su **[!UICONTROL Invia]**. Il sottodominio ottiene lo stato **[!UICONTROL Operazione riuscita]**. È pronto per essere utilizzato nelle esperienze web.

   >[!NOTE]
   >
   >In casi molto rari, l’impostazione di un sottodominio potrebbe non riuscire. In questo caso, puoi eliminare il sottodominio **[!UICONTROL Non riuscito]** per pulire l&#39;elenco utilizzando il pulsante **[!UICONTROL Elimina]** dall&#39;icona **[!UICONTROL Altre azioni]**.

## Configurare un nuovo sottodominio {#web-configure-new-subdomain}

>[!CONTEXTUALHELP]
>id="ajo_admin_web_subdomain_dns"
>title="Generare il record DNS corrispondente"
>abstract="Per configurare un nuovo sottodominio web, devi copiare le informazioni del server dei nomi di Adobe visualizzate nell’interfaccia di Journey Optimizer e incollarle nella soluzione di hosting del dominio per generare il record DNS corrispondente. Una volta completati i controlli, il sottodominio è pronto per essere utilizzato per pubblicare il contenuto proveniente dalla libreria Adobe Experience Manager Assets."

Per configurare un nuovo sottodominio, segui i passaggi indicati di seguito.

>[!NOTE]
>
>Per impostazione predefinita, [!DNL Journey Optimizer] ti consente di delegare fino a 10 sottodomini in totale (che coprono sia i canali e-mail che web). Tuttavia, a seconda del contratto di licenza, puoi delegare fino a 100 sottodomini. Per ulteriori informazioni sul numero di sottodomini a cui hai diritto, rivolgiti al tuo referente Adobe.

1. Accedi al menu **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]**, quindi seleziona **[!UICONTROL Impostazioni Web]** > **[!UICONTROL Sottodomini Web]**.

1. Fare clic su **[!UICONTROL Configura sottodominio]**.

1. Seleziona **[!UICONTROL Aggiungi il tuo dominio]** dalla sezione **[!UICONTROL Tipo di configurazione]**.

1. Specifica il sottodominio da delegare.

   >[!CAUTION]
   >
   >Non puoi utilizzare un sottodominio web esistente.
   >
   >Nei sottodomini non sono consentite lettere maiuscole.

   ![](assets/web-add-your-own-domain.png)

   Non è consentito delegare un sottodominio non valido ad Adobe. Assicurati di immettere un sottodominio valido di proprietà della tua organizzazione, ad esempio marketing.yourcompany.com.

   >[!NOTE]
   >
   >Sono supportati i sottodomini a più livelli (dello stesso dominio padre). Ad esempio, puoi utilizzare &quot;web.marketing.yourcompany.com&quot;.

1. Per impostare questo sottodominio come predefinito, seleziona l’opzione corrispondente.

   >[!NOTE]
   >
   >Verrà utilizzato solo il sottodominio **default**.

1. Viene visualizzato il record da inserire nei server DNS. Copia questo record o scarica un file CSV, quindi accedi alla soluzione di hosting del tuo dominio per generare il record DNS corrispondente.

1. Assicurati che il record DNS sia stato generato nella soluzione di hosting del dominio. Se tutto è configurato correttamente, seleziona la casella &quot;Confermo...&quot;, quindi fai clic su **[!UICONTROL Invia]**.

   ![](assets/web-add-your-own-domain-confirm.png)

   >[!NOTE]
   >
   >Quando configuri un nuovo sottodominio web, questo punterà sempre a un record CNAME.

1. Una volta inviata la delega del sottodominio, il sottodominio viene visualizzato nell&#39;elenco con lo stato **[!UICONTROL Elaborazione]**. Per ulteriori informazioni sugli stati dei sottodomini, consulta [questa sezione](../configuration/about-subdomain-delegation.md#access-delegated-subdomains).<!--Same statuses?-->

   >[!NOTE]
   >
   >Prima di poter utilizzare tale sottodominio per inviare messaggi web, devi attendere che Adobe esegua i controlli richiesti, che possono richiedere fino a 4 ore.

1. Una volta completati i controlli, il sottodominio ottiene lo stato **[!UICONTROL Completato]**. È pronto per essere utilizzato per creare configurazioni del canale web.

   Se non riesci a creare il record di convalida nella soluzione di hosting, il sottodominio verrà contrassegnato come **[!UICONTROL Non riuscito]**.

<!--
Only a subdomain with the **[!UICONTROL Success]** status can be set as default.
You cannot delete a subdomain with the **[!UICONTROL Processing]** status.
-->
