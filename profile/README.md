# Elixir Vibe

Elixir-native tooling for AI-assisted coding, AST analysis, code intelligence, quality checks, generated program facts, proof/spec experiments, and BEAM-native coding agents.

The core packages are useful independently. Vibe ties them together into an experimental agent runtime, but it is not the starting point for most users yet.

## Start here

| If you need... | Start with | What it does | Hex |
| --- | --- | --- | --- |
| AST-aware search, replace, and diffs | [ex_ast](https://github.com/elixir-vibe/ex_ast) | Match and rewrite Elixir syntax by AST pattern instead of regex | [![Hex](https://img.shields.io/hexpm/v/ex_ast.svg)](https://hex.pm/packages/ex_ast) |
| Architecture and code-flow analysis | [reach](https://github.com/elixir-vibe/reach) | Program dependence graph, call-flow, data-flow, architecture checks, and smell detection for BEAM projects | [![Hex](https://img.shields.io/hexpm/v/reach.svg)](https://hex.pm/packages/reach) |
| Duplicate-code detection | [ex_dna](https://github.com/elixir-vibe/ex_dna) | Find duplicated Elixir AST structures and extraction candidates | [![Hex](https://img.shields.io/hexpm/v/ex_dna.svg)](https://hex.pm/packages/ex_dna) |
| Credo checks for generated-code slop | [ex_slop](https://github.com/elixir-vibe/ex_slop) | Credo checks for common low-quality AI-generated Elixir patterns | [![Hex](https://img.shields.io/hexpm/v/ex_slop.svg)](https://hex.pm/packages/ex_slop) |

## Code intelligence and search

| Package | Domain | What it does | Hex |
| --- | --- | --- | --- |
| [ex_ast](https://github.com/elixir-vibe/ex_ast) | Elixir AST tooling | Search, replace, and diff Elixir code by AST pattern | [![Hex](https://img.shields.io/hexpm/v/ex_ast.svg)](https://hex.pm/packages/ex_ast) |
| [reach](https://github.com/elixir-vibe/reach) | Graph/code-flow analysis | Program dependence graph and architecture/code-flow analysis for BEAM projects | [![Hex](https://img.shields.io/hexpm/v/reach.svg)](https://hex.pm/packages/reach) |
| [exograph](https://github.com/elixir-vibe/exograph) | Indexed code intelligence | Structural Elixir code intelligence and search powered by ExAST, Reach, Ecto, and Postgres/ParadeDB | [![Hex](https://img.shields.io/hexpm/v/exograph.svg)](https://hex.pm/packages/exograph) |

## Quality and test-data packages

| Package | Domain | What it does | Hex |
| --- | --- | --- | --- |
| [ex_dna](https://github.com/elixir-vibe/ex_dna) | Duplication detection | Code duplication detector powered by Elixir AST analysis | [![Hex](https://img.shields.io/hexpm/v/ex_dna.svg)](https://hex.pm/packages/ex_dna) |
| [ex_slop](https://github.com/elixir-vibe/ex_slop) | Credo checks | Credo checks that catch AI-generated Elixir code slop | [![Hex](https://img.shields.io/hexpm/v/ex_slop.svg)](https://hex.pm/packages/ex_slop) |
| [program_facts](https://github.com/elixir-vibe/program_facts) | Analyzer fixtures | Generate Elixir programs with known structural facts for analyzer testing | [![Hex](https://img.shields.io/hexpm/v/program_facts.svg)](https://hex.pm/packages/program_facts) |

## Experimental and research projects

| Project | Domain | What it does | Hex |
| --- | --- | --- | --- |
| [vibe](https://github.com/elixir-vibe/vibe) | Experimental coding-agent runtime | BEAM-native coding agent for Elixir/OTP projects with TUI, web UI, eval, tools, memory, and subagents | [![Hex](https://img.shields.io/hexpm/v/vibe.svg)](https://hex.pm/packages/vibe) |
| [theoria](https://github.com/elixir-vibe/theoria) | Proof/spec kernel | Elixir-native proof and specification kernel inspired by Lean's trusted-kernel architecture | [![Hex](https://img.shields.io/hexpm/v/theoria.svg)](https://hex.pm/packages/theoria) |
| [hex-playground](https://github.com/elixir-vibe/hex-playground) | Corpus playground | Corpus playground for running local tools against popular Hex.pm packages | — |

## Package map

```text
Elixir Vibe packages
├── Code intelligence
│   ├── ex_ast          package: AST pattern search/replace/diff
│   ├── reach           package: graph, dependency, and architecture analysis
│   └── exograph        package: indexed code search over ExAST and Reach facts
├── Quality gates
│   ├── ex_dna          package: duplicate-code detection
│   ├── ex_slop         package: Credo checks for generated-code slop
│   └── program_facts   package: synthetic analyzer fixtures
└── Experimental / research
    ├── vibe            package: BEAM-native coding-agent runtime
    ├── theoria         package: proof/spec kernel experiments
    └── hex-playground  repository: package corpus for dogfooding tools
```

## Why this exists

Agent-assisted Elixir development is safer when tools understand Elixir syntax, OTP runtime state, and project architecture instead of treating everything as plain text and shell output. Elixir Vibe packages keep analysis structured, outputs compact, checks cheap enough to run often, and BEAM-native workflows first-class.
