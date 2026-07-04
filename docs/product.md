# Cellulose Product Direction

Cellulose is an open source spreadsheet and financial modeling workspace with
compatibility discipline and agent-friendly automation.

## Core Promise

Cellulose should make serious spreadsheet work inspectable, automatable, and
pleasant to operate. Human editing and agent-driven workflows should use the
same workbook truth.

## Product Pillars

- familiar grid interaction and spreadsheet semantics
- a well-tested formula and recalculation model
- financial modeling standards, reviewability, scenarios, and assumptions
- FMI-oriented modeling conventions where relevant
- configurable keyboard maps and command surfaces
- automation, explanation, reproducibility, and release-quality demos
- clean embedding into Yggterm and future YggUI-based hosts

## Standalone And Embedded Shape

Standalone Cellulose owns workbook navigation, multi-sheet workflows, command
surfaces, and workbook storage.

When hosted inside Yggterm, Cellulose starts as a single-sheet workspace surface
selected from Yggterm's metadata tree. The embedded variant uses Yggterm's left
navigation, keeps Cellulose-owned sheet semantics, and stores Yggterm-owned
sheet state under the active Yggterm state home.

## Non-Goals

- Do not build a superficial grid demo.
- Do not let the UI diverge from the supported spreadsheet semantics.
- Do not ship third-party branding, protected keymaps, or product-owned visual
  expression.
