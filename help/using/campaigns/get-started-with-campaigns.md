---
solution: Journey Optimizer
product: journey optimizer
title: Introduzione alle campagne
description: Ulteriori informazioni sulle campagne in Journey Optimizer
feature: Campaigns
topic: Content Management
role: User
level: Beginner
mini-toc-levels: 1
keywords: campagna, come fare, inizio, optimizer
exl-id: e2506a43-e4f5-48af-bd14-ab76c54b7c90
source-git-commit: efb943e5a6f27becc6e8b6128b776e46d6141823
workflow-type: tm+mt
source-wordcount: '931'
ht-degree: 95%

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
>abstract="Imposta il controllo della frequenza della tua campagna specificando i limiti di frequenza desiderati. Questa funzione è particolarmente utile per prevenire il sovraccarico sui sistemi a valle, come le pagine di destinazione o le piattaforme di assistenza clienti."

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
>abstract="Seleziona il tipo di campagna. I canali disponibili variano a seconda del tipo selezionato. <br>**Campagne pianificate** (campagne di azione): ideali per comunicazioni batch semplici e una tantum che puoi pianificare per essere eseguite in un momento specifico.<br>**Campagne attivate da API**: vengono attivate tramite una chiamata API e abilitano la messaggistica automatizzata basata su eventi direttamente da sistemi esterni.<br>**Campagne orchestrate**: forniscono un’area di lavoro visiva e basata su trascinamento per progettare e automatizzare flussi di lavoro di marketing complessi e in più passaggi, dalla segmentazione del pubblico alla consegna personalizzata dei messaggi su tutti i canali."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_orchestration"
>title="Campagne"
>abstract="Crea il flusso di segmentazione, definisci i messaggi cross-channel e pianifica le campagne. Canali supportati: e-mail, SMS, notifiche push."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_scheduled_marketing"
>title="Campagne"
>abstract="Consegne in uscita singole o ricorrenti o azioni in entrata continue."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_scheduled_transactional"
>title="Campagne"
>abstract="Consegna di azioni transazionali in uscita singole o ricorrenti."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_api_marketing"
>title="Campagne"
>abstract="Consegna di comunicazioni di marketing personalizzate a un pubblico target. Canali supportati: e-mail, SMS, notifiche push."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_api_transactional"
>title="Campagne"
>abstract="Consegna di comunicazioni transazionali a singoli profili o a set di profili. Canali supportati: e-mail, SMS, notifiche push."

Utilizza campagne [!DNL Journey Optimizer] per distribuire contenuti una tantum a un pubblico specifico su più canali. A differenza dei percorsi, che eseguono le azioni passaggio dopo passaggio, le campagne eseguono le azioni in maniera simultanea, immediatamente o secondo una pianificazione definita.

![](assets/gs-campaigns.png)

## Tipi di campagna

