---
solution: Journey Optimizer
product: journey optimizer
title: Linee guida CNIL sui pixel di tracciamento e-mail
description: Scopri le linee guida aggiornate di CNIL sui pixel di tracciamento delle e-mail e i controlli Adobe Journey Optimizer che possono supportare le attività di conformità.
feature: Privacy, Consent Management
topic: Content Management
role: User
level: Intermediate
keywords: CNIL, tracciamento, pixel, e-mail, consenso, rinuncia, privacy
source-git-commit: 24d6a17d57ede317d3f04add2fd01bd3ff0ab9af
workflow-type: tm+mt
source-wordcount: '1490'
ht-degree: 2%

---


# Informazioni sulle linee guida aggiornate di CNIL sui pixel di tracciamento e-mail {#cnil-pixel-tracking}

>[!BEGINSHADEBOX]

**In questa pagina:** Scopri le raccomandazioni CNIL di aprile 2026 sui pixel di tracciamento delle e-mail e scopri i controlli Adobe Journey Optimizer (attivazione/disattivazione del tracciamento, tracciamento a livello di collegamento, gestione del consenso, meccanismi di rinuncia ed eliminazione) che possono supportare le tue attività di conformità.

>[!ENDSHADEBOX]

>[!NOTE]
>
>Questa pagina ha solo scopo informativo. Non si tratta di una consulenza legale e non garantisce il rispetto delle leggi applicabili da parte dell&#39;utente. Le funzionalità dei prodotti Adobe Journey Optimizer descritte di seguito sono elementi costitutivi che, configurati e gestiti in modo appropriato, possono supportare un’implementazione conforme. Ciascun cliente è responsabile della determinazione e del rispetto degli obblighi derivanti dalla legge applicabile.

## Panoramica {#overview}

Il 14 aprile 2026 la *Commission Nationale de l&#39;Informatique et des Libertés* (CNIL), l&#39;autorità francese per la protezione dei dati, ha pubblicato una [raccomandazione sull&#39;uso dei pixel di tracciamento nelle e-mail](https://www.cnil.fr/sites/default/files/2026-04/recommandation-pixels_de_suivi.pdf). La guida chiarisce quando è necessario il consenso ed evidenzia l’importanza di pratiche di consenso appropriate per il tracciamento dei pixel dell’e-mail. Questo criterio potrebbe influire sulle pratiche di invio per qualsiasi entità che distribuisce e-mail agli abbonati con sede in Francia.

CNIL ha previsto un periodo di tre mesi dalla data della raccomandazione alle aziende di informare i propri destinatari e-mail (&quot;utenti&quot;) della presenza dei pixel di tracciamento, del loro scopo e del diritto degli utenti di rinunciare. Durante questo periodo di transizione, i clienti devono avvisare gli utenti in merito al tracciamento dei pixel e, se necessario, fornire una rinuncia. CNIL dovrebbe iniziare le attività di applicazione dopo il 14 luglio 2026.

Poiché CNIL e altri enti normativi chiariscono le linee guida sul tracciamento dei pixel e dei problemi correlati, Adobe continuerà a monitorare gli aggiornamenti e a informare i clienti sulle funzionalità tecniche dei prodotti Adobe che supportano il marketing via e-mail, incluso Adobe Journey Optimizer.

Adobe Journey Optimizer fornisce controlli che possono aiutare i clienti a gestire il tracciamento delle aperture a livello di consegna. I clienti sono responsabili della determinazione dei propri obblighi di conformità in base alle linee guida CNIL applicabili e ad altre leggi, ma queste funzionalità possono supportare le attività di conformità dei clienti.

## Cos’è un pixel di tracciamento e-mail {#tracking-pixel}

