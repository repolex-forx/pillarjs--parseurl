# Repolex Knowledge Graph of pillarjs/parseurl

RDF knowledge graph data for [pillarjs/parseurl](https://github.com/pillarjs/parseurl), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [lexq](https://github.com/repolex-ai/lexq) query tool using [uv](https://docs.astral.sh/uv/getting-started/installation/).

If you have uv installed, just copy/paste this into your terminal:

```bash
uv tool install git+https://github.com/repolex-ai/lexq
```

This installs lexq onto your system, in your user context. Verify the install:

```bash
lexq --help
```

**lexq is designed to be used primarily by LLMs in a terminal.** Start up your favorite LLM and ask it to use the lexq tool. It's that easy!

To load this repo's data:

```bash
lexq download pillarjs/parseurl
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 0022a009d0973a44ae3849e83112ea4d12ad5b49
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 0022a009d0973a44ae3849e83112ea4d12ad5b49.nq.gz
│   └── repolex
│       └── 0022a009d0973a44ae3849e83112ea4d12ad5b49
│           └── chunk-001.nq.gz
├── blob
│   ├── 061e6cdd4bb612eb87694f2410190c77726b2610.nq.gz
│   ├── 0fb9a0ef70151886358aa99bd0fe8b9389386d02.nq.gz
│   ├── 14908476db44e5c7afe3b925d92f267d413c904a.nq.gz
│   ├── 214dbd3b64279d3c31c57ef56bfdc2bdef84d818.nq.gz
│   ├── 222c64bf74f85c668105c28d71d27a8e67f89260.nq.gz
│   ├── 27653d3db7e584321691af8f1bc30d49fe105d3e.nq.gz
│   ├── 469f7812bea39a056a333ed92a19ec24581ce28e.nq.gz
│   ├── 4803393a92c27ea7d7eb2dd0642431bcfd6e2c84.nq.gz
│   ├── 603eabe12a799f38adcbcb68fad165a99ebe0b8d.nq.gz
│   ├── 61635f5d8f3c082852a045230a9fa14fe60787f0.nq.gz
│   ├── 62562b74a3b5a79e82ca417b02e0f597d85f5e2f.nq.gz
│   ├── 6e365dc90be964cee0e1b86ef5cff64c6586ab8c.nq.gz
│   ├── 7eeefc33b66c055f211388c46d17b50c45db7c25.nq.gz
│   ├── 8a39f3ab70642d6f173e45931f4e09691cd3f79d.nq.gz
│   ├── a5ccc51b0698f930634d6e0fb5d1ddac424d0d73.nq.gz
│   ├── b85e3a18e95ea4e0dbdb221061f693be43b7cb58.nq.gz
│   └── e3578aadfd3a97c6ef9d74f46e07314d775c9c61.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 0022a009d0973a44ae3849e83112ea4d12ad5b49.nq.gz
├── filetree
│   └── 0022a009d0973a44ae3849e83112ea4d12ad5b49.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 27 files
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

## Source repository

[pillarjs/parseurl](https://github.com/pillarjs/parseurl)

---
*Parsed on 2026-04-10 by [repolex](https://repolex.ai)*
