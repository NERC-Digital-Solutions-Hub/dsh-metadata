# NPPMF_CropPollinationPilot_2015_QuestionnaireData

## Overview
- Dataset of responses from 35 recorders who participated in pollinator surveys on three crops: apples, field beans, and oilseed rape.
- Collected by teams at the University of Reading and the James Hutton Institute (Scotland).
- Respondents varied in experience (novice data collectors, experienced researchers, farmers/agronomists).
- Not all recorders used all methods or surveyed all crops; data collection was heterogeneous.

## Data collection and methodology
- Volunteer recorders followed detailed written protocols and completed a questionnaire after performing methods.
- Methods used included: pan trapping, transect walking, and/or hand pollination with plant bagging.
- Transect method: 50-meter transects with a 1 m² moving observation window to record floral visitors.
- Pan trapping: three colored water trap arrays along a 50 m transect; insects recorded from traps at survey end.
- Hand pollination and plant bagging: mesh bags to exclude insect visitation, hand pollination, and counting/marking flowers with cable ties.

## Data structure and fields
- Column headers include:
  - Crop: crop species surveyed.
  - Site: field site, with RD (Reading) or JHI (James Hutton Institute) and a unique field number.
  - Recorder: unique identifier for each individual recorder.
  - Recorder type: Novice, Research, or Farmer/Agronomist.
  - Survey method: indicates whether the question refers to the overall survey process.
  - Question: the statement being scored.
  - Response: Likert-type options (Strongly agree, Agree, Neither agree nor disagree, Disagree, Strongly disagree).
  - Comments: additional notes supporting the response.
- Quality Assurance: No specific QA was performed for the data.

## Data completeness and variability
- Data reflect responses from 35 recorders, with variability in which methods and crops were used by each recorder.
- Some questions/methods may have incomplete responses due to the non-uniform data collection across recorders and crops.

## Data quality considerations for data support
- Heterogeneous respondent backgrounds may introduce varied interpretation of questions.
- Absence of QA suggests potential data quality issues to address during cleaning and validation.
- Metadata (sites, recorder IDs, and crop/method combinations) require careful harmonization for analysis.

## Potential data products and use for data support
- Summaries of responses by crop, site, recorder type, and method to assess ease of protocol, perceived usefulness, or clarity.
- Dashboards or pivot tables showing distribution of responses across questions and methods.
- Data cleaning steps to standardize site codes (RD/JHI), recorder IDs, and method classifications.
- Documentation of limitations stemming from incomplete responses and lack of QA.