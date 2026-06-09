---
title: Introduzione all’approvazione di percorsi e campagne
description: Scopri come impostare un processo di approvazione per percorsi e campagne.
role: User
level: Beginner
feature: Approval
exl-id: 92d1439e-5cac-4e7d-85f8-ebf432e9ef7c
TQID: https://experienceleague.adobe.com/dKfstmm0ilHKUATU-sz7c04IZBu2O7Ju-srPPoKJVl4
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: []
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
subfeature_v2: id: bf7a266e-e483-42c6-b5bc-09ca6e49900cid: e30b0a1a-b594-47b8-af94-1e3a2be6df11
source-git-commit: a4e4f5ca5c3eb9dbfb5691cb5de420009ed7e5a5
workflow-type: tm+mt
source-wordcount: 1006
ht-degree: 96%

---

# Introduzione all’approvazione di percorsi e campagne {#send-proofs}

## Introduzione ai criteri di approvazione {#gs}

[!DNL Journey Optimizer] consente di configurare un processo di approvazione che permette ai team di marketing di garantire che le campagne e i percorsi vengano rivisti e approvati da stakeholder appropriati, prima della pubblicazione.

I criteri di approvazione introducono un flusso di lavoro strutturato direttamente all’interno dell’interfaccia utente, eliminando la necessità di mezzi esterni come e-mail o strumenti di gestione delle attività e garantendo che tutte le approvazioni siano gestite e tracciate a livello centrale.

Inoltre, questa funzione offre un controllo migliorato sulla pubblicazione dei percorsi e delle campagne: con il processo di approvazione incorporato in Journey Optimizer, le campagne e i percorsi rimangono in uno stato “bloccato” durante la revisione, garantendo che non si verifichino modifiche o attivazioni involontarie prima che tutte le approvazioni necessarie siano state attuate.

## Prerequisiti {#prerequisites}

Prima di iniziare, assicurati che siano state configurate le autorizzazioni seguenti.

Per approvare e pubblicare percorsi e campagne è necessario concedere agli utenti le autorizzazioni **Approva e pubblica campagne** e **Approva e pubblica percorsi**. [Ulteriori informazioni](../administration/permissions.md)

+++  Scopri come assegnare autorizzazioni relative all’approvazione

1. Nel prodotto **Autorizzazioni**, passa alla scheda **Ruoli** e seleziona il **Ruolo** desiderato.

1. Fai clic su **Modifica** per modificare le autorizzazioni.

1. Aggiungi la risorsa **Campagne**, quindi seleziona **Approva e pubblica campagne** dal menu a discesa.

   ![Assegnare l’autorizzazione di approvazione e pubblicazione delle campagne](assets/permissions_approval.png){zoomable="yes"}

1. Aggiungi la risorsa **Percorsi**, quindi seleziona **Approva e pubblica percorsi** dal menu a discesa.

   ![Assegnare l’autorizzazione di approvazione e pubblicazione dei percorsi](assets/permissions_approval_2.png){zoomable="yes"}

1. Fai clic su **Salva** per applicare le modifiche.

Le autorizzazioni degli utenti già assegnati a questo ruolo verranno aggiornate automaticamente.

1. Per assegnare questo ruolo a nuovi utenti, passa alla scheda **Utenti** nella dashboard **Ruoli** e fai clic su **Aggiungi utente**.

1. Immetti il nome o l’indirizzo e-mail dell’utente o sceglilo dall’elenco e fai clic su **Salva**.

