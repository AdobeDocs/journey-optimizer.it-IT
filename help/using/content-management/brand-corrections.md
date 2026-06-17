---
solution: Journey Optimizer
product: journey optimizer
title: Correzioni del brand basate sull’intelligenza artificiale
description: Scopri come configurare e utilizzare le correzioni del brand basate sull’intelligenza artificiale in Adobe Journey Optimizer.
feature: Brand Guidelines
topic: Content Management
role: User
level: Intermediate
exl-id: a872a3a4-f05b-439d-923e-5191b6e06d34
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b6b77c26-2a48-4a62-9ceb-5ae67f4dfde5
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: a281a4d244279a6a1fce6968e4636b86414c4400
workflow-type: tm+mt
source-wordcount: 1000
ht-degree: 3%

---


# Correzioni del brand basate sull’intelligenza artificiale e suggerimenti editoriali {#brand-corrections-ai}

>[!AVAILABILITY]
>
>Questa funzionalità è disponibile per gli utenti di Adobe Journey Optimizer con linee guida per i marchi e adesioni AI Assistant attive. Per informazioni sull’accesso, contatta il rappresentante Adobe.

## Panoramica {#overview}

Adobe Journey Optimizer estende gli strumenti di conformità del brand basati su GenAI a tutti i canali di contenuti supportati: SMS, notifiche push, contenuti web ed e-mail. Quando il motore di controllo qualità del marchio rileva contenuti che violano le linee guida del marchio o non rispettano i criteri di qualità editoriali, il sistema genera automaticamente alternative corrette che puoi rivedere e applicare direttamente all’interno del flusso di lavoro di authoring.

In questo modo la convalida del brand da un elenco di controllo passivo diventa un’esperienza attiva e immediata. Invece di identificare le violazioni e tornare all’editor per risolvere manualmente ogni problema, gli autori dei contenuti ricevono suggerimenti mirati e generati dall’intelligenza artificiale, in linea con la voce del marchio, il tono e le linee guida di stile consolidate dell’organizzazione, il tutto senza uscire dall’editor dei contenuti.

Questa funzione è progettata per gli esperti di marketing dei contenuti, i copywriter e gli operatori delle campagne che devono spostare rapidamente i contenuti dalla bozza all’attivazione, mantenendo al contempo la conformità del brand su larga scala.

## Prerequisiti {#prerequisites}

Prima di utilizzare le correzioni del brand basate sull’intelligenza artificiale, conferma quanto segue:

- **Le linee guida per i marchi** sono configurate in Adobe Journey Optimizer. Senza un profilo di marchio attivo, il sistema non può generare suggerimenti di correzione allineati al brand.
- La funzionalità **Assistente AI** è abilitata per la tua organizzazione Adobe Experience Cloud.
- Disponi delle autorizzazioni appropriate per creare e modificare il contenuto per il canale rilevante (SMS, push, web o e-mail).
- Almeno un elemento di contenuto è disponibile per la revisione nell’editor di contenuti di Journey Optimizer.

>[!NOTE]
>
>I suggerimenti per la correzione del brand vengono generati utilizzando l’infrastruttura di intelligenza artificiale generativa di Adobe e sono soggetti ai criteri di utilizzo dell’Assistente di intelligenza artificiale applicabili alla tua organizzazione. Rivedi sempre i suggerimenti accettati prima di pubblicarli.

## Come funziona {#how-it-works}

Le correzioni del brand si integrano direttamente nel flusso di convalida del controllo qualità dei brand all’interno dell’editor di contenuti Journey Optimizer. Il processo end-to-end funziona come segue.

**Passaggio 1 — Analisi controllo qualità del marchio**: quando esegui un controllo di convalida del brand sul contenuto, manualmente dal pannello di revisione o attivato da una regola del flusso di lavoro, il sistema valuta ogni blocco di contenuto in base alle linee guida del brand configurate. I controlli riguardano il tono della voce, la terminologia, il linguaggio vietato, gli standard editoriali e i requisiti normativi.

**Passaggio 2: rilevamento e segnalazione di violazioni**: qualsiasi segmento di contenuto che non soddisfa i criteri di qualità editoriale o di marchio viene contrassegnato con un indicatore di violazione. Il tipo di violazione, ad esempio mancata corrispondenza dei toni, utilizzo di termini non consentiti o mancata conformità alle linee guida, viene visualizzato accanto al segmento contrassegnato in modo che gli autori possano capire esattamente cosa deve essere modificato.

**Passaggio 3 — Generazione di suggerimenti AI**: per ogni segmento contrassegnato, Journey Optimizer genera automaticamente una o più alternative corrette utilizzando l&#39;Assistente AI. I suggerimenti si basano sulle linee guida del tuo marchio attivo, per garantire che il testo consigliato rifletta la voce, la terminologia e lo stile editoriale corretti specifici per la tua organizzazione.

