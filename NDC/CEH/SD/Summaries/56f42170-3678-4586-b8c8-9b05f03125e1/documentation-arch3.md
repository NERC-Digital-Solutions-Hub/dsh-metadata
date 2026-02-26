# Documentation

- This document describes the dataset "Hydro-epidemiological datasets for a selection of place studies," including its data files, creation methods, and data structure for monitoring environmental health in place-based studies.

## Overview of the dataset

- Combines leptospirosis case data with hydrometeorological predictors across multiple place studies.
- Spatial component uses polygons (geojson) representing each study area; hydrometeorological indicators are averaged within these polygons.
- Temporal component includes weekly or monthly leptospirosis case counts, with optional age-stratified data for many Chinese provinces.
- Hydrometeorological variables include precipitation, discharge, and soil moisture, derived from established global datasets.

## Places (spatial data)

- Place studies are represented as geojson polygons with vertices in degrees (longitude/latitude).
- Chinese provinces polygons were provided by an MSc student from an official data store; smaller areas (2 counties) and other countries were sourced from OpenStreetMap.
- Quality control notes that geospatial data are open source or from official instances.

## Collection and generation methods

- Polygons: Sourced from official data stores (China) and OpenStreetMap for other areas.
- Cases: Weekly or monthly leptospirosis case counts from health department statistics or peer-reviewed literature; in China, data are from official statistics (in Chinese). Some provinces (Ningxia, Qinghai, Shanghai, Tianjin) have no data because zero cases were reported during 2004–2017.
- Hydrometeorological data:
  - Precipitation: CHIRPS dataset (0.05° x 0.05° resolution).
  - Discharge: GloFAS-ERA5 reanalysis (0.1° x 0.1°).
  - Soil moisture: ESA CCI Soil Moisture (0.25° x 0.25°).
- Data processing steps convert raster hydrometeorological data to area-weighted daily averages per place study.

## Nature and units of recorded values

- Leptospirosis cases: counts per time period (weekly or monthly), first column labeled 'datum' (date), subsequent columns contain case counts (by age bracket if applicable).
- Hydrometeorological variables:
  - Precipitation: daily rainfall in millimeters (mm).
  - Discharge: daily average river discharge in cubic meters per second (m^3/s).
  - Soil moisture: daily relative volumetric soil moisture content (unitless fraction).

## Details of data structure and organization

- Each hydrometeorological variable has its own directory; files are named with the corresponding place study.
- Data files use a standard structure:
  - First column: 'datum' (date).
  - Second column: the value.
  - Missing data are indicated as NA.
- Case data include either a single total column or multiple columns by age bracket, with age brackets indicated by a low_high format (e.g., 0_4 for ages 0 to 4).

## Quality control and provenance

- Spatial data: open source or official sources; data widely used and peer-reviewed for hydrometeorology.
- Case data: sourced from health department statistics or peer-reviewed studies.
- Data sources for hydrometeorological variables are well-documented (CHIRPS, GloFAS-ERA5, ESA CCI Soil Moisture) with references to supporting methodological literature.

## Metadata considerations and data governance

- Metadata describe data files and their creation, aiding traceability for monitoring frameworks.
- Datasets emphasize transparency of provenance, with explicit notes on data origin (official statistics, peer-reviewed literature, or recognized global datasets).
- Public sharing of underlying data is noted as a potential barrier in general, but the documented dataset itself adheres to standard formats (GeoJSON and CSV) with clear data lineage.

## Limitations and challenges (relevant to monitoring framework authors)

- Data availability: some regions lack data or have zero-case reports; data completeness varies across place studies.
- Metadata quality: some provincial data (especially from non-English sources) may present language barriers.
- Data access and timeliness: certain data sources may not be readily accessible in a timely manner.
- Siloed datasets: fragmentation across organizations can hinder integration.
- Data transformation: hydrometeorological data require raster-to-area conversions and careful alignment to place polygons.
- Communication of complex findings: translating combined epidemiological and environmental signals into actionable insights.
- Data governance: ensuring datasets meet standards and are stored, shared, and kept up-to-date with appropriate governance.

## References and data sources

- Hydrometeorological references for CHIRPS, GloFAS-ERA5, and ESA CCI Soil Moisture, including foundational methodological papers on data merging and climate variables.
- Case data sources include health department statistics and peer-reviewed articles detailing leptospirosis reporting and diagnostic methods across included regions.