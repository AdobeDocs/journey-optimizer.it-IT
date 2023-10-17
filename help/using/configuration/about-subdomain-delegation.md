---
solution: Journey Optimizer
product: journey optimizer
title: Delega dei sottodomini in [!DNL Journey Optimizer]
description: Scopri come delegare i sottodomini
feature: Subdomains
topic: Administration
role: Admin
level: Experienced
keywords: sottodominio, ottimizzatore, delega
exl-id: 1b5ca4db-44d9-49e2-ab39-a1abba223ec7
source-git-commit: c4b8a74541a3fb9fea054bd1145592d75c62b165
workflow-type: tm+mt
source-wordcount: '900'
ht-degree: 26%

---

# Delega dei sottodomini in [!DNL Journey Optimizer] {#subdomain-delegation}

La creazione di un sottodominio per le campagne e-mail consente ai brand di isolare diversi tipi di traffico (ad esempio marketing e aziendale) in pool IP specifici e con domini specifici, velocizzando il processo di riscaldamento dell’IP e migliorando complessivamente il recapito messaggi. Se condividi un dominio e questo viene bloccato o aggiunto all’elenco Bloccati, ciò potrebbe influire sulla consegna della posta aziendale. Tuttavia, problemi o blocchi di reputazione su un dominio specifico per le comunicazioni di e-mail marketing avranno un impatto solo su tale flusso di e-mail. L’utilizzo del dominio principale come mittente o indirizzo &quot;Da&quot; per più flussi di posta potrebbe inoltre interrompere l’autenticazione e-mail, causando il blocco o l’inserimento dei messaggi nella cartella di posta indesiderata.

>[!NOTE]
>
>Impossibile utilizzare lo stesso dominio di invio per inviare messaggi da [!DNL Adobe Journey Optimizer] e da un altro prodotto, ad esempio [!DNL Adobe Campaign] o [!DNL Adobe Marketo Engage].

## Perché impostare i sottodomini? {#why-set-up-subdomains}

Un sottodominio è una divisione del dominio che può essere utilizzata per isolare i brand o vari tipi di traffico, ad esempio messaggi transazionali e comunicazioni di marketing.

Prendiamo ad esempio il dominio “mybrand.com”, che viene utilizzato per inviare comunicazioni transazionali e di marketing. In questa situazione, puoi decidere di impostare due sottodomini:

* sottodominio “info.mybrand.com” per le comunicazioni transazionali (conferma degli acquisti, reimpostazione della password, ecc.),
* sottodominio “marketing.mybrand.com” per le e-mail di ricerca di potenziali clienti.

In questo modo potrai preservare la reputazione del tuo dominio e di altri sottodomini. Ad esempio, se i sottodomini “marketing.mybrand.com” venissero inseriti nell’elenco Bloccati dai provider di servizi Internet a causa di uno scarso recapito di messaggi, ciò impedirebbe l’inserimento nell’elenco Bloccati dell’intero dominio “mybrand.com” e del sottodominio “info.mybrand.com”.

Quando si implementa una soluzione, vi sono requisiti per i componenti rivolti verso l’esterno: ad esempio, è necessario configurare collegamenti e pagine web da tracciare, visualizzare pagine mirror e così via.

Questi requisiti vengono gestiti tramite componenti in hosting sia dall’Adobe che dal cliente, ma includono URL che possono essere visualizzati dai destinatari delle e-mail. Per evitare di avere URL che indicano la soluzione tecnica o il provider di hosting sottostante, è possibile configurare i sottodomini per rendere trasparente l’operazione ai destinatari delle e-mail.

**Ulteriori informazioni**

* Scopri come [delegare i sottodomini](delegate-subdomain.md) direttamente dall’interfaccia
* Scopri come [aggiungere record TXT di Google](google-txt.md) ai sottodomini per garantire la corretta consegna delle e-mail agli indirizzi Gmail
* Scopri come [accedere ai record PTR](ptr-records.md) generati per i sottodomini, che possono essere verificati inviando server di posta

## Metodi di configurazione dei sottodomini {#subdomain-delegation-methods}

La configurazione del sottodominio ti consente di configurare una sottosezione del dominio (tecnicamente una &quot;zona DNS&quot;) per l’utilizzo con Adobe Campaign. I metodi di configurazione disponibili sono:

