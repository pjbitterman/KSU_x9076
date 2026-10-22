# Extra Credit 1: Practicum 1, Open Source

**Points:** up to 20
**Platform:** Google Colab
**Individual work.** This is not a paired assignment.

## Goal

Reproduce both problems from Practicum 1 using only open-source tools: GeoPandas, Shapely, and pandas in Colab, with no arcpy. Use the same variant-card numbers your pair used on implementation day, so that your results can be compared directly with the arcpy results your pair submitted. The assignment has two purposes: to demonstrate that the workflow you designed on paper is independent of the software that runs it, and to practice translating a selection-based arcpy chain into the GeoDataFrame operations introduced in part 2

## Data

The Practicum 1 inputs are shapefiles. A shapefile is several files, so each one is provided as a single `.zip` that GeoPandas reads directly from its URL, the same `DATA_BASE` pattern used in every Part 2 notebook:

```python
DATA_BASE = "https://raw.githubusercontent.com/pjbitterman/KSU_x9076/main/data/part1"

import geopandas as gpd
counties = gpd.read_file(f"{DATA_BASE}/ohio_counties.zip")
```

The six inputs:

- `ohio_counties.zip`, `portage_adj_munis.zip`, `ohio_state_parks.zip`, and `streams_portage.geojson` in `data/part1/` (Problem 1).
- `kent_campus_buildings.zip` and `kent_paths.zip` in `data/part1/variety/` (Problem 2).

Each zip holds exactly one shapefile with its sidecars, so no inner path is needed. GeoPandas reads the GeoJSON directly.

## Translation guide

Each arcpy step in your Practicum 1 design has a GeoPandas counterpart. This table is a starting point, not a complete recipe; part of the exercise is working out the remainder from the week 9 sessions and the GeoPandas documentation.

| Practicum 1 (arcpy) | Open source (GeoPandas / Shapely) |
|---|---|
| `arcpy.management.Project(fc, out, sr)` | `gdf.to_crs(26917)` (NAD83 / UTM zone 17N, meters) |
| `MakeFeatureLayer` + `SelectLayerByAttribute` | Boolean filtering: `counties[counties["NAME"] == "Portage"]` |
| `SelectLayerByLocation(..., "INTERSECT", ...)` | `gpd.sjoin(..., predicate="intersects")`, or `gdf.intersects(geometry)` |
| `SelectLayerByLocation(..., "WITHIN_A_DISTANCE", d)` | `gdf.distance(geometry) <= d`, or buffer the target by `d` and test `intersects` |
| `SUBSET_SELECTION` | Filter the already-filtered GeoDataFrame again |
| `REMOVE_FROM_SELECTION` | Negate the condition with `~` |
| `arcpy.management.GetCount(layer)` | `len(gdf)` |
| `SHAPE@AREA` in a cursor | `gdf.geometry.area` (square meters in EPSG:26917) |
| Unit conversions | 1 mile = 1609.344 m; 1 foot = 0.3048 m; 1 acre = 4046.8564224 m² |

Distances on your card are in miles and feet. Convert them to meters once, in named variables, and use those variables everywhere; ***do not type converted numbers by hand into calls.***

## Problem 1: park expansion candidates

Reproduce the six-step workflow with your card's two distances. Requirements:

1. Reproject all four inputs to EPSG:26917 before any distance or area calculation.
2. Scope to Portage County before either proximity test. State in a comment which reading of "in Portage County" you used (intersects the county polygon, or centroid within it), matching your pair's design.
3. Keep parks within the card's municipality distance of any municipality.
4. Remove parks within the card's stream distance of any stream.
5. Print, with labeled f-strings, the count of parks remaining after each step, then the final count, the names of the candidate parks, and their combined area in acres.

## Problem 2: the best-connected building

Reproduce the per-building count with your card's path distance. Requirements:

1. Reproject both campus layers to EPSG:26917.
2. Write a function with a docstring that takes one building's geometry and a distance in meters and returns the number of path segments within that distance as an integer.
3. Call that function from a loop over the buildings your pair's design counted (for example, named buildings only), and track the most and the fewest. Report ties for the fewest the way your design specified.
4. Print the result with labeled f-strings.

A vectorized version (buffer every building, spatial join the paths, group and count) is an acceptable addition after the function-and-loop version, not a replacement for it. The function and loop are what the practicum design called for.

## Comparison

In a markdown cell at the end of the notebook, present a short table comparing your pair's arcpy results with your GeoPandas results for every reported number: parks after each step, final count, names, combined acres, most-connected building and count, least-connected building and count. Below the table, explain every difference in a sentence or two. 

Differences are expected in some cases and informative in all. If the numbers match exactly, say so and say why that is the expected outcome.

## Rules

- Individual work. You may consult your pair's practicum notebook and design artifact; you may not share code with other students for this assignment.
- The course AI policy applies in full. AI tools do not write your code or your prose.
- The notebook must run top to bottom in a fresh Colab runtime.

## Deliverable

Submit the executed `.ipynb` through the Extra Credit 1 assignment in Canvas. Name it `ec01_yourlastname.ipynb`. Put your name and your team number in the first markdown cell.

## Grading

| Component | Points |
|---|---|
| Problem 1: correct for your card, projected first, scoped before the proximity tests, labeled output | 8 |
| Problem 2: function with docstring, loop, most and fewest tracked, ties handled as designed | 6 |
| Comparison table and explanation of differences | 4 |
| Runs top to bottom; `snake_case`; f-strings; distances converted once in named variables | 2 |
| **Total** | **20** |

Late submissions are not accepted for extra credit.
