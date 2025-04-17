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
source-git-commit: 8e5a904f9310385f5a8186159dedde9942624268
workflow-type: tm+mt
source-wordcount: '2009'
ht-degree: 20%

---

# Delegare un sottodominio {#delegate-subdomain}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomainname"
>title="Delega dei sottodomini"
>abstract="Journey Optimizer consente di delegare ad Adobe i sottodomini. Puoi delegare completamente un sottodominio ad Adobe, che è il metodo consigliato. Puoi anche creare un sottodominio utilizzando i CNAME per puntare a record specifici di Adobe, tuttavia questo approccio richiede di mantenere e gestire i record DNS in autonomia."
>additional-url="https://experienceleague.adobe.com/it/docs/journey-optimizer/using/configuration/delegate-subdomains/about-subdomain-delegation#subdomain-delegation-methods" text="Metodi di configurazione dei sottodomini"

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomainname_header"
>title="Delega dei sottodomini"
>abstract="Per iniziare a inviare e-mail, devi delegare ad Adobe il tuo sottodominio. I record DNS, le caselle in entrata, il mittente, gli indirizzi per la risposta e per il mancato recapitato verranno quindi configurati per te."

## Introduzione ai sottodomini e-mail {#gs-delegate-subdomain}

La delega del nome di dominio è un metodo che consente al proprietario di un nome di dominio (tecnicamente: una zona DNS) di delegare una sua suddivisione (tecnicamente: una zona DNS al di sotto di essa, che può essere definita sottozona) a un’altra entità. In sostanza, come cliente, se gestisci la zona &quot;example.com&quot;, puoi delegare la sottozona &quot;marketing.example.com&quot; ad Adobe. Ulteriori informazioni sulla delega del [sottodominio](about-subdomain-delegation.md)

Per impostazione predefinita, [!DNL Journey Optimizer] ti consente di delegare **fino a 10 sottodomini**. Tuttavia, a seconda del contratto di licenza, puoi delegare fino a 100 sottodomini. Per ulteriori informazioni sul numero di sottodomini a cui hai diritto, rivolgiti al tuo referente Adobe.

Puoi delegare completamente un sottodominio o crearne uno utilizzando i CNAME per puntare a record specifici di Adobe.

La delega completa del sottodominio è il metodo consigliato. Ulteriori informazioni sulle differenze tra i metodi di configurazione dei [sottodomini](about-subdomain-delegation.md#subdomain-delegation-methods).

La configurazione del sottodominio è **comune a tutti gli ambienti**. Pertanto, qualsiasi modifica a un sottodominio influisce anche sulle sandbox di produzione.

>[!CAUTION]
>
>L&#39;invio parallelo di sottodomini non è supportato in [!DNL Journey Optimizer]. Se tenti di inviare un sottodominio per la delega quando un altro è nello stato **[!UICONTROL Elaborazione]**, viene visualizzato un messaggio di errore.

## Delegare completamente un sottodominio ad Adobe {#full-subdomain-delegation}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_dns"
>title="Generare i record DNS corrispondenti"
>abstract="Per delegare completamente un nuovo sottodominio ad Adobe, devi copiare e incollare le informazioni del server dei nomi di Adobe visualizzate nell’interfaccia di Journey Optimizer nella soluzione di hosting del dominio per generare i record DNS corrispondenti. Per delegare un sottodominio utilizzando i CNAME, devi anche copiare e incollare il record di convalida dell’URL CDN SSL. Una volta eseguiti i controlli, il sottodominio è pronto per essere utilizzato per consegnare i messaggi."
>additional-url="https://experienceleague.adobe.com/it/docs/journey-optimizer/using/configuration/delegate-subdomains/delegate-subdomain#cname-subdomain-delegation" text="Delega dei sottodomini CNAME"

[!DNL Journey Optimizer] consente di delegare completamente i sottodomini ad Adobe direttamente dall&#39;interfaccia del prodotto. In questo modo, Adobe sarà in grado di fornire messaggi come servizio gestito controllando e mantenendo tutti gli aspetti del DNS necessari per la distribuzione, il rendering e il tracciamento delle campagne e-mail.

Puoi affidarti ad Adobe per mantenere l’infrastruttura DNS necessaria per soddisfare i requisiti di recapito messaggi standard di settore per i domini di invio del marketing e-mail, continuando al contempo a mantenere e controllare il DNS per i domini e-mail interni.

Per delegare completamente un nuovo sottodominio ad Adobe, segui i passaggi seguenti:

1. Accedi al menu **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]** > **[!UICONTROL Impostazioni e-mail]** > **[!UICONTROL Sottodomini]**, quindi fai clic su **[!UICONTROL Configura sottodominio]**.

   ![](assets/subdomain-delegate.png)

