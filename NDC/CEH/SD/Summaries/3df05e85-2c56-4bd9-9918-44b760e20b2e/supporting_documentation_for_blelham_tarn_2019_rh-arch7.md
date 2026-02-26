# Hourly data (relative humidity) from automatic monitoring buoy from Blelham Tarn 2012 to 2019

## Overview
- Dataset from an automatic lake monitoring buoy at Blelham Tarn, Cumbria, England.
- Relative humidity (%) measured with an Onset HOBO U23 Pro V2 sensor.
- Sensor collects data every 4 minutes; hourly averages are calculated by an Oracle database.
- Time basis is GMT; coverage from January 2012 to December 2019.

## Sampling regime and collection methods
- Buoy hosts meteorological instruments including the HOBO sensor.
- 4-minute data cadence; hourly values represent the average over the previous hour (with specifics: the value for 2 p.m. is the average of data between 1 and 2 p.m., excluding 1 p.m. data, including 2 p.m. data).
- Sensors are deployed for ~2–3 months before replacement with another HOBO unit.
- After deployment, sensors are left in low RH conditions (≈40%) for at least 2 months prior to re-deployment.

## Quality control
- Data are raw and not yet calibrated or fully quality controlled.
- Visual checks performed; obvious hardware errors removed.
- Data before and after deployment excluded, as well as 30–60 minutes post-deployment (settling period).
- Hourly data removed if fewer than seven measurements were available to compute the mean.
- Other data gaps arise from buoy maintenance or sensor/logger problems.

## Data structure
- Format: comma separated values (CSV).
- Columns (described in the dataset):
  - Date GMT: Date of measurement.
  - hour: Hour of measurement (GMT).
  - RH: Relative humidity (%).
  - N: Number of measurements used to calculate the hourly mean.

## Temporal and spatial coverage
- Temporal: January 2012 to December 2019.
- Spatial: Point measurement from the buoy at Blelham Tarn, Cumbria, England.

## Usage notes for GIS specialists
- Dataset is raw; may require calibration or additional QA for rigorous GIS analyses.
- Times are in GMT; convert to local time if integrating with other datasets.
- Account for data gaps and the N field to assess reliability of each hourly value.
- With only a single buoy location, map-based analyses would rely on the temporal series or integration with other spatial datasets for broader coverage.

## Funding
- Data collection supported by Natural Environment Research Council (award NE/R016429/1) as part of the UK-SCaPE programme delivering National Capability.