---
title: Nuovi tentativi
description: Scopri come vengono eseguiti i nuovi tentativi prima di inviare un indirizzo all’elenco di soppressione
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 05564a99-da50-4837-8dfb-bb1d3e0f1097
source-git-commit: 40c42303b8013c1d9f4dd214ab1acbec2942e094
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 2%

---

# Nuovi tentativi {#retries}

Quando un messaggio e-mail non riesce a causa di un messaggio temporaneo **Rimbalzo morbido** errore, vengono eseguiti diversi tentativi. Ogni errore incrementa un contatore di errori. Quando questo contatore raggiunge la soglia limite, l’indirizzo viene aggiunto all’elenco di soppressione.

>[!NOTE]
>
>Ulteriori informazioni sui tipi di errori nel [Tipi di errori di consegna](../reports/suppression-list.md#delivery-failures) sezione .

Nella configurazione predefinita, la soglia è impostata su 5 errori.

* Per la stessa consegna, alla quinta si è verificato un errore all’interno del [periodo di tempo di nuovo](#retry-duration), l’indirizzo viene soppresso.

* Se ci sono consegne diverse e due errori si verificano almeno a 24 ore di distanza, il contatore degli errori viene incrementato a ogni errore e l’indirizzo viene eliminato anche al quinto tentativo.

Se una consegna ha esito positivo dopo un nuovo tentativo, il contatore di errori dell’indirizzo viene reinizializzato.

Nel caso in cui il valore predefinito di 5 non soddisfi le tue esigenze, puoi modificare la soglia di errore seguendo la procedura seguente.

1. Vai a **[!UICONTROL Channels]** > **[!UICONTROL Email configuration]** > **[!UICONTROL Suppression list]**.

1. Fai clic sul pulsante **[!UICONTROL Edit suppression rules]**.

   ![](assets/suppression-list-edit-retries.png)

1. Modifica il numero consentito di mancati recapiti consecutivi in base alle tue esigenze.

   ![](assets/suppression-list-edit-soft-bounces.png)

   È necessario immettere un valore intero compreso tra 1 e 20, il che significa che il numero minimo di tentativi è 1 e il numero massimo è 20.

   >[!CAUTION]
   >
   >Qualsiasi valore superiore a 10 può causare problemi di reputazione del recapito messaggi, nonché limitazione o inserire nell&#39;elenco Bloccati IP da parte degli ISP. [Ulteriori informazioni sul recapito messaggi](../reports/deliverability.md)

## Periodo di tempo di un nuovo tentativo {#retry-duration}

La **periodo di tempo di nuovo** è l’intervallo di tempo entro il quale verrà ritentato qualsiasi messaggio e-mail della consegna che abbia rilevato un errore temporaneo o un messaggio non recapitato.

Per impostazione predefinita, vengono eseguiti nuovi tentativi per **3,5 giorni** o **84 ore**) dal momento in cui il messaggio è stato aggiunto alla coda e-mail.

Tuttavia, per evitare che i tentativi non vengano più eseguiti quando non sono più necessari, è possibile modificare questa impostazione in base alle proprie esigenze durante la creazione o la modifica di un [predefinito messaggio](message-presets.md) applicazione al canale e-mail.

Ad esempio, puoi impostare il periodo di esecuzione dei nuovi tentativi su 24 ore per un’e-mail transazionale relativa alla reimpostazione della password e contenente un collegamento valido solo per un giorno. Allo stesso modo, per una vendita a mezzanotte, è possibile definire un periodo di esecuzione di un nuovo tentativo di 6 ore.

>[!NOTE]
>
>Il periodo di esecuzione dei nuovi tentativi non può superare le 84 ore. Il periodo minimo di esecuzione dei nuovi tentativi è di 6 ore per le e-mail di marketing e 10 minuti per le e-mail transazionali.

Scopri come regolare i parametri di esecuzione di un nuovo tentativo e-mail durante la creazione di un predefinito per messaggi in [questa sezione](message-presets.md#create-message-preset).

