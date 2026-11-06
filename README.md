# Repolex Knowledge Graph of google-deepmind/dmvr

RDF knowledge graph data for [google-deepmind/dmvr](https://github.com/google-deepmind/dmvr), parsed by [repolex](https://repolex.ai).

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
rlex download google-deepmind/dmvr
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 77ccedaa084d29239eaeafddb0b2e83843b613a1
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 77ccedaa084d29239eaeafddb0b2e83843b613a1
│           └── chunk-001.nq.gz
├── blob
│   ├── 00105e39ea2574b5f42aae419524f923afdb17f1.nq.gz
│   ├── 0aa277ef2da75744391721961a3761c4726d55f5.nq.gz
│   ├── 162c5dd85f20c57620bcdbbc32734f6946d49aeb.nq.gz
│   ├── 16bcaeb409f05834510841a2d1209ea50c97bd1c.nq.gz
│   ├── 2751a9ce14f04f8bdae5f5140fa9ce8c725e6c50.nq.gz
│   ├── 33e52333a8942b2c9f06fed346cb51e647eb96bb.nq.gz
│   ├── 3806e3166cc01df5b845d326f5d89b2572a269c1.nq.gz
│   ├── 4a8011b370a497504a3ea2195749c8de2382323d.nq.gz
│   ├── 56804caa37ae2b4f543a8f4de2db853077fda98e.nq.gz
│   ├── 6402fcecacc8df9950325afc2c475577a89d996c.nq.gz
│   ├── 6ffe390be15e0f8d1dfa7822d1df72f93ccb7d5c.nq.gz
│   ├── 73c63d16091a20b2e7dc6c0991041a2a3b9f879d.nq.gz
│   ├── 7b17ba58e9eb821580fe8fa5211ab1ed7cd6c78a.nq.gz
│   ├── 7f2ccfe707382b48f497a5d39659f9c997395219.nq.gz
│   ├── 7fee0743880c92fc971c4bce2da3dff0d5941442.nq.gz
│   ├── 893221c0ec565cb073fd2b235e91dc20d9640ba9.nq.gz
│   ├── a074f38807657943c2053978a18862543215a93e.nq.gz
│   ├── bf62b323f7e0c9fc2f678a4efcd81c6246df0eee.nq.gz
│   ├── c655a59aa6d8cfbd5ebef2bddbbd82647b185244.nq.gz
│   ├── c76efcafd337c3c84ddce8be34964a73121f2cac.nq.gz
│   ├── cdabf070cce57fa28e367b5608a12d43ffd25edf.nq.gz
│   ├── d645695673349e3947e8e5ae42332d0ac3164cd7.nq.gz
│   ├── e270722a8c7f60b981174affc1e4a1d5340b64d8.nq.gz
│   ├── e5c3b2868437f65d0d14f0411e9c2482bef576bf.nq.gz
│   ├── e86566802dd0850ee405f67d788cfbca69faa378.nq.gz
│   ├── e9e28cb2068daf1cefe64ec885ce154d7d87dd11.nq.gz
│   ├── eb31e81e067cc852ccc58f60e59f941a4dcf968c.nq.gz
│   ├── ebaaa54b421448ce352c1ad2c749c9408304ebad.nq.gz
│   ├── f183ac97e96213169c1f7e8e461f0249da2fb38f.nq.gz
│   ├── f836a09aa1baedd3842e8d4445cc93157158a78a.nq.gz
│   └── fed580cc0f9678f5c5846f7bba61687ef6ea252d.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 77ccedaa084d29239eaeafddb0b2e83843b613a1.nq.gz
├── issue
│   └── issue.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 38 files
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

[google-deepmind/dmvr](https://github.com/google-deepmind/dmvr)

---
*Parsed on 2026-11-06 by [repolex](https://repolex.ai)*
