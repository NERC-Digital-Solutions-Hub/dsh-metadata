# Details of data structure to ' NW_soil_minN.csv '

- Overview
  - Supplement to supporting documentation for CINAg experiments.
  - Describes the data structure of NW_soil_minN.csv.
  - Dataset consists of 9 columns and 512 rows, capturing soil NH4-N and NO3-N + NO2-N concentrations along with soil moisture.
  - Source: grassland fertiliser trial 2016, North Wyke Research Station (Rothamsted Research).

## Dataset content and structure
- 9 columns and 512 rows.
- Variables include:
  - Date: sampling date.
  - N_app: fertiliser application number (1, 2, or 3); 1st and 2nd applications are 90 kg ha-1, 3rd application is 60 kg ha-1.
  - Block: blocking factor of randomized block design (1–4).
  - Plot: plot identifier (1–16).
  - Treatment: fertiliser type (AN = ammonium nitrate, U = urea, IU = inhibited urea, C = 0N control).
  - Soil_NH4_mgNkg: ammonium concentration in soil (mg NH4-N per kg; dry weight basis).
  - Soil_NO3_NO2_mgNkg: nitrate + nitrite concentration in soil (mg NO3-N per kg; dry weight basis).
  - moisture_dry: soil moisture on a dry weight basis (g H2O per g dry soil).
  - moisture_wet: soil moisture on a wet weight basis (g H2O per g wet soil).

## Sampling, extraction, and analysis methods
- Sampling depth and method:
  - Soil samples collected from 0–10 cm using a 25 mm diameter corer.
  - For each plot, 6–8 samples were taken and bulked.
- Laboratory procedures:
  - Extraction: 50 g fresh soil mixed with 100 ml 2 M KCl; shaken for 60 minutes at 150 rpm.
  - NH4-N analysis: discrete photometric analysis.
  - NO3-N + NO2-N analysis: discrete photometric analysis.
  - Moisture determination: dried at 105°C for at least 24 hours.

## Experimental design and provenance
- Trial context: grassland fertiliser trial conducted in 2016 at North Wyke Research Station.
- Design: randomized block with blocks 1–4; plots 1–16.
- Treatments represent different nitrogen fertilisers (AN, U, IU) and a no-N control (C).

## Data governance, metadata, and discoverability
- This document serves as a data-structure specification accompanying broader CINAg experiments.
- Metadata details provided:
  - Unit definitions for each variable (e.g., mg N kg-1 dry weight, g H2O g dry/wet soil-1).
  - Clear interpretation of N_app values and corresponding application rates.
  - Sampling and analytical methods documented to support reproducibility.

## Considerations for data leaders
- Ensure consistency with related data series and documentation (e.g., Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf).
- Verify completeness and alignment of units, variable naming, and measurement methods across datasets.
- Assess data interoperability by linking to broader soil N datasets and updating metadata for discoverability.

## Limitations and scope
- Single site and year, 0–10 cm depth, 9 variables across 512 records.
- Temporal resolution tied to fertiliser applications; may limit interpretation outside those timepoints.
- Moisture metrics presented in two bases (dry and wet), requiring careful handling during analyses.

## Implications for use
- Suitable for analyses of how different N fertilisers affect soil NH4-N and NO3-N + NO2-N concentrations and soil moisture at early 2016 grassland trial stages.
- Useful for assessing data provenance, measurement methods, and sampling design to support reproducibility and integration with other data within the CINAg framework.