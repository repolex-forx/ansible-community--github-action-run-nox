# Repolex Knowledge Graph of ansible-community/github-action-run-nox

RDF knowledge graph data for [ansible-community/github-action-run-nox](https://github.com/ansible-community/github-action-run-nox), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [rlex](https://github.com/repolex-ai/rlex) query tool:

```bash
cargo install --git https://github.com/repolex-ai/rlex
```

Verify the install:

```bash
rlex --help
```

**rlex is designed to be used primarily by LLMs in a terminal.** Start up your favorite AI assistant and ask it to use rlex. It handles the SPARQL — you just ask questions in plain English.

To load this repo's data:

```bash
rlex download ansible-community/github-action-run-nox
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── d67fa677ce308414356266dcbf022778a90e35cc
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── d67fa677ce308414356266dcbf022778a90e35cc
│           └── chunk-001.nq.gz
├── blob
│   ├── 012065c8539f2bd3e61eecc74acf5a046956de40.nq.gz
│   ├── 11abc010f9eea7478b1b58c5afb41b9c7f45a451.nq.gz
│   ├── 3e5c3b6807327242f5e927ec05c7186600b1550e.nq.gz
│   ├── 4663c0dc4a46469b37e41f312178939069290899.nq.gz
│   ├── 812e0a54a9226636356656612d4f5b7c2a08c095.nq.gz
│   ├── d43561594a143fd74787862a0e80ea5dbbe603f6.nq.gz
│   ├── ded70ecc18a6b7d1b2a17883aa9c512a5fd7af98.nq.gz
│   ├── f202516808cc58b77fea74cf64d410adafd22155.nq.gz
│   ├── f288702d2fa16d3cdf0035b15a9fcbc552cd88e7.nq.gz
│   └── f88a4657de504ee89bbaa717b7d8247acb019b3d.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── d67fa677ce308414356266dcbf022778a90e35cc.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 18 files
```

| Directory | What it contains |
|-----------|-----------------|
| `blob/` | Per-file AST graphs, content-addressed by git blob SHA. Each file in the source repo gets its own graph. |
| `aggregate/ast/` | Combined AST graph per parsed commit. Merges all blob graphs for a snapshot of the entire codebase at that point. |
| `aggregate/lsp/` | Language Server Protocol enrichment: resolved symbols, definitions, references, and type information. |
| `aggregate/dataflow/` | Interprocedural data flow edges between functions and modules. |
| `aggregate/repolex/` | Combined graph (AST + LSP + dataflow) per commit. |
| `commit/` | Git commit metadata (author, date, message, parent links). |
| `branch/` | Branch metadata. |
| `tag/` | Tag metadata. |
| `filetree/` | File tree snapshots per commit (which files existed and their blob SHAs). |
| `audit/` | Code architecture and graph audit reports per commit. |

## Source repository

[ansible-community/github-action-run-nox](https://github.com/ansible-community/github-action-run-nox)

---
*Parsed on 2026-11-06 by [repolex](https://repolex.ai)*
