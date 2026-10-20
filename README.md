# Repolex Knowledge Graph of jaraco/svg.charts

RDF knowledge graph data for [jaraco/svg.charts](https://github.com/jaraco/svg.charts), parsed by [repolex](https://repolex.ai).

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
rlex download jaraco/svg.charts
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 9032cb1a993560acd40d17e6d284f7a319f47508
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 9032cb1a993560acd40d17e6d284f7a319f47508
│           └── chunk-001.nq.gz
├── blob
│   ├── 10d412f406891b9683f832fcbc134c9bdf4f916e.nq.gz
│   ├── 1f2aa7533b0423a8eb943f6f4ec02498e39581a0.nq.gz
│   ├── 240329c3604d8ead4c10aa8c88352caa8e4ce7b2.nq.gz
│   ├── 281fdad8bd74eb35f908b251c01cd2bab7ff0f07.nq.gz
│   ├── 2c0dfabcfb7243ef9eabfcabb8946e97d82ca7a4.nq.gz
│   ├── 2e3f4dd791a6372b427d618eb0baa8c4dc58e5f0.nq.gz
│   ├── 304196f81e11a168c9894f966e4a617ebf4ed53c.nq.gz
│   ├── 321c636947732ba0f615269a980a0ab227c99412.nq.gz
│   ├── 335e093fbcdde98a3caa5f950d449b0055bca556.nq.gz
│   ├── 43580675c1fa2850a910452263c78389cc4464f3.nq.gz
│   ├── 466981c11d7686b487cb80e7b0afeea798a57f28.nq.gz
│   ├── 4c83ab5a03b5d64cb3aec9af5a63f688f7e89d7b.nq.gz
│   ├── 54c9000ec94341dd65c2053251b85b124017b9b5.nq.gz
│   ├── 54cc8303b22089e12053e552d4e6cb852a865b8a.nq.gz
│   ├── 577e87a793a20e413f7321f4f17ec1eba2ea1962.nq.gz
│   ├── 5bdc232005af9be104a00437ae9bc64417a4c1cc.nq.gz
│   ├── 700235be57c1b2872455c0be5333f59cf568e252.nq.gz
│   ├── 724370638fc188317bbc7dc868f1a571995fd796.nq.gz
│   ├── 73e9494404d318389afa3808ae194023de3e3a79.nq.gz
│   ├── 7b806e5b75df1d101038853e3d37975b70630084.nq.gz
│   ├── 844a1140c73c118e34eb313de537792d0d586005.nq.gz
│   ├── 856672c694411eb798547d0b02ec9a1ae1b1c0dc.nq.gz
│   ├── 88c397a02d39ec008e0e76a7981657d020f485e2.nq.gz
│   ├── 8a47228717a2d41da322f30a6c8e4b3b755ea409.nq.gz
│   ├── 96f9335685fd928344187d7ff8fe0185ae5747fe.nq.gz
│   ├── 9a0f3bce1395ae3819030b822e5d9076c85068ea.nq.gz
│   ├── 9a9cb1f996445472cd8beb075799a36e073304d3.nq.gz
│   ├── a28bcddd5c6310bc7924cb8bb93dd3ddc4ca515e.nq.gz
│   ├── b918af1e4924a04ac1f0a8b1cbcbf3d85be7f698.nq.gz
│   ├── c592b25d29a438f6fb43bd9c9689192721385b2b.nq.gz
│   ├── c9a33908f081b2f4660770ee3b26f768b84ee586.nq.gz
│   ├── d1f679c2b703e2b6af62a73603112871e092171c.nq.gz
│   ├── e00090451a68d59e6897e133702a9fd63ad19cee.nq.gz
│   ├── e05a3d4a2ab888e32952006d8cd380864368db5f.nq.gz
│   ├── e3e4e975e2df7c630a27005d15379b8e4ea9027d.nq.gz
│   ├── efcb8cbc2043faa7caf4f92fc7488bd6914c934c.nq.gz
│   ├── f8f796c77a1a0613046afa8dd25cfa2165cc3098.nq.gz
│   ├── fd487e40e7cfa124c79e8e25475b810ec4d90ea4.nq.gz
│   └── ffdc5301fe590b6bbbb36c3e3dd0414b4977b1e6.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 9032cb1a993560acd40d17e6d284f7a319f47508.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 47 files
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

[jaraco/svg.charts](https://github.com/jaraco/svg.charts)

---
*Parsed on 2026-10-20 by [repolex](https://repolex.ai)*
