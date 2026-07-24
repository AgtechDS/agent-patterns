# Decision Journal

Un pattern LLM per tracciare decisioni, bias e risultati. Il tuo agente fa da coach: struttura ogni decisione, ti ricorda di rivederle, e scopre i tuoi pattern mentali.

## Il problema

Prendiamo decisioni ogni giorno. Tra 6 mesi non ricordiamo più il ragionamento, le alternative scartate, i bias che ci hanno influenzato. Ripetiamo gli stessi errori perché non abbiamo memoria di *perché* abbiamo scelto.

## La soluzione

Un wiki persistente dove ogni decisione è una pagina strutturata: contesto, opzioni, scelta, ragionamento, risultato. Il LLM gestisce tutto il bookkeeping: crea, aggiorna, collega, e fa meta-analisi.

```
raw/                ← appunti, email, pro/contro (li scrivi tu)
wiki/
  ├── index.md      ← catalogo di tutte le decisioni
  ├── log.md        ← timeline cronologica
  └── decisions/    ← una pagina per decisione
```

## Operazioni

| Comando | Descrizione |
|---------|-------------|
| `dj log` | Registra una nuova decisione: struttura contesto, opzioni, scelta |
| `dj review` | Ogni mese: "Decisione X di 3 mesi fa, com'è andata?" |
| `dj lint` | Cerca bias ricorrenti, decisioni mai riviste, gap |
| `dj report` | Report completo con pattern e insight |
| `dj init` | Crea la struttura `decision-journal/` |

## Perché funziona

Nessun journaling tool fa questo. I diari esistono ma nessuno li *mantiene* e *analizza*. Il LLM è il coach che non si dimentica di chiederti conto delle tue scelte.

Vedi [SCHEMA.md](SCHEMA.md) per il prompt completo da incollare nel tuo agent.
