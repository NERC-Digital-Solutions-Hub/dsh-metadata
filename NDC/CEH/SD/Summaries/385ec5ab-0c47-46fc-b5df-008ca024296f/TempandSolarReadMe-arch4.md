# TempandSolar.csv

## Overview
- Temperature and solar radiation data from four urine collection trials with Welsh Mountain ewes conducted in 2016.
- Part of the Uplands-N2O project (Grant NE/M015351/1).
- Authors: Karina A Marsden, Lucy Lush, Jon A Holmberg, Mick J Whelan, Andrew J King, Rory P Wilson, Alice F Charteris, Laura M Cardenas, Davey L Jones, Dave R Chadwick.
- If data are reused, ensure full citation.

## Data content and structure
- Variables:
  - TimeDate: date and time of measurement (dd/mm/yyyy hh:mm)
  - SolarRadiation: incoming solar radiation (W m-2)
  - AirTemp: air temperature (°C)
  - Site: semi-improved or improved
  - Season: spring, summer, autumn (semi-improved sites); autumn for the improved site
- Trials (2016):
  - Spring semi-improved site
  - Summer semi-improved site
  - Autumn semi-improved site
  - Autumn improved site
- Data collection frequency:
  - Half-hourly measurements (general)
  - Autumn improved site data recorded hourly

## Data collection context
- Weather data sourced from a meteorological station at each site (Skye Instrument, Llandrindod Wells, UK)
- Data collected specifically for the four trial conditions listed above

## Data quality and metadata considerations
- Frequency variation by site (hourly for autumn improved) may require harmonization for cross-site analyses.
- Metadata coverage includes units and measurement timing; ensure consistency in formats across the dataset.
- No explicit quality metrics provided; users may need to perform standard quality checks (range/consistency, timestamp alignment).

## Provenance and reuse
- Clear project and grant context; authorship attributed.
- Reuse requires full citation to the dataset and project details.

## Relevance for Data Leaders
- Illustrates the need to manage and harmonize time-series data across multiple sites and seasons.
- Highlights importance of detailed metadata (time stamps, units, frequency) for discoverability and reuse.
- Demonstrates considerations for data governance: provenance, access, and citation requirements.

## Actions and recommendations for data governance
- Document and standardize time intervals (half-hourly vs hourly) and ensure clear documentation of any site-specific differences.
- Maintain and publish comprehensive metadata (data source, station details, location, units, sampling frequency, data gaps).
- Implement traceable data lineage and citation requirements to support future reuse.
- Improve discoverability by indexing key attributes (Site type, Season, TimeDate, variables) and ensuring updates are tracked.