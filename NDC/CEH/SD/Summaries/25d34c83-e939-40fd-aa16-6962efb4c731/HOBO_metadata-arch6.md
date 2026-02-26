# Water temperature measurements from Durleigh Reservoir 2018 - HOBO TidbiT

## Overview
- Time-series dataset of water temperatures from Durleigh Reservoir in 2018.
- Five thermistors deployed at depths 0 m to 4 m (0, 1, 2, 3, 4 m) on a temperature chain.
- Measurements recorded at 10-minute intervals.
- Location coordinates: Lat 51.1215, Lon -3.0445.
- Instrumentation: HOBO TidbiT v2 loggers (Onset).
- Collected by Emily Slavin and Danielle Wain.
- Cited as: Slavin, E.I., Wain, D.J. 2018. Water temperature measurements from Durleigh Reservoir 2018.

## Data Content and Structure
- Time-series with a measurement per timestamp across five depths (0–4 m).
- Temperature values reported in Fahrenheit (oF).
- Date and time format specified as mm/dd/yyyy HH:MM:ss in the metadata; date range presented as 22/02/2018 to 05/10/2018, indicating a potential inconsistency to resolve (dd/mm vs mm/dd). Verification recommended before parsing.
- Sensor type: HOBO TidbiT v2 loggers.

## Metadata and Provenance
- Location: Durleigh Reservoir, UK.
- Depths: 0, 1, 2, 3, 4 meters forming a vertical profile.
- Deployed by: Emily Slavin and Danielle Wain.
- Dataset should be cited as: Slavin, E.I., Wain, D.J. 2018.

## Time Range, Resolution, and Depth Coverage
- Start/end date range: February 22, 2018 to October 5, 2018 (based on provided dates; format ambiguity exists).
- Temporal resolution: 10-minute intervals.
- Depth range: 0–4 meters with measurements from five thermistors.

## Data Quality, Formats, and Units
- Units: temperatures in Fahrenheit.
- Data format notes: ensure consistent date-time parsing given conflicting format notes.
- Quality considerations: as a single-site, multi-depth time series, consider validation against gaps or missing readings; confirm alignment of timestamps across all five sensors.

## Usage, Reuse, and Products
- Potential products: depth-resolved temperature profiles, time-series visualizations, and dashboards for self-service analysis.
- Suitable analyses: diurnal/seasonal temperature patterns, stratification opportunities, and comparisons with environmental data (e.g., weather).
- Citation and attribution: use the provided dataset citation when reproducing or referencing the data.

## Data Support Considerations for Integration
- When combining with other datasets, ensure consistent time zones and aligned timestamps across all sources.
- Consider unit conversion to Celsius for some analyses (oF to °C: (F-32)*5/9).
- Data cleaning steps may include handling gaps, verifying date formats, and reconciling the dd/mm vs mm/dd date range discrepancy.