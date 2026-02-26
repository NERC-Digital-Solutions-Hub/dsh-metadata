# Glastir Monitoring & Evaluation Programme

- Overview and purpose
  - Welsh Government monitoring of agri-environment schemes (AES) biodiversity outcomes through the Glastir Monitoring & Evaluation Programme (GMEP) since 2013.
  - Aims to measure landscape features, trees and woodland management, contributing to biodiversity evidence and progress toward reversing declines in Wales’ native biodiversity.
  - Uses an ecosystem-based approach with data collected across multiple scales in a single snap-shot visit, enabling analysis of spatial variation and temporal trends.

- Survey design and sampling framework
  - 4-year rolling survey cycle (first cycle 2013–2016) to maximize site coverage while enabling year-on-year trend detection.
  - Two components:
    - Wider Wales Component: baseline estimation, national trends, and national reporting for Glastir.
    - Targeted Component: focuses on Glastir priority areas.
  - Common spatial unit: 1 km x 1 km squares.
  - Sampling plan: 300 1 km squares over the cycle; half randomly sampled within strata defined by the ITE Land Classification of Great Britain (Bunce et al., 2007), with sampling proportional to stratum size; half targeted at Glastir priority areas.
  - Exclusion criteria: remove squares with >75% urban land or >90% sea (per LCM2007 and UK Census high-tide data).

- Data collection methods and data structure
  - Within each 1 km square, mapping of point, areal, and linear features onto base maps using pre-determined coded options (field handbooks specify attributes and codes).
  - Data capture: electronic collection using CS Surveyor software (with Esri GIS integration) to minimize post-survey digitising errors.
  - Feature types:
    - Point features: small-scale elements (e.g., individual trees or groups, ponds, cliffs, buildings) with various use codes (e.g., residential, agricultural).
    - Areal/line features: captured according to habitat attributes and survey protocols.
  - Primary dataset: GMEP_LANDSCAPE_PT_FEATURES_2013_16.csv containing landscape point features across up to 300 squares, with fields such as:
    - SQ_ID (1 km square code)
    - PCOMPDATA_ID, PCOMPDATA_GUID (landscape point identifiers)
    - THEME, HABITAT_NAME, VETERAN_TREE_TYPE, DEAD_MISSING_BARK, LIGHTNING_STRIKES, MISSING_LIMBS, HOLLOW_TRUNK, DEAD_WOOD, IVY_COVER, EPIPHYTE_COVER, CANOPY_LIVE, TREE_DEAD, VEGETATION_TYPE, MODAL_DBH, SPECIES, PROPORTION, USE, HABITAT_BOX, DISEASE_SIGNS, BUFFER, SURVEY_YEAR
    - Spatial references: EASTING_10km, NORTHING_10km (10 km resolution, OSGB 1936) and LC (ITE Land Classification 2007)
    - Notes: Species nomenclature follows Stace (1997)
  - Data confidentiality: coordinates provided as 10 km resolution to protect precise locations.

- Quality assurance and data governance
  - Staff and methodological QA through trained survey teams and strict adherence to field handbooks (Maskell et al., 2016a & 2016b).
  - Digital data capture via CS Surveyor reduces transcription errors; mandatory fields and prompts standardize data collection.
  - Post-survey quality control (QC) includes a second team re-surveying all or part of a square; findings feed back to improve future recording.
  - Ongoing internal team roles and expertise documented (project management, habitat and vegetation specialists, GIS and database management, sampling and statistical leadership).

- Field teams and leadership
  - QA and project leadership roles listed (e.g., Astbury, Burden, Emmett, Maskell, Norton, Owen, Sharps, Smart, Williams, Wood, Wright) with specific areas of responsibility.
  - Field survey teams comprised named individuals across Wales, including Habitats and Vegetation specialists, surveyors, and coordinators.

- Resources and references
  - Field handbooks: Glastir Monitoring & Evaluation Programme Mapping Field Handbook Part 1 (Habitat attributes) and Part 2 (Using Surveyor software).
  - Key methodological references: ITE Land Classification of Great Britain (Bunce et al., 2007); Biodiversity classifications and UK BAP references; Field handbooks and project website.
  - Official sources and documents: Glastir Monitoring & Evaluation Programme website (https://gmep.wales/); annual and final reports by Emmett et al. (2014, 2017) and associated CEH/NERC documentation.

- Data availability and potential GIS applications
  - Dataset and metadata are structured for integration with national and sub-national analyses, enabling cross-comparison with the Countryside Survey of Great Britain methodologies.
  - The 1 km square framework and standardized attribute fields support map-based visualizations of landscape features, biodiversity indicators, and habitat conditions across Wales.
  - Data can inform policy discussions, ecological assessments, and landscape management planning at multiple scales.