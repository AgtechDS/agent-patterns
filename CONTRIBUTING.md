# Contributing a agent-patterns

Grazie per voler contribuire. Questo repository è una collezione di pattern LLM-ready, non codice. Ogni pattern è un file Markdown che trasforma un agent generico in uno specialista.

---

## Cos'è un pattern

Un pattern è un **kit di prompt Markdown** (README + SCHEMA + examples) che:

- Definisce un **problema ricorrente** con un **dolore concreto**
- Assegna al LLM un **ruolo specifico** con operazioni chiare
- Produce un **artefatto persistente** (wiki Markdown)
- Richiede **zero setup** oltre a copiare il file nell'agent

Non è codice. Non è un'app. Non è un tool CLI. È un prompt strutturato.

## Come proporre un nuovo pattern

### 1. Apri una Issue

Usa il template [New Pattern Proposal](.github/ISSUE_TEMPLATE/new-pattern.md). La tua proposta deve passare il **5-criteria filter**:

| Criterio | Domanda |
|----------|---------|
| **Dolore reale e frequente** | "Ci sbatti la testa ogni settimana?" |
| **Dati già esistenti** | "L'utente ha già le informazioni (email, note, file) o deve crearle da zero?" |
| **LLM fa il lavoro noioso** | "C'è bookkeeping, aggiornamento, collegamento che un umano odia fare?" |
| **Output = file Markdown** | "Il risultato è portabile, versionabile, leggibile da qualsiasi tool?" |
| **Setup in 5 minuti** | "Basta incollare lo SCHEMA nell'agent e dire 'init'?" |

Se la risposta è "no" a una di queste, probabilmente non è un buon pattern per questa repo.

### 2. Scrivi il pattern

1. Forka la repo
2. Crea un branch: `pattern/nome-pattern` (es. `pattern/debug-diary`)
3. Crea la directory: `patterns/<categoria>/<nome>/`
4. Scrivi `README.md` e `SCHEMA.md` seguendo [`TEMPLATE.md`](TEMPLATE.md)
5. Aggiungi almeno 1 esempio in `examples/` con dati realistici
6. Apri una Pull Request

### 3. Categorie disponibili

| Categoria | Cosa contiene | Esempi |
|-----------|---------------|--------|
| `dev/` | Tool per sviluppatori | GitHub Gardener, Debug Diary |
| `knowledge/` | Gestione conoscenza e studio | LLM Wiki, Study Companion |
| `life/` | Organizzazione personale | Decision Journal, Health Timeline |
| `work/` | Produttività professionale | Meeting Memory, Project Postmortem |
| `creative/` | Supporto a processi creativi | World Bible |

Per proporre una nuova categoria, menzionala nella Issue.

---

## Quality bar

Prima che un pattern venga accettato, deve superare questi controlli:

### Completanza
- [ ] README con: problema, soluzione, architettura, operazioni, quick start, filosofia, limiti
- [ ] SCHEMA con: identità, struttura, formato file, operazioni (con trigger), regole, checklist init, note
- [ ] Almeno 1 esempio in `examples/` con dati realistici
- [ ] Prefisso comando di 2-4 lettere

### Validazione
- [ ] Ogni operazione è stata testata con un agent reale
- [ ] Lo SCHEMA funziona con **almeno 2 agent diversi** (es. Claude Code + GitHub Copilot + Codex)
- [ ] Tutti i comandi producono l'output descritto
- [ ] I template generano file validi

### Vincoli
- [ ] Zero dipendenze da tool esterni (nessuna API, nessun npm package, nessun binario)
- [ ] SCHEMA.md ≤ 15 KB
- [ ] Date in formato ISO 8601 (`YYYY-MM-DD`)
- [ ] ID progressivi con prefisso del pattern (`PAT-001`)

---

## Issue templates

### new-pattern.md

```markdown
---
name: New Pattern Proposal
about: Proponi un nuovo pattern per agent-patterns
title: "[New Pattern] Nome Pattern"
---

## Pattern: [Nome]

### 5-Criteria Filter
- [ ] **Dolore reale e frequente**: [descrivi]
- [ ] **Dati già esistenti**: [descrivi]
- [ ] **LLM fa il lavoro noioso**: [descrivi]
- [ ] **Output = file Markdown**: [descrivi]
- [ ] **Setup in 5 minuti**: [descrivi]

### Operazioni proposte
- `pat init` — [cosa fa]
- `pat log` — [cosa fa]
- `pat lint` — [cosa fa]

### Categoria
[dev / knowledge / life / work / creative]

### Note aggiuntive
[eventuali dettagli, riferimenti, ispirazioni]
```

### bug-report.md

```markdown
---
name: Bug Report
about: Un pattern non funziona come descritto
title: "[Bug] Nome Pattern — sintomo"
---

## Pattern
[link al pattern]

## Problema
[cosa succede invece di ciò che è descritto]

## Passi per riprodurre
1. Incollo SCHEMA in [agent]
2. Eseguo `pat comando`
3. [risultato atteso vs reale]

## Agente usato
[Claude Code / OpenCode / Codex / altro]

## Note
[eventuali dettagli aggiuntivi]
```

### improvement.md

```markdown
---
name: Improvement
about: Suggerimento per un pattern esistente
title: "[Improvement] Nome Pattern — cosa migliorare"
---

## Pattern
[link al pattern]

## Cosa migliorare
[descrizione del miglioramento]

## Perché
[perché è utile]

## Impact
[poco / medio / tanto]
```

---

## PR template

```markdown
---
name: New Pattern
about: Pull request per un nuovo pattern
---

## Pattern: [Nome]

### Categoria
[dev / knowledge / life / work / creative]

### Problema
[in 2-3 righe]

### Operazioni
- `pat init`
- `pat log`
- `pat lint`

### Test effettuato
- [ ] Testato con [agente 1]
- [ ] Testato con [agente 2]

### Checklist
- [ ] README.md completo
- [ ] SCHEMA.md completo
- [ ] Almeno 1 esempio in examples/
- [ ] Segue TEMPLATE.md
- [ ] ≤ 15 KB

### Note
[eventuali dettagli per il reviewer]
```

---

## Processo di review

1. **Apertura Issue** → discussione sulla validità del pattern (24-48h)
2. **Fork + sviluppo** → branch `pattern/nome-pattern`
3. **Pull Request** → review della struttura e qualità
4. **Test** → il maintainer testa lo SCHEMA con almeno un agente
5. **Merge** → aggiornamento README root + changelog

---

*Grazie per contribuire a fare di agent-patterns un punto di riferimento per la progettazione di agent LLM.*
