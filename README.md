# Euro-Truck-Simulator-2-1.1

Make a map of ETS2 in 1.1.

## Current target

We are starting with a small custom map prototype based around Vaassen, Netherlands.

This is the first intended playable region and the best place to begin because it is:
- mostly flat
- realistic for a small Dutch countryside map
- easy to build in a first tile or small 3x3 tile area
- expandable into a larger region later

## Project goal

Build a custom ETS2 map prototype in a realistic and scalable way, beginning with a compact region instead of trying to replace the entire game world at once.

## Core principle

The correct approach is not to build one giant map file.
The correct approach is to build a tile-based world that loads only nearby sections while driving.

## Current milestone

The first milestone is the Vaassen prototype:
- one playable tile at minimum
- OSM-derived road network
- near-flat Dutch terrain
- water features, fields, and village structures
- basic road connectivity and nav logic

## Project roadmap

We are now following this order:
1. Define the Vaassen test area
2. Prepare OSM and elevation data
3. Build a first tile around the village
4. Add roads, terrain, and water
5. Add vegetation and village props
6. Validate the tile in-game
7. Expand to neighboring tiles

See also:
- `docs/roadmap.md`
- `docs/tile-system.md`
- `docs/build-guide.md`
- `docs/vaassen-region.md`
