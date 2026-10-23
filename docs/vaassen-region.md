# Vaassen region prototype

## Target area

We will start with a small first playable region around Vaassen, Netherlands.

This is a strong first target because:
- the terrain is mostly flat and easy to work with
- the village layout is compact and realistic for a small map prototype
- it offers a mix of roads, fields, water, and a small settlement area
- it is small enough to build as a first tile or 3x3 tile region

## Why Vaassen is a good starting point

Vaassen is a good prototype location because it has:
- a village center
- nearby road connections
- open farmland areas
- canals and water features
- surrounding countryside that can be expanded later

This gives us:
- a realistic village environment
- easy road generation from OSM
- manageable building and prop placement
- a clean starting point for larger tile expansion

## First milestone

We will first build a small custom region around Vaassen, not a full replacement of the ETS2 world.

Our initial milestone is:
- 1 playable tile for the Vaassen prototype
- simple road layout from OSM
- low-relief terrain
- water and dike/canal features
- village buildings and field areas
- enough nav data for driving and basic route use

## Tile plan

We will define a first tile as a compact area centered on Vaassen.

Suggested tile naming:
- `tile_vaassen_00_00`

Later we can expand to neighboring tiles such as:
- `tile_vaassen_00_01`
- `tile_vaassen_01_00`
- `tile_vaassen_01_01`

## Region boundaries

The first prototype should remain small and manageable.

Recommended scope:
- Vaassen village core
- immediate surrounding roads and fields
- nearby rural roads and canal features
- a narrow connection to the surrounding highway/local road network

Do not start by building a giant Dutch map. Start with a compact village region and expand from there.

## Target features for the first prototype

### Road network
- main road access into the village
- connecting rural roads
- local roads around houses and fields
- small junctions and intersections
- road network derived from OSM

### Terrain
- near-flat lowland terrain
- subtle elevation changes only
- field contours and drainage patterns
- small grade changes near road edges

### Water and environment
- canals
- ditches
- small water features
- bridge crossings
- soft field edges and countryside textures

### Settlement
- village center buildings
- houses and farm properties
- sparsely placed trees and hedgerows
- a few industrial or service-area structures

### Navigation
- connected road graph for driving
- route pathing for a small region
- start point and basic map connectivity

## Build sequence

1. Download OSM data for the Vaassen region
2. Clip data to the test tile area
3. Filter roads to keep the clean road graph
4. Generate terrain and ground surface
5. Add water/canal elements
6. Place village and rural buildings
7. Add trees, hedges, and roadside props
8. Validate the road flow and route continuity
9. Expand to adjacent tiles after the prototype works

## Success criteria

The first Vaassen prototype is successful when:
- the tile loads correctly
- roads are drivable and connected
- terrain matches the flat Dutch countryside feel
- water features are present and believable
- the village feels like a real place instead of a generic block area
- the region can be expanded to neighboring tiles cleanly

## Next step

We will now define the first Vaassen tile in a concrete project layout and prepare the data sources and generation steps around it.
