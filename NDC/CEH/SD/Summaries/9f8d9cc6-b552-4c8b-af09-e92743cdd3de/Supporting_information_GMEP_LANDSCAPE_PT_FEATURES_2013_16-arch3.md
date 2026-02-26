# GMEP_LANDSCAPE_PT_FEATURES_2013_16.csv

## Overview, aims and context
- Wales-administered agri-environment schemes (AES) funding since the early 1990s supports landscape and biodiversity monitoring.
- Glastir Monitoring and Evaluation Programme (GMEP) established by the Welsh Government in 2013 to monitor Glastir’s effects on the environment, with a biodiversity focus to support progress toward reversing declines and CBD 2020 obligations.
- The landscape point features data contribute to ecosystem-based biodiversity measurement and national/national-trend reporting within Glastir.

## Monitoring design and sampling framework
- Longitudinal, rolling 4-year survey cycle (first cycle 2013–2016) to maximise site coverage and detect spatial and temporal trends cost-effectively.
- Two main components:
  - Wider Wales Component: baseline estimation and national trends for Glastir.
  - Targeted Component: links specifically to Glastir priority areas.
- Standardised spatial unit: 1 km grid squares; 300 squares sampled over the four-year cycle.
- Sampling strategy:
  - Half of squares are randomly sampled within strata defined by the ITE Land Classification of Great Britain (Bunce et al., 2007) to reflect environmental heterogeneity.
  - Other half are targeted at Glastir priority areas.
  - Exclusions: squares with >75% urban land or >90% sea coverage are excluded.
- Integration across metrics and future compatibility:
  - Same 1 km square unit across components allows data integration and potential future linkage with the Countryside Survey of Great Britain.

## Data collection methods and dataset structure
- Within each 1 km square, mapping of point, areal, and linear features onto base maps using predetermined codes.
- Field data collection:
  - Electronic data capture (CS Surveyor) with GIS support (Esri UK).
  - Field mapping handbooks guide methodologies (Maskell et al., 2016a & 2016b).
- Landscape point features:
  - Defined as features occupying less than 20 m × 20 m.
  - Examples include trees/groups of trees, ponds, cliffs, buildings, and land-use categories (e.g., residential, agricultural).
- Dataset: GMEP_LANDSCAPE_PT_FEATURES_2013_16.csv
  - Variables include: SQ_ID (1 km square site code), PCOMPDATA_ID, PCOMPDATA_GUID, THEME, HABITAT_NAME, VETERAN_TREE_TYPE, DEAD_MISSING_BARK, LIGHTNING_STRIKES, MISSING_LIMBS, HOLLOW_TRUNK, DEAD_WOOD, IVY_COVER, EPIPHYTE_COVER, CANOPY_LIVE, TREE_DEAD, VEGETATION_TYPE, MODAL_DBH, SPECIES, PROPORTION, USE, HABITAT_BOX, DISEASE_SIGNS, BUFFER, SURVEY_YEAR, EASTING_10km, NORTHING_10km, LC.
  - Species nomenclature follows Stace (1997).
  - Spatial coordinates provided at 10 km resolution for confidentiality (EASTING_10km, NORTHING_10km).
  - Land Classification (LC) uses ITE GB 2007 framework.
  - Data supports multi-scale biodiversity indicators and landscape attributes.
- Data handling and metadata:
  - The dataset uses standardized field codes and definitions (reference field handbooks for codes and categories).

## Quality assurance, governance and personnel
- QA processes:
  - Field surveys conducted by experienced botanical surveyors following rigorous training to ensure consistency with the field handbooks.
  - Electronic data capture reduces transcription errors and enables real-time data checks.
  - Mandatory data entry fields and prompts ensure completeness; post-field checks are enabled through rapid office data checks.
  - Quality control (QC) exercises: a second team repeats surveys in all or part of a square; feedback from QC informs field team improvements.
- Roles and teams:
  - QA and project leadership include specialists in database management, habitat work, vegetation and sampling design, statistics, GIS, and field coordination.
  - Field survey teams comprise numerous named surveyors and coordinators ensuring broad coverage across Wales.

## Outputs, publications and documentation
- Outputs contribute to national biodiversity evidence and Glastir reporting, supporting CBD alignment and policy evaluation.
- Key documentation and references:
  - Field handbooks: Glastir Monitoring & Evaluation Programme Mapping Field Handbook Part 1 (Habitat attributes) and Part 2 (Using Surveyor software) (2016).
  - Annual and final reports: Year 1 Annual Report to Welsh Government (2014); Final Report to Welsh Government – Executive Summary (2017).
  - Glastir Monitoring & Evaluation Programme website: gmep.wales (overview, methodologies, results).
  - Methodological references: ITE Land Classification of Great Britain (Bunce et al., 2007); guidance and related biodiversity classifications; Stace (1997) for species nomenclature.

## Key takeaways for monitoring framework authors
- Adopt an ecosystem-based, multi-scale data collection approach integrated within a single field visit to maximize efficiency and comparability.
- Implement a rolling, multi-component survey design to capture baseline, trends, and priority-area signals while ensuring national comparability.
- Use standardized sampling units (e.g., 1 km squares) and align with established national surveys to enable future data integration.
- Combine robust data capture technologies with rigorous QA and QC processes to maintain data quality and reproducibility.
- Build comprehensive metadata and documentation (field handbooks, data dictionaries) and maintain transparent data governance and access pathways.