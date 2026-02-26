# Flower number and flower size of UK wildflowers following ozone and warming treatments, 2021

## Overview
- A study dataset detailing how ozone exposure and warming affect flower number and flower size of UK wildflowers.
- Two main data files: Solardomes_flower_data_2021.csv (flower counts and widths) and 2021_Ozone_hourly.csv (hourly ozone and meteorological data).
- Collected in 2021 at the solardomes facility in North Wales, UK.
- Main contact: F.J. Hayes (UKCEH); co-author: Katrina Sharps.

## Experimental design and site
- Location: Abergwyngregyn, North Wales, UK (rural site, latitude 53°14′ N, longitude 4°01′ W, elevation 15 m).
- Setup: Eight solardomes with charcoal-filtered air; three heated domes (+4°C) for warming treatment; ozone added via a computer-controlled system (LabView) to create weekly ozone episodes (night and day).
- Duration: Treatments ran from 1 June to 24 October 2021.
- Species studied (five): Birdsfoot trefoil (Lotus corniculatus), White clover (Trifolium repens), Clustered bellflower (Campanula glomerata), Catsear (Hypochaeris radicata), Harebell (Campanula rotundifolia).
- Experimental design specifics: Domes configured with varying ozone levels (e.g., 30, 50, 65, 80, 110 ppb) and warming status (ambient vs heated). Example mappings include Dome_3 (30 ppb ambient), Dome_7 (50 ppb ambient), Dome_8 (65 ppb ambient), Dome_1 (80 ppb ambient), and Dome_5 (110 ppb ambient); Dome_6, Dome_2, and Dome_4 included heated conditions with corresponding ozone levels (e.g., 30 ppb ambient temp +4°C, 80 ppb ambient temp +4°C, 110 ppb ambient temp +4°C).
- Measurements: Hourly ozone and meteorological data collected in each dome; plant data collected manually with quality assurance.

## Data files and structure

- Solardomes_flower_data_2021.csv
  - Structure: 14 columns (A–N) and 32 data rows plus a header row.
  - Columns (sample): Month, Warming_treatment, Ozone_treatment, Dome_number, and for each species the mean flower number per pot and mean flower width per pot (per species: birdsfoot trefoil, white clover, clustered bellflower, catsear, harebell).
  - Data meaning: Mean values per pot for each measured parameter; includes both flower counts and flower widths.
  - Notes: Gaps occur in flowering data when no flowers were present in a treatment.

- 2021_Ozone_hourly.csv
  - Structure: 19 columns (A–S) and 3,527 data rows plus a header row.
  - Columns (sample): Day, Hour_of_day, and hourly measurements for each dome’s ozone concentration (Dome_1_PPB_hourly … Dome_8_PPB_hourly), plus ambient temperature (ambient_Temp_degC), light (Light_micromolm2s1), ambient relative humidity (ambient RH), and for heated domes: D2_T, D2_RH, D4_T, D4_RH, D6_T, D6_RH.
  - Data meaning: Hourly ozone concentrations by dome; accompanying meteorological and light data for ambient and heated domes.

## Quality control and limitations
- Data collection: Manual plant data with QA checks for plausible ranges; ozone and meteorological data automatically logged with QA checks and gap-filling as needed.
- Gaps: Flowering data has gaps where no flowers were present; meteorological data has startup gaps due to system failure.

## How this GIS-oriented data can be used
- Time-enabled visualizations of flower responses under varying ozone and warming treatments across eight spatially distinct domes.
- Spatial comparison of treatment effects by dome, mapped against coordinates and site context.
- Integration with hourly ozone and meteorological data for geospatial analyses of environmental drivers.
- Suitable for creating map-based data products and dashboards to explore spatial-temporal patterns in flowering metrics.