* **Delega completa del sottodominio ad Adobe** (consigliato): il sottodominio viene delegato completamente ad Adobe. Adobe è in grado di controllare e gestire tutti gli aspetti del DNS necessari per la consegna, il rendering e il tracciamento dei messaggi. [Ulteriori informazioni sulla delega completa dei sottodomini](delegate-subdomain.md#full-subdomain-delegation)

* **Utilizzo dei CNAME**: crea un sottodominio e utilizza i CNAME per puntare a record specifici dell’Adobe. Utilizzando questa configurazione, tu e Adobe condividete la responsabilità di mantenere il DNS. [Ulteriori informazioni sulla delega del sottodominio CNAME](delegate-subdomain.md#cname-subdomain-delegation)

>[!CAUTION]
>
>* La delega completa del sottodominio è il metodo preferito.
>
>* Il metodo CNAME è consigliato se i criteri dell’organizzazione limitano il metodo di delega del sottodominio completo. Questo approccio richiede di gestire e mantenere i record DNS autonomamente. Adobe non sarà in grado di fornire assistenza per la modifica, la manutenzione o la gestione del DNS per un sottodominio configurato tramite il metodo CNAME.

La tabella seguente fornisce un riepilogo del funzionamento di questi metodi, oltre al livello di impegno che comportano:

| Metodo di configurazione | Come funziona | Livello di impegno |
|---|---|---|
| **Delega completa** | Crea il record del sottodominio e dello spazio dei nomi. Adobe configurerà quindi tutti i record DNS necessari per Adobe Campaign.<br/><br/>In questa configurazione, Adobe si assume la piena responsabilità della gestione del sottodominio e di tutti i record DNS. | Bassa |
| **CNAME, metodo personalizzato** | Crea il record del sottodominio e dello spazio dei nomi. Adobe fornirà quindi i record da inserire nei server DNS e configurerà i valori corrispondenti nei server DNS di Adobe Campaign.<br/><br/>In questa configurazione, tu e Adobe condividete la responsabilità di mantenere il DNS. | Alta |

Ulteriori informazioni sulla configurazione del dominio sono disponibili in [questa documentazione](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/product-specific-resources/campaign/ac-domain-name-setup.html).

Se hai domande sui metodi di configurazione dei sottodomini, contatta un Adobe o contatta l’Assistenza clienti per richiedere consulenza sul recapito dei messaggi.

## Accedere ai sottodomini delegati {#access-delegated-subdomains}

Tutti i sottodomini delegati vengono visualizzati nel **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]** > **[!UICONTROL Sottodomini]** menu. Sono disponibili dei filtri per aiutarti a perfezionare l’elenco (data di delega, utente o stato).

![](assets/subdomain-list.png)

Il **[!UICONTROL Stato]** fornisce informazioni sul processo di delega del sottodominio:

* **[!UICONTROL Bozza]**: la delega del sottodominio è stata salvata come bozza. Fai clic sul nome del sottodominio per riprendere il processo di delega,
* **[!UICONTROL Elaborazione]**: il sottodominio sta attraversando diversi controlli di configurazione prima di poter essere utilizzato,
* **[!UICONTROL Completato]**: il sottodominio ha superato correttamente i controlli e può essere utilizzato per inviare messaggi,
* **[!UICONTROL Non riuscito]**: uno o più controlli non sono riusciti dopo l’invio della delega del sottodominio.

Per accedere a informazioni dettagliate su un sottodominio con **[!UICONTROL Completato]** stato, aprilo dall’elenco.

![](assets/subdomain-delegated.png)

Puoi eseguire le seguenti operazioni:

* Recupera il nome del sottodominio (sola lettura) configurato durante il processo di delega, nonché gli URL generati (risorse, pagine mirror, URL di tracciamento).

* Aggiungi un record TXT di Google per la verifica del sito al tuo sottodominio per assicurarti che sia verificato (vedi [Aggiungere un record TXT di Google a un sottodominio](google-txt.md)).


>[!CAUTION]
>
>La configurazione del sottodominio è comune a tutti gli ambienti. Pertanto, qualsiasi modifica a un sottodominio influirà anche sulle sandbox di produzione.
