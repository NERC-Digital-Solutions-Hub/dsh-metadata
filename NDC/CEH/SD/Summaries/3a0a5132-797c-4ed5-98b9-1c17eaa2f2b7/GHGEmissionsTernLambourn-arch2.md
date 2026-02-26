# Experimental Design and Laboratory Incubation Method

## Overview
- Study collected sediments from two river systems (River Lambourn, Chalk; River Tern, Sandstone) in September 2015.
- Aimed to examine microbial metabolic activity and greenhouse gas production across multiple substrate types, temperatures, and controlled conditions.
- Data produced include CO2, CH4, resorufin (proxy for microbial activity), and dissolved oxygen, plus sediment organic matter content.

## Sampling and Substrate Treatments
- Sediment collected from upper 10 cm of the riverbeds at three areas per site: fine (under vegetation), medium (unvegetated sand-dominated), and coarse (unvegetated gravel-dominated).
- Six substrate treatments: Chalk fine, Chalk medium, Chalk coarse, Sandstone fine, Sandstone medium, Sandstone coarse.
- Each substrate sample ~5 liters; samples homogenised, sieved (0.8 cm for fine; 1.6 cm for medium and coarse), stored airtight, cold, in the dark until incubation.
- plus control treatments consisting of 500 ml ultrapure water (18.2 MΩ).
- Triplicate samples per substrate, incubated in seven substrate treatments total (including controls).

## Incubation Protocol
- Temperature treatments: 5, 9, 15, 21, 26°C.
- Incubation setup: 300 ml sediment + 500 ml ultrapure water in sealed 1 L amber jars.
- Sampling: at 0 hours and after 5 hours of incubation.
- Jars labeled 1–21 to correspond to triplicates across substrate types (e.g., 1–3 Chalk fine, 4–6 Chalk medium, etc.); Substrate_Type and Jar IDs recorded in dataset.
- Headspace sampling included resazurin/resorufin tracer, dissolved oxygen, and headspace gas for CO2/CH4 analyses.

## Measurements and Analytical Methods
- Microbial activity: resazurin-resorufin tracer system; resorufin concentration measured as proxy for activity.
- Gas measurements: CO2 and CH4 concentrations measured with a GC-FID system.
- Resorufin: measured with GGUN-FL30 fluorometer (customized with specific excitation wavelengths).
- Dissolved oxygen: measured with Pyro-Science Firesting needle-type sensor.
- Organic matter: determined via loss on ignition (LOI) after drying and combustion at 550°C.

## Calibration and Quality Assurance
- Gas chromatograph-flame ionisation detector (GC-FID) calibration: daily four-point standards for CO2 and CH4; drift correction using periodic external standard injections; accuracy, precision, and LOD reported (CO2: 13.4/14.8/8.2; CH4: 0.07/0.11/0.15 mg/m3).
- Fluorometer calibration: weekly three-point calibration (zero, 100 ng/L resorufin, resorufin/resazurin mix); standard of 93.1 ng/L resorufin for performance checks.
- Oxygen sensor calibration: daily one-point calibration at 100% air saturation.
- Overall protocols designed to ensure traceability and comparability across substrates, temperatures, and sampling times.

## Data Collected and Dataset Description
- Dataset name: IncubationCO2_CH4_Resorufin_DO (CSV).
- Columns:
  - Temperature (°C)
  - Jar (1–21)
  - Substrate_Type ( Chalk fine, Chalk medium, Chalk coarse, Sandstone fine, Sandstone medium, Sandstone coarse)
  - Geology (Chalk or Sandstone; NA for controls)
  - Organic_Matter (%)
  - CO2 (mg C m^-2 h^-1)
  - CH4 (mg C m^-2 h^-1)
  - Resorufin (ng resorufin per μg resazurin per hour)
  - Dissolved_Oxygen (mg L^-1)

## Substrate, Geology, and Controls
- Geology field indicates origin rock type (Chalk or Sandstone) or NA for controls.
- Control experiments consist of jars with only ultrapure water (no sediment) for baseline comparisons.
- The dataset captures both substrate-specific responses and sediment organic matter influences on gas production and microbial activity.

## Context and Purpose for Monitoring Analysts
- Provides a standardized, multi-factor dataset to evaluate environmental health and microbial-mediated gas production across sediment types and temperatures.
- Methods emphasize data quality, reproducibility, and clear metadata to enable cross-site comparisons and integration into monitoring programs.
- The structured data format supports tracking environmental processes over time and contributing to policy-relevant assessments of sedimentary biogeochemical activity.