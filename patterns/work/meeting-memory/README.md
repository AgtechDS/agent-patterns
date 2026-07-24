# Meeting Memory

Un pattern LLM per non perdere più nulla dei meeting. Il tuo agente estrae decisioni, action item e follow-up da trascrizioni e note.

## Il problema

5 meeting al giorno. Dopo una settimana non ricordi chi ha deciso cosa. Le action item si perdono in chat, email, documenti sparsi. Ogni meeting è un'isola.

## La soluzione

Un wiki dei meeting: ogni riunione produce decisioni strutturate, task tracciati, follow-up programmati. Il LLM collega tra loro meeting sullo stesso progetto.

```
wiki/
  ├── index.md           ← cruscotto: decisioni recenti, task aperti
  ├── meetings/          ← una pagina per meeting
  ├── decisions-log.md   ← registro decisioni cross-meeting
  ├── tasks.md           ← tabella task con assignee e scadenza
  └── projects/          ← una pagina per progetto (sintesi multi-meeting)
```

## Operazioni

| Comando | Descrizione |
|---------|-------------|
| `mm ingest` | Carica trascrizione/note — estrai decisioni, task, follow-up |
| `mm status` | "A che punto è il progetto X?" — sintesi da tutti i meeting |
| `mm tasks` | Lista task aperti per persona o scadenza |
| `mm followup` | Trova decisioni senza azione, task scaduti, gap |
| `mm review` | Report settimanale: meeting fatti, decisioni, task completati |

Vedi [SCHEMA.md](SCHEMA.md) per il prompt completo.
