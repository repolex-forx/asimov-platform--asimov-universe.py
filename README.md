# Repolex Knowledge Graph of asimov-platform/asimov-universe.py

RDF knowledge graph data for [asimov-platform/asimov-universe.py](https://github.com/asimov-platform/asimov-universe.py), parsed by [repolex](https://repolex.ai).

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
lexq download asimov-platform/asimov-universe.py
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── blob
│   ├── 17e1e83dfd1d4b6d8d20e2837126e3021dc780b4.nq.gz
│   ├── 19a31b4dae4983cccd2cf67abb335c2b819b239b.nq.gz
│   ├── 19cc56b171e104f4ad50ca110bdf34f109aea7b9.nq.gz
│   ├── 21a01787ca0a0abaf7a195033c8b9779a238953b.nq.gz
│   ├── 2391f73aa051d3804285ce744f2e9a1c7e08993d.nq.gz
│   ├── 280f81f82f7ae0739f55ee66cd91d01651ae0245.nq.gz
│   ├── 6f83656972dcf4cdabab996bd49dde3986bc10be.nq.gz
│   ├── 825fe24c244c73eaa5f8acc2dd01fa8ddac88327.nq.gz
│   ├── 8b265cc167d538e85fcb9013e9488d98cd011ffe.nq.gz
│   ├── ac0e0fd0cc8395d2c24b639edd9a33ae35ed1596.nq.gz
│   ├── b2356fc1e346df3efa7bf4ed61c5411d5852b1a4.nq.gz
│   ├── bb67c988519445888ae76a7c7c4041de9dee75cf.nq.gz
│   ├── c32d29b038aca228c6527e02d6378d6d3f463bbb.nq.gz
│   ├── e3e57a8ce4ccbf74759a6df8fa4a3980ff1c9209.nq.gz
│   ├── efb98088164f5786b17e83ed384971fc3c74f93c.nq.gz
│   └── f7d08efa731bafe87b61018e6bc7016304458369.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── bdd31aa351d0902bcdbe2571bc1df64021440f36.nq.gz
└── tag
    └── tag.nq.gz

6 directories, 20 files
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

[asimov-platform/asimov-universe.py](https://github.com/asimov-platform/asimov-universe.py)

---
*Parsed on 2026-04-03 by [repolex](https://repolex.ai)*
