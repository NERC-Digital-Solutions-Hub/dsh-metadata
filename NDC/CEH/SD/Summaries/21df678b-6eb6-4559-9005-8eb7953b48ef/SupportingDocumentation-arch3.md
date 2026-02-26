Groundwater level information for 10 locations within the Gandak River Basin, in Bihar, India

## Overview
- Presents groundwater level information for 10 locations in the Gandak River Basin.
- Collected under the CHANSE (Coupled Human And Natural Systems Environment) project.
- Recording period: April 2017 to February 2019.
- Data captured with Troll automatic groundwater level loggers at 15-minute intervals.
- Readings corrected to local barometric pressure using a Troll barometer.

## Data collection and instrumentation
- Instrumentation used: Troll automatic groundwater level loggers; manual depth measurements with a dip meter.
- Depth measures:
  - mbgl: depth to water level recorded by logger (meters below ground level).
  - man_mbgl: manually measured depth to groundwater level (bgl) using dip meter.
- Additional variables:
  - DateTime: timestamp of recording.
  - Temp: water temperature.
  - PT: pressure transducer.
  - Baro: barometer (local atmospheric pressure).
- Data quality note: missing values are recorded as blanks.

## Variable descriptions
- DateTime: date and time of recording.
- Temp: water temperature.
- mbgl: logger depth to water level (meters below ground level).
- man_mbgl: manually measured depth to groundwater level.
- PT: pressure transducer reading.
- Baro: barometric pressure reading.
- Barriers to data quality: incomplete metadata, missing values, and formatting inconsistencies in site information.

## Site locations and dataset structure
- Ten sites with associated geolocation and installation details:
  - Chinta Manpur, Bagaha 1, Bagaha, Bagaha 3, Bettiah 1, Bettiah 2, Bettiah 3, Lalganj Basanta, Bettia4, Chalabhar.
- For each site (as documented), available fields include:
  - Longitude and latitude coordinates.
  - mbgl (depth to base) and water level depth on installation (mbgl).
  - Date installed and date last downloaded.
  - Months of record.
- Data anomalies: site entries contain formatting inconsistencies and typographical errors (e.g., typographic variations in site names, irregular date formats, and incomplete values in some fields).
- Example patterns:
  - Installation dates commonly around 2017-2018; last download dates around 2019.
  - Depths to base and water level depths vary by site; months of record listed with values like 10.5 or 22, indicating varying data spans.

## Data quality, metadata, and governance considerations
- Metadata gaps: inconsistent site naming, formatting, and some missing values in several fields.
- Verification needs: potential requirement to contact dataset originators to fill gaps or confirm values.
- Data standardization: current dataset shows non-uniform formatting; standardization would aid reuse and comparability.
- Barriers to data use: incomplete metadata and the need for data cleaning/transformations to make data readily usable.

## Relevance for monitoring frameworks
- The dataset provides high-resolution groundwater level information across 10 locations, suitable for trend analysis and policy evaluation related to groundwater management.
- The 15-minute sampling cadence enables detailed temporal analysis but requires robust metadata and data governance to ensure reliability and transparency.
- For monitoring frameworks, emphasis would be on:
  - Ensuring complete, consistent metadata for all sites.
  - Clear data sharing and data management practices.
  - Regular updates and documentation to maintain up-to-date datasets.