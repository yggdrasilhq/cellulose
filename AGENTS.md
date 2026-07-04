# AGENTS.md

## Mission

Build Cellulose: an open source spreadsheet and financial modeling workspace
with compatibility discipline, YggUI-grade automation, and a clear path from
human editing to agent-driven workflows.

## Local Repository Relationships

- `../yggterm` is the first intended host integration.
- `../paper` is a sibling YggUI app; shared app-control, proof, and design ideas
  should stay reusable instead of spreadsheet-specific when they are generic.

## Engineering Constraints

- Keep implementation boundaries explicit: workbook model, UI, commands,
  automation, and host adapters.
- Prefer Rust/YggUI-compatible architecture when implementation begins unless a
  specific surface clearly needs another runtime.
- Keep standalone workbook storage and Yggterm-hosted sheet storage behind
  adapters.
- Do not make app-control, screenshots, traces, or generated summaries the
  source of workbook truth.

## Product Direction

- Treat this as a standalone public app, not a one-off experiment.
- Spreadsheet compatibility is a product constraint, not a stretch goal. Cells,
  ranges, formulas, formatting, recalculation, and workbook behavior should
  match established user expectations wherever the supported subset claims
  compatibility.
- Finance modeling quality matters from the start: assumptions, scenarios,
  auditability, units, validation, review flows, and FMI-oriented conventions
  should influence defaults and tests.
- Keyboard behavior and command organization must be data-driven so default,
  accessibility, and organization-specific maps can evolve independently from
  core logic.
- Do not ship branding, copy, keymaps, visual assets, or metadata that imply
  ownership of or endorsement by third-party spreadsheet products.
  Compatibility docs should describe behavior and file semantics, not copy
  protected expression.
- Reuse shared `yggui` concepts where possible:
  - app-control
  - traces and perf telemetry
  - deterministic UI automation
  - proof bundles
  - demo-driven changelog workflows
- Keep the bar high on interaction quality, performance, and explainability.

## Design Philosophy

- `docs/design.md` is the source of truth for Cellulose UI taste.
- Standalone Cellulose should use a YggUI-shaped shell with a sheets tree, grid
  viewport, right command surface, and hideable titlebar.
- Embedded Cellulose should drop host-owned navigation while keeping
  Cellulose-owned sheet semantics and command surfaces.

## Workflow Expectations

- Start with product and architecture clarity before heavy implementation.
- Read `docs/product.md`, `docs/architecture.md`, `docs/design.md`, and
  `docs/protocol.md` before changing product, storage, UI, command,
  compatibility, automation, or host embedding behavior.
- Prefer durable schemas and reusable abstractions over demo-only hacks.
- Keep future release storytelling in mind from the beginning; complex product behavior should be demonstrable and verifiable.
- Keep standalone Cellulose and Yggterm-embedded Cellulose separate at the
  boundary: standalone owns workbooks and sheets navigation; the embedded
  Yggterm surface uses Yggterm navigation and starts as a single-sheet host.
- Public docs should frame the project around spreadsheet compatibility,
  financial modeling, and automation rather than replacement-product language.

## Licensing

- Repository license: Apache License 2.0
- Markdown documentation license: CC BY-SA 4.0
- Copyright owner: Avikalpa Kundu
