# A systematic florula of a disturbed urban habitat, Sheffield, England: Plant occupancy data

## Overview
- Supporting information for O.L. Pescott (2016) detailing plant occupancy data from a cross-sectional survey of pavement habitat in urban Sheffield.
- Focuses on vascular plant species found growing in pavement-associated habitats within selected urban 1 km2 grid cells.

## Sampling design and scope
- Based on the British National grid (OSGB 1936, EPSG:27700) with at least 25% built-up land cover from the Land Cover Map 2000.
- The study area in Sheffield was divided into four quadrants (north-east, south-east, south-west, north-west).
- Five 1 km2 cells were randomly selected per area; four NE cells that fell in the adjacent city of Rotherham were excluded, leaving 16 sampled cells.
- Within each selected 1 km2 cell, its four 500×500 m sub-cells with at least 50% built-up were numbered; one sub-cell was randomly chosen for survey.

## Field methods and targets
- In the field, 16 selected 500×500 m sub-cells were surveyed for 1.5 hours or until every publicly accessible street had been walked on both sides, whichever took longer.
- Plants were recorded only if they occurred in the pavement (sidewalk) habitat, including plants rooted at edges of paved areas (e.g., walls, kerbstones, grass strips, pavement furniture, utilities).
- Occurrences on the pavement side of a boundary wall but rooted in a garden were recorded as present in the focal habitat and marked as "Garden escapes; surviving" in the dataset.
- The survey period was a late-June to early-July window across three years (2012–2014), creating a cross-sectional snapshot.

## Temporal scope and phenology note
- Survey dates span 2012-06-23 to 2014-07-11.
- Late-flowering species may be identified to genus level due to phenological timing; multi-visit surveys were outside the project’s resources.
- Future re-surveys should consider shifting phenology due to climatic changes.

## Target taxa and data coverage
- Includes all vascular plant species observed in the targeted pavement habitat during the survey period.

## Data structure and geographic outputs
- Fields include:
  - recordedName (species or aggregate as observed)
  - nameAuthor (authority for name)
  - date (dd/mm/yyyy)
  - 1kmLocation (lettered British National grid reference for the 1 km square)
  - 1kmQuadrant (sub-cell quadrant)
  - centroidEasting, centroidNorthing (centroid coordinates of the 500×500 m sub-cell)
  - buffer (meters) to recreate sampled areas
  - comment (notes on observations)
- An ESRI Shapefile of the sampled areas is available to support spatial recreation.

## Quality control and identifications
- All plants were identified by the author in the field.
- Specimens not identifiable in the field were keyed using:
  - The Flora for Britain and Ireland (Stace 2010) or vegetative keys (Poland & Clement 2009).
- In cases where materials were insufficient, identifications were recorded to genus level.

## Interpretation and usage notes
- This study provides a standardized, auditable dataset of pavement-plant occupancy suitable for monitoring urban habitat health and policy performance over time.
- The data are intended for integration with other datasets to increase value beyond single-use analyses and to facilitate broader accessibility.

## Data accessibility and references
- Supporting information linked to the Biodiversity Data Journal publication (in review) and the main data paper.
- Key references acknowledged:
  - Fuller RM et al. (2002) The UK Land Cover Map 2000.
  - Pescott O.L. (2016) Biodiversity Data Journal (in review).
  - Poland J & Clement EJ (2009) The Vegetative Key to the British Flora.
  - Smith H (2010) Value for birds of green corridors in the Sheffield area.
  - Stace C (2010) New Flora of the British Isles.