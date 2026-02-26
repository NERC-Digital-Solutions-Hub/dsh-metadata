# Continuous measurements of conductivity, dissolved oxygen, pH, temperature and water level in rivers (2002-2007) [LOCAR] LOCAR BASELINE DATASETS LOCAR

## Overview
- LOCAR baseline dataset capturing continuous water quality and hydrological measurements across 23 sites in the Frome, Piddle, Pang, Lambourn, and Tern catchments from 2002–2007.
- Objectives: document environmental conditions in a standardised format to support monitoring of environmental health and policy performance over time.

## What was measured
- Water quality and related variables (measured at 15-minute intervals):
  - Conductivity (25°C), units: microsiemens per centimeter (uS/cm)
  - Dissolved oxygen (DO) as % saturation
  - pH (pH units)
  - Temperature (water, °C)
  - Water level (mm)
- Instrumentation: YSI 6-Series multi-parameter sondes for water quality; Druck PDCR 1830 transducers for water level.
- Site co-location: instruments installed at EA monitoring sites, with several also linked to NRFA stations.

## Sites and coverage
- 23 sites distributed across catchments:
  - Examples include Bere Stream, Frome, Piddle, Pang, Lambourn, Tern catchments
  - Site codes: FP01, FP02, FP06, FP11, FP12, FP15, FP21, FP22, FP23, FP26, FP31, PL09, PL15, PL17, PL18, PL19, PL20, TE03, TE05, TE09, TE16, TE20, TE22
- Some pairs of sites shared locations (e.g., TE05 and TE22).

## Methods and instrumentation
- Data collection:
  - Continuous recording at 15-minute intervals (2002–2007).
- Sensors and ranges:
  - Temperature: thermistor-based sensor; range -5 to 45°C; accuracy ±0.15°C; resolution 0.01°C
  - pH: glass electrode; range 0–14; accuracy ±0.2 pH; resolution 0.01 pH; calibration with pH buffers
  - Conductivity: four-nickel electrode cell; range 0–100 mS/cm; accuracy ±0.5% of reading plus 0.001 mS/cm; resolution 0.001–0.1 mS/cm
  - Dissolved Oxygen: rapid pulse Clark-type sensor; range 0–500% air saturation; accuracy varies by range; resolution 0.1%
  - Water level: Druck PDCR 1830 pressure transducer; range 0.75–600 mH2O; accuracy ±0.06%
- Maintenance and calibration:
  - Sondes/calibration: two-week deployment before calibration checks; calibration performed in the laboratory for DO, conductivity, and pH
  - Post-deployment checks performed upon return; calibration software used to record post-calibration values
  - Calibration steps included venting DO, stabilising DO in air-saturated conditions, and using stable buffer solutions for conductivity and pH
- Data handling:
  - Data were collected by the Catchment Service Teams in each catchment; raw data were produced
  - Data not quality-controlled or corrected for instrument drift or failures at the time of collection

## Data quality and cautions
- Data are raw and not QA’d for instrument failure or drift.
- Normal ranges (Chapman, 1996) used as reference:
  - Temperature: 0–30°C
  - pH: 6.0–8.5
  - Conductivity: 10–1000 µS/cm
  - Dissolved Oxygen: 0–20 mg/L
- Quality observations:
  - Box-and-whisker plots generated to show ranges, medians, quartiles, and outliers
  - Noted issues:
    - Broad scatter; some periods with unrealistic values
    - Battery level < 10 V indicates unreliable data for all parameters
    - DO values >200% are possible but unlikely
    - pH values outside 1–14; values >11 or <4 may be unreliable
    - Temperature outside 5–25°C warrants investigation
    - Conductivity and water level highly site-specific

## Outputs and data management
- Outputs included box-and-whisker plots for all measured parameters to summarise ranges and variability
- Location information and site details are documented (Figure 1 illustrates site locations; some sites shared coordinates)
- Responsibility for deployment, maintenance, and data download rested with the Catchment Service Teams in each catchment

## Key implications for Analysts
- The LOCAR baseline dataset provides a broad, standardized set of continuous river measurements suitable for inter-site comparisons and trend analysis over time, with explicit calibration and maintenance procedures.
- Raw data status highlights the need for subsequent QA/QC, bias correction for instrument drift, and filtering of unreliable periods (e.g., low battery intervals) before integration with other datasets.
- The data can be valuable when combined with EA NRFA data or other environmental datasets to enhance understanding of environmental health and policy outcomes, aligning with aims to increase dataset value and broaden data accessibility.