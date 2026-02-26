# Hourly data (relative humidity) from automatic monitoring buoy from Blelham Tarn 2012 to 2019. Feuchtmayr, H., Clarke, M., Jones, I.D., Maberly, S.C. (2022)

## Summary
- A dataset of hourly relative humidity (RH) measurements collected from an automatic lake monitoring buoy at Blelham Tarn, Cumbria, England, spanning 2012–2019.
- Instrument: Onset HOBO U23 Pro V2 sensor; RH measured every 4 minutes with hourly averages calculated in an Oracle database.
- Time reference: All data are in GMT. Hourly value for a given hour is the mean of measurements within that hour, excluding the exact start and including the end of the hour.
- Deployment: Sensor remains on the buoy for ~2–3 months, then exchanged. A pre-deployment period in low RH conditions (~40%) lasts at least 2 months before redeployment.

## Sampling Regime and Collection Methods
- Location: Automatic monitoring buoy on Blelham Tarn, Cumbria, England.
- Variable: Relative humidity (%).
- Temporal resolution: Original measurements every 4 minutes; hourly averages provided.
- Data handling: Hourly averages are computed from the 4-minute readings by an Oracle database.
- Time zone: Greenwich Mean Time (GMT).
- Deployment protocol: After each deployment, a settling period is excluded (30–60 minutes) from processing; data before deployment and after deployment are removed from the dataset.

## Quality Control
- Data status: Raw data, not yet calibrated or quality controlled.
- Quality checks: Visual inspection for obvious hardware-related errors; removal of data suspected to be affected by hardware malfunction.
- Exclusion criteria: Data outside deployment windows removed; hourly values rejected if fewer than seven contributing measurements are available.
- Gaps: Remaining gaps due to buoy maintenance or sensor/logger problems.

## Data Structure
- Format: Comma separated values (CSV).
- Columns:
  - Date GMT: Date of measurement.
  - hour: Hour of measurement (GMT).
  - RH: Relative humidity (%).
  - N: Number of measurements contributing to the hourly mean.

## Funding
- Data collection supported by Natural Environment Research Council (NERC) award NE/R016429/1 as part of the UK-SCaPE programme delivering National Capability.

## Implications for Monitoring Frameworks
- Demonstrates use of in-situ buoy-based sensors for high-frequency environmental monitoring and derivation of hourly indicators.
- Highlights the importance of transparent processing (4-minute raw data, hourly aggregation) and clear documentation of time stamps and data handling rules.
- Emphasizes data quality considerations: raw data status, manual QC steps, and explicit criteria for including hourly values.
- Illustrates challenges relevant to monitoring frameworks: data gaps due to maintenance, need for metadata about deployment cycles, sensor settling periods, and data provenance.
- Shows how datasets are structured to support integration with broader environmental monitoring programs and governance, including funding provenance and data lineage.