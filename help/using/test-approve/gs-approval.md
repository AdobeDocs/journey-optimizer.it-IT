---
title: Introduzione all’approvazione di percorsi e campagne
description: Scopri come impostare un processo di approvazione per percorsi e campagne.
role: User
level: Beginner
feature: Approval
exl-id: 92d1439e-5cac-4e7d-85f8-ebf432e9ef7c
source-git-commit: e6cac6aff79b30a308be480319902f478436391d
workflow-type: tm+mt
source-wordcount: '860'
ht-degree: 58%

---

# Introduzione all’approvazione di percorsi e campagne {#send-proofs}

## Introduzione ai criteri di approvazione {#gs}

[!DNL Journey Optimizer] consente di impostare un processo di approvazione che consenta ai team di marketing di assicurarsi che le campagne e i percorsi vengano esaminati e approvati dalle parti interessate prima della pubblicazione.

I criteri di approvazione introducono un flusso di lavoro strutturato direttamente all’interno dell’interfaccia utente, eliminando la necessità di mezzi esterni come e-mail o strumenti di gestione delle attività e garantendo che tutte le approvazioni siano gestite e tracciate a livello centrale.

Inoltre, questa funzione offre un controllo migliorato sulla pubblicazione dei percorsi e delle campagne: con il processo di approvazione incorporato in Journey Optimizer, le campagne e i percorsi rimangono in uno stato “bloccato” durante la revisione, garantendo che non si verifichino modifiche o attivazioni involontarie prima che tutte le approvazioni necessarie siano state attuate.

## Prerequisiti {#prerequisites}

Prima di iniziare, assicurati che siano state configurate le autorizzazioni seguenti.

Per approvare e pubblicare percorsi e campagne, è necessario concedere agli utenti le autorizzazioni **Approva e pubblica campagne** e **Approva e pubblica Percorsi**. [Ulteriori informazioni](../administration/permissions.md)

+++  Scopri come assegnare le autorizzazioni relative all’approvazione

1. Nel prodotto **Autorizzazioni**, passa alla scheda **Ruoli** e seleziona il **Ruolo** desiderato.

1. Fai clic su **Modifica** per modificare le autorizzazioni.

