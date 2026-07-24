# Life Admin

Un pattern LLM per tenere traccia di documenti, scadenze, abbonamenti e burocrazia. Il tuo agente monitora scadenze, ti alerta sui rinnovi e mantiene ordinata la tua vita amministrativa.

## Il problema

Passaporto in scadenza, assicurazione da rinnovare, abbonamenti che paghi ma non usi, tasse, contratti sparsi. Un caos di scadenze e documenti senza un punto centrale.

## La soluzione

Un wiki amministrativo che centralizza tutto: documenti, abbonamenti, scadenze, contratti. Il LLM tiene traccia delle date, prepara checklist e fa audit periodici.

```
wiki/
  ├── index.md           ← cruscotto: scadenze imminenti, alert
  ├── documents/         ← passaporto, patente, contratti, assicurazioni
  ├── subscriptions.md   ← abbonamenti con costo e ultimo uso
  ├── finances.md        ← tasse, rate, investimenti
  ├── calendar.md        ← scadenze future ordinate
  └── checklists/        ← procedure: rinnovo passaporto, cambio residenza, etc.
```

## Operazioni

| Comando | Descrizione |
|---------|-------------|
| `la add` | Registra un documento, abbonamento o scadenza |
| `la status` | Cruscotto: cosa sta per scadere, alert |
| `la audit` | Trova abbonamenti inutilizzati, documenti scaduti, contratti da rivedere |
| `la prep` | Prepara checklist per un'operazione (rinnovo, disdetta, etc.) |
| `la lint` | Gap: documenti mancanti, scadenze non tracciate, dati incompleti |

Vedi [SCHEMA.md](SCHEMA.md) per il prompt completo.
