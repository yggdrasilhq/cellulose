# Cellulose Architecture

Cellulose should separate spreadsheet truth from UI, automation, and host
embedding from the start.

## Boundaries

- `workbook`: workbook, sheet, cell, range, format, formula, dependency graph,
  recalculation, and persistence
- `ui`: shell chrome, sheets tree, grid viewport, right command surface, and
  dialogs
- `commands`: command registry, keyboard maps, palette actions, and ribbon-style
  organization
- `automation`: app-control state, deterministic actions, traces, and proof
  capture
- `host`: embedding adapters for Yggterm and future YggUI shells

## Source Of Truth

- Workbook and sheet content live in the workbook model and storage adapter.
- Formula results come from the calculation engine and dependency graph.
- Keyboard maps trigger commands; they do not define command semantics.
- App-control, screenshots, traces, and proof bundles are observers. They prove
  behavior, but they must not drive workbook state.

## Shared Platform

This repository is expected to reuse shared YggUI platform pieces over time:

- app-control
- state and trace export
- automation macros
- proof bundle capture
- changelog and demo publication workflow

The app-specific work should then focus on:

- spreadsheet and grid semantics
- formula/modeling behavior
- workbook, sheet, and embedded single-sheet storage adapters
- configurable keyboard maps and command registries
- compatibility fixtures for supported spreadsheet behavior
- visual language for analytical work
- workflow-level performance

The implementation stack is still open, but reuse of shared YggUI
infrastructure is a deliberate goal.

Standalone Cellulose should own workbook navigation and multi-sheet workflows.
When hosted inside Yggterm, the integration should start as a single-sheet
surface selected from Yggterm's metadata tree, with storage adapted to the active
Yggterm state home.
