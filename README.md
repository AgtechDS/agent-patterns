# agent-patterns

**Pattern LLM-ready per agent AI** — prompt strutturati, schemi e workflow pronti per Claude Code, OpenCode, Codex e qualsiasi agente LLM.

[![GitHub](https://img.shields.io/badge/patterns-15-blue)](https://github.com/AgtechDS/agent-patterns)
[![License](https://img.shields.io/badge/license-MIT-green)](LICENSE)

## Cos'è

Ogni pattern è un kit istantaneo: **README** (cosa fa, perché serve) + **SCHEMA.md** (prompt da copiare nell'agente) + **esempi** di wiki già popolato. Incolli lo SCHEMA, l'agente si specializza.

I pattern nascono da un'idea chiave: il LLM gestisce il bookkeeping (aggiornare, collegare, ricordare, analizzare), l'umano fa ciò che sa fare meglio (decidere, creare, pensare).

## Catalogo

### Dev
| Pattern | Cosa fa | Dolore |
|---------|---------|--------|
| [GitHub Gardener](patterns/dev/github-gardener/) | Manutenzione repo: issue, branch, PR, dipendenze | Repository che degenerano, issue dimenticate, branch morti |
| [Debug Diary](patterns/dev/debug-diary/) | Diario strutturato di bug, fix e pattern ricorrenti | Risolvi lo stesso bug due volte perché hai dimenticato il fix |
| [Dotfiles Curator](patterns/dev/dotfiles-curator/) | Analisi e documentazione di dotfile (zsh, git, nvim) | Config dimenticate, alias morti, tool mai usati |
| [Server Sentinel](patterns/dev/server-sentinel/) | Monitoraggio, diagnostica e runbook per servizi | Server in down, log che nessuno legge, runbook inesistenti |

### Knowledge
| Pattern | Cosa fa | Dolore |
|---------|---------|--------|
| [LLM Wiki](patterns/knowledge/llm-wiki/) | Wiki persistente da fonti multiple (pattern Karpathy) | Conoscenza frammentata, mai composta, sempre re-derivata |
| [Study Companion](patterns/knowledge/study-companion/) | Wiki di studio con spaced repetition e mappa concettuale | Studi e dimentichi l'80%, non colleghi i concetti |
| [Reading Companion](patterns/knowledge/reading-companion/) | Wiki companion per libri, capitolo per capitolo | Libri letti e dimenticati, idee mai estratte |

### Life
| Pattern | Cosa fa | Dolore |
|---------|---------|--------|
| [Decision Journal](patterns/life/decision-journal/) | Tracciamento decisioni, bias e risultati | Dimentichi perché hai deciso, ripeti gli stessi bias |
| [Health Timeline](patterns/life/health-timeline/) | Storia medica centralizzata: referti, farmaci, trend | Info mediche sparse tra PDF, app e memoria |
| [Personal CRM](patterns/life/personal-crm/) | Gestione relazioni: persone, interazioni, promesse | Perdi contatti, dimentichi compleanni e promesse |
| [Life Admin](patterns/life/life-admin/) | Documenti, abbonamenti, scadenze e burocrazia | Passaporto scaduto, abbonamenti fantasma, scadenze sparse |
| [Finance Narrator](patterns/life/finance-narrator/) | Racconto mensile delle finanze con trend e insight | Hai i dati ma nessuno ti racconta la storia dei tuoi soldi |

### Work
| Pattern | Cosa fa | Dolore |
|---------|---------|--------|
| [Meeting Memory](patterns/work/meeting-memory/) | Estrazione decisioni e task da meeting | 5 meeting al giorno, zero ricordo di chi ha deciso cosa |
| [Project Postmortem](patterns/work/project-postmortem/) | Retrospettive strutturate con lezioni cross-progetto | Stessi errori su progetti diversi, lezioni perse |

### Creative
| Pattern | Cosa fa | Dolore |
|---------|---------|--------|
| [World Bible](patterns/creative/world-bible/) | Wiki di mondi narrativi: personaggi, luoghi, timeline | Occhi blu nel cap.3 e marroni nel cap.12 |

## Come si usa

```
1. Scegli un pattern dal catalogo
2. Copia SCHEMA.md nel tuo agente (in una chat, in AGENTS.md, o in un file .md)
3. Usa il comando di init del pattern (es. "dj init", "ht init", "crm init")
4. Inizia a usare le operazioni: "dj log", "ht ingest", "crm update"
```

Tutti i pattern seguono la stessa architettura:

```
raw/              ← fonti, appunti, dati grezzi (li inserisci tu)
wiki/             ← wiki gestito dal LLM (scrive tutto lui)
  ├── index.md    ← catalogo/indice
  ├── log.md      ← cronologia append-only
  └── pages/      ← entità, concetti, decisioni, persone,...
schema/           ← SCHEMA.md (il prompt, lo incolli una volta)
```

## Struttura di un pattern

```
patterns/CATEGORIA/NOME/
├── README.md          ← descrizione, problema, soluzione, comandi
├── SCHEMA.md          ← prompt completo da incollare nell'agente
└── examples/          ← wiki già popolato per capire subito
```

## Per chi

- **Sviluppatori** che usano agent AI (Claude Code, Codex, OpenCode) e vogliono template pronti
- **Knowledge workers** che accumulano informazioni e vogliono un secondo cervello persistente
- **Scrittori e creativi** che devono mantenere coerenza nei mondi narrativi
- **Chiunque** abbia un problema di organizzazione che un LLM può risolvere

## Licenza

MIT
