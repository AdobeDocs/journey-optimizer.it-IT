---
title: Creare predefiniti per messaggi
description: Scopri come configurare e monitorare i predefiniti per messaggi
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
source-git-commit: 9408a93deecfb12f28a0a87c19fa0074c66844a9
workflow-type: tm+mt
source-wordcount: '1206'
ht-degree: 1%

---


# Creare predefiniti per messaggi

Con [!DNL Journey Optimizer] puoi impostare i predefiniti per messaggi che definiscono tutti i parametri tecnici necessari per i messaggi e-mail e di notifica push: tipo di e-mail, indirizzo e-mail e nome del mittente, app mobile e altro ancora.

>[!CAUTION]
>
> * La configurazione dei predefiniti per messaggi è limitata agli amministratori di Percorso. [Ulteriori informazioni](../administration/ootb-product-profiles.md#journey-administrator)
>
> * Devi eseguire i passaggi di configurazione e-mail e push prima di creare i predefiniti per i messaggi.


Una volta configurati i predefiniti per i messaggi, puoi selezionarli al momento della creazione dei messaggi dall’elenco **[!UICONTROL Presets]** .

➡️ [Scopri come creare e utilizzare i predefiniti e-mail in questo video](#video-presets)

## Creare un predefinito per messaggi {#create-message-preset}

Per creare un predefinito per messaggi, effettua le seguenti operazioni:

1. Accedi al menu **[!UICONTROL Channels]** / **[!UICONTROL Message presets]**, quindi fai clic su **[!UICONTROL Create Message preset]**.

   ![](../assets/preset-create.png)

1. Immetti un nome e una descrizione (facoltativi) per il predefinito, quindi seleziona i canali da configurare.

   ![](../assets/preset-general.png)

   >[!NOTE]
   >
   > I nomi devono iniziare con una lettera (A-Z). Può contenere solo caratteri alfanumerici. È inoltre possibile utilizzare i caratteri di sottolineatura `_`, punto`.` e trattino `-`.

1. Configura le impostazioni **email** .

   ![](../assets/preset-email.png)

   * Seleziona il tipo di messaggio da inviare con il predefinito: **Transazionale** o **Marketing**

      >[!CAUTION]
      >
      > **** I messaggi transazionali possono essere inviati a profili che hanno annullato l’abbonamento a comunicazioni di marketing. Questi messaggi possono essere inviati solo in contesti specifici, ad esempio la reimpostazione della password, lo stato dell’ordine e la notifica della consegna.

   * Seleziona il sottodominio da utilizzare per inviare le e-mail. [Ulteriori informazioni](about-subdomain-delegation.md)
   * Seleziona il pool IP da associare al predefinito. [Ulteriori informazioni](ip-pools.md)
   * Immetti i parametri di intestazione per le e-mail inviate utilizzando tale predefinito.

      >[!CAUTION]
      >
      >Ad eccezione del campo **Risposta a (inoltra e-mail)**, il dominio degli indirizzi e-mail deve utilizzare il sottodominio delegato [selezionato corrente](about-subdomain-delegation.md).

      * **[!UICONTROL Sender name]**: Nome del mittente, ad esempio il nome del brand.

      * **[!UICONTROL Sender email]**: L&#39;indirizzo e-mail che desideri utilizzare per le tue comunicazioni. Ad esempio, se il sottodominio delegato è *marketing.luma.com*, puoi utilizzare *contact@marketing.luma.com*.

      * **[!UICONTROL Reply to (name)]**: Nome che verrà utilizzato quando il destinatario fa clic sul pulsante  **** Risposta nel proprio software client e-mail.

      * **[!UICONTROL Reply to (email)]**: Indirizzo e-mail che verrà utilizzato quando il destinatario fa clic sul pulsante  **** Risposta nel proprio software client e-mail. Le e-mail inviate a questo indirizzo verranno inoltrate all&#39; **[!UICONTROL Reply to (forward email)]** indirizzo indicato di seguito. Devi utilizzare un indirizzo definito nel sottodominio delegato (ad esempio, *reply@marketing.luma.com*), altrimenti le e-mail verranno eliminate.

      * **[!UICONTROL Reply to (forward email)]**: Tutte le e-mail ricevute da  [!DNL Journey Optimizer] per il sottodominio delegato verranno inoltrate a questo indirizzo e-mail. Puoi specificare qualsiasi indirizzo, tranne un indirizzo e-mail definito nel sottodominio delegato. Ad esempio, se il sottodominio delegato è *marketing.luma.com*, qualsiasi indirizzo come *abc@marketing.luma.com* è vietato.

      * **[!UICONTROL Error email]**: Tutti gli errori generati dagli ISP dopo alcuni giorni di consegna della posta (mancati recapiti asincroni) vengono ricevuti su questo indirizzo.

      ![](../assets/preset-header.png)

      >[!NOTE]
      >
      >I nomi devono iniziare con una lettera (A-Z). Può contenere solo caratteri alfanumerici. È inoltre possibile utilizzare i caratteri di sottolineatura `_`, punto`.` e trattino `-`.

   * Configura i parametri **esecuzione di un nuovo tentativo e-mail**. Per impostazione predefinita, il [periodo di esecuzione dei nuovi tentativi](retries.md#retry-duration) è impostato su 84 ore, ma è possibile regolare questa impostazione in base alle proprie esigenze.

      ![](../assets/preset-retry-paramaters.png)

      È necessario immettere un valore intero (in ore o minuti) entro il seguente intervallo:
      * Per il tipo di e-mail di marketing, il periodo minimo di esecuzione dei tentativi è di 6 ore.
      * Per il tipo di e-mail transazionale, il periodo minimo di esecuzione dei tentativi è di 10 minuti.
      * Per entrambi i tipi di e-mail, il periodo massimo di esecuzione dei nuovi tentativi è di 84 ore (o 5040 minuti).


1. Configura le impostazioni **notifica push** .

   ![](../assets/preset-push.png)

   * Seleziona almeno una piattaforma: **iOS** e/o **Android**

   * Seleziona le applicazioni mobili da utilizzare per ogni piattaforma.

      Per ulteriori informazioni su come configurare l&#39;ambiente per l&#39;invio di notifiche push, consulta [questa sezione](../push-gs.md).

1. Una volta configurati tutti i parametri, fai clic su **[!UICONTROL Submit]** per confermare. Puoi anche salvare il predefinito del messaggio come bozza e ripristinarne la configurazione in un secondo momento.

   ![](../assets/preset-submit.png)

1. Una volta creato, il predefinito del messaggio viene visualizzato nell’elenco con lo stato **[!UICONTROL Processing]** .

   Durante questo passaggio, verranno eseguiti diversi controlli per verificare che sia stato configurato correttamente. Il tempo di elaborazione è di circa **48h-72h** e può richiedere fino a **7-10 giorni**.

   Questi controlli includono test di recapito messaggi eseguiti dal team di recapito messaggi di Adobe:

   * Convalida SPF
   * Convalida DKIM
   * Convalida record MX
   * Controlla la inserire nell&#39;elenco Bloccati degli IP
   * Controllo host Helo
   * Verifica del pool IP
   * Record A/PTR, verifica del sottodominio t/m/res

   >[!NOTE]
   >
   >Se i controlli non hanno esito positivo, ulteriori informazioni sui possibili motivi dell&#39;errore in [questa sezione](#monitor-message-presets).

1. Una volta eseguiti i controlli, il predefinito del messaggio ottiene lo stato **[!UICONTROL Active]** . È pronto per essere utilizzato per inviare messaggi.

   <!-- later on, users will be notified in Pulse -->

   ![](../assets/preset-active.png)

## Monitorare i predefiniti per messaggi {#monitor-message-presets}

Tutti i predefiniti per messaggi vengono visualizzati nel menu **[!UICONTROL Channels]** / **[!UICONTROL Message presets]** . Sono disponibili filtri per aiutarti a sfogliare l’elenco (tipo di canale, utente, stato).

![](../assets/preset-filters.png)

I predefiniti per messaggi possono avere i seguenti stati:

* **[!UICONTROL Draft]**: Il predefinito del messaggio è stato salvato come bozza e non è ancora stato inviato. Apri per riprendere la configurazione.
* **[!UICONTROL Processing]**: Il predefinito del messaggio è stato inviato e sta attraversando diverse fasi di verifica.
* **[!UICONTROL Active]**: Il predefinito del messaggio è stato verificato e può essere selezionato per creare i messaggi.
* **[!UICONTROL Failed]**: Uno o più controlli non sono riusciti durante la verifica del predefinito del messaggio.
* **[!UICONTROL De-activated]**: Il predefinito del messaggio viene disattivato. Non può essere utilizzato per creare nuovi messaggi.

Se la creazione di un predefinito di messaggio non riesce, di seguito sono descritti i dettagli di ciascun possibile motivo di errore.

Se si verifica uno di questi errori, contatta il [team di assistenza clienti Adobe](https://helpx.adobe.com/it/enterprise/admin-guide.html/enterprise/using/support-for-experience-cloud.ug.html){target=&quot;_blank&quot;} per ottenere assistenza.

* **Convalida SPF non riuscita**: SPF (Sender Policy Framework) è un protocollo di autenticazione e-mail che consente di specificare gli IP autorizzati che possono inviare e-mail da un determinato sottodominio. Un errore di convalida SPF indica che gli indirizzi IP nel record SPF non corrispondono agli indirizzi IP utilizzati per l’invio di e-mail ai provider di cassette postali.

* **Convalida DKIM non riuscita**: DKIM consente al server destinatario di verificare che il messaggio ricevuto sia stato inviato dal mittente originale del dominio associato e che il contenuto del messaggio originale non sia stato modificato durante il suo percorso. Un errore di convalida DKIM indica che i server di posta riceventi non sono in grado di verificare l’autenticità del contenuto del messaggio e la sua associazione al dominio di invio.

* **Convalida record MX non riuscita**: Un errore di convalida del record MX indica che i server di posta elettronica responsabili dell’accettazione di e-mail in entrata per conto di un determinato sottodominio non sono configurati correttamente.

* **Configurazioni del recapito messaggi non riuscite**: Un errore di configurazione del recapito messaggi può verificarsi a causa di uno dei motivi seguenti:
   * Inserire nell&#39;elenco Bloccati degli IP allocati
   * Nome `helo` non valido
   * E-mail inviate da IP diversi da quelli specificati nel pool IP del predefinito corrispondente
   * Impossibile inviare e-mail alle caselle in entrata dei principali ISP come Gmail e Yahoo

## Modificare i predefiniti per i messaggi

Per modificare un predefinito per messaggi, devi prima disattivarlo per renderlo non disponibile per la creazione di nuovi messaggi (i messaggi pubblicati con questo predefinito non saranno interessati e continueranno a funzionare). Devi quindi duplicare il predefinito per messaggi per creare una nuova versione da usare per creare nuovi messaggi:

1. Accedi all’elenco dei predefiniti per messaggi e disattiva il predefinito per messaggi da modificare.

   ![](../assets/preset-deactivate.png)

1. Duplica il predefinito di messaggio disattivato. All’elenco viene automaticamente aggiunta una copia con lo stato **[!UICONTROL Draft]** .

   ![](../assets/preset-duplicated.png)

1. Apri il predefinito di messaggio duplicato, modificalo in base alle tue esigenze, quindi invia le modifiche. Il predefinito per messaggi eseguirà lo stesso ciclo di convalida del passaggio di [creazione](#create-message-preset).

1. Una volta convalidato, ottiene lo stato **[!UICONTROL Active]** ed è pronto per essere utilizzato per creare nuovi messaggi.

   >[!NOTE]
   >
   >I predefiniti per messaggi disattivati non possono essere eliminati per evitare problemi nei percorsi che utilizzano questi predefiniti per inviare messaggi.

## Video introduttivo{#video-presets}

Scopri come creare i predefiniti per messaggi, come utilizzarli e come delegare un sottodominio e creare un pool IP.

>[!VIDEO](https://video.tv.adobe.com/v/334343?quality=12)
