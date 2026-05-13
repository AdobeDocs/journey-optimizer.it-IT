---
solution: Journey Optimizer
product: journey optimizer
title: Guida introduttiva di Journey Optimizer per l’amministratore di sistema
description: In qualità di amministratore di sistema, scopri di più su come utilizzare Journey Optimizer
feature: Get Started
role: Admin
level: Intermediate
exl-id: 24f85ced-aa45-493f-b2c4-7c7b58351b38
TQID: https://experienceleague.adobe.com/D--D1ynxQx-Q9eSzjU-fwG0Hc3emaCfa2gIwizpHsQU
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: b856530c-d60b-42d8-a19d-df2dfd7fe62a
  - id: c343082f-e963-4f57-a96b-b64d27f8118e
  - id: cf64c7f6-7428-4ae5-b158-8df9771f38f4
  - id: d2e8a157-b3b0-4143-9ff3-809bf400be56
  - id: d712382d-29ef-487a-93a7-cbebdd2ef24a
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
  - id: e5329d1b-e590-4e24-a3fb-ef3fe0f2c721
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adeb
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 1076
ht-degree: 100%

---

# Guida introduttiva per gli amministratori di sistema {#get-started-sys-admins}

In qualità di **amministratore di sistema**, devi impostare l’ambiente Journey Optimizer e gestire l’accesso per consentire ai team di lavorare in modo efficiente e sicuro. Esegui i passaggi di configurazione essenziali in modo che i [data engineer](data-engineer.md), gli [sviluppatori](developer.md) e i [marketer](marketer.md) possano iniziare a utilizzare [!DNL Adobe Journey Optimizer].

Le tue responsabilità principali includono la configurazione di gruppi di utenti e autorizzazioni, la creazione e la gestione di sandbox per il partizionamento di dati e percorsi per diversi gruppi di utenti e la configurazione di canali di consegna e predefiniti per messaggi per garantire un branding coerente tra i vari messaggi e risorse consegnati tramite Journey Optimizer. Assicurati che le persone giuste abbiano accesso alle funzionalità giuste, mantenendo al contempo la sicurezza e la governance.

Queste funzionalità possono essere gestite dagli **[!UICONTROL amministratori di prodotto]** che hanno accesso alle autorizzazioni del prodotto. [Ulteriori informazioni sulle Autorizzazioni](../../administration/permissions.md){target="_blank"}.

## Impostare l’accesso e le autorizzazioni

Per configurare la gestione degli accessi, segui questi passaggi:

