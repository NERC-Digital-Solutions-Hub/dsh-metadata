# Summary

## Context and Purpose
- Rural site in North Wales, UK, part of Bangor University farm; eight solardomes used for 2017 experiments to study ozone effects on plants.
- Ozone applied via a computer-controlled system (LabView) following a weekly profile; ozone added at night and day.
- Three heated solardomes (ambient +7°C) provide tropical/subtropical condition data; associated plant biomass and physiology data available only for these heated domes.
- Data are structured to enable self-service analysis and cross-dataset comparisons.

## Experimental Design and Treatments
- Four replicate pots per species/cultivar.
- Ozone and meteorological conditions logged hourly; ad-hoc plant physiology measurements (stomatal conductance, soil moisture, chlorophyll content) also collected.
- Treatment combinations (per dome and species) include:
  - Low ozone, unheated (35 ppb)
  - Medium ozone, unheated (80 ppb)
  - High ozone, unheated (115 ppb)
  - Low ozone, heated (+7°C)
  - Medium ozone, heated (+7°C)
  - High ozone, heated (+7°C)
- Exposure periods varied by species due to growing season; end-of-study yield measured for all.

## Data Collected and Measurements
- Three main datasets:
  - Plant_Physiology_2017.csv: measurements by species, pot, date/time; includes stomatal conductance, photosynthetically active radiation (PAR), leaf temperature, soil moisture, chlorophyll content index.
  - Ozone_and_meteorology_2017.csv: hourly records of Treatment, Day of Year, Date, Hour, Ozone_ppb, PAR, temperature, vapour pressure deficit, air pressure, wind speed, precipitation.
  - Biomass_and_Yield_2017.csv: yield-related metrics per pot (pod/bean data, weights, grain counts) and derived metrics (e.g., average pod weight, grains per ear).
- Instrumentation and measurements were QA’d for plausibility; some blanks indicate missing readings.

## Data Quality, Calibration, and Documentation
- Ozone and meteorology data logged automatically; QA ensures value plausibility; gap-filled where necessary.
- Plant physiology data collected ad-hoc; QA checks data ranges and outliers.
- Calibration:
  - AP4 porometer calibrated daily for stomatal conductance measurements.
  - Ozone analyzers calibrated by external provider.
  - CCM-200 chlorophyll index autocalibration during startup.
- Field instruments and software:
  - Solardomes ozone system controlled by LabView.
  - Stomatal conductance: AP4 porometer; soil moisture: theta probe; chlorophyll index: CCM-200.
- DO3SE model inputs require constant values for air pressure, wind speed, and a dummy 1 mm/hr precipitation; these are set accordingly in the dataset.

## Gap Filling and Data Transformation
- Gaps due to power failures or logging issues are addressed with a documented protocol that preserves original data while creating filled and corrected copies.
- Gap filling rules:
  - Ensure 24 hourly rows per day; gaps ≤5 hours filled using the average of surrounding values.
  - Larger gaps: fill using previous and next day values, or adjusted values to maintain patterns.
  - When ozone system was off, missing values represented by a dummy 5 ppb value.
- All data alterations are logged; new worksheets/files labeled as filled and corrected.

## Data Resource Structure and Accessibility
- Three CSV files with:
  - Plant_Physiology_2017.csv: 11 columns, 3112 rows (some missing values).
  - Ozone_and_meteorology_2017.csv: 11 columns, 18534 rows (gaps filled; some periods not logged).
  - Biomass_and_Yield_2017.csv: 17 columns (yield and biomass data; blanks indicate missing readings).
- Column headings and units are defined within each file (e.g., Ozone_ppb in ppb, PAR in umol/m2/s, leaf temperature in °C).

## Miscellaneous
- Facility overview: detailed description available at the CEH Solar Domes and Ozone Field Release System page.
- Data readiness for reuse:
  - Clear data provenance, QA steps, calibration records, and gap filling procedures support reliable secondary analyses.
  - Data are suitable for analyses of ozone effects on plant physiology, biomass, and yield, as well as cross-dataset integration (physiology, environmental conditions, and outcomes).