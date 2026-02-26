# Hourly water temperature of 16 experimental mesocosms and air temperature from April to November 2023

## Overview
- Dataset of hourly water temperature for 16 mesocosms (numbers 5–12 and 21–28) and concurrent air temperature.
- Time period: 21 April to 7 November 2023.
- Location: North West England, UK; mesocosms filled with ~2800 L water from Windermere; nutrient treatments applied (phosphate and nitrate).

## Sampling design and environment
- Mesocosm facility: UKCEH mesocosms.
- Mesocosms: 1 m depth, 2 m diameter.
- Water temperature measured with two platinum resistance thermometers (PRTs) shielded by a plastic cover, positioned mid-depth (~40 cm) and offset ~30 cm from the side wall.
- Air temperature measured at a Vaisala weather transmitter (WXT520) ~2.7 m above ground within the mesocosm compound.
- Nutrient treatment variations implemented (phosphate and nitrate ratios).

## Data collection and sensors
- Water temperature channels: T5–T12 and T21–T28 (total of 16 sensors).
- Data logger: Campbell Scientific Data Logger.
- Data granularity: 5-minute measurements; hourly values calculated as the average of measurements within each hour (e.g., 1 p.m. hour averages 1:00–1:55 p.m.).

## Data processing and handling
- Time zone: all data in GMT.
- Hourly data derived from 5-minute data.
- Temperature reconciliation: if the two sensors for a mesocosm differed by <0.2 °C, their values were averaged. If the difference >0.2 °C, data were checked against the overall logger average; if a sensor drifted, the drifting sensor was ignored for those occasions, resulting in single-sensor data for those hours.
- Example note: counts of single-sensor hourly data are provided for specific mesocosms (e.g., mesocosm 11 had 231 single-sensor occasions; mesocosm 12 had 1594).

## Quality control and data handling
- Data are raw and not yet calibrated or fully quality controlled.
- Visual checks performed; obvious hardware malfunctions removed.
- Data gaps attributed to sensor or logger problems.

## Data format and fields
- File format: comma-separated values (CSV).
- Columns:
  - Date (dd/mm/yyyy)
  - Hour (0–23)
  - T5, T6, T7, T8, T9, T10, T11, T12 (water temperatures for mesocosms 5–12)
  - T21, T22, T23, T24, T25, T26, T27, T28 (water temperatures for mesocosms 21–28)
  - AirT (air temperature in °C)
- All temperature values in degrees Celsius; times in GMT.

## Data availability and gaps
- Coverage: 21 April – 7 November 2023 for water and air temperatures.
- Air temperature data gap: 17 August – 6 September 2023 due to a sensor restart.

## Usage notes
- Suitable for examining temperature dynamics and cross-mensor patterns, and for relative comparisons or trend analyses within the uncalibrated dataset.
- When combining with other data (e.g., nutrient treatments), consider the lack of calibration and potential sensor drift adjustments.

## Funding and references
- Funding: European Union Horizon 2020 AQUACOSM-plus (grant No 871081) and NERC highlight topic grant NE/X00497X/1.
- Reference: Feuchtmayr H, Pottinger TG, Moore A, et al. 2019. Effects of brownification and warming on algal blooms, metabolism and higher trophic levels in productive shallow lake mesocosms. Science of the Total Environment, 678, 227-238.