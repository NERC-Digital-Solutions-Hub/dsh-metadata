# Fate of semi-natural grassland in England between 1960 and 2013: a test of national conservation policy

## Overview
- A study comparing historic grassland survey data (1960–1981) with contemporary spatial data (2013) to quantify changes in semi-natural grassland across England.
- Aims to inform national conservation policy and monitoring frameworks by linking past vegetation data with current habitat inventories.

## Data sources and survey design
- Historic survey data collected at grassland sites in England from 1960–1981 using a standardized method; some data also used in Nature Conservation Review (Ratcliffe, 1977).
- At each site: cover of vascular plant species recorded from two to six randomly placed quadrats (mostly 1m x 1m; some 2m x 2m).
- Quadrat locations recorded with six-figure British National Grid references, with an accuracy of ±100m.
- Quadrats were assigned to British National Vegetation Classification (NVC) communities using TABLEFIT and then categorized into four grassland types:
  - Calcareous grassland (Lowland Calcareous Grassland; NVC CG1-9)
  - Lowland heath and dry acid grassland (Lowland Heath; NVC U1-4, H1-H8)
  - Mesotrophic grassland (Lowland Meads; NVC MG1, MG3, MG4, MG5, MG6, MG9, MG10)
  - Wet grassland (Purple moor-grass and rush pastures; NVC M22-M26)
- Classification also linked to Biodiversity Action Plan (BAP) names and Priority Habitat statuses where applicable.

## Analytic methods
- Quadrat locations and 100m buffers were created in ESRI ArcGIS v10 to represent grassland sites, matching the ±100m spatial accuracy of the original quadrats.
- 2013 coverage of seminatural grassland was derived from Natural England’s Priority Habitats Inventory (PHI), which maps habitats of principal importance under the NERC Act (2006).
- For each site (quadrat + 100m buffer):
  - The percentage and type of priority habitat within the buffer were calculated using the tabulate intersection function in the Spatial Analyst toolbox.
  - The percentage of the buffer overlapping Sites of Special Scientific Interest (SSSI) was calculated using Natural England’s SSSI boundaries (intersected with the grassland sites).
  
## Dataset structure and metadata
- Columns include:
  - ID: Unique quadrat identifier
  - Date: Quadrat survey date
  - GridRef: Quadrat grid reference
  - Grassland category: Calcareous, Mesotrophic, Wet, or Lowland Heath and Dry Acid
  - NVC1: NVC group from TABLEFIT
  - SubCom1: Sub-community group from TABLEFIT
  - CFPGM, CSDUN, DWOOD, GQSIG, LCGRA, LDAGR, LFENS, LHEAT, LMEAD, LPAVE, MCSLP, MUDFL, PMGRP, RBEDS, TORCH, UCGRA, UFFSW, UHMEA: 100m-buffer percentage estimates for various habitat components (e.g., coastal features, woodlands, meadow types, wetlands, etc.)
  - Total % of priority habitat: Percentage of the buffer classified as a priority habitat
  - % of SSSI: Percentage of the buffer classified as SSSI
- Data provenance and definitions are linked to:
  - Hill, M. O. (1996) TABLEFIT
  - Natural England (2013) Priority Habitats Inventory
  - Natural England (2014) SSSI boundaries
  - Ratcliffe (1977) Nature Conservation Review
  - Rodwell (1992) British Plant Communities: Grasslands and Montane Communities

## References
- Hill, M. O. (1996). TABLEFIT, Version 10, for Identification of Vegetation Types. Centre for Ecology and Hydrology, UK.
- Natural England. (2013). Priority Habitats Inventory (Single Habitats Layer) for England.
- Natural England. (2014). Sites of Special Scientific Interest and historical monuments.
- Ratcliffe, D. (1977). Nature Conservation Review. Cambridge University Press.
- Rodwell, J. S. (1992). British Plant Communities: Grasslands and Montane Communities. Cambridge University Press.