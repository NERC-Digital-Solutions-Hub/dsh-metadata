# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) standing crop biomass on salt marsh sites at Morecambe Bay and Essex

## Overview
- Dataset measures standing crop biomass (kg DW m^-2) as an environmental health indicator within coastal ecosystems.
- Focuses on saltmarsh habitats at six sites across Essex and Morecambe Bay.
- Data collected during Winter and Summer 2013 using standardized vegetation sampling and drying methods.

## Study sites and context
- Essex sites: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
- Morecambe Bay sites: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP).
- Geographic coordinates:
  - Essex: AH 51.78°N, 0.87°E; FW 51.82°N, 0.97°E; TM 51.68°N, 0.93°E.
  - Morecambe Bay: CS 54.17°N, 3.00°W; WS 54.13°N, 2.80°W; WP (location not fully specified in excerpt).
- Habitat and soil contrasts:
  - Essex: clay soils, higher inundation with hare grazing and Brent geese grazing.
  - Morecambe Bay: sandy soils, intensive sheep grazing and geese grazing patterns; West Plain lightly grazed.
- Purpose of site selection: represent contrasting soil types, inundation regimes, and grazing pressures to examine biomass dynamics.

## Sampling design and field methods
- Sampling period: Winter and Summer 2013.
- Plot design: 50 cm × 25 cm sampling area within each 1 m × 1 m quadrat; biomass dried to measure standing crop.
- Processing: vegetation dried at 60°C for 72 hours to obtain dry weight biomass.
- Replication: each site uses 22 quadrats (Quadrat Numbers 1–22).
- Scale coding: data include Scale categories (A, B, C, D) corresponding to different spatial extents (A = 1 m, B = 1–10 m, C = 10–100 m, D = 100 m to upper limit).

## Variables and data structure
- Core variable: Biomass (Kg DW m^-2).
- Dataset fields (Dataset Field descriptions):
  - Row Number: sortable index (numeric).
  - Season: Winter (W) or Summer (S).
  - Location: Morecambe (M) or Essex (E).
  - Site: CS, WS, WP (Morecambe); AH, FW, TM (Essex).
  - Habitat: Mudflat (MF) or Saltmarsh (SM).
  - Quadrat Number: 1–22 (numeric).
  - Scale: A, B, C, D (text).
  - Biomass: numeric (Kg DW m^-2).
- Data format: Excel workbook.

## Data quality, documentation, and governance
- Calibration procedures: none noted.
- Quality control: explicit procedures not described in the excerpt.
- Metadata: dataset includes site coordinates, habitat, grazing context, and seasonal sampling, but some metadata (e.g., WP coordinates or full QA steps) are not detailed here.
- Data accessibility: stored as an Excel workbook; considerations for public sharing of underlying data may apply, aligned with monitoring framework concerns about data openness and governance.
- Data provenance: staff responsible for data collection is Hilary Ford.

## Relevance for Monitoring Frameworks
- Provides a concrete, field-derived metric (standing crop biomass) across contrasting coastal habitats and grazing regimes, useful for trend analysis and policy evaluation in environmental health monitoring.
- Demonstrates a clear linkage between habitat type, soil characteristics, grazing pressure, and biomass outcomes, aiding in the design of targeted monitoring programs.
- The structured data layout (site, habitat, season, quadrat, biomass) supports aggregation, trend detection, and inter-site comparisons.

## Limitations and considerations for future monitoring
- Temporal scope is limited to Winter and Summer 2013; longer time series would improve trend detection and policy relevance.
- Calibration and QA details are not specified; integrating QA steps would enhance data reliability for monitoring frameworks.
- Some metadata gaps (e.g., full WP coordinates, detailed data governance and sharing terms) may hinder data reuse and cross-program integration.
- Potential barriers to data sharing in practice should be anticipated and addressed through governance processes and metadata enhancement.