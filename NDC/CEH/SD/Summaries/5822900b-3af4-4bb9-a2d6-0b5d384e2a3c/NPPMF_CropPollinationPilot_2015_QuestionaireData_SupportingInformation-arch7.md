# NPPMF_CropPollinationPilot_2015_QuestionnaireData

## Overview
- Dataset of questionnaire responses from 35 volunteer recorders across two institutions (University of Reading and James Hutton Institute) in Scotland.
- Focuses on experiences carrying out pollinator surveys on three crops: apples, field beans, and oilseed rape.
- Collected in 2015 as part of a pollinator measurement pilot; recorders included novices, researchers, and farmers/agronomists.

## Data collection and methodology
- Recorders were taken to flowering crops to implement pollinator or pollination service measuring techniques.
- Each recorder followed detailed written protocols and completed a questionnaire after methods.
- Implemented three methods: pan trapping, transect walking, and/or hand pollination and plant bagging.
  - Transects: 50 m length, recording floral visitors within a 1 m² moving observation window.
  - Pan trapping: 3 colored water trap arrays along the 50 m transect; identification of captured insects.
  - Hand pollination and plant bagging: mesh bags over flowers to exclude visitation, hand pollination, and counting/marking flowers (with cable ties).

## Dataset structure (columns)
- Crop: crop species surveyed.
- Site: field site; codes RD (Reading) or JHI (James Hutton Institute); a unique crop field number.
- Recorder: unique code for each individual recorder (RD or JHI).
- Recorder type: Novice, Research, or Farmer/Agronomist.
- Survey method: indicates the scope (Overall includes entire survey process; may also refer to specific methods).
- Question: statement being scored by the recorder.
- Response: Likert-scale option (Strongly agree, Agree, Neither agree nor disagree, Disagree, Strongly disagree).
- Comments: supplementary notes provided by the recorder.

## Participants and dataset scope
- 35 recorders contributed data from two institutions.
- Not all recorders used every method or surveyed all crops.
- Recorder types include novice public participants, professional researchers, and farmers/agronomists.

## GIS relevance and potential uses
- Site-level identifiers (Site, crop field) enable spatial linking to other geospatial layers or field boundaries.
- Data can be mapped by crop, site, recorder type, and survey method to visualize distribution of survey effort and experience.
- Likely need for georeferencing of Site fields or joining with external spatial datasets to create spatial visuals (coordinates not provided in this dataset).
- Useful for quality checks, methodological coverage, and exploring spatial patterns in responses if integrated with spatial context (e.g., field locations, land use).

## Data quality and limitations
- No formal quality assurance was documented.
- Data variability due to mixed recorder expertise and partial method/application.
- Some crops/methods not uniformly represented across all recorders.
- Descriptive metadata about exact locations is limited; may require additional data sources to enable full GIS mapping.