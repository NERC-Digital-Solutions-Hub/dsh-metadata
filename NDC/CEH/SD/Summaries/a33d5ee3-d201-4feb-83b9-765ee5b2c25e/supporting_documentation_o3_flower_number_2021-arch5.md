# Flower number and flower size of UK wildflowers following ozone and warming treatments, 2021 Supporting documentation

## Overview
- Describes supporting data for a 2021 experimental study on how ozone and warming affect flower number and flower size in UK wildflowers.
- Conducted in eight solardomes at a rural site in North Wales (Abergwyngregyn, UK) with charcoal-filtered air and ozone manipulation.
- Experimental design includes eight domes, multiple ozone treatments, and a subset of heated domes (+4°C) to simulate warming.
- Datasets include per-pot flower measurements and hourly environmental/ozone data, with quality control and noted data gaps.

## Datasets and data structure
- Solardomes_flower_data_2021.csv
  - Structure: 14 columns (A–N), 32 rows + header.
  - Treatments/periods: Month, Warming_treatment, Ozone_treatment, Dome_number.
  - Flower metrics (per pot): 
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
- 2021_Ozone_hourly.csv
  - Structure: 19 columns (A–S), 3527 rows + header.
  - Time/conditioning: Day, Hour_of_day.
  - Ozone data by dome (hourly average, ppb): Dome_1_PPB_hourly, Dome_2_PPB_hourly, Dome_3_PPB_hourly, Dome_4_PPB_hourly, Dome_5_PPB_hourly, Dome_6_PPB_hourly, Dome_7_PPB_hourly, Dome_8_PPB_hourly.
  - Environmental covariates (hourly, across ambient/heated domes): ambient_Temp_degC, Light_micromolm2s1, ambient_RH.
  - Heated-dome measurements: D2_T, D2_RH, D4_T, D4_RH, D6_T, D6_RH.

## Site, design, and treatments
- Location and facility
  - Rural North Wales site (Abergwyngregyn), latitude 53°14'N, longitude 4°01'W, elevation 15 m.
  - Eight solardomes with controlled air and ozone addition; three domes heated by +4°C to create warming treatment.
- Experimental treatments
  - Ozone treatments (weekly profile, night and day): 
    - Dome_3: 30 ppb
    - Dome_7: 50 ppb
    - Dome_8: 65 ppb
    - Dome_1: 80 ppb
    - Dome_5: 110 ppb
  - Heated (warming) conditions:
    - Dome_6: 30 ppb, ambient + 4°C
    - Dome_2: 80 ppb, ambient + 4°C
    - Dome_4: 110 ppb, ambient + 4°C
  - Temperature and ozone management: 1 June 2021 to 24 October 2021; ozone added weekly via LabView-controlled system; nocturnal additions included.
- Replication and species
  - Ten replicate pots per species per treatment.
  - Species included: Birdsfoot trefoil (Lotus corniculatus), White clover (Trifolium repens), Clustered bellflower (Campanula glomerata), Catsear (Hypochaeris radicata), Harebell (Campanula rotundifolia).

## Data collection and quality control
- Flower data
  - Collected manually; QA checks for range plausibility; outliers assessed.
  - Gaps exist in flowering data where no flowers were present in a treatment.
- Ozone and meteorological data
  - Automatically logged with QA checks for range plausibility; gap-filling applied where necessary.
  - Some meteorological data gaps at dataset start due to system failure.
- Data provenance and documentation
  - Main point of contact: F.J. Hayes, UKCEH; authors include Katrina Sharps.
  - Documentation includes explicit definitions of each column’s meaning and units.

## Data standards, units, and structure details
- Flower data file (Solardomes_flower_data_2021.csv)
  - Columns include Month, Warming_treatment, Ozone_treatment, Dome_number, followed by 10 species-specific metrics (flower number and width per pot for five species).
  - Units: flower numbers are simple counts per pot; flower width is in millimeters.
- Hourly ozone/meteorology data file (2021_Ozone_hourly.csv)
  - Columns include Day, Hour_of_day, hourly ozone concentrations for each dome (ppb), ambient temperature (°C), light (micromol m^-2 s^-1), ambient relative humidity (%), and heated-dome T/RH values (°C and %RH) for Domes 2, 4, and 6.
  - Units: ppb for ozone; °C for temperatures; %RH for relative humidity; micromol m^-2 s^-1 for light.

## Governance and reuse considerations
- Contact and provenance
  - Main contact: Hayes, F.J. (fhay@ceh.ac.uk); UKCEH; co-authors listed.
- Data stewardship aspects
  - The datasets have documented QA processes, explicit data structures, and known data gaps.
  - The documentation highlights potential interoperability challenges due to multiple domes, formats, and legacy systems; recommended attention to metadata consistency and dataset updates.
- Limitations and caveats for users
  - Incomplete picture of full user needs may apply; data may require alignment to other datasets for broader meta-analyses.
  - Data gaps in flowering records and early meteorological records should be accounted for in analyses.