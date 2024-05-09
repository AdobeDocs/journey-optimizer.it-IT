---
solution: Journey Optimizer
product: journey optimizer
title: Delegare un sottodominio
description: Scopri come delegare i sottodomini.
feature: Subdomains, Deliverability
topic: Administration
role: Admin
level: Experienced
keywords: sottodominio, delega, dominio, DNS
exl-id: 8021f66e-7725-475b-8722-e6f8d74c9023
source-git-commit: 5b36d082e054b7b75b09bd0392f9a58527a9c0a3
workflow-type: tm+mt
source-wordcount: '1816'
ht-degree: 23%

---

# Delegare un sottodominio {#delegate-subdomain}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomainname"
>title="Delega dei sottodomini"
>abstract="Journey Optimizer consente di delegare ad Adobe i sottodomini. Puoi delegare completamente un sottodominio ad Adobe, che è il metodo consigliato. Puoi anche creare un sottodominio utilizzando i CNAME per puntare a record specifici di Adobe, tuttavia questo approccio richiede di mantenere e gestire i record DNS in autonomia."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/delegate-subdomains/about-subdomain-delegation.html?lang=it#subdomain-delegation-methods" text="Metodi di configurazione dei sottodomini"

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomainname_header"
>title="Delega dei sottodomini"
>abstract="Per iniziare a inviare e-mail, devi delegare ad Adobe il tuo sottodominio. I record DNS, le caselle in entrata, il mittente, gli indirizzi per la risposta e per il mancato recapitato verranno quindi configurati per te."

La delega del nome di dominio è un metodo che consente al proprietario di un nome di dominio (tecnicamente: una zona DNS) di delegare una sua suddivisione (tecnicamente: una zona DNS al di sotto di essa, che può essere definita sottozona) a un’altra entità. Fondamentalmente, come cliente, se gestisci la zona &quot;example.com&quot;, puoi delegare la sottozona &quot;marketing.example.com&quot; ad Adobe. Ulteriori informazioni su [delega dei sottodomini](about-subdomain-delegation.md)

>[!NOTE]
>
>Per impostazione predefinita, [!DNL Journey Optimizer] consente di delegare fino a 10 sottodomini. Tuttavia, a seconda del contratto di licenza, puoi delegare fino a 100 sottodomini. Per ulteriori informazioni sul numero di sottodomini a cui hai diritto, rivolgiti al tuo referente Adobe.

Puoi delegare completamente un sottodominio o crearne uno utilizzando i CNAME per puntare a record specifici di un Adobe.

>[!CAUTION]
>
>La delega completa del sottodominio è il metodo consigliato. Ulteriori informazioni sulle differenze tra [metodi di configurazione dei sottodomini](about-subdomain-delegation.md#subdomain-delegation-methods).
>
>La configurazione del sottodominio è comune a tutti gli ambienti. Pertanto, qualsiasi modifica a un sottodominio influirà anche sulle sandbox di produzione.

## Delega completa di sottodominio {#full-subdomain-delegation}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_dns"
>title="Generare i record DNS corrispondenti"
>abstract="Per delegare completamente un nuovo sottodominio ad Adobe, devi copiare e incollare le informazioni del server dei nomi di Adobe visualizzate nell’interfaccia di Journey Optimizer nella soluzione di hosting del dominio per generare i record DNS corrispondenti. Per delegare un sottodominio utilizzando i CNAME, devi anche copiare e incollare il record di convalida dell’URL CDN SSL. Una volta eseguiti i controlli, il sottodominio è pronto per essere utilizzato per consegnare i messaggi."
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/configuration/delegate-subdomains/delegate-subdomain#cname-subdomain-delegation" text="Delega dei sottodomini CNAME"

[!DNL Journey Optimizer] consente di delegare completamente i sottodomini ad Adobe direttamente dall’interfaccia del prodotto. In questo modo Adobe sarà in grado di fornire messaggi come servizio gestito controllando e mantenendo tutti gli aspetti del DNS necessari per la distribuzione, il rendering e il tracciamento delle campagne e-mail.

Puoi affidarti ad Adobe per mantenere l’infrastruttura DNS necessaria per soddisfare i requisiti di recapito messaggi standard di settore per i domini di invio del marketing e-mail, continuando al contempo a mantenere e controllare il DNS per i domini e-mail interni.

Per delegare completamente un nuovo sottodominio ad Adobe, segui i passaggi seguenti:

1. Accedere a **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]** > **[!UICONTROL Sottodomini]** , quindi fai clic su **[!UICONTROL Configurare il sottodominio]**.

   ![](assets/subdomain-delegate.png)

