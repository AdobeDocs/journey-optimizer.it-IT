---
solution: Journey Optimizer
product: journey optimizer
title: Elenco dei componenti
description: Scopri come utilizzare i dati del tuo rapporto
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: aa060d8e-23e2-4bab-b709-636077eb5d20
source-git-commit: be0a240f73e884fd91798952167e81689aa2ae2f
workflow-type: tm+mt
source-wordcount: '2134'
ht-degree: 0%

---

# Elenco delle metriche {#list-of-components-global}

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
<td>Coinvolgimento percorso</td> 
<td>Numero totale di individui univoci che hanno ricevuto messaggi inviati tramite il percorso, che rappresentano profili distinti che hanno raggiunto un punto di azione designato nel percorso.</td> 
</tr> 
<tr> 
<td>Entrate percorso</td> 
<td>Numero totale di individui che hanno raggiunto l'evento di ingresso del percorso.</td> 
</tr>
<tr> 
<td>Uscite dal percorso</td> 
<td>Numero totale di persone che sono uscite dal percorso.</td> 
</tr>
<tr> 
<td>Errori di percorso</td> 
<td>Numero totale di singoli percorsi non eseguiti correttamente.</td> 
</tr>
<tr> 
<td>Entrate Percorso univoche</td> 
<td>Numero totale di individui che hanno raggiunto l’evento di ingresso del percorso, senza considerare più interazioni dello stesso profilo.</td> 
</tr>
<tr> 
<td>Uscite da Percorso univoche</td> 
<td>Numero totale di individui che sono usciti dal percorso, senza considerare più interazioni dello stesso profilo.</td> 
</tr>
<tr> 
<td>Errori di Percorso univoci</td> 
<td>Numero totale di singoli percorsi non eseguiti correttamente, senza tenere conto di più interazioni dello stesso profilo.</td> 
</tr>
 </tbody> 
</table>

