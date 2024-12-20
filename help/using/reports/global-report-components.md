---
solution: Journey Optimizer
product: journey optimizer
title: Elenco dei componenti
description: Scopri come utilizzare i dati del rapporto globale
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: c487bb38-49ce-4238-8e94-8364f994cedd
source-git-commit: 47482adb84e05fe41eb1c50479a8b50e00469ec4
workflow-type: tm+mt
source-wordcount: '1155'
ht-degree: 1%

---

# Elenco dei componenti {#list-of-components-global}

>[!AVAILABILITY]
>
>L’esperienza di reporting corrente verrà ritirata a gennaio 2025. Dopo questa data, la nuova esperienza di reporting diventerà lo standard. Consigliamo di acquisire familiarità con le nuove funzioni e funzionalità per garantire una transizione senza problemi. [Introduzione alla nuova interfaccia di Journey Optimizer per la generazione di rapporti.](report-gs-cja.md)

Le tabelle seguenti forniscono l’elenco delle metriche utilizzate nei rapporti e le relative definizioni a seconda del tipo di consegna.

## Metriche di percorso {#journey-metrics}

<table> 
 <thead> 
  <tr> 
   <th> Metrica<br/> </th> 
   <th> Definizione<br/> </th> 
</tr>
 </thead> 
 <tbody> 
  <tr> 
   <td>Azioni eseguite correttamente<br/> </td> 
   <td> Numero totale di azioni eseguite correttamente per un percorso.<br/> </td> 
</tr> 
  <tr> 
   <td> Profili immessi<br/> </td> 
   <td> Numero totale di individui che hanno raggiunto l'evento di ingresso del percorso.<br/> </td> 
</tr>
  <tr> 
   <td> Errore nell'azione<br/> </td> 
   <td>Numero totale di errori che si sono verificati per le azioni.<br/> </td> 
</tr> 
  <tr> 
   <td> Profili usciti<br/> </td> 
   <td> Numero totale di persone che sono uscite dal percorso.<br/> </td> 
</tr> 
  <tr> 
   <td> Singolo percorso non riuscito<br/> </td> 
   <td> Numero totale di singoli percorsi non eseguiti correttamente.<br/> </td> 
</tr> 
 </tbody> 
</table>

## Dimensioni e metriche per e-mail e SMS {#email-and-sms-metrics}

<table> 
 <thead> 
  <tr> 
   <th> Metrica<br/> </th> 
   <th> Definizione<br/> </th> 
</tr>
 </thead> 
 <tbody>
  <tr> 
   <td> Mancati recapiti<br/> </td> 
   <td> Totale degli errori accumulati durante il processo di invio e l'elaborazione automatica della restituzione in relazione al numero totale di messaggi inviati.<br/> </td> 
</tr> 
  <tr> 
   <td> Percentuale non recapitate<br/> </td> 
   <td> Percentuale di e-mail non recapitate rispetto alle e-mail inviate.<br/> </td> 
</tr>
  <tr> 
   <td> Clic<br/> </td> 
   <td> Numero di volte in cui è stato fatto clic su un contenuto in un messaggio e-mail.<br/> </td> 
</tr> 
  <tr> 
   <td> Consegnato <br/> </td> 
   <td> Numero di messaggi inviati correttamente, in relazione al numero totale di messaggi inviati.<br/></td> 
</tr> 
  <tr> 
   <td> Percentuale di recapito<br/> </td> 
   <td> Percentuale di messaggi inviati correttamente.<br/> </td> 
</tr>
  <tr> 
   <td> Errori<br/> </td> 
   <td> Numero totale di errori che si sono verificati durante il processo di invio e che ne hanno impedito l'invio ai profili.<br/> </td> 
</tr> 
  <tr> 
   <td> Frequenza errori<br/> </td> 
   <td> Percentuale di errori che si sono verificati durante il processo di invio che ne hanno impedito l'invio rispetto alle e-mail inviate.<br/> </td> 
</tr>
</tr> 
  <tr> 
   <td> Motivo errore<br/> </td> 
   <td> Nome della causa originale specifica dell’errore. <a href="exclusion-list.md">Ulteriori informazioni sui motivi dell'errore</a>.<br/> </td> 
</tr>
  <tr> 
   <td> Escluso<br/> </td> 
   <td> Numero di profili esclusi da Adobe Journey Optimizer.<br/> </td> 
</tr>
  <tr> 
   <td> Mancato recapito<br/> </td> 
   <td> Il numero totale di errori permanenti, ad esempio un indirizzo e-mail errato. Ciò comporta un messaggio di errore che indica esplicitamente che l'indirizzo non è valido, ad esempio Utente sconosciuto.<br/> </td>
