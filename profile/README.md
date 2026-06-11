# Elixir Vibe

Elixir-native tooling for safer AI-assisted coding. Search and rewrite code by AST, detect duplication and generated-code slop, check architecture boundaries, and bootstrap strict `mix ci` quality gates — all with tools that understand Elixir syntax and BEAM projects.

Every package here is one building block of a larger thesis — a web stack
where AI-generated software can be *checked*, not just generated:
failures carry their location and cause, dependencies are traceable with
proof, and every check earns its place with a measured false-positive
rate. The full picture — manifesto, architecture, roadmap, and honest
uncertainties — lives in
**[Building Blocks for the Future Web](https://github.com/elixir-vibe/building-blocks)**.

```bash
mix igniter.install vibe_kit
mix ci
```

VibeKit is the quickest entry point: it wires Credo, Dialyzer, ExDNA, ExSlop, and Reach into new or existing Mix projects with one Igniter installer. The rest of the ecosystem is useful independently when you need deeper AST tooling, code-flow analysis, fixtures, or an experimental BEAM-native agent runtime.

## Start here

| Project | What it does | Hex |
| --- | --- | --- |
| [vibe_kit](https://github.com/elixir-vibe/vibe_kit) | Igniter installer for strict Elixir project quality checks: `mix ci`, Credo, Dialyzer, ExDNA, ExSlop, and Reach | [![Hex](https://img.shields.io/hexpm/v/vibe_kit.svg)](https://hex.pm/packages/vibe_kit) |

## Code intelligence and analysis

| Project | What it does | Hex |
| --- | --- | --- |
| [ex_ast](https://github.com/elixir-vibe/ex_ast) | AST-aware search, replace, and diffs for Elixir code | [![Hex](https://img.shields.io/hexpm/v/ex_ast.svg)](https://hex.pm/packages/ex_ast) |
| [reach](https://github.com/elixir-vibe/reach) | Program dependence graph, call-flow, data-flow, architecture checks, and smell detection for BEAM projects | [![Hex](https://img.shields.io/hexpm/v/reach.svg)](https://hex.pm/packages/reach) |
| [exograph](https://github.com/elixir-vibe/exograph) | Structural Elixir code intelligence and search powered by ExAST, Reach, Ecto, and Postgres/ParadeDB | [![Hex](https://img.shields.io/hexpm/v/exograph.svg)](https://hex.pm/packages/exograph) |

## Phoenix and LiveView tooling

| Project | What it does | Hex |
| --- | --- | --- |
| [phoenix_replay](https://github.com/elixir-vibe/phoenix_replay) | Session recording and replay for Phoenix LiveView | [![Hex](https://img.shields.io/hexpm/v/phoenix_replay.svg)](https://hex.pm/packages/phoenix_replay) |

## Quality and generated-code checks

| Project | What it does | Hex |
| --- | --- | --- |
| [ex_dna](https://github.com/elixir-vibe/ex_dna) | AST-aware duplicate-code detection with extraction candidates | [![Hex](https://img.shields.io/hexpm/v/ex_dna.svg)](https://hex.pm/packages/ex_dna) |
| [ex_slop](https://github.com/elixir-vibe/ex_slop) | Credo checks for common low-quality AI-generated Elixir patterns | [![Hex](https://img.shields.io/hexpm/v/ex_slop.svg)](https://hex.pm/packages/ex_slop) |
| [program_facts](https://github.com/elixir-vibe/program_facts) | Generate Elixir programs with known structural facts for analyzer testing | [![Hex](https://img.shields.io/hexpm/v/program_facts.svg)](https://hex.pm/packages/program_facts) |

## Experimental projects

| Project | What it does | Hex |
| --- | --- | --- |
| [vibe](https://github.com/elixir-vibe/vibe) | Experimental BEAM-native coding agent runtime with TUI, web UI, eval, tools, memory, and subagents | [![Hex](https://img.shields.io/hexpm/v/vibe.svg)](https://hex.pm/packages/vibe) |
| [theoria](https://github.com/elixir-vibe/theoria) | Elixir-native proof and specification kernel inspired by Lean's trusted-kernel architecture | [![Hex](https://img.shields.io/hexpm/v/theoria.svg)](https://hex.pm/packages/theoria) |
| [hex-playground](https://github.com/elixir-vibe/hex-playground) | Corpus playground for running local tools against popular Hex.pm packages | — |

## How it fits together

```text
Mix project
├── vibe_kit              — one-command quality setup and mix ci conventions
│   ├── credo             — general static analysis
│   ├── dialyxir          — Dialyzer integration
│   ├── ex_dna            — duplicate-code detection
│   ├── ex_slop           — generated-code slop checks
│   └── reach             — architecture and code-flow checks
├── ex_ast                — AST-aware search, replace, and diffs
├── exograph              — indexed structural code intelligence
├── program_facts         — analyzer fixtures with known facts
├── phoenix_replay        — session recording and replay for Phoenix LiveView
└── vibe                  — experimental BEAM-native agent runtime
```

## Why this exists

Agent-assisted Elixir development is safer when tools understand Elixir syntax, OTP runtime state, and project architecture instead of treating everything as plain text and shell output. Elixir Vibe packages keep analysis structured, outputs compact, checks cheap enough to run often, and BEAM-native workflows first-class.

The deeper argument — why these tools exist, how they compose with the
[Elixir Volt](https://github.com/elixir-volt) frontend stack and
[OpenPencil](https://github.com/open-pencil), and where it's all going —
is written up as a living standard:
[Building Blocks for the Future Web](https://github.com/elixir-vibe/building-blocks).
