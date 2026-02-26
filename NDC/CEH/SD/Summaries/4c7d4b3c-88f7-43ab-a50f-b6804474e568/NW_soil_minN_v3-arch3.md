# Details of data structure to 'NW_soil_minN.csv'

## Overview
- Supplement to the supporting documentation for data series described in Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf
- Dataset contains 9 columns and 512 rows
- Contains soil NH4-N and NO3-N + NO2-N concentrations along with soil moisture contents
- Data originate from a grassland fertiliser trial conducted in 2016 at North Wyke Research Station (Rothamsted Research)

## Dataset structure
- Date: Date of sampling
- N_app: Fertiliser application indicator with values 1, 2, or 3
  - 1st & 2nd applications: 90 kg ha-1
  - 3rd application: 60 kg ha-1
- Block: Blocking factor of the randomized block design (1–4)
- Plot: Sampled plot within the block (1–16)
- Treatment: Fertiliser type with codes
  - AN = ammonium nitrate
  - U = urea
  - IU = inhibited urea (Agrotain)
  - C = 0N control
- Soil_NH4_mgNkg: Ammonium concentration in soil (mg NH4-N kg-1), expressed on a dry weight basis
- Soil_NO3_NO2_mgNkg: Nitrate + nitrite concentration in soil (mg NO3-N kg-1), expressed on a dry weight basis
- moisture_dry: Soil moisture on a dry weight basis (g H2O g dry soil-1)
- moisture_wet: Soil moisture on a wet weight basis (g H2O g wet soil-1)

## Sampling and analytical methods
- Soil sample collected 0–10 cm depth using a 25 mm diameter corer
- For each plot, 6–8 samples were taken and bulked
- Extraction: 2 M KCl, 50 g fresh soil to 100 ml KCl; shaken 60 minutes at 150 rpm
- NH4-N analysis: discrete photometric analysis
- NO3-N and NO2-N analysis: discrete photometric analysis
- Soil moisture: determined after a minimum of 24 hours at 105°C

## Data provenance
- Part of the data series supplementary documentation for CINAg experiments (linked to the broader Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf)