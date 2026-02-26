# Fate of semi-natural grassland in England between 1960 and 2013: a test of national conservation policy

## Overview
- A study comparing historic grassland survey data (1960–1981) with contemporary spatial data (2013) to quantify changes in semi-natural grassland across England.
- Aimed to test national conservation policy by linking field survey data with modern habitat inventories.

## Data sources

- Historic quadrat data (1960–1981) collected at grassland sites in England using a standardized method.
  - Quadrat locations recorded to six-figure British National Grid with an approximate spatial accuracy of ±100 m.
  - At each site, vascular plant cover was recorded in 2–6 randomly positioned 1 m × 1 m (mostly) quadrats; some sites used 2 m × 2 m quadrats.
  - Some data contributed to the Nature Conservation Review (Ratcliffe, 1977).

- Quadrat classification and grassland types
  - Quadrat vegetation assigned to British National Vegetation Classification (NVC) communities using TABLEFIT (Hill, 1996).
  - Quadrat sites further classified into grassland types based on BAP/nomenclature: Calcareous, Lowland Heath & Dry Acid, Mesotrophic, and Wet grassland, with detailed mapping to NVC groups and priority habitats (e.g., Lowland Calcareous Grassland, Lowland Dry Acid Grassland, Lowland Meadows, Purple Moor Grass and Rush Pastures).

- Contemporary spatial data
  - Natural England's Priority Habitats Inventory (2013): geographic extent and locations of 27 Priority Habitats (NERC Act 2006) across England.

- Boundary and site data for overlap analysis
  - Natural England's digital boundary data for Sites of Special Scientific Interest (SSSIs) (2014).

## Survey data details

- Quadrats and sites
  - Each quadrat site has an ID, survey date, and coordinates (Eastings/Northings).
  - Grassland category codes include Calcareous, Mesotrophic, Wet, and Lowland Heath & Dry Acid.
  - NVC group and SubCommunity group fields derived from TABLEFIT.

- Habitat and landscape context attributes (buffer analysis)
  - Percent cover within a 100 m buffer around each quadrat (to represent the site, matching the ±100 m spatial accuracy).
  - Variables include percentages for various habitat/land-cover components within the buffer (e.g., coastal & floodplain grazing marsh, dunes, deciduous woodland, good quality semi-improved grassland, Lowland Calcareous Grassland, Lowland Dry Acid Grassland, Lowland Fens, Lowland Heathland, Lowland Meadows, Purple Moor Grass & Rush Pastures, upland calcareous grassland, etc.).
  - Overall metrics: Total % of buffer classified as priority habitat and the percentage of the buffer that is within an SSSI.

## Analytical methods

- Spatial processing
  - Location data imported into ESRI ArcGIS v10.
  - Generated a 100 m buffer around each quadrat to represent a grassland site given localization accuracy.

- Habitat overlap calculations
  - Priority Habitats overlap: Tabulate Intersection (Spatial Analyst) to compute the percentage of each buffered site that falls within Priority Habitats Inventory.
  - SSSI overlap: Intersect buffered sites with Natural England’s SSSI boundaries (2014) to obtain the percentage of each site classified as an SSSI.

## Column headings and variables

- Core identifiers and metadata
  - ID: Unique quadrat identifier
  - Date: Survey date (DD/MM/YYYY)
  - Easting/Northing: Quadrat location coordinates

- Grassland classification
  - Grassland category: Calcareous, Mesotrophic, Wet, Lowland Heath & Dry Acid
  - NVC1: NVC group from TABLEFIT
  - SubCom1: Sub-community group from TABLEFIT

- Landscape/habitat composition (percentages within 100 m buffer)
  - CFPGM, CSDUN, DWOOD, GQSIG, LCGRA, LDAGR, LFENS, LHEAT, LMEAD, LPAVE, MCSLP, MUDFL, PMGRP, RBEDS, TORCH, UCGRA, UFFSW, UHMEA
  - Each field represents the percentage of the 100 m buffer classified as the corresponding habitat/land-cover type

- Totals
  - Total % of priority: Percentage of the buffer classified as any priority habitat
  - Percentage of buffer classified as a Site of Special Scientific Interest (SSSI)

## Data preparation and workflow

- Reconciliation of historic quadrat data with modern habitat layers by:
  - Assigning each quadrat to a site via a 100 m buffer
  - Assessing contemporary habitat extent within buffers using Priority Habitats Inventory
  - Assessing protection status within buffers using SSSI boundaries
- Documentation and provenance
  - Data fields and codes defined to enable reproducibility and cross-checking against the underlying TABLEFIT classifications and habitat inventories.
- Key methodological references
  - TABLEFIT (Hill, 1996) for vegetation type identification
  - Natural England Priority Habitats Inventory (2013)
  - Natural England SSSI boundaries (2014)
  - Ratcliffe (1977), Rodwell (1992) as foundational classifications

## References

- Hill, M. O. (1996). TABLEFIT, Version 10, Identification of Vegetation Types. Centre for Ecology and Hydrology, UK.
- Natural England (2013). Priority Habitats Inventory (Single Habitats Layer) for England, Version 1.1.
- Natural England (2014). Sites of Special Scientific Interest boundaries.
- Ratcliffe, D. (1977). Nature Conservation Review. Cambridge University Press.
- Rodwell, J. S. (1992). British Plant Communities: Grasslands and Montane Communities. Cambridge University Press.