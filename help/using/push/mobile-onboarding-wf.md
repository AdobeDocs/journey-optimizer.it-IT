---
solution: Journey Optimizer
product: journey optimizer
title: Flusso di lavoro di avvio rapido per l’onboarding mobile
description: Scopri come utilizzare il flusso di lavoro di avvio rapido per l’onboarding mobile
topic: Mobile
feature: Push
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta" type="Informativo"
source-git-commit: 145d2a60bc5dbd6e2a92f13afbf2db662f465e36
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 5%

---


# Flusso di lavoro di avvio rapido per l’onboarding mobile {#mobile-wf}

Il nuovo **flusso di lavoro di avvio rapido onboarding mobile** è una nuova funzionalità del prodotto per configurare rapidamente l’SDK di Mobile, iniziare a raccogliere e convalidare i dati degli eventi mobili e inviare notifiche push con [!DNL Journey Optimizer].

Questa funzionalità è accessibile tramite **[!DNL Adobe Experience Platform Data Collection]** home page per tutti i clienti come versione beta pubblica.

## Introduzione{#gs-mobile-wf}

Questo nuovo flusso di lavoro automatizza la configurazione della raccolta dati riducendo i clic totali e accelerando la configurazione mobile per Journey Optimizer. Questo flusso di lavoro di avvio rapido descrive quattro semplici passaggi per [configurare](##setup-mobile-wf), [implementare](#implement-mobile-wf), [validate](#valid-mobile-wf)e [revisione](#review-mobile-wf) la configurazione mobile.

Per accedere al nuovo flusso di lavoro di avvio rapido dell’onboarding mobile, sfoglia fino a **[!DNL Data Collection]** dal commutatore della soluzione. Quindi seleziona la **[!DNL Start Collecting Mobile Data]** nella home page.

![](assets/mobile-wf-home.png)

Di seguito sono riportate alcune funzioni aggiuntive:

* Workflow a quattro passaggi e interfaccia utente semplici.
* Fornisce una configurazione di base per iniziare a raccogliere in pochi minuti i dati dell’evento mobile tramite l’SDK di Mobile.
* Possibilità di testare e convalidare un evento push mobile di base utilizzando Assurance.
* Crea e configura automaticamente tutti i dati Collection necessari e le risorse Journey Optimizer.
* Nella guida del prodotto e nelle descrizioni dei comandi.
* Fornisce una transizione naturale per un’implementazione più avanzata, se necessario.

## Configurazione {#setup-mobile-wf}

Il primo passaggio di questo flusso di lavoro crea e configura automaticamente tutte le necessarie raccolte di dati e risorse Journey Optimizer, come proprietà mobili, estensioni mobili, estensione Journey Optimizer, regole, elementi dati, ecc.

Dopo aver accettato i Termini e Condizioni Beta, immetti il nome della tua app mobile e fai clic su **[!DNL Next]**.

![](assets/mobile-wf-setup.png)

Fornisci informazioni per le piattaforme iOS e Android, incluse le chiavi di autenticazione e l&#39;ID app o il file chiave.

## Implementazione{#implement-mobile-wf}

Il passaggio successivo fornisce istruzioni dettagliate per installare il codice nell’app mobile.

![](assets/mobile-wf-add-code.png)


## Convalida{#valid-mobile-wf}

Rivedi e controlla l’implementazione per convalidarla. Puoi inviare una notifica push di prova.

![](assets/mobile-wf-valid.png)


## Revisione {#review-mobile-wf}

La configurazione automatizzata viene eseguita. Ora puoi visitare la proprietà tag mobile e configurare le regole o gli elementi dati e iniziare a inviare notifiche push con Adobe Journey Optimizer.

![](assets/mobile-wf-done.png)


**Argomenti correlati**

* [Introduzione alle notifiche push](get-started-push.md)
* [Flusso di dati e componenti della notifica push](push-gs.md)
* [Configurare il canale push](push-configuration.md)
* [Rapporto notifiche push](../reports/journey-global-report.md#push-global)
* [Creare una notifica push](create-push.md)
