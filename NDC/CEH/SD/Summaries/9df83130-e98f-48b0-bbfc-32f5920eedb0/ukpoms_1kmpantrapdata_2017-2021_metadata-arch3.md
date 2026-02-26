# The UK Pollinator Monitoring Scheme

- A national monitoring framework describing how UK pollinator populations are tracked, with three main data products and a governance/QA approach to support policy scrutiny and future decisions.

## Overview

- PoMS aims to establish how insect pollinator populations are changing across the UK and to provide evidence for national pollinator strategies.
- Data products:
  - ukpoms_1kmPanTrapData_2017-2021_samples.csv (sample-level data)
  - ukpoms_1kmPanTrapData_2017-2021_flowers.csv (flower occurrences near pan traps)
  - ukpoms_1kmPanTrapData_2017-2021_insects.csv (bee/hoverfly occurrences)
- Years covered: 2017–2021 (2017 as a pilot; 2020 data impacted by Covid; 2021 extended to Northern Ireland).
- Geography: 95 randomly selected 1 km squares across England, Scotland, Wales; Northern Ireland added from 2021.
- Data access: Environmental Information Data Centre (EIDC) under Open Government Licence; proper citation and acknowledgements required.

## Data Collection and Protocol

- Sampling design:
  - Pan-trap survey across 95 1 km squares to monitor pollinators in agricultural and semi-natural habitats.
  - Stratified by country to reflect land-cover proportions; habitat type assigned per square using UK Land Cover Map 2007.
  - Within each square, five pan-trap stations along a diagonal with minimum 100 m spacing.
- Sampling cadence:
  - Up to four visits per square in summer (May–August), weather permitting; minimum two-week gap between visits.
- Pan traps:
  - Three bowls per station (yellow, blue, white on UV primer) filled with water and a small amount of dish soap.
  - Traps exposed for 6 hours (09:00–17:00 BST), with weather thresholds (temperature, cloud cover, wind) as acceptance criteria.
  - Insects sorted and identified in UKCEH labs; bees and hoverflies to species level where possible.
- Additional data:
  - Flower-Insect Timed Counts (FIT Count) and habitat assessments are part of the broader PoMS effort and referenced in separate publications.
- Data capture and QA:
  - Multi-stage QA: online forms (iRecord/Indicia), expert taxonomic verification, cross-checks for rare/out-of-range identifications, and post-2021 QA in R.
  - Metadata and data governance are emphasized throughout the workflow.

## Data Structure and Attributes

- Sample data file (2017–2021): metadata for each pan-trap sample (location, date, grid reference, habitat, recorder, trap details, environmental variables, etc.).
- Insect data file: occurrence-level bee and hoverfly records with specimen codes, taxonomy, sex, stage, counts, and lab determinations.
- Floral data file: flower occurrence data within 2 m of each trap; taxon details, taxon source, taxonomic corrections, floral unit counts, and yearly attributes.
- Data handling notes:
  - Data cleaned in R and SQL; missing values standardized (NA); dates/times reformatted; some fields replaced by defaults (e.g., counts for non-detections).
  - Taxonomy standardisation files used to ensure consistent species aggregation across years.
  - Floral unit counts may be adjusted (floral_unit_conversions) to standardise units across taxa; Poaceae counts adjusted to 0 where appropriate.
  - Outlier handling and year-to-year collation procedures described (see below).

## Quality Assurance and Data Corrections

- QA processes:
  - Photo checks and taxonomic cross-checks by multiple taxonomists; higher-tier checks for out-of-range or difficult identifications.
  - Random and targeted checks of specimens; documentation of reasons for QA actions and corrections.
  - Post-2021 data checks in R for enhanced validation.
- Corrections and transformations:
  - Taxonomic corrections saved in transformation files; annual standardised taxonomy used for analysis.
  - Floral unit corrections implemented to ensure consistent counting (e.g., unit conversion rules, Poaceae adjustments).
  - Occurrence IDs, specimen codes, and lab bycatch identifiers validated for uniqueness.
  - Checks across datasets to ensure consistent sample IDs, trap stations, and location references.
- Cross-year collation:
  - 2017–2020 floral data were edited for outliers in floral unit counts and harmonised before combining with 2021 data.
  - 2021 data integrated with earlier years, producing five-year combined datasets; 2017–2020 data retained with noted corrections.
  - Final exported datasets for 2017–2021 are provided; method notes describe how earlier-year data were aligned with later-year formats.

## Data Files Provided and Attributes

- Data file: ukpoms_1kmPanTrapData_2017-2021_samples.csv
  - Sample-level attributes: sample_id, country, location_code/name, grid square, projection, land_cover, date, year, recorder, trap details, weather, habitat, moved, and various environmental variables.
- Data file: ukpoms_1kmPanTrapData_2017-2021_flowers.csv
  - Occurrence-level attributes for flowers: sample_id, occurrence_id, taxon_group, taxon_source, english_name, taxon_version_key, order, family, floral_unit, total_floral_units, year.
- Data file: ukpoms_1kmPanTrapData_2017-2021_insects.csv
  - Occurrence-level attributes for bees/hoverflies: sample_id, occurrence_id, specimen_code, taxon_group, taxon_source, english_name, taxon_version_key, taxon_standardised, taxon_aggregated, count, sex, stage, comment, order, family, year.
- Data file summaries and attributes are detailed in the annex; data tables include QA flags, corrections, and export-ready columns.

## Collation Across Years

- Rationale for combining years:
  - Ensure consistent taxonomy and unit definitions across years.
  - Address outliers in 2017–2020 floral unit data before final five-year dataset.
- Outcome:
  - Flowers and insects data from 2017–2021 merged into five-year products with standardized taxonomy and corrected floral units.
  - Final exports ready for integration into broader environmental data systems.

## Export and Data Governance

- Export process:
  - Pan-trap sample data and taxa data formatted for EIDC ingestion; column names aligned with prior EIDC conventions.
  - Outputs include pan_trap_samples, species_flowers, and species_insects CSVs for 2017–2021.
- Governance and licensing:
  - Data are open under the Open Government Licence; users must cite PoMS and acknowledge UKCEH/JNCC and funders.
  - Usage requires attribution to PoMS and acknowledgment of volunteers and funders as specified.

## Annex: Taxonomic Aggregation Notes

- Aggregation scheme for taxa not distinguishable to species level (examples include Hymenoptera, Diptera groups).
- Documents how recorded taxon, standardised taxon, and aggregated taxon relate, with notes on male-only species-level identifications and family-level groupings.

## Key Considerations for Monitoring Framework Authors

- Data usefulness and coverage:
  - Provides standardized, multi-year, nationally scaled pollinator data suitable for trend analysis and policy evaluation.
- Data accessibility and governance:
  - Data stored in a central, auditable repository (EIDC) with explicit licensing and citation requirements.
- Metadata and provenance:
  - Detailed description of sampling design, habitats, protocols, QA procedures, and data transformations to enable reproducibility.
- Barriers and challenges:
  - Acknowledges data gaps (e.g., 2020 Covid-related gaps), access constraints, data silos, metadata gaps, and the need for ongoing data governance.
- Implications for policy:
  - The framework supports scrutiny of policy effectiveness, enables trend analyses, and informs future monitoring decisions through clearly documented methods and data lineage.