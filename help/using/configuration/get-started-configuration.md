---
solution: Journey Optimizer
product: journey optimizer
title: Introduzione alla configurazione di  [!DNL Journey Optimizer]  canali
description: Ulteriori informazioni sulla configurazione di  [!DNL Journey Optimizer]  canali
role: Admin, Developer
level: Intermediate, Experienced
exl-id: 0964a484-f957-4aae-a571-61b2a1615026
feature: Application Settings
topic: Administration
keywords: configurazione, configurare, messaggi, canale, sandbox, optimizer
source-git-commit: efb943e5a6f27becc6e8b6128b776e46d6141823
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 34%

---


# Introduzione alla configurazione dei canali {#start-optimizer-configuration}

>[!CONTEXTUALHELP]
>id="ajo_channels_rate_controls"
>title="Controlli di frequenza per i canali"
>abstract="Controlli di frequenza per i canali"

Quando accedi a [!DNL Journey Optimizer] per la prima volta, viene effettuato il provisioning di una sandbox di produzione e viene allocato un determinato numero di IP a seconda del contratto.

Per poter inviare messaggi, devi seguire i passaggi di configurazione elencati di seguito:

1. In qualità di [amministratore di sistema Adobe Journey Optimizer](../start/path/administrator.md), definisci le configurazioni specifiche per il tuo canale. Scopri come impostare queste configurazioni nelle pagine seguenti:

   <table style="table-layout:fixed"><tr style="border: 0;">
    <td><a href="../email/get-started-email-config.md"><img alt="e-mail" src="../channels/assets/do-not-localize/email.png"></a>
    <div align="center"><a href="../email/get-started-email-config.md"><strong>E-mail</strong></a></div></td>
    <td><a href="../sms/sms-configuration.md"><img alt="SMS" src="../channels/assets/do-not-localize/sms.png"></a>
    <div align="center"><a href="../sms/sms-configuration.md"><strong>SMS</strong></a></div></td>
    <td><a href="../push/push-configuration.md"><img alt="push" src="../channels/assets/do-not-localize/push.png"></a>
    <div align="center"><a href="../push/push-configuration.md"><strong>Notifica push</strong></a></div></td>
    <td><a href="../direct-mail/direct-mail-configuration.md"><img alt="direct mail" src="../channels/assets/do-not-localize/direct-mail.jpg"></a>
    <div align="center"><a href="../direct-mail/direct-mail-configuration.md"><strong>Direct mail</strong></a></div></td>
    </tr></table>

   <table style="table-layout:fixed"><tr style="border: 0;">
    <td><a href="../in-app/inapp-configuration.md"><img alt="in-app" src="../channels/assets/do-not-localize/inapp.jpg"></a>
    <div align="center"><a href="../in-app/inapp-configuration.md"><strong>In-app</strong></a></div></td>
    <td><a href="../web/web-configuration.md"><img alt="web" src="../channels/assets/do-not-localize/web.jpg"></a>
    <div align="center"><a href="../web/web-configuration.md"><strong>Web</strong></a></div></td>
    <td><a href="../code-based/code-based-configuration.md"><img alt="esperienza basata su codice" src="../channels/assets/do-not-localize/code.png"></a>
    <div align="center"><a href="../code-based/code-based-configuration.md"><strong>Esperienza basata su codice</strong></a></div></td>
    <td><a href="../content-card/content-card-configuration-prereq.md"><img alt="schede contenuto" src="../channels/assets/do-not-localize/cards.png"></a>
    <div align="center"><a href="../content-card/content-card-configuration-prereq.md"><strong>Schede contenuto</strong></a></div></td>
    </tr></table>

   >[!NOTE]
   >
   >Per i canali mobili, la [configurazione guidata del canale](set-mobile-config.md) facilita la configurazione rapida dei canali di marketing, garantendo che tutte le risorse richieste siano prontamente disponibili in Experience Platform, Journey Optimizer e Data Collection. Questo consente al team di marketing di iniziare la creazione di campagne e percorsi.

1. Al termine, devi configurare tutti i parametri tecnici necessari per consegnare i messaggi creando **configurazioni canale**. [Ulteriori informazioni sulle configurazioni dei canali](channel-surfaces.md)

1. A seconda dei canali in uso, degli ambienti e delle esigenze, è necessario eseguire anche i seguenti passaggi:

   * Configurazione e delega del sottodominio per i canali, ad esempio [e-mail](about-subdomain-delegation.md), [SMS](../sms/sms-subdomains.md), [pagine di destinazione](../landing-pages/lp-subdomains.md) ed [esperienze Web](../web/web-delegated-subdomains.md).

   * Imposta i piani di riscaldamento IP per una consegna dei messaggi ottimale. [Ulteriori informazioni](ip-warmup-gs.md)

   * Definisci un elenco Consentiti per l’invio di e-mail. [Ulteriori informazioni](allow-list.md)

   * Gestisci il numero di giorni durante i quali vengono eseguiti nuovi tentativi prima di inviare indirizzi e-mail all’elenco di soppressione. [Ulteriori informazioni](manage-suppression-list.md)

   * Abilita l&#39;opzione e-mail **Ccn** per conservare una copia dei messaggi inviati a singoli utenti. [Ulteriori informazioni](archiving-support.md#enable-bcc)

   * Configura **regole business** per evitare di sollecitare eccessivamente i destinatari. [Ulteriori informazioni](../conflict-prioritization/rule-sets.md)

   * Determinare l’indirizzo e-mail e/o il numero di telefono da utilizzare in priorità per i destinatari quando sono disponibili diversi indirizzi/numeri in Adobe Experience Platform. [Ulteriori informazioni](primary-email-addresses.md)

## Risorse aggiuntive

* **[Configurare le superfici di canale](channel-surfaces.md)** - Scopri come impostare e gestire le superfici di canale per e-mail, push, SMS e altri canali.
* **[Delega dei sottodomini](delegate-subdomain.md)** - Scopri come delegare i sottodomini ad Adobe per il recapito messaggi e-mail e il branding.
* **[Riscaldamento IP](ip-warmup-gs.md)** - Scopri le best practice per il riscaldamento dell&#39;indirizzo IP per migliorare il recapito messaggi e-mail e la reputazione del mittente.
* **[Gestisci elenco di soppressione](manage-suppression-list.md)** - Scopri come gestire gli elenchi di soppressione per gestire i mancati recapiti e mantenere l&#39;igiene degli elenchi.
* **[Configura app mobili](set-mobile-config.md)** - Configura le configurazioni di app mobili per le notifiche push e i messaggi in-app.
* **[Esercitazioni di configurazione](https://experienceleague.adobe.com/it/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/configure-channels){target="_blank"}**: esplora esercitazioni video dettagliate sulla configurazione dei canali e sulle best practice.
