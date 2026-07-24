# Postmortem: Migrazione Cloud

**Date:** Apr-Giu 2026
**Risultato:** Successo (con ritardo di 2 settimane)
**Team:** 3 dev, 1 PM

## Cosa è andato bene
- Rollback testing: il piano di rollback ha funzionato perfettamente
- Comunicazione: standup giornalieri, nessuna sorpresa

## Cosa è andato male
- Stima tempi: overshooting del 25% (sottovalutata migrazione dati legacy)
- Documentazione: API docs aggiornate solo dopo 2 settimane dal go-live

## Lezioni
1. **Test con dati reali prima**: lo staging con dati anonimi non ha catturato edge case della migrazione
2. **Doc parallela**: aggiornare documentazione contestualmente, non dopo
