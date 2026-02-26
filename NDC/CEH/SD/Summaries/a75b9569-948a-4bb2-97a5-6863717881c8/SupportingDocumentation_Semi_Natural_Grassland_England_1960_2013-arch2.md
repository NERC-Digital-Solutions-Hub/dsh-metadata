# Fate of semi-natural grassland in England between 1960 and 2013: a test of national conservation policy

## Overview
- A study comparing historic grassland surveys (1960–1981) with contemporary spatial habitat data (2013) to quantify changes in semi-natural grassland across England.
- Aims to assess national conservation policy by measuring shifts in grassland types and their spatial context.

## Data sources and scope
- Historic quadrat data collected at grassland sites (1960–1981) using a standardised method; 2–6 randomly placed 1m x 1m quadrats per site (some 2m x 2m).
- Quadrat locations recorded with six-figure British National Grid references (±100 m accuracy).
- Vegetation in each quadrat assigned to British National Vegetation Classification (NVC) communities using TABLEFIT.
- Quadrats further classified into four grassland types: calcareous, lowland heath and dry acid, mesotrophic, and wet grassland, aligned with Biodiversity Action Plan (BAP) names and priority habitats.
- 2013 reference data from Natural England’s Priority Habitats Inventory (PHI) for habitat extent and location.
- SSSI boundaries from Natural England digital boundary data (2014).

## Analytic methods
- Quadrat locations imported into ESRI ArcGIS v10; created 100 m buffers around each quadrat to represent site extent (matching location accuracy).
- Calculated within each buffer:
  - Percentage of priority habitat (from PHI) using tabulate intersection.
  - Percentage of buffer designated as SSSI (via SSSI boundaries and intersect with grassland sites).
- Data processed and stored for downstream analyses; emphasis on reproducibility and standardized outputs.

## Data structure and key columns (high-level)
- Per-quadrat records include:
  - ID, Date, GridRef, Grassland category (Calcareous, Mesotrophic, Wet, Lowland Heath and Dry Acid).
  - NVC1 (TABLEFIT result), SubCom1 (TABLEFIT result).
  - Percent cover metrics for various surrounding habitat components within 100 m (e.g., coastal & floodplain grazing marsh, coastal sand dunes, deciduous woodland, lowland calcareous grassland, lowland dry acid grassland, lowland fens, lowland heathland, lowland meadows, upland calcareous grassland, upland flushes/fens/swamps, upland hay meadow, purple moor-grass/dominant habitats, etc.).
  - Totals: Total % priority habitat, % of buffer that is SSSI.
- This structure supports analysis of how surrounding habitats and protections relate to the grassland quadrats.

## Outputs and implications
- Quantifies the extent and quality of semi-natural grasslands in 2013 within 100 m contexts of historic sites.
- Provides standardized metrics to compare against 1960–1981 baselines, enabling assessment of conservation policy effectiveness over time.
- Produces data suitable for reporting, mapping, and policy evaluation.

## Relevance to Analysts Monitoring the Environment
- Demonstrates a standardized, auditable workflow to monitor environmental health over time using established data sources.
- Emphasises data verification, quality assurance, cleaning, and transformation to produce clear outputs (maps, reports).
- Ensures datasets are stored and accessible via appropriate data portals, enhancing transparency and reuse.

## Challenges and opportunities highlighted
- Increasing the value of datasets by integrating them with other relevant data beyond the immediate study scope.
- Facilitating access to underlying data used to create final outputs to support broader scrutiny and reuse.

## References
- Hill, M. O. (1996). TABLEFIT, Version 10, for Identification of Vegetation Types.
- Natural England (2013). Priority Habitats Inventory (Single Habitats Layer) for England, Version 1.1.
- Natural England (2014). Sites of Special Scientific Interest and historical monuments.
- Ratcliffe, D. (1977). Nature Conservation Review.
- Rodwell, J. S. (1992). British Plant Communities: Grasslands and Montane Communities.