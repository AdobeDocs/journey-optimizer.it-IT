---
solution: Journey Optimizer
product: journey optimizer
title: Guida alla richiesta di informazioni sui contenuti dell’Assistente AI
description: Scopri come creare prompt efficaci per la generazione di contenuti basati sull’intelligenza artificiale utilizzando il framework CO-STAR per creare contenuti di marketing ad alta conversione e allineati al brand.
role: User
level: Intermediate
source-git-commit: 5063115c6ac93ef332044bfff43a4df817a1a4e3
workflow-type: tm+mt
source-wordcount: '2107'
ht-degree: 1%

---

# Best practice per la richiesta di Assistente AI {#ai-assistant-prompting-guide}

>[!CONTEXTUALHELP]
>id="ajo_ai_assistant_prompt"
>title="Esempi di prompt"
>abstract="Esplora la documentazione di Journey Optimizer per scoprire come creare prompt efficaci per produrre contenuti di marketing on-brand ad alta conversione."

Questa guida ti aiuta a strutturare le richieste, comunicare le intenzioni con chiarezza e garantire che l’intelligenza artificiale produca messaggi in linea con le linee guida del tuo marchio, le esigenze del pubblico e gli obiettivi della campagna.
Scopri come scrivere prompt efficaci che consentano all’Assistente AI di generare contenuti di marketing di alta qualità e personalizzati per i tuoi obiettivi.

## Utilizzare il framework CO-STAR {#costar-framework}

Per ottenere risultati ottimali con l’Assistente AI, organizza le richieste utilizzando il framework CO-STAR. Questo approccio strutturato assicura che l’intelligenza artificiale comprenda esattamente ciò di cui hai bisogno.

| Componente | Che cosa significa | Perché è importante |
|-|-|-|
| **C - Contesto** | Informazioni sulla campagna, sul prodotto o sulla situazione | Aiuta l’intelligenza artificiale a comprendere il quadro generale |
| **O - Obiettivo** | Il tuo obiettivo di marketing specifico | Guida gli obiettivi dei contenuti |
| **S - Stile** | Modalità di comunicazione | Imposta l&#39;approccio |
| **T - Tono** | Stile e voce emotivi | Forma l&#39;impatto del messaggio |
| **A - Pubblico** | Pubblico di destinazione | Assicura che il messaggio risuonino con le persone giuste |
| **R - Requisiti** | Vincoli specifici o requisiti obbligatori | Definisce limiti ed elementi critici |

## Nozioni di base sui prompt di IA {#key-takeaways}


### Cosa fare e cosa non fare


<table style="table-layout: fixed; width: 100%; border: 0;">
<thead style="border: 0; background-color: #FFFFFF;">
<tr>
<th>Esegui</th>
<th>Non</th>
</tr>
</thead>
<tbody>
<tr style="border: 0;">
<td>
<p>Utilizzare il framework CO-STAR per la struttura</p>
<p>Chiarezza sui contenuti nuovi rispetto a quelli esistenti</p>
<p>Attenzione all’utilizzo dei documenti con indicazioni specifiche sull’estrazione</p>
<p>Utilizza selezioni a discesa per il tono, la strategia e le impostazioni internazionali</p>
<p>Corrispondenza tra obiettivi di marketing e funzionalità per tipi di contenuto</p>
<p>Generare più varianti per il test A/B</p>
</td>
<td>
<p>Richiedere modifiche strutturali, stili o modifiche di immagini nei prompt</p>
<p>Menziona tono/strategia nei prompt, se disponibile nei menu a discesa</p>
<p>Utilizzare obiettivi vaghi come "promuovere il nostro prodotto"</p>
<p>Richiedi selezioni elementi condizionali</p>
<p>Prevista modifica del layout tramite prompt</p>
</td>
</tr>
</tbody>
</table>

### Contenuto non supportato nei prompt

>[!TIP]
>
>Utilizza l&#39;**editor e-mail** o **Adobe Express** per le modifiche visive/delle immagini.

Queste richieste non sono supportate e devono essere gestite tramite altri strumenti:

