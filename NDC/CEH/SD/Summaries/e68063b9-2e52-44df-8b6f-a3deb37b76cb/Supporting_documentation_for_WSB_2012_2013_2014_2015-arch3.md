# Data from automatic water monitoring buoy from Windermere South Basin 2012, 2013, 2014 and 2015. Jones, I.D., Feuchtmayr, H., Maberly S.C. (2017)

- Overview
  - Automatic lake monitoring buoy located in Windermere South Basin, Cumbria, England.
  - Measures meteorological variables and in-lake temperature profiles: air temperature, solar radiation (pyranometer), wind speed, and water temperature at multiple depths (1, 2, 4, 7, 10, 13, 16, 19, 22, 25, 30, 35 m).
  - Data collection frequency: every 4 minutes; hourly averages calculated from the previous hour.
  - Time reference: all data in GMT.
  - Data period: 2012–2015; used in multiple current scientific studies and cited in publications.

- Sampling regime and collection methods
  - Instruments: meteorological sensors and platinum resistance thermometers for water temperature at specified depths.
  - Depths covered: 1, 2, 4, 7, 10, 13, 16, 19, 22, 25, 30, 35 m.
  - Data storage: Campbell Scientific datalogger (until 1 June 2012) and Oracle database (from 1 June 2012 onwards).
  - Data format: CSV with columns for Date_GMT, water temperatures at each depth (1m, 2m, 4m, 7m, 10m, 13m, 16m, 19m, 22m, 25m, 30m, 35m), Air_Temperature, Pyranometer (solar radiation), and Wind Speed.
  - Units: water temperatures in °C; air temperature in °C; solar radiation in W/m^2; wind speed in m/s.
  - Data quality context: raw data not yet calibrated or quality controlled; visually checked with obvious hardware errors removed; gaps attributed to buoy maintenance or sensor/logger problems.
  - Data accessibility caveats: not fully calibrated; some data gaps exist; metadata quality and completeness impact rapid verification.

- Quality control and governance
  - Quality assurance status: raw data presented; some basic cleaning for hardware-induced errors performed.
  - Gaps and issues: routine gaps due to maintenance or sensor/logger problems; inadequate metadata described but not fully detailed here.
  - Data provenance: data originate from a single buoy with clear instrument roles and depth-specific measurements; data lineage includes the transition from a datalogger to an Oracle database.

- Data structure and metadata details
  - File format: comma-separated values (CSV).
  - Key columns: Date_GMT; Water_temperature at depths (1m, 2m, 4m, 7m, 10m, 13m, 16m, 19m, 22m, 25m, 30m, 35m); Air_Temperature; Pyranometer; Wind Speed.
  - Temporal framing: measurements timestamped in GMT; hourly averages reflect the previous hour’s data.
  - Depth coverage provides a vertical profile of lake temperature alongside surface meteorology.

- Scope, usage, and scholarly context
  - The dataset has supported multiple current scientific studies, including PhD research.
  - Published work citing this dataset: Woolway, Maberly, Jones, Feuchtmayr (2014) on a method for estimating the onset of thermal stratification in lakes from surface measurements.
  - Practical relevance: enables examination of lake thermal dynamics, surface–depth interactions, and environmental health monitoring implications.

- Implications for monitoring frameworks
  - Illustrates the importance of high-frequency, multi-parameter environmental monitoring for policy scrutiny and decision-making.
  - Highlights common monitoring framework challenges: data accessibility, timeliness, data silos, the need for robust metadata, data transformation requirements, and governance for data sharing and quality assurance.
  - Demonstrates the value of documenting data provenance, storage transitions, and explicit notes on quality control to inform future data governance and open data practices.