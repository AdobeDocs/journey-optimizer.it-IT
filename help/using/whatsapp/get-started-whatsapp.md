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
source-git-commit: 31e25c511d8873e54c7b92e65511108a77f84941
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 44%

---

# Introduzione ai messaggi WhatsApp {#get-started-whatsapp}

Ora puoi inviare messaggi WhatsApp direttamente tramite Journey Optimizer tramite l&#39;[API Cloud](https://developers.facebook.com/docs/whatsapp/cloud-api/) di Meta. Questa funzione consente l’integrazione diretta di WhatsApp in percorsi e campagne, migliorando la comunicazione e il coinvolgimento con i destinatari.

* In un **percorso**. Crea un percorso, aggiungi un’attività **WhatsApp** e definisci le impostazioni di base, quindi passa al riquadro a destra **[!UICONTROL Azioni: WhatsApp]** per creare il contenuto per il messaggio WhatsApp. Ulteriori informazioni su come creare un percorso sono disponibili in [questa pagina](../building-journeys/journey-gs.md).

* In una **campagna**. Crea una campagna, seleziona **WhatsApp** come azione e definisci le impostazioni di base, quindi modifica il contenuto del messaggio per definire il messaggio WhatsApp da inviare. Ulteriori informazioni su come creare una campagna sono disponibili in [questa pagina](../campaigns/create-campaign.md#configure).

![](assets/do-not-localize/whatsapp-beta.png){zoomable="yes"}

## Prerequisiti {#prereq}

L’integrazione di WhatsApp con Journey Optimizer richiede quanto segue:

* Account Business Manager di Meta
* [Account aziendale WhatsApp con nome mittente e numero di telefono verificati](https://developers.facebook.com/docs/whatsapp/overview/business-accounts/)
* [Token di autorizzazione utente con autorizzazioni appropriate](https://developers.facebook.com/blog/post/2022/12/05/auth-tokens/)
* [Modelli di Meta approvati](https://developers.facebook.com/docs/whatsapp/message-templates/guidelines/)

Prima di procedere con l’integrazione, devi inoltre prendere atto di quanto segue:

* [Regole dei contenuti di WhatsApp](https://www.whatsapp.com/legal/messaging-guidelines)
* [Conformità ai criteri di Meta](https://www.whatsapp.com/legal)
* [Limiti di conversazione di 24 ore](https://developers.facebook.com/docs/whatsapp/messaging-limits/)

## Limitazioni {#limitations}

Al canale WhatsApp si applicano le seguenti limitazioni:

* Il canale WhatsApp in Adobe Journey Optimizer è compatibile con HIPAA, ma i fornitori di terze parti non sono coperti dalla BAA di Adobe. I clienti sono responsabili della conformità e della convalida dei fornitori.

* I messaggi di risposta automatizzati o predefiniti non sono ancora supportati.

* A partire da aprile 2025, la consegna di tutti i messaggi dei modelli di marketing agli utenti WhatsApp che hanno un numero di telefono degli Stati Uniti (un numero composto da un codice di chiamata +1 e un indicativo di località statunitense) è stata temporaneamente sospesa. [Ulteriori informazioni nella documentazione Meta](https://developers.facebook.com/docs/whatsapp/cloud-api/guides/send-message-templates#per-user-marketing-template-message-limits)

* La funzionalità di integrazione nativa non consente l&#39;integrazione con Business Service Provider (BSP) di terze parti.

## Video dimostrativo {#video}

Il video seguente mostra come integrare WhatsApp come canale nativo in Adobe Journey Optimizer per inviare messaggi sicuri, in tempo reale e personalizzati su larga scala.

+++ Guarda il video

>[!VIDEO](https://video.tv.adobe.com/v/3470252?learn=on&captions=ita)

+++

