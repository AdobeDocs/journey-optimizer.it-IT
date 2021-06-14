---
title: Impostazioni tecniche
description: Informazioni sulle linee guida per l'amministrazione e le impostazioni
hidefromtoc: true
hide: true
feature: Impostazioni applicazione
topic: Amministrazione
role: Administrator
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 8%

---

# Impostazioni tecniche

![](../assets/do-not-localize/badge.png)

## Imposta i parametri di branding{#cjm-branding}

Ogni azienda dispone di linee guida visive e tecniche per il brand. Puoi definire un set di specifiche per presentare ai clienti un brand coerente, dai loghi agli aspetti tecnici, come il mittente dell’e-mail, il dominio dell’URL delle pagine mirror o le impostazioni di tracciamento dei messaggi.
I marchi non possono essere creati o modificati dagli utenti finali: questa configurazione è gestita da Adobe.

Per impostare i parametri di branding per l&#39;istanza [!DNL Journey Optimizer], è necessario contattare Adobe e condividere i seguenti dettagli:

* Nome dell&#39;azienda

* Indirizzo e-mail mittente (da)

* Nome mittente (da)

* Indirizzo di risposta

Una volta configurati i parametri di branding, potrai selezionarli al momento della creazione dei messaggi.

Una volta configurati i parametri di branding, potrai selezionarli al momento della creazione dei messaggi dall’ elenco **[!UICONTROL Presets]** . [Ulteriori informazioni sulla creazione](../create-message.md) di contenuti.

## Configurare il canale di notifica push

Scopri come configurare il canale push in questa [sezione](../create-push.md).

## Delega dei sottodomini

Per utilizzare un nuovo sottodominio in [!DNL Journey Optimizer], il primo passaggio consiste nel delegarlo. Devi contattare il tuo contatto tecnico Adobe.

Quando si implementa una soluzione, sono presenti requisiti per i componenti rivolti all’esterno: ad esempio la configurazione di collegamenti e pagine web da tracciare, la visualizzazione di pagine mirror, ecc.

Questi requisiti vengono gestiti tramite componenti ospitati sia da Adobe che dal cliente, ma includono URL che possono essere visualizzati dai destinatari delle e-mail.  Per evitare di disporre di URL che indicano la soluzione tecnica sottostante o il provider di hosting, è possibile impostare sottodomini per renderlo trasparente ai destinatari delle e-mail.

A seguito di queste delegazioni, l’infrastruttura istituita dall’Adobe garantisce che i seguenti servizi siano eseguiti per ciascun dominio di invio delegato o con alias CNAME:

* Creazione di caselle in entrata postmaster@ e abusive@

* Impostazione dei loop di feedback per il dominio delegato

* Configurazione del record DMARC di base

I parametri stabiliti dall&#39;Adobe sono validi solo dal momento in cui la delega è stata completata e poi verificata per Adobe e rimangono funzionanti.

[Ulteriori informazioni sulla delega del dominio](https://helpx.adobe.com/it/campaign/kb/domain-name-delegation.html).


## Creare origini dati, eventi e azioni

Utilizza la sezione **[!UICONTROL Admin]** per gestire **[!UICONTROL Data Sources]**, **[!UICONTROL Events]** e **[!UICONTROL Actions]**.

![](../assets/admin-menu.png)

### Origini dati 

La configurazione Origine dati ti consente di definire una connessione a un sistema per recuperare informazioni aggiuntive che verranno utilizzate nei tuoi percorsi.

Ulteriori informazioni sulle origini dati in questa sezione [sezione](../datasource/about-data-sources.md)

### Eventi

Gli eventi ti consentono di attivare i tuoi percorsi singolarmente per inviare messaggi, in tempo reale, al singolo che scorre nel percorso.

Nella configurazione dell’evento, puoi configurare gli eventi previsti nei percorsi. I dati degli eventi in arrivo vengono normalizzati seguendo Adobe Experience Data Model (XDM). Gli eventi provengono dalle API Streaming Ingestion per gli eventi autenticati e non autenticati, ad esempio gli eventi SDK di Adobe Mobile.

Ulteriori informazioni sugli eventi in questa sezione [sezione](../event/about-events.md)

### Azioni

[!DNL Journey Optimizer] funzionalità dei messaggi integrate: devi solo progettare il contenuto e pubblicare il messaggio. Se utilizzi un sistema di terze parti per l’invio dei messaggi, puoi creare un’azione personalizzata.

Ulteriori informazioni sulle azioni in questa sezione [sezione](../action/action.md)
