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
feature: Impostazioni applicazione
topic: Amministrazione
role: Admin
level: Intermediate
source-git-commit: 63de381ea3a87b9a77bc6f1643272597b50ed575
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 2%

---


# Nuovi tentativi {#retries}

Quando un messaggio non riesce a causa di un errore temporaneo **Soft bounce** o **Ignored** , vengono eseguiti diversi tentativi. Ogni errore incrementa un contatore di errori. Quando questo contatore raggiunge la soglia limite, l’indirizzo viene aggiunto all’elenco di soppressione.

Nella configurazione predefinita<!--so can you edit this setting or not?? contradictory information was given-->, la soglia è impostata su tre errori:

* Per la stessa consegna, alla terza si è verificato un errore, l’indirizzo viene soppresso.

* Se ci sono consegne diverse e due errori si verificano almeno a 24 ore di distanza, il contatore degli errori viene incrementato a ogni errore e l’indirizzo viene eliminato anche al terzo tentativo.

Se una consegna ha esito positivo dopo un nuovo tentativo, il contatore di errori dell’indirizzo viene reinizializzato.

Puoi modificare la soglia limite utilizzando il pulsante **[!UICONTROL Edit]** dal menu **[!UICONTROL Channels]** > **[!UICONTROL Email configuration]** > **[!UICONTROL General]**.<!--currently you can edit this in staging // now I see in UI: Suppression rule > Bounce days??? > 4-->

![](../assets/retries-edition.png)

## Durata dell&#39;esecuzione di un nuovo tentativo messaggio {#retry-duration}

I tentativi verranno eseguiti per **3,5 giorni** dal momento in cui il messaggio è stato aggiunto alla coda e-mail.

Il ritardo minimo tra i nuovi tentativi e il numero massimo di tentativi da eseguire è <!--managed by the Enhanced MTA,--> in base alle prestazioni di un IP, sia storicamente che attualmente in un determinato dominio.

Dopo 3,5 giorni, qualsiasi messaggio nella coda dei nuovi tentativi verrà rimosso dalla coda e inviato nuovamente come messaggio non recapitato.<!--???-->