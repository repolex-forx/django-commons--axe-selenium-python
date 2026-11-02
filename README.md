# Repolex Knowledge Graph of django-commons/axe-selenium-python

RDF knowledge graph data for [django-commons/axe-selenium-python](https://github.com/django-commons/axe-selenium-python), parsed by [repolex](https://repolex.ai).

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
rlex download django-commons/axe-selenium-python
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 9b19cc5b7fd4c8099db5cf773e8d3d80ebb572ce
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 9b19cc5b7fd4c8099db5cf773e8d3d80ebb572ce
│           └── chunk-001.nq.gz
├── blob
│   ├── 1da178d5a9336d01401256ca2f0cc6a5fa5bf94e.nq.gz
│   ├── 2f66b0a03864cda0fd571c0fe3574ac140d57407.nq.gz
│   ├── 3175c0f74d2da6e9101199f2873bc7661f688446.nq.gz
│   ├── 35e00c24e4e49242f3ba838ea2627dfdf8362a5a.nq.gz
│   ├── 45a7717cd0a02c3ed014baf53ec62fdb191b994a.nq.gz
│   ├── 469ab827777041679452ca4fd3d96c4151f4acc7.nq.gz
│   ├── 5dfd42243d97969c3c65003b8231c8171f4f02c8.nq.gz
│   ├── 63c08e7b6b370d18476ca7af9309da1dbfd975cc.nq.gz
│   ├── 6fbe8159b2db12df85a3ecca3b73921192c6e43f.nq.gz
│   ├── 78bc391bcea361cb01c26e9a38bb0721dc3d3006.nq.gz
│   ├── 80c145e987ae0fc714ad290dfe5aeaa0f1aabfdb.nq.gz
│   ├── 85936aa703083805833a9a617ffa8f4a7f0d2bf3.nq.gz
│   ├── 8d0dcfd57f9407b4aea214e3f6b4a789f4f34695.nq.gz
│   ├── 9a24508b9baf84619fb0c847136b77d17ebe782d.nq.gz
│   ├── 9ec5616f0d83591b7e9dabcca5e771b7e1cc5e57.nq.gz
│   ├── a612ad9813b006ce81d1ee438dd784da99a54007.nq.gz
│   ├── b86eab32cfc4c1bd789fe3876d406a9409af8319.nq.gz
│   ├── c84498f3265279edf9432f5f8b7b56542f5586f4.nq.gz
│   ├── cc78e0403a53c8a45cba7a7fd59a7086d0d79b76.nq.gz
│   └── f36b4dbf71c4243588cb39a48db4ee33a8d0ab70.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 9b19cc5b7fd4c8099db5cf773e8d3d80ebb572ce.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 28 files
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

[django-commons/axe-selenium-python](https://github.com/django-commons/axe-selenium-python)

---
*Parsed on 2026-11-02 by [repolex](https://repolex.ai)*
