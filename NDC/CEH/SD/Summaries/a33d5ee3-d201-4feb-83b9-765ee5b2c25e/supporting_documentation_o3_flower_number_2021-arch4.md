# Flower number and flower size of UK wildflowers following ozone and warming treatments, 2021 Supporting documentation

## Overview
- Documents data collection and structure from the 2021 solardome ozone and warming experiment.
- Focuses on flower number and flower size per pot for five species, under multiple ozone and warming treatments.
- Describes two data files: Solardomes_flower_data_2021.csv and 2021_Ozone_hourly.csv, including methods, site details, QA, and data structure.

## Data assets and metadata
- Solardomes_flower_data_2021.csv
  - 14 columns (A–N); 32 data rows plus header.
  - Columns describe treatment, dome, and per-pot flower metrics for five species.
  - Key metrics include mean flower number per pot and mean flower width per pot (mm) for each species.
- 2021_Ozone_hourly.csv
  - 19 columns (A–S); 3527 data rows plus header.
  - Day and hour, hourly ozone concentrations for eight domes, ambient temperature, light, relative humidity, and temperatures/RH for three heated domes (D2, D4, D6).

## Experimental design and data collection methods
- Location and Setup
  - Rural site in North Wales (Abergwyngregyn), eight solardomes with charcoal-filtered air; three domes heated by +4°C for warming treatment.
  - Ozone added according to a weekly profile, controlled by LabView; additions occur day and night.
- Biological material
  - Ten replicate pots per species per treatment; plants grown from plug plants.
  - Species: Birdsfoot trefoil (Lotus corniculatus), White clover (Trifolium repens), Clustered bellflower (Campanula glomerata), Catsear (Hypochaeris radicata), Harebell (Campanula rotundifolia).
- Treatments and timing
  - Dome-specific ozone target peak heights (ppb) and warming status (ambient or heated).
  - Example domes with varying ozone levels: Dome_3 (30, 50, 65, 80, 110 ppb ambient), Dome_7 (50 ppb ambient), Dome_8 (65 ppb ambient), Dome_1 (80 ppb ambient), Dome_5 (110 ppb ambient); Dome_6/Dome_2/Dome_4 include heated conditions (+4°C) alongside ozone levels.
  - Experimental period: 1 June 2021 to 24 October 2021.
- Data collection frequency and sensors
  - Ozone and meteorological conditions sampled hourly; ambient dome meteorology measured in dome 7; temperature and RH also recorded in heated domes.
  - Plants watered as required during ozone exposure.
- Site details
  - Latitude 53°14'N, Longitude 4°01'W, Elevation 15 m.

## Data quality, QA, and gaps
- Quality assurance
  - Manual plant data collection with QA checks for plausibility and range.
  - Ozone and meteorological data automatically logged with QA checks and gap-filling where needed.
- Gaps and limitations
  - Flowering data: gaps occur when no flowers are present in a treatment.
  - Ozone/meteorological datasets: gaps at the dataset start due to system failure.

## Data structure, variables, and units
- Solardomes_flower_data_2021.csv
  - A. Month: Month of measurement
  - B. Warming_treatment: 'ambient' or 'heated'
  - C. Ozone_treatment: Ozone peak concentration in ppb
  - D. Dome_number: Solardome identifier
  - E. Trefoil_flower_number_mean_per_pot: mean number of Birdsfoot trefoil flowers per pot
  - F. Trefoil_flower_width_mean_per_pot_mm: mean width (mm) of Birdsfoot trefoil flowers per pot
  - G. White_clover_flower_number_mean_per_pot: mean number of White clover flowers per pot
  - H. White_clover_flower_width_mean_per_pot_mm: mean width (mm) of White clover flowers per pot
  - I. Bellflower_flower_number_mean_per_pot: mean number of Clustered bellflower flowers per pot
  - J. Bellflower_flower_width_mean_per_pot_mm: mean width (mm) of Clustered bellflower flowers per pot
  - K. Catsear_flower_number_mean_per_pot: mean number of Catsear flowers per pot
  - L. Catsear_flower_width_mean_per_pot_mm: mean width (mm) of Catsear flowers per pot
  - M. harebell_flower_number_mean_per_pot: mean number of Harebell flowers per pot
  - N. harebell_flower_width_mean_per_pot_mm: mean width (mm) of Harebell flowers per pot
- 2021_Ozone_hourly.csv
  - A. Day: Date of measurement
  - B. Hour_of_day: Hour (0–23)
  - C–S: Hourly measurements
    - Dome_1_PPB_hourly, Dome_2_PPB_hourly, Dome_3_PPB_hourly, Dome_4_PPB_hourly, Dome_5_PPB_hourly, Dome_6_PPB_hourly, Dome_7_PPB_hourly, Dome_8_PPB_hourly (ozone in ppb)
    - ambient_Temp_degC: Ambient dome temperature (°C)
    - Light_micromolm2s1: Light intensity (μmol m^-2 s^-1)
    - ambient_RH: Ambient relative humidity (%)
    - D2_T, D2_RH: Temperature (°C) and RH in heated Dome 2
    - D4_T, D4_RH: Temperature (°C) and RH in heated Dome 4
    - D6_T, D6_RH: Temperature (°C) and RH in heated Dome 6

## Provenance and contacts
- Main point of contact: Hayes, F.J. (UKCEH); fhay@ceh.ac.uk
- Other authors: Katrina Sharps (katshar@ceh.ac.uk)

## Access, reuse, and governance considerations
- Data are documented with dataset-level descriptions, variable definitions, and units to facilitate discovery and reuse.
- Clear naming conventions for datasets and explicit metadata in this supporting documentation support data governance, provenance, and future integration with broader data systems.
- Users should reference the two CSV files by name and consult the QA notes and gap information when analyzing data.