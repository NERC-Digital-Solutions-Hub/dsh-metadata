# Fate of semi-natural grassland in England between 1960 and 2013: a test of national conservation policy

## Overview
- Study compares historic grassland survey data (1960–1981) with contemporary habitat data to quantify changes in semi-natural grassland in England (1960–2013) and assess implications for national conservation policy.

## Data sources
- Historic quadrat data collected at grassland sites (1960–1981) using standardized methods; some data used in the Nature Conservation Review (Ratcliffe, 1977).
- Quadrat details:
  - Location recorded as six-figure British National Grid references; spatial accuracy ±100 m.
  - Typically 1 m × 1 m quadrats (small number of 2 m × 2 m).
  - Vegetation in each quadrat classified into British National Vegetation Classification (NVC) communities using TABLEFIT (Hill, 1996).
  - Quadrat sites further classified into four grassland types based on BAP/NVC groupings (Calcareous, Lowland Heath and Dry Acid Grassland, Mesotrophic grassland, Wet grassland) with corresponding NVC communities and priority habitats.

## GIS processing workflow
- Location data imported into ESRI ArcGIS v10.
- 100 m buffer created around each quadrat to reflect spatial accuracy and represent a grassland site.
- 2013 cover of priority habitats mapped using Natural England’s Priority Habitats’ Inventory (PHI).
- For each buffered site, percent coverage of priority habitats calculated with Tabulate Intersection (Spatial Analyst).
- Percent of buffer designated as a Site of Special Scientific Interest (SSSI) computed by intersecting buffered sites with Natural England’s SSSI boundaries (digital data from 2014).

## Data schema and column definitions
- Key fields include:
  - ID: Unique quadrat identifier
  - Date: Quadrat survey date (DD/MM/YYYY)
  - Easting/Northing: Quadrat coordinates
  - Grassland category: Calcareous, Mesotrophic, Wet, or Lowland Heath and Dry Acid
  - NVC1 / SubCom1: NVC group and sub-community via TABLEFIT
  - Various habitat indicators within 100 m buffer (e.g., CFPGM, CSDUN, DWOOD, GQSIG, LCGRA, LDAGR, LFENS, LHEAT, LMEAD, LPAVE, MCSLP, MUDFL, PMGRP, RBEDS, TORCH, UCGRA, UFFSW, UHMEA)
  - Totals: Total % of priority habitat; Percentage of buffer classified as SSSI

## Analytical methods and outputs
- Computed, for each quadrat site (with 100 m buffer):
  - Percentage of buffer that constitutes priority habitat
  - Percentage of buffer that is within SSSI boundaries
- Results support mapping and analysis of spatial relationships between historic grassland quadrats and contemporary habitat designations.

## References and data provenance
- Hill, M. O. (1996). TABLEFIT, Version 10.
- Natural England (2013). Priority Habitats’ Inventory (Single Habitats’ Layer).
- Natural England (2014). Sites of Special Scientific Interest boundaries.
- Ratcliffe, D. (1977). Nature Conservation Review.
- Rodwell, J. S. (1992). British Plant Communities: Grasslands and Montane Communities.