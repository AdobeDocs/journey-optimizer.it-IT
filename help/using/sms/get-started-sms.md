---
solution: Journey Optimizer
product: journey optimizer
title: Introduzione ai messaggi di testo (SMS/MMS/RCS)
description: Scopri come creare e inviare messaggi di testo in Journey Optimizer
feature: SMS
topic: Content Management
role: User
level: Beginner
exl-id: c1027268-0bbe-4e35-a5a6-2aef78083dd3
source-git-commit: 243d4e74c15057bc4bd334876a1bc87969d396e0
workflow-type: tm+mt
source-wordcount: '812'
ht-degree: 27%

---

# Introduzione agli SMS {#get-started-sms}

Utilizza [!DNL Journey Optimizer] per inviare messaggi di testo (SMS/MMS/RCS) alla clientela sui loro dispositivi mobili. Puoi creare, personalizzare e visualizzare in anteprima i messaggi in formato testo dall’editor SMS/MMS/RCS.

I messaggi di testo possono essere creati e inviati in un percorso o in una campagna. Per SMS, MMS e RCS utilizza l’azione SMS.

* In un **percorso**. Crea un percorso, aggiungi un’attività SMS e definisci le impostazioni di base. Quindi, passa al riquadro Azioni SMS a destra per creare il contenuto per il messaggio SMS, MMS o RCS. [Scopri come creare un percorso](../building-journeys/journey-gs.md)

