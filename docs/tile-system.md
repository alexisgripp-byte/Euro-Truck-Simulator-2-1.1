# Tile system

A custom ETS2 map should be built as a streamed tile world.

## Why tiles matter

A single giant map file causes:
- very long loading times
- memory pressure
- poor scalability
- difficult debugging

A tile-based world allows:
- small regions to load independently
- only nearby chunks to be active
- easier map expansion over time
- faster iteration during development

## Recommended tile grid

Use a simple coordinate system:

```text
x = 0, 1, 2, 3 ...
y = 0, 1, 2, 3 ...
```

Example:

```text
tile_00_00
tile_00_01
tile_01_00
tile_01_01
```

This can later expand into a larger map area.

## Tile contents

Each tile should contain:
- terrain height information
- road structure
- water surfaces and river crossings
- vegetation placement
- buildings and props
- navigation graph data
- tile metadata / references

## Streaming behavior

When the player is in a tile:
- current tile is loaded
- adjacent tiles are loaded
- distant tiles remain unloaded

This reduces both load time and resource usage.

## Development strategy

Recommended order:
1. Build one tile
2. Make roads and terrain work there
3. Add water and bridges
4. Add props and trees
5. Add nav graph
6. Duplicate/expand to adjacent tiles

## Important note

The tiles must be designed to fit smoothly together.
This means:
- road continuity at tile borders
- terrain continuity at tile borders
- water continuity when needed
- consistent nav graph connectivity

If borders are not handled carefully, the map will feel broken during travel.
