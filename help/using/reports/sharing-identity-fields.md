---
title: Campi di identità dell’evento di journeyStep
description: Campi di identità dell’evento di journeyStep
feature: Reporting
topic: Gestione dei contenuti
role: User
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 24%

---

# Campi di identità dell’evento di journeyStep {#sharing-identity-fields}

![](../assets/do-not-localize/badge.png)

Questo mixin è specifico per journeyStepEvent: questo evento è in relazione al percorso e non ha identityMap che descrive l&#39;eventuale identità del profilo.

Per journeyStepEvent, è inoltre necessario aggiungere campi relativi all’identità:

## profileID

Identificatore profilo

Tipo: string

## profileNamespace

Spazio dei nomi dell’identificatore del profilo

Tipo: string
