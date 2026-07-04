# Cellulose Protocol

This document records the contracts agents should preserve while the
implementation is still forming.

## Workbook Truth

- Workbook, sheet, cell, range, formula, formatting, and dependency graph state
  belong to the workbook model.
- Formula evaluation must be deterministic for a given workbook state and
  calculation mode.
- UI selection, app-control state, screenshots, and traces are observers, not
  workbook truth.

## Compatibility

- Supported spreadsheet behavior needs fixtures before it is called compatible.
- Compatibility docs should describe observable behavior, file semantics, and
  formulas without copying protected expression from third-party products.
- Keyboard maps are user-configurable data and must not define semantic
  behavior.

## Embedding

- Standalone Cellulose owns workbooks, sheets navigation, and workbook storage.
- Yggterm-hosted Cellulose starts as a single-sheet host surface selected from
  Yggterm's metadata tree.
- Embedded storage must use an explicit host adapter and preserve sheet identity
  across restarts.
- App-control must expose active sheet, active cell/range, formula/value state,
  dirty/saved state, and storage adapter.

## Automation

- App-control actions should execute the same command registry used by the UI.
- Proof bundles should include state, screenshots, and traces when user-visible
  behavior changes.
