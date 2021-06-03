---
title: Linee guida sulle impostazioni e sulla configurazione di Journey Optimizer
description: Scopri le linee guida per la configurazione dei messaggi e dei percorsi
audience: administrators
content-type: reference
role: Administrator
level: Intermediate
product: Adobe Journey Optimizer
solution: Journey Optimizer
exl-id: 0964a484-f957-4aae-a571-61b2a1615026
source-git-commit: 61de8dc27029e229a203be8a984d6fa2d4f365e0
workflow-type: tm+mt
source-wordcount: '332'
ht-degree: 9%

---


# Guida introduttiva alla configurazione [!DNL Journey Optimizer]

Quando accedi a [!DNL Journey Optimizer] per la prima volta, ti viene fornito un sandbox di produzione e assegnato un certo numero di IP a seconda del contratto.

Per poter creare i tuoi percorsi e inviare messaggi, devi seguire questi passaggi di configurazione:

1. **Configura messaggi e canali**: definire predefiniti, adattare e personalizzare e-mail e messaggi push

   * Definisci le impostazioni delle notifiche push sia in [!DNL Adobe Experience Platform] che in [!DNL Adobe Experience Platform Launch]. [Ulteriori informazioni](../push-configuration.md)

   * Crea i predefiniti per i messaggi per configurare tutti i parametri tecnici necessari per i messaggi e-mail e per i messaggi di notifica push. [Ulteriori informazioni](message-presets.md)

   * Determina l’indirizzo e-mail da utilizzare in priorità per i destinatari quando sono disponibili più indirizzi in Adobe Experience Platform. [Ulteriori informazioni](primary-email-addresses.md)

   * Gestisci il numero di giorni durante i quali vengono eseguiti nuovi tentativi prima di inviare indirizzi e-mail all’elenco di eliminazione. [Ulteriori informazioni](manage-suppression-list.md)

   <!--
    * Understand push notification flow. [Learn more](../push-gs.md)
    -->

1. **Delega sottodomini**: per utilizzare un nuovo sottodominio in Journey Optimizer, il primo passaggio consiste nel delegarlo. [Ulteriori informazioni](about-subdomain-delegation.md)

   ![](../assets/subdomain.png)

1. **Crea pool** IP: migliora il recapito e la reputazione delle e-mail raggruppando gli indirizzi IP forniti con la tua istanza. [Ulteriori informazioni](ip-pools.md)

   ![](../assets/ip-pool.png)

1. **Configura percorsi**: per generare percorsi, devi configurare  **[!UICONTROL Data Sources]**,  **[!UICONTROL Events]** e  **[!UICONTROL Actions]**. [Ulteriori informazioni](about-data-sources-events-actions.md)

   ![](../assets/admin-menu.png)

   * La configurazione **Origine dati** ti consente di definire una connessione a un sistema per recuperare informazioni aggiuntive che verranno utilizzate nei tuoi percorsi. Ulteriori informazioni sulle origini dati in questa sezione [sezione](../datasource/about-data-sources.md)

   * **** Eventsallow you per attivare i tuoi percorsi singolarmente per inviare messaggi, in tempo reale, all&#39;individuo che scorre nel percorso. Nella configurazione dell’evento, puoi configurare gli eventi previsti nei percorsi. I dati degli eventi in arrivo vengono normalizzati seguendo Adobe Experience Data Model (XDM). Gli eventi provengono dalle API Streaming Ingestion per gli eventi autenticati e non autenticati, ad esempio gli eventi SDK di Adobe Mobile. Ulteriori informazioni sugli eventi in questa sezione [sezione](../event/about-events.md)

   * [!DNL Journey Optimizer] include funzionalità integrate per messaggi: puoi progettare il contenuto e pubblicare il messaggio. Se utilizzi un sistema di terze parti per l’invio dei messaggi, crea un’ **azione personalizzata**. Ulteriori informazioni sulle azioni in questa sezione [sezione](../action/action.md)