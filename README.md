# Heatmap Ramp Studio

A single-file tool for building sets of matching five-step color ramps — the kind
GitHub and the Obsidian heatmap plugins use for contribution-style year grids.

Pick **one** starting color. The studio derives as many matching ramps as you
ask for, using a color-harmony or color-space system you choose, and previews
each one as an Obsidian year-heatmap. Copy any ramp as a quoted row, forward or
reversed.

## Use it

Open `heatmap-color-picker.html` in any browser. No build step, no server, no
dependencies — it also runs straight from `file://`.

## What's inside

- **Starting-point picker** — HSV field + hue strip; the picked color is the
  darkest step of the first ramp, and its OKLCH values drive everything else.
- **Heatmaps slider (1–8)** — how many ramps to generate.
- **Twelve systems** for how the ramps relate — triadic, analogous,
  split-complementary, tetradic, golden-angle, perceptually-even OKLCH,
  ColorBrewer sequential, cubehelix, Material tonal, classic HSL, warm/cool
  split, monochromatic — each with an inline explanation and each scaling to any
  count.
- **Ramp shaping** — hue drift, chroma curve.
- **Heatmap tuning** applied to every set at once — intensity levels, lightest
  step, step spacing (gamma), empty-cell color.
- **Live preview** — one Obsidian-style year grid per ramp, pinned beside the
  controls.
- **Copy output** — per-ramp rows and combined blocks, forward and reversed,
  with optional spacing / bracket wrapping.

All color math (OKLCH ⇄ sRGB with gamut clipping, HSV, HSL, cubehelix) is
implemented inline. Light and dark themes are both supported.

## License

[MIT](LICENSE) © 2026 Florian Lohse

See [CHANGELOG.md](CHANGELOG.md) for release history.