**Passaggio 4 — Anteprima e revisione in linea**: le correzioni suggerite vengono visualizzate in linea, direttamente accanto al contenuto contrassegnato nel pannello laterale Controllo di qualità del marchio. Puoi confrontare il testo originale con l’alternativa generata dall’intelligenza artificiale senza uscire dall’editor.

**Passaggio 5 — Accettare o chiudere**: accettare un suggerimento con un solo clic per sostituire il contenuto contrassegnato con la versione corretta. In alternativa, ignora il suggerimento e modifica manualmente il contenuto. L’accettazione di un suggerimento aggiorna immediatamente il blocco di contenuto e contrassegna la violazione come risolta nel pannello Controllo qualità.

**Passaggio 6 — Nuova convalida**: dopo aver applicato le correzioni, rieseguire l&#39;analisi di controllo qualità del marchio per verificare che tutte le violazioni siano state risolte prima di pubblicare o attivare il contenuto in un percorso o in una campagna.

## Configura {#configure}

Non è necessaria alcuna configurazione aggiuntiva oltre ai prerequisiti standard. La funzione si attiva automaticamente nel pannello Controllo qualità del brand quando un profilo del brand è associato al contenuto e l’Assistente AI è abilitato per la tua organizzazione.

Per iniziare a utilizzare le correzioni del brand basate sull’intelligenza artificiale:

1. Apri l’editor di contenuti per il canale pertinente: SMS, notifica push, web o e-mail.
2. Nella barra degli strumenti dell&#39;editor, seleziona **Linee guida per i marchi** e scegli il profilo del marchio applicabile dal menu a discesa.
3. Crea la bozza o apri il contenuto, quindi seleziona **Controllo qualità marchio** dal pannello di revisione per avviare una scansione.
4. Rivedi le violazioni segnalate nel pannello laterale **Controllo qualità marchio**. Per ogni elemento contrassegnato, viene visualizzato automaticamente un suggerimento generato dall’intelligenza artificiale.
5. Fai clic su **Applica** per accettare un suggerimento, oppure su **Ignora** per gestire la correzione manualmente.
6. Esegui nuovamente **Controllo qualità marchio** per verificare che tutte le violazioni siano state risolte, quindi procedi con il flusso di lavoro standard di approvazione o attivazione.

### Canali supportati {#supported-channels}

In Adobe Journey Optimizer sono disponibili correzioni del brand basate sull’intelligenza artificiale per i seguenti tipi di contenuto:

| Canale | Elementi di contenuto supportati |
|---|---|
| **E-mail** | Oggetto, preintestazione, corpo del testo, etichette CTA |
| **SMS** | Corpo del messaggio |
| **Notifiche push** | Titolo, corpo del testo |
| **Web** | Etichette titolo, corpo del testo e pulsante |

>[!NOTE]
>
>Gli elementi di contenuto supportati possono variare a seconda della configurazione del canale e delle linee guida del brand definite nel profilo del brand. La convalida di immagini e risorse visive non rientra nell’ambito delle correzioni di testo generate dall’intelligenza artificiale.

## Vantaggi chiave {#key-benefits}

**Riduzione delle operazioni manuali di modifica**: gli autori dei contenuti non dovranno più utilizzare riferimenti incrociati manuali alle linee guida del brand per ogni problema segnalato. I suggerimenti di IA emergono come alternative pronte da applicare, riducendo notevolmente il tempo impiegato nel ciclo di correzione.

**Coerenza con il marchio**: le correzioni si basano sulle stesse linee guida del marchio utilizzate per la convalida. I suggerimenti accettati mantengono la coerenza con gli standard editoriali e vocali del marchio approvati su tutti i canali, riducendo il rischio di messaggi incoerenti nelle campagne multicanale.

**Produzione più rapida dei contenuti**: trasformando il controllo qualità del brand in un flusso di lavoro ottimizzato e immediato, i team spostano i contenuti durante il ciclo di revisione più rapidamente, riducendo il tempo di risposta tra la bozza e l&#39;attivazione. Gli operatori di Campaign possono risolvere un intero set di violazioni in un singolo passaggio senza passare da uno strumento all’altro.

**Copertura cross-channel**: sia che si produca una campagna SMS, una sequenza push mobile o un messaggio in-app web, i suggerimenti di correzione del brand sono disponibili in modo coerente su tutte le superfici di contenuto supportate, garantendo il rispetto degli standard del brand ovunque il brand comunichi.

## Argomenti correlati {#related-topics}

- [Guida introduttiva alle linee guida per i marchi](../content-management/brands.md)
- [Utilizzare l’Assistente AI per la generazione di contenuti](../content-management/ai-assistant.md)
- [Creare un messaggio SMS](../sms/create-sms.md)
- [Creare una notifica push](../push/create-push.md)
- [Introduzione al canale Web](../web/get-started-web.md)
- [Anteprima e test del contenuto](../content-management/preview-test.md)
