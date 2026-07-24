# Dotfiles Curator

Un pattern LLM per mantenere ordinati e documentati i tuoi dotfile (config shell, editor, tooling). Il tuo agente analizza, documenta e suggerisce miglioramenti.

## Il problema

I dotfile accumulano config dimenticate, alias morti, tool installati e mai usati, setting contraddittori. Non sai cosa fa ogni riga. Hai paura di pulire perché "potrebbe rompere qualcosa".

## La soluzione

Un wiki dei tuoi dotfile: ogni file documentato, ogni configurazione spiegata, tool obsoleti identificati, conflitti segnalati.

```
wiki/
  ├── index.md           ← mappa di tutti i dotfile
  ├── files/             ← una pagina per file (~/.zshrc, ~/.gitconfig, etc.)
  ├── tools.md           ← tool installati, versioni, ultimo uso
  ├── conflicts.md       ← config contraddittorie
  └── orphans.md         ← tool/config orfane
```

## Operazioni

| Comando | Descrizione |
|---------|-------------|
| `dc scan` | Analizza tutti i dotfile e crea la mappa |
| `dc doc` | Documenta un file: spiega ogni sezione |
| `dc prune` | Trova alias morti, path inesistenti, tool non usati |
| `dc audit` | Trova conflitti, duplicati, security issue |
| `dc sync` | Confronta tra macchine e segnala differenze |

Vedi [SCHEMA.md](SCHEMA.md) per il prompt completo.
