---
solution: Journey Optimizer
product: journey optimizer
title: Prova del percorso
description: Scopri come pubblicare un percorso in modalità di esecuzione in prova
feature: Journeys
role: User
level: Intermediate
badge: label="Disponibilità limitata" type="Informative"
keywords: pubblicazione, percorso, live, validità, verifica
exl-id: 58bcc8b8-5828-4ceb-9d34-8add9802b19d
source-git-commit: 62525caa9b065538c090b98d38c15dbd960dafe7
workflow-type: tm+mt
source-wordcount: '864'
ht-degree: 24%

---

# Prova del percorso {#journey-dry-run}

>[!CONTEXTUALHELP]
>id="ajo_journey_dry_run"
>title="Modalità di esecuzione di prova"
>abstract="Questo percorso è in esecuzione di prova. L’esecuzione di prova di un percorso è una modalità speciale di pubblicazione dello stesso in Adobe Journey Optimizer che consente ai professionisti che si occupano del percorso di poterlo testare utilizzando dati reali di produzione, senza dover contattare la clientela reale o aggiornare le informazioni del profilo.  Questa funzione aiuta i professionisti del percorso ad acquisire maggiore sicurezza rispetto alla progettazione di un percorso e al targeting del pubblico, prima della pubblicazione effettiva."


>[!CONTEXTUALHELP]
>id="ajo_journey_dry_run_start"
>title="Pubblicare un percorso in modalità di esecuzione di prova"
>abstract="L’esecuzione di prova di un percorso è una modalità speciale di pubblicazione dello stesso in Adobe Journey Optimizer che consente ai professionisti che si occupano del percorso di poterlo testare utilizzando dati reali di produzione. Dopo aver progettato il percorso, esegui un’esecuzione in prova per assicurare che funzioni e che i passaggi siano corretti. Questa modalità di pubblicazione consente di eseguire un test preliminare di un percorso, senza inviare comunicazioni ad alcun profilo."

L’esecuzione di prova di un percorso è una modalità speciale di pubblicazione dello stesso in Adobe Journey Optimizer che consente ai professionisti che si occupano del percorso di poterlo testare utilizzando dati reali di produzione, senza dover contattare la clientela reale o aggiornare le informazioni del profilo.  Questa funzione aiuta i professionisti del percorso ad acquisire maggiore sicurezza rispetto alla progettazione di un percorso e al targeting del pubblico, prima della pubblicazione effettiva.


>[!AVAILABILITY]
>
>Questa funzionalità è disponibile solo per un set di organizzazioni (disponibilità limitata) e verrà introdotta a livello globale in una versione futura.


## Vantaggi chiave {#journey-dry-run-benefits}

L’esecuzione in modalità Percorsi Dry aumenta la fiducia dei professionisti e il successo del percorso consentendo test sicuri e basati sui dati dei percorsi dei clienti che utilizzano dati di produzione reali, senza il rischio di contattare i clienti o di modificare le informazioni del profilo. Questa funzione consente ai professionisti del percorso di convalidare la logica di copertura del pubblico e della diramazione prima della pubblicazione, garantendo che i percorsi siano allineati agli obiettivi di business previsti.

Con l&#39;esecuzione di prova del Percorso, è possibile identificare i problemi in anticipo, ottimizzare le strategie di targeting e migliorare la progettazione del percorso in base ai dati effettivi, non alle ipotesi. Integrato direttamente nell’area di lavoro del percorso, Dry run fornisce rapporti intuitivi e visibilità sugli indicatori delle prestazioni chiave, consentendo ai team di eseguire iterazioni affidabili e di semplificare i flussi di lavoro di approvazione. Ciò migliora l&#39;efficienza operativa, riduce il rischio di lancio e migliora i risultati del coinvolgimento dei clienti.

In ultima analisi, questa funzione migliora il time-to-value e riduce i guasti del percorso.

Percorsi Dry run porta:

1. **Ambiente di test sicuro**: i profili in modalità di esecuzione a secco non vengono contattati, garantendo che non vi sia alcun rischio di inviare comunicazioni o di influire sui dati live.
1. **Informazioni sul pubblico**: i professionisti del Percorso possono prevedere la raggiungibilità del pubblico in vari nodi del percorso, tra cui rinunce, esclusioni e altre condizioni.
1. **Feedback in tempo reale**: le metriche vengono visualizzate direttamente nell&#39;area di lavoro del percorso, in modo simile al reporting live, consentendo agli utenti del percorso di perfezionare la progettazione del percorso.

Durante il funzionamento a secco, il percorso viene eseguito con le seguenti specificità:

