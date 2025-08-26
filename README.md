# Elegoo Neptune 3 Pro – Pen Plotter Toolhead (based on pltr_toolhead)

Turn your Elegoo Neptune 3 Pro into a precise pen plotter. This is a remix of pltr_toolhead with updated mounts and clearances for the Neptune 3 Pro.

## Highlights
- Spring-loaded pen carriage (consistent pressure)
- Zero firmware changes required (uses Z for pen up/down)
- Works with Inkscape → G-code (or the included `svg2gcode.py`)

## Quick Start
1. Print `hardware/stl/*.stl` (0.2 mm, 3 perimeters, 30% gyroid).
2. Assemble and calibrate (see `docs/`).
3. Tape A4 paper to the bed, home (`G28`), jog Z until pen just touches paper, then `G92 Z0`.
4. Plot a test: `examples/*.gcode`.

## Conventions
- Pen up: `G1 Z5 F1200`
- Pen down: `G1 Z0 F600`
- Travel feed: 3000–6000; draw feed: 800–2000 (depends on pen)

## Vector → G-code
- PDF→SVG: `inkscape --export-plain-svg=out.svg input.pdf`
- SVG→G-code: `python software/svg2gcode.py out.svg --out plot.gcode`

## Licenses
- Hardware: CERN-OHL-S v2 (see `LICENSE-HW`)
- Docs: CC-BY-4.0 (see `LICENSE-DOCS`)


You can also find the full build instructions on YouTube: https://youtu.be/c1Wo9KkZKNQ

https://user-images.githubusercontent.com/46334898/128704015-6d35a433-be92-40f1-b036-9eccbbc82462.mp4

![](https://user-images.githubusercontent.com/46334898/128649924-20f4fdde-0154-433b-928d-fcd76984723f.jpeg)

https://user-images.githubusercontent.com/46334898/128702978-db2b59bf-4a6f-4ef1-8289-b92065d79d5a.mp4

