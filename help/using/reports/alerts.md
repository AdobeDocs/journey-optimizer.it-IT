---
solution: Journey Optimizer
product: journey optimizer
title: Accedere e iscriversi agli avvisi di sistema
description: Scopri come accedere e abbonarti agli avvisi di sistema
feature: Journeys, Alerts
topic: Administration
role: User
level: Intermediate
exl-id: 0855ca5b-c7af-41c4-ad51-bed820ae5ecf
source-git-commit: 3aa3203ae7763d81288cb70a2984d017b0006bb3
workflow-type: tm+mt
source-wordcount: '977'
ht-degree: 1%

---

# Accedere e iscriversi agli avvisi di sistema {#alerts}

Durante la creazione di percorsi e campagne, utilizza il pulsante **Avvisi** per verificare e risolvere gli errori prima di eseguirli o pubblicarli:

* Scopri come risolvere i problemi dei percorsi in [questa pagina](../building-journeys/troubleshooting.md).
* Scopri come rivedere le campagne in [questa pagina](../campaigns/review-activate-campaign.md).

Dal menu dedicato **[!UICONTROL Avvisi]**, puoi anche abbonarti a [!DNL Adobe Journey Optimizer] avvisi di sistema, come descritto in questa pagina.

## Accedere agli avvisi {#access-alerts}

In caso di errore, puoi ricevere gli avvisi di sistema nel centro notifiche di Journey Optimizer (avvisi in-app) e/o ricevere un messaggio e-mail. Per accedere a questi avvisi, segui la procedura indicata di seguito.

<!--These messages can repeat over a pre-defined time interval until the alert has been resolved.-->

>[!NOTE]
>
>Ulteriori informazioni sugli avvisi in Adobe Experience Platform sono disponibili nella [documentazione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=it){target="_blank"}.

Nel menu a sinistra, nella sezione **[!UICONTROL Amministrazione]**, fare clic su **[!UICONTROL Avvisi]**. Per Journey Optimizer sono disponibili diversi avvisi preconfigurati.

Esse sono elencate come segue e ogni segnalazione è descritta di seguito.

* Avvisi specifici dei percorsi:

   * l&#39;avviso [Errore azione personalizzata Percorso](#alert-custom-actions)
   * l&#39;avviso [Lettura trigger pubblico non riuscita](#alert-read-audiences)

