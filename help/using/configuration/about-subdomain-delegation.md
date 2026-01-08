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
source-git-commit: ab29af6861e8fc1137fbbffd99b9576afa7e04f5
workflow-type: tm+mt
source-wordcount: '984'
ht-degree: 25%

---

# Delega dei sottodomini in [!DNL Journey Optimizer] {#subdomain-delegation}

>[!CONTEXTUALHELP]
>id="ajo_admin_delegated_subdomains"
>title="I sottodomini delegati vengono visualizzati qui."
>abstract="Delegare il primo sottodominio. Al termine della delega, vengono creati record PTR e abilitati i canali e-mail."

La creazione di un sottodominio per i percorsi e le campagne e-mail consente ai brand di isolare diversi tipi di traffico (ad esempio marketing e aziendale) in pool IP specifici e con domini specifici, velocizzando il processo di riscaldamento dell’IP e migliorando complessivamente il recapito messaggi.

Se condividi un dominio e questo viene bloccato o aggiunto all’elenco Bloccati, ciò potrebbe influire sulla consegna della posta aziendale. Tuttavia, problemi o blocchi di reputazione su un dominio specifico per le comunicazioni di e-mail marketing avranno un impatto solo su tale flusso di e-mail. L’utilizzo del dominio principale come mittente o indirizzo &quot;Da&quot; per più flussi di posta potrebbe inoltre interrompere l’autenticazione e-mail, causando il blocco o l’inserimento dei messaggi nella cartella di posta indesiderata.

>[!CAUTION]
>
>Impossibile utilizzare lo stesso dominio di invio per inviare messaggi da [!DNL Adobe Journey Optimizer] e da un altro prodotto, ad esempio [!DNL Adobe Campaign] o [!DNL Adobe Marketo Engage].

## Perché impostare i sottodomini? {#why-set-up-subdomains}

Un sottodominio è una divisione del dominio che può essere utilizzata per isolare i brand o vari tipi di traffico, ad esempio messaggi transazionali e comunicazioni di marketing.

Prendiamo ad esempio il dominio “mybrand.com”, che viene utilizzato per inviare comunicazioni transazionali e di marketing. In questa situazione, puoi decidere di impostare due sottodomini:

* sottodominio “info.mybrand.com” per le comunicazioni transazionali (conferma degli acquisti, reimpostazione della password, ecc.),
* sottodominio “marketing.mybrand.com” per le e-mail di ricerca di potenziali clienti.

In questo modo potrai preservare la reputazione del tuo dominio e di altri sottodomini. Ad esempio, se i sottodomini “marketing.mybrand.com” venissero inseriti nell’elenco Bloccati dai provider di servizi Internet a causa di uno scarso recapito di messaggi, ciò impedirebbe l’inserimento nell’elenco Bloccati dell’intero dominio “mybrand.com” e del sottodominio “info.mybrand.com”.

Quando si implementa una soluzione, vi sono requisiti per i componenti rivolti verso l’esterno: ad esempio, è necessario configurare collegamenti e pagine web da tracciare, visualizzare pagine mirror e così via.

Questi requisiti vengono gestiti tramite componenti in hosting sia da Adobe che dal cliente, ma includono anche URL che possono essere visualizzati dai destinatari delle e-mail. Per evitare di avere URL che indicano la soluzione tecnica o il provider di hosting sottostante, è possibile configurare i sottodomini per rendere trasparente l’operazione ai destinatari delle e-mail.

**Ulteriori informazioni**

* Scopri come [delegare i sottodomini](delegate-subdomain.md) direttamente dall&#39;interfaccia
* Scopri come [aggiungere record TXT di Google](google-txt.md) ai tuoi sottodomini per garantire la corretta consegna delle e-mail agli indirizzi Gmail
* Scopri come [accedere ai record PTR](ptr-records.md) generati per i tuoi sottodomini, per verificarli inviando server di posta

## Metodi di configurazione dei sottodomini {#subdomain-delegation-methods}

La configurazione del sottodominio consente di configurare una sottosezione del dominio (tecnicamente una &quot;zona DNS&quot;) per l’utilizzo con Adobe Journey Optimizer.

I metodi di configurazione disponibili sono i seguenti.

### Delegare completamente un sottodominio ad Adobe (scelta consigliata) {#full-subdomain-delegation}

[!DNL Journey Optimizer] consente di delegare completamente i sottodomini ad Adobe direttamente dall&#39;interfaccia del prodotto. In questo modo, Adobe sarà in grado di fornire messaggi come servizio gestito controllando e mantenendo tutti gli aspetti del DNS necessari per la distribuzione, il rendering e il tracciamento.

