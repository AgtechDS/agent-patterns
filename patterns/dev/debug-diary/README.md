# Debug Diary

Un pattern LLM per non risolvere mai più lo stesso bug due volte. Il tuo agente mantiene un diario strutturato di bug, fix e lezioni apprese.

## Il problema

Risolvi un bug. Tre mesi dopo, stesso bug, stessi sintomi. Hai dimenticato il fix, il contesto, la causa radice. Perdi ore a re-diagnosticare.

## La soluzione

Un wiki di debug dove ogni bug è una pagina strutturata: sintomi, cause, fix, lezioni. Categorizzato e ricercabile.

```
wiki/
  ├── index.md           ← catalogo bug per sistema/area
  ├── bugs/              ← una pagina per bug
  ├── patterns.md        ← pattern ricorrenti: "ogni volta che X, succede Y"
  └── log.md             ← timeline dei fix
```

## Operazioni

| Comando | Descrizione |
|---------|-------------|
| `dd log` | Registra un bug con sintomi, diagnosi, fix |
| `dd search` | Cerca bug simili per sintomo o messaggio d'errore |
| `dd patterns` | Analisi pattern ricorrenti |
| `dd review` | "Bug X è ricomparso?" — confronta con storico |

Vedi [SCHEMA.md](SCHEMA.md) per il prompt completo.
