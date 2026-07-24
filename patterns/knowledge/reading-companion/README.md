# Reading Companion

Un pattern LLM per leggere libri tecnici/saggi in modo attivo e strutturato. Il tuo agente costruisce un wiki companion del libro, capitolo per capitolo.

## Il problema

Leggi libri non-fiction, prendi appunti, ma dopo mesi ricordi solo il 10%. Non hai un sistema per estrarre e collegare le idee chiave. Un libro letto è un libro dimenticato.

## La soluzione

Un wiki companion per ogni libro: riassunti per capitolo, concetti chiave, citazioni, connessioni tra libri. Il wiki diventa il tuo secondo cervello di lettura.

```
wiki/
  ├── index.md           ← scheda libro + mappa concetti
  ├── chapters/          ← un riassunto per capitolo
  ├── concepts.md        ← idee chiave con riferimenti
  ├── quotes.md          ← citazioni con contesto
  └── connections.md     ← connessioni con altri libri/concetti
```

## Operazioni

| Comando | Descrizione |
|---------|-------------|
| `rc init` | Inizia un nuovo libro: crea struttura wiki |
| `rc chapter` | Aggiunge riassunto di un capitolo |
| `rc concept` | Estrae e collega concetti chiave |
| `rc connect` | Trova connessioni tra libri diversi |
| `rc review` | Report del libro finito: 10 idee chiave |
| `rc lint` | Trova capitoli non sintetizzati, gap |

Vedi [SCHEMA.md](SCHEMA.md) per il prompt completo.
