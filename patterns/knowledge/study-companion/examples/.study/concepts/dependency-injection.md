# Dependency Injection

**Modulo:** Architettura Software
**Livello:** 4
**Ultimo ripasso:** 2026-07-22
**Prossimo ripasso:** 2026-08-05

## Definizione
Passare le dipendenze di una classe dall'esterno anziché crearle dentro. Invece di `new Database()` nel costruttore, ricevi `Database` come parametro. Questo rende il codice testabile e disaccoppiato.

## Esempi
- `class UserService { constructor(db: Database) {} }` invece di `constructor() { this.db = new Database(); }`
- Test: passo un mock di `Database` invece di quello vero

## Collegamenti
- **[[clean-architecture]]** — necessario: senza DI non puoi invertire dipendenze ai confini dell'architettura
- **[[solid-principles]]** — esemplifica: DIP in pratica — dipendi da interfacce, non da implementazioni

## Domande frequenti
- **DI Container sì o no?** Utile in app complesse, inutile in script e app semplici. Il pattern non richiede un container.
- **Constructor vs Setter?** Constructor injection è preferibile — le dipendenze sono obbligatorie e immutabili.

## Note personali
All'inizio mi sembrava solo complessità inutile. Poi ho scritto test senza DI e ho capito. È come la differenza tra saldare un componente e infilarlo in una presa.
