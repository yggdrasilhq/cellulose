# Cellulose

Spreadsheets are the most-used programming environment on earth, and finance runs on them. Yet your options are Excel, which is proprietary and closed, or a free clone that quietly breaks compatibility and feels foreign the moment you build anything real.

Cellulose is an open-source spreadsheet and financial-modeling workspace that takes compatibility seriously. Familiar grid semantics, finance-oriented modeling defaults, and first-class automation, free to use and yours to keep. It works on its own, and it embeds cleanly into Yggterm and other YggUI-based apps.

## What Cellulose is for

- familiar spreadsheet behavior for cells, ranges, formulas, formatting, and workbooks
- financial modeling with auditability, scenarios, assumptions, and review workflows
- configurable keyboard maps and command organization, so the muscle memory you already have keeps working
- automation, traces, deterministic testing, and proof bundles built in, the YggUI way
- a clean embedding boundary for Yggterm and other YggUI-based apps

Compatibility with established spreadsheet behavior is a core goal, not an afterthought. The innovation belongs in automation, observability, finance workflows, and clarity of implementation, not in surprising you with a grid that behaves differently from the one you know.

## Standalone and embedded

On its own, Cellulose owns workbook navigation, including a sheets tree.

Embedded in Yggterm, Cellulose becomes a single-sheet workspace surface chosen from Yggterm's tree. It uses Yggterm's left navigation, keeps the right-side command surface available, and stores Yggterm-owned sheet data under the active Yggterm state home.

## Status

Cellulose is early. This repository is public scaffolding and direction, not yet an installable app.

Read the direction in [docs/product.md](docs/product.md), and the shape in [docs/architecture.md](docs/architecture.md), [docs/design.md](docs/design.md), and [docs/protocol.md](docs/protocol.md).

## License

- Code: Apache-2.0, see `LICENSE-APACHE`
- Documentation: CC BY-SA 4.0, see `LICENSE-CC-BY-SA-4.0`
- Names and logos: see `TRADEMARKS.md`
- Summary in `LICENSE`
