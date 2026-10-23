# Roadmap

## Phase 1: Reference data and game setup

Collect the necessary inputs:
- ETS2 installation folder
- `base_map.scs` or equivalent base map package
- OSM dataset for roads and land features
- elevation data for terrain shape
- texture/material references
- map generation tools and scripts

Deliverable:
- working project data sources
- clear map target area
- confirmed game version compatibility

## Phase 2: Tile-based world layout

Create the map as a set of tiles rather than one giant region.

Example grid:

```text
tile_00_00  tile_00_01  tile_00_02
tile_01_00  tile_01_01  tile_01_02
tile_02_00  tile_02_01  tile_02_02
```

Each tile should contain:
- terrain data
- road network
- water surfaces
- vegetation and props
- building placement
- nav/route information

## Phase 3: Road generation from OSM

Use OSM as the road layout input.

Tasks:
- import road centerlines
- assign road widths
- identify intersections and junctions
- separate highways, roads, and local streets
- ensure the road graph is consistent inside each tile

Goal:
- a road network that can be driven and connected across tiles

## Phase 4: Elevation and terrain generation

Import height/elevation data and generate terrain.

Tasks:
- slope and contour generation
- terrain mesh creation
- road elevation alignment
- terrain masks for ground materials
- hill and valley transitions

Goal:
- terrain that supports the road network and feels like a playable landscape

## Phase 5: Water, bridges, and world masks

Add water and world masks:
- rivers
- lakes
- riverbanks
- bridge structures
- terrain material transitions

Goal:
- a believable natural environment around the roads

## Phase 6: Vegetation and buildings

Place static world objects:
- trees
- forests
- houses and city blocks
- industrial objects
- roadside props
- signs and landmarks

Goal:
- the map should not look empty or synthetic

## Phase 7: Navigation and route logic

The map must include enough route data for the game to function properly:
- road connectivity
- navigation graph
- AI pathing / traffic support
- map reference points

Goal:
- roads are not just visual; they are usable game navigation data

## Phase 8: Streaming and loading optimization

Only nearby tiles should be loaded while driving.

Implementation ideas:
- current tile + neighboring tiles active
- distant tiles unloaded
- test zones loaded first
- world chunk management handled systematically

Goal:
- avoid giant single-file load times

## Phase 9: Test, validate, expand

After the first tile works:
- test driving in that tile
- validate road continuity and terrain quality
- add adjacent tiles
- expand gradually
- fix only the current bottleneck before proceeding

## Recommended first milestone

Start with:
- 1 tile proof of concept
- then 3x3 tile region
- then multi-region expansion

Do not attempt a full ETS2 world replacement in the first pass.
