---
solution: Journey Optimizer
product: journey optimizer
title: Ottimizzazione dei canali
description: Scopri come utilizzare l’ottimizzazione dei canali per selezionare automaticamente il canale in uscita migliore per ciascun cliente in base alle sue preferenze o ai punteggi di propensione previsti dall’intelligenza artificiale.
feature: Journeys, Activities, Channels Activity
topic: Content Management, Artificial Intelligence
role: User
level: Intermediate
keywords: canale, ottimizzazione, preferenza, propensione, IA, in uscita, e-mail, push, messaggio mobile
badge: label="Disponibilità limitata" type="Informative"
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
source-git-commit: eac6801e299f743e21d84e685eb1fb50bb40ec29
workflow-type: tm+mt
source-wordcount: 1219
ht-degree: 2%

---


# Ottimizzazione dei canali {#channel-optimization}

>[!BEGINSHADEBOX]

**In questa pagina:** scopri come configurare un&#39;azione di percorso o di campagna per inviare messaggi tramite il miglior canale in uscita per ciascun cliente, utilizzando una classificazione manuale, preferenze di profilo o punteggi di propensione basati su intelligenza artificiale.

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>L’ottimizzazione del canale è attualmente disponibile per un numero limitato di organizzazioni (disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.

L’ottimizzazione dei canali consente di aggiungere più canali in uscita (e-mail, push, messaggio mobile) a un singolo percorso o azione della campagna e di fare in modo che Journey Optimizer selezioni automaticamente quello migliore per ogni cliente al momento dell’invio.

Invece di scegliere un canale upfront o di inviare messaggi ai clienti su tutti i canali contemporaneamente, il sistema sceglie il canale più alto in cui ciascun cliente può essere opt-in e fallback con facilità quando quel canale non è disponibile.

➡️ [Ulteriori informazioni sull&#39;ottimizzazione dei canali in questo video](#video)

## Guardrail e limitazioni {#limitations}

* **Canali supportati**: sono supportati solo i canali e-mail, push e di messaggistica mobile nativi. Altri canali in uscita come WhatsApp non sono supportati. L’ottimizzazione del canale richiede l’utilizzo delle funzionalità native di posta elettronica, push e messaggistica mobile di Journey Optimizer; l’esecuzione tramite azioni personalizzate non è supportata.

* **Metrica di ottimizzazione IA**: il modello di IA viene ottimizzato solo per il coinvolgimento (clic). Non viene ottimizzato per ordini, ricavi o altre metriche aziendali. Se è necessaria l’ottimizzazione per ordini o ricavi, il team di data science può addestrare offline un modello personalizzato e applicarlo tramite la funzione di attributo del profilo cliente.

* **Tracciamento dei clic richiesto per la classificazione basata su IA**: quando si utilizza la classificazione basata su modello di IA, il tracciamento dei clic deve essere abilitato per tutti i canali configurati. Il modello si basa sui dati di clic per calcolare i punteggi di tendenza; se il tracciamento è disabilitato, la modalità di classificazione IA non può funzionare correttamente. [Scopri come abilitare il tracciamento dei clic nel messaggio e-mail](../email/message-tracking.md)

* **Ore non interattive**: quando più canali vengono combinati in un&#39;unica azione, le ore non interattive vengono applicate in base alla priorità del canale: la messaggistica mobile ha la precedenza, seguita da Push, e-mail. Per utilizzare diverse impostazioni per le ore non interattive per canale, creare azioni di percorso separate anziché combinare i canali in una singola azione.

  >[!NOTE]
  >
  >Il supporto per le impostazioni delle ore non interattive per canale è pianificato per la versione con disponibilità generale.

* **Incompatibilità con l&#39;ottimizzazione dell&#39;ora di invio**: attualmente [Impossibile utilizzare contemporaneamente l&#39;ottimizzazione dell&#39;ora di invio](send-time-optimization.md) e l&#39;ottimizzazione dei canali. Scegliere una delle due opzioni. L’interfaccia utente impedisce l’abilitazione simultanea di entrambe le funzioni sulla stessa azione.

* **Eventi di reazione**: gli eventi di reazione nell&#39;area di lavoro del percorso fanno attualmente riferimento solo al primo canale in un&#39;azione multicanale.

  >[!NOTE]
  >
  >Per la versione con disponibilità generale è pianificato il supporto per la selezione di qualsiasi evento di reazione valido in presenza di più canali.

## Utilizzare l’ottimizzazione del canale in un percorso o in una campagna {#configure}

Per aggiungere più canali in uscita con ottimizzazione del canale a un percorso o a una campagna, segui la procedura riportata di seguito.

>[!BEGINTABS]

>[!TAB In un percorso]

1. Avvia il percorso con un&#39;attività [Event](general-events.md) o [Read Audience](read-audience.md).

1. Dalla sezione **[!UICONTROL Azioni]** della palette, trascina e rilascia un&#39;attività **[!UICONTROL Azione]** nell&#39;area di lavoro.

1. Seleziona un canale in uscita (messaggio e-mail, push o mobile) e fai clic su **[!UICONTROL Aggiungi]**.

   ![Aggiungere un canale in uscita a un&#39;azione di percorso](assets/journey-channel-optimization-add-outbound.png){width="60%"}

1. Immetti un&#39;etichetta per l&#39;azione e fai clic su **[!UICONTROL Configura azione]**.

>[!TAB In una campagna]

1. [Crea una campagna di azioni](../campaigns/create-campaign.md) e passa alla scheda **[!UICONTROL Azioni]**.

1. Fai clic sul pulsante **[!UICONTROL Aggiungi azione]** e seleziona un canale in uscita (e-mail, messaggio push o messaggio mobile).

>[!ENDTABS]

Dopo aver selezionato un&#39;azione in uscita nella scheda **[!UICONTROL Azioni]**, continuare con i passaggi seguenti.

1. Seleziona una configurazione di canale e fai clic su **[!UICONTROL Aggiungi azione]** per selezionare un altro canale in uscita.

   ![Aggiungi un altro canale in uscita a un&#39;azione di percorso](assets/journey-channel-optimization-add-outbound-action.png){width="1000%"}

   >[!NOTE]
   >
   >In una singola azione multicanale è supportata una sola azione per tipo di canale. Ad esempio, non puoi aggiungere due azioni E-mail separate con configurazioni diverse.

   Puoi aggiungere fino a tre canali in uscita (**[!UICONTROL E-mail]**, **[!UICONTROL Invio]**, **[!UICONTROL Messaggio mobile]**) a una singola azione o campagna di percorso.

1. Nella sezione **[!UICONTROL Ottimizzazione canale]**, impostare il metodo per determinare in che modo il sistema seleziona il canale migliore per ogni cliente. [Ulteriori informazioni](#optimization-modes)

   ![Selezionare una modalità di ottimizzazione canale](assets/journey-channel-optimization-modes.png){width="100%"}

1. Imposta l’ordine dei canali di fallback (per i metodi di classificazione manuale e di preferenze del cliente) trascinando i canali nell’ordine desiderato. [Ulteriori informazioni](#fallback)

   ![Riordino ottimizzazione canale classificazione manuale](assets/journey-channel-optimization-manual-reorder.png){width="90%"}

1. [Salva e pubblica](publish-journey.md) il tuo percorso oppure [controlla e attiva](../campaigns/review-activate-campaign.md) la tua campagna.

## Impostare il metodo di ottimizzazione del canale {#optimization-modes}

>[!CONTEXTUALHELP]
>id="ajo_channel_optimization_method"
>title="Definire il funzionamento della selezione dei canali"
>abstract="Scegli in che modo Journey Optimizer seleziona il canale migliore per ciascun cliente: **Priorità manuale** — i canali vengono provati nell&#39;ordine definito; la disponibilità è determinata applicando le preferenze di abbonamento e le regole di consenso marketing associate alle configurazioni di canale selezionate e a tutte le regole business (ad esempio, il limite di frequenza del canale) associate alla campagna o al percorso. **Attributo profilo cliente**: il canale che corrisponde alla preferenza dichiarata del cliente nel suo profilo è selezionato per primo. Se non viene trovata alcuna preferenza, viene applicata la priorità manuale. **Ottimizzato per l&#39;intelligenza artificiale**: un modello di apprendimento automatico classifica ogni canale in base al coinvolgimento storico del cliente e viene selezionato il canale disponibile con il punteggio più alto."

<!--
Previous content for contextual help: "The customer's first available channel, based on the selected prioritization method, is used for this action. Availability is determined by the customer's subscription preferences and marketing consent rules for the selected channel configurations, as well as any business rules — such as frequency capping — configured for the campaign or journey." TBC which to keep.

Additional content for contextual help: For **Manual priority** and **Customer profile attribute** modes, Journey Optimizer falls back through your configured channel order when the top-ranked channel cannot be used. For **AI optimized**, it falls back to a random available channel."
-->

L’ottimizzazione del canale supporta tre modalità, ciascuna delle quali utilizza un metodo diverso per selezionare il canale migliore per ciascun cliente al momento dell’invio.

### Classificazione manuale {#manual-ranking}

**[!UICONTROL Priorità manuale]** è la modalità predefinita. Puoi definire l’ordine dei canali preferito direttamente nell’azione. Journey Optimizer distribuisce tramite il primo canale dell&#39;elenco in cui il cliente ha effettuato l&#39;opt-in e non ha un limite di frequenza, quindi [se necessario, &#x200B;](#fallback) torna al canale successivo.

![Ottimizzazione manuale del canale di classificazione](assets/journey-channel-optimization-manual.png){width="90%"}

Utilizza questa modalità quando disponi di una preferenza di canale chiara e coerente e non è necessaria la personalizzazione per profilo.

### Preferenza cliente {#customer-preference}

Con **[!UICONTROL Attributo profilo cliente]** selezionato, Journey Optimizer legge il canale preferito dichiarato del cliente dal suo profilo, utilizzando l&#39;attributo `preferred` nel gruppo di campi XDM [Consensi e preferenze](https://experienceleague.adobe.com/it/docs/experience-platform/xdm/field-groups/profile/consents). I valori supportati sono `email`, `push` e `sms`.

![Ottimizzazione canale preferenze cliente](assets/journey-channel-optimization-profile.png){width="90%"}

Se il canale preferito non è disponibile (non è configurato, non ha prestato il consenso o ha un limite di frequenza), Journey Optimizer torna al canale successivo nell&#39;elenco di [fallback](#fallback) configurato.

Utilizza questa modalità quando i clienti hanno dichiarato esplicitamente il loro canale di comunicazione preferito.

### Classificazione basata su modello di IA {#ai-ranking}

Se selezioni **[!UICONTROL Ottimizzato per l&#39;intelligenza artificiale]**, Journey Optimizer utilizza un modello di apprendimento automatico che calcola un punteggio di propensione per canale per ogni cliente in base al suo coinvolgimento storico (aperture, clic). I punteggi vengono memorizzati nel profilo del cliente e al momento dell’invio viene selezionato il canale con la tendenza prevista più elevata.

![Ottimizzazione del canale di classificazione basata su modello AI](assets/journey-channel-optimization-ai.png){width="70%"}

Quando un cliente ha una cronologia di coinvolgimento insufficiente, il sistema utilizza come fallback un canale disponibile in modo casuale.

Utilizza questa modalità per consentire all’intelligenza artificiale di dedurre il canale più efficace per ogni cliente senza alcuna configurazione manuale.

## Comportamento di fallback {#fallback}

Indipendentemente dalla modalità di ottimizzazione, Journey Optimizer torna al successivo canale disponibile quando non è possibile utilizzare il canale con il punteggio più alto. Un canale è considerato non disponibile quando si applica una delle seguenti condizioni:

* Il cliente non viene acconsentito al canale.
* Il canale non è configurato nell’azione.
* Il canale ha raggiunto il suo limite di frequenza.
* La preferenza di profilo del cliente o il punteggio di modello di IA per quel canale non viene popolato.

Nelle modalità **[!UICONTROL Priorità manuale]** e **[!UICONTROL Attributo profilo cliente]**, il fallback segue l&#39;elenco di priorità dei canali configurato dall&#39;addetto al marketing. In **[!UICONTROL Ottimizzato ai]**, il fallback seleziona un canale disponibile casuale.

## Video introduttivo {#video}

Scopri in che modo la funzione di ottimizzazione del canale di Adobe Journey Optimizer consente di raggiungere i clienti sul canale più efficace utilizzando priorità manuale, attributi di profilo o il modello di intelligenza artificiale di Adobe.

>[!VIDEO](https://video.tv.adobe.com/v/3492132?quality=12)

<!--
**Related topics**

* [Use the Action activity](journey-action.md)
* [Send-Time optimization](send-time-optimization.md)
* [Content optimization](../content-management/gs-message-optimization.md)
-->
