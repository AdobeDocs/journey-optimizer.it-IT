---
solution: Journey Optimizer
product: journey optimizer
title: Utilizzare l’attività Attendi nelle campagne orchestrate
description: Scopri come utilizzare l’attività Attendi nelle campagne orchestrate
exl-id: 11ef095b-77ec-4e2e-ab4d-49a248354f08
version: Campaign Orchestration
source-git-commit: 07ec28f7d64296bdc2020a77f50c49fa92074a83
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 77%

---


# Attendi {#wait}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_wait"
>title="Attività Attendi"
>abstract="L’attività **Attendi** viene utilizzata per ritardare la transizione da un’attività a un’altra."

L&#39;attività **[!UICONTROL Wait]** è un componente del **[!UICONTROL controllo di flusso]** utilizzato per introdurre un ritardo tra due attività in una campagna orchestrata. In questo modo le attività di follow-up saranno più tempestive e rilevanti per il coinvolgimento dell’utente.

Ad esempio, puoi attendere alcuni giorni dopo una consegna e-mail per tenere traccia di aperture e clic prima di inviare un messaggio di follow-up.

## Configurazione{#wait-configuration}

Per configurare l’attività **[!UICONTROL Attendi]**, segui questi passaggi:

1. Aggiungi un&#39;attività **[!UICONTROL Wait]** alla campagna orchestrata.

1. Seleziona il tipo di Attesa più adatta alle tue esigenze:

   * **[!UICONTROL Durata]**: specifica un ritardo in secondi, minuti, ore o giorni prima di procedere all’attività successiva.

   * **[!UICONTROL Ora fissa]**: imposta una data e un’ora specifiche dopo le quali inizia l’attività successiva.

   ![](../assets/wait_activity.png)

## Esempio{#wait-example}

L’esempio seguente illustra l’attività **[!UICONTROL Attendi]** in un caso d’uso tipico.  Un’e-mail con un codice promozionale viene inviata ai profili che festeggiano il loro compleanno. Dopo 29 giorni, un SMS viene inviato allo stesso gruppo per ricordare che il codice promozionale in occasione del compleanno sta per scadere.

![](../assets/wait-example.png)
