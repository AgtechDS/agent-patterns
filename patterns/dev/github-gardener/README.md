# GitHub Gardener

Pattern per agent AI che mantiene in ordine le repository GitHub. Analizza, documenta e suggerisce — non tocca mai il codice.

## Comandi

| Comando | Descrizione |
|---------|-------------|
| `garden init` | Crea `.garden/` e primo snapshot |
| `garden triage` | Analizza issue: categorizza, stale, suggerisce chiusure |
| `garden prune` | Trova branch morti, PR abbandonate, file orfani |
| `garden refresh` | Confronta README/CONTRIBUTING/CHANGELOG con la realtà |
| `garden audit` | Dipendenze outdated, vulnerabilità, licenze, CI |
| `garden report` | Report completo con Top 5 priorità |
| `garden log` | Storico operazioni |

## Regola d'oro

Il Gardener **non tocca mai il codice**. Analizza, documenta, suggerisce. Le azioni distruttive sono sempre suggerimenti che l'umano approva.

Vedi [SCHEMA.md](SCHEMA.md) per il prompt completo da incollare nell'agent.
