# Supporting information for automatic water monitoring buoy data from Windermere South Basin 2008-2011

- Overview
  - Dataset from an automatic lake monitoring buoy in Windermere South Basin, Cumbria, England.
  - Covers 2008–2011; includes meteorological data and in-lake temperature profiles.
  - Used in studies of stratification and diel temperature variability; supports broader data-informed lake research.

- Data Availability and Citation
  - Data hosted by the NERC Environmental Information Data Centre.
  - DOI: https://doi.org/10.5285/bd37710e-6a53-49f0-9a07-6973408a3342
  - Citation example: Jones, I.; Feuchtmayr, H. (2017). south basin, 2008 to 2011.

- Sampling Regime and Collection Methods
  - Location: automatic buoy in Windermere South Basin, Cumbria, England.
  - Instruments: meteorological sensors and in-lake temperature sensors.
  - Variables and units:
    - Air Temperature: degrees C
    - Solar Radiation Flux (Pyranometer): Watts per metre squared
    - Wind Speed: metres per second
    - Water Temperature: degrees C at depths 1, 2, 4, 7, 10, 13, 16, 19, 22, 25, 30, 35 m
  - Data cadence:
    - Raw measurements every 4 minutes.
    - Hourly averages computed by Campbell Scientific datalogger.
    - Hourly average definition: average over the previous hour, excluding the data measured at the start of the hour and including the data measured at the end of the hour.
  - Time zone and period: All data in GMT; years 2008–2011.

- Quality Control
  - Data are raw and not yet calibrated or quality controlled.
  - Visual checks performed; obvious hardware errors removed.
  - Approximately 10 days in 2010 without data due to logger/telemetry change.
  - Other gaps attributed to buoy maintenance or sensor/logger problems.

- Data Structure
  - File format: comma separated values (CSV).
  - Columns:
    - Date GMT
    - 1m Water Temperature (°C)
    - 2m Water Temperature (°C)
    - 4m Water Temperature (°C)
    - 7m Water Temperature (°C)
    - 10m Water Temperature (°C)
    - 13m Water Temperature (°C)
    - 16m Water Temperature (°C)
    - 19m Water Temperature (°C)
    - 22m Water Temperature (°C)
    - 25m Water Temperature (°C)
    - 30m Water Temperature (°C)
    - 35m Water Temperature (°C)
    - Air Temperature (°C)
    - Pyranometer (Solar Radiation Flux, W/m²)
    - Wind Speed (m/s)

- Additional Information
  - The buoy data are used in multiple ongoing scientific studies, including:
    - Woolway et al. (2014) on estimating onset of thermal stratification from surface measurements.
    - Woolway et al. (2015) on diel variability in epilimnetic temperature across five lakes.
    - Woolway et al. (2016) on diel surface temperature range scaling with lake size (PLOS ONE).
  - Full author lists and citations available within the dataset record.

- Implications for Data Leaders
  - Discoverability and attribution enhanced by the EIDC DOI; clear citation path.
  - Data are raw with clear documentation of variables, units, and sampling regime; suitable for integration after QC/calibration.
  - Notable data gaps (10-day 2010 gap; maintenance-related gaps) to factor into analyses and metadata.
  - Rich multi-depth time series enabling analyses of stratification dynamics, diel cycles, and cross-validation with other lake datasets.
  - Emphasizes importance of metadata, provenance, and ongoing data stewardship for reuse across networks and partnerships.