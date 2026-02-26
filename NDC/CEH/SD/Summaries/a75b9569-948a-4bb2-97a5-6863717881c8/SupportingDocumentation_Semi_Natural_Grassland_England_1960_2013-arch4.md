# Fate of semi-natural grassland in England between 1960 and 2013: a test of national conservation policy

## Overview
- Study quantifies changes in semi-natural grassland in England by linking historic grassland survey data (1960–1981) with contemporary spatial data (2013) on habitats.
- Combines field quadrat data with national habitat inventories to assess conservation policy implications.

## Data sources and scope
- Historic data (1960–1981): Quadrat-based vegetation surveys at grassland sites, with 2–6 randomly placed 1m x 1m quadrats (some 2m x 2m); location recorded as six-figure grid references with ±100m spatial accuracy.
- Classification: Quadrat vegetation assigned to British National Vegetation Classification (NVC) groups using TABLEFIT; sites subsequently categorized into four grassland types:
  - Calcareous grassland (Lowland calcareous grassland; NVC CG1–CG9)
  - Lowland heath and dry acid grassland (NVC H1–H8)
  - Mesotrophic grassland (NVC MG1, MG3, MG4, MG5, MG6, MG9, MG10)
  - Wet grassland (NVC M22–M26)
- Contemporary data (2013): Natural England’s Priority Habitats Inventory (PHI) for habitat extent and location; SSSI boundaries for Site of Special Scientific Interest.
- Data integration target: quantify the share of each site (quadrat with a 100m buffer) occupied by priority habitats and SSSIs.

## Analytic methods and workflow
- Spatial processing:
  - Import quadrat locations into ArcGIS v10.
  - Generate a 100m buffer around each quadrat to represent a grassland site (matching location accuracy).
  - Intersect buffers with PHI to compute the percentage of each site that is Priority Habitat.
  - Intersect buffers with SSSI boundaries to compute the percentage of each site designated as SSSI.
- Data synthesis:
  - Use tabulate intersection to calculate percentages of various habitat components within each 100m buffer.
  - Build a site-level profile combining historic quadrat data with contemporary habitat designations.

## Data model and column headings
- Unique ID and basic metadata:
  - ID, Date, GridRef
  - Grassland category (Calcareous, Mesotrophic, Wet, or Lowland Heath and Dry Acid)
  - NVC group (NVC1) and SubCommunity (SubCom1) from TABLEFIT
- Habitat component percentages within 100m buffer (example fields):
  - CFPGM, CSDUN, DWOOD, GQSIG, LCGRA, LDAGR, LFENS, LHEAT, LMEAD, LPAVE, MCSLP, MUDFL, PMGRP, RBEDS, TORCH, UCGRA, UFFSW, UHMEA
- Summary habitat measures:
  - Total % of priority habitat within buffer
  - % of buffer classified as SSSI
- These fields collectively enable a site-level view of historic grassland classification alongside current habitat status and protections.

## Outputs and implications for data leadership
- Produces an integrated, geospatially anchored dataset linking historic grassland surveys to current habitat protections, enabling assessment of policy effectiveness over time.
- Facilitates:
  - Data governance through standardized methods (TABLEFIT classification, consistent buffering, standardized overlays)
  - Documentation of data lineage and metadata (unique IDs, dates, grid references)
  - Discoverability via explicit column definitions and references to authoritative inventories (PHI, SSSI)
  - Reproducibility and potential reuse for other policy evaluations or comparative landscape studies

## References and methodologies
- TABLEFIT (Hill, 1996) for vegetation type identification
- Priority Habitats Inventory (Natural England, 2013)
- SSSI boundaries (Natural England, 2014)
- Nature Conservation Review (Ratcliffe, 1977)
- British Plant Communities: Grasslands (Rodwell, 1992)