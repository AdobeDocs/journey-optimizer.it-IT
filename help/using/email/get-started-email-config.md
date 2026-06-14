---
solution: Journey Optimizer
product: journey optimizer
title: Introduzione alla configurazione e-mail
description: Ulteriori informazioni sulla configurazione e-mail in  [!DNL Journey Optimizer]
role: Admin
level: Experienced
feature: Channel Configuration, Email
topic: Administration
keywords: e-mail, configurazione, superficie, sottodomini
exl-id: 1fc9a4f6-6c34-4414-b400-aac6bda9ee25
TQID: https://experienceleague.adobe.com/mVdk2WGb0rL06j1cmNEh4fj0JC-hwuro8ku-0Yv02N8
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d556b755-390a-43f0-be32-a08cf6236126id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2: id: e30b0a1a-b594-47b8-af94-1e3a2be6df11id: e5329d1b-e590-4e24-a3fb-ef3fe0f2c721id: fae48155-b23f-40d2-a252-a25bce350b4d
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: bc98cb2b61c7c5c8dac78b494fe293a4106a88c4
workflow-type: tm+mt
source-wordcount: 563
ht-degree: 73%

---

# Introduzione alla configurazione e-mail {#get-starte-email-config}

>[!BEGINSHADEBOX]

**In questa pagina:** scopri i passaggi essenziali per configurare il canale e-mail in Adobe Journey Optimizer, dalla delega dei sottodomini alla creazione di pool IP alla configurazione delle configurazioni dei canali, ai campi di esecuzione e ai nuovi tentativi.

>[!ENDSHADEBOX]

La configurazione del canale e-mail in Adobe Journey Optimizer rappresenta il tuo ingresso per la creazione di esperienze e-mail significative e personalizzate che coinvolgono efficacemente il pubblico.

Questa sezione descrive i passaggi di configurazione essenziali da seguire per inviare e-mail tramite [!DNL Journey Optimizer]. Scoprirai anche come impostare le intestazioni delle e-mail, personalizzare le impostazioni per più marchi, abilitare il tracciamento URL per le analisi e persino aggiungere collegamenti con un solo clic per annullare l’abbonamento per comodità dell’utente. Ogni argomento si basa sul precedente, fornendoti gli strumenti per perfezionare la strategia e-mail mantenendo al contempo il controllo e la precisione.

Per inviare e-mail tramite percorsi e campagne in [!DNL Journey Optimizer], devi seguire diversi passaggi di configurazione. Di seguito sono elencati i passaggi da eseguire:

1. Per garantire la recapitabilità ottimale e proteggere la reputazione, inizia **delegando a Adobe i sottodomini** con cui invierai le e-mail con [!DNL Journey Optimizer]. Questi sottodomini determineranno elementi quali le pagine web da tracciare e gli URL della pagina mirror. [Ulteriori informazioni](../configuration/about-subdomain-delegation.md)

   ![](../configuration/assets/subdomain-list.png)

1. Crea pool IP per **raggruppare gli indirizzi IP** per i quali è stato eseguito il provisioning con la tua istanza. [Ulteriori informazioni](../configuration/ip-pools.md)

   ![](../configuration/assets/ip-pool-create.png)

1. Crea **configurazioni dei canali** e seleziona il canale **[!UICONTROL e-mail]**. [Ulteriori informazioni](../configuration/channel-surfaces.md)


   ![](../configuration/assets/preset-general.png)

1. In ogni configurazione dei canali e-mail, configura tutti i **parametri tecnici** necessari per inviare e-mail. [Ulteriori informazioni](email-settings.md)

   * In questo punto è possibile selezionare il sottodominio da utilizzare per inviare le e-mail e i pool IP da associare alla configurazione. [Ulteriori informazioni](email-settings.md#ip-pools)

   ![](assets/surface-subdomain-ip-pool.png)

   * Il **[!UICONTROL Prefisso e-mail Da]** e il **[!UICONTROL Prefisso e-mail di errore]** utilizzano il [sottodominio delegato](../configuration/about-subdomain-delegation.md) attualmente selezionato. Facoltativamente, **[!UICONTROL Nome mittente]** e **[!UICONTROL Indirizzo e-mail mittente]** possono identificare un&#39;altra parte trasmittente (indirizzo completo **Mittente**, non associato al suffisso del sottodominio). [Ulteriori informazioni](header-parameters.md#sender-header)

   ![](assets/preset-header.png)

1. Completa la configurazione del canale e-mail impostando altri parametri avanzati, ad esempio abilitare CCN, definire il tracciamento URL per le analisi o aggiungere collegamenti di annullamento dell’abbonamento con un solo clic per comodità dell’utente. [Ulteriori informazioni](email-settings.md)

1. Determina quali **campi di esecuzione** utilizzare in priorità per i destinatari quando sono disponibili più indirizzi in Adobe Experience Platform. [Ulteriori informazioni](../configuration/primary-email-addresses.md)

   ![](../configuration/assets/primary-address-execution-fields.png)

1. Gestisci il numero di giorni durante i quali vengono eseguiti **nuovi tentativi** prima di inviare indirizzi e-mail all’elenco di soppressione. [Ulteriori informazioni](../configuration/manage-suppression-list.md)

   ![](../configuration/assets/suppression-list-edit-retries.png)


:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg)

Consulta la configurazione e-mail

Scopri i passaggi essenziali per configurare le funzionalità e-mail, inclusa la delega dei sottodomini, i pool IP e la gestione degli elenchi di soppressione.

[Inizia la configurazione dell’e-mail](get-started-email-config.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg)

Definire le impostazioni della configurazione e-mail

Imposta le configurazioni delle e-mail per la recapitabilità, la conformità e la personalizzazione con funzioni avanzate come CCN, sostituzioni di soppressione e tracciamento URL.

[Configurare le impostazioni](email-settings.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg)

Abilitare e configurare l’annullamento dell’iscrizione alla mailing list

Scopri come abilitare la funzione “Annulla iscrizione a mailing list” per includere gli URL di annullamento dell’iscrizione con un solo clic nelle intestazioni delle e-mail per le rinunce dei destinatari.

[Configura l’annullamento dell’iscrizione a mailing list](list-unsubscribe.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg)

Configurare i parametri dell’intestazione e-mail

Personalizza gli indirizzi e-mail del mittente e della risposta, gestisci gli errori e inoltra le e-mail per una comunicazione efficace.

[Configura i parametri dell’intestazione](header-parameters.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg)

Configurare il tracciamento URL per il canale e-mail

Imposta i parametri di tracciamento URL per misurare l’efficacia delle campagne e-mail e l’integrazione con gli strumenti di analisi.

[Configura il tracciamento URL](url-tracking.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg)

Impostazioni della configurazione e-mail personalizzate

Configura sottodomini dinamici, intestazioni personalizzate e tracciamento URL per fornire esperienze e-mail personalizzate.

[Configurare un’e-mail personalizzata](surface-personalization.md)
:::

::::
