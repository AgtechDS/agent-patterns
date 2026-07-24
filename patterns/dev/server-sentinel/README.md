# Server Sentinel

Un pattern LLM per monitorare e diagnosticare server e servizi. Il tuo agente analizza log, metriche e configurazioni, segnala anomalie e suggerisce remediation.

## Il problema

Server che vanno in down, log che nessuno legge, metriche dimenticate, config che derivano. Scopri i problemi quando l'utente li segnala, non prima.

## La soluzione

Un wiki di osservabilità: ogni server documentato, ogni servizio tracciato, log analizzati, pattern di failure identificati.

```
wiki/
  ├── index.md           ← cruscotto: stato servizi, alert recenti
  ├── services/          ← una pagina per servizio (dipendenze, metriche, runbook)
  ├── incidents/         ← incident report con timeline e RCA
  ├── alerts.md          ← alert rules e soglie
  └── patterns.md        ← pattern di failure ricorrenti
```

## Operazioni

| Comando | Descrizione |
|---------|-------------|
| `ss register` | Aggiungi un server/servizio al monitoraggio |
| `ss diagnose` | Analizza log recenti, segnala anomalie |
| `ss alert` | Configura/aggiorna soglie di alert |
| `ss incident` | Registra un incidente con timeline e RCA |
| `ss review` | Report periodico: uptime, trend, capacity |
| `ss runbook` | Genera runbook per un servizio |

Vedi [SCHEMA.md](SCHEMA.md) per il prompt completo.
