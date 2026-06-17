---
solution: Journey Optimizer
product: journey optimizer
title: Correzioni del brand basate sull’intelligenza artificiale
description: Scopri come configurare e utilizzare le correzioni del brand basate sull’intelligenza artificiale in Adobe Journey Optimizer.
feature: Brand Validation
topic: Content Management
role: User
level: Intermediate
exl-id: dd4fde0e-86c8-4a57-86ba-202e3be2c41f
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2: id: c96d2aa5-76a2-443d-8d23-5de95577c909
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b6b77c26-2a48-4a62-9ceb-5ae67f4dfde5
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: a281a4d244279a6a1fce6968e4636b86414c4400
workflow-type: tm+mt
source-wordcount: 993
ht-degree: 1%

---


# Correzioni del brand basate sull’intelligenza artificiale {#brand-corrections}

>[!AVAILABILITY]
>
>Questa funzionalità è disponibile per Adobe Journey Optimizer e si applica ai canali di contenuti push, SMS e web.

## Panoramica {#overview}

Quando il contenuto viene contrassegnato durante il Controllo qualità del marchio, Adobe Journey Optimizer può generare automaticamente alternative testuali corrette o migliorate utilizzando l’intelligenza artificiale generativa. Invece di riscrivere manualmente la copia contrassegnata, puoi ricevere suggerimenti in linea in linea con le linee guida del tuo marchio, che puoi rivedere, visualizzare in anteprima e applicare con un solo clic.

In questo modo il passaggio del Controllo di qualità del marchio da gate di revisione bloccati a **esperienza di correzione**, riducendo il tempo impiegato per le correzioni manuali e accelerando la produzione di contenuti tra i canali.

Questa funzione è stata progettata per gli esperti di marketing dei contenuti, i copywriter e gli operatori delle campagne che devono mantenere la conformità al marchio in campagne multicanale di grandi volumi senza rallentare i flussi di lavoro di produzione.

## Come funziona {#how-it-works}

Il controllo qualità del brand in Adobe Journey Optimizer valuta i contenuti rispetto alle linee guida del brand della tua organizzazione, inclusi il tono della voce, la terminologia, gli standard di messaggistica e le regole editoriali. Quando viene rilevata una violazione o un problema di qualità, il sistema contrassegna l’elemento di contenuto interessato e, se supportato, genera automaticamente una sostituzione consigliata utilizzando il motore di intelligenza artificiale generativo di Adobe.

Il flusso end-to-end è il seguente:

1. **Analisi controllo qualità marchio**: quando esegui un controllo del marchio sul contenuto (corpo della notifica push, testo del messaggio SMS o blocco di contenuto Web), il sistema valuta ogni elemento in base alle regole del marchio attive.
2. **Rilevamento violazioni** — Gli elementi che non soddisfano uno o più criteri del marchio vengono contrassegnati con un indicatore di gravità (ad esempio critico, di avvertenza o di suggerimento).
3. **Generazione di suggerimenti AI**: per ogni elemento contrassegnato, il sistema genera automaticamente una o più alternative testuali corrette. I suggerimenti sono prodotti dal motore di intelligenza artificiale generativo di Adobe, che è consapevole sia del motivo della violazione che del contesto delle linee guida del tuo marchio.
4. **Anteprima in linea** - Il testo sostitutivo suggerito viene visualizzato in linea, direttamente accanto all&#39;originale contrassegnato. Puoi confrontare le versioni originale e quella suggerita una accanto all’altra prima di apportare qualsiasi modifica.
5. **Applicazione con un solo clic** - Se il suggerimento soddisfa le tue esigenze, seleziona **Applica** per sostituire il testo contrassegnato con la versione generata da IA. L’editor dei contenuti viene aggiornato immediatamente e il contrassegno del brand viene cancellato.
6. **Sostituzione manuale** - Non sei mai bloccato nel suggerimento di intelligenza artificiale. Puoi modificare il suggerimento prima di applicarlo, ignorarlo e scrivere una correzione personalizzata oppure ignorare completamente il flag se il contesto richiede un’eccezione.

>[!NOTE]
>
>I suggerimenti generati dall’intelligenza artificiale sono solo consigli. Il tuo team mantiene il pieno controllo editoriale. Rivedi sempre i suggerimenti nel contesto della campagna prima di applicarli.

## Prerequisiti {#prerequisites}

Prima di utilizzare le correzioni del marchio basate sull’intelligenza artificiale, assicurati che siano soddisfatte le seguenti condizioni:

