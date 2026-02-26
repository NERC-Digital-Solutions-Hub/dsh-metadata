# Fate of semi-natural grassland in England between 1960 and 2013: a test of national conservation policy

## Overview
- A dataset and methodology documenting changes in semi-natural grassland in England from 1960 to 2013 by linking historic survey data (1960–1981) with contemporary habitat data (2013).
- Aimed at informing national conservation policy and enabling consistent environmental health assessments over time.

## Data sources and survey details
- Historic quadrat data collected at grassland sites across England (1960–1981) with standardised methods.
- Some data contributed to the Nature Conservation Review (Ratcliffe, 1977) to identify key conservation areas.
- At each site, cover of vascular plant species was recorded from 2–6 randomly placed quadrats (mostly 1m x 1m; some 2m x 2m).
- Quadrat locations recorded with six-figure British National Grid references (spatial accuracy ~±100 m).
- Quadrats classified into British National Vegetation Classification (NVC) communities using TABLEFIT (Hill, 1996), then assigned to one of four grassland types:
  - Calcareous grassland (Lowland Calcareous Grassland; NVC CG1-9)
  - Lowland heath and dry acid grassland (Lowland Heath, NVC H1-H8)
  - Mesotrophic grassland (Lowland Meadows/Meadows; NVC MG1, MG3, MG4, MG5, MG6, MG9, MG10; including upland hay meadows)
  - Wet grassland (Purple Moor Grass and Rush Pastures; NVC M22-M26)
- Each grassland type linked to Biodiversity Action Plan (BAP) names and priority habitats; priority habitat status used for 2013 marine/inland context.

## Analytic methods and spatial processing
- Quadrat locations imported into ESRI ArcGIS v10.
- A 100 m buffer created around each quadrat to represent the corresponding grassland site, aligning with the ±100 m spatial accuracy.
- 2013 context defined using Natural England’s Priority Habitats Inventory (27 priority habitats under NERC Act 2006).
  - Calculated percentage of each buffered site that constitutes priority habitat (via Tabulate Intersection in Spatial Analyst).
- SSSI coverage within each buffered site calculated by intersecting with Natural England’s SSSI boundaries (2014 data).
- Outputs expressed as percentages of each site (quadrat + 100 m buffer) occupied by priority habitat and by SSSI.

## Dataset structure and key variables
- Core identifiers:
  - ID: unique quadrat identifier
  - Date: survey date (DD/MM/YYYY)
  - Easting / Northing: quadrat coordinates
  - Grassland category: Calcareous, Mesotrophic, Wet, or Lowland Heath and Dry Acid
  - NVC1: NVC group from TABLEFIT
  - SubCom1: Sub-community group from TABLEFIT
- Spatial context variables (percentages within 100 m buffer):
  - CFPGM, CSDUN, DWOOD, GQSIG, LCGRA, LDAGR, LFENS, LHEAT, LMEAD, LPAVE, MCSLP, MUDFL, PMGRP, RBEDS, TORCH, UCGRA, UFFSW, UHMEA
  - Total % of priority habitat
  - Percentage of buffer that is designated as an SSSI

## Outputs and intended use
- Enables consistent measurement of semi-natural grassland extent and its landscape context over time.
- Outputs suitable for reports, maps, and charts to monitor environmental health and policy performance.
- Datasets designed to be stored and uploaded to appropriate data portals for accessibility and reuse.

## Data quality, standards, and provenance
- Standardised data collection and classification methods (TABLEFIT; NVC).
- Spatial processing relies on ArcGIS v10 with a clearly defined 100 m representational buffer.
- Key references underlying classifications and data sources:
  - Hill, M. O. (1996). TABLEFIT (Version 10)
  - Natural England (2013). Priority Habitats Inventory
  - Natural England (2014). SSSI boundaries data
  - Ratcliffe (1977) Nature Conservation Review
  - Rodwell (1992). British Plant Communities: Grasslands and Montane Communities

## Practical challenges and considerations
- Balancing dataset value by integrating with additional data sources beyond the primary quadrat data.
- Facilitating access to underlying data to enable broader reuse and scrutiny of outputs.

## Relevance for Analysts Monitoring the Environment
- Demonstrates a rigorous, standardized approach to tracking environmental health indicators over time.
- Provides analyzable, policy-relevant metrics (priority habitat and SSSI overlap within defined buffer zones) aligned with national conservation priorities.
- Emphasizes data stewardship and interoperability through explicit data schema, provenance, and portal-ready outputs.