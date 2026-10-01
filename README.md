# Repolex Knowledge Graph of block/xcode-index-mcp

RDF knowledge graph data for [block/xcode-index-mcp](https://github.com/block/xcode-index-mcp), parsed by [repolex](https://repolex.ai).

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
rlex download block/xcode-index-mcp
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── c89af82aee64c42690a60c2dda6d9e0f8bf022e9
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── c89af82aee64c42690a60c2dda6d9e0f8bf022e9.nq.gz
│   └── repolex
│       └── c89af82aee64c42690a60c2dda6d9e0f8bf022e9
│           └── chunk-001.nq.gz
├── blob
│   ├── 0023a5340637983755c8c19c18cc2c2bb1dbda1c.nq.gz
│   ├── 029519e08e72704356b39174fcddc39ce1684d6b.nq.gz
│   ├── 07f78a8b08af0e4e2826d0b3e784d527a95ef04b.nq.gz
│   ├── 0b84f85741cd749194fc6a29071cbf9e38fc230c.nq.gz
│   ├── 1bc469e68eb776aa52185c6cbfc5cdcaee837ce3.nq.gz
│   ├── 1c1b8962919ee7fd203acb3b26040980adfb70ef.nq.gz
│   ├── 3f13ed3ee77e056c3928afb3ebf4ad9e85944f20.nq.gz
│   ├── 42b147a93f855c383e891ce3a9b338c98c4a8cfc.nq.gz
│   ├── 468fed1e02ce7b9ce5042f0b8cd950b428c8aa75.nq.gz
│   ├── 53ab581447e04321652e1e70639842784c863795.nq.gz
│   ├── 5d5d12d88afaeaea2668e568059255d4d94037a6.nq.gz
│   ├── 6bccf43368fd7c96d9c659562a5142b8b8cb98a1.nq.gz
│   ├── 7130cab1e526df727b00322c9d3233bcc7c22f1a.nq.gz
│   ├── 8f43a22e5b5520e0cb3d02bd8d8300d4a0e8ff8b.nq.gz
│   ├── a0ee0d7aef02120c70cecee06b92c0f20b9700fb.nq.gz
│   ├── a4f37e4e3d4c7e01354464e14907ea042b0ba930.nq.gz
│   ├── b46b227bf3b44c3ec3ff84083d7e2471e30d005e.nq.gz
│   ├── bc79e2700c67f6b3e73c2046da01a56587ae9542.nq.gz
│   ├── c9b06e5e8226094811b2fe262f58f18a84c39930.nq.gz
│   ├── ce7342cebc7180103eba3c0baa7c3fb432582e76.nq.gz
│   ├── d6f64b98bb068c88fe2998b66d59b05bd912b093.nq.gz
│   ├── de459696437ff3bf549aabdb8c00e15b92bf9d8d.nq.gz
│   ├── e001dcc79bcc5aeead9434f5029614c32bd12a6c.nq.gz
│   ├── e3069c11ec1ff4f3770d478e1e87f2a57644f540.nq.gz
│   ├── e52200eff573965c65a2339d97269bdce6410384.nq.gz
│   ├── e707ef85ef2a0cd7cdd361a115367ffc4cc76f7b.nq.gz
│   ├── f8dd1f718b85e13458c15c5d75388fc36b2b31b0.nq.gz
│   └── fbc5bfe8e19e95ac3526b4ee5e12d2585991d3fc.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── c89af82aee64c42690a60c2dda6d9e0f8bf022e9.nq.gz
├── filetree
│   └── c89af82aee64c42690a60c2dda6d9e0f8bf022e9.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 38 files
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

[block/xcode-index-mcp](https://github.com/block/xcode-index-mcp)

---
*Parsed on 2026-10-01 by [repolex](https://repolex.ai)*
