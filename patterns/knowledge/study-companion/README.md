# Study Companion

Un pattern LLM per studiare meglio e non dimenticare. Il tuo agente costruisce un wiki vivente della tua conoscenza, collega concetti e gestisce spaced repetition.

## Il problema

Studi un argomento, prendi appunti, dopo 2 settimane hai dimenticato l'80%. I concetti rimangono isolati, non vedi le connessioni. Anki aiuta ma sono flashcard senza contesto.

## La soluzione

Un wiki di studio che cresce con te: ogni concetto ha una pagina collegata ad altri, con spaced integration (non solo ripetizione) e mappa delle connessioni.

```
wiki/
  ├── index.md           ← mappa concettuale
  ├── concepts/          ← una pagina per concetto
  ├── connections.md     ← come X si collega a Y
  ├── gaps.md            ← concetti non consolidati
  └── review-queue.md    ← spaced repetition: cosa ripassare oggi
```

## Operazioni

| Comando | Descrizione |
|---------|-------------|
| `st ingest` | Aggiungi appunti/lezione — crea/aggiorna pagine concetto |
| `st quiz` | Genera domande sui concetti da ripassare |
| `st connect` | Trova e documenta connessioni tra concetti |
| `st review` | Report: argomenti solidi, gap, trend |
| `st lint` | Trova concetti isolati, definizioni incomplete, buchi |

Vedi [SCHEMA.md](SCHEMA.md) per il prompt completo.
