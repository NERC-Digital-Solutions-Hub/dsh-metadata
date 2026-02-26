# Fate of semi-natural grassland in England between 1960 and 2013: a test of national conservation policy

## Overview
- Datasets created to quantify changes in semi-natural grassland across England from 1960 to 2013 by comparing historic survey data with contemporary habitat data.
- Supports a test of national conservation policy framework (Ridding et al. 2015; Global Ecology and Conservation).
- Spatially explicit: historic quadrat observations linked to geographic locations with estimated accuracy of ±100m.

## Data sources and survey design
- Historic quadrat data collected at grassland sites in England (1960–1981) using standardized methods.
- Some data contributed to the Nature Conservation Review (Ratcliffe, 1977).
- At each site, vascular plant cover recorded from 2–6 randomly placed 1m x 1m quadrats (some 2m x 2m).
- Quadrat locations recorded as six-figure British National Grid references (±100m accuracy).
- Quadrat vegetation assigned to British National Vegetation Classification (NVC) communities (Tablefit used for classification).
- Quadrat sites further classified into one of four grassland types based on NVC groups and BAP/priority habitat associations:
  - Calcareous grassland (Lowland calcareous grassland; NVC CG1-9)
  - Lowland heath and dry acid grassland (Lowland Dry Acid Grassland; NVC H1-H8)
  - Mesotrophic grassland (Lowland meadows; NVC MG1, MG3, MG4, MG5, MG6, MG9, MG10)
  - Wet grassland (Purple moor-grass and rush pastures; NVC M22-M26)

## GIS processing and 2013 comparison
- Quadrat locations imported into ESRI ArcGIS v10.
- A 100m buffer created around each quadrat to represent the associated grassland site (matching location accuracy).
- 2013 grassland extent derived from Natural England’s Priority Habitats Inventory (PHI; Actively used to show habitats of principal importance across England).
- Percentage of priority habitat within each quadrat site buffer calculated via tabulate intersection (Spatial Analyst).
- Percentage of buffer designated as SSSI calculated by intersecting grassland sites with Natural England’s SSSI boundaries (digital data, 2014).

## Data fields (column headings)
- ID: Unique identifier for each quadrat.
- Date: Date of quadrat survey (DD/MM/YYYY).
- GridRef: Quadrat location grid reference.
- Grassland category: Designated grassland type (Calcareous, Mesotrophic, Wet, Lowland Heath and Dry Acid).
- NVC1: NVC group derived from TABLEFIT.
- SubCom1: Sub-community group derived from TABLEFIT.
- CFPGM, CSDUN, DWOOD, GQSIG, LCGRA, LDAGR, LFENS, LHEAT, LMEAD, LPAVE, MCSLP, MUDFL, PMGRP, RBEDS, TORCH, UCGRA, UFFSW, UHMEA: Percentages of various habitat components within the 100m buffer (e.g., coastal & floodplain grazing marsh, dunes, woodland, good quality semi-improved grassland, lowland calcareous grassland, etc.).
- Total % of priority habitat: Percentage of the buffer classified as a priority habitat.
- %of SSSI: Percentage of the buffer classified as a Site of Special Scientific Interest.

## References
- Hill, M. O. (1996). TABLEFIT, Version 10, for Identification of Vegetation Types. UK: Centre for Ecology and Hydrology.
- Natural England (2013). Priority Habitats Inventory (Single Habitats’ Layer) for England, Version 1.1.
- Natural England (2014). Sites of Special Scientific Interest and historic monuments.
- Ratcliffe, D. (1977). Nature Conservation Review.
- Rodwell, J. S. (1992). British Plant Communities: Grasslands and Montane Communities.