* In una **campagna**. Crea una campagna, seleziona SMS come azione e definisci le impostazioni di base. Quindi, modifica il contenuto del messaggio per definire il messaggio SMS, MMS o RCS da inviare. [Scopri come creare una campagna](../campaigns/create-campaign.md#configure)

>[!IMPORTANT]
>
>Se è la prima volta che crei messaggi di testo, assicurati che il canale SMS sia stato configurato. [Ulteriori informazioni](sms-configuration.md)

## Funzionalità di messaggistica di testo {#sms-capabilities}

Adobe Journey Optimizer fornisce funzionalità di messaggistica di testo complete per coinvolgere i clienti su più canali:

**SMS (Short Message Service)**

Inviare messaggi di solo testo composti da un massimo di 160 caratteri. Gli SMS sono il formato di messaggistica di testo più ampiamente supportato su tutti i dispositivi mobili.

**MMS (Servizio messaggi multimediali)**

Migliora la comunicazione con contenuti multimediali, inclusi video, immagini, clip audio e GIF. Oltre ai file multimediali, i messaggi MMS possono contenere un massimo di 1600 caratteri di testo. [Ulteriori informazioni sulle limitazioni di MMS](../start/guardrails.md#sms-guardrails)

**RCS (Rich Communication Services)**

Inviare messaggi interattivi e con marchio, con funzioni avanzate quali caroselli, schede ricche, azioni suggerite e supporto multimediale avanzato. RCS offre un’esperienza di messaggistica più completa sui dispositivi supportati.

## Funzioni chiave {#key-features}

**Personalization e contenuti dinamici**

Crea messaggi di testo personalizzati utilizzando l’editor di personalizzazione. Aggiungi attributi di profilo, contenuto condizionale e dati dinamici per adattare i messaggi ai singoli destinatari. [Informazioni sulla personalizzazione](../personalization/personalize.md)

**Supporto di più provider**

Adobe Journey Optimizer si integra con i principali provider di servizi SMS:

* **Sinch** - [Guida alla configurazione](sms-configuration-sinch.md)
* **Twilio** - [Guida alla configurazione](sms-configuration-twilio.md)
* **Infobip** - [Guida alla configurazione](sms-configuration-infobip.md)
* **Provider personalizzati** - Configura qualsiasi altro provider SMS utilizzando l&#39;integrazione API personalizzata. [Ulteriori informazioni](sms-configuration-custom.md)

**Riduzione e monitoraggio URL**

Aggiungi URL abbreviati e tracciabili ai messaggi per monitorare il coinvolgimento. Per la funzionalità di abbreviazione URL è necessaria la configurazione del sottodominio. [Scopri come configurare i sottodomini SMS](sms-subdomains.md)

**Gestione rinuncia**

Garantire la conformità agli standard e alle normative di settore tramite la gestione integrata delle rinunce. Journey Optimizer gestisce automaticamente le parole chiave di rinuncia standard (STOP, QUIT, CANCEL, ecc.) per i provider Sinch e Infobip. [Informazioni sulla gestione delle rinunce](sms-opt-out.md)

**Anteprima e test**

Verifica i messaggi di testo prima di inviarli utilizzando profili di test e dati di esempio. Visualizza in anteprima personalizzazione, contenuto e formattazione per garantire la corretta visualizzazione dei messaggi. [Scopri come inviare messaggi](send-sms.md)

**Reporting e analisi**

Monitora le prestazioni delle campagne e dei percorsi SMS con funzionalità di reporting complete:

* [Rapporti sulla campagna SMS](../reports/campaign-global-report-cja-sms.md)
* [Rapporti sul percorso SMS](../reports/journey-global-report-cja-sms.md)

## Requisiti di configurazione {#configuration-requirements}

Prima di inviare messaggi di testo, è necessario:

1. **Scegli un provider SMS** - Seleziona da Sinch, Twilio, Infobip o configura un provider personalizzato
2. **Configura credenziali API** - Integra i token API e gli ID servizio del provider con Journey Optimizer
3. **Crea configurazioni canale** - Configura configurazioni SMS per messaggi di marketing e messaggi transazionali
4. **Configura sottodomini (facoltativo)** - Obbligatorio solo se intendi utilizzare la riduzione degli URL nei messaggi

Questi passaggi di configurazione vengono in genere eseguiti da un amministratore di sistema. [Introduzione alla configurazione SMS](sms-configuration.md)

## Guida introduttiva {#quick-start}

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="sms-configuration.md">
<img alt="Convalida" src="../assets/do-not-localize/sms-config.jpg">
</a>
<div>
<a href="sms-configuration.md"><strong>Configurare il canale SMS</strong></a>
</div>
<p>Configurare il provider SMS e le configurazioni del canale</p>
</td>
<td>
<a href="create-sms.md">
<img alt="Lead" src="../assets/do-not-localize/sms-create.jpeg">
</a>
<div><a href="create-sms.md"><strong>Crea un messaggio di testo</strong></a>
</div>
<p>Progettare e personalizzare i contenuti di SMS, MMS o RCS</p>
</td>
<td>
<a href="send-sms.md">
<img alt="Non frequente" src="../assets/do-not-localize/sms-sending.jpg">
</a>
<div>
<a href="send-sms.md"><strong>Anteprima e invio</strong></a>
</div>
<p>Testare e inviare messaggi di testo al pubblico</p>
</td>
<td>
<a href="sms-opt-out.md">
<img alt="Convalida" src="../assets/do-not-localize/sms-opt-out.jpg">
</a>
<div>
<a href="sms-opt-out.md"><strong>Gestione rinunce</strong></a>
</div>
<p>Gestire le richieste di annullamento dell’iscrizione e garantire la conformità</p>
</td>
</tr></table>

## Risorse aggiuntive {#additional-resources}

Per ulteriori informazioni sui messaggi di testo in Journey Optimizer, consulta gli argomenti riportati di seguito.

+++Guide alla configurazione

Scopri come impostare e configurare l’ambiente SMS:

* [Panoramica sulla configurazione del canale SMS](sms-configuration.md)
* [Creare configurazioni del canale SMS](sms-configuration-surface.md)
* [Configurare i sottodomini SMS per l’abbreviazione degli URL](sms-subdomains.md)

+++

+++Guide alla configurazione del provider

Configurazione dettagliata per ogni provider di servizi SMS:

* [Configurare il provider Sinch](sms-configuration-sinch.md)
* [Configurare il provider Twilio](sms-configuration-twilio.md)
* [Configurare il provider Infobip](sms-configuration-infobip.md)
* [Configurare il provider SMS personalizzato](sms-configuration-custom.md)

+++

+++Creazione e gestione dei contenuti

Crea, personalizza e gestisci il contenuto dei messaggi di testo:

* [Creare messaggi SMS/MMS](create-sms.md)
* [Anteprima, test e invio di messaggi](send-sms.md)
* [Personalization nei messaggi di testo](../personalization/personalize.md)
* [Contenuto dinamico](../personalization/get-started-dynamic-content.md)

+++

+++Conformità e privacy

Assicurati che i messaggi di testo siano conformi alle normative e agli standard sulla privacy:

* [Gestione degli opt-out](sms-opt-out.md)
* [Privacy e consenso](../privacy/opt-out.md#sms-opt-out-management-sms-opt-out-management)

+++

+++Tracciamento delle prestazioni

Monitora e analizza le campagne SMS e le prestazioni del percorso:

* [Rapporti sulla campagna SMS](../reports/campaign-global-report-cja-sms.md)
* [Rapporti sul percorso SMS](../reports/journey-global-report-cja-sms.md)

+++

+++Integrazione di Percorsi e Campaign

Scopri come incorporare gli SMS nei percorsi e nelle campagne dei clienti:

* [Aggiungere messaggi SMS ai percorsi](../building-journeys/journeys-message.md)
* [Creare campagne SMS](../campaigns/create-campaign.md)

+++

## Video sulle procedure {#videos}

**Configurare e inviare messaggi SMS**

Scopri come configurare, creare e includere la messaggistica SMS nei tuoi percorsi cliente.

+++Guarda il video

>[!VIDEO](https://video.tv.adobe.com/v/3422695?captions=ita&learn=on)

+++

**Esplora le funzionalità di messaggistica mobile**

Scopri le funzionalità complete di messaggistica mobile offerte da Adobe Journey Optimizer agli esperti di marketing.

+++Guarda il video

>[!VIDEO](https://video.tv.adobe.com/v/3430373?captions=ita&quality=12&learn=on)

+++

**Inviare messaggi RCS con marchio**

Scopri come configurare e inviare messaggi RCS interattivi e in linea con il brand in Adobe Journey Optimizer utilizzando un provider SMS personalizzato.

+++Guarda il video

>[!VIDEO](https://video.tv.adobe.com/v/3464763?captions=ita)

+++

**Argomenti correlati**

* [Aggiungere messaggi nei percorsi](../building-journeys/journeys-message.md)
* [Creare campagne di marketing](../campaigns/create-campaign.md)
* [Guardrail e limitazioni](../start/guardrails.md#sms-guardrails)