## Metriche e-mail {#email-metrics}

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
   <td> Percentuale di messaggi e-mail che hanno generato un mancato recapito rispetto al numero totale di messaggi e-mail inviati.<br/> </td> 
  </tr> 
  <tr> 
   <td> Percentuale di apertura dei clic (CTOR)<br/> </td> 
   <td> Numero di volte in cui l'e-mail è stata aperta.<br/> </td> 
  </tr>
  <tr> 
   <td> Percentuale di click-through (CTR)<br/> </td> 
   <td> Percentuale di utenti che hanno interagito con l'e-mail.<br/> </td> 
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
   <td> Motivo errore<br/> </td> 
   <td> Nome della causa originale specifica dell’errore. <a href="exclusion-list.md">Ulteriori informazioni sui motivi dell'errore</a>.<br/> </td> 
  </tr>
  <tr> 
   <td>Aperture e-mail stimate<br/> </td> 
   <td>Stima del totale di aperture e-mail che tiene conto sia delle aperture dirette da parte dei profili sia delle aperture automatizzate attivate dai server di posta. Questa metrica viene regolata per le aperture attivate dai server di posta per l'analisi della privacy o della sicurezza applicando una percentuale di apertura calcolata dai destinatari che hanno aperto manualmente l'e-mail a quelli le cui e-mail sono state aperte solo dai server di posta.<br/> </td> 
  </tr>
  <tr> 
   <td> Percentuale di clic offerta<br/> </td> 
   <td> Percentuale di utenti che hanno interagito con l'offerta.<br/> </td> 
  </tr>
  <tr> 
   <td> Percentuale di impression offerta<br/> </td> 
   <td> Percentuale di offerte aperte rispetto al numero di offerte inviate.<br/> </td> 
  </tr>
  <tr> 
   <td> Nome offerta<br/> </td> 
   <td> Nome dell’offerta aggiunta alla consegna. Per ulteriori informazioni sul posizionamento, consulta questa <a href="../offers/offer-library/creating-personalized-offers.md">pagina</a>.<br/> </td> 
  </tr>
  <tr> 
   <td> Offerta inviata<br/> </td> 
   <td> Numero totale di invii per l'offerta.<br/> </td> 
  </tr> 
  <tr> 
   <td> Apertura di <br/> </td> 
   <td> Numero di volte in cui il messaggio è stato aperto.<br/> </td> 
  </tr> 
  <tr> 
   <td> Errori di invio<br/> </td> 
   <td> Numero totale di errori che si sono verificati durante il processo di invio e che ne hanno impedito l'invio ai profili.<br/> </td> 
  </tr> 
  <tr> 
   <td> Invia esclusioni<br/> </td> 
   <td> Numero di profili esclusi da Adobe Journey Optimizer.<br/> </td> 
  </tr>
  <tr> 
   <td> Nome posizionamento<br/> </td> 
   <td> Nome del posizionamento utilizzato per visualizzare l’offerta. Per ulteriori informazioni sul posizionamento, consulta questa <a href="../offers/offer-library/creating-placements.md">pagina</a>. </td> 
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
   <td>Mancati recapiti univoci<br/> </td> 
   <td> Numero di profili univoci per i quali almeno un’e-mail ha generato un mancato recapito.</td> 
  </tr>
  <tr> 
   <td>Percentuale non recapitate univoche<br/> </td> 
   <td>Percentuale di profili univoci le cui e-mail non venivano recapitate almeno una volta, in base al numero totale di invii univoci.</td> 
  </tr>
  <tr> 
   <td> Clic univoci<br/> </td> 
   <td> Numero di profili che hanno fatto clic su un contenuto in un messaggio e-mail.<br> Tieni presente che nel calcolo dei clic univoci vengono considerati gli ultimi 10 giorni. Se un profilo registra più clic entro il periodo di 10 giorni, verranno conteggiati come clic univoci. Tuttavia, se un profilo ha 2 clic a distanza di oltre 10 giorni, non verrà considerato come clic univoci.<br/> </td> 
  </tr>
  <tr> 
   <td>Percentuale di apertura click-through univoca<br/> </td> 
   <td> Percentuale di profili univoci che hanno fatto clic su un collegamento dopo l’apertura dell’e-mail, in base alle aperture univoche. </td> 
  </tr>
  <tr> 
   <td> Percentuale di click-through univoca<br/> </td> 
   <td> Percentuale di profili univoci che hanno fatto clic su almeno un collegamento nell’e-mail, rispetto al numero di e-mail consegnate univoche. </td> 
  </tr>
  <tr> 
   <td> Consegne univoche<br/> </td> 
   <td> Numero di profili univoci che hanno ricevuto almeno un’e-mail.</td> 
  </tr>
  <tr> 
   <td> Annullamenti iscrizione e-mail univoci<br/> </td> 
   <td> Numero di profili che hanno annullato l'abbonamento alle e-mail.<br/> </td> 
  </tr>
  <tr> 
   <td> Aperture e-mail stimate univoche<br/> </td> 
   <td> Stima del numero di destinatari e-mail univoci che probabilmente hanno aperto l’e-mail. Questa metrica ha lo scopo di fornire un conteggio più accurato del coinvolgimento individuale attivato dai server di posta elettronica per l'analisi della privacy o della sicurezza applicando un tasso di apertura univoco calcolato da profili univoci che hanno aperto manualmente l'e-mail a coloro i cui messaggi di posta elettronica sono stati aperti solo dai server di posta.<br/> </td> 
  </tr>
  <tr> 
   <td> Aperture univoche<br/> </td> 
   <td> Numero di profili che hanno aperto la consegna. <br> Tieni presente che nel calcolo delle aperture univoche vengono considerati gli ultimi 10 giorni. Se un profilo registra più aperture entro il periodo di 10 giorni, queste verranno conteggiate come aperture univoche. Tuttavia, se un profilo ha 2 aperture a più di 10 giorni di distanza, non verranno considerate come aperture univoche.<br/> </td> 
  </tr> 
  <tr>
  <tr> 
   <td> Invii univoci<br/> </td> 
   <td>Numero di profili univoci per i quali è stato tentato l'invio di almeno un messaggio e-mail.<br/> </td> 
  </tr>
  <tr> 
   <td> Errori di invio univoci<br/> </td> 
   <td>Numero di profili univoci che hanno rilevato almeno un errore di invio durante il processo in uscita.<br/> </td> 
  </tr>
  <tr> 
   <td> Esclusioni di invio univoche<br/> </td> 
   <td>Numero di profili univoci esclusi dalla ricezione dei messaggi a causa di regole di idoneità, segmentazione del pubblico o stato del profilo.<br/> </td> 
  </tr>
  <tr> 
   <td>Destinazione univoca<br/> </td> 
   <td>Numero di profili univoci target durante il processo di invio.<br/> </td> 
  </tr> 
  <tr> 
   <td> Annulla iscrizione<br/> </td> 
   <td> Numero di clic sul collegamento di annullamento dell'abbonamento.<br/> </td> 
  </tr> 
 </tbody> 
