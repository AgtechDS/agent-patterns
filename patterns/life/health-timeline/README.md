# Health Timeline

Un pattern LLM per centralizzare la tua storia medica. Il tuo agente estrae dati da referti, monitora trend, prepara i briefing per le visite e non dimentica mai una scadenza.

## Il problema

Referti in PDF sparsi, farmaci di cui non ricordi il dosaggio, sintomi che non hai mai collegato, analisi del sangue di 2 anni fa che nessuno ha mai confrontato. Dal dottore non hai mai una timeline completa.

## La soluzione

Un wiki medico persistente che il LLM mantiene aggiornato. Ogni referto diventa dati strutturati. Ogni visita ha un brief preparato. Ogni valore di laboratorio viene confrontato con i precedenti.

```
raw/                     ← referti PDF, foto, note sintomi (li metti tu)
wiki/
  ├── index.md           ← profilo sintetico: condizioni, farmaci, allergie
  ├── timeline.md        ← cronologia completa: eventi, visite, esami
  ├── conditions/        ← una pagina per condizione (diagnosi, evoluzione)
  ├── medications.md     ← farmaci attuali e passati con dosaggi
  ├── lab-results.md     ← storico esami con trend e anomalie
  ├── questions.md       ← domande accumulate per il prossimo medico
  ├── prep/              ← briefing generati per ogni visita
  └── gaps.md            ← screening in scadenza, esami dimenticati
```

## Operazioni

| Comando | Descrizione |
|---------|-------------|
| `ht ingest` | Estrai dati da un referto: valori, diagnosi, prescrizioni |
| `ht prep` | Prepara il brief per una visita specialistica |
| `ht review` | Confronta gli ultimi esami con i precedenti, segnala trend |
| `ht lint` | Cerca gap: screening in ritardo, farmaci non rivisti, sintomi isolati |
| `ht timeline` | Mostra la cronologia completa di un periodo o condizione |
| `ht init` | Crea la struttura `health-timeline/` |

## Perché funziona

Il problema medico è universale ma nessun tool lo risolve in modo semplice. O hai un' app per farmaci, una per referti, una per sintomi — mai tutto insieme. Il LLM diventa il tuo **centralizzatore medico** che vede il quadro completo.

Vedi [SCHEMA.md](SCHEMA.md) per il prompt completo da incollare nel tuo agent.
