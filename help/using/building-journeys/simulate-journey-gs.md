---
solution: Journey Optimizer
product: journey optimizer
title: Simulare il percorso
description: Scopri come simulare il percorso
feature: Journeys, Test Profiles
topic: Content Management
role: User
level: Intermediate
keywords: test, percorso, controllo, errore, risoluzione dei problemi
version: Journey Orchestration
hide: true
source-git-commit: 2083a5043bbb48085a83260086a9bdd5ac1f0953
workflow-type: tm+mt
source-wordcount: '1028'
ht-degree: 2%

---

# Introduzione alla simulazione dei Percorsi {#simulate-journey-gs}

Puoi impostare il percorso su **[!UICONTROL Simulazione]** oltre a **Bozza**, **Modalità test** e **Live**. In Simulazione, si esegue il test con **utenti simulati**: entità temporanee simili a profili aggiunte, senza utilizzare profili di test persistenti in Adobe Experience Platform.

Adobe Journey Optimizer offre due modi per testare e convalidare il percorso:

* **[Simulazione](#test-users)**: utilizzare la funzionalità di percorso **[!UICONTROL Simulazione]** e utenti simulati per eseguire rapidamente senza profili precreati in Adobe Experience Platform.

* **[Modalità di test](testing-the-journey.md)**: utilizza profili persistenti contrassegnati come profili di test in Adobe Experience Platform, riutilizzabili in più sessioni. Scegli questo approccio quando hai bisogno di dati coerenti e predefiniti. [Scopri come creare profili di test](../audience/creating-test-profiles.md).

## Simulazione per tipo di percorso {#by-journey-type}

Il pannello **[!UICONTROL Simulazione]** mostra solo i passaggi necessari per il percorso. Questo dipende dal modo in cui i profili entrano nel percorso. Da questi fattori, Adobe Journey Optimizer fa emergere diverse esperienze di simulazione. Espandi ciascun tipo riportato di seguito per vedere le differenze tra le esecuzioni e quali pannelli utilizzi.

Per ulteriori dettagli, vedere [Simulare il percorso](simulate-journey.md).

+++ Percorso batch con un pubblico di lettura

Il percorso è attivato da un pubblico **read**. L’area di lavoro non dispone di attività evento unitarie, i profili si spostano solo attraverso condizioni, attese e azioni del canale.

Con **percorso batch con pubblico di lettura**, puoi accedere alla simulazione rapida o alla simulazione manuale.

![Pannello simulazione per un percorso batch con sola lettura del pubblico](assets/simulate-14.png)

+++

+++ Percorso batch con un pubblico di lettura ed eventi unitari

Un percorso di attivazione segmento che include uno o più eventi unitari lungo il percorso. Dopo aver inviato gli utenti in, attivi gli eventi per gli utenti che attendono un nodo evento.

Con **percorso batch con pubblico in lettura ed eventi unitari**, puoi accedere a Simulazione rapida o Simulazione manuale.

![Pulsante Modalità di test nell&#39;interfaccia di percorso](assets/simulate-12.png)

+++

+++ Percorso unitario

Il percorso **inizia** con un evento unitario, non un pubblico di lettura. Un utente simulato non entra nel percorso finché l’evento di inizio non viene attivato per lui.

Con **percorso unitario**, puoi accedere direttamente al menu Simulazione manuale.

![Pannello di simulazione per un percorso unitario](assets/simulate-13.png)

+++

## Simulazione avvio {#launch}

Passa al percorso **[!UICONTROL Simulazione]** per eseguire il test con utenti simulati. Le attività dettagliate sono descritte in [Simulare il percorso](simulate-journey.md).

1. Dal tuo percorso, fai clic su **[!UICONTROL Simula]** e scegli **[!UICONTROL Simulazione]**.

   ![Pulsante Modalità di test nell&#39;interfaccia di percorso](assets/test-mode-simulated.png)

1. Attendere il completamento dell&#39;attivazione. Mentre il percorso passa a **[!UICONTROL Simulazione]**, i controlli nel pannello vengono disattivati e riattivati automaticamente al termine dell&#39;attivazione.

## Limitazioni {#limitations}

In questa versione, **[!UICONTROL La simulazione]** potrebbe non supportare tutte le attività, i canali o le integrazioni supportati dalla **[!UICONTROL Modalità di test]** o da un percorso live e il comportamento potrebbe cambiare con la maturazione delle funzionalità. Usa questo articolo per i flussi di lavoro supportati.

Per ulteriori informazioni sulle limitazioni della simulazione, consulta i menu a discesa sottostanti.

+++ Limitazioni a livello di nodo

Se un percorso contiene uno dei nodi seguenti, non può essere avviato in **[!UICONTROL Simulazione]**. Prima di eseguire la simulazione, è necessario modificare il percorso o rimuovere il nodo pertinente.

| Nodo con restrizioni | Note |
| --- | --- |
| Eventi di business | I percorsi che iniziano con un evento di business non possono essere eseguiti in **[!UICONTROL Simulazione]**. |
| ID supplementare (rientro multiplo) | Il rientro simultaneo (più istanze attive per lo stesso utente simulato) impedisce l&#39;avvio della **[!UICONTROL simulazione]**. |
| Nodo decisione contenuto | Per simulare il percorso, è necessario rimuovere o modificare questa attività. |
| Ricerca nei set di dati | Le ricerche di set di dati cliente per chiave non sono supportate. I percorsi che includono questa attività non possono essere eseguiti in **[!UICONTROL Simulazione]**. |
| Sperimentazione percorso (Ottimizza, variante esperimento) | Non supportato in **[!UICONTROL Simulazione]**. È comunque possibile utilizzare **[!UICONTROL Ottimizza]** per i flussi che in precedenza vivevano in **[!UICONTROL Condizione]** (ad esempio, condizioni dell&#39;origine dati). |
| Targeting percorso (ottimizza, variante regola di targeting) | Non supportato in **[!UICONTROL Simulazione]**. |
| Arricchimento degli attributi del pubblico esterno | I percorsi che utilizzano attributi personalizzati da origini di pubblico esterne non inizieranno in **[!UICONTROL Simulazione]** quando questa convalida è attiva. |

+++

</br>

+++ Limitazioni funzionali

Le seguenti funzionalità non sono supportate in **[!UICONTROL Simulazione]**.

| Funzionalità | Note |
| --- | --- |
| Criteri di uscita | I criteri di uscita non vengono applicati quando si esegue **[!UICONTROL Simulazione]**. |
| [!DNL Adobe Journey Optimizer] decisioni all&#39;interno di un&#39;azione (ad esempio, contenuto e-mail con Adobe Journey Optimizer decisioning) | Le bozze delle azioni per il contenuto che utilizza le decisioni [!DNL Adobe Journey Optimizer] non vengono generate. |
| Mascherare la risposta dell’azione personalizzata | [!UICONTROL Le azioni personalizzate] eseguono una chiamata in uscita reale per impostazione predefinita. Non è supportato il mascheramento della risposta in modo da non eseguire chiamate esterne. |
| Valutazione dei criteri di consenso | Il consenso non può essere deriso a livello di utente simulato. |
| Limitazione di percorso e arbitrato | Non supportato in **[!UICONTROL Simulazione]**. |
| Limitazione della frequenza (per canale o tipo di comunicazione) | Non supportato in **[!UICONTROL Simulazione]**. |
| Gestione delle rinunce, soppressione ed elenchi consentiti | Segue la configurazione di indirizzamento dei messaggi, dove applicabile. |
| Sottodominio dinamico e attributi dinamici in configurazioni di canale | Segue la configurazione di indirizzamento dei messaggi, dove applicabile. |
| Ottimizzazione dell’ora di invio (STO) | Non supportato in **[!UICONTROL Simulazione]**. |
| Strumenti sandbox (copia utenti simulati tra sandbox) | Non supportato. |
| Invio ondata in percorsi | Non supportato. |
| Ore di silenzio | Non supportato. |
| Gestione delle rinunce, soppressione ed elenchi consentiti | Non supportato. |
| Sottodominio dinamico e attributi dinamici in configurazioni di canale | Non supportato. |
| Privacy Service | Gli utenti simulati non sono profili persistenti conformi ai requisiti RGPD. Non includere dati reali dei clienti in utenti simulati. |

+++

</br>

+++ Guardrail quantitativi 

Queste protezioni si applicano alla **[!UICONTROL simulazione]**. Le maiuscole numeriche vengono applicate nell’interfaccia di percorso e in fase di runtime. I limiti possono cambiare in una versione successiva; se ti avvicini al soffitto, verifica il comportamento nella sandbox.

| Guardrail | Limite | Note |
| --- | --- | --- |
| Numero massimo di utenti simulati che possono essere selezionati e attivati in un batch (percorsi batch, flussi attivati da eventi e flussi di qualificazione del pubblico) | 20 | Conteggiato per ogni **[!UICONTROL Invia tutti]** o **[!UICONTROL Attiva eventi selezionati]**; non un limite cumulativo per l&#39;intero percorso. |
| Numero massimo di utenti simulati univoci testati in una singola esecuzione di simulazione | 100 | Il raggiungimento di **100** utenti univoci in una sola esecuzione blocca **[!UICONTROL Seleziona utenti simulati]** per i nuovi utenti simulati. Se ti trovi alle **90**, puoi aggiungerne al massimo **10** prima dello stesso blocco. |
| Numero massimo di percorsi eseguibili contemporaneamente in **[!UICONTROL Simulazione]** in una sandbox | 20 | Il limite viene condiviso da ogni **[!UICONTROL Simulazione]** percorso della sandbox. |
| Numero massimo di utenti simulati attivi in una sandbox | 2,000 | Numero massimo di utenti simulati che possono esistere nella sandbox contemporaneamente. Adobe può modificare questo limite in base al feedback ricevuto dai clienti. |
| Precompilazione evento (solo browser) | — | Puoi precompilare i campi del payload dell’evento solo nell’interfaccia utente di simulazione basata su browser. I valori precompilati rimangono in tale browser e non vengono sincronizzati con altri browser, dispositivi o sessioni, pertanto puoi visualizzare dati precompilati diversi in ogni posizione in cui esegui il test. |

+++
