---
solution: Journey Optimizer
product: journey optimizer
title: Report live
description: Scopri come utilizzare i dati dal rapporto live
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: 8dd48bb2-a805-4c46-a16c-c68173a9ac08
source-git-commit: e7431d1b69e460471b01439c9bd2577fd69944ed
workflow-type: tm+mt
source-wordcount: '1011'
ht-degree: 4%

---

# Introduzione ai rapporti live {#live-report}

Utilizza la **[!UICONTROL Report live]** per misurare e visualizzare in tempo reale l’impatto e le prestazioni dei percorsi e dei messaggi in un dashboard integrato.
I dati sono disponibili nella **[!UICONTROL Report live]** non appena la consegna viene inviata o il percorso viene eseguito da **[!UICONTROL Ultime 24 ore]** scheda .

* Se desideri eseguire il targeting di un percorso nel contesto di un percorso, dal **[!UICONTROL Percorsi]** accedere al percorso e fare clic su **[!UICONTROL Visualizza rapporto]** pulsante .

   ![](assets/report_journey.png)

* Se desideri eseguire il targeting di una campagna, dalla **[!UICONTROL Campagne]** , accedi alla campagna e fai clic su **[!UICONTROL Rapporti]** pulsante .

   ![](assets/report_campaign.png)

* Se desideri passare dalla **[!UICONTROL Report globale]** al **[!UICONTROL Report live]** per la consegna, fai clic su **[!UICONTROL Ultime 24 ore]** dal commutatore di tabulazione.

   ![](assets/report_3.png)