* Avvisi specifici per la configurazione del canale:

   * avviso [record DNS di dominio AJO mancante](#alert-dns-record-missing)
  <!--* the [AJO channel configuration failure](#alert-channel-config-failure) alert
   * the [AJO domain certificates renewal unsuccessful](#alert-certificates-renewal) alert-->

## Iscriversi agli avvisi {#subscribe-alerts}

1. È possibile sottoscrivere ogni singolo avviso dall&#39;interfaccia utente selezionando l&#39;opzione **[!UICONTROL Sottoscrivi]**.

   ![](assets/alert-subscribe.png){width=80%}

   >[!NOTE]
   >
   >L’abbonamento si applica solo a una sandbox specifica. Devi iscriverti agli avvisi di ogni sandbox singolarmente.

1. Utilizza lo stesso metodo per **[!UICONTROL annullare l&#39;abbonamento]**.

1. È inoltre possibile sottoscrivere avvisi tramite [Notifiche evento I/O](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html?lang=it){target="_blank"}. Le regole di avviso sono organizzate in pacchetti di abbonamento diversi. Gli abbonamenti agli eventi corrispondenti agli avvisi specifici di Journey Optimizer sono descritti di seguito [&#128279;](#journey-alerts).

1. Se si verifica un comportamento imprevisto e/o viene raggiunto un determinato set di condizioni nelle operazioni (ad esempio un potenziale problema quando il sistema supera una soglia), le notifiche di avviso vengono inviate a tutti gli utenti dell’organizzazione che si sono abbonati.

In base alle preferenze dell’abbonato, gli avvisi vengono inviati tramite e-mail e/o direttamente all’interno del centro notifiche di Journey Optimizer, nell’angolo in alto a destra dell’interfaccia utente (notifiche in-app). Seleziona la modalità di ricezione di questi avvisi nelle [!DNL Adobe Experience Cloud] **[!UICONTROL Preferenze]**. [Ulteriori informazioni](../start/user-interface.md#in-product-alerts)

>[!NOTE]
>
>Per impostazione predefinita, è abilitato solo l’avviso in-app.

<!--To enable email alerting, refer to [Adobe Experience Platform documentation](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html?lang=it#enable-email-alerts){target="_blank"}.-->

Quando viene risolto un avviso, gli abbonati ricevono una notifica &quot;Risolto&quot;.

## Gestire gli avvisi {#manage-alerts}

Per gestire gli avvisi, seleziona un elemento e utilizza il pulsante **[!UICONTROL Altre azioni]**.

![](assets/alert-more-actions.png){width=80%}

Per impostazione predefinita, tutti gli avvisi sono attivati. Per disattivare un avviso, selezionare l&#39;opzione **[!UICONTROL Disattiva avviso]** dal menu **[!UICONTROL Altre azioni]**. Tutti gli abbonati a questo avviso non riceveranno più le relative notifiche.

Selezionare **[!UICONTROL Gestisci sottoscrittori avviso]** per visualizzare l&#39;elenco degli utenti che si sono iscritti all&#39;avviso. Utilizza il campo vuoto per aggiungere altri abbonati.

![](assets/alert-subscribers.png){width=80%}

Di seguito sono elencati i possibili stati di avviso:

* **[!UICONTROL Abilitato]** - L&#39;avviso è abilitato e sta monitorando la condizione del trigger.
* **[!UICONTROL Disabilitato]** - L&#39;avviso è disabilitato e non sta monitorando la condizione del trigger. Non riceverai alcuna notifica per questo avviso.
* **[!UICONTROL Attivato]** - La condizione di attivazione dell&#39;avviso è attualmente soddisfatta.

## Avvisi percorso {#journey-alerts}

>[!CAUTION]
>
>Gli avvisi specifici di Adobe Journey Optimizer si applicano solo a **live** percorsi. Gli avvisi non vengono attivati per i percorsi in modalità di test.

### Azione personalizzata percorso non riuscita {#alert-custom-actions}

Questo avviso ti avvisa se un’azione personalizzata non riesce. Riteniamo che si sia verificato un errore in cui si è verificato più dell’1% di errori in una specifica azione personalizzata negli ultimi 5 minuti. Questo viene valutato ogni 30 secondi.

![](assets/alerts-custom-action.png)

Gli avvisi sulle azioni personalizzate vengono risolti quando, negli ultimi 5 minuti:

* l’azione personalizzata non contiene errori (o errori al di sotto della soglia dell’1%),

* oppure, nessun profilo ha raggiunto l’azione personalizzata.

Il nome della sottoscrizione all&#39;evento di I/O corrispondente all&#39;avviso di azione personalizzata è **Errore Percorso azione personalizzata**.

Per risolvere i problemi relativi agli avvisi di **Azione personalizzata**:

* Controlla l’azione personalizzata utilizzando la modalità di test in un altro percorso:

  ![](assets/alert-troubleshooting-2.png)

* Controlla il report di percorso per visualizzare i motivi dell’errore durante l’azione.

  ![](assets/alert-troubleshooting-3.png)

* Controlla il tuo stepEvents di percorso per cercare ulteriori informazioni su &quot;failureReason&quot;.

* Controlla la configurazione dell’azione personalizzata e verifica che l’autenticazione sia ancora valida. Esegui un controllo manuale con Postman, ad esempio.

### Attivatore Read Audience Non Riuscito {#alert-read-audiences}

Questo avviso ti avvisa se un&#39;attività **Read Audience** non ha elaborato alcun profilo 10 minuti dopo l&#39;ora di esecuzione pianificata. Questo errore può essere causato da problemi tecnici o perché il pubblico è vuoto. Se l’errore è causato da problemi tecnici, tieni presente che possono comunque verificarsi nuovi tentativi, a seconda del tipo di problema (ad esempio, se la creazione del processo di esportazione non è riuscita, verrà eseguito un nuovo tentativo ogni 10mn per un massimo di 1h).

![](assets/alerts1.png)

Gli avvisi sulle attività **Read Audience** si applicano solo ai percorsi ricorrenti. **Le attività Read Audience** nei percorsi live che hanno una pianificazione per l&#39;esecuzione di **Once** o **As soon as possible** vengono ignorate.

Gli avvisi in **Read Audience** vengono risolti quando un profilo entra nel nodo **Read Audience**.

Il nome della sottoscrizione all&#39;evento di I/O corrispondente all&#39;avviso **Read Audience Trigger Unsuccess** è **Percorso di ritardo, errori e errori di lettura del pubblico**.

Per risolvere i problemi relativi agli avvisi di **Read Audience**, controlla il numero di tipi di pubblico nell&#39;interfaccia di Experience Platform.

![](assets/alert-troubleshooting-0.png)

![](assets/alert-troubleshooting-1.png)

## Avvisi di configurazione {#configuration-alerts}

### Record DNS di dominio AJO mancante {#alert-dns-record-missing}

Questo avviso notifica quando i record DNS critici (NS o CNAME) necessari per la corretta configurazione del recapito messaggi risultano mancanti o non configurati correttamente. Senza questi record, il recapito messaggi e-mail potrebbe essere compromesso.

>[!NOTE]
>
>* I record NS sono essenziali per la delega completa dei sottodomini ad Adobe. [Ulteriori informazioni](../configuration/about-subdomain-delegation.md#full-subdomain-delegation)
>
>* I record CNAME supportano la configurazione del sottodominio CNAME. [Ulteriori informazioni](../configuration/about-subdomain-delegation.md#cname-subdomain-setup)

L&#39;avviso **Record DNS di dominio AJO mancante** viene attivato quando il sistema rileva che i record NS o CNAME richiesti sono assenti o non corrispondono agli standard di configurazione.

1. Fare clic sull&#39;avviso per reindirizzare al sottodominio [interessato](../configuration/delegate-subdomain.md) nell&#39;interfaccia [!DNL Journey Optimizer].

   <!--For guidance on editing delegated subdomains, see [this section](../configuration/delegate-subdomain.md).-->

1. Correggi la configurazione DNS impostando correttamente i record e [invia di nuovo la delega del sottodominio](../configuration/delegate-subdomain.md#submit-subdomain).

   >[!NOTE]
   >
   >Prima di procedere, assicurati che tutti i record siano stati creati correttamente nella soluzione di hosting del tuo dominio.

1. Se non si è sicuri dei valori corretti, è possibile creare un nuovo sottodominio in [!DNL Journey Optimizer] con lo stesso nome del sottodominio interessato. [Scopri come impostare un nuovo sottodominio](../configuration/delegate-subdomain.md#set-up-subdomain)

Se le modifiche non risolvono il problema, lo stesso avviso viene attivato nuovamente il giorno successivo.

<!--The I/O event subscription name corresponding to this alert is xx. > Do we need to mention this?

### AJO channel configuration failure {#alert-channel-config-failure}

>[!IMPORTANT]
>
>This alert applies only to **email** channel configurations using the [custom subdomain](../configuration/delegate-custom-subdomain.md) delegation type. ///Other channel types (such as SMS, push, or in-app) are not covered by this alert.///

This alert is triggered in case the system audit detects email channel configuration issues. These issues may include misconfigured channel settings, invalid DNS configuration, suppression list issue, IP inconsistency, or any other errors that can impact email delivery.

If you receive such an alert, the resolution steps are listed below:

1. Click the alert to be directed to the impacted [email channel configuration](../email/get-started-email-config.md) in the [!DNL Journey Optimizer] interface.

   For guidance on editing channel configurations, see [this section](../configuration/channel-surfaces.md#edit-channel-surface).

1. Review the configuration details and error messages provided. Common failure reasons include:

   * SPF validation failed
   * DKIM validation failed
   * MX record validation failed
   * Invalid DNS records

   >[!NOTE]
   >
   >The possible configuration failure reasons are listed in [this section](../configuration/channel-surfaces.md).

1. Resolve the issue:

   * Update the channel configuration as needed.
   * You may need to fix specific DNS issues mentioned in the alert.

   >[!NOTE]
   >
   >As a single domain can be associated with multiple channel configurations, resolving DNS issues for one channel configuration may automatically fix related issues across several configurations.

If the change does not resolve the issue, the same alert will be triggered again the next day.

When resolving email configuration issues, keep in mind the best practices listed below:

* Act promptly - Address configuration failures as soon as they are detected to avoid disruptions in email delivery.
* Check all configurations - If the alert indicates multiple impacted email configurations, review and fix each of them.

### AJO domain certificates renewal unsuccessful {#alert-certificates-renewal}

This alert warns you if a domain certificate (CDN, tracking URL) renewal failed for a specific Journey Optimizer subdomain.-->





