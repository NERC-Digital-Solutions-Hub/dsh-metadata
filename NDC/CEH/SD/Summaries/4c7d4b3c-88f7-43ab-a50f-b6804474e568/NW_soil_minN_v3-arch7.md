# NW_soil_minN.csv

## Overview
- Dataset with 9 columns and 512 rows.
- Contains soil NH4-N and NO3-N + NO2-N concentrations plus soil moisture contents.
- Sourced from a grassland fertiliser trial (2016) at North Wyke Research Station (Rothamsted Research).

## Dataset contents and structure
- Columns (with explanations):
  - Date: Date of sampling
  - N_app: Fertiliser application index (1|2|3); 1st & 2nd applications are 90 kg ha-1, 3rd application is 60 kg ha-1
  - Block: Blocking factor of the randomised block design (1|2|3|4)
  - Plot: Plot identifier within blocks (1–16)
  - Treatment: Fertiliser type (AN = ammonium nitrate, U = urea, IU = inhibited urea, C = 0N control)
  - Soil_NH4_mgNkg: Ammonium concentration in soil (mg NH4-N per kg dry soil)
  - Soil_NO3_NO2_mgNkg: Nitrate + nitrite concentration in soil (mg NO3-N per kg dry soil)
  - moisture_dry: Soil moisture on a dry weight basis (g H2O per g dry soil)
  - moisture_wet: Soil moisture on a wet weight basis (g H2O per g wet soil)

## Sampling design and data collection
- Soil sample taken from 0–10 cm depth using a 25 mm diameter corer.
- For each plot, 6–8 samples were collected and bulked.
- Extraction: 50 g fresh soil with 100 ml 2 M KCl; shaken for 60 minutes at 150 rpm.
- Analyses: NH4-N and NO3-N + NO2-N measured using discrete photometric analysis.
- Soil moisture: Determined after drying at 105°C for a minimum of 24 hours.

## Relevance for GIS and map-based data products
- Data organized by Block and Plot enables spatial mapping of nutrient concentrations and moisture across the field trial.
- Treatment and N_app provide the ability to visualize treatment effects geographically.
- Date field allows temporal mapping and trend analysis if multiple sampling dates exist.
- Suitable for creating thematic maps (NH4-N, NO3-N + NO2-N, moisture) at plot-level resolution and integrating with other spatial layers from the CINAg experiments.