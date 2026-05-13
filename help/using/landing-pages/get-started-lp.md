---
solution: Journey Optimizer
product: journey optimizer
title: Introduzione alle pagine di destinazione
description: Informazioni sulle pagine di destinazione in Journey Optimizer
feature: Landing Pages, Subscriptions
topic: Content Management
role: User
level: Beginner
keywords: destinazione, pagina di destinazione, inizio, inizia
exl-id: 0da96e32-52ad-4cc3-bac4-844b1f39ed16
TQID: https://experienceleague.adobe.com/wr4XGNostKoN8jZ50VRAQPoGg9tsNhMOyJGEt1mASso
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4ebid: dc22c819-3f29-4e91-8b7d-5c6719831141id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2: id: b19d9237-76be-466d-a869-aacf2d72205fid: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 712
ht-degree: 100%

---

# Introduzione alle pagine di destinazione {#get-started-lp}

Una pagina di destinazione è una pagina web autonoma a cui viene indirizzato un utente dopo aver fatto clic da un’e-mail, un sito web, un annuncio pubblicitario o qualsiasi altra posizione digitale.

[!DNL Journey Optimizer] consente di creare e progettare pagine di destinazione per indirizzare gli utenti a moduli online in cui possono acconsentire o rinunciare alla ricezione delle comunicazioni o a un servizio specifico, ad esempio una newsletter.

