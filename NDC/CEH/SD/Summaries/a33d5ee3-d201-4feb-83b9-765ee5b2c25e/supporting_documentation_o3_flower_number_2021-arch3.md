# Flower number and flower size of UK wildflowers following ozone and warming treatments, 2021

## Overview
- A study designed to quantify how ozone exposure and warming affect flowering traits of UK wildflowers, providing environmental health measures to inform policy monitoring and future decisions.
- Focuses on five wildflower species and how their flower number and flower width respond to different ozone levels and warming scenarios in controlled field-like conditions.

## Experimental design and setting
- Location and setup:
  - Rural site at Abergwyngregyn, North Wales, UK.
  - Eight solardomes used to expose plants to ozone and/or warming; charcoal-filtered air with controlled ozone addition.
  - Three solardomes included a warming treatment (temperature increased by +4°C).
- Treatments:
  - Ozone profiles varied by dome (example target peaks): 30 ppb, 50 ppb, 65 ppb, 80 ppb, 110 ppb.
  - Doms also varied by warming status (ambient vs heated). Some domes combined high ozone with warming (e.g., Dome 6, Dome 2, Dome 4 configurations).
  - A weekly ozone episode profile was applied, with ozone additions at night and day.
- Species studied (10 in total across measurements):
  - Birdsfoot trefoil (Lotus corniculatus)
  - White clover (Trifolium repens)
  - Clustered bellflower (Campanula glomerata)
  - Catsear (Hypochaeris radicata)
  - Harebell (Campanula rotundifolia)
- Experimental period:
  - Treatments run from 1 June to 24 October 2021.
- Data collection and QA:
  - Manual QA for plant data to verify plausibility; ozone/met data automatically logged with QA for ranges and plausibility; gap-filling applied when needed.
  - Meteorological measurements recorded hourly; ambient dome data referenced from a single ambient dome (dome 7) based on prior comparisons showing no variation between ambient domes.

## Data products and structure
- Flower data file: Solardomes_flower_data_2021.csv
  - Structure: 14 columns (A–N) with 32 data rows plus a header.
  - Columns include:
    - A. Month
    - B. Warming_treatment (ambient vs heated)
    - C. Ozone_treatment (peak ppb)
    - D. Dome_number
    - E–N. Flower metrics:
      - For each species: mean flower number per pot and mean flower width per pot (mm)
  - Metrics cover:
    - Birdsfoot trefoil, White clover, Clustered bellflower, Catsear, Harebell
- Hourly ozone and meteorology file: 2021_Ozone_hourly.csv
  - Structure: 19 columns (A–S) with day and hour identifiers plus 17 measured variables.
  - Key variables include:
    - Hourly ozone concentrations for Dome_1 through Dome_8 (PPB)
    - Ambient temperature (ambient_Temp_degC)
    - Light (micromol m-2 s-1)
    - Ambient relative humidity (ambient_RH)
    - Hourly temperature and RH for heated domes Dome_2 (D2_T, D2_RH), Dome_4 (D4_T, D4_RH), and Dome_6 (D6_T, D6_RH)
- Data scope:
  - Flower data: 32 rows representing measurement periods across domes/treatments.
  - Ozone hourly data: 3,527 rows representing hourly measurements across the study period.

## Data quality, gaps, and governance
- Quality control:
  - Plant data: manual QA and plausibility checks; ozone and meteorological data: automated QA with range checks and plausibility reviews; occasional gap-filling as needed.
- Gaps and limitations:
  - Flower data contain periods with no flowers under certain treatments.
  - Meteorological data show initial gaps due to system failure.
- Data sharing and openness:
  - Challenges noted in the broader context include barriers to publicly sharing datasets and ensuring metadata quality; this study provides openly structured datasets with clear metadata, though effective data governance and timely access remain important considerations for monitoring frameworks.

## Relevance for monitoring frameworks and policy decisions
- Indicator potential:
  - Flower number and flower width under varying ozone and warming scenarios serve as measurable ecological responses to air quality and climate stressors.
  - Hourly ozone exposure data aligned with ambient and heated conditions support assessment of exposure-response relationships.
- Data governance lessons for frameworks:
  - Importance of metadata, data provenance, and standardised formats to enable reuse in policy evaluation.
  - Need for timely data access, robust QA, and clear documentation to prevent data silos and facilitate integration into monitoring dashboards, reports, or dashboards used by policymakers.
- Applicability:
  - Methods and datasets exemplify how to structure monitoring outputs (treatment, dome, and species-level metrics) for policy scrutiny, trend analysis, and decision-making about environmental health under ozone and warming pressures.

## Contact and provenance
- Main point of contact: F.J. Hayes, UKCEH (fhay@ceh.ac.uk)
- Additional authors: Katrina Sharps (katshar@ceh.ac.uk)