# Silene uniflora population GPS dataset

## Overview
- Field observations collected between February 2018 and September 2021.
- Aimed to identify sites potentially colonised by Silene uniflora using Botanical Society of the British Isles records, existing literature, and communications with county recorders.
- Approximate geographic extents recorded with GPS based on observed plants; sites visited to delineate population boundaries.

## Data collected and units
- Each population record consists of a series of GPS positions (latitude and longitude in decimal degrees, Datum: WGS84) defining the population’s approximate extent.
- Habitat/substrate type recorded per population (examples: montane, coastal, mine, serpentine).

## Data quality and accuracy
- GPS positions were checked against satellite imagery to ensure correct location.
- Quality control performed to verify accurate placement of population boundaries.

## Data structure and provenance
- Dataset contains 56 rows, each representing a single population.
- Populations named using local area names/landmarks (Column 1) and assigned population codes (Column 2) used for a connected dataset (Heavy metal tolerance records for Silene uniflora).
- Column 3 records habitat type; remaining pairs of columns contain latitude/longitude positions for points bounding the site.
- Connected context: linked to, and can be integrated with, the Heavy metal tolerance dataset for Silene uniflora.

## Metadata and accessibility considerations for Data Stewards
- Sources include BSI records, existing literature, and county recorders; provenance should be captured in metadata.
- Standardize data types and coordinate system (WGS84, decimal degrees) and document the bounding-point structure.
- Consider publishing this dataset alongside the related heavy metal tolerance dataset to facilitate cross-dataset discovery and reuse.
- Include a data dictionary and note the data collection period, methods, and quality checks to aid discoverability and reuse.

## Practical considerations and potential limitations
- Temporal coverage is limited to 2018–2021; may not reflect current population extents.
- Coverage depends on sites identified from secondary sources, which could lead to incomplete geographic coverage.
- Data interoperability is improved by using a consistent coordinate system and clearly defined population-bounding points.

## Recommendations for Data Stewards
- Create and publish a complete metadata record including: title, creators, collection date range, geographic coverage, methods, data quality notes, licensing, and data access constraints.
- Provide a clear data dictionary for all columns, including how population names and codes map to the heavy metal tolerance dataset.
- Ensure versioning and update pathways are defined for future data additions or re-surveys.
- Facilitate linking this dataset with the connected heavy metal tolerance dataset to support combined analyses.