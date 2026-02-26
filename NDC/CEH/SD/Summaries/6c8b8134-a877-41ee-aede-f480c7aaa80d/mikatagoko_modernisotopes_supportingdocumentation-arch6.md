# Stable oxygen and hydrogen isotope composition of precipitation, river water and lake water in the Five Lakes of Mikata catchment, 2011-2012 and 2020-2022 - SUPPORTING DOCUMENTATION

## Overview
- Dataset on stable isotopes in water: δ18O, δ2H and d-excess for precipitation, river water, and lake water.
- Sampling spans two periods: March 2011–January 2012 and July 2020–July 2022.
- Accompanying data include total precipitation and average temperature during each subsampling period.
- Lake Suigetsu water column data (temperature and salinity with depth) across six dates within the 2020–2022 interval.
- Objective: assess whether catchment water isotopic composition reflects East Asian Monsoon variability.

## Dataset scope and contents
- Samples: 463 lake/river water samples collected weekly during 2011–2012 and 2020–2022.
- Precipitation samples: 120 event-based samples collected July 2020–July 2022.
- Water column data: depth-resolved profiles for Lake Suigetsu on six dates (temperature and salinity).
- Weather context: automated Netatmo weather station providing temperature, humidity, precipitation, and wind data to accompany isotope data.
- Data files:
  - mikatagoko_modernisotopes_results.csv: isotope data plus precipitation and average temperature for precipitation samples.
  - lakesuigetsu_tempsalinity_results.csv: depth- and date-related temperature and salinity data for Lake Suigetsu.

## Collection and generation methods
- Water sampling (lake/river): Hasu River, Lake Mikata, Lake Suigetsu; top ~50 cm sampled weekly. Monitoring locations changed between periods (within same depth range) to accommodate accessibility; samples filtered if algae present.
- Rainwater sampling: 3D-printed funnel system with glass bottles and silicon oil to prevent evaporation; event-based sampling; snowfall samples collected from pristine snow areas.
- Additional meteorological data: Netatmo weather station for temperature, humidity, precipitation, wind.
- Lake water column profiling: ~quarterly sampling dates; sampling every 2 m from surface to 10 m, every 5 m to 30 m, then every 2 m to 34 m; Van Dorn bottle used to minimize mixing; Hydrolab DS5 for temperature and salinity on most dates; high-resolution data for select dates; lower-resolution data included for August 2021.

## Isotope measurements and calculations
- δ18O: measured with Isoprime 100 IRMS using CO2 equilibration; samples equilibrated for 12–37 hours; calibrated to VSMOW2 using internal standards CA-HI and CA-LO; typical SD < 0.05 ‰.
- δ2H: measured in duplicate with TC-EA-IRMS after high-temperature conversion; samples corrected against VSMOW using CA-HI/CA-LO; typical SD < 0.5 ‰.
- Data are expressed as δ18O and δ2H relative to VSMOW; d-excess calculated as δ2H − ⟨8 × δ18O⟩ (as described in the methods).
- Precipitation data include total precipitation during the observation period and average temperature, derived from the Netatmo data where applicable.

## Sampling locations and codes
- Locations include Hasu River, Mikata, Suigetsu, and associated reference codes (e.g., HASU11, MIKATA11, SUIGETSU11, with notes on accessibility during 2020–2022).
- A location table provides coordinates and notes for each sampling site, including adjustments for accessibility and special conditions (e.g., algal growth, lake depth references).

## Quality control and data quality
- Data corrected by comparison to laboratory standards.
- Potential influencing factors: precipitation characteristics, transit/evaporation effects, interactions between lake systems and the Sea of Japan.
- 2011–2012 precipitation and water-column data are not accompanied by some weather or column data, due to the pilot nature of that period.

## Data structure and units
- mikatagoko_modernisotopes_results.csv:
  - Columns cover sample type, batch, sample code, location, sampling position, sampling depth (for column samples), dates and times, corrected δ18O and δ2H (relative to VSMOW2), calculated d-excess, precipitation data (total precipitation, average temperature) for the period (when applicable).
- lakesuigetsu_tempsalinity_results.csv:
  - Columns include sampling date, sampling depth, water temperature (°C), and water salinity (%).
- Data fields include explicit units and descriptive notes for interpretation (e.g., whether a sample is from lake/river surface, column depth, or precipitation; depth and date references).

## Potential uses and considerations
- Analyses of how catchment isotopic signatures respond to East Asian Monsoon variability.
- Cross-period comparisons (2011–2012 vs 2020–2022) to identify hydrological or climatic shifts.
- Integration with precipitation and temperature data to model isotope behavior in shallow and deep water bodies.
- Suitable for researchers studying hydrology, isotope geochemistry, climate variability, and water resource management in the Mikata catchment.
- Users should consider sampling location changes and data gaps in 2011–2012 when interpreting temporal trends.