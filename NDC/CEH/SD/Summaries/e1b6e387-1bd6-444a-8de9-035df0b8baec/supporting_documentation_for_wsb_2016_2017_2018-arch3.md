# Hourly data (air temperature, solar radiation, wind speed and lake temperature profile) from automatic water monitoring buoy from Windermere South Basin 2016 to 2018. Feuchtmayr, H., Jones, I.D., Clarke, M., Maberly S.C. (2021)

## Overview
- This dataset comes from an automatic lake monitoring buoy in Windermere South Basin, Cumbria, England.
- Measurements cover air temperature, solar radiation, wind speed, and lake water temperature profiles at multiple depths.
- Data are provided as hourly averages derived from high-frequency (every 4 minutes) measurements.
- Time reference is GMT, with data spanning 2016–2018.

## Sampling Regime and Collection Methods
- Instrument suite includes meteorological sensors and in-lake temperature probes.
- Water temperatures are recorded at depths of 1, 2, 4, 7, 10, 13, 16, 19, 22, 25, 30, and 35 meters.
- Units: air temperature (degrees C), solar radiation flux (W/m^2), wind speed (m/s), water temperatures (degrees C).
- Data collection interval: every 4 minutes; hourly averages computed in an Oracle database.
- Example calculation: the hourly value at 2 p.m. uses data from 1–2 p.m., excluding 1 p.m. data and including 2 p.m. data.

## Quality Control
- The presented data are raw and not yet calibrated or fully quality controlled.
- Visual checks performed; obvious hardware-related errors removed.
- Data gaps occur due to buoy maintenance or sensor/logger problems.

## Data Structure
- Format: comma separated values (CSV).
- Columns include:
  - Date GMT
  - Water temperature at 1m, 2m, 4m, 7m, 10m, 13m, 16m, 19m, 22m, 25m, 30m, 35m
  - Air Temperature
  - Pyranometer (solar radiation flux in W/m^2)
  - Wind Speed (m/s)

## Data Availability and Use
- Data are suitable for high-frequency environmental monitoring analyses and long-term trend studies when calibrated.
- Metadata such as depth levels, units, and GMT reference are explicitly defined in the dataset.
- The dataset has supported recent research and publications.

## Metadata and Data Governance Considerations
- Data are raw and require calibration and formal QA/QC before broad policy or decision-making use.
- Gaps and calibration status highlight the importance of transparent data provenance and QA workflows.
- Data gaps due to maintenance and sensor issues emphasize the need for robust data governance and documentation of data quality.

## Funding
- Data collection supported by Natural Environment Research Council (NERC) award NE/R016429/1, part of the UK-SCaPE programme delivering National Capability.

## Notable Publications
- Doubek, J.P. et al. (2021). The extent and variability of storm-induced temperature changes in lakes measured with long-term and high-frequency data. Limnology & Oceanography, 66, 1979-1992. DOI: 10.1002/lno.11739