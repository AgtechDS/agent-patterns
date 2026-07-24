# Mappa delle connessioni

## Richiede: Clean Architecture ←→ Dependency Injection

**Spiegazione:** La Clean Architecture richiede DI per funzionare. I confini tra i cerchi (core → database, core → UI) hanno bisogno di inversione di dipendenza, e DI è il meccanismo che la realizza. Senza DI, i confini diventano dipendenze dirette e l'architettura collassa.

**Esempi:**
- Il `UserRepository` è un'interfaccia nel core, implementata in infrastructure e iniettata via costruttore.

**Implicazioni:**
- Non puoi fare Clean Architecture senza padroneggiare DI
- Framework come Spring/Angular hanno DI nativa — non è un caso

## Esemplifica: Dependency Injection ←→ SOLID Principles (DIP)

**Spiegazione:** DI è l'implementazione pratica del Dependency Inversion Principle (DIP): dipendi da astrazioni, non da concretizzazioni. Iniettando `Database` (interfaccia) invece di new `PostgreSQLDatabase()`, applichi DIP.

**Implicazioni:**
- Capire DIP aiuta a capire perché DI esiste
- Se un codice rispetta DIP, DI viene naturale
