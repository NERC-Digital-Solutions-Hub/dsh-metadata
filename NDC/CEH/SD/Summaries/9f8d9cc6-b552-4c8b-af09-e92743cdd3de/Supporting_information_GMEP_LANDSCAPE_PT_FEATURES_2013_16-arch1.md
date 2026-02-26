# Glastir Monitoring & Evaluation Programme – Landscape point features 2013-16

## Overview
- Wales implemented agri-environment schemes since the early 1990s (e.g., ESAs, Tir Cymen, Tir Cynnal, Tir Gofal) and now Glastir.
- The Glastir Monitoring and Evaluation Programme (GMEP) was established by the Welsh Government in 2013 to monitor environmental impacts, specifically biodiversity and woodland management, supporting Wales’ CBD2020 obligations.
- The dataset focuses on landscape point features collected during the 2013–2016 monitoring cycle.

## Survey design and sampling framework
- The GMEP uses a 4-year rolling, multi-metric, ecosystem-based survey to capture spatial and temporal variation cost-effectively.
- Two components:
  - Wider Wales Component: baseline estimation and national trends for Glastir.
  - Targeted Component: links to Glastir priority areas.
- A common spatial unit of 1 km² is used for integration and comparability.
- Sampling plan:
  - 300 1 km² squares sampled over the cycle.
  - Half are Wider Wales squares, randomly sampled within strata defined by the ITE Land Classification of GB (Bunce et al., 2007) to maximize environmental heterogeneity between strata.
  - Half are targeted at Glastir priority areas.
- Exclusions: squares with more than 75% urban land or more than 90% sea are excluded (based on LCM2007 and census tide data).

## Data collection methods
- Within each 1 km² square, point, areal, and line features are mapped onto base maps using predefined codes.
- Data collection tools:
  - Electronic data capture using CS Surveyor software and Esri GIS.
- Point features:
  - Defined as features occupying less than 20 m × 20 m.
  - Include trees or groups of trees, ponds, cliffs, buildings, and land-use use codes (e.g., residential, agricultural).
- Documentation:
  - Field Mapping Handbooks (Maskell et al., 2016a & 2016b) provide definitions and methodology.

## Dataset contents
- Dataset: GMEP_LANDSCAPE_PT_FEATURES_2013_16.csv
- Key fields include:
  - SQ_ID: 1 km square sampling site code.
  - PCOMPDATA_ID / PCOMPDATA_GUID: landscape point identifiers (with GUIDs).
  - THEME, HABITAT_NAME: broad feature type and primary attribute.
  - VETERAN_TREE_TYPE, DEAD_MISSING_BARK, LIGHTNING_STRIKES, MISSING_LIMBS, HOLLOW_TRUNK, DEAD_WOOD, IVY_COVER, EPIPHYTE_COVER, CANOPY_LIVE, TREE_DEAD: condition and vegetation attributes for veteran trees.
  - VEGETATION_TYPE, MODAL_DBH, SPECIES, PROPORTION, USE, HABITAT_BOX, DISEASE_SIGNS, BUFFER: additional descriptive attributes.
  - SURVEY_YEAR: year of survey.
  - EASTING_10km, NORTHING_10km: 10 km grid coordinates (OSGB 1936).
  - LC: Land Classification category (ITE LB 2007).
- Species nomenclature follows Stace (1997).

## Quality assurance and governance
- Survey teams comprised experienced botanical surveyors; training provided to ensure consistency with field handbooks.
- Electronic data capture reduced post-survey digitising errors; mandatory data fields and prompts improved data completeness.
- Timely data transfer enabled prompt data checks.
- QC process: a second team of surveyors re-surveys all or part of a square to identify and feed back issues for improvement.
- Leadership and expertise contributions listed (QA leads, field team managers, statistical and GIS experts, etc.).

## Supporting materials and references
- Methodologies and references include:
  - ITE Land Classification of Great Britain (Bunce et al., 2007).
  - GMEP Year 1 and Final Report to Welsh Government (Emmett et al., 2014; 2017).
  - GMEP Field Mapping Handbooks (Maskell et al., 2016a, 2016b).
  - Glastir Monitoring & Evaluation Programme website (gmep.wales).
  - Guidance documents on biodiversity classifications (Jackson, 2000) and UK Biodiversity Action Plan descriptors (Stace, 1997; Maddock, 2008).

## How the data can be used
- Provide baseline estimates, national trends, and integration opportunities with GB-wide surveys for robust indicators.
- Support assessment of Glastir scheme impacts on biodiversity and landscape features at national, regional, and local scales.
- Facilitate evidence-based decision making for conservation and scheme effectiveness reporting, aligned with CBD obligations.
- Data are designed to be discoverable and usable with accompanying metadata through data portals.