</tr>
  <tr> 
   <td> Ignorato<br/> </td> 
   <td> Numero totale di messaggi temporanei, ad esempio Fuori sede, o un errore tecnico, ad esempio se il tipo di mittente è postmaster.<br/> </td> 
</tr>
   <tr> 
   <td>Percentuale di clic offerta<br/> </td> 
   <td>Percentuale di utenti che hanno interagito con l'offerta.<br/> </td> 
</tr>
   <tr> 
   <td>Percentuale di impression offerta<br/> </td> 
   <td>Percentuale di offerte aperte rispetto al numero di offerte inviate.<br/> </td> 
</tr>
   <tr> 
   <td>Nome offerta<br/> </td> 
   <td> Nome dell’offerta aggiunta alla consegna. Per ulteriori informazioni sul posizionamento, consulta questa <a href="../offers/offer-library/creating-personalized-offers.md">pagina</a>.<br/> </td> 
</tr>
   <tr> 
   <td>Offerta inviata<br/> </td> 
   <td>Numero totale di invii per l'offerta.<br/> </td> 
</tr> 
  <tr>
   <td>Apertura di <br/> </td> 
   <td> Numero di volte in cui il messaggio è stato aperto.<br/> </td> 
</tr> 
  <tr> 
   <td> Percentuale aperture<br/> </td> 
   <td> Numero totale di e-mail aperte rispetto al numero di e-mail consegnate.<br/> </td> 
</tr>
  <tr> 
   <td>Nome posizionamento<br/> </td> 
   <td> Nome del posizionamento utilizzato per visualizzare l’offerta. Per ulteriori informazioni sul posizionamento, consulta questa <a href="../offers/offer-library/creating-placements.md">pagina</a>. </td> 
</tr> 
  <tr> 
   <td> Tentativi<br/> </td> 
   <td> Numero di e-mail in coda per i nuovi tentativi.<br/> </td> 
</tr> 
  <tr> 
   <td> Inviato<br/> </td> 
   <td> Numero totale di invii per la consegna.<br/> </td> 
</tr>
  <tr> 
   <td> Mancato recapito non permanente<br/> </td> 
   <td> Numero totale di errori temporanei, ad esempio una casella in entrata completa.<br/> </td> 
</tr>
  <tr> 
   <td> Reclami spam<br/> </td> 
   <td> Numero di volte in cui un messaggio è stato dichiarato come posta indesiderata o posta indesiderata.<br/> </td> 
</tr>
  <tr> 
   <td> Destinato<br/> </td> 
   <td> Numero totale di messaggi elaborati durante l'analisi della consegna.<br/> </td> 
</tr> 
  <tr> 
   <td> Clic univoci<br/> </td> 
   <td> Numero di destinatari che hanno fatto clic su un contenuto in un messaggio e-mail.<br> Tieni presente che nel calcolo dei clic univoci vengono considerati gli ultimi 10 giorni. Se un profilo registra più clic entro il periodo di 10 giorni, verranno conteggiati come clic univoci. Tuttavia, se un profilo ha 2 clic a distanza di oltre 10 giorni, non verrà considerato come clic univoci.<br/> </td> 
</tr> 
  <tr> 
   <td>Percentuale clic univoci<br/> </td> 
   <td> Percentuale di utenti che hanno interagito con la consegna.<br/> </td> 
</tr>
  <tr> 
   <td> Aperture univoche<br/> </td> 
   <td>Numero di destinatari che hanno aperto la consegna. <br> Tieni presente che nel calcolo delle aperture univoche vengono considerati gli ultimi 10 giorni. Se un profilo registra più aperture entro il periodo di 10 giorni, queste verranno conteggiate come aperture univoche. Tuttavia, se un profilo ha 2 aperture a più di 10 giorni di distanza, non verranno considerate come aperture univoche.<br/> </td> 
</tr> 
  <tr> 
   <td> Annullamenti abbonamenti<br/> </td> 
   <td> Numero di clic sul collegamento di annullamento dell'abbonamento.<br/> </td> 
</tr> 
 </tbody> 
</table>

<!--
## Experimentation metrics {#experimentation-metrics}
<table> 
 <thead> 
  <tr> 
   <th> Metric<br/> </th> 
   <th> Definition<br/> </th> 
</tr>
 </thead> 
 <tbody>
  <tr> 
   <td>App installs<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>App launches<br/> </td> 
   <td><br/> </td> 
