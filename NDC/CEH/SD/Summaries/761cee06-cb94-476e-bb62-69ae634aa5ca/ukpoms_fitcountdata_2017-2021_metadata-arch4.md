# The UK Pollinator Monitoring Scheme

## Overview
- PoMS is a partnership to monitor UK insect pollinator populations and provide evidence for national pollinator strategies.
- Two large-scale surveys: Flower-Insect Timed Count (FIT Count) and a 1 km square survey (co-located with pan-trap data in a separate dataset).
- Surveys run UK-wide with help from volunteers; aims to engage the public and support policy and conservation actions.

## Data scope and access
- Data are available from the Environmental Information Data Centre (EIDC), part of NERC’s Environmental Data Service, hosted by UKCEH.
- Open Government Licence; dataset must be cited in publications.
- Acknowledgement required for PoMS and its funders/partners (UKCEH, JNCC, Defra etc.) and volunteers.

## Datasets and methodology
- FIT Count dataset (2017–2021): records count locations, environmental variables, and counts by broad insect groups; 2017 was a pilot with gaps, 2020 affected by Covid, NI data limited in 2021.
- Public FIT Counts: citizen-science counts on a 50 cm x 50 cm quadrat for ten minutes, with 14 suggested target flowers (photographs encouraged for verification).
- 1 km square FIT Counts: same methodology, conducted in up to ~95 randomly allocated 1 km squares; 4 visits per summer (May–August); co-located with pan-trap data in a separate dataset; NI sampling expanded from 2021.
- Habitat and floral data: farmland/land-cover stratification and habitat categorisation aligned to national frameworks (LCM 2007) and standardized across years.
- Additional data products: pan-trap data and environmental data published separately; data are re-formatted for PoMS trend analyses and public release.

## Data processing and quality assurance
- Data extraction from Indicia/SQL via R for raw cleaning; online forms promote standardized data capture (iRecord 2017–2020; UK PoMS site in 2021).
- Photo verification by PoMS staff; optional photos from participants aid validation but are not used for real-time correction during counts.
- Data cleaning steps include: filtering out non-standard counts, aligning 2017 data to later years, handling missing metadata, and updating spatial references.
- Multiple correction processes:
  - Floral corrections: adjust target flower identifications based on photos.
  - Floral unit corrections: convert/adjust units when necessary (e.g., different floral units).
  - Other plant/family/structure corrections: maintain consistent taxonomic naming and structural classifications.
  - Habitat corrections: unify habitat categories across years; manual checks for non-standard entries.
- Data integrity checks cover sample ID duplication, 1 km square grid alignment, date consistency, time of day, totals consistency across insect groups, and habitat/plant validations.

## Data exports and structure
- Export datasets:
  - fit_count_public: public FIT Counts with standardized fields and renamed columns for publication.
  - fit_count_1km: 1 km square FIT Counts with harmonised fields.
- Across-year collation:
  - 2017–2021 data combined and harmonised; floral corrections and target flower name standardisation applied for consistency.
  - 4-year dataset supports trend analysis and historical comparability.
- Documentation of file attributes and column definitions provided to aid users (sample_id, country, location_code/name, date, year, habitat, target_flower, floral_unit_count, etc.).

## Collation across years and consistency improvements
- Efforts to align terminology and taxonomy across years (e.g., target_flower names, flower family/structure) to enable robust cross-year analyses.
- Floral unit corrections and outlier handling (including grasses) implemented to improve data quality.
- Habitat categorisation harmonised into main categories (Agricultural, Garden, Semi-natural, Urban) with ongoing manual checks for new descriptions.

## Data quality checks and validation
- Checks implemented for: sample ID duplication, correct 1 km square placement, single-date records, correct daytime counts, and completeness of insect-group totals.
- Validation steps include identifying counts not following FIT Count methodology and applying necessary filters or corrections.
- Export-ready datasets include both public and 1 km data with clean metadata and corrected fields.

## Limitations and considerations
- 2017 pilot data and 2020 gaps (Covid) affect longitudinal completeness; NI data limited in 2021.
- Some corrections are manual and may introduce revisions across years; metadata documents the changes for reproducibility.
- Public counts depend on volunteer participation and weather conditions; spatial coverage varies by year and location.

## Usage and attribution
- Data intended for trend analysis, policy support, and public engagement; suitable for researchers and policymakers.
- Users should cite the PoMS dataset and acknowledge the contributing organisations and volunteers.

## References
- Carvell et al. (2020, 2016) on pollinator monitoring frameworks and PMRP progress; foundational guidance for PoMS design and collaboration.

## Dataset descriptions (columns)
- Sample identifiers, country, location details, date, year, habitat, target flowers (and corrections), flower family/structure, insect counts by group, floral unit counts, weather context (cloud cover, sunshine, wind), and other metadata necessary for analysis and replication.