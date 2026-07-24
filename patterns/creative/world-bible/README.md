# World Bible

Un pattern LLM per mantenere coerenza in mondi narrativi. Il tuo agente è il continuity editor del tuo romanzo, gioco, fumetto o campagna D&D.

## Il problema

Scrivi un romanzo: dopo 50 pagine non ricordi il colore degli occhi del personaggio secondario del capitolo 3. La timeline ha buchi. La geografia è contraddittoria. La magia ha regole che cambi senza accorgertene.

## La soluzione

Un wiki del tuo mondo narrativo: personaggi, luoghi, timeline, regole. Ogni capitolo aggiorna il wiki. Il LLM segnala ogni incoerenza prima che arrivi al lettore.

```
wiki/
  ├── index.md           ← mappa del mondo: tutto a colpo d'occhio
  ├── characters/        ← una pagina per personaggio
  ├── locations/         ← luoghi con descrizioni e mappe testuali
  ├── timeline.md        ← cronologia eventi della storia
  ├── rules.md           ← regole del mondo (magia, tecnologia, società)
  ├── factions.md        ← organizzazioni e gruppi
  ├── lore.md            ← mitologia, storia antica, leggende
  └── consistency.md     ← contraddizioni trovate e risolte
```

## Operazioni

| Comando | Descrizione |
|---------|-------------|
| `wb ingest` | Carica capitolo/brano — aggiorna personaggi, luoghi, timeline |
| `wb check` | Verifica coerenza: contraddizioni con il resto del mondo |
| `wb profile` | "Chi è X?" — scheda completa da tutte le menzioni |
| `wb timeline` | Mostra timeline eventi con filtri |
| `wb brainstorm` | Genera idee coerenti con il mondo esistente |
| `wb lint` | Trova buchi di trama, personaggi dimenticati, regole violate |

Vedi [SCHEMA.md](SCHEMA.md) per il prompt completo.
