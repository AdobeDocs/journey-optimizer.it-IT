---
solution: Journey Optimizer
product: journey optimizer
title: Note sulla versione
feature: Release Notes
topic: Content Management
description: Note sulla versione di Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: e29586f24f6ef84869a277ae6121d83f962405f7
workflow-type: tm+mt
source-wordcount: '1328'
ht-degree: 64%

---

# Note sulla versione {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Novità"
>abstract="**Adobe Journey Optimizer** offre continuamente nuove funzioni, miglioramenti a quelle esistenti e correzioni di bug. Nelle presenti note sulla versione, tutte le modifiche sono consolidate durante l’ultima settimana di ogni mese."

[!DNL Adobe Journey Optimizer] offre continuamente nuove funzioni, miglioramenti alle funzioni esistenti e correzioni di bug. Nelle presenti note sulla versione, tutte le modifiche sono consolidate durante l’ultima settimana di ogni mese. [!DNL Adobe Journey Optimizer] è stato sviluppato in modalità nativa su [!DNL Adobe Experience Platform] e ne eredita le innovazioni e i miglioramenti più recenti. Ulteriori informazioni su queste modifiche nelle [Note sulla versione di Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=it){target="_blank"}.


## Note sulla versione di marzo 2025 {#25-3-rn}


### Nuove funzionalità {#25-03-features}

Di seguito sono descritte le nuove funzionalità incluse in questa versione.

<table>
<thead>
<tr>
<th><strong>Integrazione con Adobe Express (disponibilità limitata)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>L’integrazione di Adobe Express in Adobe Journey Optimizer consente di utilizzare gli strumenti di modifica di Adobe Express direttamente durante la creazione dei contenuti, per ridimensionare, rimuovere gli sfondi, ritagliare e convertire le risorse in JPEG o PNG.<p>
<p>L’integrazione di Adobe Express in Adobe Journey Optimizer è attualmente disponibile solo per un set di organizzazioni (disponibilità limitata). Non può essere utilizzato con Healthcare Shield o Privacy and Security Shield.</p>
<p>Per ulteriori informazioni, consulta la <a href="../integrations/express.md">documentazione dettagliata</a>.</p>
</br>
<img src="assets/do-not-localize/express_resize.gif"/>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Metriche di percorso</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Sono ora disponibili le metriche di percorso, che consentono di misurare l’impatto delle attività sulle metriche chiave dell’azienda e fornire informazioni più chiare sulle prestazioni.</p>
<p>Per ulteriori informazioni, consulta la <a href="../building-journeys/success-metrics.md">documentazione dettagliata</a>.</p>
<img src="assets/do-not-localize/success-metric.gif"/>
</td>
</tr>
</tbody>
</table>

