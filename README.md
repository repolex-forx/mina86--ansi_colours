# Repolex Knowledge Graph of mina86/ansi_colours

RDF knowledge graph data for [mina86/ansi_colours](https://github.com/mina86/ansi_colours), parsed by [repolex](https://repolex.ai).

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
rlex download mina86/ansi_colours
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 84c64b3d560b51a15a9889f30ebb977815d3945e
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 84c64b3d560b51a15a9889f30ebb977815d3945e.nq.gz
│   └── repolex
│       └── 84c64b3d560b51a15a9889f30ebb977815d3945e
│           └── chunk-001.nq.gz
├── blob
│   ├── 014c59a5ea24c3a4a99a39bd83a5d8714aed7349.nq.gz
│   ├── 03d235600e1ca241f1c83e7e94d7594fe93b8a5f.nq.gz
│   ├── 096b9a94d3c50f28232e879f555575097b0249c9.nq.gz
│   ├── 0a041280bd00a9d068f503b8ee7ce35214bd24a1.nq.gz
│   ├── 28d05dfc1f45aecb72d39c5be5ac5b76745528e5.nq.gz
│   ├── 3e20ce9de8bae407a0817759d3e868e6e5bb079c.nq.gz
│   ├── 46f4db9637615a33f4d57151bdf5de7c92bc6319.nq.gz
│   ├── 4de5798c91c93a9a553b96e58870399bcd9a32e7.nq.gz
│   ├── 5ad17b1d4d9db122534c6834c324b00eebc822a2.nq.gz
│   ├── 8d15f7e370b48a1954765928c4a5dab29e60eb4a.nq.gz
│   ├── 99259fb27c37891a0e935d7f7d60959f11c4f27e.nq.gz
│   ├── 9a3753b4f644f75c6021f0e772118f3411a9a4cb.nq.gz
│   ├── bf479e08272eca695ea32106bedf6c9094264094.nq.gz
│   ├── c1163d8c1bd4c32b5e546ee6b838e91dd6f5f7cd.nq.gz
│   ├── c4f2fb3e0989e54bcfce19db36d6932cfb4a4a48.nq.gz
│   ├── d25c8cc7ff6b78d003c087d4ba4d75c5cc0770c0.nq.gz
│   ├── ecb8d0926fa1526e29dbd4d637f51d532ef2f6fa.nq.gz
│   └── f0f482375b28ae1c3c5ac281208a5b7219acf13e.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 84c64b3d560b51a15a9889f30ebb977815d3945e.nq.gz
├── filetree
│   └── 84c64b3d560b51a15a9889f30ebb977815d3945e.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 28 files
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

[mina86/ansi_colours](https://github.com/mina86/ansi_colours)

---
*Parsed on 2026-11-22 by [repolex](https://repolex.ai)*
