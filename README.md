# Repolex Knowledge Graph of tox-dev/toml-fmt-common

RDF knowledge graph data for [tox-dev/toml-fmt-common](https://github.com/tox-dev/toml-fmt-common), parsed by [repolex](https://repolex.ai).

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
rlex download tox-dev/toml-fmt-common
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 9647ac4da337e4b61ef728d252550a78faa19f7e
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 9647ac4da337e4b61ef728d252550a78faa19f7e
│           └── chunk-001.nq.gz
├── blob
│   ├── 123014908bebbfb7ecfa1d15daaceb272fabe05b.nq.gz
│   ├── 123ae508041b6ade5aea32d69a5577c9d511742a.nq.gz
│   ├── 2741f130d6266272594c327520e431f7725de0f7.nq.gz
│   ├── 2c28b78daf72ba2f923e3773b2c16284f76115a6.nq.gz
│   ├── 364982344fbd94d55705e1f27a9a87abaa255333.nq.gz
│   ├── 45f0ed7afccd6addc22cef1b1462bf19fa449a93.nq.gz
│   ├── 482e736a96a997f27ab6d5256302e60a661bc6fe.nq.gz
│   ├── 5968e5bcc55e7d0e43554bfb3203512e1e1fe0d0.nq.gz
│   ├── 5f89818f9e63c2f6829c7706c57f223cdb5bbd38.nq.gz
│   ├── 61676ceac719d5d49424d27b1256ea589d92282b.nq.gz
│   ├── aea841e9da29c023a7c7537f392635a2adfc32b6.nq.gz
│   ├── d47e4ccb5e16958a465a01ad2083d35bc865caf4.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── f140f8a8fe7761b2afb6d06d04e960392fb35124.nq.gz
│   └── f468e545d7edcfd8439d7dedfba65f58cef29082.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 9647ac4da337e4b61ef728d252550a78faa19f7e.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 22 files
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

[tox-dev/toml-fmt-common](https://github.com/tox-dev/toml-fmt-common)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
