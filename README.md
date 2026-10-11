# Repolex Knowledge Graph of agronholm/sphinx-autodoc-typehints

RDF knowledge graph data for [agronholm/sphinx-autodoc-typehints](https://github.com/agronholm/sphinx-autodoc-typehints), parsed by [repolex](https://repolex.ai).

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
rlex download agronholm/sphinx-autodoc-typehints
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── af98022c1ec2c73bc5cf1c95ca88cec9cbcc1499
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── af98022c1ec2c73bc5cf1c95ca88cec9cbcc1499
│           └── chunk-001.nq.gz
├── blob
│   ├── 00b2d61e499a882c03ebec38653345dd97667df7.nq.gz
│   ├── 09bd6a0b7e0926e338f50aaec1ac9f3b50a7162f.nq.gz
│   ├── 0e748bdc38bf17b4cbbcc4bbe6d34fb4bed3fdad.nq.gz
│   ├── 123014908bebbfb7ecfa1d15daaceb272fabe05b.nq.gz
│   ├── 14a5de119a31916bc505d0afd0f10c865ef7a9f5.nq.gz
│   ├── 1e1b3ee59df9509d4693329b121b0838562d2925.nq.gz
│   ├── 2e7a204e3082f2c75e56b7ac9c0e18d709d1c554.nq.gz
│   ├── 2ffac0b20e380bf3cd1da8dbcfc640adbee530f5.nq.gz
│   ├── 324647a7d247f0e79bfef2f3ca7f8127984693c0.nq.gz
│   ├── 35f43c1c0addbb5ca2658ee1dd7af03053e5219f.nq.gz
│   ├── 36347075581bfc15fe8f52c4ece80a0deb20ec18.nq.gz
│   ├── 373a444cec7b34db31793067a9e47e40372eeaf1.nq.gz
│   ├── 378e079509d568c7b6a9db76088c3112cb799658.nq.gz
│   ├── 3c820613e66831aaff86c8b3aa0f5e4c21490a38.nq.gz
│   ├── 3d774cb8e3cb774437219e34ff712297faabf369.nq.gz
│   ├── 3f10b4dcc3f517a84a1c602dda1c152329e7dcc4.nq.gz
│   ├── 400c748ad0a5a31431b1ddbb522d775a47a19971.nq.gz
│   ├── 43964e24cc6cc85019c6fa7cacbe8ad77e4c17ec.nq.gz
│   ├── 4cc6e96c026824e6caf78b3e7b586dc8bd3a0cf8.nq.gz
│   ├── 50fc91bc7a723d8ac17b6acb01e66b1c06c43373.nq.gz
│   ├── 5cc16cb18fdb6c24aced2eac041fb0f2f66d202e.nq.gz
│   ├── 65d35a897692141d5caf76f6096292c26670bb64.nq.gz
│   ├── 6d7e91ef654029a20e23887f5c31e8d60d0e0b81.nq.gz
│   ├── 70d092a9408feb06214c25e1372a64bfcf0aa99b.nq.gz
│   ├── 77afa93d6febbc59909cea71401c4e3bd23ec124.nq.gz
│   ├── 8ca987a0dc514548aa4e9539a88fe5773600d28d.nq.gz
│   ├── ace460916e5131b47d8066c231869700cbd9d35c.nq.gz
│   ├── b1e457b2ee3c6c451c7acf379d2ec9c570bcc945.nq.gz
│   ├── bb939ea467cf382834183c9887e8a5cd6cb2bee4.nq.gz
│   ├── c4a033bbbf628606fc9cdd3248afdef71771a20b.nq.gz
│   ├── d6f8ed8097adce91d4da7726fe07a4882631c48c.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── f30749b7b12bf6545aeb3c51494d2919470f5db4.nq.gz
│   ├── f92eae8195d16da097eaccf6e130bcffd8eb340e.nq.gz
│   └── fe120ad7549545f89368d634311400dd7c83477f.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── af98022c1ec2c73bc5cf1c95ca88cec9cbcc1499.nq.gz
└── tag
    └── tag.nq.gz

11 directories, 41 files
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

[agronholm/sphinx-autodoc-typehints](https://github.com/agronholm/sphinx-autodoc-typehints)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
