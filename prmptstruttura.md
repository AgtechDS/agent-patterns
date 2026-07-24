# 🏗️ Costruiamo la repo: `agent-patterns`

Parto subito. Creo la struttura completa della repository e il **primo pattern**. Ogni file è pronto per essere pushato su GitHub.

---

## Passo 1 — Struttura della repo + README manifesto


# ✅ Repo creata: **agent-patterns**

Ecco cosa hai in mano, Andres:

---

## 📁 Struttura finale

```
agent-patterns/
├── README.md                          ← Manifesto + catalogo (4.7 KB)
├── LICENSE                            ← MIT
├── .gitignore
├── examples/
└── patterns/
    ├── dev/
    │   ├── github-gardener/           ← ✅ PRONTO
    │   │   ├── README.md              (2.5 KB) - cos'è, perché, come si usa
    │   │   └── SCHEMA.md              (7.4 KB) - il file da incollare nell'agent
    │   ├── debug-diary/               ← 🔜
    │   ├── dotfiles-curator/          ← 🔜
    │   └── server-sentinel/           ← 🔜
    ├── knowledge/
    │   ├── llm-wiki/                  ← 🔜
    │   ├── study-companion/           ← 🔜
    │   └── reading-companion/         ← 🔜
    ├── life/
    │   ├── decision-journal/          ← 🔜
    │   ├── health-timeline/           ← 🔜
    │   ├── personal-crm/              ← 🔜
    │   ├── life-admin/                ← 🔜
    │   └── finance-narrator/          ← 🔜
    ├── work/
    │   ├── meeting-memory/            ← 🔜
    │   └── project-postmortem/        ← 🔜
    └── creative/
        └── world-bible/               ← 🔜
```

---

## 🌱 Il primo pattern: GitHub Gardener

**7 operazioni** pronte all'uso:

| Comando | Cosa fa |
|---|---|
| `garden init` | Crea `.garden/` e fa il primo snapshot della repo |
| `garden triage` | Analizza le issue: categorizza, segnala stale, suggerisce chiusure |
| `garden prune` | Trova branch morti, PR abbandonate, file orfani |
| `garden refresh` | Confronta README/CONTRIBUTING/CHANGELOG con la realtà |
| `garden audit` | Dipendenze outdated, vulnerabilità, licenze, CI |
| `garden report` | Report completo con Top 5 priorità |
| `garden log` | Storico di tutte le operazioni |

**Regola d'oro dello SCHEMA:** il Gardener **non tocca mai il codice**. Analizza, documenta, suggerisce. Le azioni distruttive (chiudere issue, cancellare branch) sono sempre **suggerimenti** che l'umano approva.

---

## 🚀 Per pubblicare su GitHub

```bash
cd agent-patterns
git init
git add .
git commit -m "Initial release: GitHub Gardener pattern + repo structure"
git branch -M main
git remote add origin https://github.com/TUO_USERNAME/agent-patterns.git
git push -u origin main
```

Poi aggiungi i **topic** nella repo: `llm`, `agent`, `patterns`, `markdown`, `productivity`, `developer-tools`

---

## ⏭️ Prossimo pattern?

La struttura è pronta. Le cartelle vuote aspettano. Dimmi quale costruiamo dopo:

| # | Pattern | Categoria | Dolore che risolve |
|---|---|---|---|
| 1 | **Debug Diary** | Dev | Risolvi lo stesso bug due volte perché hai dimenticato il fix |
| 2 | **Decision Journal** | Life | Dimentichi *perché* hai deciso, ripeti gli stessi bias |
| 3 | **Health Timeline** | Life | Info mediche sparse tra PDF, app e memoria |
| 4 | **Meeting Memory** | Work | 5 meeting al giorno, zero ricordo di chi ha deciso cosa |
| 5 | **World Bible** | Creative | Il personaggio ha gli occhi blu nel cap.3 e marroni nel cap.12 |
| 6 | **Finance Narrator** | Life | Hai i dati ma nessuno ti racconta la *storia* dei tuoi soldi |
| 7 | **Study Companion** | Knowledge | Studi, dimentichi l'80%, non colleghi i concetti |

**Quale, Andres?** Uno alla volta, li costruiamo tutti. 🛠️