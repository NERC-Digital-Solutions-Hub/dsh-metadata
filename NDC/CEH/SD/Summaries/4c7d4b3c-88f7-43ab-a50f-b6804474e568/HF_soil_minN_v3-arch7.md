# Details of data structure to ' HF_soil_minN.csv '

## Overview
- Dataset from grassland fertiliser trial 2016, Henfaes Research Station (Bangor University)
- 11 columns, 608 rows
- Contains soil NH4-N and NO3-N concentrations, plus soil moisture, pH and electrical conductivity (EC)
- Data collection and preparation described to support GIS-based analysis and map-based visualisations

## Dataset structure and contents
- Columns included: Date, N_app, Block, Plot, Treatment, Soil_NH4_mgNkg, Soil_NO3_mgNkg, moisture_dry, moisture_wet, pH, EC
- Date: sampling date
- N_app: fertiliser application identifier (1, 2, or 3); applications: 1st & 2nd at 90 kg ha-1, 3rd at 60 kg ha-1
- Block: blocking factor of the randomised block design (1–4)
- Plot: plot number sampled (1–16)
- Treatment: fertiliser type (AN = ammonium nitrate, U = urea, IU = inhibited urea, C = 0N control)
- Soil_NH4_mgNkg: ammonium concentration (mg NH4-N per kg soil, dry weight basis)
- Soil_NO3_mgNkg: nitrate concentration (mg NO3-N per kg soil, dry weight basis)
- moisture_dry: soil moisture on a dry weight basis (g H2O per g dry soil)
- moisture_wet: soil moisture on a wet weight basis (g H2O per g wet soil)
- pH: soil pH
- EC: soil electrical conductivity (µS cm)

## Sampling and laboratory methods
- Soil sample depth: 0–10 cm (soil core 1 cm diameter)
- For each plot, 6 sub-samples were collected and bulked
- Extraction: 5 g soil with 25 ml 0.5 M K2SO4; shaken 30 minutes at 200 rpm
- Nitrate analysis: colourimetric method (Miranda et al., 2001)
- Ammonium analysis: method (Mulvaney, 1996)
- Moisture determination: 24 hours at 105°C
- pH and EC: measured using standard electrodes; 1:2.5 soil-to-deionised water suspension

## GIS relevance and usage notes
- Attributes capture key soil chemical status (NH4-N, NO3-N), moisture, pH, and EC for spatial analysis
- Sampling structure aligns with plot-level GIS layers (Plot, Block, Date, N_app, Treatment)
- Useful for:
  - Assessing spatial patterns of nutrient status under different fertiliser treatments
  - Linking soil properties to potential yield or health outcomes in map-based visualisations
  - Temporal analyses across sampling dates and application events

## Data provenance and references
- Supplement to supporting documentation: Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf
- Contextual details provided for accurate interpretation and integration with other CINAg data series