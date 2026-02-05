---
solution: Journey Optimizer
product: journey optimizer
title: Introduzione alle sfide di fedeltà
description: Scopri come creare e gestire le sfide di fidelizzazione in Adobe Journey Optimizer per creare programmi di fidelizzazione coinvolgenti.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta privata" type="Informative"
mini-toc-levels: 1
source-git-commit: 5e11a0817ef6d1c7ef2e363cde48cddf932cd2c1
workflow-type: tm+mt
source-wordcount: '650'
ht-degree: 1%

---


# Introduzione alle sfide di fedeltà {#get-started-loyalty-challenges}

>[!AVAILABILITY]
>
>Questa funzionalità è attualmente in **versione beta privata** e potrebbe non essere disponibile nel tuo ambiente. Per richiedere l’accesso, contatta il rappresentante Adobe. Ulteriori informazioni sulle [etichette di disponibilità](../rn/releases.md#availability-labels).

>[!BEGINSHADEBOX]

**Documentazione sulle sfide di fedeltà:**

* **Introduzione alle sfide di fidelizzazione** ◀︎ **Sei qui**
* [Accesso e gestione di sfide e attività](access-loyalty-challenges.md)
* [Creare le sfide](create-challenges.md)
* [Creare le attività](create-tasks.md)

>[!ENDSHADEBOX]

## Panoramica {#overview}

Le sfide relative alla fedeltà consentono di creare programmi di fidelizzazione coinvolgenti e diversificati che guidano il comportamento dei clienti e approfondiscono le relazioni con il marchio. Crea sfide che premiano i clienti per azioni specifiche, dall&#39;effettuare acquisti e scrivere recensioni a coinvolgere sui social media e gli amici di riferimento.

Con Sfide di fedeltà, puoi:

* **Progetta tipi di sfida flessibili**: crea sfide standard, sequenziali o in streaming per soddisfare gli obiettivi aziendali
* **Configura i premi in modo strategico**: consegna punti alle attività cardine o al completamento completo per mantenere l&#39;impegno
* **Personalizza l&#39;esperienza**: utilizza le schede dei contenuti e la messaggistica multicanale per creare esperienze coinvolgenti e di marchio
* **Integrazione perfetta**: collegati con i provider fedeltà esistenti e sfrutta i dati di Experience Platform
* **Tieni traccia automaticamente**: monitora l&#39;avanzamento dei clienti tramite percorsi generati automaticamente senza sviluppo personalizzato

![](assets/challenges-gs.png)

Puoi creare tre tipi di esperienze di sfida:

* **Sfide standard**: i clienti completano un numero specificato di attività in qualsiasi ordine. Utilizzate questo tipo quando desiderate la flessibilità e più percorsi per il completamento.\
  *Esempio: &quot;Summer Wellness Challenge&quot; - Completa 3 attività su 5: acquistare prodotti per la salute, condividere sui social media, contattare un amico, scrivere una recensione o partecipare a un evento virtuale*

* **Sfide di Streak**: i clienti completano la stessa attività più volte consecutivamente. Utilizza questo tipo per incoraggiare un comportamento coerente e ripetuto nel tempo.\
  *Esempio: &quot;Coffee Lover&#39;s Week&quot; - Acquista prodotti a base di caffè per 7 giorni consecutivi per sbloccare un premio per bevande gratuite*

* **Sfide sequenziali**: i clienti completano le attività in un ordine definito. Utilizza questo tipo di guida per i clienti attraverso un percorso specifico o un processo di onboarding.\
  *Esempio: &quot;Nuovo Percorso membro&quot; - Iscriviti alle e-mail → Effettua il tuo primo acquisto → Scrivi una recensione del prodotto → Fai riferimento a un amico (completa nell&#39;ordine esatto)*

## Come funziona {#how-it-works}

La creazione e il lancio di una sfida di fidelizzazione segue questo flusso di lavoro:

1. **Configura l&#39;acquisizione dei dati**. Configura i connettori di origine di Experience Platform (ad esempio il [connettore capillare](https://experienceleague.adobe.com/en/docs/experience-platform/sources/home#loyalty)) per acquisire i dati dell&#39;evento fedeltà che tengono traccia delle azioni e dell&#39;avanzamento dei clienti. Questi dati consentono il rilevamento delle sfide e il completamento delle attività.

1. **Crea una sfida** - Definisci le proprietà della sfida di base, tra cui nome, tipo (Standard, Streak o Sequenziale) e intervallo di date.

1. **Aggiungi attività** - Definisci le azioni specifiche che i clienti devono completare, inclusi i tipi di attività (acquisto, spesa), le quantità, i filtri dei prodotti e i premi.

1. **Progetta schede di contenuto** - Crea la rappresentazione visiva della tua sfida utilizzando le schede di contenuto Journey Optimizer visualizzate sui dispositivi dei clienti. Le schede dei contenuti mostrano informazioni sulla sfida, l’avanzamento e i premi.

1. **Configurazione della messaggistica** (facoltativo): configurazione di messaggi multicanale (in-app, e-mail, push) per le fasi principali del ciclo di vita: avvio, in corso e completamento.

1. **Seleziona il pubblico di destinazione** - Definisci quali clienti possono partecipare alla tua sfida selezionando un pubblico da Adobe Experience Platform.

1. **Pubblica percorso** - Journey Optimizer genera automaticamente un percorso per la tua sfida. Passa all’inventario dei Percorsi e pubblica il percorso generato automaticamente per rendere la sfida disponibile ai clienti.

Per istruzioni dettagliate, consulta [Creare le sfide](create-challenges.md).

## Prerequisiti {#prerequisites}

Prima di utilizzare le sfide di fedeltà, assicurati di disporre di:

+++Configurazione dell’acquisizione dati

Le sfide relative alla fedeltà si basano sui dati acquisiti tramite i connettori di origine di Experience Platform per monitorare l’avanzamento dei clienti e il completamento delle attività.

Prima di iniziare, configura un connettore di origine supportato. Attualmente, è disponibile il connettore Capillary. Connettori aggiuntivi sono pianificati per le versioni future. [Scopri i connettori di origine fedeltà](https://experienceleague.adobe.com/en/docs/experience-platform/sources/home#loyalty).

+++

<!--+++Required permissions

To use Loyalty Challenges, you need appropriate permissions in Journey Optimizer. Required permissions include:

TBD

Contact your administrator if you cannot access the feature or need additional permissions.

+++-->

+++Pubblico target

Assicurati che il pubblico di destinazione di cui hai bisogno esista in Adobe Experience Platform prima di creare la tua sfida. Durante la configurazione della sfida, seleziona il pubblico che definisce quali clienti sono idonei a partecipare. [Scopri come utilizzare i tipi di pubblico](../audience/about-audiences.md).

+++

## Passaggi successivi {#next-steps}

<table style="table-layout:fixed">
<tr style="border: 0;">
  <td>
    <a href="access-loyalty-challenges.md">
    <!--<img alt="Access" src="../assets/do-not-localize/learn-more-button.svg">-->
    </a>
    <div>
    <a href="access-loyalty-challenges.md"><strong>Accesso e gestione di attività e problemi</strong></a>
    </div>
    <p>
    <em>Scopri come accedere alle sfide di inventario e filtro</em>
    </p>
  </td>
  <td>
    <a href="create-challenges.md">
      <!--<img alt="Create" src="../assets/do-not-localize/start-button.svg">-->
    </a>
    <div>
    <a href="create-challenges.md"><strong>Crea problemi</strong></a>
    </div>
    <p>
    <em>Scopri come creare e configurare la tua prima sfida fedeltà</em>
    </p>
  </td>
  <td>
    <a href="create-tasks.md">
    <!--<img alt="Tasks" src="../assets/do-not-localize/start-button.svg">-->
    </a>
    <div>
    <a href="create-tasks.md"><strong>Crea attività</strong></a>
    </div>
    <p>
    <em>Scopri come configurare le azioni completate dai clienti per le sfide</em>
    </p>
  </td>
</tr>
</table>
