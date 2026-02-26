# Fate of semi-natural grassland in England between 1960 and 2013: a test of national conservation policy

## Objective
- Quantify changes in semi-natural grassland in England between 1960 and 2013 by comparing historic grassland survey data with contemporary spatial data of habitats.
- Use findings to inform assessment of national conservation policy.

## Data sources and classification
- Historic quadrat data (1960–1981)
  - Sites across England; at each site, 2–6 randomly positioned 1m x 1m quadrats (some 2m x 2m).
  - Quadrat locations recorded with six-figure British National Grid references (accuracy ≈ ±100 m).
  - Vegetation in each quadrat assigned to British National Vegetation Classification (NVC) communities using TABLEFIT.
  - Quadrat sites classified into four grassland types:
    - Calcareous grassland (BAP: Lowland Calcareous Grassland; NVC CG1-9)
    - Lowland heath and dry acid grassland (BAP: Lowland Dry Acid Grassland; NVC U1-4, H1-H8)
    - Mesotrophic grassland (BAP: Lowland Meadows/Coastal & Floodplain Grazing Marsh; NVC MG1, MG3, MG4, MG5, MG6, MG9, MG10)
    - Wet grassland (BAP: Purple Moor Grass & Rush Pastures; NVC M22-M26)
- Contemporary data (2013)
  - Natural England Priority Habitats Inventory (PHI) provides geographic extent and location of 27 priority habitats.
- Administrative boundaries for context
  - SSSI (Sites of Special Scientific Interest) boundaries used to compute coverage within sites.

## Spatial analysis and methodology
- Geographic information system (GIS)
  - Location of each quadrat imported into ArcGIS v10.
  - A 100 m buffer created around each quadrat to reflect spatial accuracy and define a grassland site.
  - Percentage of each buffered site that is priority habitat calculated using tabulate intersection (PHI data).
  - Percentage of each buffered site designated as SSSI calculated by intersecting the buffer with Natural England’s SSSI boundaries (2014 data).
- Data integration and processing
  - Links between historic NVC classifications and current habitat designations enable analysis of change over time.
  - Synthesis performed at the site level (quadrat + 100 m buffer) to approximate broader grassland extent and quality.
  
## Column headings and what they capture
- ID: Unique identifier for each quadrat
- Date: Date quadrat was surveyed
- GridRef: Quadrat location reference
- Grassland category: Designated grassland type (Calcareous, Mesotrophic, Wet, Lowland Heath and Dry Acid)
- NVC1: NVC group assigned by TABLEFIT
- SubCom1: Sub-community group assigned by TABLEFIT
- CFPGM, CSDUN, DWOOD, GQSIG, LCGRA, LDAGR, LFENS, LHEAT, LMEAD, LPAVE, MCSLP, MUDFL, PMGRP, RBEDS, TORCH, UCGRA, UFFSW, UHMEA: Percent cover within the 100 m buffer for various habitat features (e.g., coastal & floodplain marsh, dunes, woodland, various grassland types, etc.)
- Total %of priority habitat: Percentage of the 100 m buffer classified as a priority habitat
- %of SSSI: Percentage of the 100 m buffer classified as a Site of Special Scientific Interest

## Purpose and expected outcomes
- To provide a quantified comparison of historical semi-natural grassland with contemporary habitat designations.
- To assess how much of the surveyed areas (within 100 m buffers) fall within priority habitats and SSSIs, informing interpretation of conservation policy effectiveness.

## References and data sources
- Hill, M. O. (1996). TABLEFIT, Version 10, for Identification of Vegetation Types. Centre for Ecology and Hydrology, UK.
- Natural England (2013). Priority Habitats Inventory (Single Habitats’ Layer) for England, Version 1.1.
- Natural England (2014). Sites of Special Scientific Interest and historical monuments.
- Ratcliffe, D. (1977). Nature Conservation Review.
- Rodwell, J. S. (1992). British Plant Communities: Grasslands and Montane Communities.