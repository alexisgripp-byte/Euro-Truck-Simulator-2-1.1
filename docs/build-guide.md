# Build guide

## Goal

Create a small, playable custom ETS2 region using a tile-based workflow.

## Step 1: Collect required files

You will need:
- ETS2 installation files
- `base_map.scs` or equivalent base map reference
- OSM data for the target region
- elevation data for terrain generation
- any custom textures or models you plan to add

## Step 2: Define a target area

Pick a very small region first.

A good first target is:
- a single small town or a short road corridor
- a small valley or farmland region
- a compact map area with 1–3 roads and a river

Avoid starting with a huge world replacement.

## Step 3: Create the project structure

Use the repo layout already defined in `docs/project-structure.md`.

The important thing is to separate:
- source data
- generated world data
- map tiles
- roads
- terrain
- props
- nav data

## Step 4: Import and process OSM data

Use OSM as the base road network:
- roads
- landuse
- water features
- intersections
- local pathways

Clean and simplify the network for use in a game map.

## Step 5: Generate terrain

Generate ground height from elevation data.

Then:
- align roads to terrain height
- generate slopes and contour transitions
- prepare terrain masks for vegetation and water

## Step 6: Add water and structures

Add:
- rivers
- lakes
- bridges
- culverts
- roadside features

## Step 7: Add vegetation and props

Place:
- trees
- forests
- houses and buildings
- signs and roadside objects

Keep placement dense enough to feel alive, but structured enough to remain usable for gameplay.

## Step 8: Add nav and connection logic

The road system must be valid for:
- pathing
- route generation
- AI traffic
- player navigation

## Step 9: Build a first tile

Before expanding, validate that a single tile works:
- road continuity
- terrain quality
- driving flow
- water crossings
- loading behavior

## Step 10: Expand to adjacent tiles

Once one tile is stable, add neighboring tiles and ensure they match at the borders.

## Final principle

Do not aim to replace the whole game map immediately.

Aim for a working region first, then expand by tile.
