# Personal CRM

Un pattern LLM per non perdere mai più un contatto. Il tuo agente tiene traccia di persone, interazioni, promesse e ti ricorda quando è il momento di sentirle.

## Il problema

Amici, colleghi, conoscenti, contatti professionali. Dimentichi compleanni, cosa vi siete detti l'ultima volta, promesse fatte. Passano mesi senza sentire persone importanti perché "tanto ci sentiamo presto". Non hai mai un briefing prima di un incontro.

## La soluzione

Un wiki relazionale dove ogni persona ha una pagina aggiornata: chi è, cosa avete in sospeso, di cosa avete parlato. Il LLM aggiorna al volo, ti fa i promemoria, prepara i briefing pre-incontro.

```
raw/                     ← note tue, screenshot chat, appunti (li butti giù tu)
wiki/
  ├── index.md           ← tutte le persone con stats
  ├── people/            ← una pagina per persona
  ├── circles.md         ← mappa: lavoro, amici, famiglia, hobby
  ├── nudge-log.md       ← storico promemoria inviati
  └── interactions.md    ← timeline cross-persona
```

## Operazioni

| Comando | Descrizione |
|---------|-------------|
| `crm add` | Aggiungi una nuova persona: contesto, come la conosci, note |
| `crm update` | "Ho incontrato X, mi ha detto che..." — aggiorna la pagina |
| `crm prep` | "Domani vedo X" — genera brief pre-incontro |
| `crm nudge` | Controlla relazioni in stallo, promemoria promise, ricorrenze |
| `crm review` | Report mensile: relazioni curate e trascurate, pattern sociali |
| `crm init` | Crea la struttura `personal-crm/` |

## Perché funziona

I CRM personali come Dex o Clay esistono ma richiedono inserimento manuale costante. Qui il LLM fa tutto il lavoro di aggiornamento, collegamento e promemoria — tu lasci solo note sporche.

Vedi [SCHEMA.md](SCHEMA.md) per il prompt completo da incollare nel tuo agent.
