---
title: Introduzione ai canali personalizzati
description: Scopri come utilizzare  [!DNL Journey Optimizer]'s Channel Builder to bring any outbound messaging channel into [!DNL Journey Optimizer]  e utilizzarlo in campagne, percorsi e campagne orchestrate.
feature: Channel Configuration
topic: Content Management
role: User
level: Beginner
badge: label="Disponibilità limitata" type="Informative"
source-git-commit: 94ca2d9458152fb471e9590d053c4729a4a5134f
workflow-type: tm+mt
source-wordcount: '628'
ht-degree: 4%

---


# Introduzione ai canali personalizzati {#get-started-custom-channel}

>[!AVAILABILITY]
>
>Questa funzionalità è in disponibilità limitata. Per ottenere l’accesso, contatta il rappresentante Adobe.

<!--Multilingual support, business rules enforcement, and [!DNL Adobe Experience Decisioning] integration are planned for a future release.-->

La funzionalità **Canali personalizzati** di [!DNL Journey Optimizer] consente di inserire in [!DNL Journey Optimizer] qualsiasi canale in uscita in modo da poterlo utilizzare in campagne, percorsi e campagne orchestrate, proprio come qualsiasi canale nativo. Utilizzando **Channel Builder**, gli amministratori possono creare e configurare nuovi canali senza l&#39;intervento degli ingegneri e gli addetti al marketing possono iniziare a utilizzarli immediatamente per comunicare con i clienti.

## Che problema risolve? {#why-custom-channels}

[!DNL Journey Optimizer] supporta in modo nativo e-mail, SMS, notifiche push, WhatsApp, LINE e altri canali. Tuttavia, molte organizzazioni utilizzano piattaforme di messaggistica che non sono integrate in modo nativo, ad esempio WeChat, Kakao Talk, Messenger o un provider esterno, e desiderano utilizzarle in [!DNL Journey Optimizer] per l&#39;orchestrazione e la creazione di campagne, pur continuando a distribuire con il proprio fornitore.

<!--TBC: Another use case is when organizations have a legacy messaging gateway that exposes an HTTP endpoint, and they want to use it in [!DNL Journey Optimizer] without having to build a custom integration.-->

I canali personalizzati colmano questo vuoto: ti consentono di utilizzare qualsiasi endpoint HTTP in uscita come canale [!DNL Journey Optimizer] completo, sbloccando:

* **Funzionalità full channel** - Ottimizzazione (sperimentazione dei contenuti e targeting), reporting e monitoraggio OOTB, applicazione del consenso e della governance e frammenti di espressione. <!--Multilingual and business rules are planned for a future release.-->
* **Orchestrazione unificata**: gestisci tutti i canali di messaggistica in un&#39;unica posizione, indipendentemente dal provider di consegna sottostante.
* **Configurazione senza codice** - Gli amministratori configurano il canale tramite l&#39;interfaccia utente di Channel Builder; non è necessario alcun codice personalizzato o intervento tecnico.

## Canale personalizzato e azioni personalizzate {#custom-channel-vs-custom-action}

Se hai utilizzato [azioni personalizzate](../action/action.md) in [!DNL Journey Optimizer] percorsi prima, i canali personalizzati affrontano un diverso set di casi d&#39;uso.

**Utilizza canali personalizzati quando** devi inviare messaggi agli utenti finali tramite una piattaforma non supportata in modo nativo in [!DNL Journey Optimizer], ad esempio WeChat, Kakao Talk o un gateway di messaggistica personalizzato. I canali personalizzati sono disponibili in campagne, percorsi, campagne orchestrate e supporto:

* Personalizzazione completa tramite l’editor di personalizzazione, simile ai canali nativi in uscita
* Editor payload visivo/di moduli, anteprima e bozza
* Sperimentazione dei contenuti e targeting
* Reporting e monitoraggio integrati
* Configurazioni di più credenziali API e canali
* RBAC/ABAC

I canali personalizzati supportano POST come unico metodo HTTP.