1. Seleziona **[!UICONTROL Completamente delegato]** dal **[!UICONTROL Metodo di configurazione]** sezione.

   ![](assets/subdomain-method-full.png)

1. Specifica il nome del sottodominio da delegare.

   ![](assets/subdomain-name.png)

   >[!CAUTION]
   >
   >La delega di un sottodominio non valido a Adobe non è consentita. Assicurati di immettere un sottodominio valido di proprietà della tua organizzazione, ad esempio marketing.yourcompany.com.

   <!--Capital letters are not allowed in subdomains. TBC by PM-->

1. Viene visualizzato l’elenco dei record da inserire nei server DNS. Copia questi record, uno per uno, o scaricando un file CSV, quindi accedi alla soluzione di hosting del tuo dominio per generare i record DNS corrispondenti.

1. Assicurati che tutti i record DNS siano stati generati nella soluzione di hosting del tuo dominio. Se tutto è configurato correttamente, seleziona la casella &quot;Confermo...&quot;.

   ![](assets/subdomain-submit.png)

1. Impostare il record DMARC. Se il sottodominio ha un record DMARC esistente e se viene recuperato da [!DNL Journey Optimizer], è possibile utilizzare gli stessi valori o modificarli in base alle esigenze. Se non aggiungi alcun valore, verranno utilizzati i valori predefiniti. [Ulteriori informazioni](dmarc-record.md)

   ![](assets/dmarc-record-found.png)

1. Fai clic su **[!UICONTROL Invia]**.

   >[!NOTE]
   >
   >Puoi creare i record e inviare la configurazione del sottodominio in un secondo momento utilizzando **[!UICONTROL Salva come bozza]** pulsante. Potrai quindi riprendere la delega del sottodominio aprendola dall’elenco dei sottodomini.

