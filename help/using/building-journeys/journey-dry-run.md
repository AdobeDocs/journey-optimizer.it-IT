---
solution: Journey Optimizer
product: journey optimizer
title: Percorso prova
description: Scopri come pubblicare un percorso in modalità di esecuzione in prova
feature: Journeys
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Disponibilità limitata" type="Informative"
keywords: pubblicazione, percorso, live, validità, verifica
exl-id: 58bcc8b8-5828-4ceb-9d34-8add9802b19d
source-git-commit: bb881f0257408ad70f3737c24d1caa28deea96e0
workflow-type: tm+mt
source-wordcount: '821'
ht-degree: 7%

---

# Percorso prova {#journey-dry-run}

>[!CONTEXTUALHELP]
>id="ajo_journey_dry_run"
>title="Esecuzione in prova del percorso"
>abstract="Dopo aver progettato il percorso, esegui un’esecuzione in prova per assicurare che funzioni e che i passaggi siano corretti. Questa modalità di pubblicazione consente di eseguire un test preliminare di un percorso, senza inviare comunicazioni ad alcun profilo."

Percorsi Dry run è una speciale modalità di pubblicazione del percorso in Adobe Journey Optimizer che consente ai professionisti del percorso di testare un percorso utilizzando dati di produzione reali senza contattare clienti reali o aggiornare le informazioni del profilo.  Questa funzione aiuta i professionisti del percorso ad acquisire fiducia nella progettazione del percorso e nel targeting del pubblico prima di pubblicarlo in diretta.


>[!AVAILABILITY]
>
>Questa funzionalità è disponibile solo per un set di organizzazioni (LA, disponibilità limitata). Per potervi accedere, contatta il tuo rappresentante Adobe.


## Vantaggi chiave {#journey-dry-run-benefits}

L’esecuzione in modalità Percorsi Dry aumenta la fiducia dei professionisti e il successo del percorso consentendo test sicuri e basati sui dati dei percorsi dei clienti che utilizzano dati di produzione reali, senza il rischio di contattare i clienti o di modificare le informazioni del profilo. Questa funzione consente ai professionisti del percorso di convalidare la logica di copertura del pubblico e della diramazione prima della pubblicazione, garantendo che i percorsi siano allineati agli obiettivi di business previsti.

Con l&#39;esecuzione di prova del Percorso, è possibile identificare i problemi in anticipo, ottimizzare le strategie di targeting e migliorare la progettazione del percorso in base ai dati effettivi, non alle ipotesi. Integrato direttamente nell’area di lavoro del percorso, Dry run fornisce rapporti intuitivi e visibilità sugli indicatori delle prestazioni chiave, consentendo ai team di eseguire iterazioni affidabili e di semplificare i flussi di lavoro di approvazione. Ciò migliora l&#39;efficienza operativa, riduce il rischio di lancio e migliora i risultati del coinvolgimento dei clienti.

In ultima analisi, questa funzione migliora il time-to-value e riduce i guasti del percorso.

Percorsi Dry run porta:

1. **Ambiente di test sicuro**: i profili in modalità di esecuzione a secco non vengono contattati, garantendo che non vi sia alcun rischio di inviare comunicazioni o di influire sui dati live.
1. **Informazioni sul pubblico**: i professionisti del Percorso possono prevedere la raggiungibilità del pubblico in vari nodi del percorso, tra cui rinunce, esclusioni e altre condizioni.
1. **Feedback in tempo reale**: le metriche vengono visualizzate direttamente nell&#39;area di lavoro del percorso, in modo simile al reporting live, consentendo agli utenti del percorso di perfezionare la progettazione del percorso.


>[!CAUTION]
>
>Le autorizzazioni per avviare l&#39;esecuzione in prova sono limitate agli utenti con l&#39;autorizzazione di alto livello **[!DNL Publish journeys]**. Le autorizzazioni per interrompere l&#39;esecuzione in prova sono limitate agli utenti con l&#39;autorizzazione di alto livello **[!DNL Manage journeys]**. Ulteriori informazioni sulla gestione dei diritti di accesso degli utenti [!DNL Journey Optimizer] in [questa sezione](../administration/permissions-overview.md).


## Guardrail e limitazioni {#journey-dry-run-limitations}

