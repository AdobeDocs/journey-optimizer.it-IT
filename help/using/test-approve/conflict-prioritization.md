---
title: Gestione dei conflitti e assegnazione delle priorità
description: Scopri come visualizzare in anteprima e testare i contenuti.
feature: Preview, Proofs
role: User
level: Beginner
badge: label="Beta"
hide: true
hidefromtoc: true
source-git-commit: ff529c9319a6eb5fe6762f30b739f2c39c3d5685
workflow-type: tm+mt
source-wordcount: '1186'
ht-degree: 21%

---


# Gestione dei conflitti e assegnazione delle priorità {#conflict-prioritization}

>[!AVAILABILITY]
>
>Gli strumenti per la gestione dei conflitti e la definizione delle priorità sono attualmente disponibili come versione beta solo per determinati utenti.

In Journey Optimizer, gestire il volume e la tempistica delle campagne e dei percorsi è essenziale per evitare di sopraffare i clienti con troppe interazioni. Nelle due sezioni seguenti vengono introdotti strumenti chiave per mantenere l’equilibrio e assegnare un’effettiva priorità alle comunicazioni

## Identificare potenziali conflitti in percorsi e campagne {#conflict}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_conflict"
>title="Visualizzatore di conflitti nelle campagne"
>abstract="Questo strumento può aiutarti a determinare la sovrapposizione con altri percorsi, campagne o configurazioni di canale. Se desideri identificare la sovrapposizione su pubblico, data di inizio e fine, configurazione dei canali, canale o set di regole, puoi visualizzare i potenziali conflitti qui."

>[!CONTEXTUALHELP]
>id="ajo_journey_conflict"
>title="Visualizzatore di conflitti nei percorsi"
>abstract="Questo strumento può aiutarti a determinare la sovrapposizione con altri percorsi, campagne o configurazioni di canale. Se desideri identificare la sovrapposizione su pubblico, data di inizio e fine, configurazione dei canali, canale o set di regole, puoi visualizzare i potenziali conflitti qui."

Con l’aumento del volume di campagne e Percorsi in Journey Optimizer, per un addetto marketing diventa sempre più difficile sapere se i propri clienti sono bombardati da troppe interazioni di marketing. è quindi essenziale identificare facilmente quando vi sono campagne e percorsi sovrapposti per garantire che raggiungano il giusto equilibrio nelle comunicazioni di marketing, mitigando al contempo i rischi di affaticamento dei clienti.

I settori chiave da monitorare per eventuali sovrapposizioni sono i seguenti:

* **Timeline** (date di inizio e di fine): troppi percorsi sono in esecuzione simultaneamente?
* **Pubblico**: quale percentuale del pubblico del mio percorso fa parte anche di altri percorsi?
* **Canale**: sono pianificate altre comunicazioni per lo stesso intervallo di tempo e, in caso affermativo, quante?
* **Set di regole di limitazione**: quali tipi di percorsi sono soggetti a limitazione e vi sono sovrapposizioni all&#39;interno di essi?
* **Configurazione canale**: ci sono altri percorsi o campagne che utilizzano una configurazione di canale utilizzata nello stesso percorso o campagna che potrebbe impedire la visualizzazione del percorso o della campagna all&#39;utente finale?

### Come Journey Optimizer rileva i conflitti {#detection}

Di seguito è riportato un riepilogo di come Journey Optimizer identifica potenziali conflitti per percorsi e campagne:

