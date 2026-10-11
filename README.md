# Repolex Knowledge Graph of python-hyper/hyperlink

RDF knowledge graph data for [python-hyper/hyperlink](https://github.com/python-hyper/hyperlink), parsed by [repolex](https://repolex.ai).

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
rlex download python-hyper/hyperlink
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 978f2e645578aad856fe5e03e2e2c017c8c0f7ca
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 978f2e645578aad856fe5e03e2e2c017c8c0f7ca
│           └── chunk-001.nq.gz
├── blob
│   ├── 017f9eb88c1a8404ceeeae8d1a79db7c91be1881.nq.gz
│   ├── 09b22da24c4c8c3faf517ac4276723147c7d2ba9.nq.gz
│   ├── 0fa9da0bc455cfb258805fe9ca71dd803a1c3ec0.nq.gz
│   ├── 19f589e551abddc1d73b964f157e53167dd1f2d8.nq.gz
│   ├── 2165a8353ba3e4004bf34fc4b811e1f69dfc9dbd.nq.gz
│   ├── 35230642121fb0288f7d4f61855944b6cf25ec78.nq.gz
│   ├── 37c917260953bcf902fceec399df83365cd93b78.nq.gz
│   ├── 3988cc8ff7bdb668177ae7cf19494340252dcc45.nq.gz
│   ├── 3bcf89706df720937a132ab442c3196a44ed344f.nq.gz
│   ├── 48452579d7804529095f78378bf6e5cd62445270.nq.gz
│   ├── 48e9f06742fa3431a433f15157658315108bceb9.nq.gz
│   ├── 4ab987eb5d9f379e2b44f4f41ad69d63689db58b.nq.gz
│   ├── 50f34c6a55509df26eb259ad9ea5cd43d6b69807.nq.gz
│   ├── 5869a052a41273e557900a74642b117d7c7b08e2.nq.gz
│   ├── 5e4090017a9bec5de60a745d17007a9e95f31a43.nq.gz
│   ├── 5f83d45bb1968fd51ba6bf7eed1d937db980269a.nq.gz
│   ├── 6326cf459bb81fcc70988baa15baa58952e1dd2a.nq.gz
│   ├── 6665f7137d92282e55d6e37964ca979da91de9d6.nq.gz
│   ├── 66b0270915b482d79f033d93b10eada24fda9d77.nq.gz
│   ├── 776ed7b71b413ebc283a3e64ec26112fa8ea92ad.nq.gz
│   ├── 8797b5cc36c63859a919b41cdf8b595309be3040.nq.gz
│   ├── 93b5c7989408fb26d8a4a05a73f5ad8236e746cb.nq.gz
│   ├── 93ebb782b635e1a08935f5ac30e652b0bd029b34.nq.gz
│   ├── a73f882ffb0354aa6d5d80d175a8dbb0edcafe0c.nq.gz
│   ├── ad3bd04a3e9447f407f5014ef2c29d8c217f7777.nq.gz
│   ├── b173d25d46667aba75a5ebe034816a0181442501.nq.gz
│   ├── b43c91e34434fa7f637bed2024229288f9839fb9.nq.gz
│   ├── b5b7e9ebc822bfe6c4531bb472e3ccfc4af54e24.nq.gz
│   ├── c7166536bacbc42286d612424781c98eeff0963a.nq.gz
│   ├── cfc0c47d16903239c95f449d21d30f0893070d27.nq.gz
│   ├── d2dfd5e49152ea42b697a4647ba9c5b56a53639b.nq.gz
│   ├── dc5e5bb86069511732645403685455947bbaebd9.nq.gz
│   ├── e10ca70f78fe592bf4f6f4a397ea30e7b52c8e91.nq.gz
│   ├── e7efe6aeb924b1ac56348e121f62dbc3761ec7dc.nq.gz
│   ├── f057fb8a9802aec18edca64375812434e62c19de.nq.gz
│   ├── f5d2fddaa13dfa2062df4a9740761dd7cda74e5d.nq.gz
│   ├── f680b01a90534f877e53142923d077b0dfb2367e.nq.gz
│   └── f8a4fb983c4f17714719d52e9f476a3daa727a7e.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 978f2e645578aad856fe5e03e2e2c017c8c0f7ca.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 46 files
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

[python-hyper/hyperlink](https://github.com/python-hyper/hyperlink)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