<table style="table-layout: fixed; border: 0;">
<thead style="border: 0; background-color: #FFFFFF">
<tr>
<th>✕ Modifiche alla struttura delle e-mail</th>
<th>✕ Modifiche allo stile visivo</th>
<th>✕ operazioni di modifica delle immagini</th>
</tr>
</thead>
<tbody>
<tr style="border: 0;">
<td>
<ul>
<li>Selezione di sezioni specifiche da modificare</li>
<li>Eliminazione o clonazione di elementi</li>
<li>Selezioni condizionali</li>
<li>Aggiunta o rimozione di sezioni layout</li>
</ul>
</td>
<td>
<ul>
<li>Formattazione del testo (grassetto, corsivo, dimensione carattere)</li>
<li>Modifiche colore</li>
<li>Stile layout (bordi, spaziatura interna, margini)</li>
<li>Effetti visivi (ombre)</li>
</ul>
</td>
<td>
<ul>
<li>Modifiche di sfondo</li>
<li>Aggiunta di sovrapposizioni di testo o logo</li>
<li>Ritaglio o ridimensionamento delle immagini</li>
<li>Regolazioni colore</li>
<li>Sostituzione immagine</li>
</ul>
</td>
</tr>
</tbody>
</table>

### Lista di controllo qualità {#quality-checklist}

Prima di generare il contenuto, verifica quanto segue:

&check; **Cancella obiettivo**: indica chiaramente l&#39;azione, il prodotto/servizio, il valore e il contesto.

&check; **Pubblico di destinazione definito**: specifica il gruppo demografico, la mansione o il segmento.

&check; **Allineamento tipo di contenuto**: l&#39;obiettivo corrisponde al canale o al formato selezionato.

&check; **Selezioni a discesa configurate**: vengono scelte il tono, la strategia e le impostazioni locali, non includerle nel prompt.

&check; **Stato attivo documento specificato**: evidenzia il contenuto o le sezioni a cui fare riferimento.

&check; **Marchio applicato**: sono state selezionate le linee guida del marchio appropriate.

&check; **Ambito realistico**: evita richieste di modifiche di layout, stile o struttura.

## Scrivi obiettivi di marketing efficaci {#marketing-objectives}

### Essere specifici e orientati alle azioni

Quando definisci gli obiettivi di marketing, assicurati che siano chiari, utilizzabili e misurabili. Evita istruzioni vaghe o generiche.

**Esempi di obiettivi validi:**

&check; &quot;Effettua le iscrizioni per la prova gratuita di 30 giorni del nuovo dashboard di analisi basato sull’intelligenza artificiale&quot;

&check; &quot;Genera lead per il nostro webinar B2B su &quot;Riduzione dei costi cloud del 40%&quot; in programma il 15 marzo&quot;

&check; &quot;Promuovi il nostro sconto limitato 25% sulle vacanze sugli abbonamenti premium, fino al 25 dicembre&quot;

**Esempi da evitare:**

✕ &quot;Promuovi il nostro prodotto&quot; (troppo vago)

✕ &quot;Fai acquistare alle persone&quot; (valore non chiaro)

✕ &quot;E-mail sulle nuove funzioni&quot; (manca lo scopo)

### Strutturare l&#39;obiettivo

Fornisci sempre contesto e proposta di valore in modo che l’intelligenza artificiale possa generare contenuti rilevanti.
Usa questa formula per scrivere obiettivi efficaci: **Azione + Prodotto/Servizio + Valore/Beneficio + Urgenza/Contesto**

**Esempi di obiettivi validi:**

&check; &quot;Incoraggia il download della nostra nuova app mobile che aiuta gli utenti a tenere traccia di abitudini di vita sostenibili con consigli personalizzati ed ecocompatibili&quot;

&check; &quot;Promuovi la registrazione per il nostro workshop esclusivo sulle tecniche avanzate di visualizzazione dei dati per i professionisti del marketing&quot;

&check; &quot;Aumenta la partecipazione all’evento di lancio del prodotto presentando il rivoluzionario assistente di scrittura AI che consente di risparmiare più di 5 ore a settimana&quot;

**Esempi da evitare:**

✕ &quot;Annuncio nuova app&quot; (proposta di valore e contesto mancanti)