<!-- table>
<thead>
<tr>
<th><strong>Calendar view for journeys (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A calendar view is now available in Journey Optimizer to visualize all journeys activations. From this view, you can browse your journeys and check details and properties.<p>
<p>This change is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<p>For more information, refer to the <a href="../configuration/rule-sets.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Integrazione con Dynamic Media (disponibilità limitata)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Le risorse Dynamic Media sono ora direttamente disponibili e accessibili in Journey Optimizer. Questa integrazione consente di:
<ul>
<li>Gestione centralizzata delle risorse con aggiornamenti in tempo reale</li>
<li>Modifica istantaneamente le impostazioni delle risorse, ad esempio larghezza e altezza</li>
<li>Personalizza i modelli Dynamic Media aggiornando i contenuti e aggiungendo campi di personalizzazione</li>
</ul>
<p>
<p>Questa integrazione è disponibile solo per un set di organizzazioni (disponibilità limitata). Per ottenere l’accesso, contatta il tuo rappresentante Adobe.</p>
<p>Per ulteriori informazioni, consulta la <a href="../integrations/aem-dynamic.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>



<table>
<thead>
<tr>
<th><strong>Integrazione con Adobe GenStudio (disponibilità limitata)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Per migliorare l’efficienza del marketing e mantenere la coerenza del marchio, ora puoi integrare perfettamente le esperienze GenStudio for Performance Marketing con Journey Optimizer. Questo consente di sfruttare la creazione di contenuti basati sull’intelligenza artificiale di GenStudio insieme alle funzionalità avanzate di orchestrazione di Journey Optimizer.<p>
<p>L'utilizzo dell'integrazione GenStudio in Journey Optimizer non è attualmente disponibile con Healthcare Shield o Privacy and Security Shield (Disponibilità limitata).</p>
<p>Per ulteriori informazioni, consulta la <a href="../integrations/genstudio.md">documentazione dettagliata</a>.</p>
<img src="assets/do-not-localize/genstudio.gif"/>
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>LINE channel (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer has expanded its cross-channel capabilities to include support for the LINE channel. This enhancement allows you to create, edit, and preview LINE experiences enabling more personalized and engaging interactions. With LINE, you can connect with more customers, send relevant content, and improve your engagement.<p>
<p>This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<p>For more information, refer to the <a href="../configuration/rule-sets.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->


### Miglioramenti {#25-03-improv}

**Editor Personalization** (data di disponibilità: 12 marzo)

L’editor di personalizzazione di Journey Optimizer è stato aggiornato con nuove funzionalità:
* **Progettazione dell’editor di codice aggiornata**: un’interfaccia più pulita e moderna per migliorare l’usabilità e la concentrazione.
* **Cerca e sostituisci**: una funzionalità aggiunta per trovare e sostituire rapidamente i contenuti all’interno dell’editor.
* **Supporto Annulla e Ripristina**: consente di ripristinare o riapplicare facilmente le modifiche.
* **Dimensione del font personalizzabile** : consente di regolare la dimensione del font dell’editor per una migliore leggibilità.
* **Convalida JSON in linea**: fornisce la convalida lato client in tempo reale per il contenuto JSON per accelerare il rilevamento degli errori.
* **Completamento automatico per attributi di profilo e di contesto**: offre suggerimenti avanzati per semplificare la creazione di contenuti.
* **Evidenziazione della sintassi migliorata**: migliora la leggibilità rendendo la struttura del codice visivamente più distinta.

![Video che mostra la nuova funzionalità nell&#39;editor di Personalization](assets/do-not-localize/personalization-editor.gif)

Per ulteriori informazioni, consulta la [documentazione dettagliata](../personalization/personalization-build-expressions.md).

**Approvazioni**

Quando si definiscono le condizioni per un criterio di approvazione, è ora possibile filtrare in base a Tag e/o Categoria oggetto.

**Configurazione**

* Ora puoi assegnare Tag unificati Adobe Experience Platform alle configurazioni dei canali. Ciò ti consente di classificarli facilmente e di migliorare la ricerca e la navigazione in tutti gli elenchi. [Ulteriori informazioni](../configuration/channel-surfaces.md#channel-config-tags)

* Quando imposti o modifichi un sottodominio e-mail in Journey Optimizer, ora puoi scegliere di gestire autonomamente il record DMARC associato, se disponibile sul dominio principale. [Ulteriori informazioni](../configuration/dmarc-record.md#set-up-dmarc)

**Regole aziendali**

Ora puoi utilizzare il limite di frequenza giornaliero in percorsi e campagne con segmentazione batch. Per garantire la precisione delle regole di quota limite giornaliera, assicurati di scegliere lo spazio dei nomi con la priorità più elevata durante la creazione di una campagna o di un percorso. Ulteriori informazioni sulla priorità dello spazio dei nomi nella [guida del servizio Platform Identity](https://experienceleague.adobe.com/en/docs/experience-platform/identity/features/identity-graph-linking-rules/namespace-priority){target="_blank"}

Come promemoria, il limite di frequenza giornaliero nei set di regole è disponibile solo per un set di organizzazioni (disponibilità limitata). Per ottenere l’accesso, contatta il tuo rappresentante Adobe.

Per ulteriori informazioni sulle regole business, consulta la [documentazione dettagliata](../configuration/rule-sets.md).

<!--**Content management**

To easily manage your fragments and your content templates, you can now use folders to organize them more effectively into a structured hierarchy. This improvement is only available for a set of organizations (Limited Availability). <!--To gain access, contact your Adobe representative.

**Deliverability**

You can now choose to have your emails relayed to your SMTP servers instead of being sent directly from Journey Optimizer to ISPs. This allows you to route final email deliveries through your own Mail Transfer Agents and IPs, or to perform final validations on the emails before sending them to your recipients. The SMTP relay capacity is available on demand - contact your Adobe representative.-->


## Note sulla versione di febbraio 2025 {#25-02-rn}

<!--
**Early release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published at the release date.-->

**Data di rilascio**: 18-19 febbraio 2025


### Nuove funzionalità {#25-02-features}

Di seguito sono descritte le nuove funzionalità incluse in questa versione.

<table>
<thead>
<tr>
<th><strong>Creare e gestire le regole di business</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>È ora possibile creare regole di business utilizzando i set di regole. I set di regole sono gruppi di regole che ti aiutano a limitare i messaggi inviati all’interno di campagne e azioni di un percorso per i diversi canali e a controllare l’ingresso dei profili nei percorsi.<p>
<p><ul><li>Crea set di regole di canale per limitare il numero di messaggi inviati su uno o più canali. Applicali alle campagne o alle azioni dei percorsi per applicare le regole definite nel set di regole. Il set di regole del canale consente di applicare regole di limitazione in base ai tipi di comunicazione. Ad esempio, puoi impostare un set di regole per limitare i “messaggi promozionali” e un altro per le “newsletter”. Applica il set di regole appropriato alla campagna o all’azione di un percorso in base al tipo di comunicazione da inviare.</li>
<li> Crea set di regole per i percorsi, per controllare l’ingresso dei profili nei percorsi. Limita la frequenza con cui un profilo può effettuare l’ingresso in un percorso in un determinato periodo o il numero di percorsi in cui può essere registrato simultaneamente. Applicali a livello di percorso per garantire una corretta gestione degli ingressi.</li></ul></p>
<p>Precedentemente disponibile per un set di organizzazioni (LA), le regole aziendali sono ora disponibili per tutti gli utenti (GA). Le regole business del dominio di percorso continuano a essere disponibili solo per un set limitato di organizzazioni (LA).</p>
<p>Per ulteriori informazioni, consulta la <a href="../configuration/rule-sets.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Generare pagine di destinazione con l’Assistente IA</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi usare l’Assistente IA per creare contenuti coinvolgenti per le pagine di destinazione, tra cui progettazioni di pagine intere, testo personalizzato e immagini personalizzate.</p>
<img src="assets/do-not-localize/ai-lp.gif">
<p>Per ulteriori informazioni, consulta la <a href="../content-management/generative-lp.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Brand con l’Assistente IA (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi impostare i tuoi brand per definirne l’identità visiva e verbale. </p>
<p>Questa funzionalità viene rilasciata come versione beta privata a un set limitato di clienti. Sarà disponibile progressivamente per tutta la clientela nelle prossime versioni.</p>
<p>Per ulteriori informazioni, consulta la <a href="../content-management/brands.md">documentazione dettagliata</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Risolvere i problemi relativi alle azioni personalizzate</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Ora puoi convalidare una configurazione di azione personalizzata effettuando chiamate API reali direttamente da Adobe Journey Optimizer. Questa nuova funzionalità consente di risolvere i problemi relativi alle azioni personalizzate prima o dopo il loro utilizzo in un percorso. </p>
<p>Per ulteriori informazioni, consulta la <a href="../action/troubleshoot-custom-action.md">documentazione dettagliata</a>.</p>
<!--p> This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Valutazione flessibile del pubblico (LA, disponibilità limitata)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La valutazione flessibile del pubblico consente di eseguire un processo di segmentazione su richiesta per i tipi di pubblico selezionati, per disporre sempre dei dati del pubblico più aggiornati prima di eseguirne il targeting in percorsi e campagne Journey Optimizer.</p>
<img src="assets/do-not-localize/flexible-audience.gif">
<p>Per ulteriori informazioni, consulta la <a href="../audience/creating-a-segment-definition.md#flexible">documentazione dettagliata</a>.</p>
<p>Questa funzionalità è disponibile solo per un set di organizzazioni (LA, disponibilità limitata). Per ottenere l’accesso, contatta il tuo rappresentante Adobe.</p>
<p>Data di disponibilità: 28 gennaio 2025</p>
</tr>
</tbody>
</table>
</table>


### Miglioramenti {#25-02-improvements}

I miglioramenti riportati di seguito sono inclusi nell’aggiornamento di febbraio.

* **Impostazione time-to-live (TTL) del set di dati**: a partire da questo mese, verrà introdotto un guardrail time-to-live (TTL) nei set di dati di Journey Optimizer generati dal sistema in nuove sandbox e nuove organizzazioni come segue:

   * 90 giorni per i dati nell’archivio dei profili
   * 13 mesi per i dati nel data lake

  In una fase successiva, questa modifica verrà implementata nelle sandbox della clientela esistente.

  Ulteriori informazioni su questo aggiornamento sono disponibili nelle [Domande frequenti dedicate](../data/datasets-ttl.md#frequently-asked-questions).

<!--* **Playbooks** - You can now create and publish your own Use Case Playbooks in Journey Optimizer.-->

* **Direct mail**: un nuovo tipo di server, Data Landing Zone, è ora supportato per il routing dei file nella configurazione del canale direct mail. [Ulteriori informazioni](../direct-mail/direct-mail-configuration.md#file-routing-configuration)

* **SMS**: è ora possibile gestire la consegna di messaggi SMS da endpoint multiregionali sovrascrivendo gli URL di consegna, feedback, in entrata e callback. Per supportare questa funzione, è stato aggiunto il nuovo campo URL di sostituzione alla configurazione delle credenziali API. Questa modifica è disponibile solo con il provider Sinch. [Ulteriori informazioni](../sms/sms-configuration-sinch.md)

* **Personalizzazione** (data di disponibilità: 29 gennaio 2025): nuove funzioni helper data/ora sono disponibili per l’utilizzo nell’editor di personalizzazione. [Ulteriori informazioni](../personalization/functions/dates.md)


<!--
* The personalization editor has been enhanced with new capabilities such as Auto-complete, Search, and filtering options. You can also show or hide deprecated attributes.-->


* **Configurazione e-mail**: se gestisci il consenso al di fuori di Adobe, ora puoi impostare un indirizzo e-mail personalizzato per l’annullamento dell’iscrizione e un URL personalizzato per l’annullamento dell’iscrizione con un solo clic, come parte delle impostazioni di configurazione del canale e-mail.[Ulteriori informazioni](../email/list-unsubscribe.md#custom-managed)

  ![](../email/assets/surface-list-unsubscribe-custom.png){width="80%"}

* **Decisioni** (data di disponibilità: 28 gennaio 2025): la funzione Decisioni ora supporta i tipi di dati Oggetto durante la modifica dello schema del catalogo elementi. [Ulteriori informazioni](../experience-decisioning/catalogs.md)

