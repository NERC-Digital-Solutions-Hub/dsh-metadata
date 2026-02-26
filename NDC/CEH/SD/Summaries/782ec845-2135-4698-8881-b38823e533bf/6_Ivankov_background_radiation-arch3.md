# 6_Ivankov_background_radiation.csv

## Overview
- Metadata describing a background radiation dataset, including sampling site locations, measurement types, dose-rate measurements at two heights, and habitat information.
- Notes on data collection context: some sites were inaccessible but retained for completeness; instrument details and geospatial references are provided.

## Data fields and meanings
- latitude: location of sampling site; decimal degrees; using WGS-84; accuracy of 10 m or less.
- longitude: location of sampling site; decimal degrees; using WGS-84; accuracy of 10 m or less.
- Analysis_type_1_or_2: 1 = site for dose measurement and soil sampling; 2 = dose measurement only.
- at_0.1m: ambient equivalent dose rate at 0.1 m above ground; measured with certified gamma-beta irradiation dosimeters (RKS-01, Stora-TU, Ukraine).
- at_1m: ambient equivalent dose rate at 1 m above ground; measured with the same dosimeters as at_0.1m.
- Sampling_site_description: habitat type at the site (description field for site context).
- Notes: includes contextual statements (e.g., seven sites inaccessible; locations retained for completeness).

## Data quality and provenance
- Geolocation is provided with explicit reference to WGS-84 and instrument details.
- Measurements distinguish height-specific dose rates (0.1 m and 1 m) and specify the instrumentation used.
- Metadata contains some formatting inconsistencies and typos (e.g., field name fragmentation: “Sampling_site_descriptio n”) and some “n/a” entries in Units/Methodology, indicating areas that may require cleaning or standardization.
- Some site accessibility information is embedded in notes, signaling potential gaps in on-site sampling data.

## Site details and accessibility
- Habitat type described for context.
- Seven sites noted as inaccessible, though their coordinates remain in the dataset for completeness.

## Implications for monitoring frameworks
- Provides a structured basis to monitor ambient radiation dose rates across multiple sites with height-specific measurements.
- Enables linkage of dose data to site context (habitat) and precise geolocation, supporting spatial analyses and trend assessments.
- Highlights metadata quality considerations (inconsistencies and typos) that can affect data ingestion, interoperability, and governance.

## Recommendations for authors of monitoring frameworks
- Standardize field names and correct typos (e.g., Sampling_site_description).
- Ensure consistent Units/Methodology entries and complete metadata to facilitate automated ingestion.
- Improve metadata quality checks to catch formatting inconsistencies before publication.
- Document data accessibility constraints and sharing permissions; clearly separate site-level accessibility notes from measured data.
- Establish data governance practices to maintain currency and completeness, especially for sites that are inaccessible but retained for completeness.