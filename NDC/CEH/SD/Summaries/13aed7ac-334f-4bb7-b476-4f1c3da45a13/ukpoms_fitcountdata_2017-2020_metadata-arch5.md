# UK Pollinator Monitoring Scheme metadata: Flower-insect timed count data from the UK Pollinator Monitoring Scheme, 2017-2020 version 2

## Overview
- Metadata for the Flower-insect timed count (FIT Count) data from the UK Pollinator Monitoring Scheme (PoMS) covering 2017–2020 (version 2; 2017 pilot year).
- Two data files are provided: one for 1 km square FIT Counts and one for Public FIT Counts.
- Version 2 has deduplicated data from the previous version.

## Data access and citation
- Data accessible via DOI: https://doi.org/10.5285/13aed7ac-334f-4bb7-b476-4f1c3da45a13
- License: Open Government Licence (OGL).
- Usage terms: You must cite the dataset in any publication describing research using the data.
- Citation example provided in the metadata.
- Acknowledgements required for use, including funders and PoMS volunteers.
- Copyright held by UKCEH and partner organisations.

## Dataset scope and context
- PoMS is part of the Pollinator Monitoring and Research Partnership (PMRP) to track UK pollinator populations.
- Two surveys under PoMS:
  - Flower-Insect Timed Count (FIT Count) data included here.
  - 1 km square survey data (also published here, with pan-trap data in a separate dataset).
- Goals include engaging volunteers, informing national pollinator strategies, and enabling habitat- and crop-related pollinator monitoring.

## Methodology and sampling design
- FIT Count description:
  - Ten-minute count within a 50 cm × 50 cm quadrat, focusing on insects visiting target flowers.
  - Public FIT Count: locations/dates chosen by volunteers, counts from 1 April to 30 September; weather thresholds determine suitability.
  - 1 km square FIT Counts: same method as public counts, with 4 visits per summer in up to 75 randomly allocated 1 km squares; co-located with NPMS/Habitat mapping efforts.
- Habitat stratification:
  - 1 km squares classified by predominant land cover (agricultural vs semi-natural) using CEH Land Cover Map 2007.
  - Additional stratification by habitat type to investigate cropped vs non-cropped landscapes.
- Data quality controls:
  - 2017–2020 online data entry via iRecord/Indicia; post-season QA checks; photo verification for target flowers; floral unit verification; plant family lookups; geolocation checks; date-range filtering.

## Data files and key attributes
- ukpoms_1kmFITCountData_2017-2020.csv
  - Contents: FIT Count results from the 1 km square surveys.
  - Key attributes include sample_id, country (England, Scotland, Wales), location_code/name, X1km_square, date/year, land_cover (agricultural or semi-natural), habitat, target_flower (with corrections), target_flower_family, floral_unit_count/type, habitat_type, count_start_time, cloud_cover, sunshine, wind_speed, insect group counts (bumblebees, honeybees, solitary_bees, wasps, hoverflies, other_flies, butterflies_moths, beetles, insects_small, insects_other), and totals.
  - Additional fields: data entry provenance, recorder_type, and qualitative context (flower_context, target flower corrections).
- ukpoms_publicFITCountData_2017-2020.csv
  - Contents: FIT Count results from public (volunteer) counts.
  - Key attributes include sample_id, country (England, Isle of Man, Northern Ireland, Scotland, Wales), date/year, X1km_square, sample_projection, digitised_by, recorder_type, habitat, target_flower (and corrected), target_flower_family, flower_cover, floral_unit_count/type, flower_context, cloud_cover, sunshine, wind_speed, enjoyment, difficulty, habitat_type, flower_structure, and insect group counts (bumblebees, honeybees, solitary_bees, wasps, hoverflies, other_flies, butterflies_moths, beetles, insects_small, insects_other) and all_insects_total.
  - Notable notes: Some Northern Ireland data include NA for some fields; corrected columns exist to accommodate photos-based reclassification.
- Both files include QA-related fields (target_flower_corrected, target_other_name_corrected, etc.), enabling standardized analyses across years and survey types.

## Quality assurance and data curation
- Data entry and validation:
  - Consistency checks via online forms; end-of-season QA by PoMS staff.
  - Photo verification to confirm or adjust target flower identifications; corrected floral units and plant-family lookups applied where needed.
  - Geolocation verification to ensure 1 km square alignment; misentries migrated to correct datasets.
  - Recording period and geolocation completeness checks leading to exclusions where appropriate.
- Documentation:
  - Methodology guidance and data interpretation resources available on the PoMS website; supports reproducibility and consistent use.

## Provenance, governance, and interoperability
- Governance:
  - Produced by UK Centre for Ecology & Hydrology (UKCEH) in collaboration with partner organisations; dataset complements PMRP efforts and national pollinator strategies.
  - Acknowledges Defra, devolved governments, JNCC, and UKCEH as funders; PoMS staff oversee data quality and curation.
- Interoperability:
  - Data harmonized across 2017–2020 with retrospective translations to align 2017 terms with 2018–2020 terminologies for consistent analysis.
  - Co-located sampling with other national schemes (NPMS) to support stratified analyses by habitat and land cover.

## Usage, attribution, and references
- Appropriate citation required per the data licence; standard citation provided in metadata.
- Acknowledgement of PoMS contributors and funding bodies is required in publications.
- References included for design, PMRP establishment, and progress reports:
  - Carvell et al. 2016; Carvell et al. 2020; PMRP progress reports (2020).
- Data users are encouraged to consult Annexes and PoMS guidance for detailed methodology and habitat mapping context.

## Summary for Data Stewards
- This dataset adheres to open data practices with a clear licence, citations, and acknowledgments.
- Metadata captures essential governance, provenance, and quality assurance steps, enabling trustworthy reuse and integration with other pollinator datasets.
- The dual-file structure (1 km square vs public FIT Counts) supports versatile analyses across scales and habitats, with standardized fields and corrections to ensure comparability over time.
- While challenges noted in the broader archetype (timeliness, cross-system interoperability, and metadata completeness) are mitigated here through structured QA, deduplication (version 2), and harmonized terminology.