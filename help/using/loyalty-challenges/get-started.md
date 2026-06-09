---
solution: Journey Optimizer
product: journey optimizer
title: Introduzione alle sfide di fedeltà
description: Scopri come creare e gestire le sfide di fidelizzazione in Adobe Journey Optimizer per creare programmi di fidelizzazione coinvolgenti e gratificanti.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
badge: label="Beta privata" type="Informative"
mini-toc-levels: 1
exl-id: 1c84d9d0-cef7-4764-9f72-5428597a7203
feature_v2: []
subfeature_v2:
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
source-git-commit: c2322ea4081f43aadf8abc8ea9791ebcc91f78bd
workflow-type: tm+mt
source-wordcount: 900
ht-degree: 14%

---

# Introduzione alle sfide di fidelizzazione {#get-started-loyalty-challenges}

>[!BEGINSHADEBOX]

**Sommario**

**[Introduzione alle sfide di fidelizzazione](get-started.md)** ◀︎ **Sei qui**

<table style="table-layout:fixed">
<tr style="border: 0;">
<td style="vertical-align:top;">

**Crea e gestisci le sfide**

* [Accesso e gestione di sfide e attività](access-loyalty-challenges.md)
* [Creare le sfide](create-challenges.md)
* [Creare le attività](create-tasks.md)
* [Monitorare le prestazioni della sfida fedeltà](loyalty-reporting.md)

</td>
<td style="vertical-align:top;">

**Configura e integra**

