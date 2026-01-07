---
solution: Journey Optimizer
product: Journey Optimizer
title: Anteprima e test del contenuto
description: Convalida la precisione del messaggio prima dell’avvio. Visualizza un’anteprima dei contenuti personalizzati con i profili di test, invia bozze alle parti interessate, controlla il rendering delle e-mail tra i client, valuta i punteggi di spam e verifica in modo efficiente più varianti di contenuto.
redpen-status: CREATED_||_2025-08-11_20-30-05
exl-id: bd78e0af-573b-4880-a9f1-44467c9db159
source-git-commit: 6b83b015dfd74da9eb58bd06958d0963d81c6489
workflow-type: tm+mt
source-wordcount: '657'
ht-degree: 23%

---

# Anteprima e test del contenuto{#section-overview}

>[!BEGINSHADEBOX]

**Scopo:** strumenti di convalida pre-avvio per campagne e percorsi\
**Utenti principali:** manager campagne, addetti al marketing e-mail, creatori di contenuti\
**Risultato chiave:** rilevare gli errori prima della consegna al cliente

>[!ENDSHADEBOX]

Assicurati una consegna dei messaggi impeccabile rilevando gli errori prima che raggiungano i clienti. Il contenuto di anteprima convalida la precisione della personalizzazione tra diversi profili cliente, mentre gli strumenti di test rivelano problemi di rendering, rischi di spam e varianti di contenuto che potrebbero influire sul coinvolgimento. Accedi a funzionalità complete per inviare bozze alle parti interessate, simulare la personalizzazione con dati di esempio, controllare il rendering delle e-mail tra i client e valutare le metriche di recapito messaggi, il tutto prima dell’attivazione. Padroneggia queste tecniche di convalida per proteggere la reputazione del marchio, massimizzare il posizionamento nella casella in entrata e fornire ai clienti esperienze sempre eccellenti.

## Anteprima e test del contenuto

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg)

Come visualizzare in anteprima e testare i contenuti

Scopri come utilizzare i profili di test e i dati di input di esempio per visualizzare in anteprima e testare i contenuti, inviare bozze e garantire la precisione della personalizzazione.

[Introduzione ad anteprima e test](../using/content-management/preview-test.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg)

Come selezionare i profili di test

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
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg)

Inviare bozze utilizzando i dati del profilo di test

Testa e convalida i messaggi e-mail inviando bozze utilizzando i dati del profilo di test per garantire la precisione del contenuto.

[Scopri come inviare le bozze](../using/content-management/proofs.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/eye.svg)

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

**Contesto:** questa tabella mappa gli obiettivi di test su strumenti specifici in Adobe Journey Optimizer.

Scegli l’approccio di test in base all’obiettivo:

| **Se è necessario...** | **Usa questo strumento** |
|----------------------|-------------------|
| Verificare che la personalizzazione venga visualizzata correttamente | [Profili di test](../using/content-management/test-profiles.md) |
| Test rapido di oltre 10 varianti di contenuto | [Dati di input di esempio](../using/test-approve/simulate-sample-input.md) |
| Ottieni l’approvazione delle parti interessate prima dell’invio | [Invia bozze](../using/content-management/proofs.md) |
| Controlla la visualizzazione delle e-mail in Gmail, Outlook, Apple Mail | [Rendering Litmus](../using/content-management/rendering.md) |
| Migliora il posizionamento della casella in entrata | [Rapporto spam](../using/content-management/spam-report.md) |
| Visualizzare in anteprima tutte le varianti contemporaneamente | [Modalità anteprima](../using/content-management/preview.md) |

## Elenco di controllo del flusso di lavoro di prova

**Contesto:** Sequenza di test consigliata in 5 passaggi applicabile a tutti i canali (e-mail, SMS, push, web, in-app).

Segui questa sequenza per una convalida completa:

1. **Anteprima** - Utilizza i profili di test per verificare correttamente i rendering di personalizzazione
2. **Varianti di test** - Carica dati di esempio in CSV/JSON per convalidare più scenari
3. **Verifica recapito messaggi** (e-mail) - Esegui report di posta indesiderata ed esegui test di rendering
4. **Invia bozze** - Condividi con le parti interessate per la revisione e l&#39;approvazione
5. **Controllo finale** - Verifica che tutti i collegamenti, le immagini e i CTA funzionino correttamente

**Suggerimento pro:** verifica con almeno 3 profili che rappresentano diversi segmenti di clienti (valore alto, nuovo, inattivo) per rilevare i casi limite.

## Scenari comuni

**Contesto:** esempi reali che mostrano come applicare strumenti di test in casi d&#39;uso tipici.

**Scenario 1: verifica delle e-mail personalizzate per una campagna con più segmenti**
→ Utilizza [dati di input di esempio](../using/test-approve/simulate-sample-input.md) per testare 20-30 varianti senza creare singoli profili di test. Carica un file CSV con attributi cliente diversi e visualizza l’anteprima contemporaneamente.

**Scenario 2: convalida del rendering di e-mail prima di un invio principale**
→ Esegui [test Litmus](../using/content-management/rendering.md) per verificare la visualizzazione tra i client e-mail principali, quindi controlla il [rapporto di posta indesiderata](../using/content-management/spam-report.md) per verificare il posizionamento della casella in entrata.

**Scenario 3: recupero dell&#39;approvazione delle parti interessate**
→ [Invia bozze](../using/content-management/proofs.md) ai revisori interni con i dati del profilo di test in modo che possano vedere esattamente ciò che i clienti riceveranno.

## Punti chiave da eliminare

- **I profili di test** sono essenziali per visualizzare in anteprima i contenuti personalizzati; utilizza dati di input di esempio per testare in modo efficiente oltre 10 varianti
- **Gli strumenti specifici per le e-mail** includono test di rendering (Litmus), report di spam e bozze
- **Sequenza consigliata:** Anteprima → varianti di test → Verifica recapito messaggi → Invia bozze → Verifica finale
- **Risparmio di tempo:** Carica CSV/JSON con gli attributi del cliente invece di creare singoli profili di test

## Risorse aggiuntive

- **[Come utilizzare il rapporto posta indesiderata](../using/content-management/spam-report.md)** - Valuta il punteggio posta indesiderata del contenuto delle e-mail utilizzando la funzione Rapporto posta indesiderata per migliorare il recapito messaggi.

**Argomenti correlati:** [Verifica e approva la pagina di destinazione](test-landing-page.md) | [Flussi di lavoro di approvazione](approve-landing-page.md) | [Creazione dei profili di test](../using/audience/creating-test-profiles.md)