* **I nodi dell&#39;azione del canale**, comprese le notifiche e-mail, SMS o push, non vengono eseguiti
* **Le azioni personalizzate** sono disabilitate durante l&#39;esecuzione di prova e le relative risposte sono impostate su null
* **I nodi di attesa** vengono ignorati durante l&#39;esecuzione di prova.
  <!--You can override the wait block timeouts, then if you have wait blocks duration longer than allowed dry run journey duration, then that branch will not execute completely.-->
* **Le origini dati**, incluse le origini dati esterne, vengono eseguite per impostazione predefinita

>[!CAUTION]
>
>* Le autorizzazioni per avviare l&#39;esecuzione in prova sono limitate agli utenti con l&#39;autorizzazione di alto livello **[!DNL Publish journeys]**. Le autorizzazioni per interrompere l&#39;esecuzione in prova sono limitate agli utenti con l&#39;autorizzazione di alto livello **[!DNL Manage journeys]**. Ulteriori informazioni sulla gestione dei diritti di accesso degli utenti [!DNL Journey Optimizer] in [questa sezione](../administration/permissions-overview.md).
>
>* Prima di iniziare a utilizzare la funzionalità di esecuzione di prova, [leggere i guardrail e le limitazioni](#journey-dry-run-limitations).


## Avvia un&#39;esecuzione di prova {#journey-dry-run-start}

Potete utilizzare la funzionalità di esecuzione di prova in qualsiasi percorso 2D senza errori.

Per attivare l&#39;esecuzione in prova, effettuare le seguenti operazioni:

1. Aprire il percorso che si desidera verificare.
1. Selezionare il pulsante **Esegui**.

   ![Avvia l&#39;esecuzione di prova del percorso](assets/dry-run-button.png)

1. Conferma la pubblicazione.

   Durante la transizione viene visualizzato il messaggio di stato **Attivazione dell&#39;esecuzione di prova**.

1. Dopo l&#39;attivazione, il percorso entra in modalità **Esecuzione a secco**.

## Monitorare un’esecuzione in prova {#journey-dry-monitor}

Una volta avviata la pubblicazione in modalità Asciutto, puoi visualizzare l’esecuzione del percorso e il modo in cui i profili progrediscono attraverso rami e nodi del percorso.

Le metriche vengono visualizzate direttamente nell’area di lavoro del percorso. Ulteriori informazioni sui report e le metriche live di percorso sono disponibili in [Report live nell&#39;area di lavoro di percorso](report-journey.md).

![Monitorare l&#39;esecuzione di prova del percorso](assets/dry-run-metrics.png)


È inoltre possibile accedere ai **report delle ultime 24 ore** e ai **report delle ultime 24 ore** per l&#39;esecuzione di prova. Per accedere a questi report, fare clic sul pulsante **Visualizza report** nell&#39;angolo superiore destro dell&#39;area di lavoro del percorso.

![Accedere ai report per l&#39;esecuzione a secco del percorso](assets/dry-run-report.png)

>[!CAUTION]
>
> I dati di reporting sono disponibili solo quando l&#39;esecuzione di prova è **attiva**.  Una volta interrotti, i dati di reporting non saranno più accessibili. Utilizza il pulsante **Esporta** sopra i report per scaricarli, se necessario.


## Interrompere un&#39;esecuzione di prova {#journey-dry-run-stop}

I percorsi di esecuzione di prova **devono** essere interrotti manualmente.

Fai clic sul pulsante **Chiudi** per terminare il test, quindi fai clic su **Torna alla bozza** per confermare.

<!-- After 14 days, Dry run journeys automatically transition to the **Draft** status.-->

## Guardrail e limitazioni {#journey-dry-run-limitations}

* La modalità di esecuzione in prova non è disponibile per i percorsi contenenti eventi di reazione
* I profili in modalità di esecuzione in prova vengono conteggiati per i profili coinvolgibili
* I percorsi in modalità di esecuzione in prova vengono conteggiati ai fini della quota di percorso in tempo reale
* I percorsi di esecuzione in prova non influiscono sulle regole aziendali
* Durante la creazione di una nuova versione del percorsi percorso, se una versione precedente è **Live**, l&#39;attivazione dell&#39;esecuzione di prova non è consentita per la nuova versione.
* L’esecuzione di prova del percorso genera stepEvents. Questi stepEvents hanno un flag specifico e un ID esecuzione di prova:
   * `_experience.journeyOrchestration.stepEvents.inDryRun` restituisce `true` se l&#39;esecuzione di prova è attivata e `false` in caso contrario
   * `_experience.journeyOrchestration.stepEvents.dryRunID` restituisce l&#39;ID di un&#39;istanza di esecuzione di prova

* Quando si analizzano le metriche di reporting del percorso utilizzando Adobe Experience Platform Query Service, è necessario escludere gli eventi di passaggio generati dall’esecuzione di prova. Per eseguire questa operazione, impostare il flag `inDryRun` su `false`.