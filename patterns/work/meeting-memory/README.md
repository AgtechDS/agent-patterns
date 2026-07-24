# 📋 Meeting Memory

Un pattern LLM per non perdere più nulla dei meeting. Ogni riunione produce decisioni strutturate, task tracciati, follow-up programmati.

## Il problema

5 meeting al giorno. Dopo una settimana non ricordi chi ha deciso cosa. Le action item si perdono in chat, email, documenti sparsi. Le decisioni vengono ribaltate perché nessuno ricorda il contesto originale. Ogni meeting è un'isola.

## La soluzione

Un wiki dei meeting: ogni riunione viene analizzata dal LLM che estrae decisioni, action item e follow-up. I meeting sullo stesso progetto vengono collegati. Le decisioni sono tracciabili nel tempo.

## Architettura

```
.meetings/
├── index.md              ← catalogo meeting per progetto
├── log.md                ← timeline cronologica
├── projects/             ← una pagina per progetto con decisioni aggregate
├── meetings/             ← una pagina per meeting
├── people-tasks.md       ← chi deve fare cosa, scadenze
├── decisions-log.md      ← registro decisioni cross-progetto
└── follow-ups.md         ← action item scadute o in scadenza
```

## Operazioni

| Comando | Cosa fa | Output |
|---------|---------|--------|
| `meeting ingest` | Carica note/trascrizione — estrae decisioni, task, follow-up | Pagina meeting + aggiornamento progetti |
| `meeting status` | "A che punto è il progetto X?" — sintesi multi-meeting | Report progetto |
| `meeting nudge` | "Chi ha task scaduti?" — elenco per persona o data | Lista task urgenti |
| `meeting prep` | "Domani ho meeting X" — brief pre-incontro | Documento pre-meeting |
| `meeting lint` | Decisioni contraddittorie, task senza owner, meeting senza follow-up | Report gap |

## Quick Start

1. Copia `SCHEMA.md` nel tuo agent
2. Digita `meeting init` per creare `.meetings/`
3. Dopo il prossimo meeting: `meeting ingest` e incolla le tue note

## Philosophy

- **Segnale, non rumore** — ogni meeting produce decisioni e task. Il resto (discussione, aggiornamenti) non si archivia.
- **Tracciabilità delle decisioni** — ogni decisione ha un contesto, un autore, un perché. Se viene ribaltata, si vede il cambiamento.
- **Proprietà chiara** — ogni task ha un owner. Senza owner non è un task.
- **Nessun giudizio** — le decisioni ribaltate non sono errori. Sono evoluzione del contesto. Si registrano e basta.

## Cosa NON è

- **Non è un verbalista** — non trascrive meeting. Elabora le note che l'umano gli dà.
- **Non è un tool di scheduling** — non fissa meeting. Non gestisce calendari.
- **Non è un CRM** — non traccia relazioni. Solo decisioni e task da meeting.

---

Part of [agent-patterns](https://github.com/AgtechDS/agent-patterns) · MIT
