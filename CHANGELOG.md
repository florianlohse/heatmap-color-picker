# Changelog

All notable changes to this project are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.0] - 2026-08-30

First public release. A single self-contained `heatmap-color-picker.html` — no
build step, no dependencies, runs from `file://`.

### Added

- **Visual starting-point picker.** HSV saturation/brightness field plus a hue
  strip; the picked color becomes the darkest (most-active) step of the first
  ramp. Its OKLCH lightness, chroma, and hue are shown and everything else is
  derived from it. Draggable, keyboard-adjustable, click-to-copy hex.
- **Heatmaps slider (1–8, default 3).** Chooses how many matching ramps to
  generate; drives the preview panels and the copy output together.
- **Twelve relationship systems**, each with an inline explanation: Evenly
  spaced (triadic), Analogous, Split-complementary, Tetradic, Golden-angle,
  Perceptually even (OKLCH), ColorBrewer sequential, Cubehelix, Material tonal,
  HSL "classic web", Warm / cool split, Monochromatic. Every system scales to
  any heatmap count.
- **Ramp shaping:** hue-drift-toward-yellow and a chroma curve (bell / falling /
  flat), with per-system defaults and a reset.
- **Heatmap tuning applied to all sets at once:** intensity levels (3–8),
  lightest-step lightness, step spacing (gamma on the ramp), and empty-cell
  color.
- **Live Obsidian-style preview** pinned beside the controls — one year-grid per
  ramp with month labels, weekday rows, and a `less → more` legend, driven by
  deterministic sample activity.
- **Copy output:** each ramp as a quoted, comma-separated row (forward or
  reversed), plus combined "all ramps" blocks in both directions and the
  empty-cell color. Optional `, ` spacing and `[ ]` wrapping.
- All color math (OKLCH ⇄ sRGB with chroma-reduction gamut clipping, HSV, HSL,
  Cubehelix) implemented inline; light/dark theme support with a manual toggle;
  responsive two-pane layout that collapses to a single column on mobile.

[1.0.0]: https://github.com/florianlohse/heatmap-color-picker/releases/tag/v1.0.0
