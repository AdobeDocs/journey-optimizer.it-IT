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
badge: label="Disponibilità limitata" type="Informative"
feature_v2: []
subfeature_v2: []
source-git-commit: 4dd5fc79ef209265b1367d414fe6020d9a50064c
workflow-type: tm+mt
source-wordcount: 1912
ht-degree: 2%

---

# Simulare il percorso{#simulate-journey}

>[!IMPORTANT]
>
> Questa funzionalità è disponibile per tutta la clientela come disponibilità limitata con funzionalità essenziali.

Puoi impostare il percorso su **[!UICONTROL Simulazione]** oltre a **Bozza**, **Modalità test** e **Live**. In Simulazione, si esegue il test con **utenti simulati**: entità temporanee simili a profili aggiunte, senza utilizzare profili di test persistenti in Adobe Experience Platform.

Adobe Journey Optimizer offre due modi per testare e convalidare il percorso:

* **[Simulazione](#test-users)**: utilizzare la funzionalità di percorso **[!UICONTROL Simulazione]** e utenti simulati per eseguire rapidamente senza profili precreati in Adobe Experience Platform.

* **[Modalità di test](testing-the-journey.md)**: utilizza profili persistenti contrassegnati come profili di test in Adobe Experience Platform, riutilizzabili in più sessioni. Scegli questo approccio quando hai bisogno di dati coerenti e predefiniti. [Scopri come creare profili di test](../audience/creating-test-profiles.md).

Si noti che la simulazione del Percorso è in **Disponibilità limitata**. Per condividere il feedback e aiutarci a migliorare l&#39;esperienza, apri **[!UICONTROL Feedback]** dalla barra superiore.

![Menu feedback Beta](assets/beta-feedback.png)

## Creare e gestire utenti simulati {#test-users}

>[!IMPORTANT]
>
>Per accedere alla funzionalità **[!UICONTROL Simulazione]** è necessaria almeno una delle seguenti autorizzazioni: **Simula percorsi**, **Pubblica percorsi** o **Approva e pubblica percorsi**. [Ulteriori informazioni](../administration/permissions.md)

Gli utenti simulati sono entità temporanee simili a profili definite in **[!UICONTROL Impostazioni simulazione]**. Questa sezione descrive come crearli, dall’interfaccia utente o da un file JSON, salvarli per il riutilizzo, regolarli o rimuoverli dall’elenco e inviarli al percorso.

### Creare utenti simulati

I passaggi seguenti mostrano come creare utenti simulati dall’interfaccia utente o importando un file JSON.

1. Dal Percorso, apri **[!UICONTROL Simula]** e scegli **[!UICONTROL Simulazione]**.

   ![Pulsante Modalità di test nell&#39;interfaccia di percorso](assets/test-mode-simulated.png)

1. Fai clic su **[!UICONTROL Crea utenti simulati]** per creare nuovi utenti e selezionare se crearli dall&#39;interfaccia utente o importarli da JSON.

   Per riutilizzare gli utenti simulati, fare clic su **[!UICONTROL Seleziona utenti simulati]** e scegliere le voci salvate in precedenza.

   ![Pannello di selezione utenti simulato](assets/simulate-2.png)

1. Se crei utenti simulati da JSON, aggiorna i campi corrispondenti con i dati utente simulati.

1. Se crei utenti simulati dall&#39;interfaccia utente, immetti un **[!UICONTROL Nome visualizzato]** e una **[!UICONTROL Descrizione]** per identificare l&#39;utente simulato. Quindi, seleziona dallo schema di unione gli attributi che desideri compilare per questo utente.

   ![Selezione di attributi dallo schema di unione](assets/simulate-3.png)

1. Fai clic su Aggiungi **[!UICONTROL Appartenenza al pubblico]** per simulare le appartenenze ai segmenti.

1. Fai clic su **[!UICONTROL Aggiungi profilo]** per creare più utenti simulati in una singola sessione.

1. Per ogni utente simulato aggiunto in questa sessione, puoi utilizzare le azioni seguenti:

   * **[!UICONTROL Duplicato]**: aggiunge un nuovo utente simulato che replica la configurazione completata di una voce esistente. Sarà quindi possibile modificare il duplicato in base alle esigenze.
   * **[!UICONTROL Applica a tutti]**: propaga i valori o le impostazioni degli attributi da un utente simulato a tutti gli altri utenti simulati dell&#39;elenco.
   * **[!UICONTROL Elimina]**: rimuove l&#39;utente simulato selezionato dall&#39;elenco.

1. Fai clic su **[!UICONTROL Salva]** per archiviare uno o più utenti simulati per utilizzi futuri.

1. Dopo il salvataggio, gli utenti simulati creati verranno visualizzati nell&#39;elenco **[!UICONTROL Test utenti]**. Per ogni voce, apri il menu delle opzioni e seleziona una delle seguenti opzioni:

   * ![Icona Modifica](assets/do-not-localize/Smock_Edit_18_N.svg): aggiorna i dettagli dell&#39;utente simulato.
   * ![Icona invio](assets/do-not-localize/Smock_Send_18_N.svg): esegui la simulazione solo per questo utente simulato.
   * ![Icona Cancella](assets/do-not-localize/Smock_Close_18_N.svg): rimuovere l&#39;utente dall&#39;elenco. L’utente simulato non viene eliminato e rimane disponibile nella selezione Utenti simulati.

   ![Pannello di selezione utenti simulato](assets/simulate-4.png)

1. Se il percorso include un&#39;attività **[!UICONTROL Attendi]**, apri la scheda **[!UICONTROL Impostazioni test]** per ottimizzare la durata dell&#39;attesa durante la simulazione.

1. Fai clic su **[!UICONTROL Invia tutto]** per inviare al percorso tutti gli utenti simulati presenti nell&#39;elenco. Viene visualizzato un messaggio di conferma `Simulated users have been sent successfully.` quando gli utenti simulati entrano correttamente nel percorso.

   ![Pannello di selezione utenti simulato](assets/simulate-5.png)

1. Accedi alla scheda **[!UICONTROL Risultati]** per aprire il registro di esecuzione e controllare come è stato eseguito ciascun passaggio. Per ulteriori informazioni, vedere [Visualizza risultati](#viewing-results).

Dopo aver convalidato il percorso in **[!UICONTROL Simulazione]**, controlla il registro **[!UICONTROL Risultati]**. Se vengono visualizzati errori, lasciare **[!UICONTROL Simulazione]**, applicare le modifiche necessarie al percorso ed eseguire di nuovo **[!UICONTROL Simulazione]** finché l&#39;esecuzione non risulta corretta. È quindi possibile pubblicare il percorso. Vedi [Pubblica il tuo percorso](../building-journeys/publish-journey.md).

### Seleziona utenti simulati

Gli utenti simulati creati manualmente vengono archiviati e possono essere selezionati da questo elenco quando la simulazione è abilitata in altri percorsi.

1. Imposta il percorso su **[!UICONTROL Simulazione]**. Apri il punto di ingresso **[!UICONTROL Simula]** e scegli **[!UICONTROL Simulazione]** in modo che il percorso utilizzi la funzione di simulazione, ad esempio insieme alla modalità di test o Live, a seconda dell&#39;area di lavoro.

   ![Pulsante Modalità di test nell&#39;interfaccia di percorso](assets/test-mode-simulated.png)

1. Nel pannello **[!UICONTROL Impostazioni simulazione]**, è possibile selezionare gli utenti simulati creati in precedenza facendo clic su **[!UICONTROL Seleziona utenti simulati]**.

   ![Modalità di test nell&#39;interfaccia di percorso](assets/simulate-11.png)

1. Seleziona dall’elenco degli utenti simulati creati e salvati in precedenza.

1. Dopo aver selezionato gli utenti simulati, sono ora disponibili nell&#39;elenco **[!UICONTROL Utenti test]**. Dal menu Opzioni, scegliere tra le seguenti opzioni:

   * ![Icona Modifica](assets/do-not-localize/Smock_Edit_18_N.svg) per modificare gli utenti e i relativi dettagli.
   * ![Icona Invia](assets/do-not-localize/Smock_Send_18_N.svg) per inviare la simulazione a un solo utente simulato.
   * ![Icona Cancella](assets/do-not-localize/Smock_Close_18_N.svg) per cancellare dall&#39;elenco gli utenti simulati. La cancellazione non ne comporta l’eliminazione, ma può comunque essere selezionata dall’elenco degli utenti simulati.

   ![Pannello di selezione utenti simulato](assets/simulate-4.png)

1. Fai clic su **[!UICONTROL Invia tutto]** per inviare al percorso tutti gli utenti simulati presenti nell&#39;elenco. Viene visualizzato un messaggio di conferma `Simulated users entered the journey successfully.` quando gli utenti simulati entrano correttamente nel percorso.

   ![Pannello di selezione utenti simulato](assets/simulate-5.png)

1. Accedi alla scheda **[!UICONTROL Risultati]** per aprire il registro di esecuzione e controllare come è stato eseguito ciascun passaggio. Per ulteriori informazioni, vedere [Visualizza risultati](#viewing-results).

Dopo aver convalidato il percorso in **[!UICONTROL Simulazione]**, controlla il registro **[!UICONTROL Risultati]**. Se vengono visualizzati errori, lasciare **[!UICONTROL Simulazione]**, applicare le modifiche necessarie al percorso ed eseguire di nuovo **[!UICONTROL Simulazione]** finché l&#39;esecuzione non risulta corretta. È quindi possibile pubblicare il percorso. Vedi [Pubblica il tuo percorso](../building-journeys/publish-journey.md).

## Attivare gli eventi {#firing_events}

Se il percorso include uno o più eventi, puoi attivarli mentre la simulazione è attiva.

1. In **[!UICONTROL Seleziona tipo di evento]**, seleziona l&#39;evento da attivare per questa simulazione.

   ![Interfaccia di configurazione degli eventi con campi e elenco a discesa per la selezione degli eventi](assets/simulate-10.png)

1. Fai clic su **[!UICONTROL Configura eventi]** per aprire l&#39;editor e regolare l&#39;evento in base alle esigenze. Per modificare il payload solo per un utente simulato specifico, fare clic su ![Modifica evento](assets/do-not-localize/Smock_Edit_18_N.svg) accanto all&#39;utente.

   ![Interfaccia di configurazione degli eventi con campi e elenco a discesa per la selezione degli eventi](assets/simulate-9.png)

1. Nella visualizzazione **[!UICONTROL Trigger evento]**, specificare gli utenti simulati da includere nell&#39;esecuzione. La configurazione dell’evento si applica a un singolo evento alla volta. La modifica dell’evento selezionato o del set di utenti inclusi reimposta i valori dei campi precedentemente immessi. Completa la configurazione corrente prima di modificare una delle selezioni.

   ![Configurazione evento con elenco utenti di prova e campi evento](assets/simulate-8.png)

1. Fai clic su **[!UICONTROL Fine]**.

1. Quindi, in **[!UICONTROL Eventi test]**, selezionare **[!UICONTROL Invia tutto]** per inviare al percorso ogni utente simulato elencato in **[!UICONTROL Verifica utenti]** oppure selezionare ![Icona invio](assets/do-not-localize/Smock_Send_18_N.svg) per consentire a un singolo utente di eseguire la simulazione solo per tale utente.

1. Accedi alla scheda **[!UICONTROL Risultati]** per aprire il registro di esecuzione e controllare come è stato eseguito ciascun passaggio. Per ulteriori informazioni, vedere [Visualizza risultati](#viewing-results).

## Visualizza risultati {#viewing-results}

La scheda **[!UICONTROL Risultati]** consente di visualizzare i risultati del test. Nell&#39;elenco a discesa **[!UICONTROL Test utente]** selezionare l&#39;utente simulato di cui si desidera verificare l&#39;esecuzione.

<!--
* **All simulated users**: Select **[!UICONTROL All]** to see results aggregated across every simulated user in the run. This view helps you scan the full simulation at a glance, activity, outcomes, and errors, without picking a single simulated user first.
-->

Per ogni attività, il registro può mostrare se l’utente simulato è entrato o uscito dal passaggio e gli errori che si sono verificati durante la simulazione.

![Registri per utenti di prova](assets/simulate-6.png)

Per le attività **Wait**, il registro include due valori relativi alla durata:

* **Durata definita**: la durata specificata nell&#39;attività **Attendi** per il percorso pubblicato e applicata una volta che il percorso è attivo. Il registro registra se Simulazione applica un&#39;esclusione dalle impostazioni del test, ad esempio 10 secondi, anziché basarsi esclusivamente sul valore definito nel percorso.
* **Durata effettiva**: tempo trascorso per cui l&#39;utente simulato è rimasto nell&#39;attività **Wait**. Questo valore è impostato dalla scheda **[!UICONTROL Impostazioni test]**.

Quando nel registro vengono visualizzati errori, lasciare **Simulazione**, applicare le modifiche necessarie al percorso ed eseguire di nuovo **Simulazione**. Dopo la convalida, pubblica il percorso. Vedi [Pubblica il tuo percorso](../building-journeys/publish-journey.md).

## Limitazioni {#limitations}

In questa versione, **[!UICONTROL La simulazione]** potrebbe non supportare tutte le attività, i canali o le integrazioni supportati dalla **[!UICONTROL Modalità di test]** o da un percorso live e il comportamento potrebbe cambiare con la maturazione delle funzionalità. Utilizza le procedure descritte in questo articolo per i flussi di lavoro supportati.

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
