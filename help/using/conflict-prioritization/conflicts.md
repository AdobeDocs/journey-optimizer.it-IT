---
title: Identificare potenziali conflitti in percorsi e campagne
description: Scopri come identificare potenziali conflitti in percorsi e campagne.
role: User
level: Beginner
exl-id: efbb5ac4-4c07-4c62-9460-39eb4fed129a
source-git-commit: a824e7342ee32eb261f2ecfb00b9ec12ec655f1e
workflow-type: tm+mt
source-wordcount: '755'
ht-degree: 16%

---

# Rilevare potenziali conflitti in percorsi e campagne {#conflict}

Con l’aumento del volume di campagne e Percorsi in Journey Optimizer, per un addetto marketing diventa sempre più difficile sapere se i propri clienti sono bombardati da troppe interazioni di marketing. È quindi essenziale identificare facilmente quando vi sono campagne e percorsi sovrapposti per garantire che raggiungano il giusto equilibrio nelle comunicazioni di marketing, mitigando al contempo i rischi di affaticamento dei clienti.

I settori chiave da monitorare per eventuali sovrapposizioni sono i seguenti:

* **Timeline** (date di inizio e di fine): troppi percorsi sono in esecuzione simultaneamente?
* **Pubblico**: quale percentuale del pubblico del mio percorso fa parte anche di altri percorsi?
* **Canale**: sono pianificate altre comunicazioni per lo stesso intervallo di tempo e, in caso affermativo, quante?
* **Set di regole di limitazione**: quali tipi di percorsi sono soggetti a limitazione e vi sono sovrapposizioni all&#39;interno di essi?
* **Configurazione canale**: ci sono altri percorsi o campagne che utilizzano una configurazione di canale utilizzata nello stesso percorso o campagna che potrebbe impedire la visualizzazione del percorso o della campagna all&#39;utente finale?

➡️ [Scopri questa funzione nel video](#video)

## Come Journey Optimizer rileva i conflitti {#detection}

Di seguito è riportato un riepilogo di come Journey Optimizer identifica potenziali conflitti per percorsi e campagne:

* **Ambito di identificazione dei conflitti**: i conflitti vengono visualizzati solo per campagne e percorsi live o pianificati.
* **percorsi unitari**: se il percorso selezionato è unitario, vengono visualizzati gli altri percorsi che iniziano con lo stesso evento, in quanto questo evento attiverà tutti i percorsi di questo tipo.
* **Qualificazione del pubblico ed evento Read Audience/Business** percorsi: se il percorso selezionato è un percorso di qualificazione del pubblico o Read Audience/Business Event, vengono visualizzati tutti gli altri percorsi dello stesso tipo con un pubblico valido, in quanto possono esserci sovrapposizioni tra i tipi di pubblico.
* **Campagne**: poiché tutte le campagne sono indirizzate a tipi di pubblico e non esiste un concetto di eventi, tutte le campagne potrebbero entrare in conflitto con percorsi attivati da segmenti (a partire da un&#39;attività Read audience).
* **Campagne live/pianificate**: le campagne live e pianificate possono entrare in conflitto tra loro a causa di una potenziale sovrapposizione di pubblico. Per una determinata campagna, tutte le campagne live o pianificate sono elencate nel visualizzatore di conflitti.

## Visualizzare i conflitti identificati per un determinato percorso o campagna {#view}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_conflict"
>title="Visualizzare i conflitti potenziali"
>abstract="Controlla se esiste la possibilità di sovrapposizione con altre campagne. I conflitti vengono visualizzati solo per le campagne live e pianificate. Il pulsante diventa disponibile non appena hai assegnato una delle seguenti impostazioni: **[!UICONTROL Data di inizio/fine]**, **[!UICONTROL Pubblico]**, **[!UICONTROL Canale]**, **[!UICONTROL Configurazione dei canali]** e **[!UICONTROL Set di regole]**."

>[!CONTEXTUALHELP]
>id="ajo_journey_conflict"
>title="Visualizzare i conflitti potenziali"
>abstract="Controlla se esiste la possibilità di sovrapposizione con altri percorsi. I conflitti vengono visualizzati solo per i percorsi live e pianificati. Il pulsante diventa disponibile non appena hai assegnato una delle seguenti impostazioni: **[!UICONTROL Data di inizio/fine]**, **[!UICONTROL Pubblico]**, **[!UICONTROL Canale]**, **[!UICONTROL Configurazione dei canali]** e **[!UICONTROL Set di regole]**."

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
   >I nuovi percorsi e le nuove campagne pubblicati potrebbero richiedere fino a 3-7 minuti per essere visualizzati nel visualizzatore dei conflitti, a causa del caching implementato.

Per perfezionare ulteriormente la ricerca di potenziali sovrapposizioni, puoi filtrare l’elenco di campagne e percorsi in base ai campi pertinenti. A questo scopo, seleziona l’icona del filtro nella vista inventario. [Scopri come utilizzare i filtri](../start/search-filter-categorize.md#filter-lists)

## Risolvi conflitti {#resolve}

Di seguito sono riportati alcuni suggerimenti per ridurre i potenziali conflitti una volta identificati:

* Modifica le **date di inizio/fine** per evitare la sovrapposizione di campagne o percorsi.
* Affina **targeting pubblico** per ridurre al minimo la sovrapposizione tra percorsi.
* Implementare **limiti di frequenza** per impedire ai clienti di ricevere troppe comunicazioni.
* Riduci il numero di **percorsi attivi** per gestire la customer experience in modo più efficace.
* Imposta **priorità** sulle azioni in entrata per garantire che venga visualizzata ai clienti l&#39;azione più importante.

Sfruttando queste funzionalità, potrai allineare le tue attività di marketing e mantenere il giusto equilibrio nella strategia di comunicazione.

## Video dimostrativo {#video}

>[!VIDEO](https://video.tv.adobe.com/v/3435528?quality=12)
