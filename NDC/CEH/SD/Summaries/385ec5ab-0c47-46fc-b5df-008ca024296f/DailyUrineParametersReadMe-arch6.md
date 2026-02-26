# DailyUrineParameters.csv ReadMe

## Overview
- ReadMe for the DailyUrineParameters.csv dataset from the Uplands-N2O project (Grant NE/M015351/1).
- Documents data processing steps, filtering, and the derived daily metrics for sheep urine data.
- Notes that data reuse should be fully cited.

## Data preparation and filtering
- Observations with zero urination events were excluded.
- Two replicate sheep (sheep 1 and sheep 5) were removed due to relative infrequency of urine events.
- Daily N excretion, volume, and frequency calculations assume the sheep’s time spent in the urine collection apparatus represents a 24-hour period (typically 10:00–16:00 collection window).

## Data schema and column definitions
- Site: Semi-improved or improved pasture.
- Season: Spring, Summer, or Autumn for the semi-improved site; Autumn for the improved site.
- Sheep_ID: Identifier for the replicate sheep.
- Date: Date of urine collection (dd/mm/yyyy).
- DailyNExcretion: Calculated daily nitrogen excretion (based on the collection period).
- DailyVol: Estimated daily urine volume (liters per sheep per day) based on time spent in collection apparatus.
- DailyFrequency: Estimated daily urine event frequency (events per sheep per day) based on time spent in collection apparatus.

## Calculation and assumptions
- Daily metrics (N excretion, volume, frequency) are derived from the observed collection window (10:00–16:00) and scaled to a 24-hour period.
- Assumes representative sampling within the specified collection times for each day.

## Reuse, citation, and provenance
- When reusing the data, ensure full citation to the original project and authors.
- The ReadMe provides essential context for data interpretation, filtering decisions, and derived metrics to enable reproducibility and proper use.

## Practical implications for Data Support
- The ReadMe clarifies data quality decisions (exclusion of zero events and certain replicates) and the exact scope of derived metrics, supporting reliable self-serve analysis.
- Facilitates data integration with other datasets by documenting site, season, and collection window metadata.
- Highlights the need to communicate the 10:00–16:00 collection window and 24-hour extrapolation when presenting daily metrics to end users.