1. Aggiungi la risorsa **Campagne**, quindi seleziona **Approva e pubblica campagne** dal menu a discesa.

   ![Assegna l&#39;autorizzazione di approvazione e pubblicazione delle campagne](assets/permissions_approval.png){zoomable="yes"}

1. Aggiungi la risorsa **Percorsi**, quindi seleziona **Approva e pubblica Percorsi** dal menu a discesa.

   ![Assegna l&#39;autorizzazione di approvazione e pubblicazione ai Percorsi](assets/permissions_approval_2.png){zoomable="yes"}

1. Fai clic su **Salva** per applicare le modifiche.

Le autorizzazioni degli utenti già assegnati a questo ruolo verranno aggiornate automaticamente.

1. Per assegnare questo ruolo a nuovi utenti, passa alla scheda **Utenti** nella dashboard **Ruoli** e fai clic su **Aggiungi utente**.

1. Immetti il nome o l’indirizzo e-mail dell’utente o sceglilo dall’elenco e fai clic su **Salva**.

1. Se l&#39;utente non è stato creato in precedenza, consulta [questa documentazione](https://experienceleague.adobe.com/it/docs/experience-platform/access-control/abac/permissions-ui/users).

L’utente riceverà un’e-mail con istruzioni per accedere all’istanza.

+++

## Panoramica sul processo di approvazione {#process}

Il processo di approvazione globale è il seguente:

![Flusso del processo di approvazione](assets/approval-process.png){zoomable="yes"}

1. **Configurazione dei criteri di approvazione**

   Un utente amministratore crea un criterio di approvazione, definendo le condizioni in cui il criterio deve essere applicato a percorsi o campagne. Ad esempio, puoi creare un criterio di approvazione che richieda l’approvazione prima dell’attivazione di tutte le campagne pianificate create da un determinato utente. [Scopri come creare i criteri di approvazione](approval-policies.md)

1. **Invio campagna/percorso per l’approvazione**

   I creatori di campagne/percorsi creano un percorso o una campagna e lo inviano per l’approvazione. La campagna o il percorso entra in stato &quot;In revisione&quot;, durante il quale non è possibile apportare modifiche a meno che la richiesta non venga annullata. [Informazioni su come richiedere l’approvazione](request-approval.md)

   >[!NOTE]
   >
   >Le campagne e i percorsi devono essere inviati per l’approvazione solo se esiste un criterio di approvazione. In caso contrario, il creatore può pubblicare direttamente la campagna o il percorso senza richiedere l’approvazione.

1. **Revisione e approvazione**

   L’approvatore o gli approvatori definiti nei criteri di approvazione applicabili al percorso o alla campagna ricevono una notifica. Questi possono esaminare il contenuto del percorso o della campagna, il pubblico e le impostazioni. Se sono necessarie modifiche, l’approvatore le richiede, restituendo la campagna nello stato di “Bozza” per le revisioni. Se sono pronti, possono attivare e lanciare il percorso o la campagna. [Informazioni su come revisionare e approvare una richiesta](review-approve-request.md)

## Monitorare le richieste di approvazione {#monitor}

Puoi monitorare tutte le richieste di approvazione e modifica inviate per un determinato percorso o campagna. A questo scopo, fai clic sull’icona **[!UICONTROL Mostra Audit Trail]** nella sezione in alto a destra dell’area di lavoro del percorso o nella schermata di revisione della campagna.

![Audit trail richieste di approvazione](assets/monitor-requests.png)

## Domande frequenti {#faq}

+++È necessario creare un criterio di approvazione per ogni campagna o percorso?

No. I criteri di approvazione sono condizionali. È necessario creare un criterio solo se si desidera imporre la revisione per un set specifico di campagne o percorsi (ad esempio, tutte le campagne pianificate create da un team specifico). Se a una campagna o a un percorso non si applica alcun criterio, l’autore può pubblicare direttamente senza richiedere l’approvazione.

+++

+++Cosa succede se l&#39;approvatore non è disponibile?

La richiesta rimane &quot;In revisione&quot; finché un approvatore non vi agisce. È possibile annullare la richiesta (restituendo l&#39;elemento a &quot;Bozza&quot;) e inviarla nuovamente quando è disponibile l&#39;approvatore corretto. Gli amministratori possono inoltre aggiornare i criteri di approvazione per aggiungere altri approvatori.

+++

+++Posso modificare una campagna o un percorso mentre è in attesa di approvazione?

No. Una volta inviata per l’approvazione, la campagna o il percorso si trova in uno stato &quot;In revisione&quot; bloccato. Per apportare modifiche, il creatore o un approvatore deve prima annullare la richiesta. L&#39;elemento torna a &quot;Bozza&quot; e può essere modificato prima di inviarlo di nuovo.

+++

+++Non vedo l’autorizzazione Approva e pubblica nel menu a discesa — cosa devo controllare?

Accertati di aggiungere prima la risorsa corretta. L&#39;autorizzazione **Approva e pubblica campagne** richiede l&#39;aggiunta della risorsa **Campagne** al ruolo e **Approva e pubblica Percorsi** richiede la risorsa **Percorsi**. Entrambi devono essere aggiunti separatamente. [Scopri come assegnare le autorizzazioni relative all&#39;approvazione](#prerequisites)

+++

## Risorse aggiuntive

* **[Creare criteri di approvazione](approval-policies.md)**: scopri come impostare i criteri di approvazione da applicare nei flussi di lavoro di revisione per le campagne e i percorsi.
* **[Richiedere l’approvazione](request-approval.md)**: scopri come inviare contenuti per l’approvazione e tenere traccia dello stato di approvazione.
* **[Rivedere e approvare le richieste](review-approve-request.md)**: scopri come rivedere, approvare o rifiutare le richieste di approvazione in qualità di approvatore.
* **[Simulare con input di esempio](simulate-sample-input.md)**: scopri come testare e convalidare il contenuto utilizzando i dati del profilo di esempio.