Per un elenco dettagliato di ciascuna metrica disponibile in Adobe Journey Optimizer, consulta [questa pagina](#list-of-components-live).

## Personalizza dashboard {#modify-dashboard}

Ogni dashboard di reporting può essere modificato ridimensionando o rimuovendo i widget. La modifica dei widget influisce solo sul dashboard dell&#39;utente corrente. Altri utenti visualizzeranno le proprie dashboard o quelle impostate per impostazione predefinita.

1. Scegli se escludere gli eventi di test dai rapporti con la barra di attivazione. Per ulteriori informazioni sugli eventi di test, consulta [questa pagina](../building-journeys/testing-the-journey.md).

   Tieni presente che **[!UICONTROL Escludere gli eventi di test]** è disponibile solo per i rapporti di Percorso.

   ![](assets/report_modify_6.png)

1. Per ridimensionare o rimuovere i widget, fai clic su **[!UICONTROL Modifica]**.

   ![](assets/report_modify_7.png)

1. Regolare le dimensioni dei widget trascinandone l&#39;angolo in basso a destra.

   ![](assets/report_modify_8.png)

1. Fai clic su **[!UICONTROL Rimuovi]** per rimuovere qualsiasi widget non è necessario.

   ![](assets/report_modify_9.png)

1. Una volta soddisfatti dell&#39;ordine di visualizzazione e delle dimensioni dei widget, fai clic su **[!UICONTROL Salva]**.

Il dashboard viene ora salvato. Le diverse modifiche verranno applicate nuovamente per un utilizzo successivo dei rapporti live. Se necessario, utilizza le **[!UICONTROL Reimposta]** per ripristinare l&#39;ordine predefinito dei widget e dei widget.

## Elenco dei componenti {#list-of-components-live}

Le tabelle seguenti forniscono l’elenco delle metriche utilizzate nei rapporti e le relative definizioni a seconda del tipo di consegna.

### Metriche di percorso {#journey-metrics}

<table> 
 <thead> 
  <tr> 
   <th> Metrica<br/> </th> 
   <th> Definizione<br/> </th> 
</tr>
 </thead> 
 <tbody> 
  <tr> 
   <td>Azioni eseguite<br/> </td> 
   <td> Numero totale di azioni eseguite correttamente per un percorso.<br/> </td> 
</tr> 
  <tr> 
   <td> Profili inseriti<br/> </td> 
   <td> Numero totale di persone che hanno raggiunto l'evento di ingresso del percorso.<br/> </td> 
</tr>
  <tr> 
   <td> Errore in azione<br/> </td> 
   <td>Numero totale di errori che si sono verificati per le azioni.<br/> </td> 
</tr> 
  <tr> 
   <td> Profili usciti<br/> </td> 
   <td> Numero totale di persone uscite dal percorso.<br/> </td> 
</tr> 
  <tr> 
   <td> Percorso singolo non riuscito<br/> </td> 
   <td> Numero totale di singoli percorsi che non sono stati eseguiti correttamente.<br/> </td> 
</tr> 
 </tbody> 
</table>

### Metriche e-mail e SMS {#email-and-sms-metrics}

<table> 
 <thead> 
  <tr> 
   <th> Metrica<br/> </th> 
   <th> Definizione<br/> </th> 
</tr>
 </thead> 
 <tbody>
  <tr> 
   <td> E-mail non consegnate<br/> </td> 
   <td> Totale degli errori cumulati durante la consegna e l'elaborazione automatica della restituzione.<br/> </td> 
</tr> 
  <tr> 
   <td> Percentuale non recapitate<br/> </td> 
   <td> Percentuale di e-mail rimbalzate rispetto alle e-mail inviate.<br/> </td> 
</tr>
  <tr> 
   <td> Clic<br/> </td> 
   <td> Numero di volte in cui è stato fatto clic su un contenuto in un’e-mail.<br/> </td> 
</tr> 
  <tr> 
   <td> Consegnate <br/> </td> 
   <td> Numero di messaggi inviati correttamente.<br/></td> 
</tr> 
  <tr> 
   <td> Tasso di consegna<br/> </td> 
   <td> Percentuale di messaggi inviati correttamente.<br/> </td> 
</tr>
  <tr> 
   <td> Errori<br/> </td> 
   <td> Numero totale di errori che si sono verificati durante una consegna e che ne impediscono l’invio ai profili.<br/> </td> 
</tr> 
  <tr> 
   <td> Frequenza errori<br/> </td> 
   <td> Percentuale di errori che si sono verificati durante una consegna che ne impedisce l’invio rispetto alle e-mail inviate.<br/> </td> 
</tr>
  <tr> 
   <td> Escluso<br/> </td> 
   <td> Numero di profili esclusi da Adobe Journey Optimizer.<br/> </td> 
</tr>
  <tr> 
   <td> Rimbalzo duro<br/> </td> 
   <td> Numero totale di errori permanenti, ad esempio un indirizzo e-mail errato. Ciò comporta un messaggio di errore che indica esplicitamente che l’indirizzo non è valido, ad esempio l’utente sconosciuto.<br/> </td>
</tr>
  <tr> 
   <td> Ignorato<br/> </td> 
   <td> Numero totale di temporanei, ad esempio Fuori sede, o un errore tecnico, ad esempio se il tipo di mittente è postmaster.<br/> </td> 
</tr>
   <tr> 
   <td>Frequenza clic offerta<br/> </td> 
   <td>Percentuale di utenti che hanno interagito con l’offerta.<br/> </td> 
</tr>
   <tr> 
   <td>Tasso di impression dell’offerta<br/> </td> 
   <td>Percentuale di offerte aperte rispetto al numero di offerte inviate.<br/> </td> 
</tr>
   <tr> 
   <td>Offer name (Nome offerta)<br/> </td> 
   <td> Nome dell’offerta aggiunta nella consegna. Per ulteriori informazioni sul posizionamento, consulta questo <a href="../offers/offer-library/creating-personalized-offers.md">page</a>.<br/> </td> 
</tr>
   <tr> 
   <td>Offerta inviata<br/> </td> 
   <td>Numero totale di invii per l’offerta.<br/> </td> 
</tr> 
  <tr>
   <td>Messaggi aperti<br/> </td> 
   <td> Numero di volte in cui il messaggio è stato aperto.<br/> </td> 
</tr> 
  <tr> 
   <td> Open Rate<br/> </td> 
   <td> Numero totale di e-mail aperte rispetto al numero di e-mail consegnate.<br/> </td> 
</tr>
  <tr> 
   <td>Nome del posizionamento<br/> </td> 
   <td> Nome del posizionamento utilizzato per visualizzare l’offerta. Per ulteriori informazioni sul posizionamento, consulta questo <a href="../offers/offer-library/creating-placements.md">page</a>. </td> 
</tr> 
  <tr> 
   <td> Nuovi tentativi<br/> </td> 
   <td> Numero di e-mail in coda per i nuovi tentativi.<br/> </td> 
</tr> 
  <tr> 
   <td> Inviate<br/> </td> 
   <td> Numero totale di invii per la consegna.<br/> </td> 
</tr>
  <tr> 
   <td> Rimbalzo morbido<br/> </td> 
   <td> Numero totale di errori temporanei, ad esempio una casella in entrata completa.<br/> </td> 
</tr>
  <tr> 
   <td> Segnalazioni di spam<br/> </td> 
   <td> Numero di volte in cui un messaggio è stato dichiarato come spam o spazzatura.<br/> </td> 
</tr>
  <tr> 
   <td> Target<br/> </td> 
   <td> Numero totale di messaggi elaborati durante l’analisi della consegna.<br/> </td> 
</tr> 
  <tr> 
   <td> Clic univoci<br/> </td> 
   <td> Numero di destinatari che hanno fatto clic su un contenuto in un’e-mail.<br/> </td> 
</tr> 
  <tr> 
   <td>Frequenza di clic univoca<br/> </td> 
   <td> Percentuale di utenti che hanno interagito con la consegna.<br/> </td> 
</tr>
  <tr> 
   <td> Aperture univoche<br/> </td> 
   <td>Numero di destinatari che hanno aperto la consegna.<br/> </td> 
</tr> 
  <tr> 
   <td> Abbonamenti annullati<br/> </td> 
   <td> Numero di clic sul collegamento di annullamento dell’abbonamento.<br/> </td> 
</tr> 
 </tbody> 
</table>

### Metriche della pagina di destinazione {#landing-page-metrics}

<table> 
 <thead> 
  <tr> 
   <th> Metrica<br/> </th> 
   <th> Definizione<br/> </th> 
</tr>
 </thead> 
 <tbody>
 <tr> 
  <td>E-mail non consegnate<br/> </td> 
   <td>Numero di persone che non hanno interagito con la pagina di destinazione e non hanno completato l’azione di iscrizione.<br/> </td> 
</tr>
 <tr>
  <tr> 
   <td>Clic<br/> </td> 
   <td>Numero di volte in cui è stato fatto clic su un contenuto nella pagina di destinazione.<br/> </td> 
</tr>
<tr>
<td>Conversione<br/> </td> 
   <td>Numero di persone che hanno interagito con la pagina di destinazione, ad esempio abbonati a un modulo.<br/> </td> 
</tr>
 <tr> 
   <td>Percorsi<br/> </td> 
   <td>Numero di visite alla pagina di destinazione provenienti da un percorso.<br/> </td> 
</tr>
 <tr> 
   <td>Altre fonti<br/> </td> 
   <td>Numero di visite alla pagina di destinazione provenienti da un’origine esterna anziché da un percorso.<br/> </td> 
</tr>
 <tr> 
   <td>Visite totali<br/> </td> 
   <td> Numero totale di visite alla pagina di destinazione provenienti da percorsi e origini esterne, comprese visite multiple di un solo destinatario.<br/> </td> 
</tr>
 <tr> 
   <td>Visitatori univoci<br/> </td> 
   <td>Numero di persone che hanno visitato la pagina di destinazione, non vengono prese in considerazione più visite di un destinatario.<br/> </td> 
</tr>
 <tr> 
   <td>Visite<br/> </td> 
   <td>Numero di visite alla pagina di destinazione, comprese più visite di un solo destinatario.<br/> </td> 
</tr>
 </tbody> 
</table>

### Metriche di notifica push {#push-notification-metrics}

<table> 
 <thead> 
  <tr> 
   <th> Metrica<br/> </th> 
   <th> Definizione<br/> </th> 
</tr>
 </thead> 
 <tbody>
 <tr> 
   <td>Azioni<br/> </td> 
   <td> Numero totale di azioni sulla notifica push consegnata, ad esempio clic su un pulsante o cancellazione.<br/> </td> 
</tr>
  <tr> 
   <td>E-mail non consegnate<br/> </td> 
   <td> Totale degli errori cumulati durante la consegna e l'elaborazione automatica della restituzione.<br/> </td> 
</tr> 
  <tr> 
   <td> Consegnate<br/> </td> 
   <td> Numero di messaggi inviati correttamente.<br/> </td> 
</tr> 
  <tr> 
   <td>Coinvolgimento<br/> </td> 
   <td> Numero totale di aperture e azioni per questa notifica push, ad esempio se il profilo ha aperto il push o se è stato fatto clic su un pulsante.<br/> </td> 
</tr> 
  <tr> 
   <td> Errori<br/> </td> 
   <td> Numero totale di errori che si sono verificati durante una consegna e che ne impediscono l’invio ai profili.<br/> </td> 
</tr>
  <tr> 
   <td> Escluso<br/> </td> 
   <td> Numero di profili esclusi da Adobe Journey Optimizer.<br/> </td> 
</tr>
  <tr> 
   <td> Messaggi aperti<br/> </td> 
   <td> Numero totale di notifiche push inviate al dispositivo e su cui gli utenti hanno fatto clic per aprire l’app. È simile al clic push, tranne per il fatto che l’apertura push non viene attivata se la notifica è stata ignorata.<br/> </td> 
</tr> 
  <tr> 
   <td> Inviate<br/> </td> 
   <td> Numero totale di invii per la consegna.<br/> </td> 
</tr> 
  <tr> 
   <td> Target<br/> </td> 
   <td> Numero totale di messaggi push elaborati durante l’analisi della consegna.<br/> </td> 
</tr>  
 </tbody> 
</table>

<!--
### In-app metrics {#inapp-metrics}
<table> 
 <thead> 
  <tr> 
   <th> Metric<br/> </th> 
   <th> Definition<br/> </th> 
</tr>
 </thead> 
 <tbody>
 <tr> 
   <td>Clicks<br/> </td> 
   <td>Total number of recipients who interacted with the buttons included in the In-app message.<br/> </td> 
</tr>
  <tr> 
   <td>Impressions<br/> </td> 
   <td> Total number of In-app messages delivered to all users.<br/> </td>
</tr>
  <tr> 
   <td>Unique impressions<br/> </td> 
   <td>Number of unique users to whom the In-app message was delivered.<br/> </td>
</tr>
 </tbody> 
</table>
-->