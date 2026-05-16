---
solution: Journey Optimizer
product: journey optimizer
title: campi del percorso
description: campi del percorso
feature: Journeys, Reporting
topic: Content Management
role: Developer, Admin
level: Experienced
exl-id: 177b4a97-c757-40ca-a190-fbd88169e5e2
TQID: https://experienceleague.adobe.com/dpQ6PEm-afX4PZuWSPrpAWDH7yBhUKZHZRF134VehAg
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
subfeature_v2:
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 130
ht-degree: 6%

---

# Campi del percorso {#sharing-journey-fields}

Questo gruppo di campi è utilizzato nello schema **percorso** (in relazione a **journeyStepEvent**). Contiene i campi elencati di seguito.


>[!NOTE]
>
>Ulteriori informazioni sugli attributi delle proprietà del percorso [in questa sezione](../building-journeys/expression/journey-properties.md#journey-properties-fields).


## journeyID {#journeyid-field}

ID del percorso principale.

Tipo: stringa

## journeyVersionID {#journeyversionid-field}

ID della versione del percorso. Questo ID rappresenta l’identità di un percorso.

Tipo: stringa

## name {#name-field}

Nome del percorso.

Tipo: stringa

>[!NOTE]
>
>Il nome del percorso viene utilizzato per collegare i dati di esecuzione del percorso con i set di dati di reporting. Se rinomini un percorso, assicurati che il nuovo nome corrisponda al nome nel set di dati di reporting per mantenere una generazione rapporti accurata. Una mancata corrispondenza può causare la mancata visualizzazione dei dati di reporting come previsto. Ulteriori informazioni su [risoluzione dei problemi relativi ai dati mancanti](../building-journeys/report-journey.md#troubleshooting-missing-data).

## descrizione {#description-field}

Descrizione del percorso.

Tipo: stringa

## version {#version-field}

Versione, rappresentata come `major`.`minor`

Tipo: stringa
