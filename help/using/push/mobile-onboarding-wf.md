---
solution: Journey Optimizer
product: journey optimizer
title: Flusso di lavoro di avvio rapido per l’onboarding mobile
description: Scopri come utilizzare il flusso di lavoro di onboarding rapido per dispositivi mobili
topic: Mobile
feature: Push
role: Admin
level: Intermediate
badge: label="Beta" type="Informative"
exl-id: 364ef926-3f92-4297-acbd-a283668106ac
source-git-commit: c4ab97999d000d969f6f09f4d84be017d1288f94
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 9%

---

# Flusso di lavoro di avvio rapido per l’onboarding mobile {#mobile-wf}

Il nuovo **flusso di lavoro di avvio rapido per l’onboarding per dispositivi mobili** è una nuova funzione del prodotto che consente di configurare rapidamente l’SDK di Adobe Experience Platform Mobile, iniziare a raccogliere e convalidare i dati degli eventi mobili e inviare notifiche push con [!DNL Journey Optimizer].

Questa funzionalità è accessibile tramite **[!DNL Adobe Experience Platform Data Collection]** home page per tutti i clienti come versione beta pubblica.

## Introduzione{#gs-mobile-wf}

Questo nuovo flusso di lavoro automatizza la configurazione della raccolta dati riducendo il numero totale di clic e accelerando la configurazione mobile per Journey Optimizer. Questo flusso di lavoro rapido illustra quattro semplici passaggi per: [configurazione](##setup-mobile-wf), [implementare](#implement-mobile-wf), [convalida](#valid-mobile-wf), e [recensione](#review-mobile-wf) la tua configurazione mobile.

Per accedere al nuovo flusso di lavoro con avvio rapido per l’onboarding di Mobile, passa a **[!DNL Data Collection]** dallo switcher della soluzione. Quindi seleziona la **[!DNL Start Collecting Mobile Data]** nella home page.

![](assets/mobile-wf-home.png)

Di seguito sono riportate alcune funzioni aggiuntive:

* Semplice workflow in quattro fasi e interfaccia utente.
* Offre una configurazione di base per iniziare a raccogliere i dati degli eventi mobili tramite [SDK di Adobe Experience Platform Mobile](https://developer.adobe.com/client-sdks/documentation/){target="_blank"} in minuti.
* Possibilità di testare e convalidare un evento push mobile di base sfruttando [Adobe Experience Platform Assurance](https://experienceleague.adobe.com/docs/experience-platform/assurance/home.html){target="_blank"}.
* Crea e configura automaticamente tutte le risorse di Data Collection e Journey Optimizer necessarie.
* Nelle guide del prodotto e nelle descrizioni.
* Fornisce una transizione naturale per un&#39;implementazione più avanzata, se necessario.

## Configurazione {#setup-mobile-wf}

Il primo passaggio di questo flusso di lavoro crea e configura automaticamente tutte le risorse necessarie di Raccolta dati e Journey Optimizer, come Proprietà mobili, Estensioni mobili, Estensione Journey Optimizer, Regole, Elementi dati, ecc.

Dopo aver accettato i termini e le condizioni beta, inserisci il nome dell’app mobile e fai clic su **[!DNL Next]**.

![](assets/mobile-wf-setup.png)

Fornisci informazioni per le piattaforme iOS e Android, compreso l&#39;App ID e le chiavi di autenticazione o il file di chiave.

## Implementazione{#implement-mobile-wf}

Il passaggio successivo fornisce indicazioni dettagliate per installare il codice nell’app mobile.

![](assets/mobile-wf-add-code.png)


## Convalida{#valid-mobile-wf}

Esamina e controlla l’implementazione per convalidarla. Puoi inviare una notifica push di prova.

![](assets/mobile-wf-valid.png)


## Revisione {#review-mobile-wf}

La configurazione automatica è completata. Ora puoi visitare la proprietà mobile dei tag, configurare le regole o l’elemento dati e iniziare a inviare notifiche push con Adobe Journey Optimizer.

![](assets/mobile-wf-done.png)


**Argomenti correlati**

* [Introduzione alle notifiche push](get-started-push.md)
* [Flusso di dati e componenti delle notifiche push](push-gs.md)
* [Configurare il canale push](push-configuration.md)
* [Rapporto notifiche push](../reports/journey-global-report.md#push-global)
* [Creare una notifica push](create-push.md)