✕ &quot;Iscrivi le persone al workshop&quot; (manca specificità su pubblico e vantaggi)

✕ &quot;Promuovi evento&quot; (nessuna azione, valore o urgenza chiari)

## Creare nuovi contenuti e modificare quelli esistenti {#new-vs-modify}

Indica chiaramente se la richiesta comporta la generazione di nuovo contenuto o l&#39;aggiornamento del materiale esistente. Questa distinzione è importante perché guida l’intelligenza artificiale nella selezione dell’approccio appropriato e garantisce un risultato più accurato e utile.

### Creazione di nuovi contenuti

Applica questa strategia quando avvii campagne di marketing, sveli nuovi prodotti o avvii qualsiasi tipo di comunicazione aggiornata o aggiornata. In questo modo il messaggio inizia forte e si allinea agli obiettivi.

**Come richiedere** ➤ Quando crei un nuovo contenuto, concentrati sul tuo obiettivo di marketing senza fare riferimento a contenuto esistente.

>[!BEGINSHADEBOX]

**Esempi:**

* **Prova SaaS**: &quot;Lancia il nostro nuovo software CRM per i proprietari di piccole imprese, evidenziando il 50% di risparmio di tempo, il 90% più veloce di qualificazione del lead e offrendo una prova gratuita di 30 giorni con onboarding personalizzato&quot;
* **Annuncio sulle funzionalità**: &quot;Annuncio di nuove funzionalità di integrazione API che riducono i tempi di sviluppo del 60% per i clienti aziendali, con targeting per i decision-maker tecnici&quot;
* **Promozione evento**: &quot;Registrazioni di unità per il nostro webinar su &#39;Tendenze di marketing digitale 2024&#39; con esperti di Google, Meta e Adobe, enfatizzando informazioni fruibili e postazioni limitate (massimo 500)&quot;

>[!ENDSHADEBOX]

### Modifica del contenuto esistente

