# Dry weight root biomass from three soil depths on salt marsh sites at Morecambe Bay and Essex

## Overview
- Dataset capturing root biomass (kgDW m^-2) across three soil depth intervals (0–10 cm, 10–20 cm, 20–30 cm) in saltmarsh quadrats during Winter and Summer 2013.
- Staff responsible: Hilary Ford.
- Part of the CBESS field campaign; Essex winter sampling also occurred 2–6 March 2013; no planned repeat sampling.

## Sampling design and methods
- Sample collection: one large sediment core per 1 × 1 m quadrat (diameter ~16 cm, depth 30 cm) including soil, intact roots, and above-ground vegetation.
- Depths measured: 0–10 cm, 10–20 cm, 20–30 cm; biomass dried at 60°C for 72 hours and weighed.
- Conversion: raw measurements converted to total root biomass for 0–30 cm (kgDW m^-2).
- Quadrat layout: twenty-two 1 × 1 m quadrats per site rectangle, randomly allocated; sites defined rectangles ranging approximately 400 × 500 m to 1000 × 1000 m, encompassing low, mid, and high marsh zones.
- Spatial scaling: four different spatial scales described (A: 1 quadrat; B: 3 quadrats at 1–10 m apart; C: 6 quadrats; D: 2, etc. – factorial description appears garbled but indicates multiple quadrat configurations).
- Calibration and quality: scales calibrated per laboratory protocols; data quality checks included entering scale readings into spreadsheets and screening for outliers.

## Locations and sites
- Essex sites (clay soils; southeastern Atlantic UK):
  - Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM)
  - Coordinates provided for each site
  - Grazing and vegetation context: hare-grazed; Abbotts Hall and Fingringhoe Wick heavily grazed by overwintering Brent geese.
- Morecambe Bay sites (sandy soils; west UK):
  - Cartmel Sands (CS), Warton Sands (WS), West Plain (WP)
  - Coordinates provided for each site
  - Grazing and vegetation context: intensive sheep grazing; pink-footed geese graze in winter; West Plain lightly grazed.
- Site selection aimed to contrast soil type (clay vs sand) and inundation, creek structure, and vegetation, influencing root biomass patterns.

## Data structure and contents
- Primary variable: Root biomass (kg DW m^-2) for each depth (RB_0-10, RB_10-20, RB_0-30).
- Total root biomass: Total Root biomass (0–30 cm) kg DW m^-2 (sum of the three depth measurements).
- File format: Comma separated values (.csv).
- Dataset fields and examples:
  - Season (Winter or Summer)
  - Location (M for Morecambe, E for Essex)
  - Site (CS, WS, WP, AH, FW, TM)
  - Habitat (Saltmarsh, Mudflat)
  - Quadrat Number (1–22)
  - Scale (A–D; descriptions include A=1 m, B=1–10 m, C=10–100 m, D=upper limit)
  - RB_0-10, RB_10-20, RB_0-30 (root biomass values)
  - Row Number (sorting/ordering code)
- Data notes:
  - Some blank cells indicate missing data due to loss of samples during processing.
  - Dataset documentation includes header and cell format descriptors.

## Quality assurance, limitations, and governance
- Quality control: data entries checked in spreadsheets; outliers screened.
- Missing data: blanks due to sample loss; not all combinations have complete data.
- Reproducibility: clearly documented methodology enabling replication of biomass measurements and conversions.
- Scope and updates: no repeat sampling planned; dataset reflects Winter and Summer 2013 field campaigns with an additional Essex winter sampling window.

## Governance and provenance considerations for Data Stewards
- Provenance: dataset stems from a defined CBESS field campaign with explicit sampling window(s) and processing steps.
- Metadata completeness: detailed field descriptions, site codes, coordinates, habitat, quadrat and scale coding, and unit definitions (kgDW m^-2) support discoverability and reuse.
- Standardization: consistent units (dry weight) and depth intervals; explicit conversion procedures (from core biomass to per-area biomass).
- Data sharing readiness: structured CSV with explicit field descriptions and coding, facilitating integration into data portals and catalogues.
- Limitations awareness: note missing data due to sample loss; interpret total and depth-specific biomass with caveats where data are incomplete.