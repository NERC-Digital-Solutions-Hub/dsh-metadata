# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) standing crop biomass on salt marsh sites at Morecambe Bay and Essex

## Overview
- Dataset describing standing crop biomass (above-ground vegetation) on salt marsh sites at Morecambe Bay and Essex.
- Measurement: standing biomass inferred from clipping 50 cm × 25 cm patches, dried to determine biomass.
- Primary author/stew: Hilary Ford.
- Field campaigns conducted in winter and summer 2013.
- Sites chosen to represent contrasting soil types (clay in Essex, sandy in Morecambe Bay) and different grazing regimes.

## Spatial Coverage
- Essex
  - Abbotts Hall (AH) – 51°47'N, 0°52'E
  - Fingringhoe Wick (FW) – 51°49'N, 0°58'E
  - Tillingham Marshes (TM) – 51°41'N, 0°56'E
- Morecambe Bay
  - Cartmel Sands (CS) – 54°10'N, 3°0'W
  - Warton Sands (WS) – 54°8'N, 2°48'W
  - West Plain (WP) – location described for habitat comparison

## Temporal Coverage
- Winter (W) and Summer (S) seasons
- Observations collected during general field campaigns in 2013 (winter and summer)

## Data Content and Format
- Primary variable: Biomass (kg DW m^-2)
- Recording framework:
  - Field sampling area: 50 cm × 25 cm from each 1 m × 1 m quadrat
  - Processing: vegetation dried at 60°C for 72 hours
- File format: Excel workbook
- Per-quadrat data include:
  - Row Number (for sorting)
  - Season (Winter W, Summer S)
  - Location (Morecambe M, Essex E)
  - Site (CS, WS, WP; AH, FW, TM)
  - Habitat (Mudflat MF, Saltmarsh SM)
  - Quadrat Number (1–22)
  - Scale (A: 1 m; B: 1–10 m; C: 10–100 m; D: 100–upper limit)
  - Biomass (Kg DW m^-2)

## Sampling and Methodology
- Sampling frame: 1 m × 1 m quadrats; within each, a 50 cm × 25 cm patch was cut.
- Seasons sampled: winter and summer 2013
- Processing: drying to obtain standing crop biomass (60°C, 72 h)
- Grazing context varies by site (see location notes) and is relevant to interpretation of biomass

## Data Structure and Attributes
- Dataset fields include:
  - Row Number (numeric)
  - Season (Winter W or Summer S)
  - Location (Morecambe M or Essex E)
  - Site (CS, WS, WP for Morecambe; AH, FW, TM for Essex)
  - Habitat (Mudflat MF or Saltmarsh SM)
  - Quadrat Number (1–22)
  - Scale (A–D with defined extents)
  - Biomass (Kg DW m^-2)

## GIS and Analysis Considerations
- Data are field-derived biomass measurements suitable for creating spatial biomass maps across sites.
- Use site, habitat, and quadrat identifiers to join with spatial layers; scale categories aid in aggregation to different map resolutions.
- Coordinate data provided for each site enable integration with GIS coordinate systems (e.g., WGS84) for map-based visualizations.
- Differences in soil type and grazing regimes across sites can be explored as factors affecting biomass distribution.

## Quality, Limitations, and Notes
- Calibration procedures: None documented.
- Data quality checks: Not described.
- Data packaging considerations: Large or complex datasets may require careful structuring for GIS workflows.
- Temporal coverage is limited to two seasons within 2013; spatial and temporal extrapolations should be treated cautiously.

## Access and Contact
- Format: Excel workbook
- Primary contact: Hilary Ford (staff responsible)