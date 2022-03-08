---
title: Introduzione a Gestione delle decisioni
description: Introduzione a Gestione delle decisioni. Scopri l’architettura, le offerte e le decisioni, nonché alcuni casi d’uso comuni che possono esserti utili
feature: Offers
topic: Integrations
role: User
level: Beginner
exl-id: 659984cb-b232-47ba-9f5a-604bf97a5e92
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '908'
ht-degree: 100%

---

# Informazioni sulla gestione delle decisioni {#about-decision-management}

Utilizza [!DNL Journey Optimizer] per offrire ai clienti l’offerta e l’esperienza migliore al momento giusto, in tutti i punti di contatto. Una volta progettate, puoi indirizzarle al tuo pubblico con offerte personalizzate.

>[!NOTE]
>
>Tutte le funzioni di gestione delle decisioni descritte in questa sezione si applicano anche agli utenti di [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html?lang=it){target=&quot;_blank&quot;} che sfruttano il servizio applicativo **Offer Decisioning**.

La capacità di Gestione delle decisioni è costituita da due componenti principali:

* La **Libreria di offerte centralizzata** è l’interfaccia in cui puoi creare e gestire i diversi elementi che compongono le offerte e definirne regole e vincoli.
* Il **motore delle decisioni per le offerte** sfrutta i dati di Adobe Experience Platform e i profili cliente in tempo reale, insieme alla Libreria di offerte, per selezionare i clienti, i canali e il momento più appropriati per l’invio delle offerte.

![](../assets/architecture.png)

I vantaggi includono:

* Miglioramento delle prestazioni delle campagne grazie alla distribuzione di offerte personalizzate su più canali.
* Flussi di lavoro migliorati: anziché creare più consegne o campagne, i team di marketing possono ottimizzare i flussi di lavoro creando un’unica consegna e variare le offerte in parti differenti del modello.
* Potrai controllare il numero di volte in cui un’offerta viene visualizzata nelle varie campagne e dai diversi clienti.

