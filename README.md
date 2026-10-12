# Repolex Knowledge Graph of simonw/datasette-auth-tokens

RDF knowledge graph data for [simonw/datasette-auth-tokens](https://github.com/simonw/datasette-auth-tokens), parsed by [repolex](https://repolex.ai).

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
rlex download simonw/datasette-auth-tokens
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 198f3af83615526522c12dfeed2ebb8dc8660ea9
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 198f3af83615526522c12dfeed2ebb8dc8660ea9
│           └── chunk-001.nq.gz
├── blob
│   ├── 0564f0c6f458d32294b4f6f8f3168f08485e2e31.nq.gz
│   ├── 0c002e2d41cdebe403dc91ef3d667ec19dafcef7.nq.gz
│   ├── 2483ebcb8da96e8d69ba3db2495830651e0902ee.nq.gz
│   ├── 261eeb9e9f8b2b4b0d119366dda99c6fd7d35c64.nq.gz
│   ├── 266dbe241ab812bcd05b495b638fd6a89895fe15.nq.gz
│   ├── 69df63bdbbb435e3f103b8855088b315b5c8735b.nq.gz
│   ├── 767998208057a9339965a8e4df727cf8f2538736.nq.gz
│   ├── 9d1f26915c164e749101f799f619e233d34b8e9c.nq.gz
│   ├── a32cf26e3c23c8627a87e094fe7453317896e2dc.nq.gz
│   ├── af4e1a0d1c96f0a840e80b50555a5ba46bef6d1f.nq.gz
│   ├── aff2b7a503264c693db5d8e12c5c69ccb41edff5.nq.gz
│   ├── cffc4ae1fa80e8c540e600326074800b183bfd99.nq.gz
│   └── feeb143dfd817fcf8429b988be8ad59e9bfe0467.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 198f3af83615526522c12dfeed2ebb8dc8660ea9.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 21 files
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

[simonw/datasette-auth-tokens](https://github.com/simonw/datasette-auth-tokens)

---
*Parsed on 2026-10-12 by [repolex](https://repolex.ai)*
