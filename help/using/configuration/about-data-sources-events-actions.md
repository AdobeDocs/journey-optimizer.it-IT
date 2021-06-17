---
title: Amministrazione e impostazioni
description: Informazioni sulle linee guida per l'amministrazione e le impostazioni
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
exl-id: 0964a484-f957-4aae-a571-61b2a1615026
feature: Impostazioni applicazione
topic: Amministrazione
role: Administrator
level: Intermediate
source-git-commit: 344bcff33895867d650f98b778cdf76c52a4b75e
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 60%

---

# Configura percorsi

Per inviare messaggi con percorsi, devi configurare **[!UICONTROL Data Sources]**, **[!UICONTROL Events]** e **[!UICONTROL Actions]**.

![](../assets/admin-menu.png)

## Origini dati 

La configurazione Origine dati ti consente di definire una connessione a un sistema per recuperare informazioni aggiuntive che verranno utilizzate nei tuoi percorsi. [Ulteriori informazioni](../../using/datasource/about-data-sources.md)

## Eventi

Gli eventi ti consentono di attivare i tuoi percorsi singolarmente per inviare messaggi, in tempo reale, al singolo che scorre nel percorso.

Nella configurazione dell’evento, puoi configurare gli eventi previsti nei percorsi. I dati degli eventi in arrivo vengono normalizzati seguendo Adobe Experience Data Model (XDM). Gli eventi provengono dalle API Streaming Ingestion per gli eventi autenticati e non autenticati, ad esempio gli eventi SDK di Adobe Mobile. [Ulteriori informazioni](../../using/event/about-events.md)

## Azioni

Le funzionalità dei messaggi Journey Optimizer sono integrate: devi solo progettare il contenuto e pubblicare il messaggio. Se utilizzi un sistema di terze parti per l’invio dei messaggi, puoi creare un’azione personalizzata. [Ulteriori informazioni](../../using/action/action.md)

## Sfogliare i campi di Adobe Experience Platform {#friendly-names-display}

Quando si definisce il [payload dell’evento](../event/about-creating.md#define-the-payload-fields) e il [payload del gruppo di campi](../datasource/configure-data-sources.md#define-field-groups) e si selezionano i campi nell’[editor delle espressioni](https://experienceleague.adobe.com/docs/journeys/using/building-advanced-conditions-journeys/expressionadvanced.html?lang=it), oltre al nome del campo viene mostrato anche il nome visualizzato. Queste informazioni vengono recuperate dalla definizione dello schema di Experience Data Model.

Se durante la configurazione degli schemi vengono forniti descrittori come &quot;xdm:alternateDisplayInfo&quot;, i nomi descrittivi sostituiranno i nomi visualizzati. È particolarmente utile quando si lavora con “eVar” e campi generici. Puoi configurare descrittori di nomi descrittivi tramite una chiamata API. Per ulteriori informazioni, consulta la [Guida per gli sviluppatori del registro dello schema](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html?lang=it).

![](../assets/xdm-from-descriptors.png)

Se è disponibile un nome descrittivo, il campo verrà visualizzato come `<friendly-name>(<name>)`. Se non è disponibile alcun nome descrittivo, verrà mostrato il nome visualizzato, ad esempio `<display-name>(<name>)`. Se non è definito nessuno dei due, verrà visualizzato solo il nome tecnico del campo `<name>`.

>[!NOTE]
>
>I nomi descrittivi non vengono recuperati quando si selezionano i campi da un’unione di schemi.