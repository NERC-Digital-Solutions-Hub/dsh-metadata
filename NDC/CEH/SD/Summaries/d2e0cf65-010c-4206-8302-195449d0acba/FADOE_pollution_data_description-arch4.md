# FADOE_pollution.csv

## Overview
- A data file documenting air pollutant concentrations collected in a field experiment with eight 8 m-diameter Free-Air Diesel and Ozone Enrichment (FADOE) rings.
- Aims to compare pollutant responses under different treatments and capture environmental context (wind).

## Experimental Design and Data Collection
- Treatments: four groups across rings— diesel exhaust (D), ozone (O3), diesel exhaust plus ozone (D+O3), and control/natural air (CON).
- Measurements within the center of each ring:
  - Pollutants: nitrogen oxide (NO), nitrogen dioxide (NO2), nitrogen oxide plus NOx (NOx), and ozone (O3).
  - Concentrations reported in parts per billion (ppb).
  - Pollutant concentrations monitored every 60 seconds using automated switching systems linked to:
    - O3 analyser (Model 49i, Thermo Scientific, USA)
    - NOx analyser (Model 42C, Thermo Scientific, USA)
- Wind context:
  - Wind speed and direction recorded from four directions around the field (south, west, north, east) using dedicated anemometers (ws1/wd1, ws2/wd2, ws3/wd3, ws4/wd4).
  - Locations: around a field of wheat.
- Temporal cadence:
  - Data organized by Year (Column A), Date (Column B), and Time (Column C).

## Data Columns and Measurements
- Pollutants and related columns:
  - NOx: Column S
  - NO: Column Q
  - NO2: Column R
  - O3: Column P
- Treatments: Column E (D, O3, D+O3, CON)
- Wind: ws1/wd1 (south), ws2/wd2 (west), ws3/wd3 (north), ws4/wd4 (east)
- Temporal markers: Year (A), Date (B), Time (C)
- Units: ppb for pollutant concentrations

## Temporal and Spatial Context
- Location: field of wheat near coordinates around latitude 51.48, longitude -0.89 (UK).
- Years of data collection: 2018 and 2019.

## Instrumentation and Equipment
- O3 measurement: Thermo Scientific Model 49i analyser
- NOx measurement: Thermo Scientific Model 42C analyser
- Wind measurements: four-direction anemometer setup around the FADOE ring field

## Data Quality and Metadata Considerations
- Data are structured around central-ring measurements with high-frequency (1-minute) sampling.
- Potential metadata needs for robust governance:
  - Clarification of column mappings (letter-to-variable) and any data cleaning steps.
  - Documentation of calibration, data gaps, and update frequency.
  - Metadata for ring positions and any environmental conditions not listed.

## Relevance for Data Leaders
- Illustrates a controlled, multi-treatment field experiment capturing pollutant dynamics and environmental context.
- Highlights data governance needs:
  - Clear data asset management (format, quality, metadata, discoverability, updates).
  - Documentation of data collection methods, instruments, and data flow (from measurement to data file).
- Potential organizational use:
  - Assessing data availability, gaps, and granularity to inform prioritization and planning for broader data collaborative efforts.
  - Supporting co-ownership of data products by policy or analytics colleagues through transparent experimental design and accessible metadata.
- Applicability for cross-network collaboration:
  - Data could be shared with wider environmental or policy communities to benchmark treatment effects on NOx and O3 under controlled conditions.