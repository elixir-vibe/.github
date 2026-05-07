# Elixir Vibe

Elixir-native tooling for AI-assisted coding, AST analysis, structural code search, code quality, generated program facts, architecture analysis, and BEAM-native coding agents.

## Packages

| Package | Description | Hex |
|---------|-------------|-----|
| [ex_ast](https://github.com/elixir-vibe/ex_ast) | Search, replace, and diff Elixir code by AST pattern | [![Hex](https://img.shields.io/hexpm/v/ex_ast.svg)](https://hex.pm/packages/ex_ast) |
| [exograph](https://github.com/elixir-vibe/exograph) | Structural Elixir code intelligence and search powered by ExAST, Reach, Ecto, and Postgres/ParadeDB | — |
| [ex_dna](https://github.com/elixir-vibe/ex_dna) | Code duplication detector powered by Elixir AST analysis | [![Hex](https://img.shields.io/hexpm/v/ex_dna.svg)](https://hex.pm/packages/ex_dna) |
| [ex_slop](https://github.com/elixir-vibe/ex_slop) | Credo checks that catch AI-generated Elixir code slop | [![Hex](https://img.shields.io/hexpm/v/ex_slop.svg)](https://hex.pm/packages/ex_slop) |
| [program_facts](https://github.com/elixir-vibe/program_facts) | Generate Elixir programs with known structural facts for analyzer testing | [![Hex](https://img.shields.io/hexpm/v/program_facts.svg)](https://hex.pm/packages/program_facts) |
| [reach](https://github.com/elixir-vibe/reach) | Program dependence graph and architecture/code-flow analysis for BEAM projects | [![Hex](https://img.shields.io/hexpm/v/reach.svg)](https://hex.pm/packages/reach) |
| [exy](https://github.com/elixir-vibe/exy) | BEAM-native coding-agent substrate for Elixir/OTP projects | [![Hex](https://img.shields.io/hexpm/v/exy.svg)](https://hex.pm/packages/exy) |

## How it fits together

```txt
Elixir project
├── ex_ast          — AST-aware search, replace, and diff
├── exograph        — indexed code intelligence/search over ExAST and Reach facts
├── ex_dna          — duplication detection and extraction hints
├── ex_slop         — Credo checks for AI-generated code smells
├── program_facts   — synthetic programs with known facts for analyzer tests
├── reach           — control/data/call-flow and architecture analysis
└── exy             — BEAM-native coding-agent runtime
    ├── ex_ast      — syntax search and patching
    ├── exograph    — persisted structural/semantic code search
    ├── ex_dna      — duplicate detection and refactoring support
    ├── ex_slop     — slop detection
    └── reach       — architecture/code-flow analysis
```

## Philosophy

Elixir Vibe tools are built to make agent-assisted Elixir development safer:

- prefer AST-aware analysis over regex
- expose compact, structured outputs for agents
- dogfood the tools on themselves
- make code quality checks cheap enough to run frequently
- keep BEAM-native workflows first-class
