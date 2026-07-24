# 🏥 Health Timeline

Un pattern LLM per centralizzare la tua storia medica. Ogni referto diventa dati strutturati. Ogni visita ha un brief preparato. Ogni valore di laboratorio viene confrontato con i precedenti.

## Il problema

Le tue informazioni mediche sono frammentate: referti in PDF sparsi, farmaci di cui non ricordi il dosaggio, sintomi che non hai mai collegato. Dal dottore non hai mai una timeline completa. Nessun tool mantiene una storia medica coerente e aggiornata per te.

## La soluzione

Un wiki medico persistente che il LLM mantiene aggiornato. Ogni referto viene analizzato e strutturato, ogni farmaco tracciato, ogni valore di laboratorio confrontato con lo storico. Il LLM prepara i briefing per le visite e segnala trend, gap e anomalie.

## Architettura

```
.health/
├── index.md              ← catalogo: condizioni, farmaci, visite
├── log.md                ← timeline cronologica eventi medici
├── timeline.md           ← narrazione cronologica della salute
├── conditions/           ← una pagina per condizione
├── medications.md        ← farmaci attuali e passati, dosaggi, interazioni
├── visits/               ← una pagina per visita medica
├── labs/                 ← risultati analisi con trend
├── questions.md          ← domande da fare al prossimo medico
└── patterns.md           ← correlazioni e osservazioni
```

## Operazioni

| Comando | Cosa fa | Output |
|---------|---------|--------|
| `health ingest` | Aggiungi referto/analisi/visita — estrae dati, aggiorna timeline | Pagine aggiornate, anomalie segnalate |
| `health prep` | Prepara brief per una visita medica specifica | File pre-visita con storia, farmaci, domande |
| `health track` | Registra un sintomo o un farmaco | Entry in log + aggiornamento pagina |
| `health review` | Revisione periodica: farmaci attivi, visite mancanti, analisi scadute | Report con raccomandazioni |
| `health query` | Cerca nella storia medica | Risposta con citazioni alle fonti |
| `health lint` | Trova interazioni farmaci, valori anomali, gap temporali | Report gap e anomalie |

## Quick Start

1. Copia `SCHEMA.md` nel tuo agent
2. Digita `health init` per creare `.health/` e la struttura
3. Inizia con `health ingest` — carica un referto e lascia che il LLM lo strutturi

## Philosophy

- **Il LLM non fa diagnosi** — estrae, organizza, confronta, segnala. Mai dire "hai X".
- **Dati locali e privati** — tutto rimane in file Markdown. Nessun dato inviato a servizi esterni.
- **Trend, non snapshot** — un valore fuori range è un dato. Un trend su 3 misurazioni è un segnale.
- **Tracciabilità** — ogni valore ha data e fonte. Mai dati senza referto.

## Cosa NON è

- **Non è un medical record** — non sostituisce il fascicolo sanitario elettronico. È un companion personale.
- **Non è un diagnostic tool** — non interpreta sintomi. Non suggerisce cure.
- **Non è un'app medica** — non ha API, non si integra con SSN. Funziona con ciò che l'utente carica.

---

Part of [agent-patterns](https://github.com/AgtechDS/agent-patterns) · MIT
