---
title: Rapporto live della campagna
description: Scopri come utilizzare i dati dal rapporto live di Campaign
feature: Reporting
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: 6177a33edeb3b8381c3eb5609762b4d974dc93e3
workflow-type: tm+mt
source-wordcount: '618'
ht-degree: 4%

---

# Rapporto live della campagna {#campaign-live-report}

Puoi accedere al rapporto live della campagna direttamente dalla tua campagna con **[!UICONTROL Live view]** pulsante .

La campagna **[!UICONTROL Live report]** La pagina verrà visualizzata con le seguenti schede:

* [Campaign](#campaign-live)
* [E-mail](#email-live)
* [Push](#push-live)

La campagna **[!UICONTROL Live report]** è suddiviso in diversi widget che descrivono in dettaglio il successo e gli errori della campagna. Se necessario, ogni widget può essere ridimensionato ed eliminato. Per ulteriori informazioni, consulta questo [sezione](../reports/live-report.md#modify-dashboard).

## Scheda Campaign {#campaign-global}

### Distribuzione {#delivery-global}

La **[!UICONTROL Campaign Statistics]** i dettagli del widget forniscono le informazioni principali relative alla campagna:

* **[!UICONTROL Entered profiles]**: Numero di profili che hanno avviato il percorso.

<!--
### Experimentation tab (#experimentation-live)

From your Campaign **[!UICONTROL Live report]**, the **[!UICONTROL Experimentation]** tab details the main information relative to how each variant is performing and if there is was winner during the test.
-->
## Scheda E-mail {#email-live}

Dalla tua campagna **[!UICONTROL Live report]**, **[!UICONTROL Email]** la scheda descrive le informazioni principali relative alle consegne e-mail inviate nella campagna.

Per un rapporto dettagliato su una consegna e-mail specifica, consulta la sezione [Report live e-mail](../reports/email-live-report.md) sezione .

La **[!UICONTROL Email Sending Statistics]** widget fornisce informazioni principali relative al messaggio:

* **[!UICONTROL Delivered]**: Numero di messaggi inviati correttamente in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Bounces]**: Totale degli errori cumulati durante la consegna e l’elaborazione automatica della restituzione in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Errors]**: Numero totale di errori che si sono verificati durante una consegna e che ne impediscono l’invio ai profili.

La **[!UICONTROL Sending metrics by Email]** tabella e **[!UICONTROL Email Summary]** il grafico descrive il successo della consegna:

* **[!UICONTROL Sent]**: Numero totale di invii per la consegna.

* **[!UICONTROL Delivered]**: Numero di messaggi inviati correttamente in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Bounces]**: Totale degli errori cumulati durante la consegna e l’elaborazione automatica della restituzione in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Errors]**: Numero totale di errori che si sono verificati durante una consegna e che ne impediscono l’invio ai profili.

* **[!UICONTROL Opens]**: Numero di volte in cui un messaggio è stato aperto in una consegna.

* **[!UICONTROL Clicks]**: Numero di volte in cui è stato fatto clic su un contenuto in una consegna.

* **[!UICONTROL Unsubscribe]**: Numero di clic sul collegamento di annullamento dell’abbonamento.

* **[!UICONTROL Spam complaints]**: Numero di volte in cui un messaggio è stato dichiarato come spam o spazzatura.

La **[!UICONTROL Bounce Reasons]**, **[!UICONTROL Bounce categories]** e **[!UICONTROL Hard and bounce - by Email]** I widget contengono i dati disponibili relativi ai messaggi non recapitati, ad esempio:

* **[!UICONTROL Hard bounce]**: Numero totale di errori permanenti, ad esempio un indirizzo e-mail errato. Ciò comporta un messaggio di errore che indica esplicitamente che l’indirizzo non è valido, ad esempio l’utente sconosciuto.

* **[!UICONTROL Soft bounce]**: Numero totale di errori temporanei, ad esempio una casella in entrata completa.

* **[!UICONTROL Ignored]**: Numero totale di temporanei, ad esempio Fuori sede, o un errore tecnico, ad esempio se il tipo di mittente è postmaster.

La **[!UICONTROL Error Reasons]** e **[!UICONTROL Exclude Reasons]** grafici e tabelle ti consentono di vedere quali errori ed esclusioni si sono verificati durante la consegna.

La **[!UICONTROL Email - Top recipient domain]** visualizza i dettagli del grafico e della tabella relativi ai domini più utilizzati dai destinatari per aprire l’e-mail.

## Scheda push {#push-live}

Dalla tua campagna **[!UICONTROL Live report]**, **[!UICONTROL Push]** la scheda descrive le informazioni principali relative alle consegne push inviate nella campagna.

Per un rapporto dettagliato su una consegna push specifica, consulta la sezione [Report live push](../reports/push-live-report.md) sezione .

**[!UICONTROL Push notification sending performance]**, **[!UICONTROL Push notification summary]** e **[!UICONTROL Sending metrics - by Push]** i widget descrivono nel dettaglio le informazioni principali relative al messaggio:

* **[!UICONTROL Sent]**: Numero totale di invii per la consegna.

* **[!UICONTROL Delivered]**: Numero di messaggi inviati correttamente in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Bounces]**: Totale degli errori cumulati durante la consegna e l’elaborazione automatica della restituzione in relazione al numero totale di messaggi inviati.

* **[!UICONTROL Errors]**: Numero totale di errori che si sono verificati durante una consegna e che ne impediscono l’invio ai profili.

* **[!UICONTROL Opens]**: Numero di volte in cui un messaggio è stato aperto in una consegna.

* **[!UICONTROL Actions]**: Numero totale di azioni sulla notifica push consegnata, ad esempio clic su un pulsante o cancellazione.

* **[!UICONTROL Engagements]**: Numero totale di aperture e azioni per questa notifica push, ad esempio se il profilo ha aperto il push o se è stato fatto clic su un pulsante.

La **[!UICONTROL Error Reasons]** e **[!UICONTROL Exclude Reasons]** grafici e tabelle ti consentono di vedere quali errori ed esclusioni si sono verificati durante la consegna.

La **[!UICONTROL Sending statistics - Failed]** widget consente di vedere quanti errori e mancati riscontri si sono verificati.

La **[!UICONTROL Tracking by platform]**, **[!UICONTROL Sending by platform]** e **[!UICONTROL Breakdown by platform]** grafici e tabelle descrivono in dettaglio il successo della notifica push in base al sistema operativo.

## Risorse aggiuntive

* [Introduzione alle campagne](get-started-with-campaigns.md)
* [Creare una campagna](create-campaign.md)
* [Creare campagne con attivazione API](api-triggered-campaigns.md)
* [Modificare o interrompere una campagna](modify-stop-campaign.md)
* [Rapporto globale della campagna](campaign-global-report.md)
