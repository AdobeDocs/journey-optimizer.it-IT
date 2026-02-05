---
title: Guida introduttiva ai criteri decisionali
description: Scopri come utilizzare i criteri di decisione per distribuire le offerte.
feature: Decisioning
topic: Integrations
role: User
level: Experienced
exl-id: 63aa1763-2220-4726-a45d-3a3a8b8a55ec
version: Journey Orchestration
source-git-commit: fb35bc5a51421818297586b5e386aa75deb1c669
workflow-type: tm+mt
source-wordcount: '674'
ht-degree: 26%

---

# Introduzione ai criteri di decisione {#create-decision}

>[!CONTEXTUALHELP]
>id="ajo_code_based_decision"
>title="Che cos’è una decisione?"
>abstract="I criteri di decisione contengono tutta la logica di selezione affinché il motore decisionale possa scegliere il contenuto migliore. I criteri di decisione sono specifici della campagna. Il loro obiettivo è selezionare le migliori offerte per ciascun profilo mentre la creazione della campagna consente di indicare come devono essere presentati gli elementi decisionali selezionati, inclusi gli attributi degli elementi da includere nel messaggio."
>additional-url="https://experienceleague.adobe.com/it/docs/journey-optimizer/using/decisioning/offer-decisioning/get-started-decision/starting-offer-decisioning" text="Informazioni sulla funzione Decisioni"

>[!CONTEXTUALHELP]
>id="ajo_journey_decision_policy"
>title="Definire un criterio di decisione"
>abstract="Un criterio di decisione consente di scegliere gli elementi migliori dal motore decisionale e di consegnarli al pubblico giusto."
>additional-url="https://experienceleague.adobe.com/it/docs/journey-optimizer/using/decisioning/offer-decisioning/get-started-decision/starting-offer-decisioning" text="Informazioni sulla funzione Decisioni"

>[!CONTEXTUALHELP]
>id="ajo_exd_decision_policy"
>title="Criterio di decisione"
>abstract="Un criterio di decisione consente di scegliere gli elementi migliori dal motore decisionale e di consegnarli a ciascun pubblico."

>[!CONTEXTUALHELP]
>id="ajo_exd_placements"
>title="Posizionamento"
>abstract="Un posizionamento determina dove vengono visualizzati in un messaggio gli elementi restituiti dal motore decisionale. Puoi tenere traccia delle relative prestazioni in diversi posizionamenti nel reporting."

>[!CONTEXTUALHELP]
>id="ajo_exd_decision_attribute"
>title="Selezionare gli attributi di decisione dal catalogo"
>abstract="Gli attributi di decisione sono memorizzati nello schema del catalogo. Seleziona un attributo da utilizzare qui dal catalogo selezionato."

I criteri di decisione sono contenitori per le offerte che sfruttano il motore di decisione per restituire in modo dinamico il contenuto migliore da consegnare per ogni membro del pubblico. Il loro obiettivo è quello di selezionare le offerte migliori per ciascun profilo, mentre l’authoring della campagna/del percorso ti consente di indicare in che modo devono essere presentati gli elementi decisionali selezionati, compresi gli attributi degli elementi da includere nel messaggio.

➡️ [Scopri questa funzione nel video](#video)

## Guardrail e limitazioni

* **Canali supportati** - I criteri di decisione sono disponibili per questi canali: esperienze basate su codice, e-mail, SMS e notifiche push.
* **Requisito SDK per le notifiche push** - Experience Decisioning con notifiche push richiede una versione specifica del SDK mobile. Prima di implementare questa funzione, controlla le [note sulla versione](https://developer.adobe.com/client-sdks/home/release-notes/){target="_blank"} per identificare la versione richiesta e assicurarti di aver effettuato l&#39;aggiornamento di conseguenza. Puoi anche visualizzare tutte le versioni di SDK disponibili per la tua piattaforma in [questa sezione](https://developer.adobe.com/client-sdks/home/current-sdk-versions/){target="_blank"}.
* **Pagine mirror e-mail** - Per il momento, gli elementi di decisione non vengono riprodotti nelle pagine mirror e-mail.
* **Tipo di tracciamento e collegamenti** - Per tenere traccia dei collegamenti generati dal decisioning, definiscili nello schema come &quot;Decisioning Assets&quot;. I collegamenti basati su attributi non sono tracciabili.
* **Nidificazione dei criteri di decisione nelle e-mail** - Non è possibile nidificare più criteri di decisione all&#39;interno di un componente e-mail principale a cui è già associato un criterio di decisione.
* **percorsi/campagne duplicati con decisioning** - Se duplichi un percorso o una campagna che include un criterio di decisione, la versione duplicata fa riferimento all&#39;e-mail o all&#39;esperienza basata su codice originale, causando errori. Riconfigura sempre il criterio di decisione dopo la duplicazione.
* **Criteri di consenso** - Gli aggiornamenti ai criteri di consenso richiedono fino a 48 ore per essere effettivi. Se un criterio di decisione fa riferimento a un attributo associato a un criterio di consenso aggiornato di recente, le modifiche non verranno applicate immediatamente.

  Analogamente, se a un criterio di decisione vengono aggiunti nuovi attributi di profilo soggetti a un criterio di consenso, questi saranno utilizzabili, ma il criterio di consenso associato a essi non verrà applicato fino a quando il ritardo non sarà passato.

  I criteri di consenso sono disponibili solo per le organizzazioni con il componente aggiuntivo Adobe Healthcare Shield o Privacy and Security Shield.

* **Classifica IA** - Per il momento, la classificazione IA non è supportata per il canale e-mail nei percorsi con decisioning.

* **Modelli di contenuto** - Tutti i criteri di decisione configurati nel contenuto non verranno salvati nel modello. Se si applica il modello a un&#39;altra azione, è necessario riconfigurare il criterio.

## Passaggi chiave {#key}

I passaggi principali per sfruttare i criteri decisionali nei messaggi sono i seguenti:

1. **Creare un criterio di decisione**

   Aggiungi un criterio di decisione nel messaggio e configura il numero di elementi da restituire, la strategia di selezione e le opzioni di fallback.

   ➡️ [Scopri come creare un criterio di decisione](../experience-decisioning/create-decision-policy.md)

1. **Utilizza il criterio di decisione nel contenuto**

   Personalizza il contenuto con l’output del criterio di decisione inserendo gli attributi dagli elementi di decisione che desideri visualizzare nel messaggio

   ➡️ [Scopri come utilizzare i criteri di decisione nei messaggi](../experience-decisioning/create-decision-policy.md)

## Video dimostrativi {#video}

Scopri come utilizzare Decisioning per personalizzare le e-mail per il pubblico.

>[!VIDEO](https://video.tv.adobe.com/v/3476158?quality=12)

Scopri come utilizzare Decisioning per personalizzare le notifiche push per il pubblico.

>[!VIDEO](https://video.tv.adobe.com/v/3479199?quality=12)

Scopri come utilizzare Decisioning per personalizzare i messaggi SMS per il pubblico.

>[!VIDEO](https://video.tv.adobe.com/v/3479529?quality=12)
