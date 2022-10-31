---
solution: Journey Optimizer
product: journey optimizer
title: Configurare i sottodomini della pagina di destinazione
description: Scopri come configurare i sottodomini della pagina di destinazione con Journey Optimizer
role: Admin
level: Intermediate
exl-id: dd1af8dc-3920-46cb-ae4d-a8f4d4c26e89
source-git-commit: 3a932747de33ced59d68835a96386b7ac560e4fe
workflow-type: tm+mt
source-wordcount: '810'
ht-degree: 1%

---

# Configurare i sottodomini della pagina di destinazione {#lp-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_lp_header"
>title="Delega di un sottodominio della pagina di destinazione"
>abstract="Imposta il sottodominio per un utilizzo della pagina di destinazione. Puoi utilizzare un sottodominio già delegato ad Adobe o configurare un altro sottodominio."

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_lp"
>title="Delega di un sottodominio della pagina di destinazione"
>abstract="Devi configurare un sottodominio da utilizzare per le pagine di destinazione, in quanto dovrai usare questo sottodominio per creare un predefinito per la pagina di destinazione. Puoi utilizzare un sottodominio già delegato ad Adobe o configurare un nuovo sottodominio."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/lp-configuration/lp-presets.html" text="Creare predefiniti per pagine di destinazione"

>[!CONTEXTUALHELP]
>id="ajo_admin_config_lp_subdomain"
>title="Creare un predefinito per pagina di destinazione"
>abstract="Per creare un predefinito per pagina di destinazione, accertati di aver configurato in precedenza almeno un sottodominio della pagina di destinazione da selezionare dall’elenco dei nomi del sottodominio."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/lp-configuration/lp-presets.html" text="Creare predefiniti per pagine di destinazione"

Essere in grado di [creare predefiniti pagina di destinazione](lp-presets.md), devi impostare i sottodomini che userai per le pagine di destinazione.

Puoi utilizzare un sottodominio già delegato ad Adobe oppure configurare un altro sottodominio. Ulteriori informazioni sulla delega dei sottodomini ad Adobe in [questa sezione](delegate-subdomain.md).

>[!CAUTION]
>
>La configurazione del sottodominio della pagina di destinazione è comune a tutti gli ambienti. Pertanto, qualsiasi modifica apportata a un sottodominio di una pagina di destinazione avrà un impatto anche sulle sandbox di produzione.

Le lettere maiuscole non devono essere consentite in un sottodominio

## Utilizzare un sottodominio esistente {#lp-use-existing-subdomain}

Per utilizzare un sottodominio già delegato ad Adobe, segui i passaggi seguenti.

1. Accedere al **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]** quindi seleziona **[!UICONTROL Configurazione e-mail]** > **[!UICONTROL Sottodomini della pagina di destinazione]**.

   ![](assets/lp_access-subdomains.png)

1. Fai clic su **[!UICONTROL Imposta sottodominio]**.

   ![](assets/lp_set-up-subdomain.png)

1. Seleziona **[!UICONTROL Usa dominio delegato]** dal **[!UICONTROL Tipo di configurazione]** sezione .

   ![](assets/lp_use-delegated-subdomain.png)

1. Immetti il prefisso che verrà visualizzato nell’URL della pagina di destinazione.

   >[!NOTE]
   >
   >Sono consentiti solo caratteri alfanumerici e trattini.

