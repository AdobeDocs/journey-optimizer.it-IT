---
title: Introduzione alla messaggistica in-app
description: Scopri come inviare notifiche in-app con Journey Optimizer
feature: In App
topic: Content Management
role: User
level: Beginner
keywords: in-app, messaggio, creazione, inizio
exl-id: 51562843-7b50-4eb5-bf79-5ce03f7549cb
TQID: https://experienceleague.adobe.com/b139LQsPe3HwKe1O5cyBx4Nj4jpW3GXCFIVIWTAIlbg
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2: id: b3a93754-a8b8-46eb-9421-7eccaeeb3dffid: cc5c44e2-54a1-4927-b794-442cd87d8f74id: c96d2aa5-76a2-443d-8d23-5de95577c909id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 75ebd043971ce40e2da0f627622441a46a8e667c
workflow-type: ht
source-wordcount: 601
ht-degree: 100%

---

# Introduzione al canale in-app {#gs-in-app}

>[!BEGINSHADEBOX]

**In questa pagina:** introduzione al canale di messaggistica in-app in Adobe Journey Optimizer per coinvolgere gli utenti dell’app con notifiche che promuovono funzioni, offerte e onboarding.

>[!ENDSHADEBOX]

I messaggi in-app sono notifiche che possono essere inviate agli utenti all’interno dell’app per indirizzarli a specifici punti di interesse. Queste notifiche possono essere utilizzate per scopi diversi, ad esempio per promuovere nuove funzioni, presentare offerte speciali o facilitare l’onboarding degli utenti. Sfruttando i messaggi in-app, puoi interagire efficacemente con il pubblico e indirizzarlo verso aspetti importanti della tua applicazione.

Utilizza Journey Optimizer per creare notifiche in-app e configurare le opzioni relative all’esperienza, tra cui il layout e la visualizzazione dei messaggi, il testo e le opzioni dei pulsanti di scelta.

</br>

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="inapp-configuration.md">
<img alt="Convalida" src="../assets/do-not-localize/inapp-config.jpg">
</a>
<div>
<a href="inapp-configuration.md"><strong>Configurare il canale in-app</strong></a>
</div>
<p>
</td>
<td>
<a href="create-in-app.md">
<img alt="Lead" src="../assets/do-not-localize/inapp-create.jpeg">
</a>
<div><a href="create-in-app.md"><strong>Creare un messaggio in-app</strong>
</div>
<p>
</td>
<td>
<a href="design-in-app.md">
<img alt="Non frequente" src="../assets/do-not-localize/inapp-design.jpg">
</a>
<div>
<a href="design-in-app.md"><strong>Creare contenuto in-app</strong></a>
</div>
<p></td>
<td>
<a href="../reports/campaign-global-report-cja-inapp.md">
<img alt="Convalida" src="../assets/do-not-localize/inapp-report.jpg">
</a>
<div>
<a href="../reports/campaign-global-report-cja-inapp.md"><strong>Accedere ai rapporti in-app</strong></a>
</div>
<p>
</td>
</tr></table>

## Casi d’uso

I messaggi in-app funzionano al meglio quando desideri guidare o influenzare gli utenti mentre sono già coinvolti nella tua app, sfruttando quel momento di attenzione attiva.

| Beneficio | Il motivo | Casi d’uso di esempio |
| --- | --- | --- |
| Coinvolgimento dell’utente elevato | Puoi raggiungere gli utenti quando stanno attivamente utilizzando l’app | Annunci relativi alle funzioni, suggerimenti per l’onboarding |
| Trigger contestualmente rilevanti | Possono essere attivati in base al comportamento o alla posizione in-app | Messa in evidenza di una funzione subito dopo che un utente visita una schermata correlata |
| Consegna in tempo reale | Nessuna dipendenza da token push o servizi di consegna esterni | Prompt urgenti visualizzati durante la sessione corrente |
| Nessuna dipendenza da canali esterni | Funzionamento completo all’interno dell’app, indipendentemente dallo stato di consenso per altri canali | Raggiungimento degli utenti che hanno rinunciato alle notifiche push |
| Miglior potenziale di conversione | Presentati in un momento di attenzione attiva, aumentano i tassi di risposta | Offerte di vendita in upselling o cross-selling, prompt di sondaggi |
| Personalizzazione e segmentazione | Layout, testo e pulsanti possono essere personalizzati per tipi di pubblico specifici | Flussi di onboarding personalizzati per diversi segmenti di utenti |
| Design non invasivo | Possono essere progettati per integrare l’esperienza utente anziché interromperla | Banner o finestre modali in linea con l’interfaccia utente dell’app |

## Quando non utilizzare

I messaggi in-app dipendono da una sessione attiva, pertanto non sono adatti a ogni scenario. Considera un altro canale nelle seguenti situazioni:

* L’utente non sta utilizzando attivamente l’app, poiché il messaggio non verrà mai visualizzato
* Il messaggio riguarda un problema critico o urgente che richiede di raggiungere gli utenti esterni all’app, ad esempio un avviso di interruzione o di sicurezza
* La comunicazione è di tipo legale o normativo e richiede una conferma di lettura che i messaggi in-app non possono fornire
* L’obiettivo è la riattivazione dell’account o una campagna di recupero per gli utenti inattivi che hanno poche probabilità di aprire l’app
* Il messaggio è un aggiornamento transazionale dal volume elevato, ad esempio una conferma d’ordine, che si presta meglio all’invio tramite e-mail o SMS
* Un uso eccessivo potrebbe portare alla “cecità da banner”, ovvero alla tendenza degli utenti a ignorare i messaggi che compaiono troppo spesso
* Al momento della consegna del messaggio, gli utenti potrebbero essere offline o non disporre di una connessione all’app



## Risorse aggiuntive

* **[Creare messaggi in-app](create-in-app.md)**: scopri come creare e configurare messaggi in-app per le applicazioni per dispositivi mobili.
* **[Configurare il canale in-app](inapp-configuration.md)**: imposta il canale di messaggistica in-app con le configurazioni appropriate per le applicazioni per dispositivi mobili.
* **[Progettare contenuti in-app](design-in-app.md)**: personalizza layout, stili, pulsanti ed elementi interattivi dei messaggi in-app.
* **[In-app per il web](create-in-app-web.md)**: scopri come creare e consegnare messaggi in-app per le applicazioni web.
* **[Tutorial sul canale in-app](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/channels/in-app-channel/in-app-messages-overview){target="_blank"}**: esplora i tutorial video dettagliati sulle funzioni e sulle best practice della messaggistica in-app.

