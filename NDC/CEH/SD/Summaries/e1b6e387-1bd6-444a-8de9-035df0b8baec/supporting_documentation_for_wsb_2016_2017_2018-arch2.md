# Hourly data (air temperature, solar radiation, wind speed and lake temperature profile) from automatic water monitoring buoy from Windermere South Basin 2016 to 2018. Feuchtmayr, H., Jones, I.D., Clarke, M., Maberly S.C. (2021)

## Purpose and scope
- Dataset from an automatic lake monitoring buoy in Windermere South Basin, Cumbria, England.
- Covers 2016–2018; measurements reported in GMT.

## Measured variables and sensors
- Air temperature (°C)
- Solar radiation flux (Pyranometer, W/m^2)
- Wind speed (m/s)
- Lake water temperature at depths: 1, 2, 4, 7, 10, 13, 16, 19, 22, 25, 30, 35 m (platinum resistance thermometers; °C)

## Sampling regime and collection methods
- Data collected every 4 minutes by an automatic buoy with meteorological and in-lake temperature sensors.
- Data are aggregated into hourly averages in an Oracle database.
- Hourly value reference: for hour X, average over the interval (X−1:00 to X:00), including the measurement at X:00 and excluding the measurement at (X−1):00.

## Data quality and limitations
- Raw data not calibrated or quality controlled within this dataset.
- Visually checked; obvious hardware-induced errors removed.
- Gaps due to buoy maintenance or sensor/logger problems.

## Data structure and format
- CSV file with columns:
  - Date GMT (timestamp)
  - 1m Water temperature (°C)
  - 2m Water temperature (°C)
  - 4m Water temperature (°C)
  - 7m Water temperature (°C)
  - 10m Water temperature (°C)
  - 13m Water temperature (°C)
  - 16m Water temperature (°C)
  - 19m Water temperature (°C)
  - 22m Water temperature (°C)
  - 25m Water temperature (°C)
  - 30m Water temperature (°C)
  - 35m Water temperature (°C)
  - Air Temperature (°C)
  - Pyranometer (Solar radiation flux in W/m^2)
  - Wind Speed (m/s)

## Data provenance and funding
- Collected by an automatic buoy in the Windermere South Basin, Cumbria, England.
- Funding: Natural Environment Research Council award NE/R016429/1 as part of the UK-SCaPE programme delivering National Capability.

## Publications and usage
- Recent usage includes studying storm-induced temperature changes in lakes using long-term/high-frequency data (Doubek et al., 2021, Limnology & Oceanography).

## Relevance for environmental monitoring and analysis
- Provides high-frequency, depth-resolved thermal and meteorological context for lake ecosystems.
- Supports data quality assessment, standardised analysis, and potential integration with other datasets.
- Suitable for inclusion in data portals and for reproducible environmental health and policy monitoring analyses.