# Hourly water temperature of 16 experimental mesocosms and air temperature from April to November 2023

- Dataset includes hourly water temperature data from an experimental mesocosm facility and air temperatures from mid-April to early November 2023.
- Location: North West England; mesocosms filled with ~2800 L water from Windermere; mesocosms labeled 1–32 but only 5–12 and 21–28 used in this experiment.
- Scope: 16 active mesocosms (5–12 and 21–28) with hourly data for each from 21 April to 7 November 2023.
- Additional environmental data: Air temperature measured at a weather station within the mesocosm compound.

- Data collection and sensors
  - Water temperature: two platinum resistance thermometers (PRTs) per mesocosm, shaded by a plastic cover, positioned around mid-depth (~40 cm) and offset ~30 cm from the wall.
  - Logging: Campbell Scientific Data Logger.
  - Air temperature: Vaisala weather transmitter WXT520 at ~2.7 m height.
  - Time reference: All data in GMT.
  - Periodic issues: Air temperature sensor stopped working from 17 August to 6 September 2023; no air temperature data during that interval.

- Data processing and hourly aggregation
  - Hourly values are averages of 5-minute measurements within the hour (e.g., 1:00–1:55 p.m. averaged to 1 p.m.).
  - Handling of sensor discrepancies:
    - If the difference between the two water-temperature sensors is ≤ 0.2 °C, their average is used.
    - If the difference is > 0.2 °C, data are checked against the overall logger average; if still discrepant, one sensor is ignored and data from the remaining sensor are used.
  - Occasions where only one sensor contributed data are documented per mesocosm (e.g., mesocosm 11 and 12 have counts of single-sensor occasions).

- Data structure and format
  - File format: comma-separated values (CSV).
  - Columns: Date (dd/mm/yyyy), Hour (0–23), T5–T12 (water temperature for mesocosms 5–12), T21–T28 (water temperature for mesocosms 21–28), AirT (air temperature).
  - Units: degrees Celsius (°C).
  - Data notes: The dataset contains raw measurements that have not been calibrated or quality controlled; visual checks were performed to remove obvious hardware errors.

- Quality control and limitations
  - Data are raw and not yet calibrated or fully quality controlled.
  - Visual checks performed; some gaps due to sensor or logger problems.
  - Air temperature data gaps exist due to sensor failure (Aug 17–Sept 6, 2023).
  - Instances of sensor drift leading to exclusion of one sensor during certain periods.

- Provenance and references
  - Funding: European Union Horizon 2020 AQUACOSM-plus (grant No 871081) and NERC highlight topic NE/X00497X/1.
  - Facility reference: Feuchtmayr et al. (2019) on brownification and warming effects in mesocosm systems.
  - Citations:
    - Primary dataset reference as described.
    - Related publication: Feuchtmayr H, Pottinger TG, Moore A, et al. Science of the Total Environment, 2019 (doi provided in reference).