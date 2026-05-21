# Elixir Vibe

Elixir-native tooling for AI-assisted coding, AST analysis, code intelligence, quality checks, generated program facts, proof/spec experiments, and BEAM-native coding agents.

```bash
mix escript.install hex vibe
vibe
```

Vibe is the agent runtime for the stack: a terminal/web coding agent that uses Elixir APIs, local SQLite state, OTP supervision, AST tooling, code-flow analysis, plugins, memory, and subagents instead of a large pile of one-off external tools.

## Start here

| Project | What it does | Hex |
| --- | --- | --- |
| [vibe](https://github.com/elixir-vibe/vibe) | BEAM-native coding agent for Elixir/OTP projects with TUI, web UI, eval, tools, memory, and subagents | [![Hex](https://img.shields.io/hexpm/v/vibe.svg)](https://hex.pm/packages/vibe) |

## Code intelligence packages

| Project | What it does | Hex |
| --- | --- | --- |
| [ex_ast](https://github.com/elixir-vibe/ex_ast) | Search, replace, and diff Elixir code by AST pattern | [![Hex](https://img.shields.io/hexpm/v/ex_ast.svg)](https://hex.pm/packages/ex_ast) |
| [reach](https://github.com/elixir-vibe/reach) | Program dependence graph and architecture/code-flow analysis for BEAM projects | [![Hex](https://img.shields.io/hexpm/v/reach.svg)](https://hex.pm/packages/reach) |
| [exograph](https://github.com/elixir-vibe/exograph) | Structural Elixir code intelligence and search powered by ExAST, Reach, Ecto, and Postgres/ParadeDB | [![Hex](https://img.shields.io/hexpm/v/exograph.svg)](https://hex.pm/packages/exograph) |

## Quality and test-data packages

| Project | What it does | Hex |
| --- | --- | --- |
| [ex_dna](https://github.com/elixir-vibe/ex_dna) | Code duplication detector powered by Elixir AST analysis | [![Hex](https://img.shields.io/hexpm/v/ex_dna.svg)](https://hex.pm/packages/ex_dna) |
| [ex_slop](https://github.com/elixir-vibe/ex_slop) | Credo checks that catch AI-generated Elixir code slop | [![Hex](https://img.shields.io/hexpm/v/ex_slop.svg)](https://hex.pm/packages/ex_slop) |
| [program_facts](https://github.com/elixir-vibe/program_facts) | Generate Elixir programs with known structural facts for analyzer testing | [![Hex](https://img.shields.io/hexpm/v/program_facts.svg)](https://hex.pm/packages/program_facts) |

## Research and playgrounds

| Project | What it does | Hex |
| --- | --- | --- |
| [theoria](https://github.com/elixir-vibe/theoria) | Elixir-native proof and specification kernel inspired by Lean's trusted-kernel architecture | [![Hex](https://img.shields.io/hexpm/v/theoria.svg)](https://hex.pm/packages/theoria) |
| [hex-playground](https://github.com/elixir-vibe/hex-playground) | Corpus playground for running local tools against popular Hex.pm packages | — |

## How it fits together

```text
Elixir project
├── vibe                  — BEAM-native coding agent runtime
│   ├── ex_ast            — AST-aware search, replace, and diff
│   ├── reach             — control/data/call-flow and architecture analysis
│   ├── exograph          — persisted structural code search
│   ├── ex_dna            — duplicate detection and extraction hints
│   └── ex_slop           — Credo checks for generated-code slop
├── code intelligence
│   ├── ex_ast            — syntax-aware transformations
│   ├── reach             — graph and dependency analysis
│   └── exograph          — indexed search over code facts
├── quality gates
│   ├── ex_dna            — duplication detection
│   ├── ex_slop           — AI slop checks
│   └── program_facts     — analyzer fixture generation
└── research
    ├── theoria           — proof/spec kernel experiments
    └── hex-playground    — package corpus for tool dogfooding
```

## Why this exists

Agent-assisted Elixir development is safer when tools understand Elixir syntax, OTP runtime state, and project architecture instead of treating everything as plain text and shell output. Elixir Vibe packages keep analysis structured, outputs compact, checks cheap enough to run often, and BEAM-native workflows first-class.
