# Dry weight root biomass from three soil depths on salt marsh sites at Morecambe Bay and Essex.

## Overview
- Dataset of root biomass (kg DW per m^2) for three soil depth intervals (0-10 cm, 10-20 cm, 20-30 cm).
- Sites span two regions: Essex (saltmarsh) and Morecambe Bay (saltmarsh), sampled in Winter and Summer 2013.
- Essex winter sampling occurred 2–6 March 2013; other samples were collected during the CBESS field campaign.

## Locations and site descriptions
- Essex
  - Abbotts Hall (AH) – 51.783°N, 0.8667°E
  - Fingringhoe Wick (FW) – 51.8167°N, 0.9667°E
  - Tillingham Marshes (TM) – 51.6833°N, 0.9333°E
- Morecambe Bay
  - Cartmel Sands (CS) – 54.1667°N, 3.0000°W
  - Warton Sands (WS) – 54.1333°N, 2.8000°W
  - West Plain (WP) – 54.1500°N, 2.9667°W
- Habitat players the saltmarsh sites were chosen to capture contrasting soil types: Essex (clay) vs Morecambe Bay (sandy); differing inundation frequency, creek structure, and vegetation.
- Grazing regimes varied by site (e.g., hare grazing and Brent geese in Essex; sheep and geese in Morecambe Bay).

## Sampling design and spatial structure
- Part of the CBESS field campaign; quadrats in 1 x 1 m plots.
- Each site rectangle: 400 x 500 m to 1000 x 1000 m, including low to high marsh zones.
- 22 quadrats per site rectangle, randomly allocated.
- Four spatial scales defined (A–D) to specify sampling configuration:
  - A = 1 quadrat
  - B = 3 quadrats at 1–10 m apart
  - C = 6 quadrats
  - D = additional scaling (not fully detailed in the description)
- Quadrats randomly allocated within each site rectangle using R (R Development Core Team, 2014).

## Methods and data collection
- Core sampling: one large sediment core (16 cm diameter, 30 cm depth) per quadrat, including soil, roots, and vegetation.
- Root biomass processing: cores exposed to erosion by water in a re-circulating flume; roots separated by depth, dried at 60°C for 72 hours, weighed.
- Units: kilograms dry weight per square metre (kg DW m^-2).
- Data conversion: raw measurements converted from kg DW per core area to kg DW m^-2.

## Dataset structure and fields
- Seasons: Winter (W), Summer (S).
- Location: Morecambe (M) or Essex (E).
- Site: CS, WS, WP (Morecambe); AH, FW, TM (Essex).
- Habitat: Mudflat (MF) or Saltmarsh (SM).
- Quadrat Number: 1–22.
- Scale: A, B, C (and D).
- Root biomass fields:
  - RB_0-10: biomass 0–10 cm
  - RB_10-20: biomass 10–20 cm
  - RB_0-30: total biomass 0–30 cm (sum of 0–10, 10–20, 20–30)
- Data notes:
  - Blank cells indicate missing data due to loss of samples during processing.
  - Dataset field descriptions and header definitions are provided (e.g., data types for each column).

## Data quality, provenance, and quality control
- Calibration procedures: scales calibrated according to laboratory protocols.
- Data handling: readings entered into spreadsheets; outliers checked.
- Statistical treatment: no statistical adjustments beyond recording raw dry weights.

## File formats and metadata
- File format: Comma Separated Values (.csv).
- Metadata includes clear definitions for each field (season, location, site, habitat, scale, RB_0-10, RB_10-20, RB_0-30) and notes on data completeness.

## Temporal coverage and maintenance
- Primary sampling during Winter and Summer 2013, with Essex winter samples collected early March 2013.
- No planned repeat sampling noted in the description.

## Personnel
- Staff responsible: Hilary Ford.

## Implications and potential uses for data leaders
- Cross-site comparison of root biomass across soil types (clay vs sandy) and grazing regimes.
- Analyses of depth-wise root distribution within saltmarsh ecosystems.
- Integration with broader CBESS datasets to model carbon storage and root dynamics in marsh habitats.
- Metadata-rich, machine-readable CSV format supports discoverability, reuse, and integration into data catalogs.