</tr>
 <tr> 
   <td>Average lift<br/> </td> 
   <td> Percentage improvement in conversion rate of a given treatment over the baseline.<a href="../content-management/experiment-calculations.md#understand-lift">Learn more</a>.<br/> </td> 
  </tr>
  <tr> 
   <td>Confidence<br/> </td> 
   <td>Evidence that a given treatment is the same as the baseline treatment. <a href="../content-management/experiment-calculations.md#understand-confidence">Learn more</a>.<br/> </td> 
</tr>
  <tr> 
   <td>Confidence interval<br/> </td> 
   <td>Percentage difference in performance between the baseline and the best performing treatment. <a href="../content-management/experiment-calculations.md#understand-intervals">Learn more</a>.<br/> </td> 
</tr> 
  <tr> 
   <td>Count per profile<br/> </td> 
   <td>Total value of the Experiment objective metric divided by the number of profiles.<br/> </td> 
</tr>
  <tr> 
   <td>Email Opens<br/> </td> 
   <td>Number of times the email was opened.<br/> </td> 
</tr>
  <tr> 
   <td>Email Unsubscribes<br/> </td> 
   <td>Number of clicks on the unsubscription link.<br/> </td> 
</tr>
  <tr> 
   <td>First app launches<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>Outbound Clicks<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>Profiles<br/> </td> 
   <td>Number of profiles targeted for this treatment.<br/> </td> 
</tr>
  <tr> 
   <td>Unique email opens<br/> </td> 
   <td>Number of recipients who opened the email.<br/> </td>
<tr>
  <tr> 
   <td>Unique email unsubscribes<br/> </td> 
   <td>Number of recipients who clicked on the unsubscription link.<br/> </td>
</tr>
  <tr> 
   <td>Unique installs<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>Unique launches<br/> </td> 
   <td><br/> </td> 
</tr> 
  <tr> 
   <td>Unique outbound clicks<br/> </td> 
   <td><br/> </td> 
</tr>
  <tr> 
   <td>Unique upgrades<br/> </td> 
   <td><br/> </td> 
</tr>
   <td>Upgrades<br/> </td> 
   <td><br/> </td> 
</tr> 
</tbody> 
</table>
-->

## Metriche in-app {#inapp-metrics}

<table> 
 <thead> 
  <tr> 
   <th> Metrica<br/> </th> 
   <th> Definizione<br/> </th> 
</tr>
 </thead> 
 <tbody>
 <tr> 
   <td>Clic<br/> </td> 
   <td>Numero totale di destinatari che hanno interagito con i pulsanti inclusi nel messaggio in-app.<br/> </td> 
</tr>
  <tr> 
   <td>Percentuale di clic<br/> </td> 
   <td>Percentuale di utenti che hanno interagito con i pulsanti inclusi nel messaggio in-app rispetto agli utenti che hanno visualizzato il messaggio.<br/> </td> 
</tr> 
  <tr> 
   <td>Percentuale ignorati<br/> </td> 
   <td> Percentuale di messaggi in-app ignorati dai destinatari.<br/> </td> 
</tr> 
  <tr> 
   <td>Impression<br/> </td> 
   <td> Numero totale di messaggi in-app recapitati a tutti gli utenti.<br/> </td>
</tr>
  <tr> 
   <td>Impression univoche<br/> </td> 
   <td>Numero di utenti univoci a cui è stato recapitato il messaggio in-app.<br/> </td>
</tr>
 </tbody> 
</table>

## Metriche delle notifiche push

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
   <td> Numero totale di azioni sulla notifica push consegnate, ad esempio clic sul pulsante o rimozione.<br/> </td> 
</tr>
  <tr> 
   <td>Mancati recapiti<br/> </td> 
   <td> Totale degli errori accumulati durante la consegna e l'elaborazione automatica della restituzione in relazione al numero totale di messaggi inviati.<br/> </td> 
</tr> 
  <tr> 
   <td> Percentuale non recapitate<br/> </td> 
   <td> Percentuale di notifiche push non recapitate rispetto alle notifiche push inviate.<br/> </td>
</tr>
  <tr> 
   <td> Consegnato<br/> </td> 
   <td> Numero di messaggi inviati correttamente, in relazione al numero totale di messaggi inviati.<br/> </td> 
</tr> 
  <tr> 
   <td> Percentuale di consegna<br/> </td> 
   <td> Percentuale di notifiche push inviate correttamente.<br/> </td> 
</tr>
  <tr> 
   <td>Coinvolgimenti<br/> </td> 
   <td> Numero totale di aperture e azioni per questa notifica push, ovvero se il profilo ha aperto la notifica push o se è stato fatto clic su un pulsante.<br/> </td> 
