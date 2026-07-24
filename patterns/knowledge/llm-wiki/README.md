# LLM Wiki

Il pattern originale di Andrej Karpathy: un wiki persistente mantenuto dal tuo LLM. Ogni fonte viene compilata una volta e il wiki si arricchisce nel tempo.

## Il problema

La conoscenza che accumuli (articoli, paper, appunti) rimane frammentata. Ogni volta che vuoi un'informazione devi re-derivarla. Le connessioni tra concetti non emergono mai.

## La soluzione

Un wiki intrecciato dove ogni fonte diventa pagine collegate. Il LLM fa il bookkeeping: crea, aggiorna, collega e mantiene. L'umano cura le fonti e fa le domande giuste.

```
raw/                    ← fonti originali (immutabili)
wiki/
  ├── index.md          ← catalogo pagine
  ├── log.md            ← cronologia operazioni
  └── pages/            ← pagine wiki generate dal LLM
```

## Operazioni

| Comando | Descrizione |
|---------|-------------|
| `wiki ingest` | Aggiungi una fonte → il LLM scrive pagine e aggiorna l'indice |
| `wiki query` | Fai una domanda → il LLM cerca nel wiki e sintetizza |
| `wiki lint` | Trova contraddizioni, pagine orfane, gap |
| `wiki connect` | Trova connessioni tra pagine esistenti |

Vedi [SCHEMA.md](SCHEMA.md) per il prompt completo.
