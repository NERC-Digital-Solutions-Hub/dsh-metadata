# Fate of semi-natural grassland in England between 1960 and 2013: a test of national conservation policy

- Overview
  - A study comparing historic grassland survey data (1960–1981) with contemporary spatial data (2013) to quantify changes in semi-natural grassland across England and to test national conservation policy. References include Ridding et al. (2015).

- Data sources and scope
  - Historic quadrat data collected at grassland sites in England (1960–1981) with standardised methods.
  - Some quadrat data used in the Nature Conservation Review (Ratcliffe, 1977).
  - Quadrat locations recorded by six-figure British National Grid references with an accuracy of about ±100 m.
  - Quadrat vegetation assigned to British National Vegetation Classification (NVC) groups using TABLEFIT (Hill, 1996).
  - Quadrat sites classified into four grassland types based on NVC and biodiversity targets:
    - Calcareous grassland (Lowland calcareous grassland; BAP; NVC CG1-9)
    - Lowland heath and dry acid grassland (Lowland dry acid grassland; NVC H1-H8)
    - Mesotrophic grassland (Lowland meadows; NVC MG1, MG3, MG4, MG5, MG6, MG9, MG10)
    - Wet grassland (Purple moor-grass and rush pastures; NVC M22-M26)
  - Contemporary coverage represented by Natural England’s Priority Habitats Inventory (2013) for principal importance habitats.
  - SSSI coverage derived from Natural England digital SSSI boundary data (2014).

- Analytic methods and data processing
  - Spatial processing in ArcGIS v10.
  - A 100 m buffer around each quadrat (to reflect the quadrat’s ±100 m location accuracy) used to define a grassland site.
  - Percentages of priority habitats within each buffered site calculated via tabulate intersection (Spatial Analyst toolbox).
  - Percentages of the site that fall within SSSIs calculated by intersecting buffered sites with Natural England’s SSSI boundaries.
  - Column definitions describe each variable (IDs, dates, grid references, grassland category, NVC/sub-community classifications, and percentages for various habitat types within the 100 m buffer).

- Data structure and key columns (examples)
  - ID: Unique quadrat identifier.
  - Date: Quadrat survey date.
  - GridRef: Quadrat location reference.
  - Grassland category: Calcareous, Mesotrophic, Wet, or Lowland Heath and Dry Acid.
  - NVC1/SubCom1: NVC group and sub-community classification (via TABLEFIT).
  - Habitat percentage columns: e.g., CFPGM (coastal & floodplain grazing marsh), CSDUN (coastal sand dunes), DWOOD (deciduous woodland), GQSIG (good quality semi-improved grassland), LCGRA (lowland calcareous grassland), LDAGR (lowland dry acid grassland), LFENS (lowland fens), LHEAT (lowland heathland), LMEAD (lowland meadows), PMGRP (purple moor-grass and rush pastures), UCGRA (upland calcareous grassland), UHMEA (upland hay meadow), plus Total % of priority habitat and % of SSSI.

- Outputs and potential data products
  - Site-level summaries of historic grassland types versus 2013 habitat coverage.
  - Quantified exposure of sites to priority habitats and SSSIs within 100 m buffers.
  - Data suitable for dashboards or self-serve exploration to assess changes in semi-natural grassland and alignment with conservation priorities.

- Key considerations, challenges, and limitations
  - Time gap: historic data (1960–1981) versus 2013 habitat data; potential changes in survey methods over time.
  - Data quality: patchy historic data and varying quadrat sizes (mostly 1 m x 1 m; some 2 m x 2 m).
  - Location accuracy: ±100 m accuracy necessitates buffer-based aggregation to define site extents.
  - Complex communications: translating NVC classifications and habitat types into actionable conservation outputs.

- References
  - Hill, M. O. (1996). TABLEFIT, Version 10, Identification of Vegetation Types.
  - Natural England (2013). Priority Habitats Inventory (Single Habitats’ Layer), Version 1.1.
  - Natural England (2014). Sites of Special Scientific Interest boundary data.
  - Ratcliffe, D. (1977). Nature Conservation Review.
  - Rodwell, J. S. (1992). British Plant Communities: Grasslands and Montane Communities.
  - Ridding, L. E.; Redhead, J. W.; Pywell, R. F. (2015). Fate of semi-natural grassland in England between 1960 and 2013: a test of national conservation policy. Global Ecology and Conservation, 4, 516-525.