# Flower number and flower size of UK wildflowers following ozone and warming treatments, 2021 Supporting documentation

## Study purpose and scope
- Investigates how ozone exposure and warming affect flower number and flower size in UK wildflowers.
- Uses controlled solardome experiments to apply ozone and temperature treatments to multiple plant species.
- Presents details on experimental design, site, species, data collection, quality control, and data structure for two datasets.

## Experimental design and site
- Location: rural site at Abergwyngregyn, North Wales, UK (53°14'N, 4°01'W, ~15 m a.s.l.).
- Facilities: eight solardomes with charcoal-filtered air; ozone added as required.
- Treatments and replication:
  - Ten replicate pots per species per treatment.
  - Ozone exposure with weekly profiles (night and day), controlled by LabView.
  - Warming treatment: three solardomes heated +4°C above ambient.
  - Treatment period: 1 June 2021 to 24 October 2021.
- Species studied:
  - Birdsfoot trefoil (Lotus corniculatus)
  - White clover (Trifolium repens)
  - Clustered bellflower (Campanula glomerata)
  - Catsear (Hypochaeris radicata)
  - Harebell (Campanula rotundifolia)

## Treatments by dome
- Dome_3: ozone ~30 ppb, ambient temperature
- Dome_7: ozone ~50 ppb, ambient temperature
- Dome_8: ozone ~65 ppb, ambient temperature
- Dome_1: ozone ~80 ppb, ambient temperature
- Dome_5: ozone ~110 ppb, ambient temperature
- Dome_6: 30 ppb with warming (+4°C)
- Dome_2: 80 ppb with warming (+4°C)
- Dome_4: 110 ppb with warming (+4°C)

## Data collection and measurements
- Flower data:
  - Collection method: manual counting/measurement of flowers per pot and mean flower width per pot for each species.
  - Data file: Solardomes_flower_data_2021.csv (14 columns, 32 rows, 1 header row).
- Ozone and meteorological data:
  - Continuous hourly data collection for ozone and meteorological variables.
  - Data file: 2021_Ozone_hourly.csv (19 columns, 3527 rows, 1 header row).
  - Ambient dome measurements (light, temperature, RH) captured hourly; heated domes collected in parallel for D2, D4, D6 with their own T and RH.

## Data structure and key variables
- Solardomes_flower_data_2021.csv:
  - Columns A-D describe Month, Warming_treatment, Ozone_treatment, Dome_number.
  - Columns E-N include mean flower numbers and mean flower widths per pot for:
    - Trefoil_flower_number_mean_per_pot
    - Trefoil_flower_width_mean_per_pot_mm
    - White_clover_flower_number_mean_per_pot
    - White_clover_flower_width_mean_per_pot_mm
    - Bellflower_flower_number_mean_per_pot
    - Bellflower_flower_width_mean_per_pot_mm
    - Catsear_flower_number_mean_per_pot
    - Catsear_flower_width_mean_per_pot_mm
    - harebell_flower_number_mean_per_pot
    - harebell_flower_width_mean_per_pot_mm
- 2021_Ozone_hourly.csv:
  - Columns A-B: Day and Hour_of_day.
  - Columns C-S: Hourly ozone concentrations (Dome_1_PPB_hourly, Dome_2_PPB_hourly, …, Dome_8_PPB_hourly) and meteorological/two more variables:
    - ambient_Temp_degC
    - Light_micromolm2s1
    - ambient_RH
    - D2_T, D2_RH
    - D4_T, D4_RH
    - D6_T, D6_RH

## Quality control and data availability
- Data QA:
  - Plant data: manual QA for plausible ranges and outliers.
  - Ozone and meteorology: automated QA with range checks, plausibility checks, and gap-filling as needed.
- Data gaps:
  - Flowering data have gaps where no flowers were present in a treatment.
  - Meteorological data have initial gaps due to system failure at dataset start.
- Data management:
  - Data collected with documentation of methods and treatments.
  - Datasets intended to be discoverable with metadata for reuse.