# Supporting information for the flora survey data generated to test the colonisation credit of woodlands on the isle of wight

## Purpose and GIS relevance
- Provides flora survey data to test colonisation credit of woodlands on the Isle of Wight.
- Data are suitable for map-based visualization to compare flora across woodlands and triplet configurations (ancient vs recent, nearby vs distant).

## Collection design
- Each woodland survey used 6 systematic quadrats.
- Triplets consist of:
  - an ancient woodland,
  - a recent woodland adjacent to the ancient,
  - a distant recent woodland of the same age and size but separated from the ancient.
- In each woodland, the percentage cover of all understory herbs was estimated.

## Spatial data
- Woodland coordinates provided as X, Y pairs (example entries listed).
- Coordinates are given for the woodlands; charting and spatial joins require the appropriate projection/CRS.

## Measurements and units
- Units represent percentage cover within a 1 m x 1 m quadrat.
- Data reflect percent cover values per quadrat for understory herbs.

## Quality control
- Plant identifications performed with dichotomous keys.
- Percentage cover estimated by marking grids on each quadrat to standardize measurements.

## Data structure and formats
- Data organized as a matrix: columns = species names; rows = quadrats (nested within woodlands and within triplets of three woodlands).
- Hierarchical arrangement implicit: quadrats within blocks of three woodlands per triplet, per woodland.

## GIS-ready considerations and transformations
- To use in GIS, convert matrix data into long-form records or per-quadrat attributes and link to woodland polygons or grid cells.
- Possible outputs: per-quadrat species cover maps, woodland-level summaries, or 1 m resolution rasters representing mean/total cover by species or groups.
- Prepare for data cleaning and standardization across woodlands and triplets (e.g., harmonize species names, handle missing values).

## Practical applications for map-based products
- Visualize spatial patterns of understory flora across ancient and recent woodlands.
- Compare colonisation signals between adjacent vs distant recent woods.
- Create thematic maps of mean percent cover by woodland or species assemblages to support ecological interpretation.