</table>

## Metriche SMS

<table> 
  <thead> 
    <tr> 
      <th> Metrica SMS </th> 
      <th> Definizione </th> 
    </tr>
  </thead> 
  <tbody> 
    <tr> 
      <td>Consegnate</td> 
      <td>Numero di messaggi SMS inviati correttamente, in relazione al numero totale di messaggi SMS.</td> 
    </tr>
    <tr> 
      <td>Clic</td> 
      <td>Numero di volte in cui è stato fatto clic su un collegamento all’interno di un messaggio SMS.</td> 
    </tr>
    <tr> 
      <td>Mancati recapiti per messaggi SMS in uscita</td> 
      <td>Numero totale di errori accumulati durante il processo di invio e l’elaborazione automatica della restituzione in relazione al numero totale di messaggi SMS inviati.</td> 
    </tr>
    <tr> 
      <td>Errori SMS in uscita</td> 
      <td>Numero totale di errori che hanno impedito l’invio del messaggio SMS ai destinatari.</td> 
    </tr>
    <tr> 
      <td>Esclusioni SMS in uscita</td> 
      <td>Numero di profili esclusi dalla ricezione di messaggi SMS da parte di Adobe Journey Optimizer.</td> 
    </tr>
    <tr> 
      <td>Clic univoci</td> 
      <td>Numero di destinatari univoci che hanno fatto clic su un collegamento in un messaggio SMS.</td> 
    </tr>
    <tr> 
      <td>Visualizzazioni</td> 
      <td>Numero di volte in cui un messaggio SMS è stato visualizzato o aperto.</td> 
    </tr>
    <tr> 
      <td>Display univoci</td> 
      <td>Numero di destinatari univoci che hanno aperto il messaggio SMS, escludendo più interazioni dallo stesso utente.</td> 
    </tr>
    <tr> 
      <td>People</td> 
      <td>Numero di profili utente univoci che hanno ricevuto o interagito con un messaggio SMS.</td> 
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
   <td> Percentage improvement in conversion rate of a given treatment over the baseline.<a href="../campaigns/experiment-calculations.md#understand-lift">Learn more</a>.<br/> </td> 
  </tr>
  <tr> 
   <td>Confidence<br/> </td> 
   <td>Evidence that a given treatment is the same as the baseline treatment. <a href="../campaigns/experiment-calculations.md#understand-confidence">Learn more</a>.<br/> </td> 
</tr>
  <tr> 
   <td>Confidence interval<br/> </td> 
   <td>Percentage difference in performance between the baseline and the best performing treatment. <a href="../campaigns/experiment-calculations.md#understand-intervals">Learn more</a>.<br/> </td> 
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
   <td>Number of profiles who opened the email.<br/> </td>
