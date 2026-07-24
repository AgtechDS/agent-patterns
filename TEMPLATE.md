# TEMPLATE — agent-patterns

Questo documento definisce il formato canonico che ogni pattern deve seguire. Usalo come checklist quando crei un nuovo pattern.

---

## README.md

### 1. Titolo + emoji + tagline (una riga)

```
# 🏷️ Nome Pattern

Una riga che spiega cosa fa, per chi, e perché è utile.
```

Esempio: `# 🔧 GitHub Gardener — Un pattern LLM per mantenere in ordine le repository GitHub. Analizza, documenta e suggerisce — non tocca mai il codice.`

### 2. The Problem (3-5 righe)

Dolore concreto in seconda persona ("You..."). Descrivi il problema prima della soluzione.

```
## Il problema

[Descrivi cosa succede senza il pattern. Frase di apertura forte, poi 2-3 esempi concreti. Finisci con il costo nascosto.]
```

### 3. The Pattern (una riga)

```
## La soluzione

[Una frase che riassume cosa fa il pattern e come risolve il problema sopra.]
```

### 4. Architecture (diagramma ASCII)

```
## Architettura

```
wiki/
  ├── index.md    ← [cosa contiene]
  ├── log.md      ← [cosa contiene]
  └── pages/      ← [cosa contiene]
```
```

Mostra **solo** la struttura wiki. `raw/` e `schema/` sono comuni a tutti.

### 5. Operations (tabella)

```
## Operazioni

| Comando | Cosa fa | Output |
|---------|---------|--------|
| `pat init` | [azione] | [file creato/aggiornato] |
| `pat log` | [azione] | [file creato/aggiornato] |
```

Ogni operazione deve essere un verbo attivo. Prefisso di 2-4 lettere.

### 6. Quick Start (3 step)

```
## Quick Start

1. [Step 1 — copiare lo SCHEMA nell'agent]
2. [Step 2 — eseguire init]
3. [Step 3 — prima operazione concreta]
```

### 7. Philosophy (3-5 bullet)

```
## Philosophy

- **[Valore 1]** — [perché è importante, cosa cambia]
- **[Valore 2]** — [come si differenzia da altri approcci]
- **[Valore 3]** — [il confine: cosa il pattern NON fa]
```

### 8. What This Is NOT (3 bullet)

```
## Cosa NON è

- **[Fraintendimento 1]** — [correzione]
- **[Fraintendimento 2]** — [correzione]
- **[Fraintendimento 3]** — [correzione]
```

### 9. Footer

```
---

Part of [agent-patterns](https://github.com/AgtechDS/agent-patterns) · MIT
```

---

## SCHEMA.md

### 1. Identità e ruolo

```
# Nome Pattern — SCHEMA

Sei **[Nome]**, [chi sei e cosa fai in 2-3 righe].

## Cosa fai

[Elenco puntato delle tue responsabilità]

## Cosa NON fai

[Elenco puntato dei limiti espliciti]
```

### 2. Struttura del workspace

```
## Struttura

```
nome-workspace/
├── index.md              ← [descrizione]
├── log.md                ← [descrizione]
└── [directory]/          ← [descrizione]
    └── [file-template]   ← [descrizione]
```
```

Ogni riga commentata deve spiegare il *ruolo* del file, non solo il nome.

### 3. Formato dei file

Per ogni tipo di pagina generata, mostra il template esatto:

```
### `index.md`

```markdown
[template completo del file]
```

### `pagina-tipo.md`

```markdown
[template completo del file con placeholder]
```
```

Usa `[PLACEHOLDER]` per i campi variabili. Mostra almeno un esempio compilato.

### 4. Operazioni

Per ogni operazione:

```
### `comando [argomenti]`

**Trigger:** [cosa fa scattare questa operazione — comando dell'utente o evento automatico]

**Passi:**
1. [passo 1 — cosa fa l'agente]
2. [passo 2 — cosa legge/scrive]
3. [passo 3 — cosa restituisce]

**Output:** [file creato/aggiornato, struttura dell'output]

**Esempio:**
> [dialogo utente → agente → risultato]
```

Ogni operazione deve avere un **trigger esplicito**. Nessuna azione senza comando.

### 5. Regole

```
## Regole

1. **[Regola 1]** — [cosa DEVE fare, in grassetto]. [spiegazione]
2. **[Regola 2]** — [cosa NON DEVE fare, in grassetto]. [spiegazione]
3. **[Regola 3]** — [regola operativa con dettaglio]. [spiegazione]
```

Minimo 5 regole. Devono coprire: principio etico, qualità dei dati, gestione errori, limiti operativi, modalità fallback.

### 6. Checklist di inizializzazione

```
## Checklist init

Quando l'utente esegue `[pat init]`, devi:

- [ ] [azione 1 — creare una directory]
- [ ] [azione 2 — creare un file con intestazione]
- [ ] [azione 3 — popolare struttura base]
- [ ] [azione 4 — stampare conferma]
```

### 7. Note filosofiche (2-3 righe)

```
## Note

[Una frase sulla natura del pattern. Perché esiste. Cosa cambia nel modo di lavorare.]

[Massimo 3 righe. Nessuna istruzione operativa.]
```

---

## Examples

```
examples/
└── wiki/           ← wiki popolato con dati realistici
    ├── index.md
    ├── log.md
    └── pages/
        └── example-page.md
```

- I dati devono essere realistici, non astratti
- Almeno 3-5 pagine di esempio
- Date coerenti tra loro
- Nomi, ID, riferimenti incrociati verosimili

---

## Convenzioni

| Elemento | Regola |
|----------|--------|
| Prefisso comandi | 2-4 lettere minuscole (es. `dj`, `ht`, `crm`) |
| Intestazione SCHEMA | `# Nome Pattern — SCHEMA` |
| Intestazione README | `# 🏷️ Nome Pattern` |
| Struttura directory | Mai più di 2 livelli di profondità |
| Formato date | ISO 8601: `YYYY-MM-DD` |
| ID progressivi | `PAT-001`, `PAT-002`, ... |
| Tag stato | `aperta`/`chiusa`, `attiva`/`in stallo` |
| Massima dimensione SCHEMA | 15 KB |

---

*Template mantenuto da [agent-patterns](https://github.com/AgtechDS/agent-patterns) · MIT*