1. Seleziona **[!UICONTROL Completamente delegato]** dalla sezione **[!UICONTROL Imposta metodo]**.

   ![](assets/subdomain-method-full.png)

1. Specifica il nome del sottodominio da delegare.

   ![](assets/subdomain-name.png)

   >[!CAUTION]
   >
   >Non è consentito delegare un sottodominio non valido ad Adobe. Assicurati di immettere un sottodominio valido di proprietà della tua organizzazione, ad esempio marketing.yourcompany.com.

   <!--Capital letters are not allowed in subdomains. TBC by PM-->

1. Viene visualizzato l’elenco dei record da inserire nei server DNS. Copia questi record, uno per uno, o scaricando un file CSV, quindi accedi alla soluzione di hosting del tuo dominio per generare i record DNS corrispondenti.

1. Assicurati che tutti i record DNS siano stati generati nella soluzione di hosting del tuo dominio. Se tutto è configurato correttamente, seleziona la casella &quot;Confermo...&quot;.

   ![](assets/subdomain-submit.png)

1. Imposta il record DMARC. Se il sottodominio ha un record DMARC esistente e viene recuperato da [!DNL Journey Optimizer], puoi utilizzare gli stessi valori o modificarli in base alle esigenze. Se non aggiungi alcun valore, verranno utilizzati i valori predefiniti. [Ulteriori informazioni](dmarc-record.md)

   ![](assets/dmarc-record-found.png)

1. Fai clic su **[!UICONTROL Invia]**.

   Puoi creare i record e inviare la configurazione del sottodominio in seguito utilizzando il pulsante **[!UICONTROL Salva come bozza]**. Potrai quindi riprendere la delega del sottodominio aprendola dall’elenco dei sottodomini.

