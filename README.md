# Repolex Knowledge Graph of kivy/audiostream

RDF knowledge graph data for [kivy/audiostream](https://github.com/kivy/audiostream), parsed by [repolex](https://repolex.ai).

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
rlex download kivy/audiostream
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 69f6b100f1ea4e3982a1acf6bbb0804e31a2cd50
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 69f6b100f1ea4e3982a1acf6bbb0804e31a2cd50
│           └── chunk-001.nq.gz
├── blob
│   ├── 031be1f626cffc95aeb465a4b943305f1f918b0d.nq.gz
│   ├── 099659b921de2f6cdfef2ee103a1b141ab439ec8.nq.gz
│   ├── 0da150b199ae5bd7150a8e0d5a128f66258f8846.nq.gz
│   ├── 1ae992e1d0e51581ba3de47d2e45b7b0512c3d3b.nq.gz
│   ├── 23e409fc74b410c4b9708dbc789f37959c769825.nq.gz
│   ├── 2693b6a6cfc464ae502e36ae057cea0748e3e9ea.nq.gz
│   ├── 2d71a4e2e87527e06744ce9aa0edb02b9ec5f16b.nq.gz
│   ├── 373a95ff398b1f6810bdefc15aebb40628b98e4c.nq.gz
│   ├── 379c10a98d8d1af188c5a5427c576f532590d8e9.nq.gz
│   ├── 38372673746e618adb7e3f01400709ebb37a4fa2.nq.gz
│   ├── 3e6b4fead8f29c47899fd7615703f6a0983b3ffb.nq.gz
│   ├── 4313b4c42eb67127c3647722eaec60160a658dda.nq.gz
│   ├── 629f5f723fa5282ec810ae73ba0280555008036d.nq.gz
│   ├── 653c8880ef7558d9d49450578f9573101e5a3060.nq.gz
│   ├── 67a401a2991e38cb80b04fe6b9d9099bc006307b.nq.gz
│   ├── 67fce54f5f7cfc35612ca14eb4a635a61d78747e.nq.gz
│   ├── 716bfc0fceab7967001f3dbe82726510a019969d.nq.gz
│   ├── 74aceebcb02097f9ab9d2153e5cdd36ced96629c.nq.gz
│   ├── 8fd3a4d01002f09207d5dff2c93a6f0b20612acd.nq.gz
│   ├── 9c1396d1207a30e6fec06cc7059b1f5e156f5696.nq.gz
│   ├── 9c93dc2b2bb3fa810d5e16cc32bf322edfc811ec.nq.gz
│   ├── 9d7c19684ce2f67000ac2e74c0f7c0094e7afcf7.nq.gz
│   ├── 9de815e1b5d29a7927ce0d5cfce215da86670de9.nq.gz
│   ├── a027b5fa5dfff0b43bcc4af62e47d48066070bd5.nq.gz
│   ├── a76d65c9f16376ad533582d83553d9f23b8316cd.nq.gz
│   ├── b443007a02b604eba25eb9419132722ee94fff6f.nq.gz
│   ├── be306ea8431ff98ef9b6edeb7697e926a2fba049.nq.gz
│   ├── c2e28a11942ad8661558296026f4b151bb0d1dc1.nq.gz
│   ├── c631806c1a33fef0f274e937d0f6cd8a68464776.nq.gz
│   ├── c8578415e9bd80d6871d4a840fcf66c561a53b2a.nq.gz
│   ├── ca87ce4e34faa7f5edfe0cd6ab3b3dd27edbc340.nq.gz
│   ├── cfbf9910237238fd8c8f44a67403ab261be1ff92.nq.gz
│   ├── d2db0298a87e1b07c420ee20292a0e2924d5c499.nq.gz
│   ├── d5d6b13c8523290257544a9fc3b75abf911b367d.nq.gz
│   ├── d6ffcc0d06e4960b54693d63a4672d5ab8e60fe3.nq.gz
│   ├── d96f7cdf4b64434ce91e91624c61f1535ebc8136.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── f06f6162333d9b2b3f86673341a4704d3211d364.nq.gz
│   ├── f80f60761beaa13a3801ab6fecd53c757cf11286.nq.gz
│   └── f857498e472d3c05508b1d56b32143d5134343b3.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 69f6b100f1ea4e3982a1acf6bbb0804e31a2cd50.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 48 files
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

[kivy/audiostream](https://github.com/kivy/audiostream)

---
*Parsed on 2026-11-07 by [repolex](https://repolex.ai)*
