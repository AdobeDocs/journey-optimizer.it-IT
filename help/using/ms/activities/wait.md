---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare l’attività Attendi nelle campagne orchestrate
description: Scopri come utilizzare l’attività Attendi nelle campagne orchestrate
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 11ef095b-77ec-4e2e-ab4d-49a248354f08
source-git-commit: bdc584c1aae0c735d81dfc95e11f96f755bea26a
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 78%

---

# Attendere {#wait}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_wait"
>title="Attività Attendi"
>abstract="L’attività **Attendi** viene utilizzata per ritardare la transizione da un’attività a un’altra."

L’attività **Attendi** è un’attività di **Controllo del flusso**. Questa attività viene utilizzata per lasciare che trascorra un certo periodo di tempo tra due attività in corso. Ad esempio, per attendere diversi giorni dopo un’attività di consegna e-mail, quindi analizzare le aperture e i clic generati durante questo periodo prima di eseguire eventuali operazioni di follow-up (e-mail di promemoria, creazione di un pubblico, ecc.).

## Configurazione{#wait-configuration}

Per configurare l’attività **Attendi**, segui questi passaggi:

1. Aggiungi un&#39;attività **Wait** alla campagna orchestrata.

1. Specifica la **Durata** dell’attesa tra le transizioni in entrata e in uscita.

1. Selezionare l&#39;unità di tempo nel campo **Periodi**: secondi, minuti, ore, giorni.

## Esempio{#wait-example}

L’esempio seguente illustra l’attività **Attendi** in un caso d’uso tipico. Viene inviata un’e-mail di invito a un evento. 24 ore dopo l’invio, viene inviata una consegna SMS alla stessa popolazione.

![](../assets/workflow-wait-example.png)