1. Il sottodominio viene visualizzato nell&#39;elenco con lo stato **[!UICONTROL Elaborazione]**. Per ulteriori informazioni sugli stati dei sottodomini, consulta [questa sezione](about-subdomain-delegation.md#access-delegated-subdomains).

   ![](assets/subdomain-processing.png)

   Prima di poter utilizzare tale sottodominio per inviare messaggi, devi attendere che Adobe esegua i controlli richiesti, che possono richiedere fino a 3 ore. Ulteriori informazioni in [questa sezione](#subdomain-validation).

   >[!NOTE]
   >
   >Eventuali record mancanti, ovvero i record non ancora creati nella soluzione di hosting, verranno elencati.

1. Una volta completati i controlli, il sottodominio ottiene lo stato **[!UICONTROL Completato]**. È pronto per essere utilizzato per inviare messaggi.

   Se non riesci a creare il record di convalida nella soluzione di hosting, il sottodominio verrà contrassegnato come **[!UICONTROL Non riuscito]**.

Una volta delegato un sottodominio ad Adobe in [!DNL Journey Optimizer], viene automaticamente creato un record PTR associato a questo sottodominio. [Ulteriori informazioni](ptr-records.md)


## Configurare un sottodominio con CNAME {#cname-subdomain-delegation}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_dns_cname"
>title="Generare i record DNS e di convalida corrispondenti"
>abstract="Per delegare un sottodominio utilizzando i CNAME, devi copiare e incollare le informazioni del server dei nomi di Adobe e il record di convalida dell’URL CDN SSL visualizzato nell’interfaccia di Journey Optimizer nella piattaforma di hosting. Una volta eseguiti i controlli, il sottodominio è pronto per essere utilizzato per consegnare i messaggi."

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_cdn_cname"
>title="Copiare il record di convalida"
>abstract="Adobe genera un record di convalida. Devi creare il record corrispondente sulla piattaforma di hosting per la convalida degli URL CDN."

Se si dispone di criteri di restrizione specifici per il dominio e si desidera che Adobe abbia solo un controllo parziale sul DNS, è possibile scegliere di eseguire tutte le attività correlate al DNS dal proprio lato.

La configurazione del sottodominio CNAME consente di creare un sottodominio e utilizzare i CNAME per puntare a record specifici di Adobe. Utilizzando questa configurazione, tu e Adobe condividete la responsabilità di mantenere il DNS per configurare l’ambiente per l’invio, il rendering e il tracciamento delle e-mail.

>[!CAUTION]
>
>Il metodo CNAME è consigliato se i criteri dell’organizzazione limitano il metodo di delega del sottodominio completo. Questo approccio richiede di gestire e mantenere i record DNS autonomamente. Adobe non sarà in grado di fornire assistenza per la modifica, la manutenzione o la gestione del DNS per un sottodominio configurato tramite il metodo CNAME.

➡️ [Scopri come creare un sottodominio utilizzando CNAME per puntare a record specifici di Adobe in questo video](#video)

Per impostare un sottodominio utilizzando i CNAME, segui i passaggi seguenti:

1. Accedi al menu **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]** > **[!UICONTROL Impostazioni e-mail]** > **[!UICONTROL Sottodomini]**, quindi fai clic su **[!UICONTROL Configura sottodominio]**.

1. Selezionare il metodo **[!UICONTROL CNAME configurato]**.

   ![](assets/subdomain-method-cname.png)

1. Specifica il nome del sottodominio da delegare.

   >[!CAUTION]
   >
   >Non devi delegare un sottodominio non valido ad Adobe. Assicurati di immettere un sottodominio valido di proprietà **della tua organizzazione**, ad esempio marketing.yourcompany.com.

   <!--Capital letters are not allowed in subdomains. TBC by PM-->

1. Viene visualizzato l’elenco dei record da inserire nei server DNS. Copia questi record, uno per uno, o scaricando un file CSV, quindi accedi alla soluzione di hosting del tuo dominio per generare i record DNS corrispondenti.

1. Assicurati che tutti i record DNS siano stati generati nella soluzione di hosting del tuo dominio. Se tutto è configurato correttamente, seleziona la casella &quot;Confermo...&quot;.

   ![](assets/subdomain-create-dns-confirm.png)

1. Configura il record DMARC. Se il sottodominio ha un record DMARC esistente e viene recuperato da [!DNL Journey Optimizer], puoi utilizzare gli stessi valori o modificarli in base alle esigenze. Se non aggiungi alcun valore, verranno utilizzati i valori predefiniti. [Ulteriori informazioni](dmarc-record.md)

   ![](assets/dmarc-record-found.png)

1. Fai clic su **[!UICONTROL Continua]**.

   In seguito potrai creare i record utilizzando il pulsante **[!UICONTROL Salva come bozza]**. A questo punto, potrai riprendere la delega del sottodominio aprendola dall’elenco dei sottodomini.

1. Attendi che Adobe verifichi che i record vengano generati senza errori nella soluzione di hosting. Questo processo può richiedere fino a 2 minuti.

   >[!NOTE]
   >
   >Eventuali record mancanti, ovvero i record non ancora creati nella soluzione di hosting, verranno elencati.

1. Adobe genera un record di convalida URL CDN SSL. Copia questo record di convalida nella piattaforma di hosting. Se hai creato correttamente questo record nella tua soluzione di hosting, seleziona la casella &quot;Confermo...&quot;, quindi fai clic su **[!UICONTROL Invia]**.

   <!--![](assets/subdomain-cdn-url-validation.png)-->

1. Una volta inviata la delega del sottodominio CNAME, il sottodominio viene visualizzato nell&#39;elenco con lo stato **[!UICONTROL Elaborazione]**. Per ulteriori informazioni sugli stati dei sottodomini, consulta [questa sezione](about-subdomain-delegation.md#access-delegated-subdomains).

   ![](assets/subdomain-cname-processing.png)

   Prima di poter utilizzare tale sottodominio per inviare messaggi, devi attendere che Adobe esegua i controlli richiesti, che in genere richiedono da 2 a 3 ore. Ulteriori informazioni in [questa sezione](#subdomain-validation).

1. Una volta completati i controlli<!--i.e Adobe validates the record you created and installs it-->, il sottodominio ottiene lo stato **[!UICONTROL Completato]**. È pronto per essere utilizzato per inviare messaggi.

   Se non riesci a creare il record di convalida nella soluzione di hosting, il sottodominio verrà contrassegnato come **[!UICONTROL Non riuscito]**.

Al momento della convalida del record e dell’installazione del certificato, Adobe crea automaticamente il record PTR per il sottodominio CNAME. [Ulteriori informazioni](ptr-records.md)


## Convalida del sottodominio {#subdomain-validation}

I controlli e le azioni di seguito vengono eseguiti fino alla verifica del sottodominio e possono essere utilizzati per inviare messaggi.

Questi passaggi vengono eseguiti da Adobe e possono richiedere **fino a 3 ore**.

1. **Pre-convalida**: Adobe controlla se il sottodominio è stato delegato ad Adobe DNS (record NS, record SOA, configurazione zona, record di proprietà). Se il passaggio di pre-convalida non riesce, viene restituito un errore insieme al motivo corrispondente, altrimenti Adobe procede al passaggio successivo.

1. **Configura DNS per il dominio**:

   * **Record MX**: record Mail eXchange - Record del server di posta che elabora le e-mail in entrata inviate al sottodominio.
   * **Record SPF**: record Framework criteri mittente - Elenca gli IP dei server di posta che possono inviare e-mail dal sottodominio.
   * **Record DKIM**: record standard DomainKeys Identified Mail - Utilizza la crittografia a chiave pubblica-privata per autenticare il messaggio ed evitare spoofing.
   * **A**: mapping IP predefinito.
   * **CNAME**: un record Canonical Name o CNAME è un tipo di record DNS che associa un nome alias a un nome di dominio vero o canonico.

1. **Crea URL di tracciamento e mirror**: se il dominio è email.example.com, il dominio di tracciamento/mirroring sarà data.email.example.com. Viene protetto installando il certificato SSL.

1. **Provisioning CDN CloudFront**: se CDN non è già configurato, Adobe esegue il provisioning per l&#39;ID della tua organizzazione.

1. **Crea dominio CDN**: se il dominio è email.example.com, il dominio CDN sarà cdn.email.example.com.

1. **Crea e allega certificato SSL CDN**: Adobe crea il certificato CDN per il dominio CDN e lo allega al dominio CDN.

1. **Crea DNS di inoltro**: se si tratta del primo sottodominio che si sta delegando, Adobe creerà il DNS di inoltro necessario per creare i record PTR, ovvero uno per ogni IP.

1. **Crea record PTR**: il record PTR, noto anche come record DNS inverso, è richiesto dagli ISP in modo che non contrassegni le e-mail come spam. Gmail consiglia inoltre di disporre di record PTR per ogni IP. Adobe crea record PTR solo quando deleghi un sottodominio per la prima volta, uno per ogni IP, tutti gli IP che puntano a quel sottodominio. Ad esempio, se l&#39;IP è *192.1.2.1* e il sottodominio è *email.example.com*, il record PTR sarà: *192.1.2.1PTR r1.email.example.com*. Puoi aggiornare il record PTR in seguito per puntare al nuovo dominio delegato. [Ulteriori informazioni sui record PTR](ptr-records.md)

## Annullare la delega di un sottodominio {#undelegate-subdomain}

Se desideri annullare la delega di un sottodominio, contatta il rappresentante Adobe.

Tuttavia, prima di contattare Adobe, devi eseguire diversi passaggi nell’interfaccia utente.

>[!NOTE]
>
>È possibile annullare la delega solo dei sottodomini con lo stato **[!UICONTROL Operazione riuscita]**. I sottodomini con stato **[!UICONTROL Bozza]** e **[!UICONTROL Non riuscito]** possono essere semplicemente eliminati dall&#39;interfaccia utente.

Eseguire innanzitutto i passaggi seguenti in [!DNL Journey Optimizer]:

1. Disattiva tutte le configurazioni di canale associate al sottodominio. [Scopri come](../configuration/channel-surfaces.md#deactivate-a-surface)

1. Annulla la delega dei sottodomini della pagina di destinazione, dei sottodomini SMS e dei sottodomini web associati a questo sottodominio.

   Devi inoltrare una richiesta dedicata per ogni [pagina di destinazione](../landing-pages/lp-subdomains.md#undelegate-subdomain), [SMS](../sms/sms-subdomains.md#undelegate-subdomain) o [sottodominio Web](../web/web-delegated-subdomains.md#undelegate-subdomain).

1. Arresta le campagne attive associate ai sottodomini. [Scopri come](../campaigns/modify-stop-campaign.md#stop)

1. Arresta i percorsi attivi associati ai sottodomini. [Scopri come](../building-journeys/end-journey.md#stop-journey)

1. Puntare i [record PTR](ptr-records.md#edit-ptr-record) collegati al sottodominio a un altro sottodominio.

   Se questo è l’unico sottodominio delegato, puoi saltare questo passaggio.

Al termine, rivolgiti al tuo rappresentante Adobe con il sottodominio da annullare la delega.

Dopo che la richiesta è gestita da Adobe, il dominio non delegato non viene più visualizzato nella pagina di inventario del sottodominio.

>[!CAUTION]
>
>Dopo l’annullamento della delega di un sottodominio:
>
>   * Non è possibile riattivare le configurazioni del canale che utilizzavano quel sottodominio.
>   * Non puoi delegare nuovamente il sottodominio esatto tramite l’interfaccia utente. Se lo desideri, contatta il tuo rappresentante Adobe.

## Video introduttivo{#video}

Scopri come creare un sottodominio utilizzando CNAME per puntare a record specifici di Adobe.

>[!VIDEO](https://video.tv.adobe.com/v/339484?quality=12)
