# Supporting information for Pescott, O.L. (2016). A systematic florula of a disturbed urban habitat, Sheffield, England: Plant occupancy data. NERC Environmental Information Data Centre. http://doi.org/10.5285/705d6e39-9b04-497d-b8e84f617f3a6477

## Purpose and scope
- Provides supplementary details for the project “A systematic florula of a disturbed urban habitat, Sheffield, England: Plant occupancy data” to support data sharing and reuse.
- Describes sampling design, data collection, and data structure to enable interpretation and reuse alongside the main Biodiversity Data Journal paper (Pescott, in review).

## Study area and sampling design
- Area: urban habitat within the British National grid (OSGB 1936, EPSG:27700) in the Sheffield area; targeted cells have at least 25% built-up land cover from the UK Land Cover Map 2000.
- Initial stratification: the 1 km2 grid cells were divided into four quadrants (NE, SE, SW, NW).
- Selection: within quadrants, urban 1 km2 cells were randomly sampled; 16 cells were selected after excluding four NE cells that fell in the neighbouring city of Rotherham.
- Within each selected 1 km2 cell: all four 500 x 500 m sub-cells with at least 50% built-up area were identified, and a single sub-cell was randomly chosen for survey (resulting in 16 sub-cells surveyed overall).
- Survey focus: plants recorded only if they occurred in the pavement (sidewalk) habitat, including species rooted at the pavement edge or immediately adjacent features (walls, grass strips, kerbstones, pavement furniture, utilities, etc.). Some garden-escaped plants that persist on the pavement boundary were recorded as such in the comments.

## Field data collection and habitat sampling
- Survey duration per sub-cell: 1.5 hours or until every publicly accessible street had been walked on both sides, whichever took longer.
- Habitat scope: pavement-dwelling vascular plant species.
- Documentation of unusual occurrences: notes such as “Garden escapes; surviving” were used when plants were present from garden-adjacent sources but persisted in the focal habitat.

## Temporal coverage and phenology
- Period: 23 June 2012 to 11 July 2014 (late June to early July each year).
- Design intent: cross-sectional snapshot for each year; acknowledges that a small number of late-flowering species were identified to genus level due to assessment timing.
- Guidance for future work: recommends considering seasonality and potential phenological shifts in re-surveys to maintain detectability consistency.

## Data structure and interpretation
- Data fields and concepts:
  - recordedName: species or aggregation as observed.
  - nameAuthor: authority for the name.
  - date: observation date (DD/MM/YYYY).
  - 1kmLocation: 1 km square identifier (lettered grid reference).
  - 1kmQuadrant: quadrant designation of the 1 km square.
  - centroidEasting / centroidNorthing: coordinates of the sub-cell centroid.
  - buffer (m): distance to recreate the sampled area geometry for analysis.
  - comment: remarks on observations (e.g., habitat notes).
- Data provisioning: an ESRI Shapefile of the sampled areas is provided to facilitate spatial recreation of sampling units.

## Quality control and identification
- Identifications: conducted by the author.
- Verification: specimens that could not be named in the field were identified using the Flora for Britain and Ireland (Stace 2010) or vegetative keys (Poland & Clement 2009).
- Limitations: in some instances, material was insufficient for definitive identification, leading to genus-level records.

## Data provenance and references
- Supporting information linked to the main dataset and the Biodiversity Data Journal article (in review).
- Key references:
  - Fuller et al. (2002) on the UK Land Cover Map 2000.
  - Poland & Clement (2009) vegetative key to the British flora.
  - Smith (2010) relevance of green corridors to birds in Sheffield.
  - Stace (2010) New Flora of the British Isles.

## Implications for monitoring frameworks
- Demonstrates a clear, randomized, nested sampling design within an urban matrix to assess pavement flora.
- Emphasizes practical field methods focused on a specific microhabitat (pavement) and explicit criteria for inclusion of observations.
- Highlights data structure that supports reproducibility and spatial recreation of sampling units, essential for monitoring over time.
- Addresses data quality controls and the need for robust metadata and reference standards to ensure data usability in policy and management contexts.
- Notes temporal constraints and the importance of considering phenology in future monitoring rounds.