---
source-git-commit: 469248d3ded81c5e3aaa9a2ccf04c0ca0c22a5d0
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 2%

---
# Tracciamento Git, PR e JIRA

Come atterrare il cambiamento in modo sicuro e tracciarlo. Due regole ferme dall’autore:

1. **Chiedi conferma prima di aprire una PR.** Genera e verifica il blocco indipendentemente, ma apri solo un pull
richiesta se l’autore dice sì.
2. **Non unire mai.** Queste PR esistono per la revisione umana. L&#39;unione è sempre la decisione dell&#39;autore.

## Sweep strutturale (eseguita prima del commit)

Per ogni pagina elaborata nella cartella:

```bash
cd <repo>
for p in <page1> <page2> ...; do
  f="help/_includes/do-not-localize/<folder>/ai-augmented-$p.md"
  inc="help/using/<folder>/$p.md"
  [ -f "$f" ] || echo "MISSING BLOCK: $f"
  grep -q '^# AI Knowledge Reference' "$f"            || echo "$p: missing H1"
  grep -q '^+++ AI Knowledge Reference' "$f"          || echo "$p: missing accordion open"
  grep -q 'This section contains structured knowledge' "$f" || echo "$p: missing opening para 1"
  grep -q 'ai-section-version' "$f"                   || echo "$p: missing sync comment"
  grep -nEi "\b(isn't|aren't|don't|doesn't|didn't|can't|won't|wouldn't|couldn't|shouldn't|it's|we've|we're|you're|they're|that's|there's|haven't|hasn't|wasn't|weren't)\b" "$f" \
    | grep -vi 'UICONTROL' && echo "  ^ $p contraction"
  grep -q "do-not-localize/<folder>/ai-augmented-$p.md" "$inc" || echo "$p: MISSING include in page"
done
echo "=== sweep done ==="
git status --short
```

Qualsiasi riga stampata (ad eccezione di &quot;sweep done&quot; e dell&#39;elenco `git status`) è un difetto da correggere prima di
commit.

## Branch e commit (mai commit su main)

```bash
git checkout main -q && git pull -q origin main
git checkout -q -b DOCAC-<key> origin/main    # branch name = the JIRA task key
# ... generate + verify + sweep ...
git add help/_includes/do-not-localize/<folder>/ help/using/<folder>/*.md
git commit -q -m "DOCAC-<key> Add AI Knowledge Reference blocks (<folder>)

<one-line what + the verification result>

Co-Authored-By: Claude <model> <noreply@anthropic.com>"
```

**Verificare che il commit sia atterrato sul ramo e non su`main`** (un&#39;arma a pedale nota) se si è passati a
`main` per esaminare le pagine, è possibile che venga eseguito un commit successivo):

```bash
git rev-parse --abbrev-ref HEAD                    # must print DOCAC-<key>
git rev-list --left-right --count origin/main...DOCAC-<key>   # must show  0<TAB>1
```

Se un commit si è verificato accidentalmente il `main`: `git branch -f DOCAC-<key> <sha>` per puntare il ramo
a questo punto, `git checkout DOCAC-<key>`, quindi `git branch -f main origin/main` per ripristinare la directory principale locale.
`origin/main` non è mai interessato da un errore locale.

Push: `git push -u origin DOCAC-<key>` (utilizzare `--force-with-lease` se il ramo esiste già
in remoto in un commit meno recente).

## Chiedi informazioni sulla PR

Chiedi all&#39;autore, ad esempio: *&quot;Blocchi generati e verificati per `<folder>`. Vuoi
aprire una PR per la revisione?&quot;* Solo in caso affermativo:

```bash
gh pr create --base main --head DOCAC-<key> \
  --title "DOCAC-<key> Add AI Knowledge Reference blocks (<folder>)" \
  --body-file <pr-body>.md
```

Il corpo della PR termina con la riga di attribuzione richiesta
(`🤖 Generated with [Claude Code](https://claude.com/claude-code)`). **Non unire** — lascia il
PR disponibile per la revisione.

## Tracciamento JIRA

Monitora ogni modifica in un&#39;attività DOCAC (rollout epico: `DOCAC-15582`). Trova o crea la cartella
attività, quindi:

1. **Commento** con modifiche e risultato della verifica (pagine coperte/saltate, verificatore)
pulita/corretta, eventuali chiamate hard-vs-default di rilievo). Includi il collegamento PR, se presente.
2. **Imposta la versione di correzione** (questo programma ha utilizzato `AJO26.9`).
3. **Transizione** Nuova → in corso → Risolta (risoluzione &quot;Fissa&quot;), in base al flusso di lavoro. In questo
progetto gli ID transizione sono stati `4` (Avvio avanzamento) quindi `5` (Risoluzione, con risoluzione
   `{"name":"Fixed"}`); è necessario avviare un&#39;attività ancora in &quot;Nuovo&quot; prima di risolverla.

Utilizzare gli strumenti MCP JIRA aziendali (`add_jira_comment`, `update_jira_issue` per `fixVersions`,
`bulk_transition_jira_issues`) o l&#39;interfaccia utente JIRA. Se non hai accesso a JIRA, passa questo passaggio a
qualcuno che ce l&#39;ha e lo annota nella tua segnalazione.

## Una cartella = un ramo = un&#39;attività

Non combinare cartelle non correlate in un singolo ramo o PR. Una nuova pagina aggiunta in seguito è la sua piccola
(modalità CREA) e possono condividere l’attività della cartella o ottenerne una propria, a scelta del team.
