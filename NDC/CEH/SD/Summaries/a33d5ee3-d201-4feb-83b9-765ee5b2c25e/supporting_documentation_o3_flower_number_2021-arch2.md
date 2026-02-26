# Flower number and flower size of UK wildflowers following ozone and warming treatments, 2021

## Overview
- A dataset describing how ozone exposure and warming affect flowering metrics (flower number and flower width) in five UK wildflower species under controlled solardome conditions in 2021.
- Aimed at consistent environmental monitoring to support assessment of ecosystem responses to ozone and climate-related warming, with data prepared for scrutiny and reuse over time.

## Experimental setup

- Location and site
  - Rural site at Abergwyngregyn, North Wales, UK
  - Coordinates: 53°14′N, 4°01′W; Elevation: 15 m

- Experimental infrastructure
  - Eight solardomes (hemispherical glasshouses) with charcoal-filtered air
  - Ozone added to domes via computer-controlled profile; three domes included a warming treatment of +4°C

- Treatments and design
  - Dome_3: Ozone 30 ppb, ambient temperature
  - Dome_7: Ozone 50 ppb, ambient temperature
  - Dome_8: Ozone 65 ppb, ambient temperature
  - Dome_1: Ozone 80 ppb, ambient temperature
  - Dome_5: Ozone 110 ppb, ambient temperature
  - Dome_6: Three parts – ambient, heated (+4°C), ozone 30 ppb with ambient +4°C
  - Dome_2: Ambient plus heated; ozone 80 ppb with ambient +4°C
  - Dome_4: Ambient plus heated; ozone 110 ppb with ambient +4°C
  - Treatments ran from 1 June to 24 October 2021

- Species studied (10 replicate pots per species per treatment)
  - Birdsfoot trefoil (Lotus corniculatus)
  - White clover (Trifolium repens)
  - Clustered bellflower (Campanula glomerata)
  - Catsear (Hypochaeris radicata)
  - Harebell (Campanula rotundifolia)

- Data collection context
  - Ozone and meteorological conditions continuously monitored hourly
  - Measurements include light, temperature, relative humidity; ambient dome measurements used due to consistency across ambient domes

## Data collection and measurements

- Plant data
  - Manual data collection with quality checks
  - Metrics per pot: mean flower number and mean flower width for each species
  - Data gaps exist where no flowers were present in a given treatment

- Ozone and meteorological data
  - Hourly logging via LabView-controlled system
  - Ambient dome metrics (temperature, RH, light) recorded; heated domes provided separate temperature and RH data

## Data files and structure

- Solardomes_flower_data_2021.csv
  - 14 columns (A–N); 32 data rows + header
  - A: Month; B: Warming_treatment (ambient/heated); C: Ozone_treatment (ppb); D: Dome_number
  - E–N: Flower data metrics
    - E. Trefoil_flower_number_mean_per_pot
    - F. Trefoil_flower_width_mean_per_pot_mm
    - G. White_clover_flower_number_mean_per_pot
    - H. White_clover_flower_width_mean_per_pot_mm
    - I. Bellflower_flower_number_mean_per_pot
    - J. Bellflower_flower_width_mean_per_pot_mm
    - K. Catsear_flower_number_mean_per_pot
    - L. Catsear_flower_width_mean_per_pot_mm
    - M. harebell_flower_number_mean_per_pot
    - N. harebell_flower_width_mean_per_pot_mm

- 2021_Ozone_hourly.csv
  - 19 columns (A–S); 3527 data rows + header
  - A: Day; B: Hour_of_day
  - C–S: Dome hourly ozone and microclimate data
    - Dome_1_PPB_hourly, Dome_2_PPB_hourly, Dome_3_PPB_hourly, Dome_4_PPB_hourly, Dome_5_PPB_hourly, Dome_6_PPB_hourly, Dome_7_PPB_hourly, Dome_8_PPB_hourly
    - ambient_Temp_degC
    - Light_micromolm2s1
    - ambient_RH
    - D2_T, D2_RH (Dome 2 heated)
    - D4_T, D4_RH (Dome 4 heated)
    - D6_T, D6_RH (Dome 6 heated)

## Quality control and data gaps

- Quality control
  - Plant data: manual QA to ensure plausible values
  - Ozone and meteorological data: automated QA for plausibility and range checks; gap-filling as needed

- Data gaps and limitations
  - Flowering data has gaps where no flowers were present in a treatment
  - Ozone/meteorological dataset has gaps at the start due to system failure

## Relevance to environmental monitoring

- Provides standardized, traceable data to monitor plant responses to ozone and warming
- Facilitates cross-dataset analyses and policy-relevant environmental health assessments
- Data are stored and prepared for upload to appropriate data portals for long-term accessibility

## Contacts and attribution

- Main point of contact: F.J. Hayes (UKCEH); fhay@ceh.ac.uk
- Other authors: Katrina Sharps (katshar@ceh.ac.uk)