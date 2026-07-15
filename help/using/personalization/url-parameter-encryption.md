---
solution: Journey Optimizer
product: journey optimizer
title: Crittografa parametri URL
description: Scopri come crittografare i parametri di query URL sensibili in modo che i dati PII non siano esposti in testo normale sui collegamenti di tracciamento e sulle pagine di destinazione di Journey Optimizer.
feature: Personalization
topic: Personalization
role: Admin
level: Intermediate
keywords: crittografia, URL, tracciamento, pagina di destinazione, registro chiavi, personalizzazione, sicurezza, privacy, sandbox
exl-id: 82e2b6e4-769f-4bdc-b2e2-19352fbaec8e
feature_v2:
  - id: fda7be7c-b81e-42c0-95a9-616e5b893c03
subfeature_v2:
  - id: cb09dcb7-3367-4b63-b02c-8a1356eb876e
source-git-commit: f552e98f370f96e9a99d2f1d604f840ac6069d65
workflow-type: tm+mt
source-wordcount: 1348
ht-degree: 1%

---

# Crittografa parametri URL {#url-parameter-encryption}

>[!BEGINSHADEBOX]

**In questa pagina:** scopri come crittografare i parametri di query URL sensibili in modo che le informazioni di identificazione personale non vengano esposte in testo normale, incluso il modo in cui gli amministratori creano, ruotano e revocano le chiavi nel registro delle chiavi sandbox di Adobe Journey Optimizer.

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Questa funzionalità è attualmente disponibile solo per il canale e-mail.

## Perché utilizzare la crittografia dei parametri URL? {#why-url-parameter-encryption}

I collegamenti di tracciamento personalizzati e gli URL delle pagine di destinazione spesso includono attributi di profilo, identificatori, token o altri valori nella stringa di query. Tali parametri sono generalmente visibili come testo normale nell’e-mail o nell’SMS e rimangono leggibili se qualcuno copia, condivide o segnalibro il collegamento. Questo può essere un rischio per la sicurezza e la privacy quando i valori possono includere informazioni personali (PII, personally identifiable information) o altri dati sensibili che devono proteggere.

[!DNL Journey Optimizer] fornisce un helper di crittografia nell&#39;editor di personalizzazione per consentirti di crittografare qualsiasi valore di espressione al momento del rendering (ad esempio un attributo di profilo, un token o una stringa creata da diversi campi). La crittografia richiede sempre una chiave del Registro di sistema dell&#39;organizzazione.

È possibile crittografare solo i parametri di query scelti, utilizzando le chiavi gestite dagli amministratori in un registro a livello di sandbox, in modo che i valori riservati non vengano lasciati esposti in testo non crittografato quando il collegamento viene condiviso o ispezionato.

### Come funziona {#how-it-works}

