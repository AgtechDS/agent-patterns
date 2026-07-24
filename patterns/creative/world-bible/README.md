# 🌍 World Bible

Un pattern LLM per mantenere coerenza in mondi narrativi. Ogni personaggio, luogo, evento e regola ha una pagina wiki sincronizzata col testo.

## Il problema

Scrivi un romanzo, un gioco, una campagna D&D. Dopo 50 pagine non ricordi il colore degli occhi del personaggio secondario del capitolo 3. La timeline ha buchi. Le regole della magia cambiano senza accorgertene. I co-autori non hanno una fonte unica di verità. La continuità narrativa si perde.

## La soluzione

Un wiki del mondo narrativo che il LLM mantiene aggiornato a ogni capitolo. Personaggi, luoghi, timeline, regole — tutto sincronizzato. Il LLM segnala ogni incoerenza prima che arrivi al lettore.

## Architettura

```
.world/
├── index.md              ← catalogo: personaggi, luoghi, eventi
├── log.md                ← timeline di scrittura
├── characters/           ← scheda per personaggio
├── locations/            ← luoghi con descrizioni e mappe testuali
├── timeline.md           ← cronologia eventi della storia
├── rules.md              ← regole del mondo (magia, tecnologia, società)
├── glossary.md           ← termini inventati, nomi, lingue
├── consistency.md        ← contraddizioni rilevate e risolte
└── style.md              ← tono, voce narrante, regole di scrittura
```

## Operazioni

| Comando | Cosa fa | Output |
|---------|---------|--------|
| `world ingest` | Carica capitolo/brano — aggiorna personaggi, luoghi, timeline | Pagine aggiornate |
| `world check` | Verifica coerenza del capitolo con tutto il wiki | Report contraddizioni |
| `world query` | "Chi è X? Di che colore ha gli occhi Y?" | Scheda dal wiki |
| `world brainstorm` | "Come potrebbe evolvere X dato Y?" | Idee coerenti col mondo |
| `world lint` | Personaggi mai più menzionati, timeline gap, regole violate | Report gap |
| `world export` | Genera la bibbia completa del mondo | File unico riassuntivo |

## Quick Start

1. Copia `SCHEMA.md` nel tuo agent
2. Digita `world init` per creare `.world/`
3. Inizia con `world ingest` — carica il primo capitolo

## Philosophy

- **L'autore scrive, il LLM protegge** — non sostituisci la creatività. Mantieni la coerenza.
- **Ogni contraddizione è un'opportunità** — segnalata, non giudicata. A volte l'incoerenza è intenzionale (narratore inaffidabile).
- **Il glossario è legge** — nomi, luoghi, termini hanno una sola definizione. Tutto il resto vi si riferisce.
- **Append-only per timeline** — la cronologia non si modifica. Se scopri un errore, aggiungi una nota.

## Cosa NON è

- **Non è un generatore di storie** — non scrive capitoli, non crea trame. Mantiene ciò che l'autore crea.
- **Non è un editor** — non migliora la prosa, non corregge grammatica. Solo coerenza interna.
- **Non è un wiki generico** — è specializzato per mondi narrativi. Personaggi, archi, regole, glossario.

---

Part of [agent-patterns](https://github.com/AgtechDS/agent-patterns) · MIT