➡️ [Guarda questi video tutorial](#tutorial-videos) per saperne di più sulla gestione delle decisioni.

## Informazioni su offerte e decisioni {#about-offers-and-decisions}

Un’**offerta** è costituita da contenuti, regole di idoneità e vincoli che definiscono le condizioni in cui viene presentata ai clienti.

Viene creata utilizzando la **Libreria offerte**, che fornisce un catalogo centrale delle offerte in cui è possibile associare regole di idoneità e vincoli a più parti di contenuto per creare e pubblicare le offerte (consulta [Interfaccia utente della Libreria offerte](../get-started/user-interface.md)).

![](../assets/offer_structure.png)

Una volta arricchita la libreria delle offerte con le offerte, puoi integrarle in **decisioni** (precedentemente note come “attività di offerta”).

Le decisioni sono contenitori per le offerte che sfrutteranno il motore delle decisioni per le offerte per scegliere l’offerta migliore da consegnare in base al target.

## Casi d’uso comuni {#common-use-cases}

Le funzionalità di Gestione delle decisioni e la sua integrazione con Adobe Experience Platform consentono di coprire numerosi casi d’uso per aumentare il coinvolgimento e la conversione dei clienti.

* Puoi visualizzare sul tuo sito web le offerte che corrispondono al punto di interesse del visitatore, in base ai dati provenienti da Adobe Experience Platform.

   ![](../assets/website.png)

* Se i clienti si trovano vicino a uno dei tuoi negozi, puoi inviare loro notifiche push sulle offerte disponibili in base ai loro attributi (livello di fedeltà, genere, acquisti precedenti...).

   ![](../assets/push_sample.png)

* La funzione di gestione delle decisioni consente inoltre di migliorare l’esperienza dei clienti che contattano il team di assistenza. Con le API di Gestione delle decisioni puoi visualizzare nel portale degli agenti del call center informazioni sulle offerte di cui il cliente ha già usufruito e sulle migliori offerte successive.

   ![](../../assets/do-not-localize/call-center.png)

## Concedere l’accesso alla gestione delle decisioni {#granting-acess-to-decision-management}

Le autorizzazioni per accedere e utilizzare le funzionalità di Offer Decisioning vengono gestite mediante [Adobe Admin Console](https://helpx.adobe.com/it/enterprise/managing/user-guide.html){target=&quot;_blank&quot;}.

Per concedere l’accesso alla funzionalità di gestione delle decisioni, devi creare un **[!UICONTROL Product profile]** e assegnare le autorizzazioni corrispondenti ai tuoi utenti. Per saperne di più sulla gestione di utenti e autorizzazioni per [!DNL Journey Optimizer], consulta [questa sezione](../../administration/permissions.md).

Le autorizzazioni specificheper la gestione delle decisioni sono elencate in [questa sezione](../../administration/high-low-permissions.md#decisions-permissions).

## Glossario {#glossary}

Di seguito è riportato l’elenco dei concetti principali con cui lavorare quando si utilizza Gestione decisioni.

* **Quota limite** o **Quota limite frequenza**: il limite viene utilizzato come vincolo per definire quante volte viene presentata un’offerta.
Ci sono due tipi di limite: uno indica quante volte un’offerta può essere proposta al pubblico target combinato, noto anche come “Limiti totali”; l’altro indica quante volte un’offerta può essere proposta allo stesso utente finale, noto anche come “Limite per profilo”.

* **Raccolte**: le raccolte sono sottoinsiemi di offerte basate su condizioni predefinite impostate da un addetto marketing, ad esempio la categoria dell’offerta.

* **Decisione**: una decisione contiene la logica su cui si basa la selezione di un’offerta.

* **Regola di decisione**: le regole di decisione sono vincoli aggiunti a un’offerta personalizzata e applicati a un profilo per determinare l’idoneità.

* **Offerta idonea**: un’offerta idonea soddisfa i vincoli definiti a monte che definiscono l’offerta coerente rispetto a un profilo.

* **Gestione delle decisioni**: consente di creare e fornire esperienze di offerta personalizzate per l’utente finale sui vari canali e applicazioni utilizzando la logica di business e le regole decisionali.

* **Offerte di fallback**: un’offerta di fallback è l’offerta predefinita che viene visualizzata se un utente finale non è idoneo per nessuna delle offerte personalizzate nella raccolta.

* **Offerta**: un’offerta è un messaggio di marketing a cui possono essere associate delle regole che determinano gli utenti idonei per visualizzare l’offerta.

* **Libreria di offerte**: la libreria di offerte è una libreria centrale utilizzata per gestire offerte personalizzate e di fallback, regole di decisione e decisioni.

* **Offerte personalizzate**: un’offerta personalizzata è un messaggio di marketing personalizzabile basato su regole e vincoli di idoneità.

* **Posizionamenti**: il posizionamento corrisponde a posizione e contesto in cui un’offerta viene mostrata a un utente finale.

* **Priorità**: la priorità viene utilizzata per classificare le offerte che soddisfano tutti i vincoli, come idoneità, calendario e limiti.

* **Rappresentazioni**: per rappresentazione si intendono le informazioni utilizzate da un canale, ad esempio posizione o lingua, per mostrare un’offerta.


## Video tutorial {#tutorial-videos}

>[!NOTE]
>
>Questi video fanno riferimento al servizio applicativo Offer Decisioning integrato in Adobe Experience Platform e non sono specifici di [!DNL Adobe Journey Optimizer]. Tuttavia, forniscono indicazioni generiche per utilizzare la gestione delle decisioni nel contesto di [!DNL Journey Optimizer].

### Che cos&#39;è la gestione delle decisioni? {#what-is-offer-decisioning}

Il video seguente fornisce un’introduzione alle funzionalità chiave di gestione delle decisioni, alla sua architettura e ai casi d’uso:

>[!VIDEO](https://video.tv.adobe.com/v/326961?quality=12&learn=on)

### Definire e gestire le offerte {#use-offer-decisioning}

Il video seguente mostra come utilizzare la funzione di gestione delle decisioni per definire e gestire le offerte e sfruttare i dati sui clienti in tempo reale.

>[!VIDEO](https://video.tv.adobe.com/v/326841?quality=12&learn=on)
