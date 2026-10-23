# Vaassen first tile plan

## Goal

Build the first playable custom map prototype as a small tile around Vaassen, Netherlands.

This is the first milestone in the project and should remain intentionally small and buildable.

## Working region

We will begin with a compact local area centered on Vaassen, not a large Dutch map.

Recommended first prototype area:
- a small village core around Vaassen
- immediate surrounding roads and fields
- a canal/ditch/water feature nearby
- a few road connections into and out of the village
- a small rural area rather than a full town block system

## Tile scale

Use a small start tile with a manageable footprint.

Recommended initial scale:
- 1 tile for the proof of concept
- optional expansion to 3x3 tiles afterward

A realistic first tile size for prototype work is a compact local region around the village, roughly on the order of a few square kilometres, not an entire province.

## Tile naming

Suggested initial naming:

```text
tile_vaassen_00_00
```

If expansion is needed later:

```text
tile_vaassen_00_01
tile_vaassen_01_00
tile_vaassen_01_01
```

## First tile content

The first prototype should include:

### Road network
- main access road into the village
- local village roads
- side roads to fields and farms
- at least one or two intersections
- simple continuous road graph

### Terrain
- near-flat lowland terrain
- subtle elevations only
- simple field and meadow layout
- minimal complexity for the first build

### Water and environment
- one canal or drainage feature
- small ditch/stream or water channel
- one bridge crossing if needed
- a few field boundaries and hedgerow-like edges

### Settlement
- a compact village core
- a handful of houses
- farm or rural structures
- simple roadside props

### Vegetation
- scattered trees
- hedgerows and field edges
- forest patches only if needed

## Scope rules

For the first tile, keep the scope intentionally limited.

Do not add yet:
- huge city blocks
- large industrial districts
- multiple major highways
- massive river systems
- large terrain complexity
- world-scale nav systems beyond the local tile

The goal is simply a stable first playable area.

## Data needed

We will gather:

1. OSM road and landuse data for the Vaassen area
2. Elevation data for the same area
3. Water features and drainage data
4. Reference materials for local textures and village props
5. Any base ETS2 map reference files available in the project environment

## Processing workflow

### Step 1: Define the exact bounding box
Choose a small region centered on Vaassen.
The bounding box should be large enough to include:
- the village core
- nearby roads
- water feature(s)
- enough surrounding fields to feel natural

### Step 2: Download OSM data
Clip OSM data to the selected area.
Keep only the relevant road, landuse, water, and settlement layers.

### Step 3: Simplify the road graph
Remove unnecessary complexity and keep a clean road network for the first tile.
Focus on:
- drivable roads
- road connectivity
- realistic lane-like structure
- a small, testable network

### Step 4: Generate terrain
Use elevation data to create a simple near-flat terrain surface.
The terrain should be:
- mostly level
- slightly varied around roads and field edges
- enough to look natural but not difficult to manage

### Step 5: Add water and dike structure
Add a canal/ditch or minor water feature.
If roads cross it, add bridge geometry.

### Step 6: Add props and settlement elements
Place:
- village houses
- a few farms or roadside buildings
- trees and hedges
- field borders

### Step 7: Validate driveability
Check:
- road continuity
- tile borders
- terrain fit under roads
- water crossing behavior
- basic route and navigation logic

### Step 8: Expand later
Once the first tile works, add neighboring tiles and ensure continuity across borders.

## Minimum success criteria for the first tile

The tile is successful if:
- the area loads cleanly
- roads are drivable and connected
- the terrain feels Dutch and flat
- the village and fields feel believable
- basic navigation works for the limited region
- the tile can be expanded without redesign

## Deliverables for this phase

- one defined Vaassen prototype tile
- road network from OSM
- terrain model for the region
- water feature and bridge placement
- village and field environment layout
- first playable validation pass

## Recommended next action

The next concrete step is to define the exact bounding box and the first tile area around Vaassen, then begin the OSM import and terrain generation pass for that region.
