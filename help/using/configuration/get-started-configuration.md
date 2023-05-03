---
solution: Journey Optimizer
product: journey optimizer
title: Introduzione alla configurazione  [!DNL Journey Optimizer]
description: Ulteriori informazioni sulla configurazione  [!DNL Journey Optimizer]
role: Admin, Developer
level: Intermediate
exl-id: 0964a484-f957-4aae-a571-61b2a1615026
feature: Application Settings
topic: Administration
keywords: configurazione, configurare, messaggi, canale, sandbox, optimizer
source-git-commit: b8065a68ed73102cb2c9da2c2d2675ce8e5fbaad
workflow-type: ht
source-wordcount: '387'
ht-degree: 100%

---


# Introduzione alla configurazione [!DNL Journey Optimizer] {#start-optimizer-configuration}

Quando accedi a [!DNL Journey Optimizer] per la prima volta, viene effettuato il provisioning di una sandbox di produzione e viene allocato un determinato numero di IP a seconda del contratto.

Per creare i tuoi percorsi e inviare messaggi, devi seguire i passaggi di configurazione riportati di seguito.

## Configurare messaggi e canali

1. Per poter creare e inviare messaggi, devi eseguire configurazioni specifiche a seconda del canale.

   * Per il canale **e-mail**, devi delegare i sottodomini ad Adobe e creare pool IP per raggruppare gli indirizzi IP. [Ulteriori informazioni](../email/get-started-email-config.md)

   * Per il canale **Push**, devi definire le impostazioni delle notifiche push in [!DNL Adobe Experience Platform] e [!DNL Adobe Experience Platform Launch]. [Ulteriori informazioni](../push/push-configuration.md)

   * Per il canale **SMS**, devi configurare l’istanza per inviare SMS, inclusa l’integrazione delle impostazioni del provider con [!DNL Journey Optimizer]. [Ulteriori informazioni](../sms/sms-configuration.md)

1. Al termine, devi creare **superfici di canale** per configurare tutti i parametri tecnici necessari per la consegna dei messaggi. [Ulteriori informazioni](channel-surfaces.md)

1. È inoltre possibile:

   * Gestisci il numero di giorni durante i quali vengono eseguiti nuovi tentativi prima di inviare indirizzi e-mail all’elenco di soppressione. [Ulteriori informazioni](manage-suppression-list.md)

   * Abilitare l’**opzione e-mail Ccn** per conservare una copia dei messaggi inviati ai singoli utenti. [Ulteriori informazioni](archiving-support.md#enable-bcc)

   * Configurare le **regole di frequenza** per evitare di sollecitare eccessivamente i destinatari. [Ulteriori informazioni](frequency-rules.md)

   * Determinare l’indirizzo e-mail e/o il numero di telefono da utilizzare in priorità per i destinatari quando sono disponibili diversi indirizzi/numeri in Adobe Experience Platform. [Ulteriori informazioni](primary-email-addresses.md)

<!--* Understand the push notification flow. [Learn more](../push/push-gs.md)-->

>[!NOTE]
>
>Questi passaggi devono essere eseguiti da un [amministratore di sistema di Adobe Journey Optimizer](../start/path/administrator.md).

## Configurare i percorsi

Per creare i percorsi, è necessario configurare **[!UICONTROL Origini dati]**, **[!UICONTROL Eventi]** e **[!UICONTROL Azioni]**. [Ulteriori informazioni](about-data-sources-events-actions.md)

![](assets/admin-menu.png)

* La configurazione dell‘**origine dati** consente di definire una connessione a un sistema per il recupero di informazioni aggiuntive che verranno utilizzate nei percorsi. [Ulteriori informazioni](../datasource/about-data-sources.md)

* **Eventi** ti consente di attivare i tuoi percorsi in modo unitario per inviare messaggi in tempo reale all’utente che entra nel percorso. Nella configurazione dell’evento, puoi configurare gli eventi previsti nei percorsi. I dati degli eventi in arrivo vengono normalizzati seguendo Adobe Experience Data Model (XDM). Gli eventi provengono dalle API Streaming Ingestion (acquisizione dati in streaming) per gli eventi autenticati e non autenticati, ad esempio gli eventi SDK di Adobe Mobile. [Ulteriori informazioni](../event/about-events.md)

* [!DNL Journey Optimizer] viene fornito con funzionalità per i messaggi incorporate che consentono di progettare e inviare il contenuto. Se per l’invio di messaggi utilizzi un sistema di terze parti, crea un‘**azione personalizzata**. [Ulteriori informazioni](../action/action.md)