**Utilizzare azioni personalizzate quando** è necessario recuperare dati da o inviare informazioni a un sistema esterno, ad esempio un call center, una piattaforma di registrazione o un database offline, come passaggio all&#39;interno di un percorso. Le azioni personalizzate sono disponibili solo nei percorsi e supportano i metodi GET, PUT e POST.

<!--
| | Custom Action | Custom Channel |
| --- | --- | --- |
| **Primary use case** | Retrieve data from or send information to external systems (call centers, offline systems, logging) | Send messages to end users through channels not natively supported in [!DNL Journey Optimizer] |
| **Available in** | Journeys only | Campaigns, journeys, and orchestrated campaigns |
| **Supported HTTP methods** | GET, PUT, POST | POST only |
| **Full personalization (PE)** | No | Yes, through the personalization editor, similar to native outbound channels |
| **Visual/form editor** | No | Yes |
| **Preview and proof** | No | Yes |
| **Content experimentation** | No | Yes |
| **Targeting** | No | Yes |
| **OOTB Reporting** | Yes | Yes |
| **Multiple API credentials and channel configurations** | No | Yes |
| **RBAC/ABAC** | No | Yes |
-->

>[!TIP]
>
>Come consiglio generale, utilizza canali personalizzati per i casi di utilizzo del canale in cui invii messaggi agli utenti finali. Per altri casi d’uso simili a quelli dei connettori necessari nei percorsi, come il recupero di dati o l’attivazione di sistemi esterni, puoi continuare a utilizzare azioni personalizzate.

## Casi d’uso {#use-cases}

I canali personalizzati sono ideali per:

* **Piattaforme di messaggistica non supportate** - Canali come WeChat, Kakao Talk, Messenger, Telegram o servizi di messaggistica regionali che non dispongono di un canale [!DNL Journey Optimizer] nativo.
* **Provider di recapito personalizzati**: organizzazioni che hanno investito in un provider esterno che desiderano continuare a utilizzare per la consegna dei messaggi, ma preferiscono sfruttare [!DNL Journey Optimizer] per l&#39;orchestrazione, la personalizzazione e la gestione delle campagne.
* **Canali legacy**: gateway di messaggistica proprietari o legacy che espongono un endpoint HTTP.
* **Canali specifici del settore** - Messaggistica sicura per l&#39;assistenza sanitaria, i sistemi di avviso bancari o i servizi di notifica governativi.

## Come funziona {#how-it-works}

L’impostazione e l’utilizzo di un canale personalizzato seguono le fasi principali riportate di seguito:

1. **Configura** (Amministratore) - Un amministratore crea un canale personalizzato nel **Channel Builder**, definendo l&#39;endpoint, l&#39;autenticazione, i criteri di limitazione e la struttura del payload dei messaggi. Viene quindi creata una configurazione di canale, che viene collegata al canale personalizzato. [Ulteriori informazioni](configure-custom-channel.md)
1. **Crea** (addetto marketing): un addetto marketing aggiunge il canale personalizzato a un percorso, a una campagna o a una campagna orchestrata, seleziona una configurazione di canale e crea il payload del messaggio utilizzando l&#39;editor di personalizzazione di [!DNL Journey Optimizer]. [Ulteriori informazioni](create-custom-experience.md)
1. **Invia** - Quando un profilo è idoneo, [!DNL Journey Optimizer] invia il payload personalizzato all&#39;endpoint configurato. Il sistema esterno elabora la chiamata e consegna il messaggio.
1. **Monitoraggio** (amministratore/addetto marketing): gli amministratori e gli addetti al marketing possono monitorare le prestazioni e l&#39;affidabilità del canale personalizzato tramite le dashboard di reporting e monitoraggio di [!DNL Journey Optimizer]. [Ulteriori informazioni](monitor-custom-channel.md)

<!--
## Next steps {#next-steps}

* Review the prerequisites and permissions before setting up your first custom channel. [Learn more](custom-channel-prerequisites.md)
* Configure your first custom channel using the Channel Builder. [Learn more](custom-channel-configuration.md)
* Create a custom channel experience in a journey or campaign. [Learn more](create-custom-experience.md)
-->
