# Ozone_and_meteorology_2018.csv

- Overview
  - Rural site in North Wales, UK, part of Bangor University farm; near the sea.
  - Eight solardomes used in 2018; three heated domes (+7°C) to mimic tropical/subtropical conditions; ozone added according to a weekly repeating profile.
  - Ozone exposure guided by LabView control; measurements logged continuously at hourly resolution.
  - Four replicate pots per species/cultivar; end-of-exposure biomass/yield measured; stomatal conductance and other physiology data collected ad-hoc during exposure.
  - Treatments include variations in ozone level (low/medium/high), temperature (ambient vs +7°C), and heating status (unheated vs heated).

- Experimental Design and Sampling
  - Species/cultivar with four replicates per treatment; exposure lengths varied by species due to growing season.
  - Continuous logging of ozone and meteorological conditions; ad-hoc physiological measurements (stomatal conductance, soil moisture, chlorophyll content) during exposure.
  - End-of-period biomass and yield data collected for all species/cultivars.
  - Treatments labeled with abbreviations (e.g., Medium/High/Low ozone, heated/unheated, ambient temperature vs elevated).

- Data Collected and Instrumentation
  - Ozone and meteorology data logged by PC; QA checks for range, plausibility, and gaps; hourly timesteps.
  - Meteorological in dome: light (PAR), relative humidity, temperature, VPD, air pressure (synthetic values used for model input).
  - Plant physiology: stomatal conductance (AP4 porometer), soil moisture (theta probe), chlorophyll content index (CCI; CCM-200).
  - Biomass and yield: species-specific measurements at harvest; notes on pod/bean counts and weights; Amaranth data includes seed head metrics; Sorghum may include total biomass where yield not reached.

- Data Quality Assurance and Calibration
  - Ozone analysers calibrated by an external company.
  - AP4 porometer calibrated daily; CCM-200 autocalibration at startup.
  - QA processes applied to all data types; outliers checked for plausibility; data kept alongside original and corrected versions.

- Data Resource Structure and Content
  - Three CSV files:
    - Biomass_and_Yield_2018.csv: 14 columns; per-pot measurements including pod/bean counts and weights, total biomass, and yield indicators.
    - Ozone_and_meteorology_2018.csv: 11 columns; hourly records with treatment, DOY, date, hour, ozone (ppb), light, VPD, air pressure (synthetic), wind speed (constant), precipitation (dummy value), etc.
    - Plant_Physiology_2018.csv: 12 columns; per-measurement records including treatment, species, replicate, date/time, RH, stomatal conductance, light, temperature, soil moisture, CCI.
  - Data notes:
    - Blank cells indicate missing readings.
    - Some PAR measurements are missing due to sensor fault.
    - Wind speed is constant due to solardome airflow; air pressure not measured and replaced with a latitude/altitude estimate.
    - DOY/Date/Time fields structured to align with hourly model input.

- Gap Filling, Data Processing, and Provenance
  - Appendix 1 documents gap-filling approach for ozone and canopy data:
    - Ensure hourly coverage for each day; gaps ≤ 5 consecutive hours filled with average of surrounding values.
    - Larger gaps cross-checked against lab notes; where possible, values from previous/next day adjusted to preserve patterns; where the system was off, missing values filled with a dummy 5 ppb ozone value.
  - All data edits are tracked by producing a separate “filled and corrected” dataset to preserve originals.
  - Data integrity checks include handling of negative ozone values (set to zero) and flagging implausible values.
  - In cases of missing or faulty readings, calibration and validation steps are applied as per instrument manuals.

- Miscellaneous and Access
  - Reference: CEH Solardomes and ozone field release system facility description (website link provided in the data description).
  - Data are structured for reuse in ozone exposure research, including model input needs (e.g., DO3SE) and cross-referencing biomass/physiology responses.
  - Applicable for studying ozone impacts on multiple crops under controlled heating and ozone regimes, with robust QA and detailed metadata to support reproducibility.