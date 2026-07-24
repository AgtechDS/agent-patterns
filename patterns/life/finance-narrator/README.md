# 💰 Finance Narrator

Un pattern LLM che trasforma i tuoi dati finanziari in storie e insight. Non un expense tracker — un narratore che ti racconta dove vanno i tuoi soldi e perché.

## Il problema

I dati finanziari ci sono (estratto conto, app della banca) ma nessuno li interpreta. Vedi numeri, non capisci trend, non vedi pattern. Gli expense tracker ti danno grafici, non significato. Non sai se stai migliorando o peggiorando.

## La soluzione

Un wiki finanziario che il LLM aggiorna mese per mese: spese raccontate come storie, trend analizzati, anomalie segnalate, obiettivi tracciati con proiezioni narrative.

## Architettura

```
.finance/
├── index.md              ← overview: entrate, uscite, trend
├── log.md                ← timeline cronologica
├── months/               ← un "racconto" per mese
│   └── YYYY-MM.md
├── categories.md         ← trend per categoria (6 mesi)
├── subscriptions.md      ← abbonamenti attivi, costo, ultimo utilizzo
├── goals.md              ← obiettivi finanziari e progressi narrati
├── projections.md        ← proiezioni: "al ritmo attuale, tra X mesi..."
└── anomalies.md          ← spese insolite, pattern sospetti
```

## Operazioni

| Comando | Cosa fa | Output |
|---------|---------|--------|
| `finance ingest` | Carica CSV/estratto conto — scrive il racconto del mese | Pagina mese + aggiornamento trend |
| `finance compare` | Confronta con periodo precedente | Report confronto narrato |
| `finance audit` | Trova abbonamenti inutilizzati, spese anomale | Report anomalie |
| `finance project` | Proietta obiettivi: "Se continuo così, quando raggiungo X?" | Proiezione narrata |
| `finance lint` | Categorie incoerenti, transazioni duplicate, gap nei dati | Report gap |

## Quick Start

1. Copia `SCHEMA.md` nel tuo agent
2. Digita `finance init` per creare `.finance/`
3. Alla fine del mese: `finance ingest` con il tuo estratto conto

## Philosophy

- **Narrazione, non tabella** — ogni mese è un racconto. I numeri da soli non dicono nulla.
- **Zero giudizio** — "Spendi molto in delivery" è un dato. Non un commento morale.
- **Trend > snapshot** — un mese non fa un pattern. Il confronto è tutto.
- **Privacy** — dati finanziari locali. Mai inviati a servizi esterni.

## Cosa NON è

- **Non è un consulente finanziario** — non dà consigli. Non dice cosa fare con i soldi.
- **Non è un expense tracker** — non registra ogni caffè. Lavora su dati aggregati (CSV).
- **Non è un'app di banking** — non ha API, non si connette a banche. Funziona con ciò che l'utente carica.

---

Part of [agent-patterns](https://github.com/AgtechDS/agent-patterns) · MIT
