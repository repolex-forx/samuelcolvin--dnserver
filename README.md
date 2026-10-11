# Repolex Knowledge Graph of samuelcolvin/dnserver

RDF knowledge graph data for [samuelcolvin/dnserver](https://github.com/samuelcolvin/dnserver), parsed by [repolex](https://repolex.ai).

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
rlex download samuelcolvin/dnserver
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── a99dfe946103a3b45b9bf627902177fed97a41aa
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── a99dfe946103a3b45b9bf627902177fed97a41aa
│           └── chunk-001.nq.gz
├── blob
│   ├── 044f8d04dae02798c823fe00ac47ced89595a866.nq.gz
│   ├── 0ea43a0282c44b7daa620fc9431b66175372a5a2.nq.gz
│   ├── 289473bea2c8b58833d4fc7e72962ffd10792600.nq.gz
│   ├── 2d34789aadd1d7b77ec2c7b120d0a6d7a6f28703.nq.gz
│   ├── 373be4f8ecdd44904aea68b29596461c97046215.nq.gz
│   ├── 3bc9793fbe82826498ac41276895855b6fb3a004.nq.gz
│   ├── 3ebb0a3da06ec66c083fd2bda1d6937807f26395.nq.gz
│   ├── 4a5aba685ff855dab27d151b2fb88fd0ef7beb86.nq.gz
│   ├── 5052c1fd1fc6cf2582c5fbc352e4369956a59cad.nq.gz
│   ├── 73d78165486eb40d6663368cf98d1d243b67d811.nq.gz
│   ├── 75b746d9ffb07bc6ce20b1d4204cd07413bac950.nq.gz
│   ├── 79bbc32d610ab8c588cd3fb422965e8be0a825b0.nq.gz
│   ├── 7bee276dbd1d03f19fef10df686f73fca3ba6bcf.nq.gz
│   ├── 7f4106bae3fdd7d644b909a470b8c35b4a507334.nq.gz
│   ├── 840f852ee0f8019ce931127fcdfb43e854f72874.nq.gz
│   ├── 91cade71fa82b94ba81cb1969f4773ebc6b4edac.nq.gz
│   ├── 9d9332b179ff330fa4631c0c0d66ed71e8b08ace.nq.gz
│   ├── a9cf68a2e23fdb1ec45945c98bc3d0071452018e.nq.gz
│   ├── aa10af54d456df42caf49f7e96dfa0af4f2634b6.nq.gz
│   ├── c7f69d5bde968285a1c270b6d8d4c6e4e58307bd.nq.gz
│   ├── c803031cbbc2b1c1a34b1973da323fc71eb3ba8b.nq.gz
│   ├── d2caf65a2da0bdd0021f79fd984404e9a7c3abd4.nq.gz
│   ├── d9bf89d9416debf8283d95a176a9e5b58eb6f4a4.nq.gz
│   ├── dd7498749d9a90cb4007ebb447e6f90a12169abf.nq.gz
│   ├── e197f4a72fb643e555871a5dd2422bdc362d4e89.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── ed6b08356352de928ee2f0fbab62ab18b75939fa.nq.gz
│   └── f3d4686a9a3c20f5b090bad6fad7d91e5d6a1807.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── a99dfe946103a3b45b9bf627902177fed97a41aa.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 36 files
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

[samuelcolvin/dnserver](https://github.com/samuelcolvin/dnserver)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