>[!TIP]
>
>Per le modifiche standard, quali elaborate, riepilogate o semplificate, utilizzare la funzione **Perfeziona** invece di scrivere prompt personalizzati. [Ulteriori informazioni](generative-uc.md##refine)

Applica questa opzione quando devi aggiornare, aggiornare o adattare le campagne di marketing correnti. Questo metodo supporta miglioramenti incrementali, garantendo che i messaggi rimangano pertinenti senza iniziare da zero.

**Come richiedere** ➤ Quando modifichi il contenuto esistente, specifica chiaramente ciò che desideri modificare e come modificarlo.

>[!BEGINSHADEBOX]

**Esempi:**

* **Aggiornamento campagna**: &quot;Modifica l&#39;e-mail di lancio del prodotto per concentrarti sulle funzionalità di sicurezza aziendale anziché sui vantaggi generali in termini di produttività, indirizzando i responsabili IT con certificazioni di conformità&quot;
* **Audience Pivot**: &quot;Adatta il nostro invito demo software per indirizzare specificamente l&#39;assistenza sanitaria, sostituendo esempi generici con casi di utilizzo dell&#39;assistenza sanitaria e vantaggi in termini di conformità HIPAA&quot;
* **Aggiornamento stagionale**: &quot;Aggiorna la nostra campagna promozionale Q3 per lo shopping per le vacanze Q4, cambiando l&#39;attenzione dal back-to-school al regalo per le vacanze con l&#39;enfasi della spedizione rapida&quot;

>[!ENDSHADEBOX]

## Migliora il prompt con le impostazioni avanzate {#personalize-prompt}

### Tipi di strategie di comunicazione

>[!TIP]
>
>Utilizza il menu a discesa Strategia di comunicazione dal menu Impostazioni testo invece di menzionarlo nella richiesta di elaborazione specializzata.

La tua strategia di comunicazione determina il modo in cui presenterai il messaggio per massimizzare l’impatto. Diverse strategie funzionano meglio per diversi obiettivi, che tu stia costruendo l&#39;urgenza, stabilendo la fiducia, o guidando l&#39;azione immediata. Scegli la strategia che meglio si allinea agli obiettivi della campagna e alla mentalità del pubblico.

| **Strategia** | **Ottimo Per** | **Stile di messaggistica** | **Esempi** |
|--------------|--------------|------------------------|--------------|
| **Urgente** | Offerte sensibili al tempo, scadenze, azioni immediate | Crea una pressione immediata con un linguaggio basato sul tempo | &quot;Agisci subito: l&#39;offerta scade a mezzanotte&quot; <br> &quot;Registrati oggi prima che gli spot si riempiscano&quot; <br> &quot;La vendita flash di 48 ore inizia ora&quot; |
| **FOMO (paura di perdere)** | Offerte limitate, eventi, accesso esclusivo | Utilizza segnali di urgenza, scarsità e pressione temporale | &quot;Mancano solo 24 ore! Stock limitati al 40% di sconto&quot; <br> &quot;Ultima possibilità: il prezzo anticipato degli uccelli termina domani&quot; <br> &quot;Rimangono solo 100 punti beta&quot; |
| **Bozza social** | Trust-building, testimonianze, prodotti popolari | Sfrutta le esperienze altrui e la convalida | &quot;Unisciti a più di 50.000 clienti soddisfatti&quot; <br> &quot;Valutazione di 4,9/5 stelle da parte di professionisti del settore&quot; <br> &quot;Affidabile alle aziende Fortune 500&quot; |
| **Scarsità** | Scorte limitate, rilasci esclusivi, articoli a forte domanda | Evidenzia la disponibilità e l&#39;esclusività limitate | &quot;Rimangono solo 5 unità&quot; <br> &quot;Edizione limitata: 100 unità disponibili&quot; <br> &quot;Rilascio esclusivo: primo arrivato, primo servito&quot; |
| **Incentivo** | Promozioni, programmi di premi, offerte speciali | Vantaggi e ricompense tangibili | &quot;Ottieni il 20% di sconto sul tuo primo ordine&quot; <br> &quot;Guadagna due punti questo weekend&quot; <br> &quot;Spedizione gratuita su ordini superiori a $50&quot; |
| **Esclusività** | Prodotti Premium, esperienze VIP, offerte per soli membri | Utilizza il posizionamento premium e un linguaggio ad accesso speciale | &quot;Invito esclusivo all&#39;anteprima privata&quot; <br> &quot;L&#39;iscrizione Elite sblocca le analisi avanzate&quot; <br> &quot;Partecipa a determinate aziende Fortune 500 che già ci utilizzano&quot; |
| **Gamification** | Campagne di coinvolgimento, programmi fedeltà, contenuti interattivi | Utilizza meccaniche di gioco e linguaggio di realizzazione | &quot;Sblocca il tuo prossimo livello di ricompensa&quot; <br> &quot;Completa le sfide per guadagnare distintivi&quot; <br> &quot;Scala la classifica dei premi esclusivi&quot; |
| **Informativo** | Istruzione, ricerca, prodotti complessi, leadership di pensiero | Utilizza fatti, dati, informazioni e spiegazione | &quot;5 approfondimenti dall&#39;analisi di oltre 10.000 interazioni&quot; <br> &quot;Nuova ricerca rivela 3 approcci rivoluzionari&quot; <br> &quot;Guida completa all&#39;implementazione dell&#39;intelligenza artificiale nel marketing&quot; |
| **Istruzione e approfondimenti** | Contenuti di apprendimento, tendenze del settore, best practice | Fornisce conoscenze preziose e soluzioni actionable | &quot;Padroneggia le tecniche avanzate con la nostra guida di esperti&quot; <br> &quot;Scopri le 7 strategie utilizzate dai principali esperti di marketing&quot; <br> &quot;Scopri come ottimizzare il flusso di lavoro in 5 passaggi&quot; |

### Imposta il tono giusto {#tone}

>[!TIP]
>
>Anziché specificarlo nel prompt, utilizzare il menu a discesa Tono del menu Impostazioni testo.

Il tono determina il modo in cui il pubblico percepisce il messaggio e lo risponde. Seleziona sempre un tono che sia allineato alla voce del brand e all’area di visualizzazione del percorso di profili.

Utilizza la tabella seguente per esplorare ogni tono in dettaglio, tra cui quando funziona meglio ed esempi di contenuto che si adattano a ogni stile.

| Tonalità | Ideale per | Esempio di contenuto |
|-|-|-|
| Professionale | Comunicazioni B2B, annunci formali | &quot;Siamo lieti di annunciare la nostra partnership strategica...&quot; |
| Empatico | Assistenza clienti, argomenti sensibili | &quot;Capiamo quanto questo debba essere frustrante per te...&quot; |
| Umoristico | Campagne coinvolgenti, contenuti dal cuore leggero | &quot;Avvertenza: può causare gravi aumenti di produttività!&quot; |
| Eccitante | Lancio di prodotti, promozioni di eventi | &quot;Questo è il momento che stavi aspettando!&quot; |
| Ispirativo | Campagne motivazionali, scopo del brand | &quot;Insieme possiamo fare la differenza nel mondo...&quot; |
| Persuasivo | Campagne di vendita, conversioni | &quot;Non perdete questa opportunità limitata di...&quot; |
| Amichevole | Coinvolgimento del cliente, messaggi di benvenuto | &quot;Siamo così felici che tu sia qui con noi!&quot; |
| Formale | Comunicazioni legali, comunicazioni ufficiali | &quot;Con la presente ti notifichiamo le seguenti modifiche...&quot; |
| Scusante | Ripristino del servizio, risoluzione dei problemi | &quot;Ci scusiamo sinceramente per qualsiasi disagio causato...&quot; |
| Assertivo | Contenuto di leadership, messaggistica autorevole | &quot;Ecco cosa devi fare in questo momento...&quot; |
| Narrazione | Racconti del brand, connessioni emotive | &quot;Tutto è iniziato con una semplice domanda...&quot; |
| Conversazionale | Campagne di sviluppo, creazione di relazioni | &quot;Parliamo di come questo possa aiutarti...&quot; |

### Ottimizzare le risorse del brand {#brand-assets}

>[!TIP]
>
>Se hai già caricato una risorsa del brand tramite il menu **Brand Assets**, non devi farvi riferimento nella richiesta. Il sistema utilizza automaticamente tutti i documenti selezionati.

Le risorse per i marchi forniscono informazioni fattuali che arricchiscono i contenuti generati con dettagli specifici e precisi.
Quando carichi ampi documenti, ad esempio brochure di prodotti, aggiungi al prompt quali parti concentrarsi su:

* **Anziché** _&quot;Utilizzare la brochure del prodotto&quot;_ **utilizzare** _&quot;Concentrarsi sulle funzionalità di sicurezza avanzate e sulle certificazioni di conformità, in particolare sulla conformità SOC 2 e sulla crittografia dei dati&quot;_

* **Anziché** _&quot;Fare riferimento ai casi di studio&quot;_ **utilizzare** _&quot;Evidenziare i risultati del ROI dai clienti del settore sanitario, in particolare la riduzione dei costi del 40% presso il Centro medico regionale&quot;_

* **Invece di** _&quot;Includi dettagli tecnici&quot;_ **devi utilizzare** _&quot;Enfatizzare le funzionalità di integrazione API e i vantaggi per gli sviluppatori, concentrandoti sugli endpoint REST API e sul 99,9% di uptime SLA&quot;_

### Perfezionamento dei contenuti

>[!TIP]
>
>Utilizza la funzione Perfeziona invece di chiedere conferma quando desideri elaborare, riepilogare, semplificare, modificare il tono o tradurre il contenuto esistente. [Ulteriori informazioni](generative-uc.md#refine)

Una volta generato il contenuto, utilizzare la funzionalità **Perfeziona** per eseguire iterazioni e migliorarle con le opzioni seguenti:

| **Azione** | **Caso d&#39;uso** | **Esempio di richiesta** |
|-|-|-|
| **Elaborare** | Aggiungere profondità e dettagli al contenuto breve | &quot;Approfondisci i vantaggi tecnici delle nostre caratteristiche di sicurezza&quot; |
| **Riepiloga** | Riduci la lunghezza dei contenuti per diversi formati | &quot;Riepiloga questa panoramica del prodotto per un post sui social media&quot; |
| **Semplifica** | Rendere più accessibili i contenuti complessi | &quot;Semplificare questa spiegazione tecnica per un pubblico generale&quot; |
| **Cambia tono** | Adattare i contenuti per tipi di pubblico diversi | &quot;Cambiare tono a più informale per i giovani&quot; |
| **Trasforma** | Adattamento culturale oltre la traduzione | &quot;Trasforma questa campagna per il mercato giapponese&quot; |

## Esempi di prompt basati su scenari

### In base al tipo di contenuto {#content-type-practices}

<table style="table-layout: fixed; border: 0;">
<thead>
<tr style="border: 0;background-color: #FFFFFF;">
<th>Canale</th>
<th>Esempio</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>E-mail</strong></td>
<td>"Sviluppare i potenziali clienti aziendali presentando tre storie di successo dei clienti con metriche dettagliate sul ROI (IBM: riduzione dei costi del 45%, Accenture: aumento del lead del 200%, Microsoft: risparmio di tempo del 60%), indirizzando i responsabili IT alle aziende con più di 1000 dipendenti"</td>
</tr>
<tr>
<td><strong>SMS</strong></td>
<td>"Avvisa i clienti VIP circa 4 ore di vendita flash su elettronica premium con il 40% di sconto, limitato ai primi 100 clienti"</td>
</tr>
<tr>
<td><strong>Notifiche push</strong></td>
<td>"Coinvolgi nuovamente gli utenti che non aprono l’app da 7 giorni con contenuti personalizzati consigliati in base alla cronologia di lettura"</td>
</tr>
<tr>
<td><strong>Pagine di destinazione</strong></td>
<td>"Convertire i visitatori B2B in lead qualificati dimostrando come la nostra soluzione di sicurezza aziendale impedisce il 99,9% degli attacchi informatici, con testimonianze Fortune 500 e audit di sicurezza gratuiti"</td>
</tr>
</tbody>
</table>

### Basato su approcci specifici del settore {#industry-approaches}

<table style="table-layout: fixed; border-collapse: collapse; border: 0;">
<thead>
<tr style="border: 0;background-color: #FFFFFF;">
<th>Settore</th>
<th>Esempio di prompt</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Tecnologia B2B</strong></td>
<td>"Dimostrare il ROI e le specifiche tecniche affrontando al tempo stesso i problemi di sicurezza per i responsabili delle decisioni IT che valutano la nostra soluzione di infrastruttura cloud, sottolineando il 99,9% di tempo di attività di SLA, la conformità SOC 2 e il 40% di risparmio sui costi".</td>
</tr>
<tr>
<td><strong>Vendita al dettaglio e-commerce</strong></td>
<td>"Crea urgenza intorno agli articoli per le vacanze con scorte limitate, evidenziando la spedizione gratuita e facili ritorni per gli acquirenti dell’ultimo minuto, evidenziando quantità limitate (meno di 50 rimanenti) e 24 ore di interruzione della spedizione."</td>
</tr>
<tr>
<td><strong>Servizi finanziari</strong></td>
<td>"Educare i clienti sulle strategie di diversificazione del portafoglio di investimenti, mantenendo al contempo la conformità normativa, con informazioni certificate di esperti finanziari e disclaimer sui rischi".</td>
</tr>
<tr>
<td><strong>Sanità e benessere</strong></td>
<td>"Promuovi i vantaggi delle cure preventive e controlli annuali dello stato di salute mantenendo l'accuratezza medica, con consigli del medico certificati dal consiglio di amministrazione e garanzie sulla privacy dei pazienti."</td>
</tr>
<tr>
<td><strong>Istruzione e formazione</strong></td>
<td>"Sottolineare i risultati di avanzamento di carriera e le certificazioni del settore mostrando al contempo le competenze degli istruttori, evidenziando il tasso di collocamento del 92% e i programmi di studio basati su progetti."</td>
</tr>
<tr>
<td><strong>Piattaforme SaaS</strong></td>
<td>"Evidenzia i vantaggi in termini di risparmio di tempo e automazione con metriche specifiche, affrontando al contempo i problemi di integrazione, con risparmi di tempo settimanali medi di 25 ore e integrazione con oltre 200 strumenti popolari".</td>
</tr>
</tbody>
</table>
