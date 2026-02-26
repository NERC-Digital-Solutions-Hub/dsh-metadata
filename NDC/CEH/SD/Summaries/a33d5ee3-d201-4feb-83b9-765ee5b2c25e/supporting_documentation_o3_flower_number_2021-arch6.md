# Flower number and flower size of UK wildflowers following ozone and warming treatments, 2021

## Overview
- Study assessing effects of ozone exposure and warming on flowering abundance and flower size for UK wildflowers in a controlled solardome facility in North Wales, UK (Abergwyngregyn).
- Species included: Birdsfoot trefoil (Lotus corniculatus), White clover (Trifolium repens), Clustered bellflower (Campanula glomerata), Catsear (Hypochaeris radicata), Harebell (Campanula rotundifolia).
- Experimental design combines eight solardomes with varying ozone peak levels and warming conditions (ambient vs heated by +4°C for some domes) across multiple treatment profiles.
- Data products intended for end users include per-pot flower counts and flower widths, plus hourly environmental data to support further analyses and self-serve exploration.

## Experimental design and site
- Location: Rural solardomes site in North Wales (Abergwyngregyn), coordinates 53°14'N, 4°01'W, elevation ~15 m.
- Experimental setup: Eight solardomes equipped with charcoal-filtered air; ozone added via a programmed weekly profile (LabView) with nighttime and daytime dosing.
- Treatments:
  - Ozone profiles by dome (e.g., Dome_3 with 30 ppb, Dome_7 with 50 ppb, Dome_8 with 65 ppb, Dome_1 with 80 ppb, Dome_5 with 110 ppb) and ambient temperature.
  - Warming: Three domes heated by +4°C above ambient.
  - Some domes feature a combination of ozone and warming (e.g., Dome_6 and Dome_2 include +4°C warming with specified ozone levels).
- Ten replicate pots per species per treatment; plants started as plug plants and exposed to treatments from 1 June to 24 October 2021.
- Data collection: Ozone and meteorological conditions monitored hourly; separate ambient and heated dome measurements.

## Data files and structure

### 1) Solardomes_flower_data_2021.csv
- Type: Flowering data by treatment and pot.
- Structure: 14 columns (A–N) across 32 data rows + 1 header row.
- Key columns:
  - A. Month: Month of measurement
  - B. Warming_treatment: ambient or heated
  - C. Ozone_treatment: weekly peak ozone level (ppb)
  - D. Dome_number: solardome identifier
  - E–N: Flower metrics for each species (mean flowers per pot; mean flower width per pot in mm)
    - Examples: Trefoil_flower_number_mean_per_pot, Trefoil_flower_width_mean_per_pot_mm, White_clover_flower_number_mean_per_pot, etc.
- Purpose: Provides per-pot mean flower counts and widths for each species under each treatment combination.

### 2) 2021_Ozone_hourly.csv
- Type: Hourly ozone and environmental data by dome.
- Structure: 19 columns (A–S) with 3527 data rows + 1 header row.
- Key columns:
  - A. Day: Date of measurement
  - B. Hour_of_day: Hour index (0–23)
  - C–R: Hourly ozone concentrations (ppb) for Domes 1–8
  - K. ambient_Temp_degC: Ambient dome temperature (°C)
  - L. Light_micromolm2s1: Light intensity (µmol m^-2 s^-1)
  - M. ambient_RH: Ambient relative humidity (%)
  - N–S: D2_T, D2_RH, D4_T, D4_RH, D6_T, D6_RH (hourly temperature and RH in heated domes 2, 4, and 6)
- Purpose: Provides hourly ozone exposure and associated environmental variables necessary to contextualize flowering responses and support data integration.

## Data quality and QA
- Plant data: Manual data collection with quality assurance to ensure values fall within plausible ranges; outlier plausibility checks performed.
- Ozone and meteorological data: Automatically logged with QA to verify reasonable ranges, plausibility of outliers, and gap-filling where needed.
- Data gaps:
  - Flowering dataset contains gaps where no flowers were present for a given treatment.
  - Meteorological dataset has initial gaps due to system failure at the start of the time series.

## Data structure details and units
- Flower data file:
  - 14 columns (A–N): includes four treatment descriptors (Month, Warming_treatment, Ozone_treatment, Dome_number) plus ten flower metrics (per-pot means for flower number and flower width across five species).
  - Values include counts (flowers per pot) and widths (mm).
- Hourly ozone/environment data file:
  - 19 columns (A–S): date, time, hourly ozone concentrations per dome (ppb) plus ambient and heated-dome environmental metrics (°C for temperature, % RH, and light in µmol m^-2 s^-1).
- Scale and resolution:
  - Flower data: summarized per pot per measurement period.
  - Ozone/environment data: hourly resolution across eight domes plus ambient conditions.

## Challenges and considerations for data users
- Patchy flowering data gaps may limit certain per-treatment inferences and require imputation or exclusion of missing periods.
- Ozone exposure is integrated with warming in several domes; careful alignment of hours, dates, and treatment descriptors is needed when merging datasets.
- Data gaps at the start of meteorological records should be accounted for during time-series analyses.

## Potential data products and use cases
- Self-serve dashboards or reports summarizing:
  - Effects of ozone concentration and warming on mean flower numbers and flower sizes per species.
  - Comparative analyses across domes and treatments to assess interaction effects.
- time-aligned datasets enabling correlation analyses between hourly ozone exposure and flowering outcomes.
- Data cleaning pipelines to standardize units, handle missing values, and join flowering metrics with corresponding environmental variables.

## Contact and provenance
- Main point of contact: Hayes, F.J. (UKCEH) - fhay@ceh.ac.uk
- Additional authors: Katrina Sharps (katshar@ceh.ac.uk)