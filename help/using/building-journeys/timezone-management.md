---
solution: Journey Optimizer
product: journey optimizer
title: Gestione del fuso orario
description: Informazioni sulla gestione del fuso orario
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: fuso orario, proprietà, percorso, condizione, ora, data, personalizzato
exl-id: 3bcc08d6-1210-4ff9-92f4-edee8285b469
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 2%

---

# Gestione del fuso orario {#timezone_management}

È possibile definire un fuso orario nel [proprietà](../building-journeys/journey-gs.md#change-properties) del tuo percorso.

Per accedere a Proprietà Percorso, fai clic sull’icona della matita in alto a destra dello schermo.

Questo fuso orario verrà utilizzato per ogni attività del percorso contenente un elemento temporale come:

* [Condizione temporale](../building-journeys/condition-activity.md#time_condition)
* [Condizione data](../building-journeys/condition-activity.md#date_condition)
* [Attesa personalizzata](../building-journeys/wait-activity.md#custom)

<!--
* [Fixed date wait](../building-journeys/wait-activity.md#fixed_date)
-->

Puoi selezionare un fuso orario o scegliere di utilizzare quello definito nel profilo utente.

>[!NOTE]
>
>Il fuso orario del profilo funziona con **fuso orario** campo esistente nel **Dettagli sulle preferenze** gruppo di campi.

## Definire un fuso orario fisso {#fixed-timezone}

È inoltre possibile correggere il fuso orario. Cancella il fuso orario predefinito e selezionane uno dall’elenco a discesa. Se si utilizza un fuso orario fisso, questo sarà lo stesso per tutte le persone che entrano nel percorso.

A tale scopo, nella **[!UICONTROL Proprietà percorso]** , selezionare un fuso orario.

![](assets/journey72.png)

## Utilizzare i profili per definire il fuso orario del percorso {#timezone-from-profiles}

Se l’evento di ingresso del percorso ha uno spazio dei nomi, il che significa che il percorso può raggiungere il servizio Profilo cliente in tempo reale di Adobe Experience Platform, puoi utilizzare il fuso orario definito a livello di profilo. A tale scopo, in **Proprietà**, spunta **Utilizza il fuso orario del profilo in attese e condizioni**. Questa opzione non è selezionata per impostazione predefinita.

Se per un profilo è stato definito un fuso orario, questo verrà recuperato e utilizzato dal percorso. In caso contrario, il fuso orario utilizzato sarà quello definito nel campo del fuso orario.

![](assets/journey73.png)

## Utilizzare i fusi orari nelle espressioni {#timezone-in-expressions}

Le date di inizio e di fine di un percorso non possono essere collegate a un fuso orario specifico. Vengono associate automaticamente al fuso orario dell’istanza.