<tr>
  <tr> 
   <td>Unique email unsubscribes<br/> </td> 
   <td>Number of profiles who clicked on the unsubscription link.<br/> </td>
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
   <td>Numero totale di profili che hanno interagito con i pulsanti inclusi nel messaggio in-app.<br/> </td> 
  </tr>
  <tr> 
   <td>Percentuale di clic<br/> </td> 
   <td>Percentuale di utenti che hanno interagito con i pulsanti inclusi nel messaggio in-app rispetto agli utenti che hanno visualizzato il messaggio.<br/> </td> 
  </tr>
  <tr> 
   <td>Percentuale ignorati<br/> </td> 
   <td>Percentuale di messaggi in-app ignorati dai profili.<br/> </td> 
  </tr>
  <tr> 
   <td>Impression<br/> </td> 
   <td>Numero totale di messaggi in-app recapitati a tutti gli utenti.<br/> </td>
  </tr>
  <tr> 
   <td>Impression univoche<br/> </td> 
   <td>Numero di utenti univoci a cui è stato recapitato il messaggio in-app.<br/> </td>
  </tr>
  <tr> 
   <td>Visualizza<br/> </td>
   <td>Numero di volte in cui il messaggio in-app è stato aperto.<br/> </td>
  </tr>
  <tr> 
   <td>Visualizzazioni univoche<br/> </td>
   <td>Numero di volte in cui il messaggio in-app è stato aperto, escludendo più interazioni dallo stesso profilo.<br/> </td>
  </tr>
  <tr> 
   <td>Clic univoci<br/> </td>
   <td>Numero di profili che hanno fatto clic sul contenuto nei messaggi in-app.<br/> </td>
  </tr>
  <tr> 
   <td>Clic<br/> </td>
   <td>Numero di volte in cui è stato fatto clic sul contenuto nei messaggi in-app.<br/> </td>
  </tr>
  <tr> 
   <td>Percentuale di click-through (CTR)<br/> </td>
   <td>Percentuale di utenti che hanno interagito con i messaggi in-app.<br/> </td>
  </tr>
  <tr> 
   <td>Percentuale di apertura dei clic (CTOR)<br/> </td>
   <td>Numero di volte in cui il messaggio in-app è stato aperto.<br/> </td>
  </tr>
  <tr> 
   <td>Invia <br/> </td>
   <td>Numero totale di messaggi in-app inviati.<br/> </td>
  </tr>
  <tr> 
   <td>Attivato in entrata<br/> </td>
   <td>Numero di volte in cui un messaggio in-app è stato attivato da un'interazione dell'utente o da un evento predefinito.<br/> </td>
  </tr>
  <tr> 
   <td>Notifiche in entrata ignorate<br/> </td>
   <td>Numero di volte in cui gli utenti hanno ignorato il messaggio in-app senza interagire con esso.<br/> </td>
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
   <td> Azioni personalizzate push<br/> </td> 
   <td>Numero di azioni personalizzate eseguite dai profili in risposta alle notifiche push.<br/> </td> 
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
   <td>Percentuale non recapitate<br/> </td> 
   <td>Percentuale di persone che hanno visualizzato la pagina di destinazione ma non hanno interagito o effettuato l'abbonamento, rispetto al numero totale di visite.<br/> </td> 
</tr>
 <tr> 
   <td>Clic<br/> </td> 
   <td>Numero di volte in cui è stato fatto clic su un contenuto nella pagina di destinazione.<br/> </td> 
</tr>

<tr> 
   <td>Conversione pagina di destinazione<br/> </td> 
   <td>Numero di persone che hanno interagito con la pagina di destinazione, ad esempio, hanno effettuato l'abbonamento a un modulo.<br/> </td> 
</tr>
<tr> 
   <td>Tasso di conversione pagina di destinazione<br/> </td> 
   <td>Percentuale di persone che hanno interagito con la pagina di destinazione, ad esempio, hanno effettuato l'abbonamento a un modulo, rispetto al numero totale di visite.<br/> </td> 
</tr>
 <tr> 
   <td>Visualizzazioni della pagina di destinazione<br/> </td> 
   <td>Numero totale di visite alla pagina di destinazione da percorsi e origini esterne, incluse più visite dallo stesso profilo.<br/> </td> 
