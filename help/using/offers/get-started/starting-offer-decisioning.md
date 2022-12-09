---
title: Guida introduttiva alla gestione delle decisioni
description: Scopri in che modo Adobe Journey Optimizer può aiutarti a inviare ai tuoi clienti l’offerta giusta al momento giusto
feature: Offers
topic: Integrations
role: User
level: Beginner
exl-id: 659984cb-b232-47ba-9f5a-604bf97a5e92
source-git-commit: c530905eacbdf6161f6449d7a0b39c8afaf3a321
workflow-type: tm+mt
source-wordcount: '929'
ht-degree: 0%

---

# Informazioni sulla gestione delle decisioni {#about-decision-management}

Utilizzo [!DNL Journey Optimizer] per offrire ai clienti la migliore offerta ed esperienza possibile in tutti i punti di contatto al momento giusto. Una volta progettato, rivolgiti al pubblico con offerte personalizzate.

La gestione delle decisioni semplifica la personalizzazione grazie a una libreria centrale di offerte di marketing e a un motore decisionale che applica regole e vincoli ai profili avanzati e in tempo reale creati da Adobe Experience Platform per aiutarti a inviare ai clienti l’offerta giusta al momento giusto.

La capacità di gestione delle decisioni è costituita da due componenti principali:

* La **Libreria di offerte centralizzata** , l’interfaccia in cui puoi creare e gestire i diversi elementi che compongono le offerte e definirne regole e vincoli.
* La **Motore di decisione dell’offerta** che sfrutta i dati di Adobe Experience Platform e i profili cliente in tempo reale, insieme alla Libreria offerte, per selezionare il momento giusto, i clienti e i canali a cui verranno distribuite le offerte.

![](../assets/architecture.png)

I vantaggi includono:

* Miglioramento delle prestazioni delle campagne grazie alla distribuzione di offerte personalizzate su più canali,
* Flussi di lavoro migliorati: invece di creare più consegne o campagne, i team di marketing possono migliorare i flussi di lavoro creando una singola consegna e variare le offerte in parti diverse del modello,
* Controllo del numero di volte in cui un’offerta viene visualizzata tra campagne e clienti.

