# Summary Description of experiment location - Rural site in North Wales, UK

## Overview
- Rural experimental site in North Wales, part of Bangor University farm, near the sea.
- Eight solardomes (hemispherical glasshouses) used in 2019; three heated to +7°C to simulate tropical/subtropical conditions.
- Ozone is added according to a set weekly profile, controlled by LabView; exposure occurs day and night.
- Watering provided as needed; ozone exposure ends at different times for different species.
- Experimental design includes multiple species/cultivars with replication and hourly monitoring of ozone and meteorological conditions.

## Experimental Design and Sampling
- Four replicate pots per species/cultivar, grown from seed.
- Ozone and meteorological data logged continuously on an hourly basis.
- Ad-hoc measurements of stomatal conductance, with accompanying soil moisture and chlorophyll content index.
- End-of-study biomass/yield measured for all species/cultivars.
- Species and exposure timelines vary by plant type (start 13/06/2019 for most; end dates range to 01/10/2019 for several).

## Treatments
- Low ozone, heated: target peak 35 ppb, ambient temperature +7°C.
- Medium ozone, heated: target peak 80 ppb, ambient temperature +7°C.
- High ozone, heated: target peak 115 ppb, ambient temperature +7°C.

## Data Collected and Data Files
- Ozone and Meteorology data (Ozone_and_meteorology_2019.csv):
  - 11 columns, 10008 rows.
  - Hourly measurements: Day_of_Year, Date, Hour_of_Day, Ozone_ppb (hourly mean), Light in dome 7 PAR, Temperature_C, Vapour_Pressure_Deficit_kPa, Air_pressure_kPa (constant placeholder), Windspeed_m/s (constant), Precipitation_mm (dummy 1 mm/h for model runs).
  - Used to run the DO3SE ozone flux model; notes on constant wind and dummy precipitation.
- Plant Physiology data (Plant_Physiology_2019.csv):
  - 12 columns, 692 rows.
  - Measurements include stomatal conductance among others; data available only for sweet potato.
  - Blank cells indicate readings not taken.
- Biomass and Yield data (Biomass_and_Yield_2019.csv):
  - 11 columns, 63 rows.
  - Bean yield per pot; tuber yield for sweet potato; some pots may have zero pods.

## Data Collection and Instrumentation
- Ozone and meteorology: solardome ozone exposure system controlled by National Instruments LabView.
- Stomatal conductance: AP4 porometer.
- Soil moisture: hand-held theta probe.
- Chlorophyll content index: CCM-200 device.

## Calibration and Quality Control
- AP4 porometer calibrated daily per manufacturer guidelines.
- Ozone analysers calibrated by an external provider (Air Monitors Ltd).
- CCM-200 autocalibration during startup.
- Data quality checks include plausibility, range checks, and outlier screening.

## Gap Filling and Data Integrity
- Gaps in hourly data addressed with a defined protocol; original data kept separately as an amended copy.
- Procedure:
  - Ensure 24 hourly data points exist for each day.
  - Gaps ≤5 consecutive hours: fill with average of surrounding values.
  - Gaps >5 hours: consult lab book; fill using values from same time on adjacent days, adjusted to maintain pattern; if system downtime prevents values, fill with a dummy value of 5 ppb for missing ozone.
  - Validate data to identify unrealistic values (e.g., negative values set to zero).
  - All modifications documented as a separate “filled and corrected” dataset.

## Data Resource Structure and Access
- Three CSV files comprising the dataset:
  - Plant_Physiology_2019.csv (12 columns, 692 rows; sweet potato only)
  - Ozone_and_meteorology_2019.csv (11 columns, 10008 rows)
  - Biomass_and_Yield_2019.csv (11 columns, 63 rows)
- Additional resources: facility description at CEH website linked in the documentation.

## Analysis Status and Limitations
- No analyses have been performed on these data yet.
- Plant physiology data limited to sweet potato; other species/cultivars may lack certain measurements.
- Some measurements are ad-hoc and not uniformly available across all time points or species.

## Miscellaneous
- Facility overview: Solardomes and ozone field release system described at the CEH website.