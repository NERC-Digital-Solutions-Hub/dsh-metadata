# Fate of semi-natural grassland in England between 1960 and 2013: a test of national conservation policy

## Overview
- A study quantifying changes in semi-natural grassland in England from 1960 to 2013 by contrasting historic survey data with contemporary habitat data.
- Reference: Ridding, Lucy E.; Redhead, John W.; Pywell, Richard F. (2015) in Global Ecology and Conservation.

## Data sources and scope
- Historic survey data (1960–1981) collected at grassland sites in England; some data also used in the Nature Conservation Review.
- Quadrat-based vegetation data: cover of vascular plant species recorded from 2–6 randomly placed 1m x 1m quadrats (some 2m x 2m).
- Quadrat locations: six-figure British National Grid references with an estimated spatial accuracy of ±100 m.
- Quadrat classification: each quadrat assigned to a British National Vegetation Classification (NVC) community using Tablefit; sites further categorized into four grassland types (calcareous, lowland heath and dry acid grassland, mesotrophic, wet grassland) with associated BAP names and NVC groups.
- Contemporary data: Natural England Priority Habitats Inventory (2013) for the distribution of 27 priority habitats; SSSI boundaries from Natural England (2014).

## Survey data details
- Grassland categories defined and mapped as Calcareous, Lowland Heath and Dry Acid, Mesotrophic, and Wet grasslands (with corresponding BAP names and NVC associations).
- NVC classification outcomes labeled as NVC group and Sub community group.
- Habitat context within each site is quantified using buffer statistics around each quadrat.

## Analytic methods
- Spatial processing in ESRI ArcGIS v10.
- A 100 m buffer created around each quadrat to represent the grassland site, matching the quadrat’s ±100 m positional accuracy.
- Percent cover within each buffer calculated for:
  - Priority Habitats (as per Natural England’s Priority Habitats Inventory) to indicate extent of priority habitats within the site.
  - SSSI status by intersecting with Natural England’s SSSI boundaries.
- Calculations performed using ArcGIS tools (e.g., tabulate intersection) to derive the percentage values for each site.

## Data schema and column headings
- Core fields include:
  - ID (unique quadrat identifier)
  - Date (survey date)
  - Easting / Northing (quadrant coordinates)
  - Grassland category (Calcareous, Mesotrophic, Wet, or Lowland Heath & Dry Acid)
  - NVC1 (NVC group from TABLEFIT)
  - SubCom1 (sub-community from TABLEFIT)
  - Various buffer-based habitat percentages (e.g., coastal & floodplain grazing marsh, lowland calcareous grassland, lowland dry acid grassland, lowland fens, lowland meadows, purple moor grass pastures, etc.)
  - Total % of priority habitat within the buffer
  - Percentage of buffer classified as SSSI
- This structure links historic quadrat data to modern habitat context and protection status.

## Data integration and quality considerations
- Spatial alignment between historic field data and modern habitat datasets achieved via 100 m site buffers.
- Data sources include established vegetation classification (TABLEFIT), Natural England Priority Habitats Inventory, and SSSI boundaries to contextualize grassland sites within current conservation priorities.
- Metadata and definitions provided for column headings to ensure clarity and reusability across analyses.

## References
- Hill, M. O. (1996). TABLEFIT, Version 10. Centre for Ecology and Hydrology.
- Natural England (2013). Priority Habitats Inventory (Single Habitats Layer) for England, Version 1.1.
- Natural England (2014). Sites of Special Scientific Interest and historical monuments.
- Ratcliffe, D. (1977). Nature Conservation Review.
- Rodwell, J. S. (1992). British Plant Communities: Grasslands and Montane Communities.