# Project Postmortem

Un pattern LLM per imparare da ogni progetto finito (bene o male). Il tuo agente guida la retrospettiva, struttura le lezioni apprese e le rende disponibili per i progetti futuri.

## Il problema

I progetti finiscono e le lezioni si perdono. Stessi errori si ripetono su progetti diversi. Le retrospettive sono meeting senza seguito, i documenti postmortem nessuno li rilegge.

## La soluzione

Un wiki di postmortem: ogni progetto ha una retrospettiva strutturata, le lezioni sono collegate per tema, e il LLM le proietta sui progetti in corso per evitare ripetizioni.

```
wiki/
  ├── index.md           ← catalogo postmortem per progetto
  ├── postmortems/       ← una pagina per progetto
  ├── lessons.md         ← lezioni cross-progetto con pattern
  ├── recommendations.md ← raccomandazioni attive per progetti in corso
  └── templates/         ← template per postmortem
```

## Operazioni

| Comando | Descrizione |
|---------|-------------|
| `pp init` | Avvia postmortem per un progetto completato |
| `pp guide` | Guida strutturata: cosa è andato bene/male, cosa migliorare |
| `pp lessons` | Estrae lezioni e le collega a pattern pregressi |
| `pp apply` | Proietta lezioni sui progetti in corso |
| `pp review` | Report: pattern ricorrenti, trend, progresso nel tempo |

Vedi [SCHEMA.md](SCHEMA.md) per il prompt completo.
