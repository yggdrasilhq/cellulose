# Cellulose Design

Cellulose should feel like a precise desktop tool for financial models and
spreadsheet work.

## Layout

- Standalone Cellulose uses a YggUI-shaped shell: left sheets tree, central grid,
  right command surface, optional inspector panels, and hideable titlebar.
- Embedded Cellulose drops host-owned navigation. In Yggterm, the left tree
  belongs to Yggterm and Cellulose owns the grid plus spreadsheet commands.
- The right command surface should be structured for keyboard navigation and
  repeated work, not decorative presentation.

## Interaction Taste

- Grid editing must feel immediate and predictable.
- Selection, fill, copy/paste, formula entry, formatting, undo/redo, and
  recalculation should behave consistently with the supported compatibility
  subset.
- Keyboard maps are configurable data. Defaults should be familiar, documented,
  and legally clean.
- Agent actions and human commands should meet at the same command registry.

## Visual Language

- Prefer quiet, dense, readable UI over illustrative chrome.
- Make active cell, selection ranges, formula references, validation issues, and
  recalculation state visually explicit.
- Treat audit trails, assumptions, scenarios, and model diagnostics as first
  class spreadsheet surfaces.

