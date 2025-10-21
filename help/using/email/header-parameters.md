---
solution: Journey Optimizer
product: journey optimizer
title: Configurare i parametri di intestazione e-mail
description: Scopri come impostare i parametri di intestazione e-mail a livello di configurazione del canale
feature: Email, Surface
topic: Administration
role: Admin
level: Experienced
keywords: impostazioni, e-mail, configurazione
exl-id: e1556c25-9c79-4362-a5a9-0a46425fa8d9
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '712'
ht-degree: 90%

---

# Parametri per intestazione {#email-header}

Durante la configurazione di una nuova [configurazione del canale e-mail](email-settings.md), nella sezione **[!UICONTROL Parametri intestazione]**, immetti i nomi del mittente e gli indirizzi e-mail associati al tipo di e-mail inviate utilizzando tale configurazione.

>[!NOTE]
>
>Per un maggiore controllo sulle impostazioni e-mail, puoi personalizzare i parametri dell’intestazione. [Ulteriori informazioni](../email/surface-personalization.md#personalize-header)

* **[!UICONTROL Dal nome]**: il nome del mittente, ad esempio il nome del tuo brand.
* **[!UICONTROL Dal prefisso e-mail]**: l’indirizzo e-mail che desideri utilizzare per le comunicazioni.
* **[!UICONTROL Rispondi a nome]**: il nome che verrà utilizzato quando il destinatario farà clic sul pulsante **Rispondi** nel software di client e-mail.
* **[!UICONTROL Rispondi a e-mail]**: l’indirizzo e-mail che verrà utilizzato quando il destinatario farà clic sul pulsante **Rispondi** nel software di client e-mail. [Ulteriori informazioni](#reply-to-email)
* **[!UICONTROL Prefisso e-mail di errore]**: tutti gli errori generati dagli ISP dopo alcuni giorni dalla consegna della mail (mancati recapiti asincroni) vengono ricevuti su questo indirizzo. Su questo indirizzo vengono inoltre ricevute le notifiche fuori sede e le risposte alle richieste di verifica.

  Se desideri ricevere le notifiche fuori sede e le risposte di richiesta di verifica su un indirizzo e-mail specifico non delegato ad Adobe, è necessario impostare un [processo di inoltro](#forward-email). In tal caso, assicurati di disporre di una soluzione manuale o automatizzata pronta per elaborare le e-mail che verranno inviate a questa casella in entrata.

>[!NOTE]
>
>Gli indirizzi **[!UICONTROL Da prefisso e-mail]** e **[!UICONTROL Prefisso e-mail di errore]** utilizzano il [sottodominio delegato](../configuration/about-subdomain-delegation.md) corrente selezionato per inviare l’e-mail. Ad esempio, se il sottodominio delegato è *marketing.luma.com*:
>
>* Immetti *contatto* come **[!UICONTROL Da prefisso e-mail]**: l’e-mail del mittente è *contatto@marketing.luma.com*.
>* Immetti *errore* come **[!UICONTROL Prefisso e-mail di errore]**: l’indirizzo di errore è *errore@marketing.luma.com*.

![](assets/preset-header.png){width="80%"}

>[!NOTE]
>
>Gli indirizzi devono iniziare con una lettera (A-Z) e possono contenere solo caratteri alfanumerici. È inoltre possibile utilizzare i caratteri trattino basso `_`, punto `.` e trattino `-`.

## Rispondi all’e-mail {#reply-to-email}

Quando definisci l’indirizzo per **[!UICONTROL Rispondi all’e-mail]**, puoi specificare qualsiasi indirizzo e-mail a condizione che sia valido, nel formato corretto e senza errori di battitura.

La casella in entrata utilizzata per le risposte riceverà tutte le e-mail di risposta, ad eccezione delle notifiche fuori sede e delle risposte di richiesta di verifica, ricevute all’indirizzo **E-mail di errore**.

Per garantire una corretta gestione delle risposte, segui i consigli seguenti:

* Assicurati che la casella in entrata dedicata disponga di una capacità di ricezione sufficiente per ricevere tutte le e-mail di risposta inviate utilizzando la configurazione e-mail. Se la casella in entrata restituisce mancati recapiti, alcune risposte da parte della clientela potrebbero non essere ricevute.

* Le risposte devono essere elaborate tenendo presenti gli obblighi di privacy e conformità, in quanto possono contenere informazioni di identificazione personale (PII).

* Non contrassegnare i messaggi come spam nella casella in entrata delle risposte, in quanto ciò influirà su tutte le altre risposte inviate a questo indirizzo.

Inoltre, quando definisci l’indirizzo per **[!UICONTROL Rispondi all’e-mail]**, assicurati di utilizzare un sottodominio con una configurazione di record MX valida, altrimenti l’elaborazione della configurazione e-mail non andrà a buon fine.

Se ricevi un errore durante l’invio della configurazione e-mail, significa che il record MX non è configurato per il sottodominio dell’indirizzo inserito. Contatta l’amministratore per configurare il record MX corrispondente o utilizza un altro indirizzo con una configurazione di record MX valida.

>[!NOTE]
>
>Se il sottodominio dell&#39;indirizzo immesso è un dominio [completamente delegato](../configuration/delegate-subdomain.md#full-subdomain-delegation) ad Adobe, contatta il rappresentante Adobe.

## Inoltra l’e-mail {#forward-email}

Per inoltrare a un indirizzo e-mail specifico tutte le e-mail ricevute da [!DNL Journey Optimizer] per il sottodominio delegato, contatta l’Assistenza clienti di Adobe.

>[!NOTE]
>
>Se il sottodominio utilizzato per l’indirizzo **[!UICONTROL Rispondi all’e-mail]** non è delegato ad Adobe, l’inoltro per tale indirizzo non può funzionare.

Dovrai fornire:

* L’indirizzo e-mail di inoltro desiderato. Il dominio dell’indirizzo e-mail di inoltro non può corrispondere ad alcun sottodominio delegato ad Adobe.
* Nome della tua sandbox.
* Il nome della configurazione o il sottodominio per cui verrà utilizzato l’indirizzo e-mail di inoltro.
  <!--* The current **[!UICONTROL Reply to (email)]** address or **[!UICONTROL Error email]** address set at the channel configuration level.-->

>[!NOTE]
>
>Può essere presente un solo indirizzo e-mail di inoltro per sottodominio. Di conseguenza, se più configurazioni utilizzano lo stesso sottodominio, è necessario utilizzare lo stesso indirizzo e-mail di inoltro per tutte.

L’indirizzo e-mail di inoltro è configurato da Adobe. Questa operazione può richiedere da 3 a 4 giorni.

Al termine, tutti i messaggi ricevuti agli indirizzi **[!UICONTROL Rispondi all’e-mail]** e **E-mail di errore**, così come tutte le e-mail inviate agli indirizzi **Da e-mail**, vengono inoltrati all’indirizzo e-mail specifico fornito.

>[!NOTE]
>
>Per impostazione predefinita, se l’inoltro non è abilitato, le e-mail inviate direttamente all’indirizzo **Da e-mail** saranno eliminate.
