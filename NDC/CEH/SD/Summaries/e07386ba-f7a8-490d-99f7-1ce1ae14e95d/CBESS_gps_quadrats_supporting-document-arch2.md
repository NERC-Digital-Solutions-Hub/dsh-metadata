# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) GPS locations of quadrats in saltmarsh and mudflat habitats

## Overview
- GPS locations and elevations for CBESS wave monitoring and sedimentation/erosion installations across six UK sites (three in Essex, three in Morecambe Bay).
- Each site includes 22 unmatted mudflat quadrats and 22 saltmarsh quadrats, with detailed spatial positioning to support environmental monitoring and policy evaluation.

## Sites and habitat context
- Essex (SE UK): Abbotts Hall, Fingringhoe Wick, Tillingham Marshes
  - Saltmarsh: predominantly clay soils
  - Mudflat: cohesive clays, mud, silt
- Morecambe Bay (NW UK): Cartmel Sands, Warton Sands, West Plain
  - Saltmarsh: sandy soils
  - Mudflat: coarse, mobile sediments
- Rationale: contrasting sediment types, inundation regimes, creek structures, and vegetation between regions.

## Data collection and parameters
- Timeframe: within two weeks before or during CBESS main campaigns in Winter and Summer 2013.
- Variables: Northing, Easting, Elevation (relative to Ordnance Datum Newlyn).
- Instrumentation: Leica GS08 GNSS; 50 mm 3D coordinate quality check; real-time Leica RTK corrections.

## Processing and data quality
- No subsequent processing beyond initial GPS locations recorded.
- Coordinates stored in OSGB1936(2); elevation in meters OD Newlyn.
- Data exported as ASCII text; duplicates cleaned in MS Excel; no additional transformations.
- NA values indicate measurements not performed.

## Dataset structure and field descriptions
- Each site includes 22 quadrats on mudflat and 22 on saltmarsh; quadrats are 1 m squares, oriented NS/EW, with SE corner coordinates recorded.
- Key fields include:
  - Season: Winter (W) or Summer (S)
  - Site: Essex (AH, FW, TM) or Morecambe (CS, WS, WP)
  - Habitat: Mudflat (MF) or Saltmarsh (SM)
  - Quadrat: 1–22
  - Scale: A (1 m), B (1–10 m), C (10–100 m), D (100–upper)
  - Easting, Northing, Elevation (m, OSGB66/OD Newlyn reference)
- Header and row structure defined to facilitate data sorting and integration.

## Access, use, and integration
- Data are provided as ASCII text with clear metadata about site, habitat, and measurement context.
- Suitable for mapping, spatial analysis, and cross-site comparisons within CBESS datasets.
- Should be stored in appropriate data portals and linked to related CBESS wave and sedimentation datasets for comprehensive environmental monitoring.

## Implications for environmental monitoring
- Establishes precise, regionally diverse baselines for saltmarsh and mudflat quadrats to support long-term monitoring of coastal biodiversity and ecosystem service sustainability.
- Enables standardized reporting and integration with other environmental health indicators and policy performance assessments.