1. **Creare sandbox** per suddividere le istanze in ambienti virtuali separati e isolati. Le **Sandbox** vengono create in [!DNL Journey Optimizer]. Per ulteriori informazioni, consulta la sezione [Sandbox](../../administration/sandboxes.md).

   >[!NOTE]
   >In qualità di **Amministratore di sistema**, se non riesci a visualizzare il menu **[!UICONTROL Sandbox]** in [!DNL Journey Optimizer], è necessario aggiornare le autorizzazioni. Ulteriori informazioni su come aggiornare il ruolo sono disponibili in [questa pagina](../../administration/permissions.md#edit-product-profile).

1. **Informazioni sui ruoli**. I ruoli sono un set di diritti unitari che consente agli utenti di accedere a determinate funzionalità o oggetti nell’interfaccia. Ulteriori informazioni, sono disponibili nella sezione [ruoli preconfigurati](../../administration/ootb-product-profiles.md).

1. **Imposta le autorizzazioni** per i ruoli, incluse le **sandbox**, e consenti l’accesso ai membri del gruppo assegnandoli a ruoli diversi. Le autorizzazioni sono diritti unitari che ti consentono di definire le autorizzazioni assegnate al **[!UICONTROL Ruolo]**. Ogni autorizzazione viene riunita nelle funzionalità, ad esempio Percorso o Offerte, che rappresentano le diverse funzionalità o oggetti in [!DNL Journey Optimizer]. Per ulteriori informazioni, consulta la sezione [Livelli di autorizzazione](../../administration/high-low-permissions.md).

1. **Utilizzare il controllo degli accessi a livello di oggetto** (facoltativo). Applica etichette di accesso a oggetti come percorsi, campagne e configurazioni dei canale per controllare quali utenti possono accedere a risorse specifiche. Ulteriori informazioni su [Controllo degli accessi a livello di oggetto (OLAC)](../../administration/object-based-access.md).

Inoltre, è necessario aggiungere gli utenti che hanno bisogno di accedere ad Assets Essentials per i ruoli di **Utenti consumer di Assets Essentials** e/o **Utenti di Assets Essentials**. [Ulteriori informazioni sono disponibili nella documentazione di Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html?lang=it){target="_blank"}.

Quando accedi a [!DNL Journey Optimizer] per la prima volta, viene effettuato il provisioning di una sandbox di produzione e viene allocato un determinato numero di IP a seconda del contratto.

## Configurare canali e messaggi

Per consentire ai [marketer](marketer.md) di creare e inviare messaggi, accedi al menu **AMMINISTRAZIONE**. Sfoglia il menu **[!UICONTROL Canali]** per configurare le impostazioni dei canali.

>[!NOTE]
>In qualità di **Amministratore di sistema**, se non visualizzi il menu **[!UICONTROL Canali]** in [!DNL Journey Optimizer], aggiorna le autorizzazioni in [Autorizzazioni](../../administration/permissions.md){target="_blank"} prodotto.

Segui questi passaggi:

1. **Imposta le configurazioni dei canali**. Definisci tutti i parametri tecnici richiesti per e-mail, SMS, notifiche push, push web, direct mail e altri canali:

   * Definisci le **impostazioni di notifica push** sia in [!DNL Adobe Experience Platform] che nella Raccolta dati di Adobe Experience Platform. [Ulteriori informazioni](../../push/push-gs.md)

   * Configura le **notifiche push web** per inviare notifiche ai browser di dispositivi mobili e desktop. [Ulteriori informazioni](../../push/push-configuration-web.md)

   * Crea **configurazioni canale** per configurare tutti i parametri tecnici necessari per e-mail, SMS, push, in-app, web e altri canali. [Ulteriori informazioni](../../configuration/channel-surfaces.md)

   * Configura il **Canale SMS** per impostare tutti i parametri tecnici richiesti per gli SMS. [Ulteriori informazioni](../../sms/sms-configuration.md)

   * Gestisci il numero di giorni durante i quali vengono eseguiti **nuovi tentativi** prima di inviare indirizzi e-mail all’elenco di soppressione. [Ulteriori informazioni](../../configuration/manage-suppression-list.md)

   * Abilita l’**esportazione dei messaggi** a livello di configurazione dei canali per archiviare il contenuto di e-mail e SMS inviato quando richiesto (offerta componente aggiuntivo). [Ulteriori informazioni](../../configuration/message-export.md)

1. **Delega sottodomini**: per utilizzare un nuovo sottodominio in Journey Optimizer, il primo passaggio consiste nel delegarlo. [Ulteriori informazioni](../../configuration/about-subdomain-delegation.md). Puoi eseguire la migrazione dei sottodomini da CNAME alla delega personalizzata quando necessario. [Ulteriori informazioni](../../configuration/custom-subdomain-migration.md)

   ![](../assets/subdomain.png)

1. **Crea pool IP**: migliora il recapito e la reputazione delle e-mail raggruppando gli indirizzi IP forniti con la tua istanza. [Ulteriori informazioni](../../configuration/ip-pools.md)

   ![](../assets/ip-pool.png)

1. **Gestisci l‘elenco di soppressione e l‘elenco Consentiti**: migliora il recapito messaggi grazie all‘elenco di soppressione e all‘elenco Consentiti

   * Un [elenco di soppressione](../../reports/suppression-list.md) è costituito da indirizzi e-mail che desideri escludere dalle consegne, in quanto l’invio a tali contatti potrebbe danneggiare la reputazione del mittente e i tassi di consegna. Puoi monitorare tutti gli indirizzi e-mail che vengono automaticamente esclusi dall’invio in un percorso, ad esempio indirizzi non validi, indirizzi con regolare mancato recapito non permanente e che potrebbero influenzare negativamente la reputazione delle e-mail e dei destinatari che presentano un reclamo spam di qualsiasi tipo relativo a uno dei tuoi messaggi e-mail. Scopri come gestire l’[elenco di soppressione](../../configuration/manage-suppression-list.md) e i [nuovi tentativi](../../configuration/retries.md).

   ![](../assets/suppression-list-filtering-example.png)

   * L’[elenco Consentiti](../../configuration/allow-list.md) consente di specificare singoli indirizzi e-mail o domini che saranno gli unici destinatari o domini autorizzati a ricevere le e-mail che stai inviando da una sandbox specifica. In questo modo puoi evitare di inviare accidentalmente e-mail a indirizzi reali dei clienti da un ambiente di test. Scopri come [abilitare l’elenco Consentiti](../../configuration/allow-list.md).

   Ulteriori informazioni sulla gestione della recapitabilità dei messaggi in [!DNL Adobe Journey Optimizer] sono disponibili [in questa pagina](../../reports/deliverability.md).

## Funzionalità aggiuntive

Man mano che le esigenze della tua organizzazione aumentano, considera queste funzionalità avanzate:

* **Criteri di consenso**: se l’organizzazione ha acquistato Healthcare Shield o Privacy and Security Shield, crea criteri del consenso per rispettare le preferenze della clientela nei vari canali. [Ulteriori informazioni](../../action/consent.md)

* **Criteri di governance dei dati**: applica etichette di utilizzo dei dati e criteri per controllare il modo in cui i dati vengono utilizzati nelle azioni di marketing. [Ulteriori informazioni](../../action/action-privacy.md)

* **Piani di preparazione IP**: aumenta gradualmente i volumi di invio di e-mail per creare la reputazione del mittente con i provider di e-mail. [Ulteriori informazioni](../../configuration/ip-warmup-gs.md)

* **Ore di silenzio**: configura i set di regole per esclusioni basate sul tempo, nei periodi specifici in cui i messaggi non devono essere inviati. [Ulteriori informazioni](../../conflict-prioritization/quiet-hours.md)

## Collaborare tra ruoli

Il tuo lavoro amministrativo consente a tutti i team di avere successo:

>[!BEGINTABS]

>[!TAB Supporto per i data engineer]

Collabora con i [data engineer](data-engineer.md) sulla gestione dei dati e dell’accesso. Rivedi la panoramica di [Introduzione alla gestione dei dati](../../data/gs-data.md) per comprendere gli schemi, i set di dati e le origini dati che i data engineer devono configurare.

* Concedi le autorizzazioni per la gestione dei dati e la creazione di schemi
* Approva l’accesso alla sandbox per lo sviluppo e il test
* Coordina i criteri di conservazione dei dati e le regole di governance
* Abilita l’accesso a funzioni avanzate come la Composizione di pubblico federato

>[!TAB Abilitare gli sviluppatori]

Collabora con gli [sviluppatori](developer.md) per l’accesso e il test delle API:

* Fornisci le credenziali API tramite Adobe Developer Console
* Imposta gli ambienti sandbox per lo sviluppo e il test
* Approva le configurazioni dei canali (certificati push, provider SMS)
* Coordina gli ambienti di test e la strategia di implementazione

>[!TAB Potenziare i marketer]

Collabora con i [marketer](marketer.md) per le autorizzazioni e l’impostazione del canale:

* Assegna le autorizzazioni appropriate per la creazione di percorsi e campagne
* Configura i canali che utilizzeranno (e-mail, push, SMS, ecc.)
* Supporta gli ambienti di test e flussi di lavoro di approvazione
* Abilita l’accesso a nuove funzioni e funzionalità

>[!ENDTABS]

## Passaggi successivi

Una volta configurato l’ambiente:

1. **Verifica l’impostazione**: verifica che tutti i membri del team possano accedere alle funzionalità richieste
2. **Monitora l’utilizzo**: utilizza le dashboard di amministrazione per tenere traccia dell’utilizzo del sistema e identificare i problemi
3. **Gestisci le autorizzazioni**: controlla e aggiorna regolarmente le autorizzazioni man mano che i ruoli del team si evolvono
