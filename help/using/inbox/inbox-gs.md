---
title: Creare una casella in entrata
description: Inizia a usare la casella in entrata in Adobe Journey Optimizer per inviare messaggi persistenti e non intrusivi agli utenti.
feature: Content Cards
topic: Content Management
role: User
level: Beginner
exl-id: 60190d0b-d8e7-4a78-9924-d948f2769f6c
source-git-commit: f7f303685e954614b44a9b62368460e9b07b26b3
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 1%

---

# Introduzione alla casella in entrata {#inbox-gs}

La casella in entrata distribuisce messaggi persistenti e a basso attrito in un’unica posizione all’interno dell’app mobile o del sito web. I messaggi in-app e push possono scomparire dopo un passaggio rapido o un tocco; la casella in entrata mantiene i messaggi disponibili in modo che le persone possano aprirli, leggerli e agire di conseguenza quando necessario.

La casella in entrata si basa sul canale Schede di contenuto e aggiunge:

* **Messaggistica persistente**: il contenuto rimane nella cartella Posta in arrivo fino alla rimozione o alla scadenza, quindi gli utenti possono tornare alla cartella dopo aver chiuso una notifica o abbandonato l&#39;app.
* **Posizione centralizzata**: una singola cassetta postale nell&#39;app o nel sito per messaggi di marketing rilevanti.
* **Implementazione flessibile**: utilizza il contenitore già pronto per la posta in arrivo o personalizza l&#39;esperienza nella tua interfaccia utente.
* **Stato lettura**: i messaggi possono essere contrassegnati come letti o non letti nel dispositivo in cui sono aperti.

## Guida introduttiva

Per configurare e utilizzare la casella in entrata, segui la procedura riportata di seguito:

1. [Configurare Adobe Journey Optimizer](inbox-configuration.md)

   Aggiungi una configurazione di canale **Posta in arrivo** in **Configurazioni canale** in modo che Journey Optimizer sappia dove e come viene eseguita la casella in entrata (pagina Web, regola o superficie dell&#39;app mobile).

1. [Creare la casella in entrata in Journey Optimizer](inbox-create.md)

   Crea una campagna che utilizza l&#39;azione **Scheda contenuto** e scegli **Casella in entrata** come percorso di consegna, pianificato dall&#39;interfaccia utente o attivato dall&#39;API.

1. [Progettare la casella in entrata](inbox-design.md)

   Scegli i modelli di casella in entrata e elenca o espandi i layout in modo che i messaggi corrispondano al tuo marchio e all’interfaccia utente.

1. [Crea la scheda dei contenuti e collegala alla casella in entrata](../content-card/create-content-card.md)

   Crea il contenuto della scheda nella finestra di progettazione, completa le opzioni specifiche per la casella in entrata, quindi attiva la campagna in modo che i messaggi raggiungano la casella in entrata.

## Risorse aggiuntive

* [Interfaccia utente casella in entrata (iOS)](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/inbox-ui/iOS/): requisiti, superficie API pubblica, impostazioni casella in entrata e collegamenti a tutorial per l&#39;implementazione di Casella in entrata Journey Optimizer in un&#39;app iOS con Adobe Experience Platform Mobile SDK (iOS 15 o versione successiva, Xcode 15 o versione successiva, Swift 5.1 o versione successiva).

* [Recupera e visualizza casella in entrata](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/inbox-ui/Android/tutorial/displaying-inbox/): carica i messaggi della casella in entrata di Journey Optimizer ed esegui il rendering dell&#39;interfaccia utente della casella in entrata su Android (documentazione di Adobe Developer).

* [Personalizzazione della casella in entrata](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/inbox-ui/Android/tutorial/customizing-inbox/): regola il layout, lo stile e il comportamento di interazione della casella in entrata per la tua app Android (documentazione di Adobe Developer).

* [Ascolto degli eventi della casella in entrata](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/inbox-ui/Android/tutorial/listening-inbox-events/): abbonati ai callback della casella in entrata per le azioni dell&#39;utente e gli aggiornamenti del ciclo di vita su Android (documentazione di Adobe Developer).
