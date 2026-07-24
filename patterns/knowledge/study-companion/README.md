# 📚 Study Companion

Un pattern LLM che trasforma i tuoi appunti in un wiki vivente della conoscenza. Spaced repetition, mappa concettuale, auto-valutazione — tutto in Markdown.

## Il problema

Studi un argomento (corso, libro, tutorial) e dopo 2 settimane hai dimenticato l'80%. I concetti rimangono isolati — non sai come X si collega a Y. Gli appunti accumulano polvere: un cimitero di note che non rileggi mai. Anki aiuta ma sono flashcard senza contesto.

## La soluzione

Un wiki di studio che cresce con te: ogni concetto ha una pagina, collegamenti ad altri concetti, spaced repetition integrata e auto-valutazioni periodiche.

## Architettura

```
.study/
├── index.md           ← catalogo concetti per modulo/argomento
├── log.md             ← timeline di studio (append-only)
├── concepts/          ← una pagina per concetto
│   └── NOME.md        ← definizione, esempi, collegamenti, livello 1-5
├── gaps.md            ← concetti non ancora consolidati
├── connections.md     ← mappa: come X si collega a Y
├── review-queue.md    ← spaced repetition: cosa ripassare oggi
└── exams/             ← auto-valutazioni e risultati
    └── MODULO.md
```

## Operazioni

| Comando | Cosa fa | Output |
|---------|---------|--------|
| `st ingest` | Carica appunti/lezione — crea/aggiorna pagine concetto | Concetti aggiornati + collegamenti nuovi |
| `st quiz` | Genera domande sui concetti più deboli | Quiz con autovalutazione |
| `st connect` | Trova e documenta connessioni tra due concetti | Relazione + spiegazione + esempi |
| `st review` | Spaced repetition: cosa ripassare oggi | Coda ripasso con priorità |
| `st assess` | Auto-valutazione per modulo | Report comprensione per concetto |
| `st lint` | Trova concetti orfani, definizioni copiate, gap | Report gap |

## Quick Start

1. Copia `SCHEMA.md` nel tuo agente
2. Digita `st init` per creare `.study/`
3. Dopo la prossima lezione: `st ingest` con i tuoi appunti

## Philosophy

- **Il LLM non insegna** — organizza, collega e testa la TUA comprensione. Lo studio lo fai tu.
- **Definisci CON PAROLE TUE** — se la definizione è copiata, non l'hai capita. Il lint lo segnala.
- **I collegamenti sono tutto** — un concetto isolato è un concetto dimenticabile. Ogni pagina deve collegarsi ad almeno un'altra.
- **Il gap è un gap** — non riempire i buchi con supposizioni. Segnali e basta. La consapevolezza dei propri buchi è più importante del falso senso di completezza.

## Cosa NON è

- **Non è un tutor** — non spiega concetti, non fa lezione, non corregge errori di comprensione.
- **Non è Anki** — Anki ripete. Questo pattern connette. Le flashcard sono un sottoprodotto, non l'obiettivo.
- **Non è un notes app** — prende i tuoi appunti e li struttura. Non sostituisce Obsidian/Notion — li integra.

---

Part of [agent-patterns](https://github.com/AgtechDS/agent-patterns) · MIT
