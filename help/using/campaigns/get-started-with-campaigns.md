---
solution: Journey Optimizer
product: journey optimizer
title: Introduzione alle campagne
description: Ulteriori informazioni sulle campagne in Journey Optimizer
feature: Campaigns
topic: Content Management
role: User
level: Beginner
keywords: campagna, come fare, inizio, optimizer
exl-id: e2506a43-e4f5-48af-bd14-ab76c54b7c90
source-git-commit: d07d4c2001bd9e9d08539788073757bc1034c9ec
workflow-type: tm+mt
source-wordcount: '750'
ht-degree: 89%

---

# Introduzione alle campagne {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule"
>title="Pianificazione della campagna"
>abstract="Per impostazione predefinita, le campagne iniziano al momento dell’attivazione manuale e terminano immediatamente dopo l’invio del messaggio. Puoi impostare una data e un’ora specifiche per l’invio del messaggio. Inoltre, puoi specificare una data di fine per le campagne di azione ricorrenti. Nei trigger di Azione, puoi anche configurare la frequenza di invio del messaggio in base alle tue preferenze."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_start"
>title="Inizio della campagna"
>abstract="Specifica la data e l’ora in cui il messaggio deve essere inviato."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_end"
>title="Fine della campagna"
>abstract="Specifica quando interrompere l’esecuzione di una campagna ricorrente."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_triggers"
>title="Trigger delle azioni della campagna"
>abstract="Definisci la frequenza con cui deve essere inviato il messaggio della campagna."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_throttling"
>title="Controllo della frequenza"
>abstract="Imposta il controllo della frequenza per la campagna specificando i limiti della frequenza desiderati. Questa funzione è particolarmente utile per prevenire il sovraccarico sui sistemi a valle, come le pagine di destinazione o le piattaforme di assistenza clienti."

>[!CONTEXTUALHELP]
>id="ajo_homepage_card3"
>title="Creare le campagne"
>abstract="Utilizza **Adobe Journey Optimizer** per distribuire contenuti una tantum a un pubblico specifico utilizzando vari canali. Quando si utilizzano i percorsi, le azioni vengono eseguite in sequenza. Con le campagne, le azioni vengono eseguite simultaneamente, immediatamente o in base a una pianificazione specifica."

>[!CONTEXTUALHELP]
>id="campaigns_list"
>title="Campagne"
>abstract="Crea campagne per distribuire contenuti una tantum a un pubblico specifico su vari canali. Prima di creare una campagna, accertati di avere una configurazione dei canali e un pubblico di Adobe Experience Platform pronti per l’uso."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_type"
>title="Tipo di campagna"
>abstract="Seleziona il tipo di campagna. I canali disponibili variano a seconda del tipo selezionato. <br>**Campagne pianificate** (campagne azioni): ideale per comunicazioni in batch semplici e una tantum che puoi pianificare per essere eseguite in un momento specifico.<br>**Campagne attivate da API** - Attivate tramite una chiamata API, abilitando la messaggistica automatizzata basata su eventi direttamente da sistemi esterni.<br>**Campagne orchestrate**: fornisci un&#39;area di lavoro visiva e trascinata per progettare e automatizzare flussi di lavoro di marketing complessi e in più passaggi, dalla segmentazione del pubblico alla consegna personalizzata dei messaggi tra i canali."

Utilizza le campagne Journey Optimizer per distribuire contenuti una tantum a un pubblico specifico utilizzando vari canali. Quando si utilizzano i percorsi, le azioni vengono eseguite in sequenza. Con le campagne, le azioni vengono eseguite simultaneamente, immediatamente o in base a una pianificazione specifica.

![](assets/gs-campaigns.png)

Puoi creare diversi tipi di campagne in Journey Optimizer:

* **Campagne di azione**

  Le campagne di azione (o campagne pianificate) consentono comunicazioni batch semplici ad hoc per casi d’uso di marketing come offerte promozionali, campagne di coinvolgimento, annunci, avvisi legali o aggiornamenti dei criteri.