1. Se l’utente non è già stato creato in precedenza, consulta [questa documentazione](https://experienceleague.adobe.com/it/docs/experience-platform/access-control/abac/permissions-ui/users).

L’utente riceverà un’e-mail con istruzioni per accedere all’istanza.

+++

## Panoramica sul processo di approvazione {#process}

Il processo di approvazione globale è il seguente:

![Flusso del processo di approvazione](assets/approval-process.png){zoomable="yes"}

1. **Configurazione dei criteri di approvazione**

   Un utente amministratore crea un criterio di approvazione, definendo le condizioni in base alle quali il criterio deve essere applicato a percorsi o campagne. Ad esempio, puoi creare un criterio di approvazione che richiede che tutte le campagne pianificate create da un determinato utente siano approvate prima di essere attivate. [Scopri come creare i criteri di approvazione](approval-policies.md)

1. **Invio campagna/percorso per l’approvazione**

   I creatori di campagne/percorsi creano un percorso o una campagna e li inviano per l’approvazione. La campagna o il percorso entra in stato &quot;In revisione&quot;, durante il quale non è possibile apportare modifiche a meno che la richiesta non venga annullata. [Informazioni su come richiedere l’approvazione](request-approval.md)

   >[!NOTE]
   >
   >Le campagne e i percorsi devono essere inviati per l’approvazione solo se esiste un criterio di approvazione. In caso contrario, il creatore può pubblicare direttamente la campagna o il percorso senza richiedere l’approvazione.

1. **Revisione e approvazione**

   L’approvatore o gli approvatori definiti nei criteri di approvazione applicabili al percorso o alla campagna ricevono una notifica. Questi possono esaminare il contenuto del percorso o della campagna, il pubblico e le impostazioni. Se sono necessarie modifiche, l’approvatore le richiede, restituendo la campagna nello stato di “Bozza” per le revisioni. Se sono pronti, possono attivare e lanciare il percorso o la campagna. [Informazioni su come revisionare e approvare una richiesta](review-approve-request.md)

## Monitorare le richieste di approvazione {#monitor}

Puoi monitorare tutte le richieste di approvazione e modifica inviate per un determinato percorso o campagna. A questo scopo, fai clic sull’icona **[!UICONTROL Mostra Audit Trail]** nella sezione in alto a destra dell’area di lavoro del percorso o nella schermata di revisione della campagna.

![Audit trail delle richieste di approvazione](assets/monitor-requests.png)

## Domande frequenti {#faq}

+++È necessario creare un criterio di approvazione per ogni campagna o percorso?

No. I criteri di approvazione sono condizionali. È necessario creare un criterio solo se desideri applicare la revisione per un set specifico di campagne o percorsi (ad esempio, tutte le campagne pianificate create da un determinato team). Se a una campagna o a un percorso non applichi alcun criterio, l’autore può pubblicare direttamente senza richiedere l’approvazione.

+++

+++Cosa succede se l’approvatore non è disponibile?

La richiesta rimane “In revisione” finché un approvatore non vi agisce. Puoi annullare la richiesta (riportando l’elemento in stato di “Bozza”) e inviarla nuovamente quando sarà disponibile l’approvatore corretto. Gli amministratori possono inoltre aggiornare il criterio di approvazione per aggiungere altri approvatori.

+++

+++Posso modificare una campagna o un percorso mentre è in attesa di approvazione?

No. Una volta inviata per l’approvazione, la campagna o il percorso si trova in uno stato “In revisione” bloccato. Per apportare modifiche, il creatore o un approvatore deve prima annullare la richiesta. L’elemento viene riportato in stato di “Bozza” e può essere modificato prima del nuovo invio.

+++

+++Non riesco a visualizzare l’autorizzazione Approva e pubblica nel menu a discesa; cosa devo controllare?

Accertati di aggiungere prima la risorsa corretta. L’autorizzazione **Approva e pubblica campagne** richiede l’aggiunta della risorsa **Campagne** al ruolo e **Approva e pubblica percorsi** richiede la risorsa **Percorsi**. Entrambe devono essere aggiunte separatamente. [Scopri come assegnare autorizzazioni relative all’approvazione](#prerequisites)

+++

+++In che modo [!DNL Journey Optimizer] determina quale criterio di approvazione applicare nel caso in cui ne corrisponda più di uno?

Quando più criteri di approvazione attivi possono essere applicati allo stesso percorso o campagna, ha la priorità spetta al criterio **attivato più di recente**. I gruppi di utenti approvatori definiti in tale criterio sono quelli notificati e che gestiscono la richiesta.

[Ulteriori informazioni](approval-policies.md#multiple-policies)

+++

+++Se un richiedente appartiene a più gruppi di utenti, può scegliere a quale gruppo inviare la richiesta di approvazione?

No. I richiedenti non possono selezionare manualmente quale gruppo di utenti riceve o instrada la richiesta di approvazione. I gruppi di utenti specificati nel criterio di approvazione applicato, in base alla [precedenza dei criteri](approval-policies.md#multiple-policies), vengono notificati automaticamente.

+++

## Risorse aggiuntive

* **[Creare criteri di approvazione](approval-policies.md)**: scopri come impostare i criteri di approvazione da applicare nei flussi di lavoro di revisione per le campagne e i percorsi.
* **[Richiedere l’approvazione](request-approval.md)**: scopri come inviare contenuti per l’approvazione e tenere traccia dello stato di approvazione.
* **[Rivedere e approvare le richieste](review-approve-request.md)**: scopri come rivedere, approvare o rifiutare le richieste di approvazione in qualità di approvatore.
* **[Simula varianti di contenuto](simulate-sample-input.md)** - Fai clic su **[!UICONTROL Simula contenuto]** per testare le varianti di contenuto con dati di input di esempio, generazione automatica di IA o utenti simulati. Fai clic su **[!UICONTROL Simula contenuto]**, quindi seleziona **[!UICONTROL Simula contenuto (profili AEP)]** dal menu a discesa per visualizzare l&#39;anteprima con i profili di test.
