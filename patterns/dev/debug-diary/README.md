# 🐛 Debug Diary

Un pattern LLM per non risolvere mai più lo stesso bug due volte. Ogni bug ha una pagina: sintomi, root cause, fix, prevenzione.

## Il problema

Risolvi un bug alle 2 di notte. Tre mesi dopo, lo stesso identico bug si ripresenta. Non ricordi come l'hai risolto. Stack Overflow non ha il tuo caso specifico. Il commit del fix dice solo "fix bug" — zero contesto. Perdi ore a re-diagnosticare.

## La soluzione

Un wiki di debug dove ogni bug è una pagina strutturata: sintomi esatti, tentativi falliti, root cause, fix applicato, prevenzione. Il LLM rende tutto ricercabile e collegato.

## Architettura

```
.debug/
├── index.md              ← catalogo bug per sistema/area
├── log.md                ← timeline cronologica
├── bugs/                 ← una pagina per bug
│   └── DD-001.md         ← sintomi, ambiente, root cause, fix
├── patterns.md           ← "i bug X tornano sempre a causa di Y"
└── environment.md        ← snapshot dell'ambiente (OS, versioni, config)
```

## Operazioni

| Comando | Cosa fa | Output |
|---------|---------|--------|
| `debug log` | Registra un bug risolto: sintomi, tentativi, root cause, fix | Pagina bug + aggiornamento index |
| `debug search` | Cerca nei bug passati per sintomo o messaggio errore | Lista bug correlati |
| `debug review` | Revisione mensile: bug ricorrenti, trend, aree critiche | Report statistiche |
| `debug lint` | Trova fix orfani, bug senza root cause, workaround temporanei | Report gap |
| `debug export` | Genera knowledge base in unico file | File riassuntivo |

## Quick Start

1. Copia `SCHEMA.md` nel tuo agent
2. Digita `debug init` per creare `.debug/` e la struttura
3. Al prossimo bug: `debug log` e descrivi sintomi e fix

## Philosophy

- **Documenta, non fissare** — il LLM non risolve il bug. Documenta la soluzione che hai trovato.
- **I fallimenti contano** — i tentativi falliti sono importanti quanto il fix finale.
- **Collegamento a codice** — ogni bug deve linkare a commit, PR, file quando possibile.
- **Pattern emerge** — dopo 5-10 bug, emergono pattern di sistema e aree fragili.

## Cosa NON è

- **Non è un debugger** — non esegue codice, non analizza stack trace in tempo reale. Lavora su ciò che l'umano gli racconta.
- **Non è un issue tracker** — non sostituisce GitHub Issues. È un diario personale di apprendimento.
- **Non è una knowledge base automatica** — non scansiona codici o commit. L'umano decide cosa registrare.

---

Part of [agent-patterns](https://github.com/AgtechDS/agent-patterns) · MIT
