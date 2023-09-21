---
solution: Journey Optimizer
product: journey optimizer
title: Eseguire il piano di riscaldamento IP
description: Scopri come eseguire e monitorare un piano di riscaldamento IP
feature: Application Settings
topic: Administration
role: Admin
level: Experienced
keywords: IP, pool, gruppo, sottodomini, recapito messaggi
hide: true
hidefromtoc: true
source-git-commit: 11bdb3ddc666d2025133f70ab522c4ce2d676aa6
workflow-type: tm+mt
source-wordcount: '791'
ht-degree: 1%

---

# Eseguire il piano di riscaldamento IP {#ip-warmup-running}

>[!BEGINSHADEBOX]

Cosa troverai in questa documentazione di guida:

* [Introduzione al riscaldamento dell’IP](ip-warmup-gs.md)
* [Creare campagne di riscaldamento IP](ip-warmup-campaign.md)
* [Creare un piano di riscaldamento IP](ip-warmup-plan.md)
* **[Eseguire il piano di riscaldamento IP](ip-warmup-running.md)**

>[!ENDSHADEBOX]

## Definire le fasi {#define-phases}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_campaigns_excluded"
>title="Seleziona i tipi di pubblico delle campagne da escludere"
>abstract="Seleziona i tipi di pubblico da altre campagne da escludere dalla fase corrente."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_domains_excluded"
>title="Seleziona i gruppi di dominio da escludere"
>abstract="Seleziona i domini da escludere dalla fase corrente."

È necessario associare la campagna e il pubblico a livello di fase e attivare alcune impostazioni in base alle esigenze per tutte le esecuzioni associate a una singola creatività/campagna

A livello di fase, il sistema assicura che i profili target + nuovi vengano selezionati E a livello di iterazione, assicura che ogni esecuzione presenti profili univoci e che il conteggio corrisponda a quanto dichiarato nel piano

