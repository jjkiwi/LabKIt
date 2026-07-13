# 🧪 LabKit

A small set of simple, offline tools for the lab bench — no build step, no sign-in,
no backend. Open `index.html` in a browser (desktop or phone) and go.

## Tools

- **🧫 Well Tracker** (`tools/wells.html`) — tap each well as you pipette so you
  never lose track of which wells already have a substance added. Supports plate
  formats from 6 to 384 wells, multiple color-coded substances, undo, and a
  "toggle" or "add-only" click mode.
- **🧬 Mastermix Calculator** (`tools/mastermix.html`) — calculates PCR/qPCR
  reaction-mix component volumes for a given number of samples/controls, with a
  configurable pipetting-error buffer. Components can be excluded from the shared
  mix (e.g. DNA template) and are aliquoted separately.
- **🧪 Dilution Calculator** (`tools/dilution.html`) — solves C1·V1 = C2·V2 for
  whichever value you mark to calculate, with unit selection and a ready-to-use
  pipetting protocol ("draw X µL of stock, top up to Y µL").
- **⏱️ Multi-Timer** (`tools/timers.html`) — runs several independently named
  countdowns at once (incubation, spins, heating block…) with quick-start presets
  and an audible alarm when a timer finishes.
- **🧮 RPM ↔ RCF Converter** (`tools/rcf.html`) — converts centrifuge speed to
  relative centrifugal force and back, with saved rotors for quick recall.

## Features

- Works fully offline, no dependencies.
- Pastel, high-contrast UI designed for lab use (readable at a distance, large
  touch targets for gloved hands).
- **PL / EN** language toggle, top-right corner, remembered across visits.
- **Phone / Computer** layout picker per tool, remembered across visits.
- All state (plate progress, mastermix recipe) is saved locally via
  `localStorage` — nothing leaves the browser.

## Project structure

```
LabKit/
  index.html            — landing page, tool grid
  assets/style.css       — shared pastel theme (variables, components)
  tools/wells.html        — Well Tracker
  tools/mastermix.html    — Mastermix Calculator
  tools/dilution.html     — Dilution Calculator
  tools/timers.html       — Multi-Timer
  tools/rcf.html          — RPM ↔ RCF Converter
```

## Running locally

No build step — just open `index.html` directly in a browser, or serve the
folder with any static file server:

```
npx serve .
```
