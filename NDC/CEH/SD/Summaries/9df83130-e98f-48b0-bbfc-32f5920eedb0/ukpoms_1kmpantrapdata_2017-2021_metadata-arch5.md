# The UK Pollinator Monitoring Scheme

- Overview: A national effort to monitor pollinator populations across the UK via the 1 km square pan-trap survey, along with Flower-Insect Timed Counts (FIT Counts). Data cover 2017–2021 and are designed for large-scale data governance, interoperability, and reuse by researchers and organisations.

- Data access and licensing:
  - Data hosted by the Environmental Information Data Centre (EIDC), UK Centre for Ecology & Hydrology (UKCEH).
  - Open Government Licence; users must cite the dataset in publications.
  - Acknowledgement required, with details on PoMS funding and contributor partners.

- Purpose and governance for data stewards:
  - Aims to provide interoperable, up-to-date datasets that are easily discoverable and reusable.
  - Ensures data standards (taxonomy, metadata, formats), data provenance, and appropriate sharing restrictions.
  - Documents work and maintains traceability across years, including corrections and transformations.

- Survey design and scope:
  - 95 randomly allocated 1 km squares across England, Scotland, Wales, and Northern Ireland (with NI added from 2021).
  - Stratified by land cover (agricultural vs semi-natural) using UKCEH Land Cover Map 2007.
  - In each square: a diagonal transect with five pan trap stations; traps out for 6 hours on sampling days.
  - Four visits per summer (May–August); weather thresholds apply.
  - Additional context: co-located with other national schemes; FIT counts provide complementary data.

- Data collection and structure:
  - Insects and flowers collected at pan trap stations; specimens sorted at UKCEH laboratories; bees/hoverflies identified to species where possible.
  - Data are stored as three main data files:
    - Samples file: pan_trap samples metadata (sample_id, location, dates, weather, habitat, etc.).
    - Insects file: occurrence-level data for bees and hoverflies (occurrence_id, specimen_code, taxon_group, taxonomy fields, count, sex, stage, etc.).
    - Flowers file: occurrence-level data for floral units near traps (sample_id, occurrence_id, taxon_source, english_name, floral_unit_count, total_floral_units, etc.).

- Quality assurance and data cleaning:
  - Multi-stage QA: online forms (iRecord/Indicia) → UKCEH lab identifications → taxonomic cross-checks (second opinions for outliers, etc.).
  - Checks include photo QA, cross-checks for rare/out-of-range identifications, and random sampling checks.
  - Data cleaning includes handling NAs, date/time formats, and standardizing spatial references.
  - Data are imported and cleaned in R, with additional checks in SQL and Python deployments as part of the workflow.

- Taxonomy, standardisation, and aggregation:
  - Taxonomic standardisation through TRANSFORM_insect_taxonomy_all_species.csv; aggregates used for analysis to ensure consistent counts.
  - Sex, stage, and taxon_group normalised (e.g., "not recorded" where unknown; adult stage assumed for insects).
  - Annex provides aggregate groupings for taxa not distinguishable to species level (e.g., Bombus spp. as multiple aggregations, hoverflies, etc.).

- Data corrections and documentation:
  - Floral units: corrections and unit conversions captured in a pan_trap_floral_unit_conversions.csv; 2017–2020 corrections applied to 4-year dataset.
  - Outliers: floral unit outliers identified and corrected (where justified) before final 2021 collation.
  - All transformations and corrections are saved to ensure reproducibility; updated files are re-downloaded and re-joined.

- Collation across years (2017–2021):
  - 2017–2021 pan-trap data combined into a single four-year dataset; adjustments made where floral data were edited in 2017–2020.
  - 2021 data integrated with 2017–2020 data; sums for invertebrate counts recalculated and trap-active formats standardized (date, time, and location fields).
  - Decisions on outliers and corrections applied consistently to ensure cross-year comparability.

- Data exports and file formats:
  - Data files provided:
    - ukpoms_1kmPanTrapData_2017-2021_samples.csv
    - ukpoms_1kmPanTrapData_2017-2021_flowers.csv
    - ukpoms_1kmPanTrapData_2017-2021_insects.csv
  - Gold standard export naming and field mappings align with EIDC schema; columns renamed to match existing EIDC dataset conventions.
  - The 2021 dataset is built from 2017–2020 data plus 2021 data, with rigorous collation and quality checks.

- Data documentation and attributes:
  - Detailed attribute descriptions for each data file (samples, flowers, insects) provided in the dataset.
  - Metadata includes sample_id, occurrence_id, taxon_group, taxon_source, english_name, taxonomy keys, counts, sex, stage, date, location, habitat, and sampling conditions.

- Governance, provenance, and usage notes:
  - Emphasises provenance tracking, versioned transformations, and QA audit trails.
  - Data stewards should maintain linkage between raw lab identifications and standardized taxonomy, with explicit documentation of corrections and rationale.
  - Encourages transparent usage, including how floral unit corrections, outliers, and cross-year aggregations were handled.

- Annex and supplementary material:
  - Annex: detailed aggregate taxon groupings for taxa not distinguishable to species level (e.g., Bombus, Nomada, Dasysyrphus, Sphaerophoria), including standardised and aggregated taxon labels.
  - Provides a framework for reproducible taxonomic grouping across years.