1. Il sottodominio viene visualizzato nell’elenco con **[!UICONTROL Elaborazione]** stato. Per ulteriori informazioni sugli stati dei sottodomini, consulta [questa sezione](about-subdomain-delegation.md#access-delegated-subdomains).

   ![](assets/subdomain-processing.png)

   Prima di poter utilizzare tale sottodominio per inviare messaggi, devi attendere che Adobe esegua i controlli richiesti, che possono richiedere fino a 3 ore. Ulteriori informazioni in [questa sezione](#subdomain-validation).

   >[!NOTE]
   >
   >Eventuali record mancanti, ovvero i record non ancora creati nella soluzione di hosting, verranno elencati.

1. Quando i controlli hanno esito positivo, il sottodominio ottiene il **[!UICONTROL Completato]** stato. È pronto per essere utilizzato per inviare messaggi.

   >[!NOTE]
   >
   >Il sottodominio verrà contrassegnato come **[!UICONTROL Non riuscito]** se non riesci a creare il record di convalida nella soluzione di hosting.

Una volta delegato un sottodominio all’Adobe in [!DNL Journey Optimizer]: viene creato e associato automaticamente un record PTR a questo sottodominio. [Ulteriori informazioni](ptr-records.md)

>[!CAUTION]
>
>L’esecuzione parallela dei sottodomini non è attualmente supportata in [!DNL Journey Optimizer]. Se tenti di inviare un sottodominio per la delega quando un altro ha la proprietà **[!UICONTROL Elaborazione]** stato, verrà visualizzato un messaggio di errore.

## Configurazione del sottodominio CNAME {#cname-subdomain-delegation}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_dns_cname"
>title="Generare i record DNS e di convalida corrispondenti"
>abstract="Per delegare un sottodominio utilizzando i CNAME, devi copiare e incollare le informazioni del server dei nomi di Adobe e il record di convalida dell’URL CDN SSL visualizzato nell’interfaccia di Journey Optimizer nella piattaforma di hosting. Una volta eseguiti i controlli, il sottodominio è pronto per essere utilizzato per consegnare i messaggi."

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_cdn_cname"
>title="Copiare il record di convalida"
>abstract="Adobe genera un record di convalida. Devi creare il record corrispondente sulla piattaforma di hosting per la convalida degli URL CDN."

Se si dispone di criteri di restrizione specifici per il dominio e si desidera che Adobe abbia solo un controllo parziale sul DNS, è possibile scegliere di eseguire tutte le attività correlate al DNS dal proprio lato.

La configurazione del sottodominio CNAME consente di creare un sottodominio e utilizzare i CNAME per puntare a record specifici di un Adobe. Utilizzando questa configurazione, tu e Adobe condividete la responsabilità di mantenere il DNS per configurare l’ambiente per l’invio, il rendering e il tracciamento delle e-mail.

>[!CAUTION]
>
>Il metodo CNAME è consigliato se i criteri dell’organizzazione limitano il metodo di delega del sottodominio completo. Questo approccio richiede di gestire e mantenere i record DNS autonomamente. Adobe non sarà in grado di fornire assistenza per la modifica, la manutenzione o la gestione del DNS per un sottodominio configurato tramite il metodo CNAME.

➡️ [Scopri come creare un sottodominio utilizzando CNAME per puntare a record specifici per Adobe in questo video](#video)

Per impostare un sottodominio utilizzando i CNAME, segui i passaggi seguenti:

1. Accedere a **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]** > **[!UICONTROL Sottodomini]** , quindi fai clic su **[!UICONTROL Configurare il sottodominio]**.

1. Seleziona la **[!UICONTROL Configurazione CNAME]** metodo.

   ![](assets/subdomain-method-cname.png)

1. Specifica il nome del sottodominio da delegare.

   >[!CAUTION]
   >
   >La delega di un sottodominio non valido a Adobe non è consentita. Assicurati di immettere un sottodominio valido di proprietà della tua organizzazione, ad esempio marketing.yourcompany.com.

   <!--Capital letters are not allowed in subdomains. TBC by PM-->

1. Viene visualizzato l’elenco dei record da inserire nei server DNS. Copia questi record, uno per uno, o scaricando un file CSV, quindi accedi alla soluzione di hosting del tuo dominio per generare i record DNS corrispondenti.

1. Assicurati che tutti i record DNS siano stati generati nella soluzione di hosting del tuo dominio. Se tutto è configurato correttamente, seleziona la casella &quot;Confermo...&quot;.

   ![](assets/subdomain-create-dns-confirm.png)

1. Imposta il record DMARC. Se il sottodominio ha un record DMARC esistente e se viene recuperato da [!DNL Journey Optimizer], è possibile utilizzare gli stessi valori o modificarli in base alle esigenze. Se non aggiungi alcun valore, verranno utilizzati i valori predefiniti. [Ulteriori informazioni](dmarc-record.md)

   ![](assets/dmarc-record-found.png)

1. Fai clic su **[!UICONTROL Continua]**.

   >[!NOTE]
   >
   >È possibile creare i record in un secondo momento utilizzando **[!UICONTROL Salva come bozza]** pulsante. A questo punto, potrai riprendere la delega del sottodominio aprendola dall’elenco dei sottodomini.

1. Attendi che Adobe verifichi che i record vengano generati senza errori nella soluzione di hosting. Questo processo può richiedere fino a 2 minuti.

   >[!NOTE]
   >
   >Eventuali record mancanti, ovvero i record non ancora creati nella soluzione di hosting, verranno elencati.

1. L’Adobe genera un record di convalida URL CDN SSL. Copia questo record di convalida nella piattaforma di hosting. Se hai creato correttamente questo record nella tua soluzione di hosting, seleziona la casella &quot;Confermo...&quot;, quindi fai clic su **[!UICONTROL Invia]**.

   <!--![](assets/subdomain-cdn-url-validation.png)-->

1. Una volta inviata la delega del sottodominio CNAME, il sottodominio viene visualizzato nell’elenco con **[!UICONTROL Elaborazione]** stato. Per ulteriori informazioni sugli stati dei sottodomini, consulta [questa sezione](about-subdomain-delegation.md#access-delegated-subdomains).

   ![](assets/subdomain-cname-processing.png)

   Prima di poter utilizzare tale sottodominio per inviare messaggi, devi attendere che Adobe esegua i controlli richiesti, che in genere richiedono da 2 a 3 ore. Ulteriori informazioni in [questa sezione](#subdomain-validation).

1. Una volta completati i controlli<!--i.e Adobe validates the record you created and installs it-->, il sottodominio ottiene il **[!UICONTROL Completato]** stato. È pronto per essere utilizzato per inviare messaggi.

   >[!NOTE]
   >
   >Il sottodominio verrà contrassegnato come **[!UICONTROL Non riuscito]** se non riesci a creare il record di convalida nella soluzione di hosting.

Al momento della convalida del record e dell’installazione del certificato, Adobe crea automaticamente il record PTR per il sottodominio CNAME. [Ulteriori informazioni](ptr-records.md)

>[!CAUTION]
>
>L’esecuzione parallela dei sottodomini non è attualmente supportata in [!DNL Journey Optimizer]. Se tenti di inviare un sottodominio per la delega quando un altro ha la proprietà **[!UICONTROL Elaborazione]** stato, verrà visualizzato un messaggio di errore.

## Convalida del sottodominio {#subdomain-validation}

I controlli e le azioni seguenti verranno eseguiti fino alla verifica del sottodominio e possono essere utilizzati per inviare messaggi.

>[!NOTE]
>
>Questi passaggi vengono eseguiti da Adobe e possono richiedere fino a 3 ore.

1. **Pre-convalida**: Adobe controlla se il sottodominio è stato delegato al DNS Adobe (record NS, record SOA, configurazione zona, record di proprietà). Se il passaggio di preconvalida non riesce, viene restituito un errore insieme al motivo corrispondente, altrimenti Adobe passa al passaggio successivo.

1. **Configurare il DNS per il dominio**:

   * **Record MX**: record Mail eXchange: record del server di posta che elabora le e-mail in entrata inviate al sottodominio.
   * **Record SPF**: record Framework dei criteri del mittente: elenca gli IP dei server di posta che possono inviare e-mail dal sottodominio.
   * **Record DKIM**: record standard di DomainKeys Identified Mail - Utilizza la crittografia a chiave pubblica-privata per autenticare il messaggio ed evitare spoofing.
   * **A**: mappatura IP predefinita.
   * **CNAME**: un nome canonico o record CNAME è un tipo di record DNS che associa un nome alias a un nome di dominio vero o canonico.

1. **Creare URL di tracciamento e mirror**: se il dominio è email.example.com, il dominio di tracciamento/mirroring sarà data.email.example.com. Viene protetto installando il certificato SSL.

1. **Provisioning di CloudFront CDN**: se CDN non è già configurato, Adobe esegue il provisioning per l’ID della tua organizzazione.

1. **Crea dominio CDN**: se il dominio è email.example.com, il dominio CDN sarà cdn.email.example.com.

1. **Crea e allega il certificato SSL CDN**: Adobe crea il certificato CDN per il dominio CDN e allega il certificato al dominio CDN.

1. **Crea DNS di inoltro**: se si tratta del primo sottodominio che stai delegando, Adobe creerà il DNS di inoltro necessario per creare record PTR, uno per ogni IP.

1. **Crea record PTR**: il record PTR, noto anche come record DNS inverso, è richiesto dagli ISP in modo che non contrassegni le e-mail come spam. Gmail consiglia inoltre di disporre di record PTR per ogni IP. In questo Adobe vengono creati record PTR solo quando si delega un sottodominio per la prima volta, uno per ogni IP, tutti gli IP che puntano a tale sottodominio. Ad esempio, se l’IP è *192.1.2.1.* e il sottodominio è *email.example.com*, il record PTR sarà: *PTR 192.1.2.1 r1.email.example.com*. Puoi aggiornare il record PTR in seguito per puntare al nuovo dominio delegato. [Ulteriori informazioni sui record PTR](ptr-records.md)

## Video introduttivo{#video}

Scopri come creare un sottodominio utilizzando CNAME per puntare a record specifici di Adobe.

>[!VIDEO](https://video.tv.adobe.com/v/339484?quality=12)
