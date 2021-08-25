---
title: Nuovi tentativi
description: Scopri come vengono eseguiti i nuovi tentativi prima di inviare un indirizzo all’elenco di soppressione
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
source-git-commit: 79c3c47eb6978f377bf4dc49f787e9a509aa3f61
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 0%

---


# Nuovi tentativi {#retries}

Quando un messaggio e-mail non riesce a causa di un errore temporaneo **Soft bounce** o **Ignored** , vengono eseguiti diversi tentativi. Ogni errore incrementa un contatore di errori. Quando questo contatore raggiunge la soglia limite, l’indirizzo viene aggiunto all’elenco di soppressione.

>[!NOTE]
>
>Ulteriori informazioni sui tipi di errori nella sezione [Tipi di errori di consegna](../suppression-list.md#delivery-failures) .

Nella configurazione predefinita, la soglia è impostata su tre errori:

* Per la stessa consegna, alla terza si è verificato un errore, l’indirizzo viene soppresso.

* Se ci sono consegne diverse e due errori si verificano almeno a 24 ore di distanza, il contatore degli errori viene incrementato a ogni errore e l’indirizzo viene eliminato anche al terzo tentativo.

Se una consegna ha esito positivo dopo un nuovo tentativo, il contatore di errori dell’indirizzo viene reinizializzato.

Puoi modificare la soglia limite utilizzando il pulsante **[!UICONTROL Edit]** dal menu **[!UICONTROL Channels]** > **[!UICONTROL Email configuration]** > **[!UICONTROL General]** .

![](../assets/retries-edition.png)

<!--The minimum delay between retries and the maximum number of retries to be performed are based on how well an IP is performing, both historically and currently, at a given domain.-->

## Periodo di tempo di un nuovo tentativo {#retry-duration}

Il **periodo di tempo per l&#39;esecuzione di un nuovo tentativo** è l&#39;intervallo di tempo in cui verrà ritentato qualsiasi messaggio e-mail della consegna che ha rilevato un errore temporaneo o un messaggio non recapitato.

Per impostazione predefinita, i nuovi tentativi vengono eseguiti per **3,5 giorni** (o **84 ore**) dal momento in cui il messaggio è stato aggiunto alla coda e-mail.

Tuttavia, per evitare che i tentativi non vengano più eseguiti quando non sono più necessari, puoi modificare questa impostazione in base alle tue esigenze quando crei o modifichi un [messaggio preimpostato](message-presets.md) applicabile al canale e-mail.

Ad esempio, puoi impostare il periodo di esecuzione dei nuovi tentativi su 24 ore per un’e-mail transazionale relativa alla reimpostazione della password e contenente un collegamento valido solo per un giorno. Allo stesso modo, per una vendita a mezzanotte, è possibile definire un periodo di esecuzione di un nuovo tentativo di 6 ore.

>[!NOTE]
>
>Il periodo di esecuzione dei nuovi tentativi non può superare le 84 ore. Il periodo minimo di esecuzione dei nuovi tentativi è di 6 ore per le e-mail di marketing e 10 minuti per le e-mail transazionali.

Scopri come regolare i parametri dei tentativi e-mail durante la creazione di un predefinito messaggio in [questa sezione](message-presets.md#create-message-preset).

<!--After 3.5 days, any message in the retry queue will be removed from the queue and sent back as a bounce.-->