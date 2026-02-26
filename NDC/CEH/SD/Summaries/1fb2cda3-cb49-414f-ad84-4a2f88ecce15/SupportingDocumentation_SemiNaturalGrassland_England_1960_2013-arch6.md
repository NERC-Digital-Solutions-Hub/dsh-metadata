# Fate of semi-natural grassland in England between 1960 and 2013: a test of national conservation policy

- Overview
  - A dataset created to quantify changes in semi-natural grassland in England from 1960–1981 (historic quadrat data) to 2013 (contemporary spatial data), comparing historic surveys with current habitat data to inform national conservation policy.

- Data sources and study design
  - Historic quadrat data (1960–1981): at each site, 2–6 randomly positioned 1m x 1m quadrats (a few sites used 2m x 2m); vascular plant cover recorded; quadrat locations captured as six-figure British National Grid references with ~±100 m spatial accuracy.
  - Quadrat classification: each quadrat vegetation assigned to a British National Vegetation Classification (NVC) community using TABLEFIT; aggregated into four grassland types and linked to Biodiversity Action Plan (BAP) names and Priority Habitats.
  - Grassland types and mappings:
    - Calcareous grassland (Lowland Calcareous Grassland; NVC CG1-9)
    - Lowland heath and dry acid grassland (Lowland Heath; NVC H1-H8)
    - Mesotrophic grassland (Meadow types; NVC MG1, MG3, MG4, MG5, MG6, MG9, MG10)
    - Wet grassland (Purple Moor-grass and rush pastures; NVC M22-M26)
  - Priority habitat and SSSI data used for 2013/2014 spatial context:
    - Natural England Priority Habitats Inventory (2013) for the geographic extent of 27 priority habitats.
    - Natural England SSSI boundaries (2014) for sites of Special Scientific Interest.

- Spatial data processing and analysis
  - For each quadrat, a 100 m buffer was generated in ArcGIS v10 to reflect the reported spatial accuracy and to define the associated site footprint.
  - Within-buffer habitat composition calculated by intersecting the 100 m buffer with Priority Habitats Inventory data (via Tabulate Intersection in Spatial Analyst).
  - SSSI proportion within each buffer computed by intersecting the 100 m buffer with Natural England SSSI boundaries.
  - Outputs express the percentage of each site’s buffer designated as each priority habitat and the percentage overlapping with SSSIs.

- Data structure and column definitions
  - ID: Unique quadrat identifier.
  - Date: Quadrat survey date (DD/MM/YYYY).
  - Easting/Northing: Quadrat location coordinates.
  - Grassland category: Designated grassland type (Calcareous, Mesotrophic, Wet, Lowland Heath and Dry Acid).
  - NVC1/SubCom1: NVC group and sub-community classification from TABLEFIT.
  - Habitat composition percentages within 100 m buffer (examples include CFPGM, CSDUN, DWOOD, GQSIG, LCGRA, LDAGR, LFENS, LHEAT, LMEAD, LPAVE, MCSLP, MUDFL, PMGRP, RBEDS, TORCH, UCGRA, UFFSW, UHMEA).
  - Total % of priority: Overall percentage of the buffer classified as priority habitat.
  - Percentage of buffer classified as a Site of Special Scientific Interest (SSSI).

- Data provenance and key references
  - TABLEFIT (Hill, 1996) for vegetation type identification.
  - Natural England Priority Habitats Inventory (2013) and SSSI boundaries (2014) for spatial context.
  - Foundational ecology references: Ratcliffe (1977) Nature Conservation Review; Rodwell (1992) British Plant Communities.

- Potential data use and value for end users
  - Enables temporal comparison of historic grassland presence with contemporary habitat contexts around survey sites.
  - Provides spatially explicit, queryable metrics of habitat overlap (priority habitats and SSSIs) around each quadrat site.
  - Supports policy evaluation and impact assessment by linking field-derived grassland data to current habitat designations and protected areas.
  - Facilitate data products (e.g., dashboards, reports) that allow stakeholders to explore habitat context around sites and to identify areas where data or conservation actions could be enhanced.