➡️ [Ulteriori informazioni su Gestione delle decisioni in questi video](#video)


>[!NOTE]
>
>Se sei un [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html)Utente {target=&quot;_blank&quot;} che sfrutta **Offer Decisioning** il servizio applicativo, tutte le funzioni di gestione delle decisioni descritte in questa sezione si applicano anche all&#39;utente.

## Informazioni su offerte e decisioni {#about-offers-and-decisions}

Un **Offerta** è costituito da contenuto, regole di idoneità e vincoli che definiscono le condizioni in cui viene presentato ai clienti.

Viene creato utilizzando **Libreria offerte**, che fornisce un catalogo centrale delle offerte in cui è possibile associare regole di idoneità e vincoli a più parti di contenuto per creare e pubblicare offerte (consulta [Interfaccia utente della Libreria offerte](../get-started/user-interface.md)).

![](../assets/offer_structure.png)

Una volta arricchita la libreria delle offerte con le offerte, puoi integrare le offerte in **decisioni**.

Le decisioni sono contenitori per le offerte che sfrutteranno il motore decisionale dell’offerta per scegliere l’offerta migliore da consegnare in base al target della consegna.

## Casi d’uso comuni {#common-use-cases}

Le funzionalità di gestione delle decisioni e l’integrazione con Adobe Experience Platform ti consentono di coprire numerosi casi d’uso per aumentare il coinvolgimento e la conversione dei clienti.

* Puoi visualizzare nella home page le offerte che corrispondono al punto di interesse del cliente che visita, in base ai dati provenienti da Adobe Experience Platform.

   ![](../assets/website.png)

* Se i clienti si trovano vicino a uno dei tuoi negozi, invia loro notifiche push che ricordano le offerte disponibili in base ai loro attributi (livello di fedeltà, genere, acquisti precedenti..).

   ![](../assets/push_sample.png)

* La gestione delle decisioni consente inoltre di migliorare l’esperienza dei clienti quando si contattano i team di supporto. Le API per la gestione delle decisioni ti consentono di visualizzare nel portale degli agenti del call center informazioni sulle offerte rimborsate e sulle migliori offerte successive del cliente.

   ![](../../assets/do-not-localize/call-center.png)

## Concedere l’accesso alla gestione delle decisioni {#granting-acess-to-decision-management}

Le autorizzazioni di accesso e utilizzo delle funzionalità decisionali vengono gestite utilizzando [Adobe Admin Console](https://helpx.adobe.com/enterprise/managing/user-guide.html){target=&quot;_blank&quot;}.

Per concedere l&#39;accesso alla funzionalità Gestione delle decisioni, devi creare un **[!UICONTROL Product profile]** e assegna le autorizzazioni corrispondenti ai tuoi utenti. Ulteriori informazioni sulla gestione [!DNL Journey Optimizer] utenti e autorizzazioni in [questa sezione](../../administration/permissions.md).

Le autorizzazioni specifiche di Gestione delle decisioni sono elencate in [questa sezione](../../administration/high-low-permissions.md#decisions-permissions).

## Glossario {#glossary}

Di seguito è riportato l&#39;elenco dei concetti principali con cui lavorare quando si utilizza Gestione decisioni.

* **Limitazione** o **Limitazione di frequenza**: La limitazione di utilizzo viene utilizzata come vincolo per definire il numero di volte in cui viene presentata un’offerta. Esistono due tipi di limiti massimi, quante volte un’offerta può essere proposta tra il pubblico di destinazione combinato, noto anche come &quot;limiti massimi totali&quot; e quante volte un’offerta può essere proposta allo stesso utente finale, noto anche come &quot;limiti di profilo&quot;.

* **Raccolte**: Le raccolte sono sottoinsiemi di offerte in base a condizioni predefinite definite da un addetto al marketing, ad esempio la categoria dell’offerta.

* **Decisione**: Una decisione contiene la logica che informa la selezione di un’offerta.

* **Regola decisionale**: Le regole decisionali sono vincoli aggiunti a un’offerta personalizzata e applicati a un profilo per determinare l’idoneità.

* **Offerta idonea**: Un’offerta idonea soddisfa i vincoli definiti a monte che possono essere offerti in modo coerente a un profilo.

* **Gestione delle decisioni**: Consente di creare e fornire esperienze di offerta personalizzate per l’utente finale tra canali e applicazioni utilizzando la logica di business e le regole decisionali.

* **Offerte di fallback**: Un’offerta di fallback è l’offerta predefinita visualizzata quando un utente finale non è idoneo per alcuna delle offerte personalizzate nella raccolta.

* **Offerta**: Un’offerta è un messaggio di marketing a cui possono essere associate regole che specificano gli utenti idonei per visualizzare l’offerta.

* **Libreria offerte**: La libreria delle offerte è una libreria centrale utilizzata per gestire offerte personalizzate e di fallback, regole decisionali e decisioni.

* **Offerte personalizzate**: Un’offerta personalizzata è un messaggio di marketing personalizzabile basato su regole e vincoli di idoneità.

* **Posizionamenti**: Un posizionamento è la posizione e o il contesto in cui viene visualizzata un’offerta per un utente finale.

* **Priorità**: La priorità viene utilizzata per classificare le offerte che soddisfano tutti i vincoli, ad esempio idoneità, calendario e limiti.

* **Rappresentazioni**: Per rappresentazione si intendono le informazioni utilizzate da un canale, ad esempio la posizione o la lingua in cui visualizzare un’offerta.

## Video dimostrativi{#video}

>[!NOTE]
>
>Questi video si applicano al servizio di applicazione Offer Decisioning integrato in Adobe Experience Platform e non sono specifici per [!DNL Adobe Journey Optimizer]. Essi forniscono tuttavia indicazioni generiche per utilizzare la gestione delle decisioni nel contesto [!DNL Journey Optimizer].

### Che cos&#39;è la gestione delle decisioni? {#what-is-offer-decisioning}

Il video seguente fornisce un’introduzione alle funzionalità chiave di Gestione delle decisioni, all’architettura e ai casi d’uso:

>[!VIDEO](https://video.tv.adobe.com/v/326961?quality=12&learn=on)

### Definire e gestire le offerte {#use-offer-decisioning}

Il video seguente mostra come utilizzare Gestione decisioni per definire e gestire le offerte e sfruttare i dati sui clienti in tempo reale.

>[!VIDEO](https://video.tv.adobe.com/v/326841?quality=12&learn=on)


