# Supporting documentation for dataset relating to Dorset Valuing Nature Project field component botanical data

## Overview
- Purpose: Establish a baseline to assess how ecosystem services change with habitat condition, using Good’s 1931–1939 Dorset botanical survey as the reference.
- Source: Data derived from the Good archive; publicly available via the Dorset Environmental Records Centre (DERC).
- Scope: Subsampled Good-identified calcareous grassland, heathland, and woodland sites to create a gradient of habitat condition (degradation/restoration/SSSI quality) for survey and comparison.
- Site selection: 13 calcareous grassland, 13 heathland, and 12 woodland sites chosen to represent a range of condition states across the gradient.
- Gradient framework: Each habitat type has defined gradient categories (e.g., improvements, restorations, SSSI-quality status) linked to historical (1940) and contemporary (2017) classifications.

## Experimental design
- Baseline data source: Prof. Ronald Good’s 1930s botanical survey.
- Data sources for site identification and context: UK Land Cover Map 2007, Natural England Priority Habitat Inventory (2015), Sites of Special Scientific Interest (SSSIs; 2014), Horsfall (1981), Dorset Heathland survey (Rose et al., 2000), Higher Level Stewardship data.
- Gradient definitions by habitat:
  - Calcareous: categories range from improved grassland (historical calcareous grassland lost or altered) to calcareous grassland (SSSI quality) and restoration scenarios.
  - Heathland: categories include coniferous plantation on heathland, high-gorse heathland, and heathland (SSSI quality).
  - Woodland: categories include coniferous plantation, broadleaf woodland, and ancient woodland (SSSI quality); some relate to maintenance/restoration designations.
- Note: The gradient categories are linked to both historical (1940) and current (2017) habitat classifications via a lookup framework.

## Collection methods
- Plot design:
  - Heathland and calcareous grassland: 50m x 50m sample square with five 1m x 1m quadrats per site; sampling points chosen along a W-shaped transect within each square.
  - Woodland: five 10m x 10m quadrats laid in a cross across the 50m x 50m area to capture canopy; within each, a center 5m x 5m quadrat for understory and shrubs, and a nested 2m x 2m quadrat for ground-level and herbaceous data.
- Measurements:
  - Heathland/grassland: percent cover by species (to species or genus), bare ground and litter, and sward height (average of five ruler measurements per quadrat).
  - Woodland: canopy cover and species in the 10m x 10m quadrats; detailed recording of tree types, growth forms, and understory components within nested sub-quadrats.
- Data capture: Field ecologists record data directly into spreadsheets; emphasis on consistent methodology within the survey team.

## Quality control
- Consistency: All surveys conducted by the same experienced field ecologists to ensure comparability.
- Data integrity: Field data checked for anomalies during entry.
- Metadata and structure:
  - Two main data files with explicit column headings and units:
    - DVNP_Botanical_Data_Groundcover
    - DVNP_Botanical_Data_WoodlandCanopy
  - Fields include site identifiers, dates, surveyors, habitat, grid references, quadrat details, species names (or genus when needed), cover percentages, vegetation layers, and measurement units.
- Provenance mapping: A lookup table connects 1940 habitat classifications to 2017 gradient categories to support gradient analysis.

## Data structure and provenance
- Data organization:
  - Groundcover data file records ground-level and herbaceous data for heathland and calcareous grassland plots.
  - WoodlandCanopy data file records canopy and structural data for woodland plots (tree, shrub, understory, and saplings across nested quadrats).
- Metadata emphasis:
  - Detailed field definitions, units, and data column semantics to support discovery, re-use, and integration with other datasets.
- Gradient linkage: 2017 habitat gradient categories are mapped from 1940 classifications to enable longitudinal analyses of habitat condition effects on botanical data.

## References
- Good, R. (1937) An account of a botanical survey of Dorset. Proc Linn Soc 149:114-116
- Horsfall, A. (1981) A pattern of change: observations on plant habitat change in North-East Dorset since 1931: Part 3, 1981. Dorset Proc 103
- Natural England (2014) Sites of Special Scientific Interest and historical monuments
- Natural England (2015) Priority Habitats' Inventory version 2.1
- Rose RJ, Webb NR, Clarke RT, Traynor CH (2000) Changes on the heathlands in Dorset, England, between 1987 and 1996. Biol Conserv 93:117-125