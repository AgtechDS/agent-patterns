# Finance Narrator

Un pattern LLM che trasforma i tuoi dati finanziari in storie e insight. Non un expense tracker — un narratore che ti racconta dove vanno i tuoi soldi e perché.

## Il problema

I dati finanziari ci sono (estratto conto, app della banca) ma nessuno li interpreta. Vedi numeri, non capisci trend, non vedi pattern. Gli expense tracker ti danno grafici, non significato.

## La soluzione

Un wiki finanziario che il LLM aggiorna mese per mese: spese raccontate, trend analizzati, anomalie segnalate, obiettivi tracciati con narrazione.

```
wiki/
  ├── index.md           ← cruscotto: patrimonio, spesa mensile, trend
  ├── months/            ← un racconto per mese
  ├── categories.md      ← trend per categoria con insight
  ├── anomalies.md       ← spese anomale, abbonamenti fantasma
  ├── goals.md           ← obiettivi finanziari con progresso narrato
  └── projections.md     ← proiezioni: "al ritmo attuale, tra X mesi..."
```

## Operazioni

| Comando | Descrizione |
|---------|-------------|
| `fn ingest` | Carica estratto conto CSV — il LLM scrive il racconto del mese |
| `fn review` | Confronta con mese/anno scorso, evidenzia trend |
| `fn query` | "Quanto ho speso in ristoranti quest'anno?" con insight |
| `fn goal` | Definisci/traccia un obiettivo finanziario |
| `fn alert` | Trova anomalie, abbonamenti inutilizzati, categorie in crescita |

Vedi [SCHEMA.md](SCHEMA.md) per il prompt completo.
