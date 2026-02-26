# Supporting Document
Hourly data (relative humidity) from automatic monitoring buoy from Blelham Tarn 2012 to 2019. Feuchtmayr, H., Clarke, M., Jones, I.D., Maberly, S.C. (2022)

- Overview
  - Dataset of hourly relative humidity (RH) measured by an automatic lake monitoring buoy at Blelham Tarn, Cumbria, England.
  - Time period: January 2012 to December 2019.
  - Sensor: Onset HOBO U23 Pro V2; data recorded every 4 minutes; hourly averages computed during post-processing.

- Sampling regime and collection methods
  - Location: Blelham Tarn, Cumbria.
  - Instruments: Meteorological sensors on a buoy; RH measured in percent.
  - Data aggregation: Hourly average RH calculated from 4-minute interval measurements.
  - Time standard: All values in GMT (UTC).

- Data processing rules (hourly averaging)
  - The hourly value for a given time (e.g., 2 p.m.) is the average of data from 1–2 p.m., excluding 1 p.m. but including 2 p.m.
  - Data are stored as GMT timestamps corresponding to the hour being reported.

- Sensor deployment and maintenance
  - Sensor deployment cycle: Each sensor remains on the buoy for ~2–3 months before exchange.
  - Pre-deployment conditioning: After redeployment, sensors are left in low RH conditions (~40%) for at least 2 months prior to re-deployment.

- Quality control and data screening
  - Data are raw and not yet calibrated or fully quality controlled.
  - Visual checks performed; obvious hardware malfunctions removed.
  - Data immediately before/after deployment removed; first 30–60 minutes after deployment discarded to allow sensor stabilization.
  - Hourly records removed if fewer than seven measurements available to compute the mean.
  - Other gaps arise from buoy maintenance or sensor/logger problems.

- Data structure
  - Format: Comma-separated values (CSV).
  - Columns:
    - Date GMT: Date of measurement.
    - hour: Hour of measurement (GMT).
    - RH: Relative humidity (%).
    - N: Number of measurements used to calculate the hourly mean.

- Data provenance and funding
  - Funding: Natural Environment Research Council award NE/R016429/1 (UK-SCaPE programme, National Capability).

- Implications for analysis
  - Raw RH data are uncalibrated; consider calibration or cross-validation if precise RH values are required.
  - Be mindful of data gaps due to maintenance, sensor issues, and deployment transitions.
  - The 7-measurement threshold may bias hourly completeness; consider sensitivity analyses for missing data.
  - Metadata and traceability are maintained via documented deployment cycles and timestamps.