* **Gli amministratori** utilizzano il Registro di sistema delle chiavi per [creare le chiavi](#create-keys) e [gestire le chiavi](#manage-keys) in conformità ai criteri di sicurezza della tua organizzazione.
* **Gli addetti al marketing** inseriscono l&#39;helper `Encrypt` nell&#39;editor di personalizzazione e trasmettono il valore da proteggere più un identificatore di chiave attiva dal Registro di sistema. Per informazioni sulla sintassi e sulle opzioni, vedere [questa sezione](functions/helpers.md#url-parameter-encryption-helper).

>[!IMPORTANT]
>
>La decrittografia è responsabilità della tua organizzazione. [!DNL Journey Optimizer] crittografa i valori al rendering del messaggio. Il sito web, l’app o l’API devono decrittografare i parametri utilizzando lo stesso materiale e gli stessi processi di crittografia definiti, in modo coerente con il modello di sicurezza.

### Esempio

L&#39;URL di una pagina di destinazione può utilizzare un parametro di query come `token` il cui valore è un token di stringa (ad esempio un payload JSON con identificatori di offerta o profilo). Senza crittografia, il token di stringa è visibile come testo normale nel collegamento. Se racchiudi tale valore nell’helper di crittografia, il payload sensibile viene sostituito con un testo crittografato nell’URL, lasciando invariato il resto del collegamento.

## Creare le chiavi {#create-keys}

Prima di poter utilizzare l’helper per la crittografia dei parametri URL, devi creare una chiave. A questo scopo, segui i passaggi riportati qui sotto.

>[!IMPORTANT]
>
>Per accedere e gestire le chiavi, è necessario disporre delle autorizzazioni **Visualizza registro chiavi** e **Gestisci registro chiavi**. [Ulteriori informazioni](../administration/high-low-permissions.md#administration-permissions)

1. Vai a **[!UICONTROL Amministrazione]** > **[!UICONTROL Configurazioni]**.

1. Fai clic sul pulsante **[!UICONTROL Gestisci]** per aprire il **[!UICONTROL Registro di sistema delle chiavi]**.

   ![Sezione registro chiavi nel menu Amministrazione](assets/encryption-key-registry.png){width="80%"}

1. Utilizzando il pulsante dedicato, crea le chiavi necessarie per la tua organizzazione.

   ![Pulsante Crea chiave nella sezione Registro di sistema delle chiavi](assets/encryption-create-key.png){width="80%"}

1. Assegna loro un’etichetta chiara o un identificatore a cui i team possono fare riferimento nell’editor di personalizzazione.

   ![Dettagli chiave nella sezione Registro di sistema delle chiavi](assets/encryption-key-details.png){width="80%"}

1. Fai clic su **[!UICONTROL Invia]** per confermare le modifiche.

Una volta creata una chiave, gli addetti al marketing possono utilizzare l&#39;helper per la crittografia del parametro [URL](functions/helpers.md#url-parameter-encryption-helper) nell&#39;editor di personalizzazione per crittografare valori specifici inseriti nei parametri di query URL.

## Gestione chiavi {#manage-keys}

Per gestire le chiavi, segui la procedura riportata di seguito.

1. Accedere al **[!UICONTROL Registro chiavi]**. In una vista a elenco puoi visualizzare tutte le chiavi create per la sandbox corrente.

   ![Visualizzazione elenco chiavi del Registro di sistema](assets/encryption-key-registry-list.png){width="100%"}

1. Fai clic su una chiave con lo stato **[!UICONTROL Attivo]** per aprire i dettagli della chiave.

   ![Dettagli chiave attiva](assets/encryption-key-active-details.png){width="80%"}

1. Fai clic sul pulsante **[!UICONTROL Revoca]** per disabilitare definitivamente la chiave per la nuova crittografia.

   Una volta revocata una chiave, i tentativi di utilizzarla nell’helper non dovrebbero riuscire al momento del rendering. Le voci revocate rimangono visibili per il controllo di audit; i team potrebbero avere ancora bisogno del materiale corrispondente per decrittografare i payload precedenti sui propri sistemi.

1. Fai clic sul pulsante **[!UICONTROL Ruota]** per fornire nuovo materiale chiave mantenendo un identificatore di chiave stabile a cui i percorsi e le campagne fanno già riferimento.

   Il materiale precedente viene conservato nel Registro di sistema con uno stato revocato e un motivo appropriato (ad esempio un timestamp di rotazione) e una nuova riga o versione riflette la chiave attiva.

   >[!NOTE]
   >
   >Per crittografare i nuovi valori nell’editor di personalizzazione devono essere selezionate solo le chiavi attive. Non utilizzare le chiavi revocate per i nuovi contenuti.

## Riferimento rapido {#quick-reference}

Questa sezione contiene informazioni strutturate che supportano l&#39;interpretazione, il recupero e la risposta alle domande relative a questo argomento.

Per una comprensione completa, queste informazioni devono essere unite alla documentazione su questa pagina. Nessuna delle due origini è progettata per essere indipendente; la pagina descrive la funzione, mentre questa sezione fornisce un contesto aggiuntivo che aiuta a non ambiguare la terminologia, le finalità, l’applicabilità e i vincoli.

>[!BEGINTABS]

>[!TAB Panoramica]

**TL;DR**

Questa pagina spiega come gli amministratori creano, ruotano e revocano le chiavi di crittografia nel registro delle chiavi a livello di sandbox di Journey Optimizer, consentendo agli addetti al marketing di crittografare i parametri delle query URL sensibili in modo che i dati PII non vengano esposti in testo normale nei collegamenti di tracciamento e nelle pagine di destinazione.

**Intenti**

* Scopri perché è necessaria la crittografia dei parametri URL (dati sensibili e PII visibili nelle stringhe di query in testo normale)
* Crea chiavi di crittografia nel Registro di sistema delle chiavi sandbox (attività di amministrazione che richiede autorizzazioni specifiche)
* Revoca di una chiave per disabilitarla definitivamente per la nuova crittografia
* Ruotare una chiave per fornire nuovo materiale crittografico mantenendo lo stesso identificatore
* Utilizza l&#39;helper `Encrypt` nell&#39;editor di personalizzazione per proteggere valori di parametri di query specifici

>[!TAB Glossario]

* **Registro di sistema delle chiavi**: un archivio a livello di sandbox in Journey Optimizer (Amministrazione > Configurazioni) in cui gli amministratori creano e gestiscono le chiavi di crittografia utilizzate dall&#39;helper per la crittografia dei parametri URL. *(specifico per prodotto)*
* **Helper crittografia (`Encrypt`)**: funzione helper nell&#39;editor di personalizzazione che crittografa un valore di espressione al momento del rendering, sostituendo PII con testo crittografato nei parametri di query URL. *(specifico per prodotto)*
* **Revoca (chiave)**: l&#39;operazione di disabilitazione permanente di una chiave per la nuova crittografia; la voce della chiave rimane visibile nel Registro di sistema per il controllo e i payload precedenti potrebbero ancora richiederla per la decrittografia nei sistemi dell&#39;organizzazione.
* **Ruota (chiave)**: fornisce nuovo materiale crittografico per una chiave mantenendo stabile il relativo identificatore, pertanto non è necessario aggiornare le campagne e i percorsi che fanno già riferimento a tale chiave.
* **PII (personalmente identificabili)**: dati che possono identificare un individuo, ad esempio attributi di profilo, token o identificatori di offerta, che devono essere protetti quando sono inclusi nei parametri di query URL.

>[!TAB Terminologia]

* **Nome canonico:** Crittografia parametro URL — varianti: Crittografia URL, Crittografia parametro query, Offuscamento parametro URL
* **Sinonimi:** &quot;registro chiavi&quot; = &quot;Registro chiavi&quot; (etichetta interfaccia utente in Amministrazione > Configurazioni)
* **Non confondere:** Revoca (disabilita definitivamente la chiave per la nuova crittografia; la voce rimane per il controllo) ≠ Ruota (sostituisce il materiale crittografico ma mantiene attivo lo stesso identificatore di chiave per la nuova crittografia)

>[!TAB Guardrail e limitazioni]

* La crittografia dei parametri URL è attualmente disponibile solo per il canale e-mail.
* Richiede le autorizzazioni **Visualizza registro chiavi** e **Gestisci registro chiavi** per accedere e gestire le chiavi.
* La decrittografia è responsabilità dell&#39;organizzazione. Journey Optimizer crittografa i valori al momento del rendering; il sito web, l’app o l’API devono decrittografare i parametri utilizzando lo stesso materiale e gli stessi processi di crittografia definiti dall’organizzazione.
* Per crittografare i nuovi valori nell’editor di personalizzazione devono essere utilizzate solo le chiavi attive; le chiavi revocate non devono essere utilizzate per i nuovi contenuti.
* Le chiavi revocate rimangono visibili nel registro di sistema a scopo di audit; potrebbero essere ancora necessarie ai sistemi dell’organizzazione per decrittografare i payload precedenti.

>[!TAB Domande frequenti]

**Q: chi è responsabile della decrittografia?**

La decrittografia è responsabilità dell&#39;organizzazione. Journey Optimizer crittografa i valori durante il rendering del messaggio. Il sito web, l’app o l’API devono decrittografare i parametri di query utilizzando lo stesso materiale crittografico e i processi definiti dall’organizzazione.

**Q: Qual è la differenza tra Revoca e Rotazione?**

Revoca disattiva definitivamente una chiave per la nuova crittografia mantenendo la voce visibile nel Registro di sistema per il controllo (i payload meno recenti potrebbero avere ancora bisogno della chiave per la decrittografia nei sistemi dell&#39;organizzazione). Rotate fornisce nuovo materiale crittografico per una chiave mantenendo lo stesso identificatore di chiave, in modo che le campagne e i percorsi che vi fanno riferimento continuino a funzionare senza aggiornamenti.

**D: quali autorizzazioni sono necessarie per gestire le chiavi?**

**Visualizza registro chiavi** e **Gestisci registro chiavi** autorizzazioni.

**Q: quali canali supportano la crittografia dei parametri URL?**

Attualmente solo il canale e-mail.

**D: è possibile utilizzare una chiave revocata per la nuova crittografia?**

No. Una volta revocata una chiave, i tentativi di utilizzarla nell’helper di crittografia dovrebbero non riuscire al momento del rendering. Non utilizzare le chiavi revocate per i nuovi contenuti.

>[!ENDTABS]

<!-- ai-section-version: 1 | source-hash: c594ce24 -->
