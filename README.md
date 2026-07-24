# agent-patterns

[![Version](https://img.shields.io/badge/version-0.1.0-blue)]()
[![Patterns](https://img.shields.io/badge/patterns-16-green)]()
[![License](https://img.shields.io/badge/license-MIT-green)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen)](CONTRIBUTING.md)

> **Copy-paste patterns that turn any LLM agent into a specialist. No code. No setup. Just Markdown.**

## Quick Start

```bash
# 1. Pick a pattern and copy its SCHEMA.md into your agent
# 2. Run init
# 3. Start using it

# Example — Decision Journal:
# Copy patterns/life/decision-journal/SCHEMA.md into your agent
# Then:
"dj init"              # Creates .decisions/
"dj log Mi sono iscritto a un corso da €2000. Dubbio: vale la pena?"
                      # Creates a structured decision entry
"dj review"            # Shows all decisions, bias pattern, pending outcomes
```

## Patterns

### Dev
| Pattern | Problema | Ops | Stato |
|---------|----------|-----|-------|
| 🧑‍🌾 GitHub Gardener | Repository che degenerano, issue dimenticate, branch morti | 6 | ✅ |
| 🐛 Debug Diary | Risolvi lo stesso bug due volte perché hai dimenticato il fix | 5 | ✅ |
| ⚙️ Dotfiles Curator | Config dimenticate, alias morti, tool mai usati | 5 | ✅ |
| 🛡️ Server Sentinel | Server in down, log che nessuno legge, runbook inesistenti | 4 | ✅ |

### Knowledge
| Pattern | Problema | Ops | Stato |
|---------|----------|-----|-------|
| 🧠 LLM Wiki | Conoscenza frammentata, mai composta, sempre re-derivata | 5 | ✅ |
| 📚 Study Companion | Studi e dimentichi l'80%, non colleghi i concetti | 7 | ✅ |
| 📖 Reading Companion | Libri letti e dimenticati, idee mai estratte | 5 | ✅ |

### Life
| Pattern | Problema | Ops | Stato |
|---------|----------|-----|-------|
| 📓 Decision Journal | Dimentichi perché hai deciso, ripeti gli stessi bias | 5 | ✅ |
| ❤️ Health Timeline | Info mediche sparse tra PDF, app e memoria | 5 | ✅ |
| 🤝 Personal CRM | Perdi contatti, dimentichi compleanni e promesse | 5 | ✅ |
| 📋 Life Admin | Passaporto scaduto, abbonamenti fantasma, scadenze sparse | 5 | ✅ |
| 💰 Finance Narrator | Hai i dati ma nessuno ti racconta la storia dei tuoi soldi | 6 | ✅ |

### Work
| Pattern | Problema | Ops | Stato |
|---------|----------|-----|-------|
| 🗣️ Meeting Memory | 5 meeting al giorno, zero ricordo di chi ha deciso cosa | 5 | ✅ |
| 🔍 Project Postmortem | Stessi errori su progetti diversi, lezioni perse | 4 | ✅ |

### Creative
| Pattern | Problema | Ops | Stato |
|---------|----------|-----|-------|
| 🌍 World Bible | Occhi blu nel cap.3 e marroni nel cap.12 | 7 | ✅ |

## How It Works

```
  User                    Agent                     Workspace
  ─────                   ─────                     ─────────
  "st ingest" ──▶  ┌─────────────────┐  ──▶  .study/
                   │  SCHEMA.md       │        ├── index.md
  Appunti ──────▶  │  → Legge input   │  ──▶  ├── concepts/
                   │  → Crea/aggiorna │        ├── gaps.md
  "st quiz"  ──▶   │  → Collega       │  ──▶  └── review-queue.md
                   │  → Restituisce   │
                   └─────────────────┘
```

You do the thinking. The agent does the bookkeeping. The workspace is your persistent second brain — pure Markdown, portable forever.

## Why It Works

- **Dolore reale** — ogni pattern nasce da un problema che incontri ogni settimana, non da un'astrazione teorica
- **LLM fa il lavoro noioso** — aggiornare, collegare, ricordare, analizzare è ciò che gli agenti sanno fare meglio
- **Artefatto persistente** — il wiki Markdown vive oltre la chat. Lo riapri, lo cerchi, lo versioni
- **Zero codice, zero setup** — copi un file Markdown, scrivi `init`, e l'agente è specializzato
- **Effetto composto** — dopo 10 decisioni tracciate, dopo 20 lezioni processate, il wiki è un asset che cresce da solo

## Contribute

Hai un dolore ricorrente che un pattern LLM potrebbe risolvere? Apri una Issue o una PR.

→ [CONTRIBUTING.md](CONTRIBUTING.md)

## Philosophy

**You do the thinking. The agent does the bookkeeping.** Ogni pattern toglie all'umano il carico della memoria e dell'organizzazione. Non è automazione — è leverage. L'agente non decide per te, non crea per te, non pensa per te. Ti libera la mente per farlo.

## Versioning

`agent-patterns` follows [SemVer](https://semver.org/):

| Change | Version bump |
|--------|-------------|
| New pattern added | `0.X.0` (minor) |
| Fix/improvement to existing pattern | `0.X.Y` (patch) |
| All patterns complete + examples | `1.0.0` (major) |

## License

MIT
