---
solution: Journey Optimizer
product: journey optimizer
title: Note pre-release per Journey Optimizer
description: Note pre-release di Adobe Journey Optimizer
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 3a44111345c1627610a6b026d7b19b281c4538d3
workflow-type: ht
source-wordcount: '591'
ht-degree: 100%

---

# Note pre-release {#e-release-notes}

[!DNL Adobe Journey Optimizer] offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. Nell’ultima settimana di ogni mese, tutte le modifiche vengono consolidate nelle [note sulla versione](release-notes.md).

**Le note pre-release riportate di seguito sono soggette a modifica senza preavviso fino alla data del rilascio della versione definitiva**. I collegamenti, le schermate e la documentazione aggiornata vengono pubblicati nelle [note sulla versione](release-notes.md), alla data di rilascio.


## Note pre-release di agosto 2025 {#25-7-rn}

**Le note pre-release riportate di seguito sono soggette a modifica senza preavviso fino alla data del rilascio della versione definitiva**. I collegamenti, le schermate e la documentazione aggiornata sono pubblicati alla data di rilascio.

Consulta anche [Note pre-release di Adobe Experience Platform](https://experienceleague.adobe.com/it/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Data di rilascio**: 19 agosto 2025


### Nuove funzionalità {#Aug-25-8-features}

Di seguito sono descritte le nuove funzionalità incluse in questa versione.

<table>
<thead>
<tr>
<th><strong>Mettere in pausa e riprendere i percorsi</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile mettere in pausa e riprendere i percorsi. Questa funzionalità offre ai professionisti del percorso maggiore controllo e flessibilità, consentendo di sospendere temporaneamente i percorsi live senza compromettere l’esperienza cliente. Quando il percorso è in pausa, le comunicazioni non vengono inviate e i profili rimangono in stato di sospensione fino a quando il percorso non viene ripreso.</p>
<p>È possibile mettere in pausa e riprendere un singolo percorso, oppure eseguire operazioni di pausa e di ripresa in blocco su un gruppo di percorsi.</p>
<p>Inoltre, è possibile applicare filtri globali ai percorsi in pausa per escludere i profili in base ai rispettivi attributi.</p>
<img src="assets/do-not-localize/PauseResume.gif">
<p>Precedentemente disponibile per un set limitato di clientela (disponibilità limitata), questa funzionalità è ora disponibile per tutti gli ambienti (disponibilità generale).</p>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/journey-pause.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>



<table>
<thead>
<tr>
<th><strong>Vista calendario</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Negli elenchi dei percorsi e delle campagne è ora disponibile una vista calendario. Consente di visualizzare tutte le attivazioni dei percorsi e delle campagne nei rispettivi elenchi.</p>
<p>Precedentemente rilasciata in versione a disponibilità limitata, questa funzione è ora disponibile per tutti gli ambienti. Con questa versione in disponibilità generale, la funzione include:</p>
<ul>
<li>Miglioramenti della progettazione per la navigazione tra date</li>
<li>Possibilità di visualizzare le campagne di bozza se hai impostato una data di inizio e una data di fine</li>
<li>Nuova impostazione per nascondere e visualizzare gli elementi del calendario in esecuzione per molto tempo</li>
</ul>
<img src="assets/do-not-localize/calendar.gif">
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/journey-ui.md#journeys-calendar">documentazione dettagliata</a></p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Modalità scura in E-mail designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>E-mail designer di Journey Optimizer ora offre la possibilità di passare alla visualizzazione in modalità scura, in cui è possibile definire anche impostazioni personalizzate specifiche da mostrare solo per i destinatari che leggono le e-mail in modalità scura.</p>
<p>Si noti quanto segue:</p>
<ul>
<li>Il rendering finale in modalità scura può variare e dipende dal client e-mail del destinatario.</li>
<li>Non tutti i client e-mail supportano la modalità scura personalizzata. Inoltre, alcuni client e-mail applicano soltanto la propria modalità scura predefinita per tutte le e-mail ricevute. In entrambi i casi, non è possibile eseguire il rendering delle impostazioni personalizzate definite in E-mail designer.</li>
</ul>
<P>Questa funzionalità è disponibile attualmente in versione beta e solo per la clientela beta. Per partecipare al programma Beta, contatta il tuo rappresentante Adobe.</p>
<p><img src="assets/do-not-localize/dark-mode.gif"/></p>
<p>Per ulteriori informazioni, consulta la <a href="../email/dark-mode.md">documentazione dettagliata</a>. </p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Ottimizzazione nelle campagne</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer ora offre gli strumenti necessari per fornire contenuti personalizzati e ottimizzati al pubblico delle campagne, consentendoti di eseguire esperimenti sui contenuti, creare targeting basato su regole e utilizzare combinazioni avanzate di entrambe queste attività per massimizzare l’efficacia delle campagne.</p>
<p>Con l'ottimizzazione è possibile:</p>
<ul>
<li>Testare più varianti di contenuto per identificare la messaggistica più efficace.</li>
<li>Distribuire contenuti personalizzati in base agli attributi utente e ai dati contestuali.</li>
<li>Combinare targeting e sperimentazione per strategie di campagna avanzate.</li>
<li>Escludere gli utenti che non corrispondono ai criteri della variante.</li>
<li>Includere meccanismi di fallback per mantenere vivo il coinvolgimento dell’utente.</li>
</ul>
<P>Una volta che la campagna è attiva, i profili vengono valutati in base ai criteri definiti e, secondo i criteri di corrispondenza, vengono consegnati con l’esperienza o il contenuto appropriato dalla campagna.</p>
<p><img src="assets/do-not-localize/campaign-optimization.gif"/></p>
<!--p>For more information, refer to the <a href="../FILE.md">detailed documentation</a></p-->
</td>
</tr>
</tbody>
</table>

### Miglioramenti {#Aug-25-8-improv}

Di seguito sono elencati i miglioramenti inclusi in questa versione.