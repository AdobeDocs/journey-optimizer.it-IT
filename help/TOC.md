---
product: Journey Optimizer
audience: end-user
user-guide-title: Guida di Journey Optimizer
user-guide-description: Utilizza Journey Optimizer per creare e fornire ai clienti esperienze connesse, contestuali e personalizzate
type: Documentation
solution: Journey Optimizer
source-git-commit: 513fddf21eaf7958df45d97f028103519c77ec44
workflow-type: tm+mt
source-wordcount: '1750'
ht-degree: 99%

---

# Guida di Adobe Journey Optimizer {#using}

+ [Documentazione di Journey Optimizer ](ajo-home.md)
+ Novità {#whats-new}
   + [Note preliminari sulla versione](using/rn/e-release-notes.md)
   + [Note sulla versione più recente](using/rn/release-notes.md)
   + Note sulle versioni precedenti {#previous-rn-new}
      + [Note sulla versione 2023](using/rn/release-notes-2023.md)
      + [Note sulle versioni 2022](using/rn/release-notes-2022.md)
      + [Note sulle versioni 2021](using/rn/release-notes-2021.md)
   + [Aggiornamenti alla documentazione](using/rn/documentation-updates.md)
   + [Nuova area di lavoro del percorso](using/rn/new-canvas.md)
+ Introduzione{#get-started}
   + [Cos’è Journey Optimizer](using/start/get-started.md)
   + Guide rapide{#quick-start}
      + [Panoramica](using/start/quick-start.md)
      + [Introduzione per addetti marketing](using/start/path/marketer.md)
      + [Introduzione per Data Engineer](using/start/path/data-engineer.md)
      + [Introduzione per amministratori](using/start/path/administrator.md)
      + [Introduzione per sviluppatori](using/start/path/developer.md)
   + [Interfaccia utente](using/start/user-interface.md)
   + [Cercare, filtrare, categorizzare](using/start/search-filter-categorize.md)
   + [Accessibilità](using/start/accessibility.md)
   + [Usare i playbook sui casi d’uso](using/start/playbooks.md)
   + [Integrazioni](using/start/ajo-integrations.md)
   + [Guardrail](using/start/guardrails.md)
   + [Best practice](using/start/best-practices.md)
+ Percorsi {#orchestrate-journeys}
   + [Introduzione ai percorsi](using/building-journeys/journey.md)
   + Creare un percorso{#create-journey}
      + [Creare il primo percorso](using/building-journeys/journey-gs.md)
      + [Progettazione del percorso](using/building-journeys/using-the-journey-designer.md)
      + [Test del percorso](using/building-journeys/testing-the-journey.md)
      + [Simulare il percorso](using/building-journeys/journey-simulation.md)
      + [Pubblicare il percorso](using/building-journeys/publishing-the-journey.md)
   + Gestire i percorsi{#manage-journey}
      + [Terminare il percorso](using/building-journeys/end-journey.md)
      + [Gestione del fuso orario](using/building-journeys/timezone-management.md)
      + [Gestione dell’ingresso nel profilo](using/building-journeys/entry-management.md)
      + [Copiare un percorso in un’altra sandbox](using/building-journeys/copy-to-sandbox.md)
      + [Risolvere i problemi di un percorso](using/building-journeys/troubleshooting.md)
      + [Integrare con Intelligent Services](using/building-journeys/ai-services-overview.md)
   + Attività {#about-journey-building}
      + [Introduzione alle attività dei percorsi](using/building-journeys/about-journey-activities.md)
      + [Eventi generali](using/building-journeys/general-events.md)
      + [Reazione](using/building-journeys/reaction-events.md)
      + [Qualifica tipi di pubblico](using/building-journeys/audience-qualification-events.md)
      + [Condizione](using/building-journeys/condition-activity.md)
      + [Attendere](using/building-journeys/wait-activity.md)
      + [Leggere tipi di pubblico](using/building-journeys/read-audience.md)
      + [E-mail, In-app, Push, SMS](using/building-journeys/journeys-message.md)
      + [Azioni personalizzate](using/building-journeys/using-custom-actions.md)
      + [Azioni di Adobe Campaign Standard](using/building-journeys/using-adobe-campaign-standard.md)
      + [Azioni Adobe Campaign v7/v8](using/building-journeys/using-adobe-campaign-v7-v8.md)
      + [Salta](using/building-journeys/jump.md)
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
            + [inAudience](using/building-journeys/functions/functioninaudience.md)
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
            + [currentTime&#x200B;InMillis](using/building-journeys/functions/functioncurrenttimeinmillis.md)
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
            + [distinct](using/building-journeys/functions/functiondistinct.md)
            + [distinctWithNull](using/building-journeys/functions/functiondistinctwithnull.md)
            + [filter](using/building-journeys/functions/functionfilter.md)
            + [getListItem](using/building-journeys/functions/functiongetlistitem.md)
            + [in](using/building-journeys/functions/functionin.md)
            + [intersect](using/building-journeys/functions/functionintersect.md)
            + [limit](using/building-journeys/functions/functionlimit.md)
            + [listSize](using/building-journeys/functions/functionlistsize.md)
            + [serializeList](using/building-journeys/functions/functionserializelist.md)
            + [sort](using/building-journeys/functions/functionsort.md)
         + Matematica {#math}
            + [random](using/building-journeys/functions/functionrandom.md)
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
            + [lunghezza](using/building-journeys/functions/functionlength.md)
            + [lower](using/building-journeys/functions/functionlower.md)
            + [matchRegExp](using/building-journeys/functions/functionmatchregexp.md)
            + [notequalIgnoreCase](using/building-journeys/functions/functionnotequalignorecase.md)
            + [replace](using/building-journeys/functions/functionreplace.md)
            + [replaceAll](using/building-journeys/functions/functionreplaceall.md)
            + [split](using/building-journeys/functions/functionsplit.md)
            + [startWith](using/building-journeys/functions/functionstartwith.md)
            + [startWithIgnoreCase](using/building-journeys/functions/functionstartwithignorecase.md)
            + [substr](using/building-journeys/functions/functionsubstr.md)
            + [trim](using/building-journeys/functions/functiontrim.md)
            + [upper](using/building-journeys/functions/functionupper.md)
            + [uuid](using/building-journeys/functions/functionuuid.md)
   + Casi d’uso {#journey-use-cases}
      + Casi d’uso aziendali {#business-use-cases}
         + [Inviare messaggi multicanale](using/building-journeys/journeys-uc.md)
         + [Inviare un messaggio con Campaign v7/v8](using/building-journeys/ajo-ac.md)
         + [Inviare un messaggio agli abbonati](using/building-journeys/message-to-subscribers-uc.md)
      + Casi d’uso tecnico {#technical-use-cases}
         + [Passaggio dinamico delle raccolte tramite azioni personalizzate](using/building-journeys/collections.md)
         + [Incrementare gradualmente le consegne](using/building-journeys/ramp-up-deliveries-uc.md)
         + [Limite di trasmissione con origini dati esterne e azioni personalizzate](using/building-journeys/limit-throughput.md)
+ Campagne{#campaigns}
   + [Introduzione alle campagne](using/campaigns/get-started-with-campaigns.md)
   + [Creare una campagna](using/campaigns/create-campaign.md)
   + [Rivedere e attivare una campagna](using/campaigns/review-activate-campaign.md)
   + [Gestire le campagne](using/campaigns/modify-stop-campaign.md)
   + Esperimento sui contenuti {#content-experiment}
      + [Introduzione all’esperimento sui contenuti](using/campaigns/get-started-experiment.md)
      + [Creare un esperimento sui contenuti](using/campaigns/content-experiment.md)
      + [Configurare i rapporti sulla sperimentazione](using/campaigns/reporting-configuration.md)
      + Note tecniche {#technotes}
         + [Comprendere i calcoli statistici](using/campaigns/experiment-calculations.md)
         + [Comprendere i calcoli statistici nel rapporto sulla sperimentazione](using/campaigns/experiment-report-calculations.md)
   + [Attivare campagne tramite API](using/campaigns/api-triggered-campaigns.md)
+ Canale e-mail {#email}
   + [Introduzione alle e-mail](using/email/get-started-email.md)
   + [Creare un messaggio e-mail](using/email/create-email.md)
   + Progettare i contenuti delle e-mail {#design-email}
      + [Introduzione alla progettazione delle e-mail](using/email/get-started-email-design.md)
      + Iniziare a creare contenuti {#start-creating-content}
         + [Creare contenuti da zero](using/email/content-from-scratch.md)
         + [Importare i contenuti](using/email/existing-content.md)
         + [Creare il codice del contenuto](using/email/code-content.md)
         + [Utilizzare modelli di e-mail](using/email/use-email-templates.md)
      + Creare contenuti {#add-content}
         + [Utilizzare i componenti per contenuti](using/email/content-components.md)
         + [Sfruttare i frammenti visivi](using/email/use-visual-fragments.md)
         + [Aggiungere collegamenti e tracciare i messaggi](using/email/message-tracking.md)
         + [Inserire offerte personalizzate](using/email/add-offers-email.md)
         + [Generare la versione del testo](using/email/text-version-email.md)
         + [Aggiungere una preintestazione](using/email/preheader.md)
      + Modificare lo stile {#edit-style}
         + [Introduzione allo stile delle e-mail](using/email/get-started-email-style.md)
         + [Modificare le impostazioni dello sfondo](using/email/backgrounds.md)
         + [Regolare l’allineamento verticale e la spaziatura](using/email/alignment-and-padding.md)
         + [Aggiungere attributi di stile in linea](using/email/inline-styling.md)
   + [Utilizzare i modelli di Experience Manager](using/email/aem-templates.md)
   + [Gestire la rinuncia alle e-mail](using/email/email-opt-out.md)
   + Configurare il canale e-mail {#configure-email}
      + [ Introduzione alla configurazione e-mail](using/email/get-started-email-config.md)
      + [Configurare le impostazioni della superficie e-mail](using/email/email-settings.md)
      + [Personalizzare le impostazioni della superficie e-mail](using/email/surface-personalization.md)
+ Canale in-app{#in-app}
   + [Introduzione al canale in-app](using/in-app/get-started-in-app.md)
   + [Prerequisiti per il canale in-app](using/in-app/inapp-configuration.md)
   + [Creare un messaggio in-app per dispositivi mobili](using/in-app/create-in-app.md)
   + [Creare un messaggio in-app per il web](using/in-app/create-in-app-web.md)
   + [Creare contenuto in-app](using/in-app/design-in-app.md)
   + [Verifica e invio della notifica in-app](using/in-app/send-in-app.md)
+ Canale di notifica push{#push}
   + [Introduzione alle notifiche push](using/push/get-started-push.md)
   + [Creare una notifica push](using/push/create-push.md)
   + [Progettare una notifica push](using/push/design-push.md)
   + [Verificare e inviare la notifica push](using/push/send-push.md)
   + Configurare le notifiche push{#push-config}
      + [Flusso di notifica push](using/push/push-gs.md)
      + [Configurare il canale di notifica push](using/push/push-configuration.md)
      + [Flusso di lavoro di avvio rapido per l’onboarding mobile](using/push/mobile-onboarding-wf.md)
+ Canale SMS/MMS{#sms}
   + [Introduzione ai messaggi di testo](using/sms/get-started-sms.md)
   + [Creare un messaggio SMS](using/sms/create-sms.md)
   + [Creare un messaggio MMS](using/sms/create-mms.md)
   + [Verificare e inviare i messaggi di testo](using/sms/send-sms.md)
   + [Gestire la rinuncia ai messaggi di testo](using/sms/sms-opt-out.md)
   + [Configurare il canale SMS](using/sms/sms-configuration.md)
   + [Configurare i sottodomini SMS](using/sms/sms-subdomains.md)
+ Direct mail {#direct-mail}
   + [Introduzione alle direct mail](using/direct-mail/get-started-direct-mail.md)
   + [Creare una direct mail](using/direct-mail/create-direct-mail.md)
   + [Controllare e inviare un messaggio direct mail](using/direct-mail/test-send-direct-mail.md)
   + [Configurare direct mail](using/direct-mail/direct-mail-configuration.md)
+ Canale Web {#web}
   + [Introduzione al canale Web](using/web/get-started-web.md)
   + Configurare il canale Web {#configure-web-channel}
      + [Prerequisiti per il canale Web](using/web/web-prerequisites.md)
      + [Configurare i sottodomini web](using/web/web-delegated-subdomains.md)
   + [Creare esperienze web](using/web/create-web.md)
   + Authoring di pagine web {#author-web-pages}
      + [Modificare il contenuto di una pagina web](using/web/edit-web-content.md)
      + [Gestire le modifiche](using/web/manage-web-modifications.md)
      + [Monitorare le campagne web](using/web/monitor-web-campaigns.md)
      + [Creare applicazioni a pagina singola](using/web/web-spa.md)
+ Esperienza basata su codice {#code-based-experience}
   + [Introduzione al canale basato su codice](using/code-based/get-started-code-based.md)
   + [Guardrail e prerequisiti](using/code-based/code-based-prerequisites.md)
   + [Esempi di metodi di implementazione](using/code-based/code-based-implementation-samples.md)
   + [Creare esperienze basate su codice](using/code-based/create-code-based.md)
+ Pagine di destinazione {#landing-pages}
   + [Introduzione alle pagine di destinazione](using/landing-pages/get-started-lp.md)
   + [Creare una pagina di destinazione](using/landing-pages/create-lp.md)
   + Creare i contenuti {#landing-pages-design}
      + [Informazioni sulla creazione di pagine di destinazione](using/landing-pages/design-lp.md)
      + [Creare il contenuto della pagina di destinazione](using/landing-pages/lp-content.md)
      + [Creare modelli](using/landing-pages/lp-templates.md)
      + [Aggiungere JavaScript personalizzato](using/landing-pages/lp-custom-js.md)
   + [Creare un elenco di iscrizione](using/landing-pages/subscription-list.md)
   + [Esempi di casi d’uso](using/landing-pages/lp-use-cases.md)
   + Configurare le pagine di destinazione {#lp-configuration}
      + [Configurare i sottodomini della pagina di destinazione](using/landing-pages/lp-subdomains.md)
      + [Definire i predefiniti per la pagina di destinazione](using/landing-pages/lp-presets.md)
+ Gestione dei contenuti {#content-management}
   + Utilizzare l’Assistente contenuti{#content-assistant}
      + [Introduzione all’Assistente contenuti](using/content-management/gs-generative.md)
      + [Generazione di contenuti](using/content-management/generative-content.md)
      + [Generazione di immagini](using/content-management/generative-image.md)
   + Utilizzare il contenuto multilingue{#content-multilingual}
      + [Introduzione al contenuto multilingue](using/content-management/multilingual-gs.md)
      + [Creare contenuto multilingue con traduzione manuale](using/content-management/multilingual-manual.md)
      + [Creare contenuto multilingue con traduzione automatica](using/content-management/multilingual-automated.md)
      + [Rapporto campagna multilingue](using/content-management/multilingual-report.md)
   + Risorse/Immagini {#assets-images}
      + [Utilizzare Experience Manager Assets](using/content-management/assets.md)
      + [Utilizzare Adobe Stock](using/content-management/stock.md)
   + Personalizzazione {#personalization}
      + [Introduzione alla personalizzazione](using/personalization/personalize.md)
      + [Contesti di personalizzazione](using/personalization/personalization-contexts.md)
      + [Sintassi di personalizzazione](using/personalization/personalization-syntax.md)
      + Utilizzare l’editor di espressioni {#expression-editor}
         + [Informazioni sull’editor di espressioni](using/personalization/personalization-build-expressions.md)
         + [Aggiungere attributi ai preferiti](using/personalization/personalization-favorites.md)
         + [Utilizzare frammenti di espressione](using/personalization/use-expression-fragments.md)
         + [Convalida della personalizzazione](using/personalization/personalization-validation.md)
      + Funzioni Helper{#functions}
         + [Guida introduttiva alle funzioni Helper](using/personalization/functions/functions.md)
         + [Funzioni di aggregazione](using/personalization/functions/aggregation.md)
         + [Funzioni aritmetiche](using/personalization/functions/arithmetic-functions.md)
         + [Funzioni array ed elenco](using/personalization/functions/arrays-list.md)
         + [Funzioni data](using/personalization/functions/dates.md)
         + [Funzioni booleane e di confronto](using/personalization/functions/operators.md)
         + [Helper](using/personalization/functions/helpers.md)
         + [Funzioni di mappatura](using/personalization/functions/maps.md)
         + [Funzioni matematiche](using/personalization/functions/math.md)
         + [Funzioni oggetto](using/personalization/functions/objects.md)
         + [Funzioni stringa](using/personalization/functions/string.md)
      + Casi d’uso della personalizzazione{#personalization-use-cases}
         + [Notifica dello stato dell’ordine](using/personalization/personalization-use-case.md)
         + [E-mail di abbandono carrello](using/personalization/personalization-use-case-helper-functions.md)
   + Gestire il contenuto riutilizzabile {#reusable-content}
      + [Utilizzare i modelli di contenuto](using/content-management/content-templates.md)
      + [Utilizzare i frammenti](using/content-management/fragments.md)
   + Contenuto dinamico {#dynamic}
      + [Introduzione ai contenuti dinamici](using/personalization/get-started-dynamic-content.md)
      + [Creare regole condizionali](using/personalization/create-conditions.md)
      + [Creare contenuti dinamici](using/personalization/dynamic-content.md)
   + Anteprima e test del contenuto {#preview-test}
      + [Introduzione ad anteprima e test](using/content-management/preview-test.md)
      + [Selezionare i profili di test](using/content-management/test-profiles.md)
      + [Anteprima del contenuto](using/content-management/preview.md)
      + [Inviare bozze e-mail](using/content-management/proofs.md)
      + [Testare il rendering delle e-mail](using/content-management/rendering.md)
      + [Usare il rapporto spam](using/content-management/spam-report.md)
+ Tipi di pubblico, profili e identità{#audiences-profiles-identities}
   + Tipi di pubblico {#audiences}
      + [Introduzione ai tipi di pubblico](using/audience/about-audiences.md)
      + [Generare definizioni di segmento](using/audience/creating-a-segment-definition.md)
      + Comporre i tipi di pubblico {#audience-orchestration}
         + [Introduzione alla composizione dei tipi di pubblico](using/audience/get-started-audience-orchestration.md)
         + [Creare flussi di lavoro di composizione](using/audience/create-compositions.md)
         + [Lavorare nell’area di lavoro per la composizione](using/audience/composition-canvas.md)
         + [Accesso e gestione dei tipi di pubblico](using/audience/access-audiences.md)
   + Profili{#profiles}
      + [Introduzione ai profili](using/audience/get-started-profiles.md)
      + [Creare profili di test](using/audience/creating-test-profiles.md)
      + [Utilizzo di attributi con più valori](using/audience/computed-attributes.md)
   + [Identità](using/audience/get-started-identity.md)
   + [Utilizzo delle licenze](using/audience/license-usage.md)
+ Tracciare e monitorare {#reporting}
   + Rapporti live {#live-report}
      + [Introduzione ai rapporti live](using/reports/live-report.md)
      + [Elenco dei componenti](using/reports/live-report-components.md)
      + [Rapporto live dei percorsi](using/reports/journey-live-report.md)
      + [Rapporto live della campagna](using/reports/campaign-live-report.md)
      + [Rapporto live delle pagine di destinazione](using/reports/lp-report-live.md)
      + [Rapporto live dell’elenco iscrizioni](using/reports/subscription-report-live.md)
   + Rapporto globale {#global-report}
      + [Introduzione ai rapporti globali](using/reports/global-report.md)
      + [Elenco dei componenti](using/reports/global-report-components.md)
      + [Rapporto globale dei percorsi](using/reports/journey-global-report.md)
      + [Rapporto globale della campagna](using/reports/campaign-global-report.md)
      + [Rapporto delle finalità](using/reports/objective-report.md)
      + [Rapporto globale delle pagine di destinazione](using/reports/lp-report-global.md)
      + [Rapporto globale dell’elenco iscrizioni](using/reports/subscription-report-global.md)
   + Rapporti sul canale {#channel-report}
      + [Introduzione ai rapporti sul canale](using/reports/channel-report-gs.md)
      + [Rapporti sul canale](using/reports/channel-report.md)
   + Rapporti sul percorso {#reports}
      + [Creare rapporti sul percorso](using/reports/sharing-overview.md)
      + [Elenco dei campi evento del passaggio](using/reports/sharing-field-list.md)
      + Campi di eventi passaggio legacy{#legacy-step-event-fields}
         + [Informazioni sui campi legacy](using/reports/sharing-legacy-fields.md)
         + [Campi del percorso](using/reports/sharing-journey-fields.md)
         + [Campi comuni](using/reports/sharing-common-fields.md)
         + [Campi di esecuzione azione](using/reports/sharing-execution-fields.md)
         + [Campi di recupero dati](using/reports/sharing-fetch-fields.md)
         + [Campi di identità](using/reports/sharing-identity-fields.md)
      + [Esempi di query](using/reports/query-examples.md)
   + Recapitabilità {#deliverability}
      + [Introduzione alla recapitabilità](using/reports/deliverability.md)
      + [Informazioni sull’elenco di soppressione](using/reports/suppression-list.md)
      + [Nuovo requisito DMARC](using/configuration/dmarc-record-update.md)
   + [Avvisi](using/reports/alerts.md)
   + [Utilizzare Customer Journey Analytics](using/reports/cja-ajo.md)
   + [Motivi di esclusione](using/reports/exclusion-list.md)
+ Gestione delle decisioni {#offer-decisioning}
   + Introduzione alla gestione delle decisioni {#get-started-decision}
      + [Informazioni sulla gestione delle decisioni](using/offers/get-started/starting-offer-decisioning.md)
      + [Interfaccia utente](using/offers/get-started/user-interface.md)
      + [Passaggi chiave per creare e gestire le offerte](using/offers/offer-library/key-steps.md)
      + [Caso di utilizzo: inserire offerte in un messaggio e-mail](using/offers/offers-e2e.md)
   + Creare componenti {#create-components}
      + [Creare posizionamenti](using/offers/offer-library/creating-placements.md)
      + [Creare regole di decisione](using/offers/offer-library/creating-decision-rules.md)
      + [Creare qualificatori di raccolta](using/offers/offer-library/creating-tags.md)
   + Creare classificazioni {#rankings}
      + [Introduzione alle classificazioni](using/offers/ranking/get-started-rankings.md)
      + [Formule di classificazione](using/offers/ranking/create-ranking-formulas.md)
      + Modelli IA {#ai-models}
         + [Informazioni sui modelli AI](using/offers/ranking/ai-models.md)
         + Tipi di modelli IA {#ai-model-types}
            + [Modello di ottimizzazione automatica](using/offers/ranking/auto-optimization-model.md)
            + [Modello di ottimizzazione personalizzata](using/offers/ranking/personalized-optimization-model.md)
         + [Creare modelli AI](using/offers/ranking/create-ranking-strategies.md)
   + Creare e gestire le offerte {#managing-offers-in-the-offer-library}
      + Configurare le offerte {#configure-offers}
         + [Creare le offerte personalizzate](using/offers/offer-library/creating-personalized-offers.md)
         + [Aggiungere rappresentazioni](using/offers/offer-library/add-representations.md)
         + [Aggiungere vincoli](using/offers/offer-library/add-constraints.md)
      + [Creare offerte di fallback](using/offers/offer-library/creating-fallback-offers.md)
      + [Creare raccolte](using/offers/offer-library/creating-collections.md)
   + Creare e gestire decisioni {#create-manage-activities}
      + [Creare decisioni](using/offers/offer-activities/create-offer-activities.md)
      + [Configurare la selezione di offerte nelle decisioni](using/offers/offer-activities/configure-offer-selection.md)
      + [Creare simulazioni](using/offers/offer-activities/simulation.md)
   + [Utilizzare Batch Decisioning](using/offers/batch-delivery.md)
   + Raccogliere dati evento {#collect-event-data}
      + [Guida introduttiva alla raccolta dati](using/offers/data-collection/data-collection.md)
      + [Creare un set di dati per raccogliere gli eventi](using/offers/data-collection/create-dataset.md)
      + [Configurare l’acquisizione di eventi](using/offers/data-collection/schema-requirement.md)
   + Creare rapporti di gestione delle decisioni {#create-reports}
      + [Utilizzare gli eventi di gestione delle decisioni](using/offers/reports/get-started-events.md)
      + [Accedere ai campi XDM degli eventi](using/offers/reports/xdm-fields.md)
   + Esportare il catalogo delle offerte {#export-catalog}
      + [Introduzione all’esportazione del catalogo delle offerte](using/offers/export-catalog/get-started-export.md)
      + [Accedere al catalogo delle offerte esportato](using/offers/export-catalog/access-dataset.md)
      + [Set di dati di offerte personalizzate](using/offers/export-catalog/export-offers.md)
      + [Set di dati sulle decisioni](using/offers/export-catalog/export-decisions.md)
      + [Set di dati sui posizionamenti](using/offers/export-catalog/export-placements.md)
      + [Set di dati sui fallback](using/offers/export-catalog/export-fallback.md)
   + Documentazione di riferimento API {#api-reference}
      + [Introduzione](using/offers/api-reference/getting-started.md)
      + Creare e gestire offerte tramite API {#offers-api}
         + Posizionamenti {#placements}
            + [Elencare posizionamenti](using/offers/api-reference/offers-api/placements/placements-list.md)
            + [Ricercare un posizionamento](using/offers/api-reference/offers-api/placements/lookup.md)
            + [Creare un posizionamento](using/offers/api-reference/offers-api/placements/create.md)
            + [Aggiornare un posizionamento](using/offers/api-reference/offers-api/placements/update.md)
            + [Eliminare un posizionamento](using/offers/api-reference/offers-api/placements/delete.md)
         + Regole di decisione {#decision-rules}
            + [Elencare regole di decisione](using/offers/api-reference/offers-api/decision-rules/rules-list.md)
            + [Ricercare una regola di decisione](using/offers/api-reference/offers-api/decision-rules/lookup.md)
            + [Creare una regola di decisione](using/offers/api-reference/offers-api/decision-rules/create.md)
            + [Aggiornare una regola di decisione](using/offers/api-reference/offers-api/decision-rules/update.md)
            + [Eliminare una regola di decisione](using/offers/api-reference/offers-api/decision-rules/delete.md)
         + Qualificatori di raccolta {#tags}
            + [Elenco dei qualificatori di raccolta](using/offers/api-reference/offers-api/tags/tags-list.md)
            + [Cercare un qualificatore di raccolta](using/offers/api-reference/offers-api/tags/lookup.md)
            + [Creare un qualificatore di raccolta](using/offers/api-reference/offers-api/tags/create.md)
            + [Aggiornare un qualificatore di raccolta](using/offers/api-reference/offers-api/tags/update.md)
            + [Eliminare un qualificatore di raccolta](using/offers/api-reference/offers-api/tags/delete.md)
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
         + Decisioni {#decisions-api}
            + [Elencare le decisioni](using/offers/api-reference/activities-api/activities/activities-list.md)
            + [Ricercare una decisione](using/offers/api-reference/activities-api/activities/lookup.md)
            + [Creare una decisione](using/offers/api-reference/activities-api/activities/create.md)
            + [Aggiornare una decisione](using/offers/api-reference/activities-api/activities/update.md)
            + [Eliminare una decisione](using/offers/api-reference/activities-api/activities/delete.md)
         + API Legacy {#legacy-api}
            + [Informazioni sulle API Legacy](using/offers/api-reference/offers-api/legacy-apis/about-legacy-apis.md)
            + Posizionamenti {#placements}
               + [Elencare posizionamenti](using/offers/api-reference/offers-api/legacy-apis/placements/placements-list.md)
               + [Ricercare un posizionamento](using/offers/api-reference/offers-api/legacy-apis/placements/lookup.md)
               + [Creare un posizionamento](using/offers/api-reference/offers-api/legacy-apis/placements/create.md)
               + [Aggiornare un posizionamento](using/offers/api-reference/offers-api/legacy-apis/placements/update.md)
               + [Eliminare un posizionamento](using/offers/api-reference/offers-api/legacy-apis/placements/delete.md)
            + Regole di decisione {#decision-rules}
               + [Elencare regole di decisione](using/offers/api-reference/offers-api/legacy-apis/decision-rules/rules-list.md)
               + [Ricercare una regola di decisione](using/offers/api-reference/offers-api/legacy-apis/decision-rules/lookup.md)
               + [Creare una regola di decisione](using/offers/api-reference/offers-api/legacy-apis/decision-rules/create.md)
               + [Aggiornare una regola di decisione](using/offers/api-reference/offers-api/legacy-apis/decision-rules/update.md)
               + [Eliminare una regola di decisione](using/offers/api-reference/offers-api/legacy-apis/decision-rules/delete.md)
            + Qualificatori di raccolta {#tags}
               + [Elenco dei qualificatori di raccolta](using/offers/api-reference/offers-api/legacy-apis/tags/tags-list.md)
               + [Cercare un qualificatore di raccolta](using/offers/api-reference/offers-api/legacy-apis/tags/lookup.md)
               + [Creare un qualificatore di raccolta](using/offers/api-reference/offers-api/legacy-apis/tags/create.md)
               + [Aggiornare un qualificatore di raccolta](using/offers/api-reference/offers-api/legacy-apis/tags/update.md)
               + [Eliminare un qualificatore di raccolta](using/offers/api-reference/offers-api/legacy-apis/tags/delete.md)
            + Offerte personalizzate {#personalized-offers}
               + [Elencare offerte personalizzate](using/offers/api-reference/offers-api/legacy-apis/personalized-offers/offers-list.md)
               + [Ricercare un’offerta personalizzata](using/offers/api-reference/offers-api/legacy-apis/personalized-offers/lookup.md)
               + [Creare un’offerta personalizzata](using/offers/api-reference/offers-api/legacy-apis/personalized-offers/create.md)
               + [Aggiornare un’offerta personalizzata](using/offers/api-reference/offers-api/legacy-apis/personalized-offers/update.md)
               + [Eliminare un’offerta personalizzata](using/offers/api-reference/offers-api/legacy-apis/personalized-offers/delete.md)
            + Offerte di fallback {#fallback-offers}
               + [Elencare offerte di fallback](using/offers/api-reference/offers-api/legacy-apis/fallback-offers/fallback-list.md)
               + [Ricercare un’offerta di fallback](using/offers/api-reference/offers-api/legacy-apis/fallback-offers/lookup.md)
               + [Creare un’offerta di fallback](using/offers/api-reference/offers-api/legacy-apis/fallback-offers/create.md)
               + [Aggiornare un’offerta di fallback](using/offers/api-reference/offers-api/legacy-apis/fallback-offers/update.md)
               + [Eliminare un’offerta di fallback](using/offers/api-reference/offers-api/legacy-apis/fallback-offers/delete.md)
            + Raccolte {#collections}
               + [Elencare raccolte](using/offers/api-reference/offers-api/legacy-apis/collections/collections-list.md)
               + [Ricercare una raccolta](using/offers/api-reference/offers-api/legacy-apis/collections/lookup.md)
               + [Creare una raccolta](using/offers/api-reference/offers-api/legacy-apis/collections/create.md)
               + [Aggiornare una raccolta](using/offers/api-reference/offers-api/legacy-apis/collections/update.md)
               + [Eliminare una raccolta](using/offers/api-reference/offers-api/legacy-apis/collections/delete.md)
            + Decisioni {#decisions-api}
               + [Elencare le decisioni](using/offers/api-reference/offers-api/legacy-apis/activities-api/activities-list.md)
               + [Ricercare una decisione](using/offers/api-reference/offers-api/legacy-apis/activities-api/lookup.md)
               + [Creare una decisione](using/offers/api-reference/offers-api/legacy-apis/activities-api/create.md)
               + [Aggiornare una decisione](using/offers/api-reference/offers-api/legacy-apis/activities-api/update.md)
               + [Eliminare una decisione](using/offers/api-reference/offers-api/legacy-apis/activities-api/delete.md)
      + Consegnare offerte tramite API {#offer-delivery-api}
         + [Introduzione alla recapitabilità delle offerte tramite API](using/offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)
         + [API Decisioning](using/offers/api-reference/offer-delivery-api/decisioning-api.md)
         + [API Edge Decisioning](using/offers/api-reference/offer-delivery-api/edge-decisioning-api.md)
         + [API Batch Decisioning](using/offers/api-reference/offer-delivery-api/batch-decisioning-api.md)
+ Offer Decisioning {#experience-decisioning}
   + [Introduzione a Offer Decisioning](using/experience-decisioning/gs-experience-decisioning.md)
   + Gestire gli elementi decisionali {#decision-items}
      + [Configurare il catalogo degli elementi](using/experience-decisioning/catalogs.md)
      + [Creare elementi decisionali](using/experience-decisioning/items.md)
      + [Gestire le raccolte di elementi](using/experience-decisioning/collections.md)
   + Configurare la selezione degli elementi {#selection}
      + [Creare regole di decisione](using/experience-decisioning/rules.md)
      + [Creare metodi di classificazione](using/experience-decisioning/ranking.md)
   + [Creare strategie di selezione](using/experience-decisioning/selection-strategies.md)
   + [Creare criteri di decisione](using/experience-decisioning/create-decision.md)
+ Gestione dei dati {#data-management}
   + [Introduzione alla gestione dei dati](using/data/gs-data.md)
   + [Utilizzare gli schemi](using/data/get-started-schemas.md)
   + Set di dati di Journey Optimizer {#datasets}
      + [Introduzione ai set di dati](using/data/get-started-datasets.md)
      + [Esporta i set di dati di Journey Optimizer](using/data/export-datasets.md)
      + [Esempi di query](using/data/datasets-query-examples.md)
      + [Schemi incorporati > ](https://experienceleague.adobe.com/tools/ajo-schemas/schema-dictionary.html?lang=it)
   + [Query](using/data/get-started-queries.md)
+ Configurazione {#configuration}
   + [Introduzione alla configurazione di Journey Optimizer](using/configuration/get-started-configuration.md)
   + [Impostare le superfici di canale](using/configuration/channel-surfaces.md)
   + Delegare i sottodomini e-mail {#delegate-subdomains}
      + [Introduzione alla delega dei sottodomini](using/configuration/about-subdomain-delegation.md)
      + [Delegare un sottodominio](using/configuration/delegate-subdomain.md)
      + [Impostare il record DMARC](using/configuration/dmarc-record.md)
      + [Aggiungere un record TXT di Google](using/configuration/google-txt.md)
      + [Accedere e modificare i record PTR](using/configuration/ptr-records.md)
      + [Creare pool IP](using/configuration/ip-pools.md)
   + Implementare un piano di preparazione IP {#implement-ip-warmup-plan}
      + [Introduzione ai piani di preparazione IP](using/configuration/ip-warmup-gs.md)
      + [Creare campagne di preparazione IP](using/configuration/ip-warmup-campaign.md)
      + [Creare un piano di preparazione IP](using/configuration/ip-warmup-plan.md)
      + [Eseguire il piano di preparazione IP](using/configuration/ip-warmup-execution.md)
      + [File del piano di preparazione IP](using/configuration/ip-warmup-plan-files.md)
   + Monitorare gli indirizzi e-mail {#monitor-reputation}
      + [Elenco di soppressione](using/configuration/manage-suppression-list.md)
      + [Nuovi tentativi](using/configuration/retries.md)
      + [Elenco Consentiti](using/configuration/allow-list.md)
   + [Utilizzare gli elenchi seed](using/configuration/seed-lists.md)
   + [Supporto per l’archiviazione](using/configuration/archiving-support.md)
   + [Modificare gli indirizzi di esecuzione](using/configuration/primary-email-addresses.md)
   + [Configurare le regole di frequenza](using/configuration/frequency-rules.md)
   + Configurare percorsi {#configure-journeys}
      + [Informazioni su origini dati, eventi e azioni](using/configuration/about-data-sources-events-actions.md)
      + Integrazione con sistemi esterni {#external-systems}
         + [Integrazione dei percorsi con sistemi esterni](using/configuration/external-systems.md)
         + [API di limitazione di utilizzo](using/configuration/capping.md)
         + [API di limitazione](using/configuration/throttling.md)
      + Configurazione evento {#events-journeys}
         + [Utilizzare gli eventi del percorso](using/event/about-events.md)
         + Configurare un evento unitario {#unitary-events}
            + [Introduzione agli eventi unitari](using/event/about-creating.md)
            + [Informazioni sugli schemi ExperienceEvent](using/event/experience-event-schema.md)
            + [Utilizzare Adobe Analytics](using/event/about-analytics.md)
         + [Configurare un evento di business](using/event/about-creating-business.md)
         + [Passaggi aggiuntivi per l’invio di eventi](using/event/additional-steps-to-send-events-to-journey.md)
      + Configurazione origine dati{#data-source-journeys}
         + [Informazioni sulle origini dati](using/datasource/about-data-sources.md)
         + [Configurare un’origine dati](using/datasource/configure-data-sources.md)
         + [Origine dati Adobe Experience Platform](using/datasource/adobe-experience-platform-data-source.md)
         + [Origini dati esterne](using/datasource/external-data-sources.md)
      + Configurazione delle azioni {#action-journeys}
         + [Informazioni sulle azioni](using/action/action.md)
         + [Configurare un’azione](using/action/about-custom-action-configuration.md)
         + [Integrare con Adobe Campaign Standard](using/action/acs-action.md)
         + [Integrare con Adobe Campaign v7/v8](using/action/acc-action.md)
         + [Utilizzare le risposte alle chiamate API nelle azioni personalizzate](using/action/action-response.md)
   + [Origini](using/start/get-started-sources.md)
+ Controllo degli accessi {#access-control}
   + Panoramica sul controllo degli accessi {#privacy}
      + [Introduzione alla gestione degli utenti](using/administration/permissions-overview.md)
      + [Ruoli incorporati](using/administration/ootb-product-profiles.md)
      + [Autorizzazioni incorporate](using/administration/ootb-permissions.md)
      + [Livelli di autorizzazione](using/administration/high-low-permissions.md)
   + [Gestire utenti e ruoli](using/administration/permissions.md)
   + [Controllo degli accessi basato su attributi](using/administration/attribute-based-access.md)
   + [Controllo dell’accesso a livello di oggetto](using/administration/object-based-access.md)
   + [Gestione delle sandbox](using/administration/sandboxes.md)
+ Privacy {#privacy}
   + [Introduzione alla privacy](using/privacy/get-started-privacy.md)
   + [Richieste di accesso a dati personali](using/privacy/requests.md)
   + [Azioni di audit sulle risorse](using/privacy/audit-logs.md)
   + [Eseguire operazioni di igiene dei dati](using/privacy/data-hygiene.md)
   + Gestire il consenso {#consent}
      + [Gestire la rinuncia](using/privacy/opt-out.md)
      + [Utilizzare i criteri di consenso](using/action/consent.md)
   + [Governance dei dati](using/action/action-privacy.md)
   + [Configurazione e gestione delle chiavi gestite dal cliente](using/privacy/cmk.md)
