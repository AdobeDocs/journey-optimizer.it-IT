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
source-git-commit: 170bdaaa13fe78ad4c47a6e091c8090156fde8f6
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 22%

---

# Introduzione alle pagine di destinazione {#get-started-lp}

Una pagina di destinazione è una pagina web autonoma a cui viene indirizzato un utente dopo aver fatto clic da un’e-mail, un sito web, un annuncio pubblicitario o qualsiasi altra posizione digitale.

[!DNL Journey Optimizer] consente di creare e progettare pagine di destinazione per indirizzare gli utenti a moduli online in cui possono acconsentire o rinunciare alla ricezione delle comunicazioni o di un servizio specifico, ad esempio una newsletter.

➡️ [Questo video offre ulteriori informazioni sulla configurazione delle iscrizioni e sulla creazione di pagine di destinazione](#video)

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
<a href="design-lp.md">
<img alt="Convalida" src="../assets/do-not-localize/lp-design.jpg">
</a>
<div>
<a href="design-lp.md"><strong>Progettazione delle pagine di destinazione</strong></a>
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

## Quando utilizzare le pagine di destinazione {#when-to-use}

Utilizza le pagine di destinazione per:

* Consenti ai clienti di **dare il consenso o rinunciare** a comunicazioni di marketing o a un servizio o a una newsletter specifico da un collegamento in un&#39;e-mail o in una campagna, inclusi gli elenchi di abbonamento per i servizi di destinazione. [Ulteriori informazioni](lp-use-cases.md#subscription-to-a-service)
* **Raccogli il consenso** prima di inviare le comunicazioni e invia una **e-mail di conferma** al momento del consenso o della rinuncia. [Ulteriori informazioni](lp-use-cases.md#send-confirmation-email)
* Reindirizza gli utenti a un **modulo Web dedicato** senza creare una pagina esterna all&#39;esterno di [!DNL Journey Optimizer]
* Crea **pagine di destinazione dinamiche** utilizzando le funzionalità di progettazione del contenuto di [!DNL Journey Optimizer]

## Prima di iniziare {#prerequisites}

Prima di creare una pagina di destinazione, completa i passaggi di configurazione seguenti:

1. [**Configura un sottodominio**](lp-subdomains.md) — Configura un sottodominio dedicato all&#39;hosting delle pagine di destinazione.
1. [**Crea un predefinito per la pagina di destinazione**](lp-presets.md#lp-create-preset). Un predefinito definisce il sottodominio e le altre impostazioni applicate alle pagine di destinazione.
1. [**Crea un elenco di abbonamenti**](subscription-list.md) (per i casi di utilizzo degli abbonamenti): obbligatorio se si desidera che i clienti si abbonino o annullino l&#39;abbonamento a un servizio specifico.

## Come funziona {#how-it-works}

La creazione e la distribuzione di una pagina di destinazione seguono questa sequenza:

1. [**Crea e configura la pagina di destinazione**](create-lp.md): seleziona un predefinito, imposta la pagina principale e aggiungi le pagine secondarie richieste.
1. [**Progetta la pagina**](design-lp.md): crea il contenuto della pagina e il modulo utilizzando l&#39;editor di trascinamento di [!DNL Journey Optimizer].
1. [**Verifica**](create-lp.md#test-landing-page) e [**pubblica**](create-lp.md#publish-landing-page) la tua pagina di destinazione - Visualizza l&#39;anteprima della pagina, verifica il comportamento del modulo, quindi pubblica per renderla live.
1. [**Collegamento in un messaggio o in un percorso**](../email/message-tracking.md#insert-links) — Aggiungi l&#39;URL della pagina di destinazione a un&#39;azione e-mail, campagna o percorso in modo che i clienti possano raggiungerlo.

## Video introduttivo{#video}

Il video seguente mostra come creare un elenco di iscrizioni, impostare pagine di destinazione per il consenso o la rinuncia a un servizio, integrare l’opzione di consenso/rinuncia in un messaggio e configurare i percorsi rilevanti.

>[!VIDEO](https://video.tv.adobe.com/v/341280?quality=12&learn=on)
