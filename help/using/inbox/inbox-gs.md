---
title: Creare una casella in entrata
description: Inizia a utilizzare la casella in entrata in Adobe Journey Optimizer per recapitare messaggi persistenti e non invasivi agli utenti.
feature: Content Cards
topic: Content Management
role: User
level: Beginner
exl-id: 60190d0b-d8e7-4a78-9924-d948f2769f6c
source-git-commit: c2bb6cf702a14b4eef8f2209082e39cd73338378
workflow-type: ht
source-wordcount: '453'
ht-degree: 100%

---

# Introduzione alla casella in entrata {#inbox-gs}

>[!BEGINSHADEBOX]

**In questa pagina:** scopri come il canale della casella in entrata conserva i messaggi di marketing in un unico spazio persistente all’interno dell’app o del sito web, consentendo agli utenti di tornare a leggerli e di interagire con essi quando preferiscono.

>[!ENDSHADEBOX]

La casella in entrata recapita messaggi persistenti e senza problemi in un’unica posizione all’interno dell’app mobile o del sito web. I messaggi in-app e push possono scomparire dopo un scorrimento o un tocco; la casella in entrata mantiene i messaggi disponibili in modo che le persone possano aprirli, leggerli e agire di conseguenza quando necessario.

La casella in entrata si basa sul canale Scheda contenuto e aggiunge:

* **Messaggistica persistente**: il contenuto rimane nella casella in entrata fino alla rimozione o alla scadenza, pertanto gli utenti possono tornarvi dopo aver chiuso una notifica o l’app.
* **Posizione centralizzata**: cassetta postale unica nell’app o nel sito per messaggi di marketing rilevanti.
* **Implementazione flessibile**: utilizza il contenitore predefinito della casella in entrata o personalizza l’esperienza nella tua interfaccia utente.
* **Stato lettura**: i messaggi possono essere contrassegnati come letti o non letti nel dispositivo in cui sono aperti.

## Guida introduttiva

Per configurare e utilizzare la casella in entrata, segui la procedura riportata di seguito:

1. [Configurare Adobe Journey Optimizer](inbox-configuration.md)

   Aggiungi una configurazione del canale della **casella in entrata** in **Configurazioni canale** in modo che Journey Optimizer sappia dove e come viene eseguita la casella in entrata (pagina o regola Web oppure superficie dell’app mobile).

1. [Creare la casella in entrata in Journey Optimizer](inbox-create.md)

   Crea una campagna che utilizza l’azione **Scheda contenuto** e scegli **Casella in entrata** come posizione di consegna, pianificata dall’interfaccia utente o attivata dall’API.

1. [Progettare la casella in entrata](inbox-design.md)

   Scegli i modelli per la casella in entrata e i layout ad elenco o espansi per fare in modo che i messaggi si adattino al brand e all’esperienza utente.

1. [Creare la scheda contenuto e collegarla alla casella in entrata](../content-card/create-content-card.md)

   Crea il contenuto della scheda nel designer, completa le opzioni specifiche per la casella in entrata, quindi attiva la campagna in modo che i messaggi raggiungano la casella in entrata.

## Risorse aggiuntive

* [Interfaccia utente della casella in entrata (iOS)](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/inbox-ui/iOS): requisiti, superficie API pubblica, impostazioni della casella in entrata e collegamenti ai tutorial per l’implementazione della casella in entrata di Journey Optimizer in un’app iOS con Adobe Experience Platform Mobile SDK (iOS 15 o versioni successive, Xcode 15 o versioni successive, Swift 5.1 o versioni successive).

* [Recupero e visualizzazione della casella in entrata](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/inbox-ui/Android/tutorial/displaying-inbox): carica i messaggi della casella in entrata di Journey Optimizer ed esegui il rendering dell’interfaccia utente della casella in entrata su Android (documentazione di Adobe Developer).

* [Personalizzazione della casella in entrata](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/inbox-ui/Android/tutorial/customizing-inbox): regola il layout, lo stile e il comportamento di interazione della casella in entrata per la tua app Android (documentazione di Adobe Developer).

* [Ascolto degli eventi della casella in entrata](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/inbox-ui/Android/tutorial/listening-inbox-events): iscriviti ai callback della casella in entrata per le azioni dell’utente e gli aggiornamenti del ciclo di vita su Android (documentazione di Adobe Developer).
