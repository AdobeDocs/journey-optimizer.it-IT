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
source-git-commit: d0dd382521aeb2c7e18dc547c2ec55fa1472ab8d
workflow-type: tm+mt
source-wordcount: '698'
ht-degree: 14%

---

# Introduzione alle pagine di destinazione {#get-started-lp}

Una pagina di destinazione è una pagina web autonoma a cui viene indirizzato un utente dopo aver fatto clic da un’e-mail, un sito web, un annuncio pubblicitario o qualsiasi altra posizione digitale.

[!DNL Journey Optimizer] consente di creare e progettare pagine di destinazione per indirizzare gli utenti a moduli online in cui possono acconsentire o rinunciare alla ricezione delle comunicazioni o di un servizio specifico, ad esempio una newsletter.

➡️ [Questo video offre ulteriori informazioni sulla configurazione delle iscrizioni e sulla creazione di pagine di destinazione](#video)

## Quando utilizzare le pagine di destinazione {#when-to-use}

Utilizza le pagine di destinazione per:

* Consenti ai clienti di **dare il consenso o rinunciare** a comunicazioni di marketing o a un servizio o a una newsletter specifico da un collegamento in un&#39;e-mail o in una campagna, inclusi gli elenchi di abbonamento per i servizi di destinazione. [Ulteriori informazioni](lp-use-cases.md#subscription-to-a-service)
* **Raccogli il consenso** prima di inviare le comunicazioni e invia una **e-mail di conferma** al momento del consenso o della rinuncia. [Ulteriori informazioni](lp-use-cases.md#send-confirmation-email)
* **Acquisisci o aggiorna i dati del profilo** utilizzando i moduli nelle **[!UICONTROL pagine di destinazione di Acquisizione dati]** per profili progressivi, preferenze, registrazioni e scenari simili. [Ulteriori informazioni](#data-capture-lp)
* Reindirizza gli utenti a un **modulo Web dedicato** senza creare una pagina esterna all&#39;esterno di [!DNL Journey Optimizer]
* Crea **pagine di destinazione dinamiche** utilizzando le funzionalità di progettazione del contenuto di [!DNL Journey Optimizer]

### Acquisizione dei dati con pagine di destinazione {#data-capture-lp}

Le pagine di destinazione di **[!UICONTROL Acquisizione dati]** consentono di incorporare i moduli pubblicati in modo che i visitatori possano inviare attributi scritti nel set di dati di [!DNL Adobe Experience Platform] tramite la connessione streaming configurata nel predefinito per moduli. [Scopri come creare e incorporare moduli in una pagina di destinazione](lp-forms.md)

>[!NOTE]
>
>L&#39;acquisizione dei dati tramite i moduli delle pagine di destinazione è supportata per **profili noti** (profili esistenti identificati in [!DNL Adobe Experience Platform]). La pagina di destinazione deve essere aperta da un **collegamento personalizzato** (ad esempio da una campagna e-mail) in modo che l&#39;identità del profilo possa essere risolta al caricamento della pagina.

Di seguito sono riportati alcuni esempi di casi di utilizzo:

1. **Arricchimento progressivo del profilo**: raccogli attributi aggiuntivi dai clienti noti, ad esempio numero di telefono, data di nascita o posizione, tramite una pagina di destinazione personalizzata per arricchire il profilo [!DNL Experience Platform] esistente per la segmentazione e la personalizzazione.

2. **Aggiornamento del centro preferenze**: consente agli abbonati noti di gestire le proprie preferenze di comunicazione (interessi relativi a canali e argomenti) tramite una pagina di destinazione, con le modifiche generalmente riportate nel profilo [!DNL Experience Platform] entro circa 15 minuti.

3. **Registrazione evento o webinar** - Acquisisci dati specifici dell&#39;evento dai profili noti in una pagina di registrazione, aggiorna il profilo con gli attributi di registrazione e attiva un percorso di conferma.

4. **Iscrizione programma o programma fedeltà**: consenti ai clienti esistenti di iscriversi a programmi fedeltà o livelli di iscrizione inviando ulteriori dettagli tramite una pagina di destinazione, arricchendo il profilo per il targeting a valle.

5. **Partecipazione a concorsi o concorsi**: consente ai clienti noti di partecipare a concorsi o tornei tramite un modulo della pagina di destinazione; acquisisce i dettagli specifici dell&#39;iscrizione (risposte, preferenze o dichiarazioni) e li scrive nel profilo per supportare i percorsi di idoneità, selezione dei vincitori e follow-up.

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
<a href="subscription-list.md"><strong>Creare elenchi di abbonamenti</strong></a>
</div>
<p></td>
<td>
<a href="lp-forms.md">
<img alt="Elenco Forms per pagine di destinazione in Journey Optimizer" src="../assets/do-not-localize/lp-design.jpg">
</a>
<div>
<a href="lp-forms.md"><strong>Utilizza i moduli nelle pagine di destinazione</strong></a>
</div>
<p>
</td>
<td>
<a href="../reports/lp-report-live.md">
<img alt="Convalida" src="../assets/do-not-localize/lp-reporting.jpg">
</a>
<div>
<a href="../reports/lp-report-live.md"><strong>Generazione rapporti</strong></a>
</div>
<p>
</td>
</tr></table>

## Prima di iniziare {#prerequisites}

Prima di creare una pagina di destinazione, completa i passaggi di configurazione seguenti:

1. **Configura un sottodominio** — Configura un sottodominio dedicato all&#39;hosting delle pagine di destinazione. [Ulteriori informazioni](lp-subdomains.md)
1. **Crea un predefinito per la pagina di destinazione**. Un predefinito definisce il sottodominio e le altre impostazioni applicate alle pagine di destinazione. [Ulteriori informazioni](lp-presets.md#lp-create-preset)
1. **Crea un elenco di abbonamenti** (per i casi di utilizzo degli abbonamenti): obbligatorio se si desidera che i clienti si abbonino o annullino l&#39;abbonamento a un servizio specifico. [Ulteriori informazioni](subscription-list.md)
1. **Crea un modulo** (per i casi di utilizzo dell&#39;acquisizione dati): necessario quando si desidera incorporare un modulo in una pagina di destinazione **[!UICONTROL Acquisizione dati]** e inviare gli invii a [!DNL Experience Platform]. [Ulteriori informazioni](lp-forms.md)

## Come funziona {#how-it-works}

La creazione e la distribuzione di una pagina di destinazione seguono questa sequenza:

1. **Crea e configura la pagina di destinazione**: seleziona un predefinito, imposta la pagina principale e aggiungi le pagine secondarie richieste. [Ulteriori informazioni](create-lp.md#create-landing-page)
1. **Progetta la pagina**: crea il contenuto della pagina e il modulo utilizzando l&#39;editor di trascinamento di [!DNL Journey Optimizer]. [Ulteriori informazioni](design-lp.md)
1. **Verifica e pubblica la pagina di destinazione** - Visualizza l&#39;anteprima della pagina, verifica il comportamento del modulo, quindi pubblica per renderla live. [Ulteriori informazioni](create-lp.md#test-landing-page)
1. **Collegamento in un messaggio o in un percorso** — Aggiungi l&#39;URL della pagina di destinazione a un&#39;azione e-mail, campagna o percorso in modo che i clienti possano raggiungerlo. [Ulteriori informazioni](../email/message-tracking.md#insert-links)

## Video introduttivo{#video}

Il video seguente mostra come creare un elenco di iscrizioni, impostare pagine di destinazione per il consenso o la rinuncia a un servizio, integrare l’opzione di consenso/rinuncia in un messaggio e configurare i percorsi rilevanti.

>[!VIDEO](https://video.tv.adobe.com/v/344399?captions=ita&quality=12&learn=on)