* **Campagne attivate da API**

  Le campagne attivate da API consentono di inviare comunicazioni di marketing a un pubblico al momento giusto oppure messaggi operativi o transazionali a singoli utenti, ad esempio per la reimpostazione della password. Possono includere la personalizzazione basata non solo sugli attributi del profilo, ma anche sui dati contestuali in tempo reale presenti nel trigger, che è un payload API REST.

* **Campagne orchestrate**

  L’orchestrazione delle campagne in Adobe Journey Optimizer potenzia campagne di marketing sofisticate e avviate dal brand su tutti i canali, aiutandoti a incrementare il coinvolgimento, i ricavi e la fidelizzazione della clientela su larga scala.

  Anche se il marketing cross-channel è essenziale, le campagne orchestrate lo rendono semplice. Grazie a un’interfaccia visiva basata su un trascinamento, puoi progettare e automatizzare flussi di lavoro di marketing complessi, dalla segmentazione alla consegna dei messaggi, su più canali. Tutto avviene in un ambiente intuitivo, progettato per velocità, controllo ed efficienza.

## Prerequisiti {#prerequisites}

Prima di creare la campagna, assicurati di aver rivisto i prerequisiti di seguito.

### Autorizzazioni

Le campagne sono disponibili solo per gli utenti con le autorizzazioni appropriate elencate di seguito. [Ulteriori informazioni sui ruoli incorporati di Journey Optimizer](../administration/ootb-product-profiles.md)

>[!BEGINTABS]

>[!TAB Campagne di azione]

Amministratore campagna
Approvatore campagna
Responsabile campagna
Visualizzatore campagna

>[!TAB Campagne attivate da API]

Amministratore campagna
Approvatore campagna
Responsabile campagna
Visualizzatore campagna

>[!TAB Campagne orchestrate]

Amministratore campagna orchestrata
Approvatore campagna orchestrata
Responsabile campagna orchestrata
Visualizzatore campagna orchestrata

>[!ENDTABS]

Se non riesci ad accedere alle funzionalità delle campagne, contatta l’amministratore per richiedere le autorizzazioni necessarie.

+++Scopri come assegnare il ruolo correlato alla campagna

1. Per assegnare un ruolo a un utente nel prodotto [!DNL Permissions], passa alla scheda **[!UICONTROL Ruoli]** e seleziona uno dei **[!UICONTROL Ruoli]** incorporati relativi alle campagne.

1. Dalla sezione **[!UICONTROL Utenti]**, fai clic su **[!UICONTROL Aggiungi utente]**.

1. Digita il nome o l’indirizzo e-mail dell’utente o selezionalo dall’elenco e fai clic su **[!UICONTROL Salva]**.

   Se l’utente non è stato creato in precedenza, consulta la [documentazione Aggiungere utenti](https://experienceleague.adobe.com/it/docs/experience-platform/access-control/ui/users).

L’utente dovrebbe quindi ricevere un messaggio e-mail di reindirizzamento all’istanza.

+++

### Pubblico

I tipi di pubblico devono essere disponibili prima di creare la campagna. [Introduzione ai tipi di pubblico](../audience/about-audiences.md)

### Configurazione dei canali

Per poter selezionare un canale, è necessario che la configurazione dei canali corrispondente (ovvero, preimpostata) sia creata e disponibile. [Scopri come impostare la configurazione di canale](../configuration/channel-surfaces.md).

## Approfondiamo

Ora che conosci le campagne in [!DNL Journey Optimizer], è il momento di approfondire queste sezioni della documentazione per iniziare a creare le prime campagne.

<table style="table-layout:fixed"><tr style="border: 0; text-align: center;">
<td><a href="create-campaign.md"><img width="70%" alt="campagne di azione" src="assets/do-not-localize/gs-action-campaign.png"></a><br/><a href="create-campaign.md">Campagne di azione</a></td>
<td><a href="api-triggered-campaigns.md"><img width="70%" alt="SMS" src="assets/do-not-localize/gs-api-triggered-campaign.png"></a><br/><a href="api-triggered-campaigns.md">Campagne attivate da API</a></td>
<td><a href="../orchestrated/gs-orchestrated-campaigns.md"><img width="70%" alt="push" src="assets/do-not-localize/gs-orchestrated-campaign.png"></a><a href="../orchestrated/gs-orchestrated-campaigns.md">Campagne orchestrate</a></td>
</tr></table>
