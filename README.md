# Repolex Knowledge Graph of SergioBenitez/cookie-rs

RDF knowledge graph data for [SergioBenitez/cookie-rs](https://github.com/SergioBenitez/cookie-rs), parsed by [repolex](https://repolex.ai).

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
rlex download SergioBenitez/cookie-rs
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 1ec8fded5654679482a91c784e7ff2874b0fdeff
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 1ec8fded5654679482a91c784e7ff2874b0fdeff.nq.gz
│   └── repolex
│       └── 1ec8fded5654679482a91c784e7ff2874b0fdeff
│           └── chunk-001.nq.gz
├── blob
│   ├── 1a45eee7760d240bfa8ac1989088e0349169f264.nq.gz
│   ├── 29953103374fc2734bdf136de0a78df973759aa2.nq.gz
│   ├── 35ae347dff11d9972ce3fdbf760329fc0f0e8e95.nq.gz
│   ├── 3797fee154e61479b7e07a11e47bf3d129ca0e5d.nq.gz
│   ├── 4fffb2f89cbd8f2169ce9914bd16bd43785bb368.nq.gz
│   ├── 5cd49dc7e968cca184e517354ed6a20a2f9a9fc4.nq.gz
│   ├── 66f1ea2136797dd4797a14dc6ed1b9c4856777bc.nq.gz
│   ├── 7497003166ac8b855bb94c1f3791b90780b9bcde.nq.gz
│   ├── 7624e6b256b9cc09d5c999d9796ee210f271a2dc.nq.gz
│   ├── 7c49de955e1242147df3e193e801bfc9ac893990.nq.gz
│   ├── 7d5091ca789d6e62b9237dd95d523fbfaba32182.nq.gz
│   ├── 894d468eb7078e1932bb672f467df662e64a8482.nq.gz
│   ├── 89eaf9fbb2574b1c8d4d603211031954a9480146.nq.gz
│   ├── 8b62a933d8917b6db704583d9d9cb4f614cdd348.nq.gz
│   ├── 8caf86e5e93e6e17715ca97ecc557e6a5d620551.nq.gz
│   ├── 8d7e9d59c0bfdfaedb77e584dd0c79db22d6eb6e.nq.gz
│   ├── 9575b2e7de42766640bd10718c4a1b4c5540d3fe.nq.gz
│   ├── 9dbb732fb3df60b6a7a55085d1c871cf7ea72310.nq.gz
│   ├── c0913d655891b5dbe2fee23c4398c388a6713681.nq.gz
│   ├── d88f940f4aa3a81b2f093d5da2efa6c0d5418a72.nq.gz
│   ├── dee45b214624c594f70e7f5cc6fd72fad6c83574.nq.gz
│   ├── e2da4ffdf7d823501f57f1eeb3c4558be330e94f.nq.gz
│   ├── e625e81c90f1fad4809850eaec40d5858a6afa5a.nq.gz
│   ├── e832801a438a7ef119b676f687815e07c61b7764.nq.gz
│   ├── ea417054efad43d1d1223659f66e50a912ac2938.nq.gz
│   ├── f44cff5ede6c7915bd844611d85ecdaf4509b4b8.nq.gz
│   └── f666d2c3bc9e0a7335fa23e250caea928fa49e67.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 1ec8fded5654679482a91c784e7ff2874b0fdeff.nq.gz
├── filetree
│   └── 1ec8fded5654679482a91c784e7ff2874b0fdeff.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 37 files
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

[SergioBenitez/cookie-rs](https://github.com/SergioBenitez/cookie-rs)

---
*Parsed on 2026-11-22 by [repolex](https://repolex.ai)*
