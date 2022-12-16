---
solution: Journey Optimizer
product: journey optimizer
title: Delega dei sottodomini in [!DNL Journey Optimizer]
description: Scopri come delegare i sottodomini
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 1b5ca4db-44d9-49e2-ab39-a1abba223ec7
source-git-commit: c6498633fdfdc9442203a3bf980f1b12bd1c6a6b
workflow-type: tm+mt
source-wordcount: '897'
ht-degree: 26%

---

# Delega dei sottodomini in [!DNL Journey Optimizer] {#subdomain-delegation}

La creazione di un sottodominio per le campagne e-mail consente ai brand di isolare diversi tipi di traffico (marketing e aziende, ad esempio) in pool IP specifici e con domini specifici, velocizzando il processo di riscaldamento dell’IP e migliorando il recapito messaggi in generale. Se condividi un dominio e questo viene bloccato o aggiunto all&#39;elenco Bloccati, potrebbe influire sulla consegna della posta aziendale. Tuttavia, problemi o blocchi di reputazione su un dominio specifico per le tue comunicazioni di marketing e-mail avranno un impatto solo su quel flusso di e-mail. L’utilizzo del dominio principale come mittente o indirizzo &quot;Da&quot; per più flussi di posta potrebbe anche interrompere l’autenticazione delle e-mail, bloccando o inserendo i messaggi nella cartella spam.

>[!NOTE]
>
>Non è possibile utilizzare lo stesso dominio di invio per inviare messaggi da [!DNL Adobe Journey Optimizer] e da un altro prodotto, quali [!DNL Adobe Campaign] o [!DNL Adobe Marketo Engage].

## Perché impostare i sottodomini? {#why-setting-up-subdomains}

Un sottodominio è una divisione del dominio che può essere utilizzata per isolare i brand o vari tipi di traffico, ad esempio messaggi transazionali e comunicazioni di marketing.

Prendiamo ad esempio il dominio “mybrand.com”, che viene utilizzato per inviare comunicazioni transazionali e di marketing. In questa situazione, puoi decidere di impostare due sottodomini:

* sottodominio “info.mybrand.com” per le comunicazioni transazionali (conferma degli acquisti, reimpostazione della password, ecc.),
* sottodominio “marketing.mybrand.com” per le e-mail di ricerca di potenziali clienti.

In questo modo potrai preservare la reputazione del tuo dominio e di altri sottodomini. Ad esempio, se i sottodomini “marketing.mybrand.com” venissero inseriti nell’elenco Bloccati dai provider di servizi Internet a causa di uno scarso recapito di messaggi, ciò impedirebbe l’inserimento nell’elenco Bloccati dell’intero dominio “mybrand.com” e del sottodominio “info.mybrand.com”.

Quando si implementa una soluzione, sono presenti requisiti per i componenti rivolti all’esterno: ad esempio la configurazione di collegamenti e pagine web da tracciare, la visualizzazione di pagine mirror, ecc.

Questi requisiti vengono gestiti tramite componenti ospitati sia da Adobe che dal cliente, ma includono URL che possono essere visualizzati dai destinatari delle e-mail. Per evitare di disporre di URL che indicano la soluzione tecnica sottostante o il provider di hosting, è possibile impostare sottodomini per renderlo trasparente ai destinatari delle e-mail.

**Ulteriori informazioni**

* Scopri come [delegare i sottodomini](delegate-subdomain.md) direttamente dall&#39;interfaccia
* Scopri come [aggiungere record TXT di Google](google-txt.md) ai sottodomini per garantire la corretta consegna delle e-mail agli indirizzi Gmail
* Scopri come [accedere ai record PTR](ptr-records.md) generato per i sottodomini, per verificarli inviando server di posta elettronica

## Metodi di configurazione dei sottodomini {#subdomain-delegation-methods}

La configurazione dei sottodomini ti consente di configurare una sottosezione del dominio (tecnicamente una &quot;zona DNS&quot;) da utilizzare con Adobe Campaign. I metodi di configurazione disponibili sono:

