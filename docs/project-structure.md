# Project structure

This repo is organized as a custom ETS2 map development project.

## Top-level layout

```text
/
  README.md
  docs/
    roadmap.md
    tile-system.md
    build-guide.md
  data/
    README.md
    osm/
    elevation/
    reference/
  src/
    README.md
    generation/
    terrain/
    roads/
    streaming/
  tools/
    README.md
    scripts/
```

## Purpose of each folder

- `docs/`: planning and development documentation
- `data/`: all imported source datasets and reference assets
- `src/`: map generation and world-building logic
- `tools/`: custom scripts for conversion and processing

## Current objective

Build a small, playable custom ETS2 region before trying to expand to a full map replacement.

The current goal is:
- roads from OSM
- elevation-based terrain
- tile-based streaming
- water, bridges, and vegetation
- basic route/nav data
- a test map that can be expanded later

## Main principle

A large ETS2 map should not be created as one giant file.
It should be divided into tiles and streamed during driving.