</tr>
<tr> 
   <td>Conversioni pagina di destinazione univoche<br/> </td> 
   <td>Numero di persone univoche che hanno interagito con la pagina di destinazione, escludendo più interazioni dallo stesso profilo.<br/> </td> 
</tr>
 <tr> 
   <td>Visualizzazioni pagina di destinazione univoche<br/> </td> 
   <td>Numero di persone univoche che hanno visitato la pagina di destinazione, escludendo più visite dallo stesso profilo.<br/> </td> 
</tr>
 </tbody> 
</table>

## Direct mail {#direct-mail}

<table> 
 <thead> 
  <tr> 
   <th> Metrica<br/> </th> 
   <th> Definizione<br/> </th> 
  </tr>
 </thead> 
 <tbody>
<tr> 
   <td>Consegnato<br/> </td> 
   <td>Numero di messaggi di direct mailing recapitati correttamente ai destinatari.<br/> </td> 
</tr>
<tr> 
   <td>Errori in uscita<br/> </td> 
   <td>Numero di messaggi di direct mailing che hanno rilevato errori durante l'elaborazione o l'invio, impedendo il corretto recapito.<br/> </td> 
</tr>
<tr> 
   <td>Esclusioni in uscita<br/> </td> 
   <td>Numero di profili esclusi dalla ricezione della direct mailing a causa di criteri predefiniti o filtro da parte di Adobe Journey Optimizer.<br/> </td> 
</tr>
<tr> 
   <td>Profili<br/> </td> 
   <td>Numero di profili utente identificati come pubblico target per la campagna di direct mailing.<br/> </td> 
</tr>
<tr> 
   <td>Inviato<br/> </td> 
   <td>Numero totale di messaggi di direct mailing inviati correttamente come parte della campagna.<br/> </td> 
</tr>
<tr> 
   <td>Destinato<br/> </td> 
   <td>Numero totale di messaggi di direct mailing preparati ed elaborati per l'invio.<br/> </td> 
</tr>
 </tbody> 
</table>


## Metriche delle schede di contenuto {#content-based}

<table> 
 <thead> 
  <tr> 
   <th> Metrica<br/> </th> 
   <th> Definizione<br/> </th> 
  </tr>
 </thead> 
 <tbody>
<tr> 
   <td>Percentuale di click-through (CTR)<br/> </td> 
   <td>Percentuale di utenti che hanno interagito con la scheda Contenuto.<br/> </td> 
</tr>
<tr> 
   <td>Clic<br/> </td> 
   <td>Numero di volte in cui è stato fatto clic su un contenuto nella scheda Contenuto.<br/> </td> 
</tr>
<tr> 
   <td>Visualizza<br/> </td> 
   <td>Numero di volte in cui il messaggio è stato aperto.<br/> </td> 
</tr>
<tr> 
   <td>Persone<br/> </td> 
   <td>Numero di profili utente qualificati come profili target per le schede di contenuto.<br/> </td> 
</tr>
<tr> 
   <td>Clic univoci<br/> </td> 
   <td>Numero di profili che hanno fatto clic su un contenuto nella scheda Contenuto.<br/> </td> 
</tr>
<tr> 
   <td>Visualizzazioni univoche<br/> </td> 
   <td>Numero di volte in cui il messaggio è stato aperto. Non vengono prese in considerazione più interazioni di un profilo.<br/> </td> 
</tr>
 </tbody> 
</table>

## Metriche delle pagine web {#web}

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
   <td>Numero di volte in cui è stato fatto clic su un contenuto nelle pagine Web.<br/> </td> 
</tr>
<tr> 
   <td>Percentuale di click-through (CTR)<br/> </td> 
   <td>Percentuale di utenti che hanno interagito con le pagine Web.<br/> </td> 
</tr>
<tr> 
   <td>Visualizza<br/> </td> 
   <td>Numero di volte in cui la pagina Web è stata aperta.<br/> </td> 
