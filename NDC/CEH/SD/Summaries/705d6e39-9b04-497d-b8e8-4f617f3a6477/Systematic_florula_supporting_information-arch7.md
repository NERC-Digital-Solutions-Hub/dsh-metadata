# Supporting information for Pescott, O.L. (2016). A systematic florula of a disturbed urban habitat, Sheffield, England: Plant occupancy data

## Overview
- Provides methodological and data-structure details for the plant occupancy dataset collected in a disturbed urban habitat in the Sheffield area.
- Cross-sectional snapshot survey conducted late June to early July across multiple urban 1 km2 grid cells within the British National grid.

## Sampling framework and selection
- Study area limited to 1 km2 grid cells in the British National grid (OSGB 1936, EPSG:27700) with at least 25% built-up land cover (as per the Centre for Ecology & Hydrology Land Cover Map 2000).
- Each 1 km2 cell divided into four 500 m × 500 m sub-cells (quadrants) centered on specified coordinates.
- Within each selected 1 km2 cell, all four sub-cells numbered; a random selection identified five 1 km2 cells for survey (overall 16 cells after excluding four NE cells in the Rotherham boundary).
- In each chosen 1 km2 cell, four sub-cells (0.25 km2 each) with at least 50% built-up area were numbered; one sub-cell selected randomly for survey.
- Final fieldwork surveyed 16 sub-cells across 16 urban 1 km2 cells.

## Field sampling protocol
- Survey duration: 1.5 hours per selected sub-cell or until every publicly accessible street had been walked on both sides, whichever lasted longer.
- Target habitat: pavement (sidewalk) habitat; included species rooted at edges of paved areas (walls, grass strips, kerbstones, pavement furniture, utilities, etc.).
- Garden escapes: plants observed on pavement but rooted in a garden were recorded as such (noted as “Garden escapes; surviving” in comments).
- Time window: 2012-06-23 to 2014-07-11; late June to early July each year to maintain phenological consistency.
- Taxonomic scope: all vascular plant species found in the pavement habitat; some late-flowering species may be identified to genus level if necessary due to phenology.

## Data structure and fields
- recordedName: species or aggregated name as recorded in the field.
- nameAuthor: authority for name (where applicable).
- date: collection date (DD/MM/YYYY).
- 1kmLocation: lettered British National grid reference for sampled 1 km square.
- 1kmQuadrant: quadrant (500 m × 500 m sub-cell) within the 1 km square.
- centroidEasting / centroidNorthing: coordinates of the centroid of the sampled sub-cell.
- buffer (m): distance by which centroids should be buffered and squared off to recreate sampled areas; ESRI Shapefile of these areas referenced.
- comment: notes related to plant observations (e.g., habitat context, garden escapes).

## Temporal scope and phenology notes
- Snapshot survey period limited to late June/early July; phenology may affect detectability; some late-flowering taxa identified only to genus level when identifications were uncertain.
- Suggests future resampling to account for potential phenological shifts due to climate.

## Taxonomic identification and quality control
- All plants identified by the author; specimens that could not be named in the field were keyed using Stace (2010) Flora for Britain and Ireland or vegetative keys (Poland & Clement, 2009).
- In cases with insufficient material for confident identification, observations were recorded to genus level.

## Spatial data and GIS considerations
- Uses OSGB 1936 / British National Grid coordinates; explicit 1 km2 and 500 m × 500 m sampling units.
- Data includes centroid coordinates and buffering guidance to reconstruct the exact sampled areas.
- Notes existence of an ESRI Shapefile of the sampling areas referenced in the dataset (Pescott, In review).

## Availability and references
- See also the Biodiversity Data Journal article by Pescott (2016) for full context; the Biodiversity Data Journal manuscript is listed as “In review.”
- Key references:
  - Fuller RM et al. (2002) UK Land Cover Map 2000 methodology.
  - Poland J & Clement EJ (2009) The Vegetative Key to the British Flora.
  - Stace C (2010) New Flora of the British Isles.
  - Smith H (2010) Value for birds of river corridor habitats in Sheffield area.