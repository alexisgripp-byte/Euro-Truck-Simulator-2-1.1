# Euro-Truck-Simulator-2-1.1

Make a map of ETS2 in 1.1.

## Project goal

Build a custom ETS2 map prototype in a realistic and scalable way, starting from a small tile-based region instead of trying to replace the entire game world at once.

We will focus on:
- OSM road data for the road network
- height/elevation data for terrain
- rivers, lakes, bridges, and water flow
- trees, buildings, and props
- tile-based streaming so the map can load progressively while driving
- a playable custom region before expanding to a bigger world

## Core principle

The correct approach is not to make one giant file.

The correct approach is:
- split the map into tiles
- generate terrain and roads per tile
- load nearby tiles only
- unload far tiles
- build the world progressively

This keeps loading times manageable and matches how large maps are normally structured.

## Recommended first milestone

We do NOT start by replacing the whole ETS2 map.

We start with a small test map:
- 1 tile for a proof of concept
- 3x3 tile region for a first playable area
- then expand after the world generation pipeline works

## Project roadmap

### Phase 1: Setup and reference data

We need the game files and project folders:
- ETS2 installation
- base_map.scs or equivalent base map package
- project folder structure
- OSM dataset
- elevation dataset
- reference textures/materials

### Phase 2: World layout and tile system

Define a tile grid, for example:
- tile_00_00
- tile_00_01
- tile_01_00
- tile_01_01

Each tile will contain:
- terrain data
- roads
- water
- vegetation
- buildings
- route/nav information

### Phase 3: Road generation from OSM

Use OSM data to create:
- road centerlines
- road widths
- intersections
- lane structure basics
- road ordering for map generation

This becomes the road skeleton for the custom area.

### Phase 4: Terrain and elevation

Import height data and convert it into:
- terrain mesh / ground model
- slope transitions
- valleys, hills, ridges
- road placement based on elevation

This is what turns a flat road network into a believable driving map.

### Phase 5: Water, bridges, and environment

Add:
- rivers
- lakes
- bridges over water and roads
- ground material zones
- terrain masks for grass, dirt, asphalt, water

### Phase 6: Trees, buildings, and props

Add assets and placement logic for:
- trees and forests
- houses and buildings
- industrial structures
- roadside props
- signs and landmarks

### Phase 7: Navigation and route graph

The map must include enough route data for:
- GPS / navigation
- AI traffic paths
- pathfinding
- player positioning and world logic

### Phase 8: Streaming and loading

For a large map, we need tile streaming:
- load current tile + neighboring tiles
- keep memory and loading time controlled
- unload distant tiles

This is essential for large custom worlds.

## Tools and workflow

We will likely use a pipeline like:
- OSM data import
- elevation data import
- terrain generation
- road generation
- map tile generation
- map asset placement
- test build and validation

## Realistic approach for this project

This project should be treated as a staged custom map build, not a one-shot mod.

The best order is:
1. Build a tiny tile test area
2. Make roads and terrain work there
3. Add water and bridges
4. Add vegetation and buildings
5. Add nav graph / route logic
6. Extend to multiple tiles
7. Then consider bigger world expansion

## Initial repository structure

We will organize the project like this:

```text
/
  README.md
  docs/
    roadmap.md
    tile-system.md
    build-guide.md
  data/
    osm/
    elevation/
    reference/
  src/
    generation/
    terrain/
    roads/
    streaming/
  tools/
    scripts/
```

## Important note

This is a large and advanced project. We are not trying to create a complete ETS2 replacement world in one pass.

The correct target is: a working custom region, tile-based streaming, and a clean path toward expansion.

## Next step

The next step is to create the initial project structure and write down the roadmap in the repository so the work is organized and traceable.