</tr>
<tr> 
   <td>Persone<br/> </td> 
   <td>Numero di profili idonei come profili target per le pagine Web.<br/> </td> 
</tr>
<tr> 
   <td>Clic univoci<br/> </td> 
   <td>Numero di profili che hanno fatto clic su un contenuto nelle pagine Web.<br/> </td> 
</tr>
<tr> 
   <td>Visualizzazioni univoche<br/> </td> 
   <td>Numero di volte in cui la pagina Web è stata aperta, non vengono prese in considerazione più interazioni di un profilo.<br/> </td> 
</tr>
 </tbody> 
</table>

## Metriche delle esperienze basate su codice {#code-based}

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
   <td>Numero totale di volte in cui gli utenti hanno fatto clic su esperienze personalizzate che sono state visualizzate.<br/> </td> 
</tr>
<tr> 
   <td>Tasso di click-through (CTR)<br/> </td> 
   <td>Percentuale di utenti che fanno clic su un collegamento, un annuncio pubblicitario o un consiglio rispetto al numero di volte in cui è stato visualizzato.<br/> </td> 
</tr>
<tr> 
   <td>Tasso di conversione<br/> </td> 
   <td>Percentuale di visualizzazioni che hanno generato azioni dell'utente (ad esempio, clic), a indicare il successo del modello nel coinvolgere gli utenti.<br/> </td> 
</tr>
<tr> 
   <td>Prestazioni Elementi Decisione<br/> </td> 
   <td>Valuta le prestazioni di ogni elemento nel coinvolgimento degli utenti e nell'esecuzione delle azioni desiderate, ad esempio acquisti, clic o altre risposte.<br/> </td> 
</tr>
<tr> 
   <td>Decisioning degli indicatori KPI<br/> </td> 
   <td>Informazioni chiave sul coinvolgimento dei visitatori con le esperienze, inclusi elementi totali, clic totali, visualizzazioni totali e tasso di fallback.<br/> </td> 
</tr>
<tr> 
   <td>Visualizza<br/> </td> 
   <td>Numero totale di volte in cui sono state mostrate o presentate agli utenti esperienze personalizzate attraverso vari punti di contatto.<br/> </td> 
</tr>
<tr> 
   <td>Coinvolgimento Funnel<br/> </td> 
   <td>Monitora le prestazioni delle esperienze personalizzate valutando l'efficacia di ogni fase di funnel nel determinare le interazioni degli utenti.<br/> </td> 
</tr>
<tr> 
   <td>Coinvolgimento Funnel per strategia di selezione<br/> </td> 
   <td>Esegue il monitoraggio e l'analisi dell'efficacia con cui le diverse strategie di selezione coinvolgono gli utenti con esperienze personalizzate.<br/> </td> 
</tr>
<tr> 
   <td>Persone<br/> </td> 
   <td>Numero di profili utente qualificati come profili target per le esperienze basate su codice.<br/> </td> 
</tr>
<tr> 
   <td>Strategia di classificazione<br/> </td> 
   <td>Informazioni sulle prestazioni dei modelli di classificazione basati sull'intelligenza artificiale confrontando due tipi di traffico: Basato su modello e Holdout.<br/> </td> 
</tr>
<tr> 
   <td>Elementi decisionali principali per CTR<br/> </td> 
   <td>Evidenzia le prestazioni dei singoli elementi in base al relativo CTR (Click-through Rate), consentendo di valutare quali elementi sono più efficaci per coinvolgere gli utenti.<br/> </td> 
</tr>
<tr> 
   <td>Clic univoci<br/> </td> 
   <td>Numero di profili che hanno fatto clic su un contenuto nelle esperienze basate su codice.<br/> </td> 
</tr>
<tr> 
   <td>Visualizzazioni univoche<br/> </td> 
   <td>Numero di volte in cui l'esperienza è stata aperta, non vengono prese in considerazione più interazioni di un profilo.<br/> </td> 
</tr>
 </tbody> 
</table>