[!DNL Journey Optimizer] supporta tre tipi di campagna. Ogni tipo si adatta a casi d’uso diversi e supporta canali diversi. Per ulteriori informazioni sui canali disponibili con ciascun tipo di campagna, consulta la tabella in questa sezione: [Canali in percorsi e campagne](../channels/gs-channels.md#channels)

![](assets/campaign-modal.png)

>[!BEGINTABS]

>[!TAB Campagne orchestrate]

L’**orchestrazione delle campagne** potenzia campagne di marketing sofisticate e avviate dal brand su tutti i canali, aiutandoti a incrementare il coinvolgimento, i ricavi e la fidelizzazione della clientela su larga scala.

Anche se il marketing cross-channel è essenziale, le campagne orchestrate lo rendono semplice. Grazie a un’interfaccia visiva basata su un trascinamento, puoi progettare e automatizzare flussi di lavoro di marketing complessi, dalla segmentazione alla consegna dei messaggi, su più canali. Tutto avviene in un ambiente intuitivo, progettato per velocità, controllo ed efficienza.

➡️ [Scopri come utilizzare le campagne orchestrate](../orchestrated/gs-orchestrated-campaigns.md).

>[!TAB Campagne azione (o campagne pianificate)]

Le **campagne di azione**, note anche come campagne pianificate, consentono semplici comunicazioni batch ad hoc.

* **Pianificata - Marketing**: per casi d’uso di marketing come offerte promozionali, campagne di coinvolgimento, annunci, note legali o aggiornamenti dei criteri. Richiede il consenso dei destinatari.
* **Pianificata - Transazionale**: a differenza delle campagne di marketing, le campagne transazionali non richiedono il consenso dei destinatari. Utilizza questa categoria per le comunicazioni relative a interruzioni, emergenze, cancellazioni. Canali supportati: e-mail, SMS, notifiche push.

➡️ [Scopri come utilizzare le campagne di azione](create-campaign.md)

>[!TAB Campagne attivate da API]

Le **campagne attivate da API** consentono di attivare l’esecuzione della campagna tramite una chiamata API. Queste comunicazioni possono essere inviate quando è necessario applicare la personalizzazione non solo tramite attributi di profilo (come per il ripristino della password), ma anche tramite dati contestuali in tempo reale presenti nel trigger, che è un payload dell’API REST.

* **Attivata da API - Marketing**: invia comunicazioni di marketing personalizzate a tipi di pubblico mirati.
* **Attivata da API - Transazionale**: invia messaggi in seguito a un’azione eseguita da un singolo utente come richiesta di reimpostazione della password, acquisto dal carrello, ecc.

➡️ [Scopri come utilizzare le campagne attivate da API](api-triggered-campaigns.md)


>[!ENDTABS]

## Prerequisiti {#prerequisites}

Prima di utilizzare le campagne, assicurati di aver rivisto i prerequisiti di seguito.

* I **tipi di pubblico** devono essere disponibili prima di creare la campagna. [Introduzione ai tipi di pubblico](../audience/about-audiences.md).

* **Configurazione dei canali**: per poter selezionare un canale, è necessario che la configurazione dei canali corrispondente (ovvero, predefinita) sia stata creata e che sia disponibile. [Scopri come impostare la configurazione di canale](../configuration/channel-surfaces.md).

* **Autorizzazioni**: le campagne sono disponibili solo per gli utenti con le autorizzazioni appropriate elencate di seguito. Se non riesci ad accedere alle funzionalità delle campagne, contatta l’amministratore per richiedere le autorizzazioni necessarie. [Ulteriori informazioni sui ruoli incorporati di Journey Optimizer](../administration/ootb-product-profiles.md)

  | Tipo di campagna | Autorizzazioni |
  |----------------------------|----------------------------------------------------------------------------|
  | **Campagne di azione** | Amministratore campagna<br>Approvatore campagna<br>Responsabile campagna<br>Visualizzatore campagna |
  | **Campagne attivate da API** | Amministratore campagna<br>Approvatore campagna<br>Responsabile campagna<br>Visualizzatore campagna |
  | **Campagne orchestrate** | Amministratore campagna orchestrata<br>Approvatore campagna orchestrata<br>Responsabile campagna orchestrata<br>Visualizzatore campagna orchestrata |

  +++Scopri come assegnare un ruolo relativo alla campagna

   1. Per assegnare un ruolo a un utente nel prodotto [!DNL Permissions], passa alla scheda **[!UICONTROL Ruoli]** e seleziona uno dei **[!UICONTROL Ruoli]** incorporati relativi alle campagne.

   1. Dalla scheda **[!UICONTROL Utenti]**, fai clic su **[!UICONTROL Aggiungi utente]**.

   1. Digita il nome o l’indirizzo e-mail dell’utente o selezionalo dall’elenco e fai clic su **[!UICONTROL Salva]**.

      Se l&#39;utente non è stato creato in precedenza, consulta la [documentazione sull&#39;aggiunta di utenti](https://experienceleague.adobe.com/it/docs/experience-platform/access-control/ui/users){target="_blank"}


  L’utente dovrebbe quindi ricevere un messaggio e-mail di reindirizzamento all’istanza.

  +++

## Approfondiamo

Ora che conosci le campagne in [!DNL Journey Optimizer], è il momento di approfondire queste sezioni della documentazione per iniziare a creare le prime campagne.

<table style="table-layout:fixed"><tr style="border: 0; text-align: center;">
<td><a href="create-campaign.md"><img width="70%" alt="campagne di azione" src="assets/do-not-localize/gs-action-campaign.png"></a><br/><a href="create-campaign.md">Campagne di azione</a></td>
<td><a href="api-triggered-campaigns.md"><img width="70%" alt="SMS" src="assets/do-not-localize/gs-api-triggered-campaign.png"></a><br/><a href="api-triggered-campaigns.md">Campagne attivate da API</a></td>
<td><a href="../orchestrated/gs-orchestrated-campaigns.md"><img width="70%" alt="push" src="assets/do-not-localize/gs-orchestrated-campaign.png"></a><a href="../orchestrated/gs-orchestrated-campaigns.md">Campagne orchestrate</a></td>
</tr></table>
