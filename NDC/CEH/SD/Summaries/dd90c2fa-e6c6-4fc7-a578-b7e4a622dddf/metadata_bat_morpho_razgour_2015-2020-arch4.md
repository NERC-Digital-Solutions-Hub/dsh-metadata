# Metadata for 'bat_morpho_razgour_2015-2020.csv'

## Overview
- Dataset of morphological and life history data collected 2015–2020 from three bat species: Barbastella barbastellus, Plecotus auritus, and Myotis escalerai.
- Geographic scope: England, Spain, and Portugal.
- Purpose: study adaptive responses to climate change as part of a NERC IRF project.

## Collection and generation methods
- Biological samples collected: tissue (wing biopsies), blood, and fecal samples.
- Capture methods: mist nets and harp traps at roosts, caves, foraging sites, and near small water bodies.
- Processing protocol: bats kept in individual cotton bags during processing; non-target species released immediately; target species released back at the capture site after processing.

## Nature and units of recorded values
- Location: Latitude and Longitude in WGS84 decimal degrees with a resolution of 10 km.
- Sex: F or M.
- Age: Adults, Sub-adults, or Juveniles (based on ossification of finger bones).
- Reproductive condition:
  - Females: Nulliparous, Pregnant, Lactating, Post-lactating, Nonreproductive.
  - Males: Based on position and size of the testes.
- Morphometrics:
  - Forearm: measured in millimetres.
  - BodyMass: measured in grams.
- Data representation: a single CSV file for all three species; empty cells represent missing values.

## Quality control
- All measurements performed by the same experienced person to ensure consistency.
- Data checked for outliers and anomalies.

## Details of data structure
- Structure: single CSV file containing records for all three species.
- Missing data: represented by empty cells.
- Metadata emphasizes measurement methods, units, and data quality checks to aid interpretation and reuse.

## Implications for data management and reuse (Data Leaders perspective)
- The dataset provides a coherent, consistently collected set of morphological and life-history traits across three species and three countries, suitable for cross-species climate-change analyses.
- Centralized collection method and single-collector quality control support data consistency, but may limit generalizability due to single-observer bias.
- Spatial data resolution (10 km) and precise coordinate handling are important for ecological analyses and integration with other spatial datasets.
- Clear categorization of age and reproductive status aids demographic analyses but requires careful interpretation when combining with other datasets lacking the same classifications.
- Missing values are explicit in the CSV, underscoring the need for metadata on missingness patterns and potential imputation strategies during analysis.
- Important next steps for data governance (not specified in the document but relevant for Data Leaders):
  - Document dataset licensing and access rights to facilitate wider reuse.
  - Provide a data dictionary or metadata file detailing column names, units, and acceptable values.
  - Include data provenance and versioning to track updates or corrections.
  - Consider additional metadata on collection dates, sampling effort, and exact transect/site locations to enhance discoverability and interoperability.