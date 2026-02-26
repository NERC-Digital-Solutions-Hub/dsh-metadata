# The UK Pollinator Monitoring Scheme

- The UK Pollinator Monitoring Scheme (PoMS) aims to establish how insect pollinator populations are changing across the UK, provide evidence to support national pollinator strategies, and engage volunteers and communities in action for pollinators.

## What PoMS is and who participates

- PoMS is a partnership of UKCEH, JNCC, and funders, coordinating large-scale surveys with volunteer input.
- It runs two large-scale surveys across the UK to monitor pollinators:
  - The Flower-Insect Timed Count (FIT Count) dataset (the focus of the public dataset described here).
  - The 1 km square survey (which also collects pan-trap and environmental data, published as a separate dataset).
- Surveys are designed to enable monitoring across landscape types and facilitate comparisons over time.

## Surveys and data collection

- FIT Count dataset (2017–2021):
  - Public FIT Counts: volunteers count insects visiting 14 target flowers (or any suitable flower) within a 50 cm x 50 cm quadrat for 10 minutes, during days with suitable weather (minimum 13°C if sky is clear; 15°C if cloudy).
  - 1 km square FIT Counts: similar methodology conducted in up to 95 randomly allocated 1 km squares; includes data from May–August with four visits per summer; some data co-located with the National Plant Monitoring Scheme.
  - Data include location (1 km resolution for FIT Count; precise location for 1 km square counts), environmental variables, and counts by insect groups.
- Sampling design and habitat stratification:
  - 1 km squares are selected to reflect land-use types and habitat cover, matched to UKCEH Land Cover Map 2007 (LCM) classifications: AG (agricultural) and SN (semi-natural) are primary categories; urban/coastal squares are excluded from sampling.
  - Co-location with other national monitoring schemes in England, Scotland, Wales, and Northern Ireland (from 2021 NI pilot).
- Data sources and access:
  - Data collected by volunteers and PoMS staff, entered via online forms (iRecord 2017–2020; PoMS website in 2021), stored in Indicia data warehouse; queries and extractions done via SQL and R.

## Data quality assurance and cleaning

- Quality assurance processes:
  - Photo verification of target flowers by PoMS staff; records can be corrected if misidentified.
  - Data retrieved from the warehouse and cleaned with R scripts; standardized data formats to support analysis.
- Data filtering and corrections:
  - Counts that do not follow FIT Count methodology are excluded (e.g., non-suitable targets, non-day counts, night-time counts, etc.).
  - Floral corrections: corrections to target flower identifications based on photos; corrections to target_other_name where applicable.
  - Floral unit corrections: conversions for incorrect floral units (e.g., counts scaled to correct units); grasses and non-flowering plants handled by standardising or NA-ing certain fields.
  - Habitat and plant data are harmonised across years; manual checks for items like habitat detailing and plant family/structure are performed, with updates stored for consistency.
  - Non-flowering plants: floral_unit_count set to NA in some cases to standardise data.
  - Unit count outliers: identified and corrected using year-specific conversions; some outliers are removed or adjusted based on sample_id.
  - Location and grid-square checks: corrections for grid references and square boundaries; some counts may be retained if they fall within the intended square limits but look like minor deviations.
  - Date and time checks: single-day counts are enforced; night-time counts are removed if time cannot be verified.
- Data integrity checks:
  - Sample ID duplication checks.
  - 1 km square checks to ensure counts are within the correct 1 km square network and the correct survey type.
  - Consistency checks across year collations (e.g., harmonising target flower names across years).

## Data processing, export, and collation

- Data processing steps:
  - Import raw data from Indicia, apply QA, and perform floral/habitat corrections.
  - Combine public FIT Count and 1 km FIT Count datasets; standardize fields and rename for export.
  - Collate data across years (2017–2021) to create four-year and full datasets for trend analysis.
- Datasets and file attributes:
  - Public FIT Count data: ukpoms_publicFITCountData_2017-2021.csv
  - 1 km FIT Count data: ukpoms_1kmFITCountData_2017-2021.csv
  - Exported datasets are formatted for PoMS trend analysis and for the Environmental Information Data Centre (EIDC).
  - Dataset descriptions include fields such as sample_id, country, location_code, location_name, x1km_square, sample_projection, habitat, target_flower, target_flower_family, flower_structure, floral_unit_count, floral_unit, count_start_time, weather variables, and insect counts by group.
- Collation across years:
  - Datasets are joined year-by-year to support trend analyses; floral names and units are standardised to ensure cross-year comparability.
  - Outliers and corrections are applied consistently across years to enable reliable long-term analyses.
- Data outputs and documentation:
  - The dataset includes detailed documentation (Dataset description, file attributes) to support reuse and proper interpretation by analysts.

## Licensing, access, and attribution

- Data access:
  - Data is accessible from the Environmental Information Data Centre (EIDC), part of NERC EDS, hosted by UKCEH.
- Licensing and citation:
  - Use of the dataset is under the Open Government Licence.
  - Proper citation required: UK Pollinator Monitoring Scheme (2024). Flower-insect timed count data from the UK Pollinator Monitoring Scheme, 2017-2021. NERC EDS Environmental Information Data Centre.
- Acknowledgments:
  - PoMS partnership funded by UKCEH and JNCC with Defra/Scottish/Welsh/National counterparts; continued thanks to volunteers and contributors.

## Practical relevance for environmental monitoring analysts

- Consistent, long-term view: The FIT Count and 1 km square surveys provide standardized, repeatable measures of pollinator activity across multiple UK regions and habitat types, enabling temporal trend analysis.
- Data quality and transparency: Robust QA processes, transparent data cleaning, and explicit handling of non-standard observations support credible environmental health assessments.
- Broad data utility: Datasets include rich contextual information (location, habitat, flower targets, insect groups, weather), enabling integrated analyses with landscape and climate data.
- Open access and collaboration: Data are openly licensed and stored in a central data centre, facilitating reuse, cross-study comparisons, and linking with other monitoring schemes.
- Challenges and opportunities: The documentation highlights ongoing efforts to increase data value by linking datasets, improve data accessibility, and harmonise across years and habitats.

## References

- Carvell, C., et al. (2020). Establishing a UK Pollinator Monitoring and Research Partnership (PMRP). Final report to Defra, Scottish Government, Welsh Government, and JNCC.
- Carvell, C., et al. (2020). Design and Testing of a National Pollinator and Pollination Monitoring Framework. Final Defra project report.