* **Delega completa del sottodominio ad Adobe** (consigliato): il sottodominio viene delegato completamente ad Adobe. Adobe è in grado di controllare e mantenere tutti gli aspetti del DNS necessari per la consegna, il rendering e il tracciamento dei messaggi. [Ulteriori informazioni sulla delega completa dei sottodomini](delegate-subdomain.md#full-subdomain-delegation)

* **Utilizzo dei CNAME**: Crea un sottodominio e utilizza i CNAME per puntare a record specifici per l’Adobe. Utilizzando questa configurazione, tu e Adobe condividete la responsabilità di mantenere il DNS. [Ulteriori informazioni sulla delega dei sottodomini CNAME](delegate-subdomain.md#cname-subdomain-delegation)

>[!CAUTION]
>
>* La delega completa del sottodominio è il metodo preferito.
>
>* Il metodo CNAME è consigliato se i criteri aziendali limitano il metodo di delega del sottodominio completo. Questo approccio richiede la gestione e la gestione autonoma dei record DNS. Adobe non sarà in grado di fornire assistenza per modificare, mantenere o gestire il DNS per un sottodominio configurato tramite il metodo CNAME.


La tabella seguente fornisce un riepilogo del funzionamento di questi metodi, oltre al livello di impegno che comportano:

| Metodo di configurazione | Come funziona | Livello di impegno |
|---|---|---|
| **Delega completa** | Crea il record del sottodominio e dello spazio dei nomi. Adobe configurerà quindi tutti i record DNS necessari per Adobe Campaign.<br/><br/>In questa configurazione, Adobe si assume la piena responsabilità della gestione del sottodominio e di tutti i record DNS. | Bassa |
| **CNAME, metodo personalizzato** | Crea il record del sottodominio e dello spazio dei nomi. Adobe fornirà quindi i record da inserire nei server DNS e configurerà i valori corrispondenti nei server DNS di Adobe Campaign.<br/><br/>In questa configurazione, tu e Adobe condividete la responsabilità di mantenere il DNS. | Alta |

Ulteriori informazioni sulla configurazione del dominio sono disponibili in [questa documentazione](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/product-specific-resources/campaign/ac-domain-name-setup.html).

Se hai domande sui metodi di configurazione dei sottodomini, contatta l’Adobe o contatta l’Assistenza clienti per richiedere consulenza sul recapito messaggi.

## Accedere ai sottodomini delegati {#access-delegated-subdomains}

Tutti i sottodomini delegati vengono visualizzati nella sezione **[!UICONTROL Amministrazione]** > **[!UICONTROL Canali]** > **[!UICONTROL Sottodomini]** menu. Sono disponibili filtri per facilitare la definizione dell’elenco (data di delega, utente o stato).

![](assets/subdomain-list.png)

La **[!UICONTROL Stato]** La colonna fornisce informazioni sul processo di delega del sottodominio:

* **[!UICONTROL Bozza]**: La delega del sottodominio è stata salvata come bozza. Fai clic sul nome del sottodominio per riprendere il processo di delega,
* **[!UICONTROL Elaborazione]**: Il sottodominio sta effettuando diversi controlli di configurazione prima di poter essere utilizzato,
* **[!UICONTROL Completato]**: Il sottodominio ha superato i controlli con successo e può essere utilizzato per inviare messaggi,
* **[!UICONTROL Non riuscito]**: Uno o più controlli non sono riusciti dopo l’invio della delega del sottodominio.

Per accedere a informazioni dettagliate su un sottodominio con **[!UICONTROL Completato]** , aprilo dall&#39;elenco.

![](assets/subdomain-delegated.png)

Puoi eseguire le seguenti operazioni:

* Recupera il nome del sottodominio (sola lettura) configurato durante il processo di delega, nonché gli URL generati (risorse, pagine mirror, URL di tracciamento),

* Aggiungi un record TXT di Google per la verifica del sito al tuo sottodominio per assicurarti che sia verificato (vedi [Aggiungere un record TXT di Google a un sottodominio](google-txt.md)).


>[!CAUTION]
>
>La configurazione del sottodominio è comune a tutti gli ambienti. Pertanto, qualsiasi modifica apportata a un sottodominio influirà anche sulle sandbox di produzione.
