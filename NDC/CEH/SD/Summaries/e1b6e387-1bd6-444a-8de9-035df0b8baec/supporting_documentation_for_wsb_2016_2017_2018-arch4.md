# Hourly data (air temperature, solar radiation, wind speed and lake temperature profile) from automatic water monitoring buoy from Windermere South Basin 2016 to 2018. Feuchtmayr, H., Jones, I.D., Clarke, M., Maberly S.C. (2021)

- What it is: A dataset from an automatic lake monitoring buoy in Windermere South Basin (Cumbria, England) providing environmental measurements including atmospheric and lake conditions.

- Variables measured:
  - Air temperature (°C)
  - Solar radiation flux (W/m^2) from a pyranometer
  - Wind speed (m/s)
  - Lake water temperature profiles at depths of 1, 2, 4, 7, 10, 13, 16, 19, 22, 25, 30 and 35 meters (°C) using platinum resistance thermometers

- Temporal resolution and reference:
  - Measurements collected every 4 minutes
  - Hourly averages calculated from the 4-minute data by an Oracle database
  - Time reference is GMT (UTC)

- Time period:
  - Data spanning 2016, 2017 and 2018

- Data quality and provenance:
  - Raw data are supplied; no calibration or formal quality control completed within this dataset
  - Visual checks performed; obvious hardware-related errors removed
  - Gaps attributed to buoy maintenance or sensor/logger problems

- Data structure and contents:
  - CSV format
  - Columns include:
    - Date GMT
    - Water temperature at each depth (1m, 2m, 4m, 7m, 10m, 13m, 16m, 19m, 22m, 25m, 30m, 35m)
    - Air Temperature
    - Pyranometer (solar radiation)
    - Wind Speed

- Funding and context:
  - Supported by Natural Environment Research Council award NE/R016429/1 as part of the UK-SCaPE programme delivering National Capability

- Example usage and impact:
  - Recent publication example: Doubek et al. (2021) on storm-induced temperature changes in lakes, leveraging long-term, high-frequency data

- Governance and data-leadership implications:
  - Highlights the importance of metadata clarity (units, depths, measurement methods)
  - Demonstrates need for data quality provenance and documentation of calibration status
  - Emphasizes discoverability through structured data (clearly labeled depth columns) and time-series formatting
  - Underlines potential data-sharing value for cross-network analyses and collaboration in broader aquatic systems research
  - Shows relevance for tracking data lineage, gaps, and update practices in ongoing monitoring programs