Un pixel di tracciamento e-mail è un’immagine trasparente 1x1 incorporata nel HTML di un’e-mail. Quando il client e-mail del destinatario carica l’immagine, il pixel invia un ping a un server che registra dati quali marca temporale, tipo di dispositivo, client e-mail e, a volte, un indirizzo IP per la posizione approssimativa. Il registro viene quindi associato al record di un destinatario, consentendo agli addetti al marketing di verificare se è stata aperta un’e-mail.

## Assistenza clienti {#support}

I clienti che necessitano di assistenza per implementare le modifiche descritte qui sopra possono interagire con il loro ecosistema Adobe esistente. Per domande tecniche sulle funzionalità Adobe a cui si fa riferimento, contatta il tuo Customer Success Manager o Technical Account Manager.

## Funzionalità Adobe Journey Optimizer relative al tracciamento e-mail {#ajo-functionality}

Adobe Journey Optimizer fornisce diversi controlli nativi per aiutare i clienti a risolvere gli elementi della guida CNIL. Le sezioni seguenti descrivono le funzionalità del prodotto rilevanti.

### Classificazione del tipo di e-mail {#email-type}

In Adobe Journey Optimizer, ogni configurazione del canale e-mail è classificata come Marketing o Transazionale. Questa classificazione determina se è necessario il consenso dell’abbonato prima dell’invio.

