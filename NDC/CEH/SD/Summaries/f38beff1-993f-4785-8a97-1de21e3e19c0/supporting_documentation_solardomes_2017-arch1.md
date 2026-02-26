# Ozone and Meteorology and Plant Physiology Data 2017

## Context and Site
- Rural site in North Wales, UK, part of Bangor University farm; near the sea.
- Eight solardomes (hemispherical glasshouses) used in 2017 experiments; ozone added at target levels.
- Three solardomes were heated by 7°C above ambient to mimic tropical/subtropical conditions; associated plant biomass and physiology data available only for these heated domes.
- Ozone exposure followed a weekly profile, controlled by LabView software; additions occur at night and day.
- Continuous hourly sampling of ozone and meteorological conditions; ad-hoc plant measurements and end-of-experiment yield data.

## Experimental Design
- Four replicate pots per species/cultivar grown from seed and exposed to ozone in solardomes.
- Ozone and meteorology logged hourly; stomatal conductance measured ad-hoc with soil moisture and chlorophyll content index data also collected.
- Exposure length varied by species due to differing growing seasons.
- End-of-experiment yield measured for all species/cultivars.

## Treatments
- Treatment abbreviations include:
  - Low ozone, unheated: target peak 35 ppb, ambient temperature
  - Medium ozone, unheated: target peak 80 ppb, ambient temperature
  - High ozone, unheated: target peak 115 ppb, ambient temperature
  - Low ozone, heated: 35 ppb, ambient temperature +7°C
  - Medium ozone, heated: 80 ppb, ambient temperature +7°C
  - High ozone, heated: 115 ppb, ambient temperature +7°C

## Data Collected and Variables
- Ozone and Meteorology (Ozone_and_meteorology_2017.csv):
  - Day_of_Year, Date, Hour_of_Day, Ozone_ppb
  - Light_in_dome_7 (PAR)
  - Temperature, Vapour Pressure Deficit, Air_pressure, Windspeed, Precipitation
  - Treatment, DO3SE model inputs (for ozone flux calculations)
- Plant Physiology (Plant_Physiology_2017.csv):
  - Treatment, Plant_Species, Pot_Number, Date/Time
  - Leaf_side, stomatal_conductance (mmol H2O/m2/s), Light, Leaf_Temperature, Soil_Moisture, Chlorophyll_Content_Index
- Biomass and Yield (Biomass_and_Yield_2017.csv):
  - Plant_Species_and_variety, Treatment, Pot_Number
  - Pod_number, Pod_weight_grams, Bean_number, Bean_weight_grams
  - Seed_head_total_weight_grams, Seeds_per_pod, Weights per pod, Total grains, 100_grain_weight, Ears per pot, Calculated totals

## Equipment and Calibration
- Ozone exposure system controlled by LabView (National Instruments, v2012)
- AP4 Porometer for stomatal conductance (calibrated daily)
- Theta probe for soil moisture
- CCM-200 for Chlorophyll Content Index (auto-calibration in startup)
- External calibration for ozone analysers (Air Monitors Ltd)

## Data Resource Structure and Quality Control
- Three CSV files:
  - Biomass_and_Yield_2017.csv: 17 columns, 3112 rows
  - Ozone_and_meteorology_2017.csv: 11 columns, 18534 rows
  - Plant_Physiology_2017.csv: 11 columns, 3112 rows
- Blank cells indicate missing readings; some measurements missing due to QA issues.
- QA procedures:
  - Automatic data logging with plausibility checks
  - Ad-hoc plant data QA with plausibility checks
  - End-of-experiment yield data QA with plausibility checks

## Gap Filling and Data Processing
- Gaps identified to ensure a complete 24-hour record; gaps ≤5 hours filled with the average of surrounding values.
- Larger gaps: refer to lab book to determine reason; fill using previous/next day values when appropriate (e.g., 09:00 value is the average of 09:00 on previous day and next day).
- If system not running, fill with a dummy 5 ppb ozone value to reflect no supplementary ozone.
- Original data preserved; amended copies created and logged as separate “filled and corrected” datasets.
- Data are prepared to enable DO3SE ozone flux modeling; windswept and precipitation values are set to constant dummy values to support model runs.

## Analytical Opportunities and Considerations
- Data enable analysis of ozone exposure effects on plant physiology and yield across multiple species, with temperature interaction (heated vs unheated).
- Potential correlations between ozone levels, stomatal conductance, photosynthetically active radiation, leaf temperature, soil moisture, and final biomass/yield.
- Multi-species and multi-treatment comparisons, with consideration of data gaps and QA-limited measurements.

## Miscellaneous
- Facility description and research context available at the CEH Solardomes and Ozone Field Release System page:
  https://www.ceh.ac.uk/our-science/research-facilities/solardomes-and-ozone-field-releasesystem
- Analytical Methods: No formal analysis implemented within the dataset description; data are prepared for subsequent analysis.