---
title: Delegare un sottodominio
description: Scopri come delegare i sottodomini.
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 8021f66e-7725-475b-8722-e6f8d74c9023
source-git-commit: 59cba4086cd198a8be597a9971105569d5db2eee
workflow-type: tm+mt
source-wordcount: '1667'
ht-degree: 9%

---

# Delegare un sottodominio {#delegate-subdomain}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomainname"
>title="Delega dei sottodomini"
>abstract="Journey Optimizer ti consente di delegare ad Adobe i sottodomini. Puoi delegare completamente un sottodominio ad Adobe, che è il metodo consigliato. Puoi anche creare un sottodominio utilizzando i CNAME per puntare a record specifici per gli Adobi, ma questo approccio richiede di mantenere e gestire i record DNS da solo."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/configuration-message/email-configuration/delegate-subdomains/about-subdomain-delegation.html#subdomain-delegation-methods" text="Metodi di configurazione dei sottodomini"

La delega del nome di dominio è un metodo che consente al proprietario di un nome di dominio (tecnicamente: una zona DNS) per delegare una sua suddivisione (tecnicamente: una zona DNS sotto di essa, che può essere chiamata sottozona) a un’altra entità. In sostanza, come cliente, se gestisci la zona &quot;example.com&quot;, puoi delegare ad Adobe la sottozona &quot;marketing.example.com&quot; . Ulteriori informazioni su [delega dei sottodomini](about-subdomain-delegation.md)

>[!NOTE]
>
>Per impostazione predefinita, [!DNL Journey Optimizer] il contratto di licenza ti consente di delegare fino a 10 sottodomini. Contatta il tuo contatto Adobe se desideri aumentare questa limitazione.

Puoi delegare completamente un sottodominio o creare un sottodominio utilizzando CNAME per puntare a record specifici per Adobi.

>[!CAUTION]
>
>La delega completa del sottodominio è il metodo consigliato. Ulteriori informazioni sulle differenze tra i due [metodi di configurazione del sottodominio](about-subdomain-delegation.md#subdomain-delegation-methods).

## Delega di sottodomini completa {#full-subdomain-delegation}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_dns"
>title="Genera i record DNS corrispondenti"
>abstract="Per delegare completamente un nuovo sottodominio ad Adobe, è necessario copiare e incollare le informazioni del server dei nomi di Adobe visualizzate nell’interfaccia Journey Optimizer nella soluzione di hosting del dominio per generare i record DNS corrispondenti. Per delegare un sottodominio utilizzando i CNAME, devi anche copiare e incollare il record di convalida dell’URL CDN SSL. Una volta eseguiti i controlli, il sottodominio è pronto per essere utilizzato per inviare i messaggi."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/configuration-message/email-configuration/delegate-subdomains/delegate-subdomain.html#cname-subdomain-delegation" text="Delega dei sottodomini CNAME"

[!DNL Journey Optimizer] ti consente di delegare completamente i sottodomini ad Adobe direttamente dall’interfaccia del prodotto. In questo modo, Adobe sarà in grado di inviare messaggi come servizio gestito controllando e mantenendo tutti gli aspetti del DNS necessari per la consegna, il rendering e il tracciamento delle campagne e-mail.

Puoi contare sull’Adobe per mantenere l’infrastruttura DNS necessaria per soddisfare i requisiti di recapito dei messaggi standard del settore per i domini di invio di e-mail marketing, mantenendo e controllando il DNS per i domini di e-mail interni.

Per delegare completamente un nuovo sottodominio ad Adobe, effettua le seguenti operazioni:

1. Accedere al **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Subdomains]** menu, quindi fai clic su **[!UICONTROL Set up subdomain]**.

   ![](assets/subdomain-delegate.png)

1. Seleziona **[!UICONTROL Fully delegated]** dal **[!UICONTROL Set up method]** sezione .

   ![](assets/subdomain-method-full.png)

1. Specifica il nome del sottodominio da delegare.

   ![](assets/subdomain-name.png)

   >[!CAUTION]
   >
   >Delega di un sottodominio non valido ad Adobe non consentita. Assicurati di inserire un sottodominio valido di proprietà della tua organizzazione, ad esempio marketing.yourcompany.com.
   >
   >I sottodomini di più livelli come e-mail.marketing.yourcompany.com non sono attualmente supportati.

1. Viene visualizzato l’elenco dei record da inserire nei server DNS. Copia questi record, uno per uno, o scaricando un file CSV, quindi accedi alla soluzione di hosting del tuo dominio per generare i record DNS corrispondenti.

1. Assicurati che tutti i record DNS siano stati generati nella tua soluzione di hosting del dominio. Se tutto è configurato correttamente, seleziona la casella &quot;Confermo...&quot;, quindi fai clic su **[!UICONTROL Submit]**.

   ![](assets/subdomain-submit.png)

   >[!NOTE]
   >
   >Puoi creare i record e inviare la configurazione del sottodominio in un secondo momento utilizzando il **[!UICONTROL Save as draft]** pulsante . Potrai quindi riprendere la delega del sottodominio aprendola dall’elenco dei sottodomini.

