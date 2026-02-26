# Fate of semi-natural grassland in England between 1960 and 2013: a test of national conservation policy

## Overview
- A study linking historic grassland survey data (1960–1981) with contemporary spatial data to quantify changes in semi-natural grassland in England (1960–2013) and to test national conservation policy.
- Data are intended to support assessments of habitat extent, conservation status, and policy effectiveness across England.

## Data Collection

- Historic quadrat data collected at grassland sites in England (1960–1981) using standardized methods.
- At each site, cover of vascular plant species recorded from 2–6 randomly placed quadrats, mostly 1m x 1m (some 2m x 2m).
- Quadrat locations given as six-figure British National Grid references with an estimated spatial accuracy of ±100 m.
- Quadrat vegetation assigned to British National Vegetation Classification (NVC) communities using TABLEFIT, then grouped into one of four grassland types:
  - Calcareous grassland (Lowland Calcareous Grassland; NVC CG1–CG9)
  - Lowland heath and dry acid grassland
  - Mesotrophic grassland
  - Wet grassland
- Each quadrat site categorized into NVC/subcommunity groups and linked to BAP habitat categories.

## Data Processing and Analysis

- Quadrat locations imported into ESRI ArcGIS v10; a 100 m buffer created around each quadrat to represent the site (matching spatial accuracy).
- 2013 representation of seminatural grassland derived from Natural England’s Priority Habitats Inventory (PHI) for 27 habitat types.
- For each site (quadrat + 100 m buffer), calculate:
  - Percentage of buffer area classified as each priority habitat (PHI overlap via tabulate intersection).
  - Percentage of buffer area designated as a Site of Special Scientific Interest (SSSI) using Natural England’s SSSI boundaries.
- The dataset combines historic survey data with contemporary habitat and protection layers to enable landscape-scale analyses.

## Dataset Structure and Metadata

- Core columns and descriptions include:
  - ID: Unique quadrat identifier
  - Date: Quadrat survey date
  - GridRef: Quadrat grid reference
  - Grassland category: Calcareous, Mesotrophic, Wet, or Lowland Heath/Dry Acid
  - NVC1: NVC group from TABLEFIT
  - SubCom1: Sub-community from TABLEFIT
  - Habitat overlap percentages within 100 m buffer for various habitat components (e.g., CFPGM, CSDUN, DWOOD, GQSIG, LCGRA, LDAGR, LFENS, LHEAT, LMEAD, LPAVE, MCSLP, MUDFL, PMGRP, RBEDS, TORCH, UCGRA, UFFSW, UHMEA)
  - Total % of priority habitat within buffer
  - % of buffer classified as SSSI
- Data sources and references used for classification and spatial overlays:
  - Hill (1996) TABLEFIT v10
  - Natural England Priority Habitats’ Inventory (2013)
  - Natural England SSSI boundaries (2014)
  - Ratcliffe (1977) Nature Conservation Review
  - Rodwell (1992) British Plant Communities: Grasslands and Montane Communities

## Provenance and References

- Primary dataset provenance from historic grassland surveys (1960–1981) and derived classifications (NVC via TABLEFIT).
- Spatial overlays rely on:
  - Natural England Priority Habitats Inventory (2013)
  - Natural England SSSI boundaries (2014)
- Foundational taxonomic and vegetation classification references:
  - Ratcliffe, 1977; Rodwell, 1992; Hill, 1996

## Data Quality, Limitations, and Governance

- Quality considerations:
  - Spatial accuracy of quadrat locations is ±100 m; buffering to 100 m aligns with this accuracy.
  - Historic data use variable quadrat sizes and may introduce heterogeneity (predominantly 1 m x 1 m; some 2 m x 2 m).
  - NVC assignment depends on TABLEFIT methodology; classifications may carry inherent uncertainties.
- Limitations:
  - Temporal mismatch between historic field data (1960–1981) and contemporary PHI/SSSI layers (circa 2013–2014) for overlap analyses.
  - Potential biases related to data collection timing, site selection, and habitat classification granularity.
- Governance and stewardship considerations:
  - Clear metadata should be maintained (data provenance, methods, and transformation steps).
  - Document data quality checks, uncertainties, and assumptions (e.g., buffer rationale, spatial alignment).
  - Manage updates and interoperability across systems (historic survey data, NVC classifications, PHI, and SSSI layers).
  - Address sharing limitations, licensing, and attribution per original data sources and software tools used (TABLEFIT, ArcGIS).

## Reuse and Access Considerations

- Suitable for policy evaluation, conservation planning, and habitat-change analyses across England.
- Enables reproducible comparisons between historical grassland surveys and current habitat distributions.
- Users should reference the original study (Ridding et al., 2015) and acknowledge data sources (TABLEFIT, PHI, SSSI boundaries, NVC classifications) when reusing the dataset.