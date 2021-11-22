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
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 8021f66e-7725-475b-8722-e6f8d74c9023
source-git-commit: a174944bb8efcb67d758d4fe215674c1b8bbee13
workflow-type: tm+mt
source-wordcount: '760'
ht-degree: 6%

---

# Delegare un sottodominio

La delega del nome di dominio è un metodo che consente al proprietario di un nome di dominio (tecnicamente: una zona DNS) per delegare una sua suddivisione (tecnicamente: una zona DNS sotto di essa, che può essere chiamata sottozona) a un’altra entità. In sostanza, come cliente, se gestisci la zona &quot;example.com&quot;, puoi delegare ad Adobe la sottozona &quot;marketing.example.com&quot; .

Delega di un sottodominio per l’utilizzo con [!DNL Journey Optimizer], i client possono fare affidamento sull’Adobe per mantenere l’infrastruttura DNS necessaria per soddisfare i requisiti di recapito dei messaggi standard del settore per i propri domini di invio di e-mail marketing, continuando a mantenere e controllare il DNS per i propri domini e-mail interni.

[!DNL Journey Optimizer] ti consente di delegare completamente i sottodomini ad Adobe direttamente dall’interfaccia del prodotto. In questo modo, Adobe sarà in grado di inviare messaggi come servizio gestito controllando e mantenendo tutti gli aspetti del DNS necessari per la consegna, il rendering e il tracciamento delle campagne e-mail.

>[!NOTE]
>
>Per impostazione predefinita, [!DNL Journey Optimizer] il contratto di licenza ti consente di delegare fino a 10 sottodomini. Contatta il tuo contatto Adobe se desideri aumentare questa limitazione.
>
>L’utilizzo di CNAME per la delega dei sottodomini non è attualmente supportato da Journey Optimizer.

Per delegare un nuovo sottodominio, effettua le seguenti operazioni:

1. Accedere al **[!UICONTROL Channels]** / **[!UICONTROL Subdomains]** menu, quindi fai clic su **[!UICONTROL Delegate subdomain]**.

   ![](../assets/subdomain-delegate.png)

1. Specifica il nome del sottodominio da delegare.

   ![](../assets/subdomain-name.png)

   >[!CAUTION]
   >
   >Delega di un sottodominio non valido ad Adobe non consentita. Assicurati di inserire un sottodominio valido di proprietà della tua organizzazione, ad esempio marketing.yourcompany.com.
   >
   >I sottodomini di più livelli come e-mail.marketing.yourcompany.com non sono attualmente supportati.

1. Viene visualizzato l’elenco dei record da inserire nei server DNS. Copia questi record, uno per uno, o scaricando un file CSV, quindi accedi alla soluzione di hosting del tuo dominio per generare i record DNS corrispondenti.

1. Assicurati che tutti i record DNS siano stati generati nella tua soluzione di hosting del dominio. Se tutto è configurato correttamente, seleziona la casella &quot;Confermo...&quot;, quindi fai clic su **[!UICONTROL Submit]**.

   ![](../assets/subdomain-submit.png)

   >[!NOTE]
   >
   >Puoi creare i record e inviare la configurazione del sottodominio in un secondo momento utilizzando il **[!UICONTROL Save as draft]** pulsante . Potrai quindi riprendere la delega del sottodominio aprendola dall’elenco dei sottodomini.

1. Una volta inviata la delega del sottodominio, il sottodominio viene visualizzato nell’elenco con la **[!UICONTROL Processing]** stato. Per ulteriori informazioni sugli stati dei sottodomini, consulta [questa sezione](access-subdomains.md).

   ![](../assets/subdomain-processing.png)

   Prima di poter utilizzare quel sottodominio per inviare messaggi, è necessario attendere che Adobe esegua i controlli richiesti, che possono richiedere fino a 3 ore. [Ulteriori informazioni](#subdomain-validation).

1. Una volta eseguiti i controlli, il sottodominio ottiene il **[!UICONTROL Success]** stato. È pronto per essere utilizzato per inviare messaggi.

   <!-- later on, users will be notified in Pulse -->

   ![](../assets/subdomain-notification.png)

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

1. **Creare URL di tracciamento e mirroring**: se il dominio è email.example.com, il dominio di tracking/mirror sarà data.email.example.com. È protetto installando il certificato SSL.

1. **Provisioning di CDN CloudFront**: se CDN non è già configurato, Adobe lo prevede per l’imsorg.

1. **Crea dominio CDN**: se il dominio è email.example.com, il dominio CDN sarà cdn.email.example.com.

1. **Creare e allegare il certificato SSL CDN**: Adobe crea il certificato CDN per il dominio CDN e allega il certificato al dominio CDN.

1. **Crea DNS in avanti**: se si tratta del primo sottodominio che stai delegando, Adobe creerà il DNS in anticipo richiesto per creare record PTR, uno per ciascuno dei tuoi IP.

1. **Crea record PTR**: Il record PTR, noto anche come record DNS inversi, è richiesto dagli ISP in modo che non contrassegnino le e-mail come spam. Gmail consiglia inoltre di disporre di record PTR per ogni IP. Adobe crea record PTR solo quando deleghi il primo sottodominio, uno per ogni IP, tutti gli IP che puntano al primo sottodominio. Ad esempio, se l’IP è *192.1.2.1* e il sottodominio è *email.example.com*, il record PTR sarà: *192.1.2.1 PTR r1.email.example.com*. È possibile aggiornare successivamente il record PTR in modo da puntare al nuovo dominio delegato.
