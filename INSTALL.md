---
source-git-commit: 08eaa7ae974c134ea2e920a1fa854dcf6a971e18
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 1%

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

3. L’agente:
   - Verifica accesso SSH e HTTPS
   - Utilizzare il metodo di lavoro
   - Guida all&#39;installazione, se necessario
4. Fine. ✨

**Nota:** l&#39;agente rileva automaticamente se si dispone dell&#39;accesso SSH o HTTPS a `git.corp.adobe.com` e utilizza il metodo appropriato. In caso contrario, viene fornita una configurazione guidata.

### Opzione 2: utilizzo del terminale

1. Apri il terminale nella directory principale dell’archivio
2. Esegui:

   ```bash
   ./setup-agents.sh
   ```

   Lo script eseguirà automaticamente le operazioni seguenti:
   - Verifica accesso SSH e HTTPS
   - Utilizzare il metodo di lavoro
   - Se necessario, mostra le istruzioni di configurazione

   Oppure manualmente (se sai che il Git è configurato):

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

Per l&#39;elenco completo degli agenti disponibili, vedere [AGENTS.md](AGENTS.md).

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
your-repo/
  ├── .cursor-agents/          ← Git submodule
  │   ├── agents/
  │   │   ├── draft-page-generator.md
  │   │   └── fix-grammar.md
  │   └── AGENTS.md
  ├── setup-agents.sh          ← Setup script
  └── your-content/
```

Il sottomodulo punta a:
**https://git.corp.adobe.com/AdobeDocs/CursorAgents**

In questo modo tutti utilizzano gli stessi agenti aggiornati.

## Per i manutentori

### Aggiunta a un nuovo archivio

1. Aggiungi il modulo secondario:

   ```bash
   git submodule add https://git.corp.adobe.com/AdobeDocs/CursorAgents.git .cursor-agents
   ```

2. Copia file di installazione:
   - `setup-agents.sh`
   - `setup-agent.md` (posizione nella radice, non nel sottomodulo)
   - `INSTALL.md`

3. Conferma:

   ```bash
   git add .gitmodules .cursor-agents setup-agents.sh
   git commit -m "Add Cursor Agents submodule"
   ```

### Aggiornamento dell’archivio centrale

Le modifiche degli agenti devono essere effettuate in:
**https://git.corp.adobe.com/AdobeDocs/CursorAgents**

Tutti gli archivi riceveranno aggiornamenti tramite `git submodule update --remote`.

---

**Hai bisogno di aiuto?** Contatta il responsabile del team della documentazione o controlla il wiki interno.
