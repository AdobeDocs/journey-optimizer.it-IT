---
solution: Journey Optimizer
product: journey optimizer
title: Configurare i percorsi
description: Scopri come configurare origini dati, eventi e azioni
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
keywords: configurazione, percorso, dashboard, origini dati, eventi, azioni
exl-id: c144d44f-031f-4ca2-800e-d3878af400a5
TQID: https://experienceleague.adobe.com/e-4vo3PypkPPOl5pIKWJ1Ecmflj3-CTIAtEV8fjMdk4
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d556b755-390a-43f0-be32-a08cf6236126
subfeature_v2:
  - id: c2062154-398f-466d-bbc2-4e0d0c3f37a9
  - id: d08afb72-92f6-4856-88e3-11ec34313c2f
  - id: dd51b532-b93f-4bcf-8dbf-0d007f593aca
  - id: efb19423-4da4-4fd1-88d8-5ee8c71ae766
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 539
ht-degree: 64%

---

# Introduzione alla configurazione dei percorsi {#configure-journeys}

>[!CONTEXTUALHELP]
>id="ajo_journey_configuration_dashboard"
>title="Informazioni sulla configurazione dei percorsi"
>abstract="Per inviare messaggi con i percorsi, è necessario configurare origini dati, eventi e azioni. Le origini dati consentono di stabilire una connessione a un sistema per il recupero di informazioni aggiuntive che verranno utilizzate nei percorsi, ad esempio all’interno delle condizioni. Gli eventi consentono di attivare i percorsi quando viene ricevuto un evento. Le azioni personalizzate facilitano la connessione a un sistema di terze parti per l’invio dei messaggi. Se utilizzi le funzionalità di messaggistica incorporate di Journey Optimizer, non è necessario configurare un’azione."

Per inviare messaggi con percorsi, è necessario configurare **[!UICONTROL Origini dati]**, **[!UICONTROL Eventi]** e **[!UICONTROL Azioni]**. Le origini dati consentono di stabilire una connessione a un sistema per il recupero di informazioni aggiuntive che verranno utilizzate nei percorsi, ad esempio all’interno delle condizioni. Gli eventi consentono di attivare i percorsi quando viene ricevuto un evento. Le azioni personalizzate facilitano la connessione a un sistema di terze parti per l’invio dei messaggi. Se utilizzi le funzionalità di messaggistica incorporate di Journey Optimizer, non è necessario configurare un’azione.


![](assets/admin-menu.png)

Puoi anche configurare le connessioni a sistemi esterni tramite origini dati e azioni personalizzate. Ciò ti consente, ad esempio, di arricchire i tuoi percorsi con dati provenienti da un sistema di prenotazione esterno o di inviare messaggi utilizzando un sistema di terze parti come Epsilon o Facebook. Scopri come [integrare Journey Optimizer con sistemi esterni](external-systems.md).

## Origini dati {#data-sources}

La configurazione di Data Source consente di definire una connessione a un sistema per il recupero di informazioni aggiuntive, le quali verranno utilizzate nei percorsi. [Ulteriori informazioni](../../using/datasource/about-data-sources.md)

## Eventi {#events}

Gli eventi consentono di attivare i percorsi in modo unitario per inviare messaggi in tempo reale all’utente che entra nel percorso.

Nella configurazione dell’evento, puoi configurare gli eventi previsti nei percorsi. I dati degli eventi in arrivo vengono normalizzati seguendo Adobe Experience Data Model (XDM). Gli eventi provengono dalle API di acquisizione in streaming per gli eventi autenticati e non autenticati, ad esempio gli eventi SDK di Adobe Mobile. [Ulteriori informazioni](../../using/event/about-events.md)

## Azioni {#actions}

Le funzionalità per i messaggi di Journey Optimizer sono integrate: devi solo aggiungere un’attività di azione sul canale al percorso. Se utilizzi un sistema di terze parti per l’invio dei messaggi, puoi creare un’azione personalizzata. [Ulteriori informazioni](../../using/action/action.md)

## Sfogliare i campi di Adobe Experience Platform {#friendly-names-display}

Quando si definisce il [payload dell’evento](../event/about-creating.md#define-the-payload-fields) e il [payload del gruppo di campi](../datasource/configure-data-sources.md#define-field-groups) e si selezionano i campi nell’[editor delle espressioni](../building-journeys/expression/expressionadvanced.md), oltre al nome del campo viene mostrato anche il nome visualizzato. Queste informazioni vengono recuperate dalla definizione dello schema di Experience Data Model.

Se durante la configurazione degli schemi vengono forniti descrittori come &quot;xdm:alternateDisplayInfo&quot;, i nomi descrittivi sostituiranno i nomi visualizzati. È particolarmente utile quando si lavora con &quot;eVar&quot; e campi generici. Puoi configurare descrittori di nomi descrittivi tramite una chiamata API. Per ulteriori informazioni, consulta la [Guida per gli sviluppatori del registro dello schema](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html?lang=it){target="_blank"}.

![](assets/xdm-from-descriptors.png)

Se è disponibile un nome descrittivo, il campo verrà visualizzato come `<friendly-name>(<name>)`. Se non è disponibile alcun nome descrittivo, verrà mostrato il nome visualizzato, ad esempio `<display-name>(<name>)`. Se non è definito nessuno dei due, verrà visualizzato solo il nome tecnico del campo `<name>`.

>[!NOTE]
>
>I nomi descrittivi non vengono recuperati quando si selezionano i campi da un’unione di schemi.
