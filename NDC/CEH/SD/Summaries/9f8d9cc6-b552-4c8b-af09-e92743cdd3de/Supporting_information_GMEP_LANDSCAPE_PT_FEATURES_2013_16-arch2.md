# Glastir Monitoring & Evaluation Programme (GMEP) – Landscape point features 2013-16

## Overview and Aim
- Welsh Government monitoring programme (GMEP) established in 2013 to assess Glastir scheme’s effects on the environment.
- Data contribute to biodiversity evidence base for Wales and support obligations under the Convention on Biological Diversity (CBD) 2020.
- Focus: landscape features and trees/woodland management; aims to track biodiversity progress and inform policy performance over time.

## Survey Design and Sampling
- 4-year rolling survey cycle (2013–2016) to maximize site visits nationally while enabling year-on-year trend detection in a cost-efficient way.
- Two components:
  - Wider Wales Component: baseline estimation, national trends, national reporting for Glastir.
  - Targeted Component: links to Glastir priority areas.
- Common spatial unit: 1 km²; sampling across both components with 300 squares in total per cycle.
- Sampling approach:
  - Half of squares randomly sampled within strata defined by the ITE Land Classification of Great Britain (Bunce et al., 2007) to minimize environmental heterogeneity within strata and maximize differences between strata.
  - Other half targeted specifically at Glastir priority areas.
- Exclusion criteria: remove squares with >75% urban land or >90% sea (based on LCM2007 and census high-tide data).

## Data Collection Methods
- In each 1 km² survey area, map point, areal, and line features onto base maps using predetermined coded options.
- Data capture via electronic tools: CS Surveyor software (CEH) and Esri GIS suite.
- Point features: <20 m × 20 m; include trees/groups, ponds, cliffs, buildings, with use codes (e.g., residential, agricultural).
- Data stored and uploaded to appropriate data portals; integrated across metrics to support ecosystem-based analysis.

## Data Schema and Variables (GMEP_LANDSCAPE_PT_FEATURES_2013_16.csv)
- Core fields:
  - SQ_ID: 1 km square sampling site code.
  - PCOMPDATA_ID: landscape point identifier.
  - PCOMPDATA_GUID: Globally Unique Identifier for the point.
  - THEME, HABITAT_NAME: broad feature type and primary descriptor.
  - VETERAN_TREE_TYPE, DEAD_MISSING_BARK, LIGHTNING_STRIKES, MISSING_LIMBS, HOLLOW_TRUNK, DEAD_WOOD, IVY_COVER, EPIPHYTE_COVER, CANOPY_LIVE, TREE_DEAD: various attributes related to veteran trees and tree health.
  - VEGETATION_TYPE, MODAL_DBH, SPECIES, PROPORTION: vegetation characteristics and species data.
  - USE, HABITAT_BOX, DISEASE_SIGNS, BUFFER: functional/use features, habitat considerations, disease signs, buffering.
  - SURVEY_YEAR: year of survey.
  - EASTING_10km, NORTHING_10km, LC: grid references and Land Classification category.
- Species nomenclature follows Stace (1997).
- Purpose: capture multi-scale landscape features and associated attributes for integration with broader biodiversity indicators.

## Quality Assurance (QA) and Data Quality
- Surveys conducted by experienced botanical surveyors; mandatory training to ensure consistency with GMEP field handbooks.
- Electronic data capture reduces transcription errors; built-in prompts and mandatory fields to ensure data completeness.
- Central QA: second-team QC surveys to verify data in all or part of a square; feedback loop to field teams to improve data quality.
- Team roles and project leadership documented for ongoing quality and methodological rigor.

## Field Teams and Leadership
- Project leadership and technical experts across habitat, vegetation, statistics, GIS, and database management.
- Field survey teams comprised of numerous named surveyors and field staff, ensuring broad geographic coverage and capacity.

## Accessibility, Reuse, and Integration
- Emphasis on integrating survey data across scales and with national surveys (e.g., Countryside Survey) thanks to harmonized sampling units and methodology.
- Data are stored and uploaded to appropriate portals to enable access and reuse by policymakers, researchers, and stakeholders.
- The GMEP website provides methodological details, linked handbooks, and results for transparency and further analysis.

## Relevance to Environmental Monitoring and Policy
- Provides standardized, repeatable biodiversity and landscape feature indicators aligned with Welsh environmental policy goals.
- Enables monitoring of year-on-year changes and national trends, supporting evidence-based decision making and biodiversity recovery targets.
- Offers a structured dataset for multi-criteria analysis, enabling data readers to assess habitat attributes, veteran trees, vegetation types, and associated ecological features.

## Key References and Documentation
- Field handbooks and methodology: Glastir Monitoring & Evaluation Programme Mapping Field Handbook Parts 1 and 2 (habitat attributes; using Surveyor software).
- Land Classification framework: Bunce et al. 2007 (ITE Land Classification of Great Britain).
- GMEP reports and outputs: annual and final reports (2014–2017) to Welsh Government; CEH and NERC project documents.
- Related biodiversity and habitat guidance: JNCC Biodiversity Broad Habitat classifications; UKBAP Priority Habitat Descriptions.
- GMEP website: gmep.wales (central hub for methodology, results, and documentation).