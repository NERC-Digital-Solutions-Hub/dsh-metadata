# Meteorological data from Glencorse ammonia enhancement site near UKCEH, Edinburgh (2021-2022)

## Overview
- Dataset from the Glencorse ammonia enhancement site near Edinburgh, UK, collected 28 May 2021 to 5 January 2023.
- Measurements collected from a 16 m mast (2 m above forest canopy) adjacent to the ammonia enhancement manifold, with the aim of supporting ammonia deposition experiments.
- Data cadence: instruments record every 20 seconds; values averaged to 15-minute intervals; all timestamps in GMT.
- Location and altitude: Glencorse woodland (55.8539 N, -3.2151 W; altitude 200 m).
- Complete details of experimental design, methodology, analysis, and findings are described in Deshpande et al. (2024).

## Data collected and sampling design
- Variables span meteorology, canopy- and soil-related measurements, and radiative metrics:
  - Air temperature, relative humidity, leaf wetness, wind speed (four heights), rainfall, wind direction, barometric pressure, photosynthetically active radiation (PAR), and total solar radiation (above and below canopy).
  - Soil: volumetric water content, electrical conductivity, and temperature at three depths.
- Data format: CSV file containing 56,154 measurements across 41 parameters.
- Columns include detailed metadata per record (Timestamp, Height, Manufacturer, Instrument, Description) along with parameter-specific values.
- Data scope supports elucidating wind-controlled NH3 enhancement effects on ammonia deposition studies.

## Quality control and data quality notes
- Data subjected to visual quality control; obvious instrument errors, datalogger issues, and power outages corrected or removed.
- Some gaps remain due to sensor replacement and maintenance.
- GMT used for all timestamps; calibration and sensor provenance documented via instrument metadata.

## Data structure and documentation
- The dataset is structured with 15-minute records and multi-sensor fields, enabling cross-comparison across heights, depths, and sensor types.
- The provided field-level metadata (Height, Instrument, Description, Unit) supports interpretability, though the sample description shows some inconsistent labeling in places.
- A comprehensive data dictionary and methodological context are available in the associated Deshpande et al. (2024) publication.

## Access, sharing, and reuse considerations for data stewards
- Provenance is anchored to a UKRI GCRF South Asian Nitrogen Hub-funded facility; dataset used for ammonia deposition work and published analyses.
- Recommended catalog metadata:
  - Collection site details: Glencorse woodland, coordinates, altitude.
  - Temporal coverage and sampling cadence: 28 May 2021 – 5 Jan 2023; 20 s raw cadence; 15-minute means.
  - Variables included (41 parameters) and their units; sensor types and calibration status.
  - Data quality notes: QC steps performed; known gaps; any corrections applied.
  - Data format and access: CSV, with timestamped records; licensing and access conditions.
  - Related publications and provenance: Deshpande et al. 2024; Atmos Environment; funding details.
- Recommend linking to the Deshpande et al. (2024) study for methodology and analytical context.

## Provenance and references
- Funding: UKRI GCRF South Asian Nitrogen Hub.
- Related publication: Deshpande AG, Jones MR, van Dijk N, Mullinger NJ, Harvey D, Nicoll R, et al. Estimation of ammonia deposition to forest ecosystems in Scotland and Sri Lanka using wind-controlled NH3 enhancement experiments. Atmos Environ. 2024; doi:10.1016/j.atmosenv.2023.120325.