---
solution: Journey Optimizer
product: Journey Optimizer
title: Anteprima e test dei contenuti
description: Convalida la precisione del messaggio prima del lancio. Visualizza l’anteprima dei contenuti personalizzati con i profili di test, invia bozze agli stakeholder, controlla il rendering delle e-mail tra i client, valuta i punteggi dello spam e testa in modo efficiente più varianti di contenuto.
redpen-status: CREATED_||_2025-08-11_20-30-05
exl-id: bd78e0af-573b-4880-a9f1-44467c9db159
source-git-commit: 6b83b015dfd74da9eb58bd06958d0963d81c6489
workflow-type: ht
source-wordcount: '657'
ht-degree: 100%

---

# Anteprima e test dei contenuti{#section-overview}

>[!BEGINSHADEBOX]

**Scopo:** strumenti di convalida pre-avvio per campagne e percorsi\
**Utenti principali:** responsabili delle campagne, marketer delle e-mail, creatori di contenuti\
**Risultato chiave:** rilevare gli errori prima della consegna al cliente

>[!ENDSHADEBOX]

Assicurati una consegna dei messaggi impeccabile rilevando gli errori per tempo. L’anteprima dei contenuti convalida la precisione della personalizzazione tra diversi profili cliente, mentre gli strumenti di test rivelano problemi di rendering, rischi di spam e varianti di contenuto che potrebbero influire sul coinvolgimento. Prima di attivare una consegna, accedi a funzionalità complete per inviare bozze agli stakeholder, simulare la personalizzazione con dati di esempio, controllare come verranno riprodotte le e-mail su client diversi e valutare le metriche di recapitabilità. Padroneggia queste tecniche di convalida per proteggere la reputazione del brand, massimizzare la consegna nella casella in entrata e fornire alla clientela esperienze sempre eccellenti.

## Anteprima e test del contenuto

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg?lang=it)

Come visualizzare in anteprima e testare contenuti

Scopri come utilizzare i profili di test e i dati di input di esempio per visualizzare in anteprima e testare i contenuti, inviare bozze e garantire la precisione della personalizzazione.

[Introduzione ad anteprima e test](../using/content-management/preview-test.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg)

Come selezionare profili di test

Scopri come selezionare e gestire i profili di test per visualizzare in anteprima e testare in modo efficace i contenuti personalizzati.

[Scopri come selezionare i profili di test](../using/content-management/test-profiles.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg)

Visualizzare l’anteprima del contenuto utilizzando i profili di test

Guida dettagliata per la visualizzazione in anteprima dei contenuti personalizzati utilizzando i profili di test e simulando le varianti di contenuto.

[Visualizza l’anteprima del contenuto con profili di test](../using/content-management/preview.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg?lang=it)

Inviare bozze utilizzando i dati del profilo di test

Testa e convalida i messaggi e-mail inviando bozze utilizzando i dati del profilo di test per garantire la precisione del contenuto.

[Scopri come inviare le bozze](../using/content-management/proofs.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/eye.svg?lang=it)

Come testare il rendering di e-mail con Litmus

Integra Litmus per visualizzare in anteprima il rendering delle e-mail per i client e-mail più diffusi e assicurarne la corretta visualizzazione.

[Testare il rendering delle e-mail con Litmus](../using/content-management/rendering.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg)

Come simulare e testare le varianti di contenuto

Simula le varianti di contenuto utilizzando dati di input di esempio per testare contenuti personalizzati e assicurarne la precisione.

[Simulare varianti di contenuto](../using/test-approve/simulate-sample-input.md)
:::

::::

## Guida rapida alle decisioni

**Contesto:** questa tabella mappa gli obiettivi di test a strumenti specifici in Adobe Journey Optimizer.

Scegli l’approccio di test in base all’obiettivo:

| **Se è necessario...** | **Utilizza questo strumento** |
|----------------------|-------------------|
| Verifica che la personalizzazione venga visualizzata correttamente | [Profili di test](../using/content-management/test-profiles.md) |
| Test rapido di oltre 10 varianti di contenuto | [Dati di input di esempio](../using/test-approve/simulate-sample-input.md) |
| Ottieni l’approvazione degli stakeholder prima dell’invio | [Invia bozze](../using/content-management/proofs.md) |
| Controlla la visualizzazione delle e-mail in Gmail, Outlook, Apple Mail | [Rendering con Litmus](../using/content-management/rendering.md) |
| Migliora la consegna nella casella in entrata | [Rapporto spam](../using/content-management/spam-report.md) |
| Visualizza l’anteprima di tutte le varianti contemporaneamente | [Modalità anteprima](../using/content-management/preview.md) |

## Lista di controllo del flusso di lavoro di test

**Contesto:** sequenza di test consigliata in 5 passaggi applicabile a tutti i canali (e-mail, SMS, push, web, in-app).

Segui questa sequenza per una convalida completa:

1. **Anteprima**: utilizza i profili di test per controllare se la personalizzazione viene eseguita correttamente
2. **Varianti di test**: carica dati di esempio in CSV/JSON per convalidare più scenari
3. **Controlla la recapitabilità** (e-mail): esegui rapporti di spam e test di rendering
4. **Invia bozze**: condividile con gli stakeholder per la revisione e l’approvazione
5. **Controllo finale**: verifica che tutti i collegamenti, le immagini e i CTA funzionino correttamente

**Suggerimento pro:** esegui test con almeno 3 profili che rappresentano diversi segmenti di cliente (valore alto, nuovo, inattivo) per rilevare i casi limite.

## Scenari comuni

**Contesto:** esempi reali che mostrano come applicare strumenti di test in casi d’uso tipici.

**Scenario 1: test delle e-mail personalizzate per una campagna con più segmenti**
→ Utilizza [dati di input di esempio](../using/test-approve/simulate-sample-input.md) per testare 20-30 varianti senza creare singoli profili di test. Carica un file CSV con attributi cliente diversi e visualizza in anteprima contemporaneamente.

**Scenario 2: convalida del rendering delle e-mail prima di un invio importante**
→ Esegui [test Litmus](../using/content-management/rendering.md) per controllare come le e-mail verranno visualizzate nei client e-mail principali, quindi controlla il [rapporto spam](../using/content-management/spam-report.md) per assicurarti che vengano consegnate nella casella in entrata.

**Scenario 3: recupero dell’approvazione finale degli stakeholder**
→ [Invia bozze](../using/content-management/proofs.md) ai revisori interni con i dati del profilo di test in modo che possano vedere esattamente ciò che la clientela riceverà.

## Concetti chiave

- **I profili di test** sono essenziali per visualizzare in anteprima i contenuti personalizzati; utilizzano dati di input di esempio per testare in modo efficiente oltre 10 varianti
- **Gli strumenti specifici per le e-mail** includono test di rendering (Litmus), rapporti spam e bozze
- **Sequenza consigliata:** Visualizza anteprima → Varianti di test → Controlla recapitabilità → Invia bozze → Verifica finale
- **Risparmio di tempo:** carica file CSV/JSON con gli attributi cliente invece di creare singoli profili di test

## Risorse aggiuntive

- **[Come utilizzare il rapporto spam sulle email](../using/content-management/spam-report.md)**: valuta il punteggio dello spam dei contenuti e-mail utilizzando la funzione Rapporto spam per migliorare la recapitabilità.

**Argomenti correlati:** [Testare e approvare la pagina di destinazione](test-landing-page.md) | [Flussi di lavoro di approvazione](approve-landing-page.md) | [Creazione dei profili di test](../using/audience/creating-test-profiles.md)
