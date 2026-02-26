# Fate of semi-natural grassland in England between 1960 and 2013: a test of national conservation policy

- Purpose and scope
  - Quantified changes in semi-natural grassland across England from 1960 to 2013 by comparing historic grassland survey data with contemporary spatial habitat data.
  - Aimed to inform national conservation policy and assess policy effectiveness.

- Survey data and sampling design
  - Historic quadrat data collected at grassland sites in England between 1960 and 1981 using a standardised methodology.
  - Some data contributed to the Nature Conservation Review (Ratcliffe, 1977).
  - At each site: cover of vascular plant species recorded from 2–6 randomly placed square quadrats (mostly 1m x 1m; some 2m x 2m).
  - Quadrat locations recorded with six-figure British National Grid references (spatial accuracy ±100 m).
  - Quadrat vegetation assigned to British National Vegetation Classification (NVC) communities using TABLEFIT (Hill, 1996).
  - Quadrat sites further classified into four grassland types: Calcareous grassland, Lowland heath and dry acid grassland, Mesotrophic grassland, and Wet grassland, linked to Biodiversity Action Plan (BAP) names and NVC groups.

- Analytic methods and spatial analysis
  - Quadrat locations imported into ESRI ArcGIS v10.
  - 100 m buffer created around each quadrat to represent grassland site with spatial accuracy alignment.
  - 2013 grassland extent determined using Natural England’s Priority Habitats Inventory (PHI) for habitats of principal importance (NERC Act 2006).
  - Percentage of each buffer classified as priority habitat calculated using tabulate intersection in Spatial Analyst.
  - Percentage of each buffer that intersects Sites of Special Scientific Interest (SSSI) calculated using Natural England’s digital SSSI boundaries.

- Dataset structure and key variables
  - Distance and location: Date; Easting; Northing.
  - Land cover and classification: Grassland category (Calcareous, Mesotrophic, Wet, Lowland Heath and Dry Acid); NVC group (NVC1); Sub community (SubCom1).
  - Habitat composition within 100 m buffer (percentages): CFPGM (coastal & floodplain grazing marsh), CSDUN (coastal sand dunes), DWOOD (deciduous woodland), GQSIG (good quality semi-improved grassland), LCGRA (lowland calcareous grassland), LDAGR (lowland dry acid grassland), LFENS (lowland fens), LHEAT (lowland heathland), LMEAD (lowland meadows), LPAVE (limestone pavements), MCSLP (maritime cliff and slope), MUDFL (mudflats), PMGRP (Purple Moor Grass and Rush Pastures), RBEDS (reed beds), TORCH (traditional orchards), UCGRA (upland calcareous grassland), UFFSW (upland flushes, fens and swamps), UHMEA (upland hay meadow).
  - Summary habitat metrics: Total % of buffer classified as a priority habitat; Percentage of buffer classified as SSSI.
  - Data source and references: TABLEFIT (Hill, 1996) for vegetation typing; Natural England PHI (2013); Natural England SSSI data (2014); Nature Conservation Review (Ratcliffe, 1977); Rodwell (1992) NVC references.

- Data provenance and references
  - Primary data from historic grassland surveys (1960–1981) used in the Nature Conservation Review.
  - Contemporary habitat data drawn from Natural England’s Priority Habitats Inventory (2013) and SSSI boundary data (2014).
  - Vegetation typing and classification supported by TABLEFIT (Hill, 1996) and NVC framework (Rodwell, 1992).