- **Linee guida per il marchio configurate**: la tua organizzazione deve disporre di almeno un profilo di marchio attivo configurato in Adobe Journey Optimizer. I profili del brand definiscono le regole in base alle quali viene valutato il contenuto. Contatta l’amministratore di Adobe o il brand manager per verificare che i profili del brand siano pubblicati e associati alle sandbox.
- **Funzionalità di IA per la gestione dei contenuti abilitate**: l&#39;assistenza basata su IA deve essere abilitata per l&#39;organizzazione e la sandbox. Viene gestito a livello di profilo di prodotto in Adobe Admin Console. Se i suggerimenti di IA non vengono visualizzati dopo la scansione del brand, conferma con l’amministratore che l’adesione alla generazione di contenuti di IA è attiva.
- **Tipo di contenuto supportato** — Sono supportate le correzioni del marchio con suggerimenti di IA per i seguenti tipi di contenuto: Titolo e corpo della notifica push, testo del messaggio SMS e blocchi di contenuto Web modificati tramite Journey Optimizer Web Designer. Le risorse rich media (immagini, video) vengono valutate separatamente per la conformità al brand e non rientrano nell’ambito delle correzioni di IA a livello di testo.
- **Autorizzazioni di modifica** - È necessario disporre dell&#39;accesso di modifica al percorso, alla campagna o al modello di contenuto in cui si trova il contenuto contrassegnato.

## Configura {#configure}

Non è necessaria alcuna configurazione aggiuntiva per abilitare le correzioni del marchio basate sull’intelligenza artificiale se l’organizzazione utilizza già il Controllo qualità dei marchi. Il livello di suggerimento AI si attiva automaticamente quando vengono rilevate violazioni del brand nei tipi di contenuto supportati.

Per eseguire un controllo del brand e accedere ai suggerimenti di IA:

1. Apri la campagna o il percorso in Adobe Journey Optimizer.
2. Passa al passaggio di contenuto per il canale pertinente (push, SMS o web).
3. Seleziona **Verifica l&#39;allineamento del brand** (oppure apri il pannello **Controllo qualità del brand** dalla barra degli strumenti dell&#39;editor di contenuti).
4. Attendere il completamento dell&#39;analisi. Gli elementi contrassegnati sono evidenziati nell&#39;area di lavoro ed elencati nel pannello **Problemi del marchio** a destra.
5. Per ogni elemento contrassegnato, espandi la riga del problema per visualizzare il motivo della violazione e il suggerimento generato dall’intelligenza artificiale.
6. Utilizza **Anteprima** per visualizzare il testo suggerito nell&#39;area di lavoro del contenuto.
7. Seleziona **Applica suggerimento** per sostituire il testo contrassegnato oppure seleziona **Modifica** per modificare il suggerimento prima di applicare.
8. Dopo aver risolto o riconosciuto tutti i problemi, esegui nuovamente il controllo del brand per confermare la conformità.

>[!NOTE]
>
>L’applicazione di un suggerimento aggiorna il contenuto live nell’editor, ma non pubblica o attiva automaticamente la campagna. Devi completare i passaggi rimanenti di configurazione e attivazione della campagna come di consueto.

### Utilizzo di più suggerimenti {#multiple-suggestions}

Per alcune violazioni, il motore di intelligenza artificiale può generare più di un’alternativa. In questi casi, nel pannello **Problemi del marchio** viene visualizzato un elenco numerato di opzioni. Utilizza le frecce avanti e indietro per scorrere le alternative prima di selezionare quella che meglio si adatta al tuo intento. Ogni alternativa viene generata con un diverso approccio stilistico — ad esempio, si può dare priorità alla concisione mentre un altro enfatizza l&#39;allineamento del tono.

### Correzioni in blocco {#bulk-corrections}

Se più elementi nello stesso contenuto sono contrassegnati, puoi applicare i suggerimenti singolarmente o utilizzare l&#39;azione **Applica tutti i suggerimenti** nella parte superiore del pannello **Problemi del marchio** per accettare tutte le sostituzioni generate da IA in un singolo passaggio. Rivedi attentamente l’elenco prima di utilizzare l’applicazione in blocco, in quanto questa azione sostituisce tutto il testo contrassegnato contemporaneamente.

>[!NOTE]
>
>L’applicazione in blocco è disponibile solo quando a tutti gli elementi contrassegnati è associato un suggerimento di IA. Gli elementi senza suggerimenti disponibili (ad esempio, i flag di conformità per le immagini) vengono ignorati e rimangono contrassegnati per la revisione manuale.

## Argomenti correlati {#related-topics}

- [Panoramica sulle linee guida per il marchio](../content-management/brands.md)
- [Esegui un controllo del brand sul contenuto](../content-management/brand-score.md)
- [Assistente IA per la generazione di contenuti](../content-management/gs-generative.md)
- [Creare una notifica push](create-push.md)
- [Creare un messaggio SMS](../sms/create-sms.md)
- [Modificare i contenuti web con Journey Optimizer](../web/edit-web-content.md)
