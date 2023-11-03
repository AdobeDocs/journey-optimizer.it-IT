---
solution: Journey Optimizer
product: journey optimizer
title: Rapporto globale della campagna
description: Scopri come utilizzare i dati del rapporto globale della campagna
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: fa64f5b8-75f2-40e6-8566-5766fafe6cd6
source-git-commit: 2e8476636fafcba77cbd25ca13324652178224ed
workflow-type: tm+mt
source-wordcount: '3192'
ht-degree: 29%

---

# Rapporto globale della campagna {#campaign-global-report}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_report"
>title="Rapporto globale della campagna"
>abstract="Il rapporto globale delle campagne consente di misurare l’impatto di una campagna in un periodo di tempo selezionato. Il rapporto è suddiviso in diversi widget che descrivono il successo e gli errori della campagna. Ogni dashboard di reporting può essere modificata ridimensionando o spostando i widget."

Rapporti globali, accessibili dalla **Sempre** , visualizza gli eventi che si sono verificati almeno due ore fa e copre gli eventi in un periodo di tempo selezionato. Al confronto, i rapporti live si concentrano sugli eventi che si sono verificati nelle ultime 24 ore, con un intervallo di tempo minimo di due minuti dall’occorrenza dell’evento.

Il rapporto globale della campagna è accessibile direttamente dalla campagna con **[!UICONTROL Visualizza rapporto]** pulsante.

![](assets/campaign_report_global_5.png)

La campagna **[!UICONTROL Rapporto globale]** La pagina verrà visualizzata con le seguenti schede:

