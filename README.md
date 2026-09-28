# Repolex Knowledge Graph of pytest-dev/apipkg

RDF knowledge graph data for [pytest-dev/apipkg](https://github.com/pytest-dev/apipkg), parsed by [repolex](https://repolex.ai).

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
rlex download pytest-dev/apipkg
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 9d3f894a53da084961aeb7e298c38f7d889b1cfc
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 9d3f894a53da084961aeb7e298c38f7d889b1cfc.nq.gz
│   └── repolex
│       └── 9d3f894a53da084961aeb7e298c38f7d889b1cfc
│           └── chunk-001.nq.gz
├── blob
│   ├── 0c3202387b19cbf21702b3a3ad287a79960ee858.nq.gz
│   ├── 151c0e9a2f1e60fe951e2bbd272e231e445c982c.nq.gz
│   ├── 6606cef8fae8fa2e60378b6c1cef2a7558e57ae0.nq.gz
│   ├── 672a52a66a20207614e53e6371a64b0ef1f513c8.nq.gz
│   ├── 67a907338ff359bd64abc6c0853b002b224f3cbb.nq.gz
│   ├── 6fbb667ab9f295b1aa70f3101380c2482bca304d.nq.gz
│   ├── 70f19cb5e446b0e37d9779fc899f06b51df968d5.nq.gz
│   ├── 71d3c2cb207dea7664d39a536ba0de09342e0466.nq.gz
│   ├── 77e47e802e5463a00dc5dce336ccfcd87b9d99e6.nq.gz
│   ├── 795c06bd9fee5706fb27bff1b92b8f53381659a1.nq.gz
│   ├── 7fe64e85d684e2566b1aa19ca9a851bd7871f60a.nq.gz
│   ├── 84451f52a42f9877f7ffb9173e1112c31ee2c71e.nq.gz
│   ├── 8534e25f60c1584ce1d4f0fe4e3475f2d46cd417.nq.gz
│   ├── 8dd399ab55bce8a4a1ddfd0c98170f771f6e5c35.nq.gz
│   ├── 91efda2e7da4ec68593d93c387182384dcdbeeb9.nq.gz
│   ├── b125751079484225b8e3b38b80c481ccf13e9422.nq.gz
│   ├── b573b8e36fb0c0008e6930a5c6fb33be13582967.nq.gz
│   ├── c439360e4977ee617bd61aef7e5ce0efca72d30d.nq.gz
│   ├── d828959a5d4f6a5e785eafc61e5dd9d78a0bad27.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── ea4587054e6dc0bb6977a385687f376ccc03cbe8.nq.gz
│   ├── efd65767f14a5cbf9fa58db5a23f92e93d965ce5.nq.gz
│   └── ff33b8f7ca0b1c05bb0bdc546aa760c8e78757be.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 9d3f894a53da084961aeb7e298c38f7d889b1cfc.nq.gz
├── filetree
│   └── 9d3f894a53da084961aeb7e298c38f7d889b1cfc.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 33 files
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

[pytest-dev/apipkg](https://github.com/pytest-dev/apipkg)

---
*Parsed on 2026-09-28 by [repolex](https://repolex.ai)*
