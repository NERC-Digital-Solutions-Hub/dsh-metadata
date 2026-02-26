# The UK Pollinator Monitoring Scheme

- The PoMS aims to establish how insect pollinator populations are changing across the UK and to support evidence for national pollinator strategies.
- Two large-scale surveys are used: Flower-Insect Timed Count (FIT Count) and the 1 km square pan-trap survey; this dataset covers the 1 km square survey data (2017–2021) with NI data added from 2021 onward.
- Data are produced by a UK-wide network of volunteers and staff, with standardised protocols designed for non-experts and volunteer involvement.
- From 2017–2021, data include pan-trap samples, insect and floral occurrences, plus associated environmental data; 2017 is a pilot year, 2020 had COVID-related gaps, and NI data from 2021 is from a limited pilot.

## Data access and citation

- Data are accessible via the Environmental Information Data Centre (EIDC), NERC Environmental Data Service, hosted by UKCEH.
- Licence: Open Government Licence; datasets must be cited in publications describing research using the data.
- Suggested citation: UK Pollinator Monitoring Scheme (2024). 1km square pan trap data from the UK Pollinator Monitoring Scheme, 2017-2021. NERC EDS Environmental Information Data Centre.
- Acknowledgement: PoMS partnership (UKCEH, JNCC, Defra and devolved administrations) and the volunteers who contributed data.

## Survey scope and timeline

- Geography: England, Scotland, Wales; Northern Ireland data added from 2021.
- Years: 2017–2021 (2017 as pilot year with limited data; 2020 data affected by COVID; 2021 NI data from a pilot).
- Co-location: PoMS squares co-located with National Plant Monitoring Scheme (England/Scotland/Wales) and other national monitoring efforts.

## Pan trap dataset description

- Contains samples and occurrences of insects and flowers collected for the PoMS 1 km square survey.
- Years covered: 2017–2021 (combined dataset; some floral data edits applied 2017–2020 so the dataset differs from earlier publications).
- Structure: three data files — sample data, insect data, floral data.
- Data quality: extensive QA and corrections implemented; 2021 introduced additional QA steps and R-based checks.

## Sample locations and sampling protocol

- Sampling framework: up to 95 randomly allocated 1 km squares across GB and NI; four visits per summer (May–August) per square, weather-dependent, with a minimum two-week gap between visits.
- Pan traps: three bowls per sampling station (one each in yellow, blue, white primer) filled with water and a drop of detergent, placed on stakes at vegetation height.
- Stations: five trap stations per square along a diagonal with a minimum 100 m separation; traps set 09:00–17:00 BST.
- Habitat stratification: squares categorized as agricultural or semi-natural based on UK Land Cover Map; sampling design aims to capture landscape-typical pollinator communities.
- Practical guidelines: traps in open, accessible areas; avoid heavy shading, livestock fields, and high-traffic areas; use tramlines in cropped fields when possible; obtain landowner permissions; avoid periods of planned operations (spraying/harvest).

## Data attributes

- Sample data files (pan_trap samples):
  - Location and environmental metadata; trap station numbers (1–5); total insect counts per trap; date; recorder; spatial references; and flags for data checks.
- Insect data (pan_trap insects):
  - Occurrence-level data for bees and hoverflies; includes sample_id, occurrence_id, specimen_code, taxon_group, taxon_source, English name, taxon version key, counts, sex, life stage, and taxonomy-related fields.
- Floral data (pan_trap flowers):
  - Occurrence-level data for forbs within 2 m of traps; includes sample_id, occurrence_id, taxon_group (flowering plant), taxon_source, English name, taxon version key, order, family, floral_unit counts, total_floral_units, and year.

## Quality assurance

- Data entry (2017–2020) via iRecord/Indicia; 2021 moved to PoMS site with the same data structure.
- Staged QA: photo verification of flowering plants; taxonomic identifications by specialists; cross-checks for difficult or out-of-range identifications; random and targeted checks from 2019 onward.
- Additional QA implemented in 2021 using R for data quality assessment.
- Specimen and taxonomy standardisation: workflow to standardise taxonomy and aggregates across years; procedures for handling uncertain identifications and outliers.

## Data processing and corrections

- Taxonomy and aggregates: a transformation file (TRANSFORM_insect_taxonomy_all_species_to_2021.csv) is used to standardise taxa; new identifications added and the combined taxonomy used for analysis.
- Insect data: checks that specimen codes are unique and of reasonable length; corrections to lab codes and re-downloading raw data as needed.
- Floral data: corrections to floral unit counts, translation of Welsh records, and emphasis on counting only flowering plants (Poaceae adjustments); unit conversions applied where necessary; 0 floral_unit_count values treated as NA in certain contexts.
- Outlier handling: outliers in floral unit counts identified and corrected for cross-year collation; 2017–2020 outliers corrected manually to align with 2021 data.

## Combined checks and export

- Cross-compatibility checks between pan_trap and insect data (e.g., ensuring all sample IDs and bycatch/specimen codes are accounted for).
- Creation of code lists for bycatch and specimens to verify unique combinations and detect missing codes.
- Totals and inspections: alignment between counts in pan_trap and insect totals; reconciliation across samples.
- Export: final data columns formatted to match EIDC dataset conventions; three CSVs prepared for export:
  - ukpoms_1kmPanTrapData_2017-2021_samples.csv
  - ukpoms_1kmPanTrapData_2017-2021_flowers.csv
  - ukpoms_1kmPanTrapData_2017-2021_insects.csv

## Data files provided

- Data file: ukpoms_1kmPanTrapData_2017-2021_samples.csv
  - Sample-level attributes including sample_id, location, date, trap details, and environmental context.
- Data file: ukpoms_1kmPanTrapData_2017-2021_flowers.csv
  - Occurrence-level floral data with taxon information, floral_unit_count, total_floral_units, and year.
- Data file: ukpoms_1kmPanTrapData_2017-2021_insects.csv
  - Occurrence-level insect data (bees and hoverflies) with specimen_code, taxon_group, sex, stage, count, and related taxonomy fields.

## Collation across years

- 2021 dataset combined with 2017–2020 data; floral unit outliers identified in 2017–2020 were edited when integrating with 2021 data.
- Flower data from 2017–2020 updated to reflect corrections; 2021 data integrated with the corrected 4-year dataset.

## Annex: Aggregate species groupings for taxa not distinguishable to species level

- Provides standardised and aggregated taxon groupings for Hymenoptera and Diptera (e.g., Bombus lucorum / terrestris / magnus / cryptarum treated as aggregated taxa; several groups where only males can be identified to species level).
- Notes emphasize limitations of identifications and the use of aggregated groups for robust analysis.

## References

- Core design and testing documents for pollinator monitoring framework; PMRP progress; PoMS reports and related Defra/Scottish/Welsh/NIEA documentation.