➡️ [Questo video offre ulteriori informazioni sulla configurazione delle iscrizioni e sulla creazione di pagine di destinazione](#video)

## Quando utilizzare le pagine di destinazione {#when-to-use}

Utilizza le pagine di destinazione quando desideri:

* Consentire alla clientela di **dare il consenso o rinunciare** a comunicazioni di marketing o a un servizio o newsletter specifici da un collegamento in un’e-mail o in una campagna, inclusi gli elenchi di iscrizioni a servizi mirati. [Ulteriori informazioni](lp-use-cases.md#subscription-to-a-service)
* **Ottenere il consenso** prima di inviare comunicazioni e inviare un’**e-mail di conferma** al momento del consenso o della rinuncia. [Ulteriori informazioni](lp-use-cases.md#send-confirmation-email)
* **Acquisire o aggiornare i dati del profilo** utilizzando i moduli nelle pagine di destinazione di **[!UICONTROL Acquisizione dati]** per profilazione progressiva, preferenze, registrazioni e scenari simili. [Ulteriori informazioni](#data-capture-lp)
* Reindirizzare gli utenti a un **modulo web dedicato** senza creare una pagina esterna al di fuori di [!DNL Journey Optimizer]
* Creare **pagine di destinazione dinamiche** utilizzando le funzionalità di progettazione del contenuto di [!DNL Journey Optimizer]

### Acquisizione dei dati con pagine di destinazione {#data-capture-lp}

Le pagine di destinazione di **[!UICONTROL Acquisizione dati]** consentono di incorporare i moduli pubblicati in modo che i visitatori possano inviare attributi scritti nel set di dati di [!DNL Adobe Experience Platform] tramite la connessione streaming configurata nel predefinito per moduli. [Scopri come creare e incorporare moduli in una pagina di destinazione](lp-forms.md)

>[!NOTE]
>
>L’acquisizione dei dati tramite i moduli delle pagine di destinazione è supportata per i **profili noti** (profili esistenti identificati in [!DNL Adobe Experience Platform]). La pagina di destinazione deve essere aperta da un **collegamento personalizzato** (ad esempio da una campagna e-mail) in modo che l’identità del profilo possa essere risolta al caricamento della pagina.

Di seguito sono riportati alcuni esempi di casi d’uso:

1. **Arricchimento progressivo del profilo**: raccogli attributi aggiuntivi dai clienti noti, ad esempio numero di telefono, data di nascita o posizione, tramite una pagina di destinazione personalizzata per arricchire il profilo [!DNL Experience Platform] esistente per la segmentazione e la personalizzazione.

2. **Aggiornamento del centro preferenze**: consenti agli iscritti noti di gestire le proprie preferenze di comunicazione (interessi relativi a canali e argomenti) tramite una pagina di destinazione, con modifiche generalmente riflesse nel loro profilo [!DNL Experience Platform] entro circa 15 minuti.

3. **Registrazione evento o webinar**: acquisisci dati specifici dell’evento dai profili noti in una pagina di registrazione, aggiorna il profilo con gli attributi di registrazione e attiva un percorso di conferma.

4. **Iscrizione a programma o programma di fidelizzazione**: consenti alla clientela esistente di iscriversi a programmi di fidelizzazione o livelli di appartenenza inviando ulteriori dettagli tramite una pagina di destinazione, arricchendo il profilo per il targeting a valle.

5. **Partecipazione a concorsi o contest**: consenti ai clienti noti di partecipare a concorsi o concorsi a premi tramite un modulo della pagina di destinazione; acquisisci i dettagli specifici di partecipazione (risposte, preferenze o dichiarazioni) e scrivili nel profilo per supportare l’idoneità, la selezione dei vincitori e i percorsi di follow-up.

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="create-lp.md">
<img alt="Lead" src="../assets/do-not-localize/lp-subscription.jpeg">
</a>
<div><a href="create-lp.md"><strong>Creare pagine di destinazione</strong>
</div>
<p>
</td>
<td>
<a href="subscription-list.md">
<img alt="Non frequente" src="../assets/do-not-localize/lp-list.jpg">
</a>
<div>
<a href="subscription-list.md"><strong>Creare elenchi di iscrizioni</strong></a>
</div>
<p></td>
<td>
<a href="lp-forms.md">
<img alt="Elenco moduli per pagine di destinazione in Journey Optimizer" src="../assets/do-not-localize/lp-design.jpg">
</a>
<div>
<a href="lp-forms.md"><strong>Utilizzare i moduli nelle pagine di destinazione</strong></a>
</div>
<p>
</td>
<td>
<a href="../reports/lp-report-live.md">
<img alt="Convalida" src="../assets/do-not-localize/lp-reporting.jpg">
</a>
<div>
<a href="../reports/lp-report-live.md"><strong>Reporting</strong></a>
</div>
<p>
</td>
</tr></table>

## Prima di iniziare {#prerequisites}

Prima di creare una pagina di destinazione, completa questi passaggi di configurazione:

1. **Configurare un sottodominio**: configura un sottodominio dedicato all’hosting delle pagine di destinazione. [Ulteriori informazioni](lp-subdomains.md)
1. **Creare un predefinito per la pagina di destinazione**: un predefinito definisce il sottodominio e le altre impostazioni applicate alle pagine di destinazione. [Ulteriori informazioni](lp-presets.md#lp-create-preset)
1. **Creare un elenco di iscrizioni** (per i casi d’uso relativi alle iscrizioni): obbligatorio se desideri che i clienti possano iscriversi o annullare l’iscrizione a un servizio specifico. [Ulteriori informazioni](subscription-list.md)
1. **Creare un modulo** (per i casi d’uso relativi all’acquisizione dati): necessario quando desideri incorporare un modulo in una pagina di destinazione **[!UICONTROL Acquisizione dati]** e inviare gli invii a [!DNL Experience Platform]. [Ulteriori informazioni](lp-forms.md)

## Come funziona {#how-it-works}

La creazione e l’implementazione di una pagina di destinazione seguono questa sequenza:

1. **Creare e configurare la pagina di destinazione**: seleziona un predefinito, configura la pagina principale e aggiungi eventuali pagine secondarie richieste. [Ulteriori informazioni](create-lp.md#create-landing-page)
1. **Progettare la pagina**: crea il contenuto della pagina e il modulo utilizzando l’editor basato su trascinamento di [!DNL Journey Optimizer]. [Ulteriori informazioni](design-lp.md)
1. **Testare e pubblicare la pagina di destinazione**: visualizza l’anteprima della pagina, testa il comportamento del modulo, quindi pubblica per renderla live. [Ulteriori informazioni](create-lp.md#test-landing-page)
1. **Collegamento in un messaggio o in un percorso**: aggiungi l’URL della pagina di destinazione a un’azione del percorso, una campagna o un’e-mail in modo che la clientela possa giungervi. [Ulteriori informazioni](../email/message-tracking.md#insert-links)

## Video dimostrativo{#video}

Il video seguente mostra come creare un elenco di iscrizioni, configurare pagine di destinazione per acconsentire o rinunciare a un servizio, integrare l’opzione di consenso/rinuncia in un messaggio e configurare percorsi rilevanti.

>[!VIDEO](https://video.tv.adobe.com/v/341280?quality=12&learn=on)
