# Summary Description of experiment location - Rural site in North Wales, UK.

## Overview
- Ozone exposure experiment conducted at a rural site near Bangor University, North Wales, UK, adjacent to the sea.
- Eight solardomes were used in 2018; three of these domes were heated (+7°C) to mimic tropical/subtropical conditions.
- Ozone was added according to a weekly, computer-controlled profile (LabView), with exposure during both day and night.
- Four replicate pots per species/cultivar; exposure timings varied by species due to differing growing seasons.
- Plant biomass and physiology data are available only for the three heated domes.

## Experimental Design and Treatments
- Location: Rural site, coordinates 53°14'N, 4°01'W, elevation 15 m.
- Domiciles: Eight solardomes; three heated to simulate warmer conditions; five unheated.
- Ozone treatments: Varied levels (low/medium/high) with target peak concentrations and ambient temperature conditions; heating was implemented in half of the domes.
- Exposure duration: Different across species/cultivars, ending at different times for each species.
- Measurements during exposure: Ad-hoc stomatal conductance measurements, alongside soil moisture and chlorophyll content index.

## Treatments Details (Summary)
- Treatments combined ozone concentration levels (low/medium/high) with dome heating status (heated vs unheated) and ambient vs elevated temperature profiles.
- Three heated domes provided the detailed plant biomass and physiology data.

## Data Collected
- Ozone and meteorological data: Hourly measurements logged automatically; QA checks performed; gaps filled as needed.
- Plant physiology data: Ad-hoc measurements (stomatal conductance, chlorophyll content index, soil moisture, etc.) with QA checks.
- Biomass and yield data: End-of-experiment biomass and yield metrics for all species/cultivars; some crops had limited yield data (e.g., Amaranth seed heads only).

## Instrumentation and Calibration
- Ozone and meteorology: Logged via LabView-controlled system; external QA checks.
- Stomatal conductance: AP4 porometer (Delta-T), calibrated daily.
- Soil moisture: Theta probe (Delta-T).
- Chlorophyll Content Index: CCM-200 (OptiSciences) with autocalibration.
- Ozone analysers: Calibrated by external supplier.

## Data Resource Structure
- Biomass_and_Yield_2018.csv
  - 14 columns; end-of-season yield/biomass metrics; notes on certain measurements (e.g., Amaranth seed heads only).
- Ozone_and_meteorology_2018.csv
  - 11 columns; hourly ozone, DOY, date, time, meteorological variables; includes DO3SE-model inputs (wind speed, pressure, precipitation dummy).
- Plant_Physiology_2018.csv
  - 12 columns; measurements by treatment/species/date/time, including stomatal conductance, light, temperature, soil moisture, and chlorophyll index.

## Data Quality Control and Processing
- Quality assurance applied to all data: range checks, plausibility checks, and outlier screening.
- Gap filling (Appendix 1) for ozone/met data:
  - Ensure 24 hourly records per day.
  - Gaps ≤ 5 consecutive hours: fill with the average of adjacent values.
  - Larger gaps: consult lab book; fill using previous/next day values, adjusted to preserve patterns; in non-operational periods, fill with a 5 ppb dummy value.
  - Anomalous values identified and replaced using neighboring data (e.g., negative values set to zero).
- Data integrity: Original and gap-filled datasets maintained separately; all changes documented.

## Appendix: Gap Filling Procedure (Key Points)
- Maintain an original amended copy; record all changes.
- If gaps ≤ 5 hours, interpolate from surrounding values.
- If gaps > 5 hours, use same time on adjacent days, adjusted to reflect patterns; otherwise, use a reasonable proxy (e.g., 5 ppb during non-operation).
- Mark and review anomalous readings before substitution.

## Analytical Status and Considerations
- No formal analysis has been performed on these data yet.
- Data are suitable for modelling ozone fluxes (DO3SE) and for exploring plant physiological responses across treatments.
- Potential limitations:
  - Biomass/physiology data limited to the three heated domes.
  - Some measurements missing (e.g., certain readings in Plant_Physiology_2018.csv; photosynthetically active radiation gaps).
  - DO3SE inputs rely on assumed wind and pressure values for the site.

## Miscellaneous
- Further details about the experimental facility available at: https://www.ceh.ac.uk/our-science/research-facilities/solardomes-and-ozone-fieldrelease-system