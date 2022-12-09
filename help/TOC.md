---
product: Journey Optimizer
audience: end-user
user-guide-title: Guida di Journey Optimizer
user-guide-description: Utilizza Journey Optimizer per creare e distribuire esperienze personalizzate, contestuali e connesse ai tuoi clienti
type: Documentation
solution: Journey Optimizer
source-git-commit: c6498633fdfdc9442203a3bf980f1b12bd1c6a6b
workflow-type: tm+mt
source-wordcount: '1297'
ht-degree: 0%

---

# Guida di Adobe Journey Optimizer {#using}

+ [Documentazione di Journey Optimizer](ajo-home.md)
+ Cosa c&#39;è di nuovo? {#whats-new}
   + [Note sulla versione più recente](using/rn/release-notes.md)
   + Note sulla versione precedenti {#previous-rn-new}
      + [Note sulla versione 2022](using/rn/release-notes-2022.md)
      + [Note sulla versione 2021](using/rn/release-notes-2021.md)
   + [Aggiornamenti alla documentazione](using/rn/documentation-updates.md)
+ Introduzione{#get-started}
   + [Cos’è Journey Optimizer](using/start/get-started.md)
   + Guide rapide{#quick-start}
      + [Panoramica](using/start/quick-start.md)
      + [Introduzione come addetto al marketing](using/start/path/marketer.md)
      + [Guida introduttiva a Data Engineer](using/start/path/data-engineer.md)
      + [Introduzione come amministratore](using/start/path/administrator.md)
      + [Guida introduttiva come sviluppatore](using/start/path/developer.md)
   + [Interfaccia utente](using/start/user-interface.md)
   + [Integrazioni](using/start/ajo-integrations.md)
   + [Guardrail](using/start/guardrails.md)
+ Percorsi {#orchestrate-journeys}
   + [Guida introduttiva ai percorsi](using/building-journeys/journey.md)
   + Creare un percorso{#create-journey}
      + [Creare il primo percorso](using/building-journeys/journey-gs.md)
      + [Progettazione del percorso](using/building-journeys/using-the-journey-designer.md)
      + [Testare il percorso](using/building-journeys/testing-the-journey.md)
      + [Pubblicare il percorso](using/building-journeys/publishing-the-journey.md)
   + Gestire i percorsi{#mannage-journey}
      + [Termina il percorso](using/building-journeys/end-journey.md)
      + [Gestione del fuso orario](using/building-journeys/timezone-management.md)
      + [Gestione dell’ingresso del profilo](using/building-journeys/entry-management.md)
      + [Copiare un percorso in un’altra sandbox](using/building-journeys/copy-to-sandbox.md)
      + [Risolvere i problemi del percorso](using/building-journeys/troubleshooting.md)
      + [Integrazione con i servizi intelligenti](using/building-journeys/ai-services-overview.md)
   + Attività {#about-journey-building}
      + [Guida introduttiva alle attività del percorso](using/building-journeys/about-journey-activities.md)
      + [Eventi generali](using/building-journeys/general-events.md)
      + [Reazione](using/building-journeys/reaction-events.md)
      + [Qualificazione di un segmento](using/building-journeys/segment-qualification-events.md)
      + [Condizione](using/building-journeys/condition-activity.md)
      + [Wait](using/building-journeys/wait-activity.md)
      + [Leggi segmento](using/building-journeys/read-segment.md)
      + [E-mail, SMS, push](using/building-journeys/journeys-message.md)
      + [Azioni personalizzate](using/building-journeys/using-custom-actions.md)
      + [Azioni di Adobe Campaign Standard](using/building-journeys/using-adobe-campaign-standard.md)
      + [Azioni Adobe Campaign v7/v8](using/building-journeys/using-adobe-campaign-classic.md)
      + [Salto](using/building-journeys/jump.md)
      + [Aggiorna profilo](using/building-journeys/update-profiles.md)
   + Creare espressioni {#building-advanced-conditions-journeys}
      + [Panoramica](using/building-journeys/expression/expressionadvanced.md)
      + Sintassi {#syntax}
         + [Generalità](using/building-journeys/expression/generalities.md)
         + [Istruzione condizionale](using/building-journeys/expression/conditional-instruction.md)
         + [Tipi di dati](using/building-journeys/expression/data-types.md)
         + [Riferimenti campo](using/building-journeys/expression/field-references.md)
         + [Funzioni di gestione delle raccolte](using/building-journeys/expression/collection-management-functions.md)
         + [Operatori](using/building-journeys/expression/operators.md)
         + [Proprietà del percorso](using/building-journeys/expression/journey-properties.md)
         + [Esempi](using/building-journeys/expression/advanced-editor-use-cases.md)
      + Funzioni {#main-functions-journey}
         + [Funzioni principali](using/building-journeys/expression/functions.md)
         + Adobe Experience Platform {#adobe-experience-platform}
            + [inSegment](using/building-journeys/functions/functioninsegment.md)
         + Aggregazione {#aggregation}
            + [avg](using/building-journeys/functions/functionavg.md)
            + [count](using/building-journeys/functions/functioncount.md)
            + [countOnlyNull](using/building-journeys/functions/functioncountonlynull.md)
            + [countWithNull](using/building-journeys/functions/functioncountwithnull.md)
            + [distinctCount](using/building-journeys/functions/functiondistinctcount.md)
            + [distinctCountWithNull](using/building-journeys/functions/functiondistinctcountwithnull.md)
            + [max](using/building-journeys/functions/functionmax.md)
            + [min](using/building-journeys/functions/functionmin.md)
            + [sum](using/building-journeys/functions/functionsum.md)
         + Conversione {#conversion}
            + [toBool](using/building-journeys/functions/functiontobool.md)
            + [toDateOnly](using/building-journeys/functions/functiontodateonly.md)
            + [toDateTime](using/building-journeys/functions/functiontodatetime.md)
            + [toDateTimeOnly](using/building-journeys/functions/functiontodatetimeonly.md)
            + [toDecimal](using/building-journeys/functions/functiontodecimal.md)
            + [toDuration](using/building-journeys/functions/functiontoduration.md)
            + [toInteger](using/building-journeys/functions/functiontointeger.md)
            + [toString](using/building-journeys/functions/functiontostring.md)
         + Data {#date}
            + [currentTime &#x200B; InMillis](using/building-journeys/functions/functioncurrenttimeinmillis.md)
            + [inLastDays](using/building-journeys/functions/functioninlastdays.md)
            + [inLastHours](using/building-journeys/functions/functioninlasthours.md)
            + [inLastMonths](using/building-journeys/functions/functioninlastmonths.md)
            + [inLastYears](using/building-journeys/functions/functioninlastyears.md)
            + [inNextDays](using/building-journeys/functions/functioninnextdays.md)
            + [inNextHours](using/building-journeys/functions/functioninnexthours.md)
            + [inNextMonths](using/building-journeys/functions/functioninnextmonths.md)
            + [inNextYears](using/building-journeys/functions/functioninnextyears.md)
            + [now](using/building-journeys/functions/functionnow.md)
            + [nowWithDelta](using/building-journeys/functions/functionnowwithdelta.md)
            + [setHours](using/building-journeys/functions/functionsethours.md)
            + [setDays](using/building-journeys/functions/functionsetdays.md)
            + [updateTimeZone](using/building-journeys/functions/functionupdatetimezone.md)
         + Elenco {#list}
            + [distinto](using/building-journeys/functions/functiondistinct.md)
            + [distinctWithNull](using/building-journeys/functions/functiondistinctwithnull.md)
            + [filter](using/building-journeys/functions/functionfilter.md)
            + [getListItem](using/building-journeys/functions/functiongetlistitem.md)
            + [in](using/building-journeys/functions/functionin.md)
            + [intersecare](using/building-journeys/functions/functionintersect.md)
            + [limite](using/building-journeys/functions/functionlimit.md)
            + [listSize](using/building-journeys/functions/functionlistsize.md)
            + [serializeList](using/building-journeys/functions/functionserializelist.md)
            + [sort](using/building-journeys/functions/functionsort.md)
         + Matematica {#math}
            + [casuale](using/building-journeys/functions/functionrandom.md)
            + [round](using/building-journeys/functions/functionround.md)
         + Stringa {#string}
            + [concat](using/building-journeys/functions/functionconcat.md)
            + [contain](using/building-journeys/functions/functioncontain.md)
            + [containIgnoreCase](using/building-journeys/functions/functioncontainwithignorecase.md)
            + [endWith](using/building-journeys/functions/functionendwith.md)
            + [endWithIgnorecase](using/building-journeys/functions/functionendwithignorecase.md)
            + [equalIgnoreCase](using/building-journeys/functions/functionequalignorecase.md)
            + [indexOf](using/building-journeys/functions/functionindexof.md)
            + [isEmpty](using/building-journeys/functions/functionisempty.md)
            + [isNotEmpty](using/building-journeys/functions/functionisnotempty.md)
            + [lastIndexOf](using/building-journeys/functions/functionlastindexof.md)
            + [length](using/building-journeys/functions/functionlength.md)
            + [Lower](using/building-journeys/functions/functionlower.md)
            + [matchRegExp](using/building-journeys/functions/functionmatchregexp.md)
            + [quadqualIgnoreCase](using/building-journeys/functions/functionnotequalignorecase.md)
            + [replace](using/building-journeys/functions/functionreplace.md)
            + [replaceAll](using/building-journeys/functions/functionreplaceall.md)
            + [dividere](using/building-journeys/functions/functionsplit.md)
            + [startWith](using/building-journeys/functions/functionstartwith.md)
            + [startWithIgnoreCase](using/building-journeys/functions/functionstartwithignorecase.md)
            + [substr](using/building-journeys/functions/functionsubstr.md)
            + [trim](using/building-journeys/functions/functiontrim.md)
            + [superiore](using/building-journeys/functions/functionupper.md)
            + [uuid](using/building-journeys/functions/functionuuid.md)
   + Casi d’uso {#journey-use-cases}
      + Casi d&#39;uso aziendali {#business-use-cases}
         + [Inviare messaggi multicanale](using/building-journeys/journeys-uc.md)
         + [Inviare un messaggio utilizzando Campaign v7/v8](using/building-journeys/ajo-ac.md)
         + [Inviare un messaggio agli abbonati](using/building-journeys/message-to-subscribers-uc.md)
      + Casi d&#39;uso tecnico {#technical-use-cases}
         + [Trasmettere dinamicamente le raccolte utilizzando azioni personalizzate](using/building-journeys/collections.md)
         + [Incremento delle consegne](using/building-journeys/ramp-up-deliveries-uc.md)
         + [Limitare il throughput con origini dati esterne e azioni personalizzate](using/building-journeys/limit-throughput.md)
+ Campagne{#campaigns}
   + [Guida introduttiva alle campagne](using/campaigns/get-started-with-campaigns.md)
   + [Creare una campagna](using/campaigns/create-campaign.md)
   + [Rivedere e attivare una campagna](using/campaigns/review-activate-campaign.md)
   + [Gestire le campagne](using/campaigns/modify-stop-campaign.md)
   + Esperimento dei contenuti {#content-experiment}
      + [Introduzione all’esperimento sui contenuti](using/campaigns/get-started-experiment.md)
      + [Creazione di un esperimento sul contenuto](using/campaigns/content-experiment.md)
      + [Comprendere i calcoli statistici](using/campaigns/experiment-calculations.md)
      + [Configurare i rapporti sulla sperimentazione](using/campaigns/reporting-configuration.md)
   + [Campagne di trigger tramite API](using/campaigns/api-triggered-campaigns.md)
+ Canale e-mail {#email}
   + [Guida introduttiva alle e-mail](using/email/get-started-email.md)
   + [Creare un messaggio e-mail](using/email/create-email.md)
   + Progettazione di contenuti e-mail {#design-email}
      + [Guida introduttiva alla progettazione delle e-mail](using/email/get-started-email-design.md)
      + Iniziare a creare contenuto {#start-creating-content}
         + [Inizia da zero](using/email/content-from-scratch.md)
         + [Importare il contenuto dell’e-mail](using/email/existing-content.md)
         + [Creare un codice per il proprio contenuto](using/email/code-content.md)
         + [Utilizzare i modelli](using/email/email-templates.md)
      + Progettazione di contenuti {#add-content}
         + [Utilizzare i componenti contenuto](using/email/content-components.md)
         + [Aggiungere collegamenti e tenere traccia dei messaggi](using/email/message-tracking.md)
         + Gestire le risorse {#manage-asset}
            + [Utilizzare le funzioni di base Assets](using/email/assets-essentials.md)
            + [Utilizzare Adobe Stock](using/email/stock.md)
         + [Inserire offerte personalizzate](using/email/add-offers-email.md)
         + [Genera la versione del testo](using/email/text-version-email.md)
         + [Aggiungi una preintestazione](using/email/preheader.md)
      + Modifica stile {#edit-style}
         + [Guida introduttiva allo stile e-mail](using/email/get-started-email-style.md)
         + [Modifica impostazioni di sfondo](using/email/backgrounds.md)
         + [Regolare l’allineamento verticale e la spaziatura](using/email/alignment-and-padding.md)
         + [Definire uno stile per i collegamenti](using/email/styling-links.md)
         + [Aggiungi attributi di stile in linea](using/email/inline-styling.md)
   + [Anteprima e verifica il messaggio e-mail](using/email/preview.md)
   + [Gestire la rinuncia alle e-mail](using/email/email-opt-out.md)
   + Configurare il canale e-mail {#configure-email}
      + [Guida introduttiva alla configurazione delle e-mail](using/email/get-started-email-config.md)
      + [Configurare le impostazioni della superficie e-mail](using/email/email-settings.md)
+ Canale in-app{#in-app}
   + [Guida introduttiva al canale in-app](using/in-app/get-started-in-app.md)
   + [Configurare il canale in-app](using/in-app/inapp-configuration.md)
   + [Creare un messaggio in-app](using/in-app/create-in-app.md)
   + [Progettazione di contenuti in-app](using/in-app/design-in-app.md)
   + [Rapporto in-app](using/in-app/inapp-report.md)
+ Canale di notifica push{#push}
   + [Guida introduttiva alla notifica push](using/push/get-started-push.md)
   + [Creare una notifica push](using/push/create-push.md)
   + [Progettazione della notifica push](using/push/design-push.md)
   + [Invia la notifica push](using/push/send-push.md)
   + Configurare le notifiche push{#push-config}
      + [Notifiche push e Adobe Journey Optimizer](using/push/push-gs.md)
      + [Configurare il canale di notifica push](using/push/push-configuration.md)
+ Canale SMS{#sms}
   + [Guida introduttiva a SMS](using/sms/get-started-sms.md)
   + [Creare un messaggio SMS](using/sms/create-sms.md)
   + [Inviare un messaggio SMS](using/sms/send-sms.md)
   + [Gestire la rinuncia SMS](using/sms/sms-opt-out.md)
   + [Configurare il canale SMS](using/sms/sms-configuration.md)
+ Direct mail {#direct-mail}
   + [Creare una direct mailing](using/direct-mail/create-direct-mail.md)
   + [Configurare la direct mailing](using/direct-mail/direct-mail-configuration.md)
+ Canale web{#web}
   + [Guida introduttiva al canale web](using/web/get-started-web.md)
   + [Creare esperienze web](using/web/create-web.md)
   + [Creare pagine web](using/web/author-web.md)
   + [Estensione Visual Editing Helper](using/web/visual-editing-helper.md)
   + [Generazione rapporti Web](using/web/web-report.md)
+ Pagine di destinazione {#landing-pages}
   + [Guida introduttiva alle pagine di destinazione](using/landing-pages/get-started-lp.md)
   + [Creare una pagina di destinazione](using/landing-pages/create-lp.md)
   + Progettazione di contenuti {#landing-pages-design}
      + [Informazioni sulla progettazione di pagine di destinazione](using/landing-pages/design-lp.md)
      + [Creare il contenuto della pagina di destinazione](using/landing-pages/lp-content.md)
      + [Creare modelli](using/landing-pages/lp-templates.md)
      + [Aggiungi JavaScript personalizzato](using/landing-pages/lp-custom-js.md)
   + [Creare un elenco di iscrizioni](using/landing-pages/subscription-list.md)
   + [Scopri i casi di utilizzo](using/landing-pages/lp-use-cases.md)
   + Configurare le pagine di destinazione {#lp-configuration}
      + [Configurare i sottodomini della pagina di destinazione](using/landing-pages/lp-subdomains.md)
      + [Definire i predefiniti per le pagine di destinazione](using/landing-pages/lp-presets.md)
+ Personalizzazione e contenuto dinamico {#personalized-dynamic-content}
   + Personalizzazione {#personalization}
      + [Guida introduttiva alla personalizzazione](using/personalization/personalize.md)
      + [Contesti di personalizzazione](using/personalization/personalization-contexts.md)
      + Creare espressioni {#build-expressions}
         + [Sintassi di personalizzazione](using/personalization/personalization-syntax.md)
         + Utilizzare l’editor espressioni {#expression-editor}
            + [Informazioni sull’editor espressioni](using/personalization/personalization-build-expressions.md)
            + [Aggiungi attributi ai preferiti](using/personalization/personalization-favorites.md)
            + [Utilizzare espressioni salvate](using/personalization/personalization-library.md)
            + [Convalida della personalizzazione](using/personalization/personalization-validation.md)
         + Funzioni di supporto{#functions}
            + [Guida introduttiva alle funzioni di supporto](using/personalization/functions/functions.md)
            + [Funzioni di aggregazione](using/personalization/functions/aggregation.md)
            + [Funzioni aritmetiche](using/personalization/functions/arithmetic-functions.md)
            + [Array e funzioni elenco](using/personalization/functions/arrays-list.md)
            + [Funzioni data](using/personalization/functions/dates.md)
            + [Funzioni booleane e di confronto](using/personalization/functions/operators.md)
            + [Helper](using/personalization/functions/helpers.md)
            + [Mappare le funzioni](using/personalization/functions/maps.md)
            + [Funzioni dell&#39;oggetto](using/personalization/functions/objects.md)
            + [Funzioni stringa](using/personalization/functions/string.md)
      + Casi d’uso{#personalization-use-cases}
         + [Notifica dello stato dell&#39;ordine](using/personalization/personalization-use-case.md)
         + [E-mail di abbandono carrello](using/personalization/personalization-use-case-helper-functions.md)
   + Contenuto dinamico {#dynamic}
      + [Introduzione al contenuto dinamico](using/personalization/get-started-dynamic-content.md)
      + [Creare regole condizionali](using/personalization/create-conditions.md)
      + [Creare contenuto dinamico](using/personalization/dynamic-content.md)
+ Segmenti, profili e identità{#segment}
   + Segmenti {#segments}
      + [Introduzione ai segmenti](using/segment/about-segments.md)
      + [Creare segmenti](using/segment/creating-a-segment.md)
   + Profili{#profiles}
      + [Guida introduttiva ai profili](using/segment/get-started-profiles.md)
      + [Creare profili di test](using/segment/creating-test-profiles.md)
   + [Identità](using/segment/get-started-identity.md)
   + Componi tipi di pubblico {#audience-orchestration}
      + [Introduzione alla composizione dell’audience](using/segment/get-started-audience-orchestration.md)
      + [Creazione di flussi di lavoro di composizione](using/segment/create-compositions.md)
      + [Lavorare con il quadro di composizione](using/segment/composition-canvas.md)
      + [Accesso e gestione dei tipi di pubblico](using/segment/access-audiences.md)
   + [Utilizzo della licenza](using/segment/license-usage.md)
+ Tracciamento e monitoraggio {#reporting}
   + Report live {#live-report}
      + [Guida introduttiva a Live Report](using/reports/live-report.md)
      + [Rapporto Journey Live](using/reports/journey-live-report.md)
      + [Rapporto Campaign Live](using/reports/campaign-live-report.md)
      + [Rapporto Live sulla pagina di destinazione](using/reports/lp-report-live.md)
      + [Lista sottoscrizioni Live report](using/reports/subscription-report-live.md)
   + Report globale {#global-report}
      + [Guida introduttiva al report globale](using/reports/global-report.md)
      + [Rapporto globale sul percorso](using/reports/journey-global-report.md)
      + [Report globale della campagna](using/reports/campaign-global-report.md)
      + [Rapporto globale sulla pagina di destinazione](using/reports/lp-report-global.md)
      + [Lista di abbonamenti Rapporto globale](using/reports/subscription-report-global.md)
   + Rapporti sul percorso {#reports}
      + [Creare rapporti sui percorsi](using/reports/sharing-overview.md)
      + [Elenco dei campi evento del passaggio](using/reports/sharing-field-list.md)
      + Campi evento del passaggio precedente {#legacy-step-event-fields}
         + [Informazioni sui campi legacy](using/reports/sharing-legacy-fields.md)
         + [Campi del percorso](using/reports/sharing-journey-fields.md)
         + [Campi comuni](using/reports/sharing-common-fields.md)
         + [Campi di esecuzione azione](using/reports/sharing-execution-fields.md)
         + [Campi di recupero dati](using/reports/sharing-fetch-fields.md)
         + [Campi di identità](using/reports/sharing-identity-fields.md)
      + [Esempi di query](using/reports/query-examples.md)
   + Consegna {#deliverability}
      + [Introduzione al recapito messaggi](using/reports/deliverability.md)
      + [Comprendere l&#39;elenco di soppressione](using/reports/suppression-list.md)
   + [Avvisi](using/reports/alerts.md)
   + [Utilizzare Customer Journey Analytics](using/reports/cja-ajo.md)
+ Gestione delle decisioni {#offer-decisioning}
   + Guida introduttiva alla gestione delle decisioni {#get-started-decision}
      + [Informazioni sulla gestione delle decisioni](using/offers/get-started/starting-offer-decisioning.md)
      + [Interfaccia utente](using/offers/get-started/user-interface.md)
      + [Passaggi chiave per creare e gestire le offerte](using/offers/offer-library/key-steps.md)
      + [Caso di utilizzo: inserire offerte in un messaggio e-mail](using/offers/offers-e2e.md)
   + Creare componenti {#create-components}
      + [Creare posizionamenti](using/offers/offer-library/creating-placements.md)
      + [Creare regole decisionali](using/offers/offer-library/creating-decision-rules.md)
      + [Creare tag](using/offers/offer-library/creating-tags.md)
   + Creare classificazioni {#rankings}
      + [Guida introduttiva alle classificazioni](using/offers/ranking/get-started-rankings.md)
      + [Classificazione delle formule](using/offers/ranking/create-ranking-formulas.md)
      + Modelli AI {#ai-models}
         + [Informazioni sui modelli AI](using/offers/ranking/ai-models.md)
         + Tipi di modelli AI {#ai-model-types}
            + [Modello di ottimizzazione automatica](using/offers/ranking/auto-optimization-model.md)
            + [Modello di ottimizzazione personalizzata](using/offers/ranking/personalized-optimization-model.md)
         + Creare modelli AI {#configure-ai-model}
            + [Creare un set di dati per raccogliere gli eventi](using/offers/ranking/create-dataset.md)
            + [Creare un modello AI](using/offers/ranking/create-ranking-strategies.md)
            + [Configurare l’acquisizione di eventi](using/offers/ranking/schema-requirement.md)
   + Creare e gestire le offerte {#managing-offers-in-the-offer-library}
      + Configurare le offerte {#configure-offers}
         + [Creare offerte personalizzate](using/offers/offer-library/creating-personalized-offers.md)
         + [Aggiungi rappresentazioni](using/offers/offer-library/add-representations.md)
         + [Aggiungi vincoli](using/offers/offer-library/add-constraints.md)
      + [Creare offerte di fallback](using/offers/offer-library/creating-fallback-offers.md)
      + [Creare raccolte](using/offers/offer-library/creating-collections.md)
   + Creare e gestire le decisioni {#create-manage-activities}
      + [Creare decisioni](using/offers/offer-activities/create-offer-activities.md)
      + [Configurare la selezione delle offerte nelle decisioni](using/offers/offer-activities/configure-offer-selection.md)
      + [Creare simulazioni](using/offers/offer-activities/simulation.md)
   + [Decisioni in batch](using/offers/batch-delivery.md)
   + Creare rapporti di gestione delle decisioni {#create-reports}
      + [Guida introduttiva agli eventi di gestione delle decisioni](using/offers/reports/get-started-events.md)
      + [Informazioni chiave sugli eventi di Gestione decisioni](using/offers/reports/key-information.md)
      + [Accedere ai campi XDM degli eventi](using/offers/reports/xdm-fields.md)
   + Esportare il catalogo delle offerte {#export-catalog}
      + [Guida introduttiva all’esportazione del catalogo delle offerte ](using/offers/export-catalog/get-started-export.md)
      + [Accedere al catalogo delle offerte esportato](using/offers/export-catalog/access-dataset.md)
      + [Set di dati di offerte personalizzate](using/offers/export-catalog/export-offers.md)
      + [Set di dati sulle decisioni](using/offers/export-catalog/export-decisions.md)
      + [Set di dati sui posizionamenti](using/offers/export-catalog/export-placements.md)
      + [Set di dati di fallback](using/offers/export-catalog/export-fallback.md)
   + Riferimento API {#api-reference}
      + [Introduzione](using/offers/api-reference/getting-started.md)
      + Creare e gestire offerte tramite API {#offers-api}
         + Posizionamenti {#placements}
            + [Elencare posizionamenti](using/offers/api-reference/offers-api/placements/placements-list.md)
            + [Ricercare un posizionamento](using/offers/api-reference/offers-api/placements/lookup.md)
            + [Creare un posizionamento](using/offers/api-reference/offers-api/placements/create.md)
            + [Aggiornare un posizionamento](using/offers/api-reference/offers-api/placements/update.md)
            + [Eliminare un posizionamento](using/offers/api-reference/offers-api/placements/delete.md)
         + Regole decisionali {#decision-rules}
            + [Elencare regole decisionali](using/offers/api-reference/offers-api/decision-rules/rules-list.md)
            + [Ricercare una regola decisionale](using/offers/api-reference/offers-api/decision-rules/lookup.md)
            + [Creare una regola decisionale](using/offers/api-reference/offers-api/decision-rules/create.md)
            + [Aggiornare una regola decisionale](using/offers/api-reference/offers-api/decision-rules/update.md)
            + [Eliminare una regola decisionale](using/offers/api-reference/offers-api/decision-rules/delete.md)
         + Tag {#tags}
            + [Elencare tag](using/offers/api-reference/offers-api/tags/tags-list.md)
            + [Ricercare un tag](using/offers/api-reference/offers-api/tags/lookup.md)
            + [Creare un tag](using/offers/api-reference/offers-api/tags/create.md)
            + [Aggiornare un tag](using/offers/api-reference/offers-api/tags/update.md)
            + [Eliminare un tag](using/offers/api-reference/offers-api/tags/delete.md)
         + Offerte personalizzate {#personalized-offers}
            + [Elencare offerte personalizzate](using/offers/api-reference/offers-api/personalized-offers/offers-list.md)
            + [Ricercare un’offerta personalizzata](using/offers/api-reference/offers-api/personalized-offers/lookup.md)
            + [Creare un’offerta personalizzata](using/offers/api-reference/offers-api/personalized-offers/create.md)
            + [Aggiornare un’offerta personalizzata](using/offers/api-reference/offers-api/personalized-offers/update.md)
            + [Eliminare un’offerta personalizzata](using/offers/api-reference/offers-api/personalized-offers/delete.md)
         + Raccolte {#collections}
            + [Elencare raccolte](using/offers/api-reference/offers-api/collections/collections-list.md)
            + [Ricercare una raccolta](using/offers/api-reference/offers-api/collections/lookup.md)
            + [Creare una raccolta](using/offers/api-reference/offers-api/collections/create.md)
            + [Aggiornare una raccolta](using/offers/api-reference/offers-api/collections/update.md)
            + [Eliminare una raccolta](using/offers/api-reference/offers-api/collections/delete.md)
         + Offerte di fallback {#fallback-offers}
            + [Elencare offerte di fallback](using/offers/api-reference/offers-api/fallback-offers/fallback-list.md)
            + [Ricercare un’offerta di fallback](using/offers/api-reference/offers-api/fallback-offers/lookup.md)
            + [Creare un’offerta di fallback](using/offers/api-reference/offers-api/fallback-offers/create.md)
            + [Aggiornare un’offerta di fallback](using/offers/api-reference/offers-api/fallback-offers/update.md)
            + [Eliminare un’offerta di fallback](using/offers/api-reference/offers-api/fallback-offers/delete.md)
      + Creare e gestire decisioni tramite API {#activities-api}
         + [Elencare le decisioni](using/offers/api-reference/activities-api/activities/activities-list.md)
         + [Ricercare una decisione](using/offers/api-reference/activities-api/activities/lookup.md)
         + [Creare una decisione](using/offers/api-reference/activities-api/activities/create.md)
         + [Aggiornare una decisione](using/offers/api-reference/activities-api/activities/update.md)
         + [Eliminare una decisione](using/offers/api-reference/activities-api/activities/delete.md)
      + Consegnare offerte tramite API {#offer-delivery-api}
         + [Guida introduttiva alle API di consegna delle offerte](using/offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)
         + [Decisioning API](using/offers/api-reference/offer-delivery-api/decisioning-api.md)
         + [API di Edge Decisioning](using/offers/api-reference/offer-delivery-api/edge-decisioning-api.md)
         + [API Batch Decisioning](using/offers/api-reference/offer-delivery-api/batch-decisioning-api.md)
+ Gestione dati {#data-management}
   + [Guida introduttiva alla gestione dei dati](using/data/gs-data.md)
   + [Utilizzare gli schemi](using/data/get-started-schemas.md)
   + Set di dati di Journey Optimizer {#datasets}
      + [Guida introduttiva ai set di dati](using/data/get-started-datasets.md)
      + [Esempi di query](using/data/datasets-query-examples.md)
   + [Query](using/data/get-started-queries.md)
+ Configurazione{#configuration}
   + [Guida introduttiva alla configurazione di Journey Optimizer](using/configuration/get-started-configuration.md)
   + Delega sottodomini e-mail {#delegate-subdomains}
      + [Guida introduttiva alla delega dei sottodomini](using/configuration/about-subdomain-delegation.md)
      + [Delega un sottodominio](using/configuration/delegate-subdomain.md)
      + [Aggiungere un record TXT di Google](using/configuration/google-txt.md)
      + [Accedere e modificare i record PTR](using/configuration/ptr-records.md)
      + [Creare pool IP](using/configuration/ip-pools.md)
   + [Impostare le superfici del canale](using/configuration/channel-surfaces.md)
   + Monitorare gli indirizzi e-mail {#monitor-reputation}
      + [Elenco di eliminazione](using/configuration/manage-suppression-list.md)
      + [Nuovi tentativi](using/configuration/retries.md)
      + [Elenco consentito](using/configuration/allow-list.md)
   + [Supporto per l&#39;archiviazione](using/configuration/archiving-support.md)
   + [Configurare le regole di frequenza](using/configuration/frequency-rules.md)
   + [Gestire gli indirizzi di esecuzione](using/configuration/primary-email-addresses.md)
   + Configurare i percorsi {#configure-journeys}
      + [Informazioni su origini dati, eventi e azioni](using/configuration/about-data-sources-events-actions.md)
      + [Integrazione con sistemi esterni](using/configuration/external-systems.md)
      + Configurazione dell’evento {#events-journeys}
         + [Principio generale](using/event/about-events.md)
         + Configurare un evento unitario {#unitary-events}
            + [Introduzione agli eventi unitari](using/event/about-creating.md)
            + [Informazioni sugli schemi ExperienceEvent](using/event/experience-event-schema.md)
            + [Utilizzo di Adobe Analytics](using/event/about-analytics.md)
         + [Configurare un evento aziendale](using/event/about-creating-business.md)
         + [Passaggi aggiuntivi per l’invio di eventi](using/event/additional-steps-to-send-events-to-journey.md)
      + Configurazione origine dati{#data-source-journeys}
         + [Informazioni sulle origini dati](using/datasource/about-data-sources.md)
         + [Configurare un’origine dati](using/datasource/configure-data-sources.md)
         + [Origine dati Adobe Experience Platform](using/datasource/adobe-experience-platform-data-source.md)
         + [Origini dati esterne](using/datasource/external-data-sources.md)
      + Configurazione azione {#action-journeys}
         + [Informazioni sulle azioni](using/action/action.md)
         + [Configurare un’azione](using/action/about-custom-action-configuration.md)
         + [Integrazione con Adobe Campaign Standard](using/action/acs-action.md)
         + [Integrazione con Adobe Campaign v7/v8](using/action/acc-action.md)
   + [Origini](using/start/get-started-sources.md)
+ Controllo dell&#39;accesso {#access-control}
   + [Panoramica sul controllo degli accessi](using/administration/permissions-overview.md)
   + [Profili di prodotto incorporati](using/administration/ootb-product-profiles.md)
   + [Gestione di utenti e profili di prodotto](using/administration/permissions.md)
   + [Livelli di autorizzazione](using/administration/high-low-permissions.md)
   + [Gestione delle sandbox](using/administration/sandboxes.md)
   + [Controllo dell&#39;accesso basato su attributi](using/administration/attribute-based-access.md)
   + [Controllo dell&#39;accesso a livello di oggetto](using/administration/object-based-access.md)
+ Privacy {#privacy}
   + [Introduzione alla privacy](using/privacy/get-started-privacy.md)
   + [Richieste sulla privacy](using/privacy/requests.md)
   + [Azioni di audit sulle risorse](using/privacy/audit-logs.md)
   + Gestire il consenso {#consent}
      + [Gestire la rinuncia](using/privacy/opt-out.md)
      + [Utilizzare i criteri di consenso](using/action/consent.md)
   + [Governance dei dati](using/action/action-privacy.md)