1. Seleziona un sottodominio delegato dall’elenco.

   >[!NOTE]
   >
   >Non puoi selezionare un sottodominio già utilizzato come sottodominio della pagina di destinazione.

   <!--Capital letters are not allowed in subdomains. TBC by PM-->

   ![](assets/lp_prefix-and-subdomain.png)

   Non è possibile utilizzare più sottodomini delegati dello stesso dominio padre. Ad esempio, se &#39;marketing1.yourcompany.com&#39; è già delegato ad Adobe per le pagine di destinazione, non potrai utilizzare &#39;marketing2.yourcompany.com&#39;. Tuttavia, i sottodomini di più livelli supportati per le pagine di destinazione, puoi procedere utilizzando un sottodominio di &quot;marketing1.yourcompany.com&quot; (ad esempio &quot;email.marketing1.yourcompany.com&quot;) o un dominio padre diverso.

   >[!CAUTION]
   >
   >Se selezioni un dominio delegato ad Adobe utilizzando [metodo CNAME](delegate-subdomain.md#cname-subdomain-delegation), devi creare il record DNS sulla piattaforma di hosting. Per generare il record DNS, il processo è lo stesso di quando configuri un nuovo sottodominio della pagina di destinazione. Scopri come in [questa sezione](#lp-configure-new-subdomain).

1. Fai clic su **[!UICONTROL Invia]**.

1. Dopo l’invio, il sottodominio viene visualizzato nell’elenco con la **[!UICONTROL Elaborazione]** stato. Per ulteriori informazioni sugli stati dei sottodomini, consulta [questa sezione](access-subdomains.md).<!--Same statuses?-->

   ![](assets/lp_subdomain-processing.png)

   >[!NOTE]
   >
   >Prima di poter utilizzare quel sottodominio per inviare messaggi, è necessario attendere che Adobe esegua i controlli richiesti, che possono richiedere fino a 4 ore.<!--Learn more in [this section](delegate-subdomain.md#subdomain-validation).-->

1. Una volta eseguiti i controlli, il sottodominio ottiene il **[!UICONTROL Completato]** stato. È pronto per essere utilizzato per creare i predefiniti per le pagine di destinazione.

## Configurare un nuovo sottodominio {#lp-configure-new-subdomain}

>[!CONTEXTUALHELP]
>id="ajo_admin_lp_subdomain_dns"
>title="Genera il record DNS corrispondente"
>abstract="Per configurare un nuovo sottodominio della pagina di destinazione, è necessario copiare le informazioni del server dei nomi di Adobe visualizzate nell’interfaccia Journey Optimizer e incollarle nella soluzione di hosting del dominio per generare il record DNS corrispondente. Una volta eseguiti i controlli, il sottodominio è pronto per essere utilizzato per creare i predefiniti della pagina di destinazione."

Per configurare un nuovo sottodominio, effettua le seguenti operazioni.

1. Accedere al **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]** quindi seleziona **[!UICONTROL Configurazione e-mail]** > **[!UICONTROL Sottodomini della pagina di destinazione]**.

1. Fai clic su **[!UICONTROL Imposta sottodominio]**.

1. Seleziona **[!UICONTROL Aggiungi il tuo dominio]** dal **[!UICONTROL Tipo di configurazione]** sezione .

   ![](assets/lp_add-your-own-subdomain.png)

1. Specifica il sottodominio da delegare.

   >[!CAUTION]
   >
   >Non puoi utilizzare un sottodominio della pagina di destinazione esistente.
   >
   >Le lettere maiuscole non sono consentite nei sottodomini.

   Delega di un sottodominio non valido ad Adobe non consentita. Assicurati di inserire un sottodominio valido di proprietà della tua organizzazione, ad esempio marketing.yourcompany.com.

   >[!NOTE]
   >
   >Per le pagine di destinazione, sono supportati i sottodomini di più livelli. Ad esempio, puoi utilizzare &#39;email.marketing.yourcompany.com&#39;.

1. Viene visualizzato il record da inserire nei server DNS. Copia questo record o scarica un file CSV, quindi accedi alla tua soluzione di hosting del dominio per generare il record DNS corrispondente.

1. Assicurati che il record DNS sia stato generato nella tua soluzione di hosting del dominio. Se tutto è configurato correttamente, seleziona la casella &quot;Confermo...&quot;, quindi fai clic su **[!UICONTROL Invia]**.

   ![](assets/lp_add-your-own-subdomain-confirm.png)

   >[!NOTE]
   >
   >Quando configuri un nuovo sottodominio della pagina di destinazione, questo punta sempre a un record CNAME.

1. Una volta inviata la delega del sottodominio, il sottodominio viene visualizzato nell’elenco con la **[!UICONTROL Elaborazione]** stato. Per ulteriori informazioni sugli stati dei sottodomini, consulta [questa sezione](access-subdomains.md).<!--Same statuses?-->

   >[!NOTE]
   >
   >Prima di poter utilizzare quel sottodominio per inviare messaggi, è necessario attendere che Adobe esegua i controlli richiesti, che possono richiedere fino a 4 ore.<!--Learn more in [this section](#subdomain-validation).-->

1. Una volta eseguiti i controlli, il sottodominio ottiene il **[!UICONTROL Completato]** stato. È pronto per essere utilizzato per creare i predefiniti per le pagine di destinazione.

   Il sottodominio verrà contrassegnato come **[!UICONTROL Non riuscito]** se non riesci a creare il record di convalida nella soluzione di hosting.
