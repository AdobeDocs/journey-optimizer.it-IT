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
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/PdwGEuWqJcncbkokE0eOhMaEk9L0AmCJ--VZBxxtDDU
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: a5d9be4fcfcb52bb1ee65096262e18feaa2ce4b1
workflow-type: tm+mt
source-wordcount: 418
ht-degree: 15%

---

# Gestione del fuso orario {#timezone_management}

>[!BEGINSHADEBOX]

**In questa pagina:** scopri come impostare il fuso orario di un percorso, fisso o derivato da ciascun profilo, per controllare quando vengono eseguite attività basate sul tempo come condizioni temporali, condizioni di data e attese personalizzate.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_time_zone"
>title="Fuso orario del percorso"
>abstract="L’impostazione del fuso orario definisce il fuso orario del percorso. Quando si utilizza un fuso orario fisso, questo è lo stesso per tutti i singoli utenti che entrano nel percorso."


Puoi definire un fuso orario nelle [proprietà](../building-journeys/journey-properties.md#timezone) del tuo percorso.

Per accedere alle proprietà del percorso, seleziona l’icona a forma di matita in alto a destra dello schermo.

Questo fuso orario verrà utilizzato per ogni attività del percorso contenente un elemento temporale come:

* [Condizione temporale](../building-journeys/conditions.md#time_condition)
* [Condizione data](../building-journeys/conditions.md#date_condition)
* [Attesa personalizzata](../building-journeys/wait-activity.md#custom)

<!--
* [Fixed date wait](../building-journeys/wait-activity.md#fixed_date)
-->

È possibile selezionare un [fuso orario fisso](#fixed-timezone) o scegliere di utilizzare il fuso orario [definito nel profilo utente](#timezone-from-profiles).

## Definire un fuso orario fisso {#fixed-timezone}

Il fuso orario può essere corretto. Cancella il fuso orario predefinito e selezionane uno dall’elenco a discesa. Se si utilizza un fuso orario fisso, questo sarà lo stesso per tutte le persone che entrano nel percorso.

A tale scopo, nel riquadro **[!UICONTROL Proprietà Percorso]** selezionare un fuso orario.

![Elenco a discesa per la selezione del fuso orario nelle proprietà del percorso](assets/journey72.png)

## Utilizzare il fuso orario del profilo {#timezone-from-profiles}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties_profile_time_zone"
>title="Utilizzare il fuso orario del profilo"
>abstract="Questa opzione utilizza il fuso orario del profilo in tempo reale nelle attività **Wait** e **Condition**. Se per un profilo è stato definito un fuso orario, questo verrà recuperato e utilizzato dal percorso. In caso contrario, viene usato il fuso orario definito nel campo del fuso orario precedente."

Se l&#39;evento di ingresso del percorso ha uno spazio dei nomi, il che significa che il percorso può raggiungere il servizio Profilo cliente in tempo reale di [!DNL Adobe Experience Platform], è possibile utilizzare il fuso orario definito a livello di profilo. A tale scopo, in **Proprietà**, selezionare **Usa fuso orario profilo in attese e condizioni**. Questa opzione non è selezionata per impostazione predefinita.

Se per un profilo è stato definito un fuso orario, questo viene recuperato e utilizzato dal percorso. In caso contrario, il fuso orario utilizzato è quello definito nel campo corrispondente.

![Configurazione del fuso orario del profilo nelle origini dati per intervalli personalizzati](assets/journey73.png)

>[!NOTE]
>
>Il fuso orario del profilo funziona con il campo **fuso orario** esistente nel gruppo di campi **Dettagli preferenza**.

## Utilizzare i fusi orari nelle espressioni {#timezone-in-expressions}

Le date di inizio e di fine di un percorso non possono essere collegate a un fuso orario specifico. Vengono associate automaticamente al fuso orario dell’istanza.
