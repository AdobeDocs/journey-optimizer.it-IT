---
source-git-commit: f59dc265b0de732b52e9d26b6ee510733d0d760e
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 0%

---
# Strumenti della casella &quot;In questa pagina&quot;

Strumenti per aggiungere e verificare la casella ombreggiata standard **&quot;In questa pagina&quot;** nella parte superiore di
pagine della documentazione di AJO. Vedere le specifiche in `.cursor/rules/on-this-page-box.mdc`.
Il rollout viene tracciato in **DOCAC-14936** epico (un&#39;attività per cartella di livello superiore).

## Descrizione dell&#39;aspetto della casella

```text
# Page Title {#anchor}

>[!BEGINSHADEBOX]

**On this page:** <one clear sentence describing the page's purpose>

>[!ENDSHADEBOX]
```

## Workflow consigliato (per cartella/attività Jira)

Esecuzione dalla directory principale del repository (`journey-optimizer.en/`).

1. **Inserisci le caselle** (iniziando una prima bozza di frase dall&#39;argomento di ogni pagina
   `description`). Meccanico, idempotente, non tocca mai la materia frontale:

   ```bash
   python scripts/on-this-page/add_on_this_page.py help/using/reports --seed-from-description
   ```

   Anteprima con `--dry-run`.

2. **Modifica il testo.** Il valore di inizializzazione è un punto di partenza. Modificare ogni frase in modo che
legge come dichiarazione di scopo (una frase, testo normale, inglese americano). **Lead
con il perché**: indicare il risultato/beneficio del lettore (&quot;...in modo da poter <outcome>&quot;), non
solo un elenco di ciò che copre la pagina. Corrispondenza con i nomi delle funzionalità in stile house (ad es.
&quot;Campagna orchestrata&quot;, &quot;In-app&quot;). Vedere `.cursor/rules/on-this-page-box.mdc`. Se
ignora `--seed-from-description`, è stato inserito un segnaposto `{{TODO...}}` e
la convalida contrassegna tutti gli elementi rimanenti.

3. **Convalida** prima di aprire la PR:

   ```bash
   python scripts/on-this-page/validate_on_this_page.py help/using/reports --require
   ```

   Il codice di uscita è diverso da zero in caso di errore, quindi può generare CI.

## Ambito/esclusioni

Le pagine di riferimento e sintassi sono escluse per impostazione predefinita (parti di percorso `api-reference`,
`expression`, `functions`). Sostituisci con `--exclude ...` se necessario.

## Verifica dell’avanzamento a livello di archivio

```bash
python scripts/on-this-page/validate_on_this_page.py help
```

Senza `--require`, le pagine ancora mancanti in una casella vengono segnalate come `pending` (non come
), per tenere traccia dell’avanzamento del rollout nella guida.
