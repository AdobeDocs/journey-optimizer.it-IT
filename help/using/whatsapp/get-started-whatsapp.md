---
solution: Journey Optimizer
product: journey optimizer
title: Introduzione ai messaggi WhatsApp
description: Scopri come creare e inviare messaggi WhatsApp in Journey Optimizer
feature: Whatsapp
topic: Content Management
role: User
level: Beginner
exl-id: 22df2bfa-4d86-464e-ad83-3aa457e3a747
TQID: https://experienceleague.adobe.com/uHzRC9X6rB9EXH4gIFiRxFaeNcrTD0-40RrxZkN4XFg
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2: id: b8df23d2-98a2-4406-86cc-2babe8728d36id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: 75ebd043971ce40e2da0f627622441a46a8e667c
workflow-type: tm+mt
source-wordcount: 686
ht-degree: 64%

---

# Introduzione ai messaggi WhatsApp {#get-started-whatsapp}

>[!BEGINSHADEBOX]

**In questa pagina:** scopri come funziona il canale WhatsApp in Journey Optimizer, insieme ai relativi prerequisiti e limitazioni, in modo da poter decidere come aggiungere WhatsApp ai percorsi e alle campagne.

>[!ENDSHADEBOX]

Ora puoi inviare messaggi WhatsApp direttamente tramite Journey Optimizer utilizzando l’[API cloud](https://developers.facebook.com/docs/whatsapp/cloud-api/) di Meta. Questa funzione consente l’integrazione diretta di WhatsApp in percorsi e campagne, migliorando la comunicazione e il coinvolgimento con i destinatari.

* In un **percorso**. Crea un percorso, aggiungi un’attività **WhatsApp** e definisci le impostazioni di base, quindi passa al riquadro a destra **[!UICONTROL Azioni: WhatsApp]** per creare il contenuto per il messaggio WhatsApp. Ulteriori informazioni su come creare un percorso sono disponibili in [questa pagina](../building-journeys/journey-gs.md).

* In una **campagna**. Crea una campagna, seleziona **WhatsApp** come azione e definisci le impostazioni di base, quindi modifica il contenuto del messaggio per definire il messaggio WhatsApp da inviare. Scopri come creare [una campagna di azione](../campaigns/campaign-action.md#action-campaign-action) | [una campagna attivata da API](../campaigns/api-triggered-campaigns.md) | [una campagna orchestrata](../orchestrated/create-orchestrated-campaign.md#create)

![](assets/do-not-localize/whatsapp-beta.png){zoomable="yes"}

## Casi d’uso {#use-cases}

WhatsApp funziona al meglio quando il pubblico utilizza già la piattaforma e vuoi combinare contenuti avanzati con una conversazione genuinamente bidirezionale.

| Beneficio | Perché | Casi d’uso di esempio |
| --- | --- | --- |
| Coinvolgimento globale elevato | Piattaforma di messaggistica ampiamente utilizzata e ampiamente adottata in molte aree geografiche | Raggiungere un pubblico internazionale già attivo su WhatsApp |
| Messaggi avanzati e interattivi | Supporta immagini, video, pulsanti e risposte rapide | Cataloghi di prodotti, conferme di appuntamenti con opzioni di risposta rapida |
| Esperienze di conversazione bidirezionali | I destinatari possono rispondere nello stesso thread | Conversazioni con l’Assistenza clienti, domande sul tracciamento degli ordini |
| Conformità e attendibilità tramite API ufficiale | Fornito tramite API cloud verificata di Meta con verifica del mittente | Comunicazioni verificate per il marchio che generano l’attendibilità del destinatario |
| Integrazione con altri canali | Possono essere sovrapposti con percorsi e campagne insieme ad altri canali | Percorsi multicanale che utilizzano WhatsApp come punto di contatto complementare |

## Quando non utilizzare {#when-not-to-use}

WhatsApp dipende dall’adozione del pubblico e dal consenso esplicito, quindi non è adatto a ogni scenario. Considera un altro canale nelle seguenti situazioni:

* Il tuo pubblico non utilizza WhatsApp, in quanto l’adozione varia notevolmente a seconda dell’area geografica e della popolazione
* I destinatari non hanno fornito il consenso esplicito, richiesto dai criteri di messaggistica di Meta
* Il messaggio è urgente e richiede una consegna garantita, che SMS o push gestisce meglio in base ai vincoli di consegna e revisione dei modelli di WhatsApp
* Il contenuto è lungo o complesso e più adatto alle e-mail, che offre più spazio e una formattazione più ricca
* Il supporto conversazionale in tempo reale non è fattibile da parte tua, poiché i thread WhatsApp bidirezionali impostano l’aspettativa di una risposta tempestiva

## Prerequisiti {#prereq}

L’integrazione di WhatsApp con Journey Optimizer richiede quanto segue:

* Account Business Manager di Meta
* [Account aziendale WhatsApp con nome mittente e numero di telefono verificati](https://developers.facebook.com/docs/whatsapp/overview/business-accounts/)
* [Token di autorizzazione utente con le autorizzazioni appropriate](https://developers.facebook.com/blog/post/2022/12/05/auth-tokens/)
* [Modelli di Meta approvati](https://developers.facebook.com/docs/whatsapp/message-templates/guidelines/)

Prima di procedere con l’integrazione, devi inoltre prendere atto di quanto segue:

* [Regole dei contenuti di WhatsApp](https://www.whatsapp.com/legal/messaging-guidelines)
* [Conformità ai criteri di Meta](https://www.whatsapp.com/legal)
* [Limiti di conversazione di 24 ore](https://developers.facebook.com/docs/whatsapp/messaging-limits/)

## Limitazioni {#limitations}

Al canale WhatsApp vengono applicate le seguenti limitazioni:

* Il canale WhatsApp in Adobe Journey Optimizer è compatibile con HIPAA, ma i fornitori di terze parti non sono coperti dal BAA di Adobe. La clientela è responsabile della propria conformità e della convalida dei fornitori.

* I messaggi di risposta automatizzati o predefiniti non sono ancora supportati.

* A partire da aprile 2025, la consegna di tutti i messaggi dei modelli di marketing agli utenti di WhatsApp che hanno un numero di telefono degli Stati Uniti (un numero composto da un prefisso telefonico +1 e da un codice di zona statunitense) è stata temporaneamente sospesa. [Ulteriori informazioni nella documentazione su Meta](https://developers.facebook.com/docs/whatsapp/cloud-api/guides/send-message-templates#per-user-marketing-template-message-limits)

* La funzionalità di integrazione nativa non consente l’integrazione con fornitori di servizi aziendali (BSP) di terze parti.

## Video introduttivo {#video}

Il video seguente mostra come integrare WhatsApp come canale nativo in Adobe Journey Optimizer per consegnare messaggi sicuri, in tempo reale e personalizzati su larga scala.

+++ Guarda il video

>[!VIDEO](https://video.tv.adobe.com/v/3470244?learn=on)

+++

## Risorse di apprendimento aggiuntive

Esplora ulteriori tutorial video sulla messaggistica e la configurazione di WhatsApp.

➡️ [Tutorial sul canale WhatsApp](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/channels/whatsapp/whatsapp-introduction){target="_blank"}

