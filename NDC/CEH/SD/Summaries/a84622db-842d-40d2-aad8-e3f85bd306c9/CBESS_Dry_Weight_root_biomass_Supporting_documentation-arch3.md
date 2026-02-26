# Dry weight root biomass from three soil depths on salt marsh sites at Morecambe Bay and Essex.

## Overview and purpose
- Dataset of root biomass (kg dry weight per m^2, DW m^-2) for three soil depths (0–10 cm, 10–20 cm, 20–30 cm) across saltmarsh sites in Essex and Morecambe Bay.
- Collected during the CBESS field campaign in Winter and Summer 2013, with an additional Essex-specific sampling window (2–6 March 2013).
- Aims to support environmental health monitoring by providing site- and depth-specific root biomass data to inform habitat status, carbon stocks, and potential responses to grazing and inundation regimes.

## Study area and sampling design
- Locations:
  - Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
  - Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP).
- Site characteristics:
  - Saltmarsh sites chosen to represent contrasting soil types (clay in Essex; sandy in Morecambe Bay) and differing inundation frequency, creek structure, and vegetation.
  - Grazing regimes varied: heavily grazed by Brent geese in Essex; intensive sheep grazing in Morecambe Bay; light grazing at West Plain.
- Sampling design:
  - Each site rectangle ranged from 400 × 500 m to 1000 × 1000 m, including low, mid, and high marsh zones.
  - Twenty-two 1 × 1 m quadrats randomly allocated per site rectangle.
  - Four spatial scales defined (A–D) with increasing numbers of quadrats per site; quadrats randomly allocated within each rectangle using R.
  - At least one large sediment core (16 cm diameter, 30 cm depth) per quadrat collected for analysis.

## Methods and measurements
- Field procedure:
  - Core collected per quadrat, including soil, intact roots, and above-ground vegetation.
  - Roots eroded in a re-circulating flume, then separated into depth bands (0–10 cm, 10–20 cm, 20–30 cm).
  - Roots dried at 60°C for 72 hours, weighed, and converted to kg DW per m^2.
- Units and derivations:
  - Primary variable: root biomass by depth (RB_0-10, RB_10-20, RB_0-30).
  - Total root biomass 0–30 cm calculated as the sum of the three depth intervals (RB_0-30).
- Documentation and metadata:
  - Staff responsible: Hilary Ford.
  - Sampling periods: Winter and Summer 2013, with Essex winter samples collected 2–6 March 2013.
  - Data format: CSV files; full dataset includes fields for season, location, site, habitat, quadrat number, scale, depth-band biomass, and total biomass.

## Data structure and variables
- Key variables:
  - RB_0-10: root biomass 0–10 cm (kg DW m^-2)
  - RB_10-20: root biomass 10–20 cm (kg DW m^-2)
  - RB_0-30: total root biomass 0–30 cm (kg DW m^-2)
  - Other fields: Season (Winter/Summer), Location (Morecambe or Essex), Site (AH, FW, TM, CS, WS, WP), Habitat (Mudflat, Saltmarsh), Quadrat Number (1–22), Scale (A–D)
- Data quality notes:
  - Some missing data indicated where samples were lost during processing.
  - Data checked by entering scale readings into spreadsheets and screening for outliers.

## Quality control, governance, and data sharing
- QA steps:
  - Data entry into spreadsheets; outlier checks performed.
  - Calibration procedures referenced where applicable; scales documented.
- Metadata and openness:
  - Dataset includes extensive site and sampling metadata to support transparency and reuse.
  - Data management aligns with open data practices, though some entries indicate potential gaps due to missing samples.
- Governance context:
  - Part of CBESS field campaign; staff and site descriptions help inform monitoring design and interpretation.
  - Clear documentation of sampling plan and procedures supports integration into monitoring frameworks, subject to data availability and completeness.

## Relevance for monitoring frameworks
- Strengths for environmental monitoring:
  - Provides standardized, depth-resolved root biomass data across contrasting saltmarsh habitats and grazing regimes.
  - Explicit sampling design (random quadrats, site rectangles, multiple spatial scales) supports robust trend analysis and power calculations.
  - Clear processing workflow (core sampling, depth separation, drying, weighing) and derived total biomass facilitate comparability over time.
- Considerations and potential limitations:
  - No planned repeat sampling beyond 2013; temporal coverage is limited to the campaign period, which may constrain trend detection.
  - Some data gaps due to sample loss and potential metadata inconsistencies; ensure careful data cleaning before integration into dashboards or policy briefs.
  - Site-level ecological context (grazing intensity, inundation regime) is described, aiding interpretation of biomass results within monitoring frameworks.