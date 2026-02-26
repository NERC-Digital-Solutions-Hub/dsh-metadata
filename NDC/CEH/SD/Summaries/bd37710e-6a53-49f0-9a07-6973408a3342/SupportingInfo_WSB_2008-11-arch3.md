# Supporting information for automatic water monitoring buoy data from Windermere South Basin 2008-2011

- Overview
  - Dataset from an automatic lake monitoring buoy in Windermere South Basin, Cumbria, England.
  - Measured variables: air temperature, solar (pyranometer) radiation, wind speed, and in-lake temperatures at depths of 1–35 m.
  - Data collection frequency: every 4 minutes; hourly averages computed by the datalogger.
  - Timeframe: 2008–2011; all times in GMT.

- Data availability and citation
  - Sourced from the NERC Environmental Information Data Centre.
  - Citation: Jones, I.; Feuchtmayr, H. (2017). south basin, 2008 to 2011. DOI: https://doi.org/10.5285/bd37710e-6a53-49f0-9a07-6973408a3342.

- Sampling regime and collection methods
  - Instrumentation: buoy-mounted meteorological sensors and in-lake temperature sensors (platinum resistance thermometers).
  - Measurements and units:
    - Air temperature: degrees C.
    - Solar radiation: Watts per square metre.
    - Wind speed: metres per second.
    - Water temperatures: degrees C at depths 1, 2, 4, 7, 10, 13, 16, 19, 22, 25, 30, and 35 m.
  - Data processing: hourly averages derived from 4-minute interval data; timestamps in GMT.
  - Data file format: CSV with columns for Date GMT and each depth temperature, plus air temperature, pyranometer, and wind speed.

- Quality control
  - Data are raw and not yet calibrated or quality controlled.
  - Visual checks performed; obvious hardware malfunctions removed.
  - Known data gaps: ~10 days in 2010 due to a logger/telemetry change.
  - Other gaps attributed to buoy maintenance or sensor/logger issues.

- Data structure
  - CSV columns include:
    - Date GMT
    - Temperature at 1 m, 2 m, 4 m, 7 m, 10 m, 13 m, 16 m, 19 m, 22 m, 25 m, 30 m, 35 m
    - Air Temperature
    - Pyranometer (solar radiation)
    - Wind Speed
  - Clear documentation of column descriptions and units.

- Additional information and usage
  - The buoy data are currently used in multiple scientific studies, including PhD research.
  - Notable publications leveraging this dataset:
    - 2014: Woolway et al. – A novel method for estimating the onset of thermal stratification in lakes from surface water measurements (Water Resources Research).
    - 2015: Woolway et al. – Diel variability in epilimnetic temperature for five lakes in the English Lake District (Inland Waters).
    - 2016: Woolway et al. – Diel surface temperature range scales with lake size (PLoS ONE).
  - Indicates potential for ongoing research and validation of lake thermal processes, as well as utility for monitoring framework analyses.