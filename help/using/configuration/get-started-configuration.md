---
solution: Journey Optimizer
product: journey optimizer
title: Introduzione a [!DNL Journey Optimizer] configurazione
description: Ulteriori informazioni [!DNL Journey Optimizer] configurazione
role: Admin
level: Intermediate
exl-id: 0964a484-f957-4aae-a571-61b2a1615026
feature: Application Settings
topic: Administration
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 40%

---


# Introduzione a [!DNL Journey Optimizer] configurazione {#start-optimizer-configuration}

Quando accedi a [!DNL Journey Optimizer] per la prima volta, viene effettuato il provisioning di una sandbox di produzione e viene allocato un determinato numero di IP a seconda del contratto.

Per creare i tuoi percorsi e inviare messaggi, devi seguire i passaggi di configurazione riportati di seguito.

## Configurare messaggi e canali

Definisci le superfici dei canali, adatta e personalizza i messaggi.

* [Delega ad Adobe dei sottodomini](about-subdomain-delegation.md) desideri utilizzare per inviare e-mail e [creare pool IP](ip-pools.md) per raggruppare gli indirizzi IP forniti con la tua istanza.

* Gestisci il numero di giorni durante i quali vengono eseguiti nuovi tentativi prima di inviare indirizzi e-mail all’elenco di soppressione. [Ulteriori informazioni](manage-suppression-list.md)

* Definisci le impostazioni delle notifiche push sia in [!DNL Adobe Experience Platform] e in [!DNL Adobe Experience Platform Launch]. [Ulteriori informazioni](../push/push-gs.md)

   <!--* Understand the push notification flow. [Learn more](../push/push-gs.md)-->

* Configura l’istanza per inviare SMS (attualmente disponibile solo per un set di organizzazioni - Disponibilità limitata). [Ulteriori informazioni](../sms/sms-configuration.md)

* Crea superfici di canale per configurare tutti i parametri tecnici necessari per la consegna dei messaggi. [Ulteriori informazioni](channel-surfaces.md)

* Determina l’indirizzo e-mail e/o il numero di telefono da utilizzare in priorità per i destinatari quando sono disponibili diversi indirizzi/numeri in Adobe Experience Platform. [Ulteriori informazioni](primary-email-addresses.md)

## Configurare i percorsi

Per generare percorsi, è necessario configurare **[!UICONTROL Origini dati]**, **[!UICONTROL Eventi]** e **[!UICONTROL Azioni]**. [Ulteriori informazioni](about-data-sources-events-actions.md)

![](assets/admin-menu.png)

* La **sorgente dati** La configurazione ti consente di definire una connessione a un sistema per recuperare informazioni aggiuntive che verranno utilizzate nei tuoi percorsi. [Ulteriori informazioni](../datasource/about-data-sources.md)

* **Eventi** ti consente di attivare i tuoi percorsi in modo unitario per inviare messaggi in tempo reale all’utente che entra nel percorso. Nella configurazione dell’evento, puoi configurare gli eventi previsti nei percorsi. I dati degli eventi in arrivo vengono normalizzati seguendo Adobe Experience Data Model (XDM). Gli eventi provengono dalle API Streaming Ingestion (acquisizione dati in streaming) per gli eventi autenticati e non autenticati, ad esempio gli eventi SDK di Adobe Mobile. [Ulteriori informazioni](../event/about-events.md)

* [!DNL Journey Optimizer] viene fornito con funzionalità integrate per la progettazione e l’invio di contenuti. Se utilizzi un sistema di terze parti per l’invio dei messaggi, crea un **azione personalizzata**. [Ulteriori informazioni](../action/action.md)