* **Ambito di identificazione dei conflitti**: i conflitti vengono visualizzati solo per campagne e percorsi live o pianificati.
* **percorsi unitari**: se il percorso selezionato è unitario, vengono visualizzati gli altri percorsi che iniziano con lo stesso evento, in quanto questo evento attiverà tutti i percorsi di questo tipo.
* **Qualificazione del pubblico ed evento Read Audience/Business** percorsi: se il percorso selezionato è un percorso di qualificazione del pubblico o Read Audience/Business Event, vengono visualizzati tutti gli altri percorsi dello stesso tipo con un pubblico valido, in quanto possono esserci sovrapposizioni tra i tipi di pubblico.
* **Campagne**: poiché tutte le campagne sono indirizzate a tipi di pubblico e non esiste un concetto di eventi, tutte le campagne potrebbero entrare in conflitto con percorsi attivati da segmenti (a partire da un&#39;attività Read audience).
* **Campagne live/pianificate**: le campagne live e pianificate possono entrare in conflitto tra loro a causa di una potenziale sovrapposizione di pubblico. Per una determinata campagna, tutte le campagne live o pianificate sono elencate nel visualizzatore di conflitti.

### Visualizzare i conflitti identificati per un determinato percorso o campagna {#view}

Durante la creazione di un percorso o di una campagna, Journey Optimizer consente di verificare ogni volta che esiste la possibilità di sovrapposizione con altri percorsi o campagne. Per farlo, segui questi passaggi:

1. Al momento della creazione di un percorso o di una campagna, fai clic sul pulsante **[!UICONTROL Visualizza conflitti potenziali]** nelle proprietà del percorso o della campagna.

   ![](assets/view-conflicts.png)

   >[!NOTE]
   >
   >Il pulsante **[!UICONTROL Visualizza potenziali conflitti]** diventa disponibile per la selezione non appena viene assegnata una delle seguenti impostazioni: **[!UICONTROL Data di inizio/fine]**, **[!UICONTROL Pubblico]**, **[!UICONTROL Canale]**, **[!UICONTROL Configurazione canale]** e **[!UICONTROL Set di regole]**. Accertati di selezionare **[!UICONTROL Salva]** dopo aver assegnato queste impostazioni, in quanto il pulsante non sarà selezionabile fino al salvataggio delle modifiche.

1. Viene visualizzata la finestra **[!UICONTROL Potenziali conflitti]**, che consente di visualizzare tutti gli elementi che si sovrappongono al percorso o alla campagna corrente.

   Puoi aprire un percorso o una campagna sovrapposti direttamente da questa schermata selezionandone il nome.

   ![](assets/potential-conflicts.png)

   >[!NOTE]
   >
   >Le nuove campagne pubblicate potrebbero richiedere fino a 5 minuti per essere visualizzate nel visualizzatore dei conflitti, a causa del caching implementato

Per perfezionare ulteriormente la ricerca di potenziali sovrapposizioni, puoi filtrare l’elenco di campagne e percorsi in base ai campi pertinenti. A questo scopo, seleziona l’icona del filtro nella vista inventario. [Scopri come utilizzare i filtri](../start/search-filter-categorize.md#filter-lists)

### Risolvi conflitti {#resolve}

Di seguito sono riportati alcuni suggerimenti per ridurre i potenziali conflitti una volta identificati:

* Modifica le **date di inizio/fine** per evitare la sovrapposizione di campagne o percorsi.
* Affina **targeting pubblico** per ridurre al minimo la sovrapposizione tra percorsi.
* Implementare **limiti di frequenza** per impedire ai clienti di ricevere troppe comunicazioni.
* Riduci il numero di **percorsi attivi** per gestire la customer experience in modo più efficace.
* Imposta **priorità** sulle azioni in entrata per garantire che venga visualizzata ai clienti l&#39;azione più importante.

Sfruttando queste funzionalità, potrai allineare le tue attività di marketing e mantenere il giusto equilibrio nella strategia di comunicazione.

## Assegnare punteggi di priorità a percorsi e campagne {#priority}

>[!CONTEXTUALHELP]
>id="ajo_journey_priority"
>title="Priorità"
>abstract="Assegna al percorso un punteggio di priorità compreso tra 0 e 100. Un numero più alto indica una priorità più alta. Il valore di priorità qui inserito viene ereditato da tutte le azioni in entrata (come in-app) contenute in questo percorso. Nelle situazioni in cui la stessa configurazione del canale in entrata viene utilizzata in altre campagne o percorsi, al destinatario viene mostrata l’azione in entrata con il punteggio di priorità più alto. Se più percorsi o campagne hanno lo stesso punteggio, viene scelto l’elemento modificato più di recente."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_priority"
>title="Priorità"
>abstract="Assegna alla campagna un punteggio di priorità compreso tra 0 e 100. Un numero più alto indica una priorità più alta. Nelle situazioni in cui la stessa configurazione del canale in entrata (come in-app) viene utilizzata in altre campagne o percorsi, al destinatario viene mostrata l’azione in entrata con il punteggio di priorità più alto. Se più percorsi o campagne hanno lo stesso punteggio, viene scelto l’elemento modificato più di recente."

Journey Optimizer ti consente di assegnare un punteggio di priorità a un percorso o a una campagna. La priorità è essenziale per assegnare la priorità a un percorso, una campagna o un’azione in presenza di un vincolo imposto (ad esempio un limite di frequenza). In situazioni in cui un cliente si qualifica per molti percorsi, campagne o comunicazioni e desideri essere selettivo in merito al quale deve entrare e ricevere, utilizza questo campo.

>[!NOTE]
>
>Il punteggio di priorità è disponibile per i canali in entrata: canali web, in-app e basati su codice. In percorso, il punteggio di priorità è disponibile solo per i canali **in-app** e **basati su codice**.

L’assegnazione di un punteggio di priorità è fondamentale per le comunicazioni in entrata, ad esempio web, mobile e in-app. Se disponi di più campagne che utilizzano la stessa configurazione di canale (ad esempio, un banner nella parte superiore della pagina web), ciò potrebbe rappresentare un problema in quanto è possibile visualizzare facilmente solo il contenuto di una campagna. Il punteggio di priorità è il punto in cui inserirai la tua preferenza per la campagna da mostrare quando il destinatario può qualificarsi per più di una campagna.

Per assegnare un punteggio di priorità a un percorso o a una campagna, immettere un valore numerico (da 0 a 100) nel campo **[!UICONTROL Punteggio di priorità]** incluso nelle proprietà del percorso o della campagna. Tieni presente che più alto è il numero, maggiore è la priorità. Se stavi creando questa campagna e volessi essere certo che il contenuto della campagna sia visualizzato, gli daresti un punteggio di 100.

![](assets/priority-score.png)

Per le situazioni in cui due campagne hanno lo stesso punteggio di priorità, verrà visualizzata la campagna attivata per prima.
