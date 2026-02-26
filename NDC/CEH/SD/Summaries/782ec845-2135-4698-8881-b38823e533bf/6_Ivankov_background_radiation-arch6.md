# Metadata for 6_Ivankov_background_radiation.csv

- The dataset provides geolocated ambient background radiation measurements and site metadata.
- Key geospatial details are stored as decimal degrees in WGS-84 with an accuracy of about 10 meters or less.
- Each site is labeled by a sampling location and includes an accompanying habitat-type description.

## Data fields and meaning

- latitude
  - Location of the sampling site in decimal degrees.
  - Notes indicate GPS data captured with a Garmin GPSmap 78S using WGS-84.
- longitude
  - Location of the sampling site in decimal degrees.
  - Notes indicate GPS data captured with a Garmin GPSmap 78S using WGS-84.
- Analysis_type_1_or_2
  - Indicates site type: 1 = dose measurement and soil sampling; 2 = only dose measured.
  - Units: n/a; Notes: 1 or 2.
- at_0.1m
  - Ambient equivalent dose rate measured at 0.1 m above ground.
  - Instrument: certified gamma-beta irradiation dosimeters (RKS-01, Stora-TU, Ukraine).
- at_1m
  - Ambient equivalent dose rate measured at 1 m above ground.
  - Instrument: certified gamma-beta irradiation dosimeters (RKS-01, Stora-TU, Ukraine).
- Sampling_site_description
  - Habitat type at the sampling location.
  - Notes: habitat description included; data may reflect seven inaccessible sites still listed for completeness.
- Notes (general field-level)
  - n/a in several fields; specific notes accompany each field where provided.

## Data quality and caveats

- Coordinates are in decimal degrees using the WGS-84 system; expect ~10 m or better positional accuracy.
- Some sites were inaccessible (as noted) but are retained in the dataset for completeness, which may affect interpretation of surrounding conditions.
- Field-level notes indicate limited metadata in some columns (e.g., “n/a” in Notes), which may require inference from related fields.

## Potential data products and insights

- Visualizations
  - Interactive map of sampling sites showing latitude/longitude with hover details (habitat type, analysis type).
  - Time-agnostic bore-sight: compare 0.1 m vs 1 m dose rates across sites.
- Comparative analyses
  - Group by Analysis_type_1_or_2 to distinguish sites with soil sampling versus dose-only measurements.
  - Compare dose rates by habitat type, leveraging Sampling_site_description.
- Dashboards and reports
  - Self-serve dashboards with filters for site accessibility, analysis type, and dose-rate ranges.
  - Pivot tables summarizing mean dose rates by habitat and measurement height (0.1 m vs 1 m).

## Data gaps and improvement suggestions

- Consider adding a measurement date/time to enable temporal analyses.
- Introduce a explicit site identifier field to robustly join with other datasets.
- Expand metadata with units for all numeric fields and a formal data dictionary.
- Include data provenance and QA steps (e.g., calibration details for RKS-01 dosimeters).
- Provide a clear data quality flag or completeness indicator for each site (e.g., accessible vs. inaccessible).

## Considerations for data sharing and reuse

- Be mindful of the note about inaccessible sites when analyzing spatial coverage or extrapolating results.
- When combining with other datasets, ensure consistent coordinate reference (WGS-84) and unit conventions.
- Provide access to the full metadata alongside the data to aid reproducibility and interpretation.