* La modalità di esecuzione in prova non è disponibile per i percorsi contenenti eventi di reazione.
* I profili in modalità di esecuzione in prova vengono conteggiati per i profili coinvolgibili.
* I percorsi di esecuzione in prova non influiscono sulle regole aziendali.
* Durante la creazione di una nuova versione del percorsi percorso, se una versione precedente è **Live**, l&#39;attivazione dell&#39;esecuzione di prova non è consentita per la nuova versione.
* L’esecuzione di prova del percorso genera stepEvents. Questi stepEvents hanno un flag specifico e un ID esecuzione di prova:
   * `_experience.journeyOrchestration.stepEvents.inDryRun` restituisce `true` se l&#39;esecuzione di prova è attivata e `false` in caso contrario
   * `_experience.journeyOrchestration.stepEvents.dryRunID` restituisce l&#39;ID di un&#39;istanza di esecuzione di prova
* Durante il funzionamento a secco, il percorso viene eseguito con le seguenti specificità:

   * **I nodi dell&#39;azione del canale**, comprese le notifiche e-mail, SMS o push, non vengono eseguiti.
   * **Le azioni personalizzate** sono disabilitate durante l&#39;esecuzione di prova e le relative risposte sono impostate su null.
   * **I nodi di attesa** vengono ignorati durante l&#39;esecuzione di prova.
     <!--You can override the wait block timeouts, then if you have wait blocks duration longer than allowed dry run journey duration, then that branch will not execute completely.-->
   * **Le origini dati**, incluse le origini dati esterne, vengono eseguite per impostazione predefinita.

## Avvia un&#39;esecuzione di prova {#journey-dry-run-start}

Potete utilizzare la funzionalità di esecuzione di prova in qualsiasi percorso 2D senza errori.

Per attivare l&#39;esecuzione in prova, effettuare le seguenti operazioni:

1. Aprire il percorso che si desidera verificare.
1. Fare clic sul pulsante **Esegui**.

   ![Avvia l&#39;esecuzione di prova del percorso](assets/dry-run-button.png)

1. Conferma la pubblicazione

   Durante la transizione viene visualizzato il messaggio di stato **Attivazione dell&#39;esecuzione di prova**.

1. Dopo l&#39;attivazione, il percorso entra in modalità **Esecuzione a secco**.

## Monitorare un’esecuzione in prova {#journey-dry-monitor}

Una volta avviata la pubblicazione in modalità Asciutto, puoi visualizzare l’esecuzione del percorso e il modo in cui i profili progrediscono attraverso rami e nodi del percorso.

Le metriche vengono visualizzate direttamente nell’area di lavoro del percorso.

![Monitorare l&#39;esecuzione di prova del percorso](assets/dry-run-metrics.png)

Per ogni attività, puoi controllare:

* **[!UICONTROL Immesso]**: numero totale di singoli utenti che hanno iniziato questa attività.
* **[!UICONTROL Uscita (ha soddisfatto i criteri di uscita)]**: numero totale di persone che sono uscite dal percorso da tale attività, a causa di un criterio di uscita.
* **[!UICONTROL Uscita (uscita forzata)]**: numero totale di individui che sono usciti dal percorso mentre era in pausa a causa di una configurazione di percorso da parte di un operatore. Questa metrica è sempre uguale a zero per i percorsi in modalità di esecuzione a secco.
* **[!UICONTROL Errore]**: numero totale di persone che hanno avuto un errore in quell&#39;attività.


A livello di percorso, puoi controllare:

* Numero totale di **profili immessi**
* Numero totale di **profili in uscita**
* Numero totale di **profili in errore**
* Numero totale di **profili scartati** nel percorso

È inoltre possibile accedere ai **report delle ultime 24 ore** e ai **report delle ultime 24 ore** per l&#39;esecuzione di prova. Per accedere a questi report, fare clic sul pulsante **Visualizza report** nell&#39;angolo superiore destro dell&#39;area di lavoro del percorso.

![Accedere ai report per l&#39;esecuzione a secco del percorso](assets/dry-run-report.png)

>[!CAUTION]
>
> I dati di reporting sono disponibili solo quando l&#39;esecuzione di prova è **attiva**.  Una volta interrotti, i dati di reporting non saranno più accessibili. Utilizza il pulsante **Esporta** sopra i report per scaricarli, se necessario.


## Interrompere un&#39;esecuzione di prova {#journey-dry-run-stop}

I percorsi di esecuzione di prova **devono** essere interrotti manualmente.

Fai clic sul pulsante **Chiudi** per terminare il test e confermare.

<!-- After 14 days, Dry run journeys automatically transition to the **Draft** status.-->
