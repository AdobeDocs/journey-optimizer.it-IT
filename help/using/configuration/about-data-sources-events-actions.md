---
solution: Journey Optimizer
product: journey optimizer
title: Configurare i percorsi
description: Scopri come configurare origini dati, eventi e azioni
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: c144d44f-031f-4ca2-800e-d3878af400a5
source-git-commit: f04454860ebe597d3306e62b58de5f32e08342ee
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 0%

---

# Configurare i percorsi {#configure-journeys}

>[!CONTEXTUALHELP]
>id="ajo_journey_configuration_dashboard"
>title="Informazioni sulla configurazione del percorso"
>abstract="Per inviare messaggi con i percorsi, devi configurare Origini dati, Eventi e Azioni. Le origini dati ti consentono di definire una connessione a un sistema per recuperare informazioni aggiuntive che verranno utilizzate nei tuoi percorsi, ad esempio nelle tue condizioni. Gli eventi ti consentono di attivare i percorsi quando viene ricevuto un evento. Le azioni personalizzate consentono di connettersi a un sistema di terze parti per l’invio dei messaggi. Se utilizzi le funzionalità dei messaggi incorporati di Journey Optimizer non è necessario configurare un&#39;azione."

Per inviare messaggi con i percorsi, devi configurare **[!UICONTROL Data Sources]**, **[!UICONTROL Events]** e **[!UICONTROL Actions]**.

![](assets/admin-menu.png)

## Origini dati {#data-sources}

La configurazione Origine dati ti consente di definire una connessione a un sistema per il recupero di informazioni aggiuntive che verranno utilizzate nei tuoi percorsi. [Ulteriori informazioni](../../using/datasource/about-data-sources.md)

## Eventi {#events}

Gli eventi ti consentono di attivare i tuoi percorsi singolarmente per inviare messaggi in tempo reale al singolo utente che accede al percorso.

Nella configurazione dell’evento, puoi configurare gli eventi previsti nei percorsi. I dati degli eventi in arrivo vengono normalizzati seguendo Adobe Experience Data Model (XDM). Gli eventi provengono dalle API Streaming Ingestion per gli eventi autenticati e non autenticati, ad esempio gli eventi SDK di Adobe Mobile. [Ulteriori informazioni](../../using/event/about-events.md)

## Azioni {#actions}

Le funzionalità dei messaggi di Journey Optimizer sono integrate: devi solo aggiungere un’attività azione canale al tuo percorso. Se utilizzi un sistema di terze parti per l’invio dei messaggi, puoi creare un’azione personalizzata. [Ulteriori informazioni](../../using/action/action.md)

## Sfoglia i campi di Adobe Experience Platform {#friendly-names-display}

Quando definisci [payload dell’evento](../event/about-creating.md#define-the-payload-fields), [payload del gruppo di campi](../datasource/configure-data-sources.md#define-field-groups) e selezionando i campi nella [editor di espressioni](../building-journeys/expression/expressionadvanced.md), oltre al nome del campo viene visualizzato anche il nome visualizzato. Queste informazioni vengono recuperate dalla definizione dello schema in Experience Data Model.

Se durante la configurazione degli schemi vengono forniti descrittori come &quot;xdm:alternateDisplayInfo&quot;, i nomi descrittivi sostituiranno i nomi visualizzati. È particolarmente utile quando si lavora con &quot;eVar&quot; e campi generici. Puoi configurare descrittori di nomi descrittivi tramite una chiamata API. Per ulteriori informazioni, consulta la sezione [Guida per gli sviluppatori del Registro di sistema dello schema](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html){target=&quot;_blank&quot;}.

![](assets/xdm-from-descriptors.png)

Se è disponibile un nome descrittivo, il campo verrà visualizzato come `<friendly-name>(<name>)`. Se non è disponibile alcun nome descrittivo, verrà visualizzato il nome visualizzato, ad esempio `<display-name>(<name>)`. Se non è definito nessuno dei due, verrà visualizzato solo il nome tecnico del campo `<name>`.

>[!NOTE]
>
>I nomi descrittivi non vengono recuperati quando si selezionano i campi da un’unione di schemi.
