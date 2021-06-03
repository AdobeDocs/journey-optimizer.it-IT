---
title: Delega sottodomini
description: Scopri come delegare i sottodomini
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
source-git-commit: da995c56b59fb191934788c7aea9048123a2fe6d
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 43%

---


# Guida introduttiva alla delega dei sottodomini

## Isolare i marchi per proteggere la reputazione

Un sottodominio è una divisione del dominio che può essere utilizzata per isolare i brand o vari tipi di traffico (messaggi transazionali, informazioni di marketing, ecc.).
Prendiamo ad esempio il dominio “mybrand.com”, che viene utilizzato per inviare comunicazioni transazionali e di marketing. In questa situazione, puoi decidere di impostare due sottodomini:

* sottodominio “info.mybrand.com” per le comunicazioni transazionali (conferma degli acquisti, reimpostazione della password, ecc.),
* sottodominio “marketing.mybrand.com” per le e-mail di ricerca di potenziali clienti.

In questo modo potrai preservare la reputazione del tuo dominio e di altri sottodomini. Ad esempio, se i sottodomini “marketing.mybrand.com” venissero inseriti nell’elenco Bloccati dai provider di servizi Internet a causa di uno scarso recapito di messaggi, ciò impedirebbe l’inserimento nell’elenco Bloccati dell’intero dominio “mybrand.com” e del sottodominio “info.mybrand.com”.

## Mantenere gli URL delle risorse trasparenti per i clienti

Quando si implementa una soluzione, sono presenti requisiti per i componenti rivolti all’esterno: ad esempio la configurazione di collegamenti e pagine web da tracciare, la visualizzazione di pagine mirror, ecc.

Questi requisiti vengono gestiti tramite componenti ospitati sia da Adobe che dal cliente, ma includono URL che possono essere visualizzati dai destinatari delle e-mail. Per evitare di disporre di URL che indicano la soluzione tecnica sottostante o il provider di hosting, è possibile impostare sottodomini per renderlo trasparente ai destinatari delle e-mail. [Ulteriori informazioni sulla delega del dominio](https://helpx.adobe.com/it/campaign/kb/domain-name-delegation.html).

## Delega dei sottodomini in Journey Optimizer

Journey Optimizer offre diverse funzioni per la gestione dei sottodomini:

* [Delega i ](delegate-subdomain.md) sottodomini direttamente dall&#39;interfaccia,
* [Aggiungi ](google-txt.md) i record TXT di Google ai tuoi sottodomini per garantire la corretta consegna delle e-mail agli indirizzi Gmail,
* [Accedi ai ](ptr-records.md) record PTR generati per i tuoi sottodomini, per verificarli inviando server di posta elettronica.
