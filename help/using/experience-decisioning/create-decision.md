---
title: Guida introduttiva ai criteri decisionali
description: Scopri come utilizzare i criteri di decisione per distribuire le offerte.
feature: Decisioning
topic: Integrations
role: User
level: Experienced
exl-id: 63aa1763-2220-4726-a45d-3a3a8b8a55ec
version: Journey Orchestration
source-git-commit: 0b94bfeaf694e8eaf0dd85e3c67ee97bd9b56294
workflow-type: tm+mt
source-wordcount: '612'
ht-degree: 29%

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

>[!AVAILABILITY]
>
>Per il momento, i criteri decisionali sono disponibili per tutti i clienti del canale di esperienza basato su codice. Sono disponibili per il canale e-mail come Disponibilità limitata. Per ottenere l’accesso, contatta il tuo rappresentante Adobe.

## Passaggi chiave {#key}

I passaggi principali per sfruttare i criteri decisionali nei messaggi sono i seguenti:

1. [Creare un criterio di decisione](../experience-decisioning/create-decision-policy.md)

   Imposta un criterio di decisione nel messaggio scegliendo il numero di elementi da restituire, configurando strategie di selezione, opzioni di fallback e ordine di valutazione.

1. [Utilizzare il criterio di decisione nel contenuto](../experience-decisioning/use-decision-policy.md)

   Personalizza il contenuto con l’output del criterio di decisione e gli attributi degli elementi di decisione che desideri visualizzare nel messaggio.

1. [Creare dashboard di reporting](cja-reporting.md)

   Crea dashboard di Customer Journey Analytics personalizzati per misurare le prestazioni e ottenere informazioni approfondite su come vengono distribuite e utilizzate le politiche e le offerte decisionali.

## Guardrail e limitazioni

* **Pagine mirror e-mail** - Per il momento, gli elementi di decisione non vengono riprodotti nelle pagine mirror e-mail.
* **Tipo di tracciamento e collegamenti** - Per tenere traccia dei collegamenti generati dal decisioning, definiscili nello schema come &quot;Decisioning Assets&quot;. I collegamenti basati su attributi non sono tracciabili.
* **Nidificazione dei criteri di decisione nelle e-mail** - Non è possibile nidificare più criteri di decisione all&#39;interno di un componente e-mail principale a cui è già associato un criterio di decisione.
* **percorsi/campagne duplicati con decisioning** - Se duplichi un percorso o una campagna che include un criterio di decisione, la versione duplicata fa riferimento all&#39;e-mail o all&#39;esperienza basata su codice originale, causando errori. Riconfigura sempre il criterio di decisione dopo la duplicazione.
* **Criteri di consenso** - Gli aggiornamenti ai criteri di consenso richiedono fino a 48 ore per essere effettivi. Se un criterio di decisione fa riferimento a un attributo associato a un criterio di consenso aggiornato di recente, le modifiche non verranno applicate immediatamente.

  Analogamente, se a un criterio di decisione vengono aggiunti nuovi attributi di profilo soggetti a un criterio di consenso, questi saranno utilizzabili, ma il criterio di consenso associato a essi non verrà applicato fino a quando il ritardo non sarà passato.

  I criteri di consenso sono disponibili solo per le organizzazioni con il componente aggiuntivo Adobe Healthcare Shield o Privacy and Security Shield.

* **Classifica IA** - Per il momento, la classificazione IA non è supportata per il canale e-mail nei percorsi con decisioning.

## Passaggi successivi {#next-steps}

Ora che sai come funzionano i criteri di decisione e come aiutano a fornire offerte personalizzate, puoi creare il tuo primo criterio di decisione.

➡️ [Scopri come creare un criterio di decisione](../experience-decisioning/create-decision-policy.md)

