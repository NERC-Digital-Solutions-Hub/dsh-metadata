# NPPMF_CropPollinationPilot_2015_QuestionnaireData

## Overview
- Data from 35 recorders on experiences carrying out pollinator surveys across apples, field beans, and oilseed rape.
- Collected in 2015 by teams at the University of Reading and the James Hutton Institute (Scotland).
- Respondents varied: novice data collectors, professional researchers, and farmers/agronomists; not all used all methods or surveyed all crops.

## Data Collection & Methods
- Volunteer recorders implemented pollinator survey techniques in flowering crops following detailed protocols.
- After completing methods, recorders filled out a questionnaire.
- Methods included: pan trapping, transect walking, hand pollination, and plant bagging.
- Transects: 50 meters with a 1 m² moving observation window.
- Pan trapping: three colored water trap arrays along the 50 m transect; insects recorded at survey end.
- Hand pollination/plant bagging: mesh bags to exclude visitation, hand pollination, and counting/marking flowers with cable ties.

## Data Structure & Content
- Columns (structured data): 
  - Crop, Site (RD for Reading, JHI for James Hutton Institute)
  - Recorder (unique code per individual)
  - Recorder type (Novice, Research, Farmer/Agronomist)
  - Survey method (Overall)
  - Question (the statement being scored)
  - Response options (Strongly agree, Agree, Neither agree nor disagree, Disagree, Strongly disagree)
  - Comments (supporting or reflective notes)
- Comments field provides justification or context for scores.

## Provenance & Metadata
- Data contributed by 35 recorders across two institutions.
- Unique recorder codes enable traceability of responses.
- Quality Assurance: No specific quality assurance was performed.

## Quality, Gaps & Considerations
- Potential issues:
  - Variation in recorder experience may affect responses.
  - Not all data completed for every crop or method; possible missing data.
  - Absence of QA introduces reliability concerns.
- Metadata clarity: explicit definitions for method categories (Overall vs. specific methods) and questions present but require consistent interpretation for reuse.

## Data Governance & Reuse
- Suitable for evaluating survey protocols, training needs, and data collection approaches in pollination studies.
- Reuse considerations:
  - Harmonize coding of survey methods and questions across datasets.
  - Acknowledge potential biases from recorder heterogeneity and the lack of QA.
  - Document data lineage and provenance for reliable interpretation.

## Relevance to Data Leaders
- Illustrates end-to-end data lifecycle: ground data collection, metadata, response coding, and initial quality considerations.
- Highlights importance of standardization, metadata richness, and basic QA to enhance data discovery, interoperability, and long-term value.
- Emphasizes need for clear data governance practices when aggregating data from multiple contributors and methods.

## Recommendations for Data Strategy
- Implement basic data quality checks and validation rules during and after collection.
- Develop a comprehensive data dictionary and standardized schemas for methods, questions, and response categories.
- Capture additional contextual metadata (e.g., observer training level, environmental conditions, method-specific details).
- Establish a central, versioned data repository to improve discoverability, provenance tracking, and collaboration.
- Consider coordinating across projects to reduce duplication of effort and foster communities of practice.