1. Per ogni fase, seleziona la campagna da associare a questa fase del piano di riscaldamento IP.

   ![](assets/ip-warmup-plan-select-campaign.png)

   Tieni presente quanto segue:

   * Solo le campagne con **[!UICONTROL Attivazione del piano di riscaldamento IP]** opzione abilitata <!--and live?--> sono disponibili per la selezione. [Ulteriori informazioni](#create-ip-warmup-campaign)

   * È necessario selezionare una campagna che utilizza la stessa superficie di quella selezionata per il piano di riscaldamento IP corrente.

   * Non puoi selezionare una campagna già in uso in un’altra campagna di riscaldamento IP.

1. In **[!UICONTROL Esclusione profilo]** sezione, puoi notare che i profili delle esecuzioni precedenti di quella fase sono sempre esclusi. Ad esempio, se in #1 di esecuzione un profilo è stato coperto dalle prime 4800 persone target, il sistema si assicurerà automaticamente che lo stesso profilo non riceva l’e-mail in #2. di esecuzione

1. Dalla sezione **[!UICONTROL Pubblico della campagna escluso]** , seleziona i tipi di pubblico da un&#39;altra <!--executed/live?-->campagne che desideri escludere dalla fase corrente.

   ![](assets/ip-warmup-plan-exclude-campaigns.png)

   Ad esempio, durante l’esecuzione della fase 1, era necessario [dividilo](#split-phase) per qualsiasi motivo. Pertanto, puoi escludere la campagna utilizzata nella fase 1 in modo che i profili contattati in precedenza dalla fase 1 non siano inclusi nella fase 2. Puoi anche escludere le campagne da altri piani di riscaldamento dell’IP.

1. Dalla sezione **[!UICONTROL Gruppi di domini esclusi]** , selezionare i domini che si desidera escludere da tale fase.

   ![](assets/ip-warmup-plan-exclude-domains.png)

   Ad esempio, dopo aver eseguito il riscaldamento dell’IP per alcuni giorni, ti rendi conto che la reputazione dell’ISP con un dominio (ad Adobe) non è buona e desideri risolverla senza interrompere il piano di riscaldamento dell’IP. In questo caso, puoi escludere il gruppo di dominio Adobe.

   >[!NOTE]
   >
   >L’esclusione del dominio richiede una fase non eseguita, quindi potrebbe essere necessario dividere una fase in esecuzione per aggiungere esclusioni. Analogamente, se il gruppo di dominio non è un gruppo di dominio OOTB, devi aggiungerlo al file Excel, caricarlo e quindi escludere il dominio.

   ![](assets/ip-warmup-plan-phase-1.png)

1. Se necessario, puoi aggiungere una fase. Verrà aggiunta dopo l&#39;ultima fase corrente.

1. Utilizza il **[!UICONTROL Elimina fase]** per rimuovere eventuali fasi indesiderate.

   ![](assets/ip-warmup-plan-add-delete-phases.png)

   >[!CAUTION]
   >
   >Non è possibile annullare **[!UICONTROL Elimina]** azione.
   >
   >Se elimini tutte le fasi dal piano di riscaldamento IP, si consiglia di ricaricare un piano.

## Definire le esecuzioni {#define-runs}

1. Seleziona una pianificazione per ogni esecuzione. <!--which is actually a window of opportunity. meaning? how many hours? shall we specify that to clarify?-->

   ![](assets/ip-warmup-plan-send-time.png)

1. Seleziona un’ora di fine, che definisce la finestra all’interno della quale la campagna di riscaldamento IP può essere eseguita in caso di ritardi nell’esecuzione del processo di segmentazione del pubblico. Se non viene specificato un orario di fine, l’esecuzione viene tentata all’orario di inizio e avrà esito negativo se la segmentazione non è stata completata.

1. Attiva ogni esecuzione. Assicurati di pianificare con un tempo sufficiente per consentire l’esecuzione del processo di segmentazione. <!--explain how you can evaluate a proper time-->

   >[!CAUTION]
   >
   >Ogni esecuzione deve essere attivata almeno 12 ore prima dell’ora di invio effettiva. In caso contrario, la segmentazione potrebbe non essere completata. <!--How do you know when segmentation is complete? Is there a way to prevent user from scheduling less than 12 hours before the segmentation job?-->

   <!--Sart to execute on every day basis by simply clicking the play button > for each run? do you have to come back every day to activate each run? or can you schedule them one after the other?)-->

1. Se l’esecuzione della campagna non è stata avviata, puoi interrompere un’esecuzione.<!--why?-->

   >[!NOTE]
   >
   >Una volta avviata l’esecuzione della campagna, il **[!UICONTROL Interrompi]** non è più disponibile. <!--TBC in UI-->

   ![](assets/ip-warmup-plan-stop-run.png)

1. Per aggiungere un’esecuzione, seleziona **[!UICONTROL Aggiungi una sequenza di seguito]** dall’icona dei tre puntini.

   ![](assets/ip-warmup-plan-run-more-actions.png)

## Dividere una fase {#split-phase}

In qualsiasi momento, se desideri utilizzare una campagna diversa a partire da un’esecuzione specifica, seleziona la **[!UICONTROL Opzione Dividi in una nuova fase]** dall’icona dei tre puntini.

Viene creata una nuova fase per le restanti esecuzioni della fase corrente. Segui i passaggi [sopra](#define-phases) per definire la nuova fase.

Ad esempio, se selezioni questa opzione per Esegui #4, le esecuzioni #4 a #8 verranno spostate in una nuova fase.

<!--
You don't have to decide the campaign upfront. You can do a split later. It's a work in progress plan: you activate one run at a time with a campaign and you always have the flexibility to modify it while working on it.

But need to explain in which case you want to modify campaigns, provide examples
-->

## Monitorare il piano

Un’esecuzione può avere i seguenti stati<!--TBC with Medha-->:

* **[!UICONTROL Completato]**:
* **[!UICONTROL Non riuscito]**:
* **[!UICONTROL Annullato]**: l’esecuzione è stata interrotta prima dell’avvio dell’esecuzione della campagna.

Vantaggi :

* I rapporti continueranno a essere visualizzati a livello di campagna con funzionalità simili a quelle attuali. Ma il piano di riscaldamento dell&#39;IP funge anche da rapporto consolidato in un unico luogo di quante esecuzioni sono state effettuate e così via.

* Un’unica posizione per gestire e visualizzare l’avanzamento degli indirizzi IP caldi.

* Rapporto consolidato a livello creativo/campagna in quanto tutti i dati vengono eseguiti per una fase