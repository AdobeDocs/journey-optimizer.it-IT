---
solution: Journey Optimizer
product: journey optimizer
title: Gestione del fuso orario
description: Informazioni sulla gestione del fuso orario
feature: Journeys, Profiles
topic: Content Management
role: User
level: Intermediate
keywords: fuso orario, proprietà, percorso, condizione, ora, data, personalizzato
exl-id: 3bcc08d6-1210-4ff9-92f4-edee8285b469
source-git-commit: 21b53c72976d1a65651bc142e23ba847dc40a305
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 1%

---

# Gestione del fuso orario {#timezone_management}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_time_zone"
>title="Fuso orario"
>abstract="Seleziona il fuso orario del percorso. Quando si utilizza un fuso orario fisso, questo è lo stesso per tutti i singoli utenti che entrano nel percorso."


È possibile definire un fuso orario nel [proprietà](../building-journeys/journey-properties.md#timezone) del tuo percorso.

Per accedere alle proprietà del percorso, fai clic sull’icona della matita in alto a destra dello schermo.

Questo fuso orario verrà utilizzato per ogni attività del percorso contenente un elemento temporale come:

* [Condizione temporale](../building-journeys/condition-activity.md#time_condition)
* [Condizione data](../building-journeys/condition-activity.md#date_condition)
* [Attesa personalizzata](../building-journeys/wait-activity.md#custom)

<!--
* [Fixed date wait](../building-journeys/wait-activity.md#fixed_date)
-->

È possibile selezionare una [fuso orario fisso](#fixed-timezone) o scegliere di utilizzare il fuso orario [definito nel profilo utente](#timezone-from-profiles).

## Definire un fuso orario fisso {#fixed-timezone}

Il fuso orario può essere corretto. Cancella il fuso orario predefinito e selezionane uno dall’elenco a discesa. Se si utilizza un fuso orario fisso, questo sarà lo stesso per tutte le persone che entrano nel percorso.

A tale scopo, nella **[!UICONTROL Proprietà percorso]** , selezionare un fuso orario.

![](assets/journey72.png)

## Utilizzare il fuso orario dei profili {#timezone-from-profiles}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_profile_time_zone"
>title="Usa fuso orario del profilo"
>abstract="Seleziona la casella per utilizzare il fuso orario del profilo in tempo reale nelle attività di attesa e condizione. Se per un profilo è stato definito un fuso orario, questo verrà recuperato e utilizzato dal percorso. In caso contrario, il fuso orario sarà quello definito nel campo del fuso orario precedente."

Se l’evento di ingresso del percorso ha uno spazio dei nomi, il che significa che il percorso può raggiungere il servizio Profilo cliente in tempo reale di Adobe Experience Platform, puoi utilizzare il fuso orario definito a livello di profilo. A tale scopo, in **Proprietà**, spunta **Utilizza il fuso orario del profilo in attese e condizioni**. Questa opzione non è selezionata per impostazione predefinita.

Se per un profilo è stato definito un fuso orario, questo verrà recuperato e utilizzato dal percorso. In caso contrario, il fuso orario utilizzato sarà quello definito nel campo del fuso orario.

![](assets/journey73.png)

>[!NOTE]
>
>Il fuso orario del profilo funziona con **fuso orario** campo esistente nel **Dettagli sulle preferenze** gruppo di campi.

## Utilizzare i fusi orari nelle espressioni {#timezone-in-expressions}

Le date di inizio e di fine di un percorso non possono essere collegate a un fuso orario specifico. Vengono associate automaticamente al fuso orario dell’istanza.