* [Configurare le sfide relative alla fedeltà](loyalty-admin.md)
* [Dati e set di dati sulla fedeltà](loyalty-data-and-datasets.md)
* [Riferimento API per le sfide di fedeltà](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

</td>
</tr>
</table>

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Questa funzionalità è attualmente in **versione beta privata**. Per informazioni dettagliate sul ciclo di rilascio e sulle fasi di disponibilità, consulta [Ciclo di rilascio di Journey Optimizer](../rn/releases.md).

## Panoramica {#overview}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_inventory"
>title="Sfide fedeltà"
>abstract="Le sfide relative alla fedeltà ti consentono di creare programmi di fidelizzazione coinvolgenti e basati sulla gamification che influenzano il comportamento dei clienti e consolidano le relazioni con il brand. Crea sfide che premiano i clienti per azioni specifiche: dagli acquisti effettuati e la scrittura di recensioni, fino all’interazione sui social media ai consigli agli amici."

Le sfide relative alla fedeltà ti consentono di creare programmi di fidelizzazione coinvolgenti e basati sulla gamification che influenzano il comportamento dei clienti e consolidano le relazioni con il brand. Crea sfide che premiano i clienti per azioni specifiche: dagli acquisti effettuati e la scrittura di recensioni, fino all’interazione sui social media ai consigli agli amici.

Con Sfide di fedeltà, puoi:

* **Progetta tipi di sfida flessibili**: crea sfide standard, sequenziali o in streaming per soddisfare gli obiettivi aziendali
* **Configura i premi in modo strategico**: consegna punti alle attività cardine o al completamento completo per mantenere l&#39;impegno
* **Personalizza l&#39;esperienza**: utilizza le schede dei contenuti e la messaggistica multicanale per creare esperienze coinvolgenti e di marchio
* **Integrazione perfetta**: collegati con i provider fedeltà esistenti e sfrutta i dati di Experience Platform
* **Tieni traccia automaticamente**: monitora l&#39;avanzamento dei clienti tramite percorsi generati automaticamente senza sviluppo personalizzato
* **Misura le prestazioni**: utilizza dashboard di reporting incorporati per tenere traccia dei KPI del programma, dei risultati delle sfide e delle metriche a livello di attività

![](assets/challenges-gs.png)

Puoi creare questi tipi di esperienze di sfida:

* **Sfide standard**: i clienti completano un numero specificato di attività in qualsiasi ordine. Utilizzate questo tipo quando desiderate la flessibilità e più percorsi per il completamento.\
  *Esempio: &quot;Summer Wellness Challenge&quot; - Completa 3 attività su 5: acquistare prodotti per la salute, condividere sui social media, contattare un amico, scrivere una recensione o partecipare a un evento virtuale*

* **Sfide di Streak**: i clienti completano la stessa attività più volte consecutivamente. Utilizza questo tipo per incoraggiare un comportamento coerente e ripetuto nel tempo.\
  *Esempio: &quot;Coffee Lover&#39;s Week&quot; - Acquista prodotti a base di caffè per 7 giorni consecutivi per sbloccare un premio per bevande gratuite*

* **Sfide sequenziali**: i clienti completano le attività in un ordine definito. Utilizza questo tipo di guida per i clienti attraverso un percorso specifico o un processo di onboarding.\
  *Esempio: &quot;Nuovo Percorso membro&quot; - Iscriviti alle e-mail → Effettua il tuo primo acquisto → Scrivi una recensione del prodotto → Fai riferimento a un amico (completa nell&#39;ordine esatto)*

* **Problemi relativi ai dati** (disponibilità limitata): il framework delle sfide (attività e premi) viene assemblato dall&#39;integrazione dei dati delle sfide di fidelizzazione. Puoi configurare Impostazioni, Contenuto e Messaggistica come faresti per qualsiasi altro tipo di sfida.

## Come funziona {#how-it-works}

La creazione e il lancio di una sfida di fidelizzazione segue questo flusso di lavoro:

1. **Crea una sfida** - Scegli il tipo di sfida (Standard, Streak, Sequenziale o Includi i tuoi dati quando disponibili). [Scopri come scegliere un tipo di sfida](create-challenges.md#create-the-challenge).

1. **Configura impostazioni** - Nella scheda Impostazioni, definisci i dettagli della richiesta di verifica, il pubblico, la pianificazione, le regole (consenso, tracciamento dell&#39;avanzamento, limiti di ripetizione) e i metadati facoltativi. [Informazioni sulle impostazioni di verifica](create-challenges.md#settings).

1. **Aggiungi attività e premi** - Nella scheda Struttura, definisci attività e premi (non necessari per risolvere i problemi relativi ai dati).

1. **Progetta schede di contenuto** - Crea la rappresentazione visiva della tua sfida utilizzando le schede di contenuto Journey Optimizer visualizzate sui dispositivi dei clienti.

1. **Configurazione della messaggistica** (facoltativo): configurazione di messaggi multicanale (in-app, e-mail, push) per le fasi principali del ciclo di vita: avvio, in corso e completamento.

1. **Avvia la sfida** - Pubblica la sfida, quindi genera un percorso. Journey Optimizer crea automaticamente il percorso per la sfida. Pubblica il percorso generato automaticamente per rendere la sfida disponibile ai clienti.

Per istruzioni dettagliate, consulta [Creare le sfide](create-challenges.md).

## Prerequisiti {#prerequisites}

Prima di utilizzare le sfide di fedeltà, assicurati di disporre di:

+++Autorizzazioni richieste

Per utilizzare le sfide di fidelizzazione, è necessario disporre delle autorizzazioni appropriate in Journey Optimizer e Adobe Experience Platform.

**Journey Optimizer:**

* `journeys.read`
* `journeys.write`
* `journeys.delete`
* `journeys.publish`
* `journeys_events.read`
* `journeys_events.write`
* `journeys_events.delete`
* `journeys_report.read`
* `messages.read`
* `messages_report.read`

**Adobe Experience Platform:**

* `segments.read`
* `profiles.read`
* `identity_namespace.read`

Se non riesci ad accedere alla funzione o se hai bisogno di autorizzazioni aggiuntive, contatta l’amministratore.

+++

+++Configurare il programma fedeltà (amministratori)

Gli amministratori configurano i provider di premi, le definizioni degli eventi, l&#39;inventario dei prodotti, le esclusioni e le impostazioni globali nel menu **[!UICONTROL Amministratore fedeltà]**. Gli addetti al marketing che creano solo problemi non devono accedere a questo menu. [Scopri come configurare le sfide relative alla fedeltà](loyalty-admin.md)

Contatta l&#39;amministratore se il menu **[!UICONTROL Amministratore fedeltà]** non è visibile nel menu di navigazione a sinistra.

+++

+++Pubblico target

Assicurati che il pubblico di destinazione di cui hai bisogno esista in Adobe Experience Platform prima di creare la tua sfida. Durante la configurazione della sfida, seleziona il pubblico che definisce quali clienti sono idonei a partecipare. [Scopri come utilizzare i tipi di pubblico](../audience/about-audiences.md).

+++

## Argomenti di approfondimento {#lets-dive-deeper}

Ora che sai cosa sono le sfide della fedeltà e come funzionano, è il momento di entrare nei dettagli. Esplora i seguenti argomenti per accedere all’interfaccia, creare la prima sfida e definire le attività che i clienti completeranno.

<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <a href="access-loyalty-challenges.md">
      <img alt="Accesso" src="assets/do-not-localize/icon-access.png" width="200"/>
    </a>
    <div>
    <a href="access-loyalty-challenges.md"><strong>Accesso e gestione di attività e sfide</strong></a>
    </div>
    <p>
    <em>Scopri come accedere all'inventario e gestire sfide e attività</em>
    </p>
  </td>
  <td>
    <a href="create-challenges.md">
      <img alt="Creare" src="assets/do-not-localize/icon-challenge.png" width="200"/>
    </a>
    <div>
    <a href="create-challenges.md"><strong>Creare le sfide</strong></a>
    </div>
    <p>
    <em>Scopri come creare e configurare la tua prima sfida fedeltà</em>
    </p>
  </td>
  <td>
    <a href="create-tasks.md">
      <img alt="Attività" src="assets/do-not-localize/icon-task.png" width="200"/>
    </a>
    <div>
    <a href="create-tasks.md"><strong>Creare le attività</strong></a>
    </div>
    <p>
    <em>Scopri come definire le attività completate dai clienti per le sfide</em>
    </p>
  </td>
  <td>
    <a href="loyalty-reporting.md">
      <img alt="Rapporti" src="assets/do-not-localize/icon-reporting.png" width="200"/>
    </a>
    <div>
    <a href="loyalty-reporting.md"><strong>Monitoraggio delle prestazioni</strong></a>
    </div>
    <p>
    <em>Tieni traccia di KPI del programma, risultati della sfida e metriche delle attività con dashboard incorporati</em>
    </p>
  </td>
  <!--
    <a href="loyalty-admin.md"><strong>Configure the loyalty program</strong></a>
  <td>
    <a href="loyalty-admin.md">
    <em>Set up reward providers, event definitions, and org settings for fulfillment</em>
    </a>
    <div>
  -->
    <a href="loyalty-admin.md"><strong>Configurare le sfide relative alla fedeltà</strong></a>
    </div>
    <p>
    <em>Imposta i provider di premi, le definizioni degli eventi e le impostazioni dell'organizzazione</em>
    </p>
  </td>
</tr>
</table>

## Documentazione delle API {#api-reference}

Per gestire le sfide di fidelizzazione a livello di programmazione, utilizza l&#39;API [Sfide di fedeltà](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}. L’API consente di creare, aggiornare e gestire le sfide e le attività tramite endpoint REST.
