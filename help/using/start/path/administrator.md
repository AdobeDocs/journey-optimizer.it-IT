---
title: Guida introduttiva di Journey Optimizer per l'amministratore di sistema
description: In qualità di amministratore di sistema, scopri di più su come lavorare con Journey Optimizer
level: Intermediate
exl-id: 24f85ced-aa45-493f-b2c4-7c7b58351b38
source-git-commit: 1d0e28583c500d5eddf9f88250f279d188c4784a
workflow-type: tm+mt
source-wordcount: '704'
ht-degree: 2%

---

# Guida introduttiva per gli amministratori di sistema {#get-started-sys-admins}

Prima di iniziare a utilizzare [!DNL Adobe Journey Optimizer], sono necessari diversi passaggi per preparare l’ambiente.  È necessario eseguire questi passaggi in modo che il [Ingegnere dati](data-engineer.md) e [Praticatore percorso](marketer.md) può iniziare a lavorare con [!DNL Adobe Journey Optimizer].


Come **Amministratore di sistema**, devi **comprendere i profili di prodotto e assegnare le autorizzazioni** per l’amministrazione sandbox e la configurazione del canale. È inoltre necessario impostare le sandbox e gestirle per i profili di prodotto disponibili. Potrai quindi assegnare i membri del team ai profili di prodotto.

Queste funzionalità possono essere gestite da **[!UICONTROL Product administrators]** che hanno accesso ad Admin Console. [Ulteriori informazioni su Adobe Admin Console](https://helpx.adobe.com/it/enterprise/admin-guide.html){target=&quot;_blank&quot;}.

Scopri la gestione degli accessi nelle pagine seguenti:

1. **Creare sandbox** per suddividere le istanze in ambienti virtuali separati e isolati. **Sandbox** vengono create in [!DNL Journey Optimizer]. Ulteriori informazioni nel [Sandbox](../../administration/sandboxes.md) sezione .

   >[!NOTE]
   >Come **Amministratore di sistema**, se non riesci a visualizzare il **[!UICONTROL Sandboxes]** menu in [!DNL Journey Optimizer], aggiorna le autorizzazioni in [Admin Console](https://adminconsole.adobe.com/){_blank}. Scopri come aggiornare il profilo di prodotto in [questa pagina](../../administration/permissions.md#edit-product-profile).

1. **Comprendere i profili di prodotto**. I profili di prodotto sono un insieme di diritti unitari che consentono agli utenti di accedere a determinate funzionalità o oggetti nell’interfaccia. Ulteriori informazioni nel [Profili di prodotto preconfigurati](../../administration/ootb-product-profiles.md) sezione .

1. **Impostare le autorizzazioni** per i profili di prodotto, tra cui **Sandbox** e dai accesso ai membri del tuo team assegnandoli a profili di prodotto diversi. Questo passaggio viene eseguito nella [Admin Console](https://adminconsole.adobe.com/){_blank}. Le autorizzazioni sono diritti unitari che ti consentono di definire le autorizzazioni assegnate a **[!UICONTROL Product profile]**. Ogni autorizzazione viene raccolta in funzionalità, ad esempio Percorso, Messaggi o Offerte, che rappresentano le diverse funzionalità o oggetti in [!DNL Journey Optimizer]. Ulteriori informazioni nel [Livelli di autorizzazione](../../administration/high-low-permissions.md) sezione .

Inoltre, devi aggiungere gli utenti che devono accedere ad Assets Essentials al **Utenti consumer Assets Essentials** o **Utenti Assets Essentials** Profili di prodotto. [Ulteriori informazioni nella documentazione di Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html){target=&quot;_blank&quot;}.

>[!NOTE]
>Per i prodotti Journey Optimizer ottenuti prima del 6 gennaio 2022, devi distribuire [!DNL Adobe Experience Manager Assets Essentials] per la tua organizzazione. Ulteriori informazioni nel [Distribuzione di Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html)Sezione {target=&quot;_blank&quot;}.

Quando accedi [!DNL Journey Optimizer] per la prima volta, viene effettuato il provisioning di una sandbox di produzione e viene allocato un certo numero di IP a seconda del contratto.

Per creare i tuoi percorsi e inviare messaggi, accedi al **AMMINISTRAZIONE** menu. Sfoglia il **[!UICONTROL Channels]** per configurare i messaggi e-mail e i predefiniti.

>[!NOTE]
>Come **Amministratore di sistema**, se non riesci a visualizzare il **[!UICONTROL Channels]** menu in [!DNL Journey Optimizer], aggiorna le autorizzazioni in [Admin Console](https://adminconsole.adobe.com/){_blank}. Scopri come aggiornare il profilo di prodotto in [questa pagina](../../administration/permissions.md#edit-product-profile).

Segui i passaggi elencati di seguito:

1. **Configurare messaggi e canali**: definire predefiniti, adattare e personalizzare le impostazioni e-mail e messaggi push

   * Definisci **impostazioni delle notifiche push** in entrambi [!DNL Adobe Experience Platform] e [!DNL Adobe Experience Platform Launch]. [Ulteriori informazioni](../../configuration/push-gs.md)

   * Crea **predefiniti messaggio** per configurare tutti i parametri tecnici necessari per i messaggi e-mail e di notifica push. [Ulteriori informazioni](../../configuration/message-presets.md)

   * Gestire il numero di giorni durante i quali **tentativi** vengono eseguite prima di inviare indirizzi e-mail all’elenco di soppressione. [Ulteriori informazioni](../../configuration/manage-suppression-list.md)

1. **Delega sottodomini**: per utilizzare un nuovo sottodominio in Journey Optimizer, il primo passaggio consiste nel delegarlo. [Ulteriori informazioni](../../configuration/about-subdomain-delegation.md)

   ![](../assets/subdomain.png)

1. **Creare pool IP**: migliora il recapito e la reputazione delle e-mail raggruppando gli indirizzi IP forniti con la tua istanza. [Ulteriori informazioni](../../configuration/ip-pools.md)

   ![](../assets/ip-pool.png)

1. **Gestire la soppressione e l’elenco Consentiti**: migliorare il recapito messaggi con soppressione ed elenchi Consentiti

   * A [elenco a discesa](../../reports/suppression-list.md) è costituito da indirizzi e-mail che desideri escludere dalle consegne, in quanto l’invio a tali contatti potrebbe danneggiare la reputazione dell’invio e i tassi di consegna. Puoi monitorare tutti gli indirizzi e-mail che vengono automaticamente esclusi dall’invio in un percorso, ad esempio indirizzi non validi, indirizzi costantemente non recapitati e che potrebbero influenzare negativamente la reputazione dell’e-mail e destinatari che inviano un reclamo di qualche tipo relativo a uno dei tuoi messaggi e-mail. Scopri come gestire il [elenco a discesa](../../configuration/manage-suppression-list.md) e [tentativi](../../configuration/retries.md).
   ![](../assets/suppression-list-filtering-example.png)

   * La [elenco Consentiti](../../reports/allow-list.md) consente di specificare singoli indirizzi e-mail o domini che saranno gli unici destinatari o domini autorizzati a ricevere le e-mail che stai inviando da una sandbox specifica. Questo può impedire l’invio accidentale di e-mail a veri indirizzi dei clienti in un ambiente di test. Scopri come [abilita l&#39;elenco Consentiti](../../reports/allow-list.md).
   Ulteriori informazioni sulla gestione del recapito messaggi in [!DNL Adobe Journey Optimizer] [in questa pagina](../../reports/deliverability.md).
