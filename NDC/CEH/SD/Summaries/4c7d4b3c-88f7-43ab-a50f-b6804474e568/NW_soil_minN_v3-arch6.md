# Details of data structure to ' NW_soil_minN.csv '

## Overview
- Supplement to supporting documentation for data series referenced in Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf
- Dataset: 9 columns, 512 rows
- Variables included: soil NH4-N, NO3-N + NO2-N concentrations and soil moisture contents
- Source: grassland fertiliser trial 2016, North Wyke Research Station (Rothamsted Research)

## Data Structure
- Column header explanations and units are provided for each variable
- Key columns and their meanings:
  - Date: Date of sampling
  - N_app: fertiliser application identifier (1, 2, or 3); 1st & 2nd applications 90 kg ha-1, 3rd application 60 kg ha-1
  - Block: blocking factor of randomized block design (1–4)
  - Plot: plot number sampled (1–16)
  - Treatment: N fertiliser type (AN = ammonium nitrate, U = urea, IU = inhibited urea, C = 0N control)
  - Soil_NH4_mgNkg: ammonium concentration in soil (mg NH4-N per kg dry soil)
  - Soil_NO3_NO2_mgNkg: nitrate + nitrite concentration in soil (mg NO3-N per kg dry soil)
  - moisture_dry: soil moisture on a dry weight basis (g H2O per g dry soil)
  - moisture_wet: soil moisture on a wet weight basis (g H2O per g wet soil)

## Sampling and Analytical Methods
- Soil sampled from 0–10 cm depth using a 25 mm diameter corer
- For each plot, 6–8 samples were collected and bulked
- Extraction: 50 g fresh soil to 100 mL 2 M KCl; shaken for 60 minutes at 150 rpm
- NH4-N determined by discrete photometric analysis
- NO3-N + NO2-N determined by discrete photometric analysis
- Soil moisture measured after drying at 105°C for at least 24 hours

## Notes for Use
- Data are part of a larger data series and linked to supporting documentation (Supplementary to Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf)
- Structure enables self-contained interpretation of sampling events, treatments, and measurements, with clear units and coding for fertilizer types and plot design
- Useful for cross-dataset integration involving soil nitrogen pools and moisture in the context of grassland fertiliser experiments