* **E-mail marketing**: comunicazioni promozionali inviate agli abbonati che hanno prestato il consenso. È necessario il consenso dell’utente. Queste e-mail rispettano automaticamente le preferenze di eliminazione e rinuncia.
* **E-mail transazionali**: comunicazioni non commerciali (ad esempio, conferme d&#39;ordine, reimpostazioni password). Questi possono essere inviati a profili che hanno annullato l’abbonamento alle comunicazioni di marketing, in base alle leggi applicabili.

Il tipo di e-mail è impostato a livello di configurazione del canale. Durante l’authoring di un’e-mail in un percorso o in una campagna, gli autori devono selezionare una configurazione di canale il cui tipo di e-mail corrisponda alla natura della comunicazione. Questa classificazione indica quali controlli del consenso vengono applicati prima della consegna.

### Apri controlli di tracciamento {#open-tracking}

Adobe Journey Optimizer consente agli esperti di marketing di controllare il tracciamento delle aperture (ovvero, il pixel 1x1) a livello di singolo messaggio. Durante la creazione di un messaggio e-mail in un percorso o in una campagna, nel pannello delle proprietà del messaggio sono disponibili due opzioni di tracciamento:

* **[!UICONTROL Apertura e-mail]**: controlla se il pixel di tracciamento aperto è incluso nell&#39;e-mail. Questa opzione è abilitata per impostazione predefinita.
* **[!UICONTROL Fai clic sull&#39;e-mail]**: controlla se i clic sui collegamenti sono tracciati. Anche questa opzione è attivata per impostazione predefinita.

Per disabilitare il tracciamento delle aperture per un messaggio e-mail specifico, deseleziona l&#39;opzione **[!UICONTROL Aperture messaggi e-mail]** durante la creazione del messaggio. Se è disabilitata, l’opzione impedisce la raccolta dei dati di tracciamento aperti per quella consegna. Per le organizzazioni che inviano messaggi agli abbonati francesi, controlla le impostazioni di tracciamento aperte per tutti i percorsi e le campagne attivi prima della data di applicazione.

<!--
EDITORIAL NOTE – ENGINEERING CONFIRMATION NEEDED before publish:
Clarify whether unchecking "Email opens" fully removes the 1x1 tracking pixel from the delivered HTML, or whether the pixel is still present in the HTML but open data is suppressed at the data processing layer only. The current wording ("prevents open tracking data from being collected") is intentionally neutral. If the pixel is removed: update to state this explicitly. If the pixel remains but data is not processed: reword to make that distinction clear, to avoid misleading customers seeking CNIL compliance.
-->

[Scopri come tenere traccia dei messaggi](../email/message-tracking.md)

### Gestione del tracciamento a livello di collegamento {#link-tracking}

Oltre all’attivazione/disattivazione del tracciamento dell’apertura per messaggio, Adobe Journey Optimizer E-mail Designer fornisce un controllo granulare sugli URL tracciati. Tramite il pannello Collegamenti nel Designer e-mail, gli autori possono visualizzare tutti gli URL tracciati in un messaggio e impostare la modalità di tracciamento per ogni singolo collegamento.

Le modalità di tracciamento disponibili per ogni collegamento includono:

* **Tracciato**: attiva il tracciamento su questo URL.
* **Rinuncia**: designa questo URL come URL di rinuncia o di annullamento dell&#39;abbonamento.
* **Pagina mirror**: designa questo URL come collegamento di pagina mirror.
* **Mai**: il tracciamento non viene mai attivato per questo URL, indipendentemente dalle impostazioni a livello di messaggio.

L&#39;impostazione di collegamenti specifici a **Mai** può contribuire a garantire che alcuni URL non vengano tracciati anche quando è abilitato il tracciamento a livello di messaggio.

### Acquisizione e gestione del consenso {#consent-management}

Adobe Journey Optimizer gestisce il consenso tramite lo schema Consenso e preferenze di Adobe Experience Platform (AEP). Le preferenze di consenso vengono memorizzate a livello di profilo e applicate automaticamente durante l’esecuzione del percorso e della campagna.

Gli attributi di consenso chiave rilevanti per il tracciamento e-mail includono:

* **`consents.marketing.email.val`**: campo del consenso e-mail marketing primario. Il valore `y` indica il consenso; `n` indica la rinuncia. Per impostazione predefinita, un valore vuoto viene trattato come consenso (questa impostazione predefinita può essere modificata all’onboarding).

### Meccanismi di rinuncia e di ritiro {#opt-out}

Adobe Journey Optimizer offre diversi meccanismi per consentire agli abbonati di rinunciare alle comunicazioni e gestire le loro preferenze, che aggiornano tutti gli attributi di consenso del profilo in Adobe Experience Platform.

**Annulla iscrizione con un solo clic (intestazione e-mail)**

Quando l&#39;opzione **[!UICONTROL Abilita annullamento iscrizione a mailing list]** è attivata nella configurazione del canale e-mail, un URL con un solo clic e un indirizzo di posta vengono aggiunti automaticamente all&#39;intestazione dell&#39;e-mail. I destinatari possono scegliere di rinunciare direttamente al client e-mail senza fare clic sul corpo dell’e-mail. Questa opzione è attivata per impostazione predefinita per le nuove configurazioni di canale.

**Rinuncia con un solo clic (corpo dell&#39;e-mail)**

Gli autori possono inserire un collegamento di rinuncia con un solo clic direttamente nel contenuto dell’e-mail utilizzando E-mail Designer. Quando un destinatario fa clic su questo collegamento, la sua preferenza viene aggiornata immediatamente. L’ambito della rinuncia può essere:

* **Livello canale**: rifiuta il profilo di tutte le comunicazioni e-mail future nel canale.
* **Livello identità**: rifiuta l&#39;indirizzo e-mail specifico utilizzato solo nel messaggio corrente.

**Centro preferenze tramite pagine di destinazione di AJO**

La funzionalità di pagina di destinazione nativa di Adobe Journey Optimizer consente alle organizzazioni di creare centri di preferenze in cui gli abbonati possono gestire le loro preferenze di comunicazione e tracciamento. Quando un abbonato invia un modulo del centro preferenze, le sue scelte vengono riportate nei suoi attributi di profilo AEP nel gruppo di campi Consenso e preferenze.

Per gli scenari di conformità CNIL, è possibile collegare una pagina di destinazione del centro preferenze dal piè di pagina dell’e-mail (diverso dal collegamento per annullare l’abbonamento) in modo che i destinatari possano gestire le loro preferenze di tracciamento indipendentemente dal loro stato di abbonamento.

### Elaborazione e applicazione del consenso {#consent-enforcement}

Quando un destinatario rinuncia tramite uno dei meccanismi di cui sopra, si verifica quanto segue:

* L&#39;attributo di consenso del profilo (`consents.marketing.email.val`) è stato aggiornato a `n` in Adobe Experience Platform.
* Il profilo viene immediatamente escluso da futuri invii e-mail di marketing in percorsi e campagne.
* Le informazioni di rinuncia vengono memorizzate nel set di dati del servizio di consenso di AEP.
* Journey Optimizer esegue un controllo del consenso a livello di canale prima di ogni invio, garantendo che i profili con rinuncia non ricevano comunicazioni di marketing.

### Criteri di consenso {#consent-policies}

Le organizzazioni possono creare e applicare i criteri di consenso in Adobe Journey Optimizer per garantire che solo i profili che soddisfano specifici criteri di consenso ricevano le comunicazioni. I criteri di consenso possono essere associati alle configurazioni del canale tramite azioni di marketing.

[Scopri come utilizzare i criteri di consenso](../action/consent.md)

### Elenco di soppressione e richiesta {#suppression}

Adobe Journey Optimizer gestisce automaticamente un elenco di soppressione che include indirizzi e-mail con conseguenti mancati recapiti permanenti, mancati recapiti non permanenti o reclami di spam. I profili nell’elenco di soppressione sono esclusi dagli invii di marketing futuri.

L’API REST per l’eliminazione di Journey Optimizer fornisce un controllo programmatico aggiuntivo sui messaggi in uscita, consentendo alle organizzazioni di gestire l’eliminazione e di inserire nell&#39;elenco Consentiti il comportamento tramite API.

<!--
EDITORIAL NOTE – ENGINEERING CONFIRMATION NEEDED before publish:
AJO has no native equivalent of Campaign v8's "lastPixelRefusalDate" field or re-solicitation typology rule. If re-solicitation governance for pixel consent refusal is required, customers would likely need to: (a) create a custom XDM date field to capture the pixel refusal date, and (b) build an AEP audience that filters out profiles where that date falls within the last six months, then use that audience as a suppression filter in campaigns/journeys. Confirm with Engineering: (1) whether this guidance should be included in this article, and (2) whether any native AJO improvements are planned in this area.
-->

### Generazione di rapporti {#reporting}

Il reporting sulle e-mail di Adobe Journey Optimizer fornisce metriche di apertura e clic tramite rapporti live e rapporti Customer Journey Analytics. Quando il tracciamento **[!UICONTROL E-mail apre]** è disabilitato per un messaggio, i dati aperti non vengono raccolti per tale consegna; il reporting rifletterà solo i clic e altri segnali di coinvolgimento.

## Riferimenti alla documentazione {#references}

Per ulteriori informazioni sul tracciamento e-mail e sulla gestione del consenso in Adobe Journey Optimizer, consulta la documentazione di seguito.

| Argomento | Documentazione di riferimento |
|-------|------------------------|
| Abilitare e disabilitare il tracciamento delle aperture | [Tracciamento messaggi](../email/message-tracking.md) |
| Gestione della rinuncia e-mail | [Gestione della rinuncia alle e-mail](../email/email-opt-out.md) |
| Annullamento iscrizione a mailing list (intestazione e-mail) | [Configura annullamento sottoscrizione a elenco](../email/list-unsubscribe.md) |
| Pagine di destinazione del centro preferenze | [Casi d’uso per pagine di destinazione](../landing-pages/lp-use-cases.md) |
| Gestione del consenso e della rinuncia | [Gestione rinuncia](opt-out.md) |
| Criteri di consenso | [Utilizzare i criteri di consenso](../action/consent.md) |
| Configurazione del canale e-mail | [Configura impostazioni e-mail](../email/email-settings.md) |
| Elenco di soppressione | [Gestire l&#39;elenco di soppressione](../configuration/manage-suppression-list.md) |