</tr> 
  <tr> 
   <td> Tasso di coinvolgimento<br/> </td> 
   <td> Percentuale di aperture e azioni per questa notifica push, ovvero se il profilo ha aperto la notifica push o se è stato fatto clic su un pulsante.<br/> </td> 
</tr>
  <tr> 
   <td> Errori<br/> </td> 
   <td> Numero totale di errori che si sono verificati durante una consegna e che ne hanno impedito l'invio ai profili.<br/> </td> 
</tr>
  <tr> 
   <td> Frequenza errori<br/> </td> 
   <td> Percentuale di errori che si sono verificati durante una consegna che ne ha impedito l'invio rispetto alle notifiche push inviate.<br/> </td> 
</tr>
  <tr> 
   <td> Motivo errore<br/> </td> 
   <td> Nome della causa originale specifica dell’errore. <a href="exclusion-list.md">Ulteriori informazioni sui motivi dell'errore</a>.<br/> </td> 
</tr>
  <tr> 
   <td> Escluso<br/> </td> 
   <td> Numero di profili esclusi da Adobe Journey Optimizer.<br/> </td> 
</tr>
  <tr> 
   <td> Apertura di <br/> </td> 
   <td> Numero totale di notifiche push inviate al dispositivo e su cui gli utenti hanno fatto clic, aprendo in tal modo l’app. È simile al clic push, tranne per il fatto che l'apertura push non verrà attivata se la notifica viene chiusa.<br/> </td> 
</tr> 
  <tr> 
   <td> Percentuale aperture<br/> </td> 
   <td> Percentuale di notifiche push aperte.<br/> </td> 
</tr> 
  <tr> 
   <td> Inviato<br/> </td> 
   <td> Numero totale di invii per la consegna.<br/> </td> 
</tr> 
  <tr> 
   <td> Destinato<br/> </td> 
   <td> Numero totale di messaggi push elaborati durante l'analisi della consegna.<br/> </td> 
</tr>  
 </tbody> 
</table>

## Metriche della pagina di destinazione {#landing-page-metrics}

<table> 
 <thead> 
  <tr> 
   <th> Metrica<br/> </th> 
   <th> Definizione<br/> </th> 
</tr>
 </thead> 
 <tbody>
 <tr> 
  <td>Mancati recapiti<br/> </td> 
   <td>Numero di persone che non hanno interagito con la pagina di destinazione e non hanno completato l'azione di abbonamento.<br/> </td> 
</tr>
 <tr> 
   <td>Percentuale non recapitate<br/> </td> 
   <td>Numero di persone che non hanno interagito con la pagina di destinazione e non hanno completato l'azione di iscrizione, in relazione al numero totale di visite.<br/> </td> 
</tr>
 <tr>
  <tr> 
   <td>Clic<br/> </td> 
   <td>Numero di volte in cui è stato fatto clic su un contenuto nella pagina di destinazione.<br/> </td> 
</tr>
 <tr> 
   <td>Percentuale di clic<br/> </td> 
   <td>Percentuale di clic nella pagina di destinazione.<br/> </td>
</tr>
<tr>
<td>Conversione<br/> </td> 
   <td>Numero di persone che hanno interagito con la pagina di destinazione, ad esempio hanno effettuato l'abbonamento a un modulo.<br/> </td> 
</tr>
<tr>
   <td>Tasso di conversione<br/> </td> 
   <td>Numero di persone che hanno interagito con la pagina di destinazione, ad esempio hanno effettuato l'abbonamento a un modulo, in relazione al numero totale di visite.<br/> </td> 
</tr>
 <tr> 
   <td>Percorso/i<br/> </td> 
   <td>Numero di visite alla pagina di destinazione provenienti da un percorso.<br/> </td> 
</tr>
 <tr> 
   <td>Altre origini<br/> </td> 
   <td>Numero di visite alla pagina di destinazione provenienti da un'origine esterna anziché da un percorso.<br/> </td> 
</tr>
 <tr> 
   <td>Visite totali<br/> </td> 
   <td> Numero totale di visite alla pagina di destinazione provenienti da percorsi e origini esterne, incluse più visite di un destinatario.<br/> </td> 
</tr>
 <tr> 
   <td>Visitatori univoci<br/> </td> 
   <td>Numero di persone che hanno visitato la pagina di destinazione, non vengono prese in considerazione più visite di un destinatario.<br/> </td> 
</tr>
 <tr> 
   <td>Visite<br/> </td> 
   <td>Numero di visite alla pagina di destinazione, incluse più visite di un destinatario.<br/> </td> 
</tr>
 </tbody> 
</table>
