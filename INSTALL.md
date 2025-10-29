---
source-git-commit: 80d5f294491b35dcdbfe4976cb3ec4cf14384858
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 2%

---
# 🚀 Installazione degli agenti cursore

Gli agenti cursore sono strumenti condivisi che consentono di creare e gestire la documentazione in modo più efficiente.

## Prima configurazione

È necessario eseguire questa operazione solo **una volta** per archivio.

### Opzione 1: utilizzo del cursore (scelta consigliata ⭐)

1. Apri chat cursore (`Cmd+L` o `Ctrl+L`)
2. Tipo:

   ```
   @setup-agents
   ```

3. Segui le istruzioni
4. Fine. ✨

### Opzione 2: utilizzo del terminale

1. Apri il terminale nella directory principale dell’archivio
2. Esegui:

   ```bash
   ./setup-agents.sh
   ```

   Oppure manualmente:

   ```bash
   git submodule update --init --recursive
   ```

3. Fine. ✨

## Verifica

Dopo l&#39;installazione, verificare quanto segue:

```bash
ls .cursor-agents/agents/
```

Dovresti vedere:
- `draft-page-generator.md`
- `fix-grammar.md`
- ecc.

## Utilizzo

Una volta installato, è possibile utilizzare gli agenti in Cursore:

```
@draft-page      # Generate a new documentation page
@fix-grammar     # Fix grammar in current file
```

Per l&#39;elenco completo degli agenti disponibili, vedere `.cursor-agents/AGENTS.md`.

## Aggiornamento degli agenti

Per ottenere la versione più recente di tutti gli agenti:

### Opzione 1: utilizzo del cursore

```
@update-agents
```

### Opzione 2: utilizzo del terminale

```bash
git submodule update --remote
```

## Risoluzione dei problemi

### Errore &quot;Agente non trovato&quot;

Se visualizzi questo errore, gli agenti non sono ancora installati. Esegui:

```
@setup-agents
```

### Il sottomodulo è vuoto

Se `.cursor-agents/` esiste ma è vuoto:

```bash
git submodule update --init --recursive --remote
```

### Autorizzazione negata

Verifica che lo script di installazione sia eseguibile:

```bash
chmod +x setup-agents.sh
```

### Problemi di rete/VPN

- Assicurati di essere connesso alla VPN di Adobe
- Verifica connettività di rete
- Verifica accesso Git:

  ```bash
  git ls-remote https://git.corp.adobe.com/AdobeDocs/CursorAgents
  ```

## Come funziona

Gli agenti cursore sono distribuiti come **modulo Git secondario**:

```
journey-optimizer.en/
  ├── .cursor-agents/          ← Git submodule
  │   ├── agents/
  │   │   ├── draft-page-generator.md
  │   │   └── fix-grammar.md
  │   └── AGENTS.md
  ├── setup-agents.sh          ← Setup script
  ├── setup-agent.md           ← Bootstrap agent
  └── help/                    ← Your documentation
```

Il sottomodulo punta a:
**https://git.corp.adobe.com/AdobeDocs/CursorAgents**

In questo modo tutti utilizzano gli stessi agenti aggiornati.

**Hai bisogno di aiuto?** Contatta il responsabile del team della documentazione o controlla il wiki interno.

