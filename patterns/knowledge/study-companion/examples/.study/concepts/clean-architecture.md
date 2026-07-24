# Clean Architecture

**Modulo:** Architettura Software
**Livello:** 3
**Ultimo ripasso:** 2026-07-20
**Prossimo ripasso:** 2026-07-27

## Definizione
Un'architettura a cerchi concentrici dove il dominio sta al centro e non dipende da nulla. I dettagli esterni (database, framework, UI) sono plugin del dominio. La regola d'oro: le dipendenze vanno verso l'interno, mai verso l'esterno.

## Esempi
- Un'entità `Ordine` nel core non sa se i dati arrivano da PostgreSQL o MongoDB
- Il caso d'uso `CreaOrdine` non importa Express o React — riceve dati da un controller che è un dettaglio

## Collegamenti
- **[[dependency-injection]]** — richiede: Clean Architecture ha bisogno di DI per invertire le dipendenze ai confini
- **[[repository-pattern]]** — richiede: Repository è l'interfaccia ai confini che il core definisce
- **[[solid-principles]]** — analogo: DIP (Dependency Inversion) è lo stesso principio applicato a livello di classe

## Domande frequenti
- **Differenza con Hexagonal Architecture?** Nessuna — stesso principio, nomi diversi. Clean è più stratificata, Hexagonal è più centrata sui port/adapter.
- **Quando è overkill?** CRUD semplice con un database solo. Lì stratificare pulisce ma non porta beneficio netto.

## Note personali
Mi ricorda gli strati di una cipolla. Più vai dentro, più è stabile. Il problema è che all'inizio è difficile decidere cosa è "dominio" e cosa è "dettaglio".
