# Cellulose

Cellulose is an open source spreadsheet and financial modeling workspace.

The project is early scaffolding. The intended product is a focused, modern
spreadsheet environment with strong compatibility discipline, finance-oriented
modeling defaults, and first-class automation.

## Direction

Cellulose is designed around:

- familiar spreadsheet semantics for cells, ranges, formulas, formatting, and
  workbook behavior
- financial modeling standards, auditability, scenarios, assumptions, and review
  workflows
- FMI-oriented modeling conventions where they apply
- configurable keyboard maps and command organization
- YggUI-style app-control, traces, deterministic automation, and proof bundles
- a clean embedding boundary for Yggterm and other YggUI-based apps

Compatibility with established spreadsheet behavior is a core product goal.
Innovation should happen in automation, observability, finance workflows, and
clarity of implementation rather than by surprising users with incompatible grid
semantics.

## Relationship To Yggterm

The standalone Cellulose app owns workbook navigation, including a sheets tree.

When embedded in Yggterm, Cellulose should act as a single-sheet workspace
surface selected from Yggterm's metadata tree. The embedded variant should use
Yggterm's left navigation, keep the right-side command surface available, and
store Yggterm-owned sheet data under the active Yggterm state home.

## Repository Status

This repository currently contains public project scaffolding only. It is not
ready for end-user installation.

## Docs

- [Product direction](docs/product.md)
- [Architecture](docs/architecture.md)
- [Design](docs/design.md)
- [Protocol](docs/protocol.md)

## Licensing

- Code: Apache License 2.0
- Markdown docs: CC BY-SA 4.0
