---
title: Delega sottodomini
description: Scopri come delegare i sottodomini
internal: n
snippet: y
source-git-commit: e569e992530df5429ffb96f78ba28b53de0ded81
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 26%

---


# Delega dei sottodomini in [!DNL Journey Optimizer]

La creazione di un sottodominio per le campagne e-mail consente ai brand di isolare diversi tipi di traffico (marketing e aziende, ad esempio) in pool IP specifici e con domini specifici, velocizzando il processo di riscaldamento dell’IP e migliorando il recapito messaggi in generale. Se condividi un dominio e questo viene bloccato o aggiunto all&#39;elenco Bloccati, potrebbe influire sulla consegna della posta aziendale. Tuttavia, problemi o blocchi di reputazione su un dominio specifico per le tue comunicazioni di marketing e-mail avranno un impatto solo su quel flusso di e-mail. L’utilizzo del dominio principale come mittente o indirizzo &quot;Da&quot; per più flussi di posta potrebbe anche interrompere l’autenticazione delle e-mail, bloccando o inserendo i messaggi nella cartella spam.

Un sottodominio è una divisione del dominio che può essere utilizzata per isolare i brand o vari tipi di traffico, ad esempio messaggi transazionali e comunicazioni di marketing.

Prendiamo ad esempio il dominio “mybrand.com”, che viene utilizzato per inviare comunicazioni transazionali e di marketing. In questa situazione, puoi decidere di impostare due sottodomini:

* sottodominio “info.mybrand.com” per le comunicazioni transazionali (conferma degli acquisti, reimpostazione della password, ecc.),
* sottodominio “marketing.mybrand.com” per le e-mail di ricerca di potenziali clienti.

In questo modo potrai preservare la reputazione del tuo dominio e di altri sottodomini. Ad esempio, se i sottodomini “marketing.mybrand.com” venissero inseriti nell’elenco Bloccati dai provider di servizi Internet a causa di uno scarso recapito di messaggi, ciò impedirebbe l’inserimento nell’elenco Bloccati dell’intero dominio “mybrand.com” e del sottodominio “info.mybrand.com”.

Quando si implementa una soluzione, sono presenti requisiti per i componenti rivolti all’esterno: ad esempio la configurazione di collegamenti e pagine web da tracciare, la visualizzazione di pagine mirror, ecc.

Questi requisiti vengono gestiti tramite componenti ospitati sia da Adobe che dal cliente, ma includono URL che possono essere visualizzati dai destinatari delle e-mail. Per evitare di disporre di URL che indicano la soluzione tecnica sottostante o il provider di hosting, è possibile impostare sottodomini per renderlo trasparente ai destinatari delle e-mail.

**Ulteriori informazioni**

* Scopri come [delegare i tuoi sottodomini](delegate-subdomain.md) direttamente dall’interfaccia
* Scopri come [aggiungere record TXT di Google](google-txt.md) ai tuoi sottodomini per garantire la corretta consegna delle e-mail agli indirizzi Gmail
* Scopri come [accedere ai record PTR](ptr-records.md) generati per i tuoi sottodomini, per verificarli inviando server di posta elettronica