* [Campaign](#campaign-global)
* [E-mail](#email-global)
* [In-app](#inapp-global)
* [Push](#push-global)
* [SMS](#sms-global)
* [Web](#web-tab)
* [Direct mail](#direct-mail-global)

La campagna **[!UICONTROL Rapporto globale]** è diviso in diversi widget che descrivono nel dettaglio il successo e gli errori della campagna. Ogni widget può essere ridimensionato ed eliminato, se necessario. Per ulteriori informazioni, consulta questa [sezione](../reports/global-report.md#modify-dashboard).

Per un elenco dettagliato di tutte le metriche disponibili in Adobe Journey Optimizer, consulta [questa pagina](global-report.md#list-of-components-global.md)

## Scheda Campagna {#campaign-global}

### Distribuzione {#delivery-global}

>[!CONTEXTUALHELP]
>id="ajo_campaign_delivery_global"
>title="Statistiche della campagna"
>abstract="Il widget Statistiche della campagna descrive le informazioni principali relative alla campagna, ad esempio i profili immessi e le azioni consegnate."

![](assets/campaign_report_global_1.png)

Il **[!UICONTROL Statistiche della campagna]** widget fornisce dettagli sulle informazioni principali relative alla campagna:

* **[!UICONTROL Profili immessi]**: numero di profili che hanno avviato il percorso.

* **[!UICONTROL Azioni consegnate]**: numero totale di volte in cui è stata consegnata un’azione nel percorso.

* **[!UICONTROL Azioni non riuscite in %]**: numero totale di volte in cui un’azione non è riuscita nel percorso rispetto al numero totale di volte in cui è stata consegnata un’azione.

<!--
### Objectives report {#objectives-global}

![](assets/performance_report.gif)

The **[!UICONTROL Objectives]** tab allows you to better fine-tune your deliveries' reports by targeting one specific metric.

The **[!UICONTROL Objectives]** listed are linked to **[!UICONTROL Datasets]** that define a connection to a system in order to retrieve additional information. A list of built-in **[!UICONTROL Objectives]** is available but you can add your own by adding new **[!UICONTROL Dataset]**. For the detailed procedure, refer to this [section](../campaigns/reporting-configuration.md).

After selecting the Objectives you want to target on, the two **[!UICONTROL Performance overview]** and **[!UICONTROL Campaign objective]** widgets will provide a detailed summary of your delivery performance. 

With the **[!UICONTROL Campaign objective]** widget, you can also choose to compare your main objective with another metric.
-->

### Rapporto sulla sperimentazione {#experimentation-global}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_click"
>title="Metrica Successo"
>abstract="Valore totale della metrica Successo, precedentemente selezionata durante la creazione degli esperimenti, diviso per il numero di profili."

![](assets/experimentation_report_3.png)

Il **[!UICONTROL Sperimentazione]** fornisce informazioni chiave sulle prestazioni di ciascuna variante e identifica quella di maggior successo.

La definizione dell&#39;esecutore migliore potrebbe richiedere un po&#39; di tempo, sarà rappresentata da questa icona ![](assets/experimentation_report_1.png).

+++Ulteriori informazioni sulle diverse metriche e widget disponibili per il rapporto Sperimentazione.

Il **[!UICONTROL Risultato esperimento]** il widget descrive le prestazioni di ogni variante. È possibile modificare la linea di base selezionando uno dei trattamenti tra **[!UICONTROL Linea di base]** il menu a discesa. Il miglior trattamento sarà rappresentato da un’icona a forma di stella.

La tabella presenta le metriche seguenti:

* **[!UICONTROL Incremento rispetto alla linea di base]**: misura del miglioramento percentuale del tasso di conversione di un dato trattamento rispetto al basale.

* **[!UICONTROL Affidabilità]**: evidenza che un dato trattamento è uguale al trattamento di base. [Ulteriori informazioni](../campaigns/experiment-calculations.md#understand-confidence)

* **[!UICONTROL Clic in uscita univoci]**: numero totale di clic tra i canali in uscita.

* **[!UICONTROL Profili]**: numero di profili target per questo trattamento.

* **[!UICONTROL Clic/profili in uscita univoci]**: valore totale della metrica di successo, precedentemente selezionata durante la creazione degli esperimenti, diviso per il numero di profili.

Il **[!UICONTROL Intervallo di affidabilità]** Il grafico misura l’incertezza riguardo al miglioramento. Descrive la differenza percentuale nelle prestazioni tra la linea di base e il trattamento dalle prestazioni migliori. [Ulteriori informazioni](../campaigns/experiment-calculations.md#confidence-intervals).

![](assets/experimentation_report_4.png)

L&#39;ultimo widget fornisce dati relativi al **[!UICONTROL Metrica di successo]** ha selezionato in precedenza per i trattamenti. È possibile selezionare una metrica di destinazione diversa dalla **[!UICONTROL Metrica]** menu a discesa per tenere traccia dei dati alternativi.

>[!CAUTION]
>
>Quando lavori con metriche filtrate per sperimentazione, tieni presente che la modifica della selezione della metrica dal menu a discesa nella pagina di confronto per la sperimentazione non manterrà il valore del filtro. Ad esempio, il passaggio da &quot;Clic&quot; a &quot;Clic univoci&quot; causerà la perdita del filtro applicato, rendendo il confronto impreciso o non valido.

+++

Per informazioni approfondite su questi risultati e su come interpretarli, consulta [questa pagina](../campaigns/get-started-experiment.md#interpret-results).

## Scheda e-mail {#email-global}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_sending_statistics"
>title="E-mail - Statistiche di invio"
>abstract="La tabella della sezione E-mail - Statistiche di invio riepiloga dati essenziali sulle e-mail, ad esempio Target o Consegnati."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_tracking_statistics"
>title="E-mail - Statistiche di tracciamento"
>abstract="La tabella della sezione E-mail - Statistiche di tracciamento e-mail fornisce i dati sulle attività dei profili per l’e-mail."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_sending_performance"
>title="E-mail - Prestazioni di invio"
>abstract="Il grafico della sezione E-mail - Prestazioni di invio presenta dati completi sulle e-mail inviate, fornendo insight su metriche chiave quali consegne e mancati recapiti e consentendo un’analisi dettagliata del processo di consegna delle e-mail."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_bounce_categories"
>title="E-mail - Categorie di mancato recapito"
>abstract="I grafici e la tabella della sezione E-mail - Categorie di mancato recapito forniscono dati su errori temporanei e permanenti."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_bounce_reasons"
>title="E-mail - Motivi di mancato recapito"
>abstract="I grafici e la tabella della sezione E-mail - Motivi di mancato recapito contengono i dati disponibili relativi ai messaggi non recapitati."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_error_reasons"
>title="E-mail - Motivi di errore"
>abstract="I grafici e la tabella della sezione E-mail - Motivi di errore consentono di identificare gli errori specifici che si sono verificati durante l’invio."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_excluded_reasons"
>title="E-mail - Motivi di esclusione"
>abstract="I grafici e la tabella della sezione Motivi di esclusione illustrano i vari fattori a causa dei quali il messaggio non è stato ricevuto dai profili utente che sono stati esclusi dal pubblico target."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_top_url"
>title="E-mail - URL principale"
>abstract="Il grafico e la tabella della sezione E-mail - URL principale offrono una panoramica completa degli URL all’interno dell’e-mail che vengono visitati di più, consentendoti di individuare i collegamenti più popolari."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_email_best_recipient"
>title="E-mail - Dominio destinatario migliore"
>abstract="Il grafico e la tabella della sezione E-mail - Dominio destinatario migliore forniscono un raggruppamento dettagliato dei domini utilizzati più di frequente dai destinatari per aprire l’e-mail e insight sul comportamento dei destinatari."

![](assets/campaign_report_global_2.png)

Dalla campagna **[!UICONTROL Rapporto globale]**, il **[!UICONTROL E-mail]** Questa scheda contiene le informazioni principali relative alle consegne e-mail inviate nella campagna.

+++Ulteriori informazioni sulle diverse metriche e widget disponibili per il rapporto e-mail.

Il **[!UICONTROL Statistiche di invio e-mail]** il grafico descrive il successo della tua e-mail:

* **[!UICONTROL Target]**: numero totale di messaggi elaborati durante il processo di invio.

* **[!UICONTROL Inviato]**: numero totale di invii per e-mail.

* **[!UICONTROL Consegnato]**: numero di messaggi inviati correttamente rispetto al numero totale di messaggi inviati.

* **[!UICONTROL Percentuale di consegna]**: percentuale di messaggi inviati correttamente.

* **[!UICONTROL Mancati recapiti]**: totale degli errori accumulati durante il processo di invio e l’elaborazione automatica della restituzione in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Percentuale non recapitate]**: percentuale di e-mail non recapitate rispetto alle e-mail inviate.

* **[!UICONTROL Errori]**: numero totale di errori che si sono verificati durante il processo di invio e che ne hanno impedito l’invio ai profili.

* **[!UICONTROL Frequenza errori]**: percentuale di errori che si sono verificati durante il processo di invio e che ne hanno impedito l’invio, rispetto alle e-mail inviate.

* **[!UICONTROL Nuovi tentativi]**: numero di e-mail nella coda per i nuovi tentativi.

* **[!UICONTROL Escluso]**: numero di profili che sono stati esclusi da Adobe Journey Optimizer.

Il **[!UICONTROL E-mail - Statistiche di tracciamento]** il widget contiene i dati disponibili per l’attività profilo per l’e-mail:

* **[!UICONTROL Aperture]**: numero di volte in cui l’e-mail è stata aperta.

* **[!UICONTROL Aperture univoche]**: percentuale di e-mail aperte.

* **[!UICONTROL Percentuale aperture]**: numero totale di e-mail aperte rispetto al numero di e-mail consegnate.

* **[!UICONTROL Clic]**: numero di volte in cui è stato fatto clic su un contenuto in un’e-mail.

* **[!UICONTROL Clic univoci]**: numero di profili che hanno fatto clic su un contenuto in un messaggio e-mail.

* **[!UICONTROL Percentuale clic univoci]**: percentuale di utenti che hanno interagito con il messaggio e-mail.

* **[!UICONTROL Annullamenti iscrizione]**: numero di clic sul collegamento di annullamento dell’abbonamento.

* **[!UICONTROL Reclami spam]**: numero di volte in cui un messaggio è stato dichiarato come spam o posta indesiderata.

Il **[!UICONTROL Prestazioni di invio]** il grafico contiene i dati disponibili per le e-mail inviate, ad esempio:

* **[!UICONTROL Consegnato]**: numero di messaggi inviati correttamente rispetto al numero totale di messaggi inviati.

* **[!UICONTROL Mancati recapiti]**: totale degli errori accumulati durante il processo di invio e l’elaborazione automatica della restituzione in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Nuovi tentativi]**: numero di e-mail nella coda per i nuovi tentativi.

* **[!UICONTROL Errori]**: numero totale di errori che si sono verificati durante il processo di invio e che ne hanno impedito l’invio ai profili.

Il **[!UICONTROL Motivi di mancato recapito]** e **[!UICONTROL Categorie di mancato recapito]** I widget contengono i dati disponibili relativi ai messaggi non recapitati, ad esempio:

* **[!UICONTROL Mancato recapito permanente]**: numero totale di errori permanenti, ad esempio un indirizzo e-mail errato. Ciò comporta un messaggio di errore che indica esplicitamente che l’indirizzo non è valido, ad esempio Utente sconosciuto.

* **[!UICONTROL Mancato recapito non permanente]**: numero totale di errori temporanei, ad esempio una casella in entrata completa.

* **[!UICONTROL Ignorato]**: numero totale di messaggi temporanei, ad esempio Fuori sede, o un errore tecnico, ad esempio se il tipo di mittente è postmaster.

Per ulteriori informazioni sui mancati recapiti, consulta [Elenco di soppressione](../reports/suppression-list.md) pagina.

Il **[!UICONTROL Motivi di errore]** Il grafico e la tabella consentono di vedere quale errore si è verificato durante il processo di invio.

Il **[!UICONTROL Motivi di esclusione]** il grafico e la tabella mostrano i diversi motivi che hanno impedito ai profili utente, esclusi dai profili target, di ricevere il messaggio.

Il **[!UICONTROL E-Mail - URL principale]** il grafico e la tabella indicano gli URL più visitati del tuo indirizzo e-mail.

Il **[!UICONTROL E-mail - Dominio destinatario principale]** il grafico e la tabella indicano i domini più utilizzati dai profili per aprire l’e-mail.

>[!CAUTION]
>
> Il **[!UICONTROL E-mail - Dominio destinatario principale]** widget ha una percentuale di precisione del 99,95%.

Il **[!UICONTROL Ottimizzato e non ottimizzato]** il grafico descrive le informazioni principali relative al messaggio, ottimizzate o meno:

* **[!UICONTROL Inviato]**: numero totale di invii.

* **[!UICONTROL Aperture]**: numero di volte in cui il messaggio è stato aperto.

* **[!UICONTROL Clic]**: numero di volte in cui è stato fatto clic su un contenuto in un’e-mail.

Il **[!UICONTROL Ottimizzazione del tempo di invio]** Il completamento dell’e-mail dipende dal metodo di invio: ottimizzato o normale.

* **[!UICONTROL Consegnato]**: numero di messaggi inviati correttamente rispetto al numero totale di messaggi inviati.

* **[!UICONTROL Mancati recapiti]**: totale degli errori accumulati durante il processo di invio e l’elaborazione automatica della restituzione in relazione al numero totale di messaggi inviati.

>[!NOTE]
>
>Il **[!UICONTROL Ottimizzato e non ottimizzato]** e **[!UICONTROL Ottimizzazione del tempo di invio]**  I widget sono disponibili solo se per l’e-mail è attivata l’opzione Ottimizzazione ora di invio. Per ulteriori informazioni sull’ottimizzazione dell’ora di invio, consulta [questa pagina](../building-journeys/journeys-message.md#send-time-optimization).

+++

## Scheda in-app {#inapp-global}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_inapp_performance"
>title="Prestazioni in-app"
>abstract="I KPI (Key Performance Indicator) in-app forniscono informazioni essenziali sul coinvolgimento dei visitatori con i messaggi in-app."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_inapp_interactions"
>title="Interazioni per tipo"
>abstract="Le Interazioni per tipo rappresentano grafici e tabelle che descrivono il modo in cui gli utenti hanno interagito con il messaggio in-app tracciando eventuali clic, eliminazioni o interazioni."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_inapp_summary"
>title="Riepilogo in-app"
>abstract="Il grafico di riepilogo in-app illustra la progressione delle impression e delle interazioni in-app nel periodo specificato."

Dalla campagna **[!UICONTROL Rapporto globale]**, il **[!UICONTROL In-app]** Questa scheda contiene le informazioni principali relative alle consegne in-app inviate nella campagna.

![](assets/campaign_report_global_6.png)

+++Ulteriori informazioni sulle diverse metriche e widget disponibili per il rapporto in-app.

Il **[!UICONTROL Prestazioni in-app]** I KPI descrivono le informazioni principali relative al coinvolgimento dei visitatori con i messaggi in-app, ad esempio:

* **[!UICONTROL Impression univoche]**: numero di utenti univoci a cui è stato recapitato il messaggio in-app.

* **[!UICONTROL Impression]**: numero totale di messaggi in-app consegnati a tutti gli utenti.

* **[!UICONTROL Tasso di interazioni]**: percentuale di accordi con il messaggio in-app. Ciò include tutte le azioni intraprese dagli utenti, come clic, revoche o qualsiasi altra interazione.

Il **[!UICONTROL Interazioni per tipo]** grafici e tabelle dettagliano il modo in cui gli utenti interagivano con il messaggio in-app tracciando i clic, le eliminazioni o le interazioni.

Il **[!UICONTROL Riepilogo in-app]** Il grafico mostra l’evoluzione delle impression e delle interazioni in-app per il periodo in questione.
+++

## Scheda notifica push {#push-global}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_sending_statistics"
>title="Notifica push - Statistiche di invio"
>abstract="La tabella Statistiche di invio delle notifiche push riepiloga i dati essenziali sulle notifiche push, come i messaggi di mirati o recapitati."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_tracking_statistics"
>title="Notifica push - Statistiche di tracciamento"
>abstract="Le statistiche di tracciamento push forniscono dati sulle attività dei profili per le notifiche push."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_sending_summary"
>title="Notifica push - Riepilogo di invio"
>abstract="Il grafico Riepilogo invio notifiche push visualizza i dati disponibili per le notifiche push inviate."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_excluded_reasons"
>title="Notifica push - Motivi di esclusione"
>abstract="I grafici e la tabella dei motivi di esclusione illustrano i vari fattori che hanno portato ai profili utente, esclusi dal pubblico mirato, a non ricevere il messaggio."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_error_reasons"
>title="Notifica push - Motivi di errore"
>abstract="I grafici e la tabella Motivi di errore consentono di identificare gli errori specifici che si sono verificati durante il processo di invio."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_push_breakdown_platform"
>title="Notifica push - Raggruppamento per piattaforma"
>abstract="La tabella e i grafici della sezione Raggruppamento per piattaforma forniscono un riepilogo del successo delle notifiche push in base al sistema operativo del profilo."

Dalla campagna **[!UICONTROL Rapporto globale]**, il **[!UICONTROL Notifica push]** La scheda descrive le informazioni principali relative alle consegne push inviate nella campagna.

![](assets/campaign_report_global_3.png)I KPI relativi alle prestazioni in-app descrivono nel dettaglio le informazioni principali relative al coinvolgimento dei visitatori con i messaggi in-app.

+++Ulteriori informazioni sulle diverse metriche e widget disponibili per il rapporto push.

Il **[!UICONTROL Notifica push - Statistiche di invio]** la tabella descrive le informazioni principali relative alle notifiche push

* **[!UICONTROL Target]**: numero totale di messaggi elaborati durante l’analisi.

* **[!UICONTROL Inviato]**: numero totale di invii per la notifica push.

* **[!UICONTROL Consegnato]**: numero di messaggi inviati correttamente rispetto al numero totale di messaggi inviati.

* **[!UICONTROL Percentuale di consegna]**: percentuale di messaggi inviati correttamente.

* **[!UICONTROL Mancati recapiti]**: totale degli errori accumulati durante il processo di invio e l’elaborazione automatica della restituzione in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Percentuale non recapitate]**: percentuale di notifiche push non recapitate rispetto alle notifiche push inviate.

* **[!UICONTROL Errori]**: numero totale di errori che ne hanno impedito l’invio ai profili.

* **[!UICONTROL Frequenza errori]**: percentuale di errori che si sono verificati durante il blocco dell’invio rispetto alle notifiche push inviate.

* **[!UICONTROL Escluso]**: numero di profili che sono stati esclusi da Adobe Journey Optimizer.

Il **[!UICONTROL Push - Statistiche di tracciamento]** contiene i dati disponibili per l’attività profilo per la notifica push:

* **[!UICONTROL Aperture]**: numero di volte in cui la notifica push è stata aperta.

* **[!UICONTROL Percentuale aperture]**: percentuale di notifiche push aperte.

* **[!UICONTROL Azioni]**: numero totale di azioni sulla notifica push consegnata, ad esempio clic su pulsante o rimozione.

* **[!UICONTROL Coinvolgimenti]**: numero totale di aperture e azioni per questa notifica push, ovvero se il profilo ha aperto la notifica push o se è stato fatto clic su un pulsante.

* **[!UICONTROL Tasso di coinvolgimento]**: percentuale di aperture e azioni per questa notifica push, ovvero se il profilo ha aperto la notifica push o se è stato fatto clic su un pulsante.

Il **[!UICONTROL Riepilogo notifiche push]** il grafico contiene i dati disponibili per le notifiche push inviate, ad esempio:

* **[!UICONTROL Aperture]**: numero di volte in cui la notifica push è stata aperta.

* **[!UICONTROL Azioni]**: numero totale di azioni sulla notifica push consegnata, ad esempio clic su pulsante o rimozione.

* **[!UICONTROL Mancati recapiti]**: totale degli errori accumulati e dell’elaborazione automatica della restituzione in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Consegnato]**: numero di messaggi inviati correttamente rispetto al numero totale di messaggi inviati.

* **[!UICONTROL Errori]**: numero totale di errori che ne hanno impedito l’invio ai profili.

>[!NOTE]
>
>Il **[!UICONTROL Ottimizzato e non ottimizzato]** e **[!UICONTROL Ottimizzazione del tempo di invio]**  I widget sono disponibili solo se per la notifica push è attivata l’opzione Ottimizzazione dell’ora di invio. Per ulteriori informazioni sull’ottimizzazione dell’ora di invio, consulta [questa pagina](../building-journeys/journeys-message.md#send-time-optimization).

Il **[!UICONTROL Ottimizzato e non ottimizzato]** il grafico descrive le informazioni principali relative al messaggio, ottimizzate o meno:

* **[!UICONTROL Consegnato]**: numero di messaggi inviati correttamente rispetto al numero totale di messaggi inviati.

* **[!UICONTROL Aperture]**: numero di volte in cui la notifica push è stata aperta.

* **[!UICONTROL Azioni]**: numero totale di azioni sulla notifica push consegnata, ad esempio clic su pulsante o rimozione.

Il **[!UICONTROL Ottimizzazione del tempo di invio]** descrive il successo della notifica push in base al metodo di invio: ottimizzato o normale.

* **[!UICONTROL Consegnato]**: numero di messaggi inviati correttamente rispetto al numero totale di messaggi inviati.

* **[!UICONTROL Mancati recapiti]**: totale degli errori accumulati durante il processo di invio e l’elaborazione automatica della restituzione in relazione al numero totale di messaggi inviati.

Il **[!UICONTROL Motivi di errore]** i grafici e la tabella consentono di vedere quale errore si è verificato.

Il **[!UICONTROL Motivi di esclusione]** i grafici e le tabelle mostrano i diversi motivi che hanno impedito ai profili utente, esclusi dai profili target, di ricevere il messaggio.

Il **[!UICONTROL Raggruppamento per piattaforma]** grafico e tabella descrivono il successo della notifica push in base al sistema operativo del profilo.
+++

## Scheda SMS {#sms-global}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_sending_statistics"
>title="SMS - Statistiche di invio"
>abstract="La tabella Statistiche di invio SMS riepiloga dati essenziali sui messaggi SMS, ad esempio i messaggi mirati o recapitati."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_error_reasons"
>title="SMS - Motivi di errore"
>abstract="I grafici e la tabella della sezione SMS - Motivi di errore consentono di individuare gli errori specifici che si sono verificati durante il processo di invio."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_performance"
>title="SMS - Prestazioni per data"
>abstract="Il widget Prestazioni SMS per data fornisce informazioni chiave sui messaggi tramite una rappresentazione grafica."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_excluded_reasons"
>title="SMS - Motivi di esclusione"
>abstract="I grafici e la tabella dei motivi di esclusione illustrano i vari fattori che hanno portato ai profili utente, esclusi dal pubblico mirato, a non ricevere il messaggio."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_bounces_reasons"
>title="SMS - Motivi di mancato recapito"
>abstract="I grafici e la tabella Motivi di mancato recapito contengono i dati disponibili relativi ai messaggi non recapitati."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_sms_clicks_links"
>title="SMS - Clic per collegamenti"
>abstract="Il widget SMS - Clic per collegamenti fornisce informazioni essenziali sul coinvolgimento dei visitatori con gli URL nei messaggi"

Dalla campagna **[!UICONTROL Rapporto globale]**, il **[!UICONTROL SMS]** Questa scheda fornisce le informazioni principali relative alle consegne di SMS inviate nella campagna.

![](assets/campaign_report_global_4.png)

+++Ulteriori informazioni sulle diverse metriche e widget disponibili per il rapporto SMS.

Il **[!UICONTROL SMS - Statistiche di invio]** la tabella descrive il completamento del messaggio SMS:

* **[!UICONTROL Target]**: numero di profili utente qualificati come profili target.

* **[!UICONTROL Escluso]**: numero di profili utente, esclusi dai profili target, che non hanno ricevuto il messaggio.

* **[!UICONTROL Inviato]**: numero totale di invii per il messaggio SMS.

* **[!UICONTROL Mancati recapiti]**: totale degli errori accumulati durante il processo di invio e l’elaborazione automatica della restituzione in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Errori]**: numero totale di errori che ne hanno impedito l’invio ai profili.

Il **[!UICONTROL Prestazioni SMS per data]** un grafico fornisce dettagli sulle informazioni principali relative al messaggio:

* **[!UICONTROL Inviato]**: numero totale di invii per i messaggi SMS.

* **[!UICONTROL Mancati recapiti]**: totale degli errori accumulati durante il processo di invio e l’elaborazione automatica della restituzione in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Errori]**: numero totale di errori che ne hanno impedito l’invio ai profili.

Il **[!UICONTROL Escludi motivi]** e **[!UICONTROL Motivi di mancato recapito]** e **[!UICONTROL Motivi di errore]** grafici e tabelle consentono di vedere quali errori ed esclusioni si sono verificati durante il processo di invio.

Il **[!UICONTROL SMS - Clic per collegamenti]** i widget descrivono le informazioni principali relative al coinvolgimento dei visitatori con gli URL.

+++

## Scheda web {#web-tab}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_web_performance"
>title="Prestazioni web"
>abstract="I KPI per le prestazioni web forniscono informazioni complete sul coinvolgimento dei visitatori con le esperienze web."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_web_summary"
>title="Riepilogo web"
>abstract="Il grafico Riepilogo web illustra la progressione delle esperienze web, incluse impression, impression univoche e interazioni, nel periodo specificato."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_web_interactions"
>title="Interazioni per elemento"
>abstract="La tabella Interazioni per elemento fornisce informazioni chiave sul coinvolgimento dei visitatori con diversi elementi nelle pagine web."

Dalla campagna **[!UICONTROL Rapporto globale]**, il **[!UICONTROL Web]** Questa scheda fornisce informazioni dettagliate sulle informazioni principali relative alle pagine Web.

![](assets/web-report.png)

+++Ulteriori informazioni sulle diverse metriche e widget disponibili per il rapporto Web.

Il **[!UICONTROL Prestazioni web]** I KPI descrivono le informazioni principali relative al coinvolgimento dei visitatori con le esperienze web, ad esempio:

* **[!UICONTROL Impression univoche]**: numero di utenti univoci a cui è stata consegnata l’esperienza web.

* **[!UICONTROL Impression]**: numero totale di esperienze web consegnate a tutti gli utenti.

* **[!UICONTROL Tasso di interazione]**: percentuale di accordi con la pagina web. Ciò include qualsiasi azione eseguita dagli utenti, ad esempio clic o altre interazioni.

Il **[!UICONTROL Riepilogo web]** il grafico mostra l’evoluzione delle tue esperienze web (impression, impressioni e interazioni uniche) per il periodo in questione.

Il **[!UICONTROL Interazioni per elemento]** la tabella descrive le informazioni principali relative al coinvolgimento dei visitatori con i vari elementi presenti nelle pagine web.
+++

## Scheda direct mail {#direct-mail-global}

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_direct_sending_statistics"
>title="Direct mail - Statistiche di invio"
>abstract="La tabella Statistiche di invio Direct Mail riepiloga i dati essenziali relativi ai messaggi Direct Mail, ad esempio i messaggi mirati o recapitati."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_direct_error_reasons"
>title="Direct mail - Motivi di errore"
>abstract="I grafici e la tabella Direct Mail - Motivi di errore consentono di individuare gli errori specifici che si sono verificati durante il processo di invio."

>[!CONTEXTUALHELP]
>id="ajo_campaign_global_direct_excluded_reasons"
>title="Direct mail - Motivi di esclusione"
>abstract="I grafici e la tabella dei motivi di esclusione di Direct mail illustrano i vari fattori che hanno portato ai profili utente, esclusi dal pubblico mirato, a non ricevere il messaggio."

Dalla campagna **[!UICONTROL Rapporto globale]**, il **[!UICONTROL Direct mail]** Questa scheda contiene le informazioni principali relative alle consegne Direct mailing.

![](assets/direct-mail-report_1.png)

+++Ulteriori informazioni sulle diverse metriche e widget disponibili per il rapporto Direct mail.

Il **[!UICONTROL Direct mailing - Statistiche di invio]** la tabella descrive il successo della direct mailing:

* **[!UICONTROL Target]**: numero di profili utente qualificati come profili target per questa direct mailing.

* **[!UICONTROL Inviato]**: numero totale di invii per questa direct mailing.

* **[!UICONTROL Errori]**: numero totale di errori che si sono verificati durante il processo di invio e che ne hanno impedito l’invio ai profili.

* **[!UICONTROL Escluso]**: numero di profili utente, esclusi dai profili target, che non hanno ricevuto la direct mailing.

Il **[!UICONTROL Direct mailing - Motivi di esclusione]** e **[!UICONTROL Direct mailing - Motivi di errore]** grafici e tabelle consentono di vedere quali errori ed esclusioni si sono verificati durante il processo di invio.
+++

## Risorse aggiuntive

* [Introduzione alle campagne](../campaigns/get-started-with-campaigns.md)
* [Creare una campagna](../campaigns/create-campaign.md)
* [Creare campagne attivate da API](../campaigns/api-triggered-campaigns.md)
* [Modificare o interrompere una campagna](../campaigns/modify-stop-campaign.md)
* [Rapporto live della campagna](campaign-live-report.md)
