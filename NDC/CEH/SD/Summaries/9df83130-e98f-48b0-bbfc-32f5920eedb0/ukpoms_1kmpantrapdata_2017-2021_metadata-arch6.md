# The UK Pollinator Monitoring Scheme

- Overview
  - PoMS aims to monitor UK pollinator populations and provide data to national pollinator strategies.
  - Data described here come from the 1 km square pan-trap survey conducted 2017–2021, with 2017 as a pilot year and gaps in 2020 due to COVID-19; Northern Ireland data from NI are limited pilots in 2021.
  - Three main data files are provided for 2017–2021: samples (sample-level), flowers (flower occurrences near traps), and insects (bee and hoverfly occurrences). From 2021, data are also compiled into year-specific exports.
  - Data are available under the Open Government Licence and must be cited when used; acknowledgements to PoMS partners and volunteers are required.

- Data scope and access
  - Data are accessible via the Environmental Information Data Centre (EIDC), NERC Env Data Service, hosted by UKCEH.
  - Required citation: UK Pollinator Monitoring Scheme (2024). 1km square pan trap data from PoMS, 2017-2021. NERC EDS EIDC. Acknowledgement language provided in documentation.

- What PoMS collects and how
  - Pan-trap network
    - Up to 95 randomly allocated 1 km squares across England, Scotland, Wales, and Northern Ireland; stratified by agricultural vs semi-natural land cover.
    - In each square, five pan-trap stations along a diagonal; traps open for 6 hours per visit, with up to four visits per summer (May–August).
    - Weather thresholds apply (temperature, cloud cover, wind) for trapping; traps are configured with three coloured bowls per station.
  - Taxa and identification
    - Insects: bees and hoverflies identified to species level; other invertebrates identified to taxon-group level.
    - Plants: flowers recorded within a 2 m radius of each trap station (herbaceous flowering plants excluding grasses/rushes/sedges).
  - Data collection and QA
    - Data captured by volunteers and PoMS staff; entered into Indicia/iRecord systems; insects sorted in UKCEH labs; taxonomic identifications verified by specialists; cross-checks increased from 2019; post-2021 QA implemented in R.
    - QA includes checks for unique specimen codes, bycatch integrity, trap location uniqueness, date formats, and completeness of fields; photos and external checks used for plant identifications.
  - Collation and corrections
    - Floral unit counts sometimes require corrections; corrections are stored and applied consistently year-to-year; 2017–2020 floral data can be adjusted to align with 2021 standards.
    - Taxonomy standardisation: a formal transformation file is used to standardise species names and aggregates; new identifications added to the standard file; inconsistent or uncertain identifications flagged for review.
    - Outlier handling: floral unit outliers identified and corrected during collation, with 2017–2020 outliers adjusted before final 2021-merged dataset.

- Data files and structure
  - ukpoms_1kmPanTrapData_2017-2021_samples.csv
    - Sample-level data: sample_id, country, location_code, location_name, x1km_square, sample_projection, land_cover, date_from, date_to, year, digitised_by, trap_station, trap_active_from, trap_active_to, environmental variables, and derived QA fields.
  - ukpoms_1kmPanTrapData_2017-2021_flowers.csv
    - Occurrence-level data for flowers within 2 m of traps: sample_id, occurrence_id, taxon_group (flowering plant), taxon_source, english_name, source_taxon_version_key, order, family, floral_unit, total_floral_units, year.
  - ukpoms_1kmPanTrapData_2017-2021_insects.csv
    - Occurrence-level data for bees/hoverflies: sample_id, occurrence_id, specimen_code, taxon_group, taxon_source, english_name, source_taxon_version_key, taxon_standardised, taxon_aggregated, count, sex, stage, comment, order, family, year.
  - 2017–2020 data are also present in separate files for collation during assembly (e.g., ukpoms_1kmPanTrapData_2017-2020_*), used to build the 2017–2021 four-year dataset.
  - Data export products (post-processing to align with EIDC naming):
    - pan_trap_samples: cleaned sample-level dataset with renamed fields for EIDC compatibility
    - species_flowers: cleaned flower occurrences with standardised taxonomy fields
    - species_insects: cleaned insect occurrences with standardised taxonomy fields
  - Data collation across years
    - The 2021 dataset was combined with the 2017–2020 datasets, applying floral unit corrections and removing 2017–2020 outliers where necessary.
    - The final four-year dataset (2017–2021) includes revised flower data and harmonised taxonomy, with 2021 data appended.
  - Data attributes
    - Sample attributes include location, coordinates, habitat, date, trap details, and environmental context (temperature, wind, cloud cover, exposure, etc.).
    - Insect attributes include specimen code, taxon group, taxonomy (standardised and aggregated), count, sex, stage, and identification metadata.
    - Floral attributes include taxon_source, english_name, taxonomic corrections, floral_unit_count, and total_floral_units.

- Data quality, validation, and governance
  - Data entry and QA
    - 2017–2020 data entered via online forms; 2021 data entered via PoMS site; all data stored in UKCEH Indicia warehouse.
    - QA includes cross-checks by taxonomists, verification of photographs, and cross-checks of rare/out-of-range identifications starting in 2019.
    - Specimen-level QA includes ensuring unique specimen codes, correct taxonomic assignments, and appropriate counts; multiple taxonomist reviews where needed.
  - Data cleaning and standardisation
    - Taxonomy transformations saved in a separate file and updated annually; new identifications appended to standard taxonomy files.
    - Floral unit corrections are documented and applied when mapping 2017–2020 data to the 2021 standard.
  - Data integrity checks during export
    - Ensuring alignment of sample, taxa, and bycatch codes; verification that traps are correctly assigned to 1 km squares; checks for duplicate or missing sample IDs; verification of trap active windows and date formats.
  - Documentation and references
    - Links to PoMS methods with citations (Carvell et al. 2016, 2020) and the PoMS project documentation; detailed annexes describe aggregate groupings for taxa not identifiable to species level.

- Practical use for data support and data products
  - Ready-to-use data products
    - Three primary export files (samples, flowers, insects) enabling a self-serve workflow for researchers or analysts to explore pollinator abundance, floral resources, and their relationships across years and landscapes.
  - Cross-year analyses
    - The four-year dataset (2017–2021) supports trend analyses in pollinator taxa and flora availability across different land-use types; corrections ensure comparability across years.
  - Taxonomic and data quality considerations
    - Taxonomic standardisation allows consistent analysis of aggregated taxa; awareness of data gaps (e.g., NI 2021 pilot data) and pilot status for some years is important when interpreting trends.
  - Data accessibility and attribution
    - Datasets should be cited with the provided reference; users should acknowledge PoMS partners and volunteers; license is Open Government Licence.

- Annex: taxonomy aggregation
  - An annex provides guidelines for aggregating taxa not distinguishable to species level (e.g., Bombus lucorum complex, Dasysyrphus venustus complex) with multiple standardised and aggregated forms to enable consistent analysis across years and datasets.

- Key takeaways for data support workflows
  - Understand the data structure: sample-level vs occurrence-level (flowers, insects), with year-specific and cross-year consolidated datasets.
  - Leverage taxonomy standardisation to ensure consistent analysis across years and taxonomic groups.
  - Use the QA flags and QA-check outputs to identify records requiring manual review or correction.
  - Be mindful of data gaps and pilot status (e.g., 2017 pilot, 2020 pandemic gaps, NI data limitations in 2021) when designing analyses or dashboards.
  - Export-ready formats are provided to align with EIDC conventions, facilitating integration into broader data platforms and dashboards.