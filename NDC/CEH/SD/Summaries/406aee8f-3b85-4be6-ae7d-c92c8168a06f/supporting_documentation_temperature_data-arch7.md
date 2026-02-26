# Hourly water temperature of 16 experimental mesocosms and air temperature from April to November 2023

## Overview
- Time period: 21 April to 7 November 2023 (GMT).
- Measurements: hourly water temperature for mesocosms 5–12 and 21–28; and air temperature.
- Purpose: dataset from UKCEH mesocosm facility to study effects of nutrient treatments and warming on aquatic temperatures.
- Data status: raw data with basic visual quality checks; not yet calibrated or fully quality controlled.

## Location and experimental design
- Setting: North West England, mesocosm facility; water sourced from Windermere.
- Mesocosm setup: 1 m deep, 2 m diameter tanks; labeled 1–32 but only 5–12 and 21–28 used in this experiment.
- Treatments: different nutrient ratio treatments (phosphate and nitrate additions).
- Air temperature reference: measured at a weather station within the mesocosm compound.

## Sensors and data collection
- Water temperature: two platinum resistance thermometers (PRTs) per mesocosm, shaded by a plastic cover; positioned around mid-depth (≈40 cm) and offset ~30 cm from the side wall; logged by a Campbell Scientific Data Logger.
- Air temperature: measured with a Vaisala WXT520 at ≈2.7 m height.
- Sampling interval: 5-minute measurements; hourly average is computed from the 5-minute data (hourly value is the mean of 60 records).

## Data structure and format
- Data file format: comma-separated values (CSV).
- Columns included:
  - Date (dd/mm/yyyy)
  - Hour (0-23)
  - T5 to T12 (water temperatures for mesocosms 5–12)
  - T21 to T28 (water temperatures for mesocosms 21–28)
  - AirT (air temperature in °C)
- Time zone: GMT.
- Notes on data columns: values are hourly averages derived from 5-minute readings.

## Quality control and processing
- Data type: raw data; no calibration applied yet.
- Quality checks:
  - Visual inspection to remove obvious hardware errors.
  - If the two water-temperature sensors for a mesocosm differ by <0.2 °C, the values are averaged.
  - If the difference >0.2 °C, data are checked against the overall average from each data logger; if drift is detected (one sensor anomalously high or low), that sensor is ignored and data from the remaining sensor used for those intervals.
- Documentation note: “Number of occasions” of single-sensor data are recorded in accompanying documentation (table referenced but not included here).

## Data availability and limitations
- Air temperature data gap: missing from 17 August to 6 September due to sensor downtime.
- General limitations: raw data not yet calibrated; gaps due to sensor or logger problems; any large discrepancies flagged and addressed as described above.

## Potential GIS applications
- Time-series visualization by mesocosm across space (mesocosm IDs map to spatial locations within the facility).
- Spatial comparison of temperature dynamics under different nutrient treatments.
- Integration with auxiliary data (e.g., nutrient treatment, environmental context) for predictive mapping and choropleth or isotherm-type visualizations.
- Use as baseline for calibrating modelled temperature fields in controlled aquatic experiments.

## Funding and references
- Funding: European Union Horizon 2020 AQUACOSM-plus (grant agreement No 871081) and NERC highlight topic NE/X00497X/1.
- Reference: Feuchtmayr H, et al. (2019) Effects of brownification and warming on algal blooms, metabolism and higher trophic levels in productive shallow lake mesocosms. Science of the Total Environment, 678, 227-238. DOI: https://doi.org/10.1016/j.scitotenv.2019.04.105