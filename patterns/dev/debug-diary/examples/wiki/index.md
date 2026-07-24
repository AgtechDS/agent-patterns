# Catalogo Bug

| ID | Data | Sistema | Sintomo | Causa | Stato |
|----|------|---------|---------|-------|-------|
| DD-001 | 2026-06-15 | Backend API | GET /users timeout dopo 30s | N+1 query su ORM | Risolto |
| DD-002 | 2026-07-01 | Frontend | Pagina bianca su Safari | Polyfill mancante | Risolto |
| DD-003 | 2026-07-10 | Database | Deadlock su INSERT concorrenti | Lock order non deterministico | In analisi |
