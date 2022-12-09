---
solution: Journey Optimizer
product: journey optimizer
title: Guida introduttiva di Journey Optimizer per l'amministratore di sistema
description: In qualità di amministratore di sistema, scopri di più su come lavorare con Journey Optimizer
level: Intermediate
exl-id: 24f85ced-aa45-493f-b2c4-7c7b58351b38
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '709'
ht-degree: 0%

---

# Guida introduttiva per gli amministratori di sistema {#get-started-sys-admins}

Prima di iniziare a utilizzare [!DNL Adobe Journey Optimizer], sono necessari diversi passaggi per preparare l’ambiente.  È necessario eseguire questi passaggi in modo che il [Ingegnere dati](data-engineer.md) e [Journey Practicer](marketer.md) può iniziare a lavorare con [!DNL Adobe Journey Optimizer].


Come **Amministratore di sistema**, devi **comprendere i profili di prodotto e assegnare le autorizzazioni** per l’amministrazione sandbox e la configurazione del canale. È inoltre necessario impostare le sandbox e gestirle per i profili di prodotto disponibili. Potrai quindi assegnare i membri del team ai profili di prodotto.

Queste funzionalità possono essere gestite da **[!UICONTROL Product administrators]** che hanno accesso ad Admin Console. [Ulteriori informazioni su Adobe Admin Console](https://helpx.adobe.com/enterprise/admin-guide.html){target=&quot;_blank&quot;}.

Scopri la gestione degli accessi nelle pagine seguenti:

1. **Creare sandbox** per suddividere le istanze in ambienti virtuali separati e isolati. **Sandbox** vengono create in [!DNL Journey Optimizer]. Ulteriori informazioni nel [Sandbox](../../administration/sandboxes.md) sezione .

   >[!NOTE]
   >Come **Amministratore di sistema**, se non riesci a visualizzare il **[!UICONTROL Sandboxes]** menu in [!DNL Journey Optimizer], aggiorna le autorizzazioni in [Admin Console](https://adminconsole.adobe.com/){_blank}. Scopri come aggiornare il profilo di prodotto in [questa pagina](../../administration/permissions.md#edit-product-profile).

1. **Comprendere i profili di prodotto**. I profili di prodotto sono un insieme di diritti unitari che consentono agli utenti di accedere a determinate funzionalità o oggetti nell’interfaccia. Ulteriori informazioni nel [Profili di prodotto preconfigurati](../../administration/ootb-product-profiles.md) sezione .

1. **Impostare le autorizzazioni** per i profili di prodotto, tra cui **Sandbox** e dai accesso ai membri del tuo team assegnandoli a profili di prodotto diversi. Questo passaggio viene eseguito nella [Admin Console](https://adminconsole.adobe.com/){_blank}. Le autorizzazioni sono diritti unitari che ti consentono di definire le autorizzazioni assegnate a **[!UICONTROL Product profile]**. Ogni autorizzazione è raccolta in funzionalità, ad esempio Journey o Offerte, che rappresenta le diverse funzionalità o oggetti in [!DNL Journey Optimizer]. Ulteriori informazioni nel [Livelli di autorizzazione](../../administration/high-low-permissions.md) sezione .

Inoltre, devi aggiungere gli utenti che hanno bisogno di accedere ad Assets Essentials alla sezione **Utenti consumer di Assets Essentials** o **Utenti di Assets Essentials** Profili di prodotto. [Ulteriori informazioni nella documentazione di Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html){target=&quot;_blank&quot;}.

>[!NOTE]
>Per i prodotti Journey Optimizer ottenuti prima del 6 gennaio 2022, devi distribuire [!DNL Adobe Experience Manager Assets Essentials] per la tua organizzazione. Ulteriori informazioni nel [Distribuire le risorse di base](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html)Sezione {target=&quot;_blank&quot;}.

Quando accedi [!DNL Journey Optimizer] per la prima volta, viene effettuato il provisioning di una sandbox di produzione e viene allocato un certo numero di IP a seconda del contratto.

Per creare i tuoi percorsi e inviare messaggi, accedi al **AMMINISTRAZIONE** menu. Sfoglia il **[!UICONTROL Channels]** per configurare i messaggi e le superfici del canale (ad es. predefiniti messaggio).

>[!NOTE]
>Come **Amministratore di sistema**, se non riesci a visualizzare il **[!UICONTROL Channels]** menu in [!DNL Journey Optimizer], aggiorna le autorizzazioni in [Admin Console](https://adminconsole.adobe.com/){_blank}. Scopri come aggiornare il profilo di prodotto in [questa pagina](../../administration/permissions.md#edit-product-profile).

Segui i passaggi elencati di seguito:

1. **Configurare messaggi e canali**: definire superfici, adattare e personalizzare le impostazioni e-mail, sms e messaggi push

   * Definisci **impostazioni delle notifiche push** in entrambi [!DNL Adobe Experience Platform] e [!DNL Adobe Experience Platform Launch]. [Ulteriori informazioni](../../push/push-gs.md)

   * Crea **superfici del canale** (ad esempio, predefiniti per messaggi) per configurare tutti i parametri tecnici richiesti per e-mail, sms e notifiche push. [Ulteriori informazioni](../../configuration/channel-surfaces.md)

   * Configura le **Canale SMS** per configurare tutti i parametri tecnici richiesti per SMS. [Ulteriori informazioni](../../sms/sms-configuration.md)

   * Gestire il numero di giorni durante i quali **tentativi** vengono eseguite prima di inviare indirizzi e-mail all’elenco di soppressione. [Ulteriori informazioni](../../configuration/manage-suppression-list.md)

1. **Delega sottodomini**: per utilizzare qualsiasi nuovo sottodominio in Journey Optimizer, il primo passaggio consiste nel delegarlo. [Ulteriori informazioni](../../configuration/about-subdomain-delegation.md)

   ![](../assets/subdomain.png)

1. **Creare pool IP**: migliora il recapito e la reputazione delle e-mail raggruppando gli indirizzi IP forniti con la tua istanza. [Ulteriori informazioni](../../configuration/ip-pools.md)

   ![](../assets/ip-pool.png)

1. **Gestire la soppressione e gli elenchi consentiti**: migliorare il recapito messaggi con eliminazione ed elenchi consentiti

   * A [elenco a discesa](../../reports/suppression-list.md) è costituito da indirizzi e-mail che desideri escludere dalle consegne, in quanto l’invio a tali contatti potrebbe danneggiare la reputazione dell’invio e i tassi di consegna. Puoi monitorare tutti gli indirizzi e-mail che vengono automaticamente esclusi dall’invio in un percorso, ad esempio indirizzi non validi, indirizzi costantemente non recapitati e che potrebbero influenzare negativamente la reputazione dell’e-mail e destinatari che inviano un reclamo di qualche tipo relativo a uno dei tuoi messaggi e-mail. Scopri come gestire il [elenco a discesa](../../configuration/manage-suppression-list.md) e [tentativi](../../configuration/retries.md).
   ![](../assets/suppression-list-filtering-example.png)

   * La [elenco Consentiti](../../configuration/allow-list.md) consente di specificare singoli indirizzi e-mail o domini che saranno gli unici destinatari o domini autorizzati a ricevere le e-mail che stai inviando da una sandbox specifica. Questo può impedire l’invio accidentale di e-mail a veri indirizzi dei clienti in un ambiente di test. Scopri come [abilitare l’elenco consentito](../../configuration/allow-list.md).
   Ulteriori informazioni sulla gestione del recapito messaggi in [!DNL Adobe Journey Optimizer] [in questa pagina](../../reports/deliverability.md).