<!--The subdomain is fully delegated to Adobe. Adobe is able to control and maintain all aspects of DNS that are required for delivering, rendering and tracking messages.-->

Puoi affidarti ad Adobe per mantenere l’infrastruttura DNS necessaria per soddisfare i requisiti di recapito messaggi standard di settore per i domini di invio del marketing e-mail, continuando al contempo a mantenere e controllare il DNS per i domini e-mail interni.

>[!IMPORTANT]
>
>La delega completa del sottodominio è il metodo preferito.

Scopri come delegare completamente un sottodominio ad Adobe in [questa sezione](delegate-subdomain.md#set-up-subdomain).

### Configurare un sottodominio con CNAME {#cname-subdomain-setup}

Se si dispone di criteri di restrizione specifici per il dominio e si desidera che Adobe abbia solo un controllo parziale sul DNS, è possibile scegliere di eseguire tutte le attività correlate al DNS dal proprio lato.

La configurazione del sottodominio CNAME consente di creare un sottodominio e utilizzare i CNAME per puntare a record specifici di Adobe. Utilizzando questa configurazione, tu e Adobe condividete la responsabilità di mantenere il DNS per configurare l’ambiente per l’invio, il rendering e il tracciamento delle e-mail.

>[!CAUTION]
>
>Il metodo CNAME è consigliato se i criteri dell’organizzazione limitano il metodo di delega del sottodominio completo. Questo approccio richiede di gestire e mantenere i record DNS autonomamente.
>
>Adobe non sarà in grado di fornire assistenza per la modifica, la manutenzione o la gestione del DNS per un sottodominio configurato tramite il metodo CNAME.

Scopri come creare un sottodominio utilizzando i CNAME per puntare a record specifici di Adobe in [questa sezione](delegate-subdomain.md#cname-subdomain-setup).

### Utilizzare un sottodominio personalizzato {#custom-subdomain-delegation}

Il metodo di delega personalizzata consente di gestire e controllare tutti gli aspetti del DNS necessari per la consegna, il rendering e il tracciamento dei messaggi.

In questo caso, possiedi e gestisci completamente i nostri sottodomini e hai il pieno controllo sui certificati generati come parte di questo processo.

Scopri come impostare un dominio personalizzato in [questa sezione](delegate-custom-subdomain.md).

## Confronto dei metodi di configurazione

La tabella seguente fornisce un riepilogo del funzionamento di questi metodi, oltre al livello di impegno che comportano:
<!--
| Configuration method | How it works | Level of effort |
|---|---|---|
| **Full delegation** | Create the subdomain and namespace record. Adobe will then configure all DNS records required for Adobe Journey Optimizer.<br/><br/>In this setup, Adobe is fully responsible for managing the subdomain and all the DNS records. | Low |
| **CNAME method** |  Create the subdomain and namespace record. Adobe will then provide the records to be placed in your DNS servers and will configure the corresponding values in Adobe Journey Optimizer DNS servers.<br/><br/>In this setup, both you and Adobe share responsibility for maintaining DNS. | High |-->


| Metodo di configurazione | Come funziona | Livello di impegno |
|---|---|---|
| **Delega completa** | Crea il record del sottodominio e dello spazio dei nomi. Adobe configurerà quindi tutti i record DNS necessari per Adobe Journey Optimizer.<br/><br/>In questa configurazione, Adobe si assume la piena responsabilità della gestione del sottodominio e di tutti i record DNS. | Basso |
| **metodo CNAME** | Crea il record del sottodominio e dello spazio dei nomi. Adobe fornirà quindi i record da inserire nei server DNS e configurerà i valori corrispondenti nei server DNS Adobe Journey Optimizer.<br/><br/>In questa configurazione, tu e Adobe condividete la responsabilità di mantenere il DNS. | Alto |
| **Metodo di delega personalizzato** | Creazione del record del sottodominio e dello spazio dei nomi: Adobe fornirà quindi i record da inserire nei server DNS. Carica il certificato SSL ottenuto dall’autorità di certificazione e completa i passaggi del ciclo di feedback verificando la proprietà del dominio e l’indirizzo e-mail di reporting.<br/><br/>In questa configurazione, hai la piena responsabilità di mantenere il DNS. | Molto alto |

Per ulteriori informazioni sulla configurazione del dominio, consulta [questa documentazione](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/product-specific-resources/campaign/ac-domain-name-setup.html?lang=it){target="_blank"}.

Per qualsiasi domanda sui metodi di configurazione dei sottodomini, contatta Adobe o l’Assistenza clienti per richiedere consulenza sul recapito messaggi.