1. Una volta inviata la delega completa del sottodominio, il sottodominio viene visualizzato nell’elenco con la **[!UICONTROL Processing]** stato. Per ulteriori informazioni sugli stati dei sottodomini, consulta [questa sezione](access-subdomains.md).

   ![](assets/subdomain-processing.png)

   Prima di poter utilizzare quel sottodominio per inviare messaggi, è necessario attendere che Adobe esegua i controlli richiesti, che possono richiedere fino a 3 ore. Ulteriori informazioni in [questa sezione](#subdomain-validation).

   >[!NOTE]
   >
   >Vengono elencati tutti i record mancanti, ovvero quelli non ancora creati nella soluzione di hosting.

1. Una volta eseguiti i controlli, il sottodominio ottiene il **[!UICONTROL Success]** stato. È pronto per essere utilizzato per inviare messaggi.

   >[!NOTE]
   >
   >Il sottodominio verrà contrassegnato come **[!UICONTROL Failed]** se non riesci a creare il record di convalida nella soluzione di hosting.

   <!-- later on, users will be notified in Pulse -->

Una volta delegato un sottodominio ad Adobe in [!DNL Journey Optimizer], viene creato automaticamente un record PTR associato a questo sottodominio. [Ulteriori informazioni](ptr-records.md)

>[!CAUTION]
>
>L’esecuzione parallela dei sottodomini non è attualmente supportata in [!DNL Journey Optimizer]. Se tenti di inviare un sottodominio per la delega quando un altro ha **[!UICONTROL Processing]** stato, riceverai un messaggio di errore.

## Delega dei sottodomini CNAME {#cname-subdomain-delegation}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_dns_cname"
>title="Genera i record DNS e di convalida corrispondenti"
>abstract="Per delegare un sottodominio utilizzando i CNAME, devi copiare e incollare le informazioni del server dei nomi di Adobe e il record di convalida dell’URL CDN SSL visualizzato nell’interfaccia Journey Optimizer nella piattaforma host. Una volta eseguiti i controlli, il sottodominio è pronto per essere utilizzato per inviare i messaggi."

Se si dispone di criteri di restrizione specifici per il dominio e si desidera che l&#39;Adobe abbia solo un controllo parziale sul DNS, è possibile scegliere di eseguire tutte le attività relative al DNS sul proprio lato.

La delega dei sottodomini CNAME ti consente di creare un sottodominio e di utilizzare i CNAME per puntare a record specifici per Adobe. Utilizzando questa configurazione, tu e Adobe condividete la responsabilità di mantenere il DNS per configurare l’ambiente per l’invio, il rendering e il tracciamento delle e-mail.

>[!CAUTION]
>
>Il metodo CNAME è consigliato se i criteri aziendali limitano il metodo di delega del sottodominio completo. Questo approccio richiede la gestione e la gestione autonoma dei record DNS. Adobe non sarà in grado di fornire assistenza per modificare, mantenere o gestire il DNS per un sottodominio configurato tramite il metodo CNAME.

➡️ [Scopri come creare un sottodominio utilizzando CNAME per puntare a record specifici per Adobi in questo video](#video)

Per delegare un sottodominio utilizzando i CNAME, segui i passaggi seguenti:

1. Accedere al **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Subdomains]** menu, quindi fai clic su **[!UICONTROL Set up subdomain]**.

1. Seleziona la **[!UICONTROL CNAME set up]** metodo .

   ![](assets/subdomain-method-cname.png)

1. Specifica il nome del sottodominio da delegare.

   >[!CAUTION]
   >
   >Delega di un sottodominio non valido ad Adobe non consentita. Assicurati di inserire un sottodominio valido di proprietà della tua organizzazione, ad esempio marketing.yourcompany.com.
   >
   >I sottodomini di più livelli come e-mail.marketing.yourcompany.com non sono attualmente supportati.

1. Viene visualizzato l’elenco dei record da inserire nei server DNS. Copia questi record, uno per uno, o scaricando un file CSV, quindi accedi alla soluzione di hosting del tuo dominio per generare i record DNS corrispondenti.

1. Assicurati che tutti i record DNS siano stati generati nella tua soluzione di hosting del dominio. Se tutto è configurato correttamente, seleziona la casella &quot;Confermo...&quot;.

   ![](assets/subdomain-create-dns-confirm.png)

   >[!NOTE]
   >
   >Puoi creare i record in un secondo momento utilizzando il **[!UICONTROL Save as draft]** pulsante . A questo punto potrai riprendere la delega del sottodominio aprendola dall’elenco dei sottodomini.

1. Attendi che l&#39;Adobe verifichi che questi record vengano generati senza errori nella tua soluzione di hosting. Questo processo può richiedere fino a 2 minuti.

   >[!NOTE]
   >
   >Vengono elencati tutti i record mancanti, ovvero quelli non ancora creati nella soluzione di hosting.

1. Adobe genera un record di convalida URL CDN SSL. Copia questo record di convalida nella piattaforma host. Se hai creato correttamente questo record nella tua soluzione di hosting, seleziona la casella &quot;Conferma...&quot;, quindi fai clic su **[!UICONTROL Submit]**.

   ![](assets/subdomain-cdn-url-validation.png)

   >[!NOTE]
   >
   >Puoi anche creare il record di convalida e inviare la configurazione del sottodominio in un secondo momento utilizzando il **[!UICONTROL Save as draft]** pulsante . Potrai quindi riprendere la delega del sottodominio aprendola dall’elenco dei sottodomini.

1. Una volta inviata la delega del sottodominio CNAME, il sottodominio viene visualizzato nell’elenco con la **[!UICONTROL Processing]** stato. Per ulteriori informazioni sugli stati dei sottodomini, consulta [questa sezione](access-subdomains.md).

   Prima di poter utilizzare tale sottodominio per inviare messaggi, è necessario attendere che Adobe esegua i controlli richiesti, che in genere richiedono da 2 a 3 ore. Ulteriori informazioni in [questa sezione](#subdomain-validation).

1. Una volta eseguiti i controlli<!--i.e Adobe validates the record you created and installs it-->, il sottodominio ottiene **[!UICONTROL Success]** stato. È pronto per essere utilizzato per inviare messaggi.

   >[!NOTE]
   >
   >Il sottodominio verrà contrassegnato come **[!UICONTROL Failed]** se non riesci a creare il record di convalida nella soluzione di hosting.

Dopo aver convalidato il record e aver installato il certificato, in Adobe viene creato automaticamente il record PTR per il sottodominio CNAME. [Ulteriori informazioni](ptr-records.md)

>[!CAUTION]
>
>L’esecuzione parallela dei sottodomini non è attualmente supportata in [!DNL Journey Optimizer]. Se tenti di inviare un sottodominio per la delega quando un altro ha **[!UICONTROL Processing]** stato, riceverai un messaggio di errore.

## Convalida del sottodominio {#subdomain-validation}

I controlli e le azioni seguenti vengono eseguiti fino a quando il sottodominio non viene verificato e possono essere utilizzati per inviare messaggi.

>[!NOTE]
>
>Questi passaggi vengono eseguiti per Adobe e possono richiedere fino a 3 ore.

1. **Pre-convalida**: Adobe controlla se il sottodominio è stato delegato a DNS Adobi (record NS, record SOA, configurazione zona, record di proprietà). Se il passaggio di pre-convalida non riesce, viene restituito un errore insieme al motivo corrispondente, altrimenti l’Adobe passa al passaggio successivo.

1. **Configurare il DNS per il dominio**:

   * **Record MX**: Record eXchange di posta - Record server di posta che elabora le e-mail in entrata inviate al sottodominio.
   * **Record SPF**: Record del framework dei criteri del mittente: elenca gli IP dei server di posta che possono inviare e-mail dal sottodominio.
   * **Record DKIM**: Record standard DomainKeys Identified Mail - Utilizza la crittografia a chiave pubblica-privata per autenticare il messaggio per evitare lo spoofing.
   * **A**: Mappatura IP predefinita.
   * **CNAME**: Un record Canonical Name o CNAME è un tipo di record DNS che mappa un nome di alias a un nome di dominio vero o canonico.

1. **Creare URL di tracciamento e mirroring**: se il dominio è email.example.com, il dominio di tracking/mirror sarà data.email.example.com. È protetto installando il certificato SSL.

1. **Provisioning di CDN CloudFront**: se CDN non è già configurato, Adobe lo fornisce per l’ID della tua organizzazione.

1. **Crea dominio CDN**: se il dominio è email.example.com, il dominio CDN sarà cdn.email.example.com.

1. **Creare e allegare il certificato SSL CDN**: Adobe crea il certificato CDN per il dominio CDN e allega il certificato al dominio CDN.

1. **Crea DNS in avanti**: se si tratta del primo sottodominio che stai delegando, Adobe creerà il DNS in anticipo richiesto per creare record PTR, uno per ciascuno dei tuoi IP.

1. **Crea record PTR**: Il record PTR, noto anche come record DNS inversi, è richiesto dagli ISP in modo che non contrassegnino le e-mail come spam. Gmail consiglia inoltre di disporre di record PTR per ogni IP. Adobe crea record PTR solo quando deleghi un sottodominio per la prima volta, uno per ogni IP, tutti gli IP che puntano a quel sottodominio. Ad esempio, se l’IP è *192.1.2.1* e il sottodominio è *email.example.com*, il record PTR sarà: *192.1.2.1 PTR r1.email.example.com*. È possibile aggiornare successivamente il record PTR in modo da puntare al nuovo dominio delegato. [Ulteriori informazioni sui record PTR](ptr-records.md)

## Video introduttivo{#video}

Scopri come creare un sottodominio utilizzando CNAME per puntare a record specifici di Adobe.

>[!VIDEO](https://video.tv.adobe.com/v/339484?quality=12)
