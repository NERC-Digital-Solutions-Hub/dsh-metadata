# NPPMF_CropPollinationPilot_2015_QuestionnaireData

## Overview
- Dataset of questionnaire responses from 35 recorders assessing their experience carrying out pollinator surveys on three crops: apples, field beans, and oilseed rape.
- Collected from teams at the University of Reading (RD) and the James Hutton Institute (JHI) in Scotland.
- Respondents varied in experience (novice, researchers, farmers/agronomists) and did not all complete every method or survey across all crops.

## Data collection and methods
- Volunteer recorders implemented pollinator or pollination service measurement techniques on flowering crops.
- Detailed written protocols provided for each method; participants completed a questionnaire after implementation.
- Methods used:
  - Pan trapping: three colored water trap arrays along a 50m transect; recorded insects caught.
  - Transect walking: walking a 50m transect with a 1m^2 moving observation window to record floral visitors.
  - Hand pollination and plant bagging: mesh bags over flowers to exclude visitation, hand pollination, and counting/marking flowers (with cable ties).

## Data structure and fields
- Columns include:
  - Crop: crop species surveyed.
  - Site: field site coded as RD (Reading) or JHI (James Hutton Institute) with a numeric site identifier.
  - Recorder: unique code for each individual recorder.
  - Recorder type: Novice, Research, or Farmer/Agronomist.
  - Survey method: method or combination of methods referenced (e.g., Overall).
  - Question: statement being scored by the recorder.
  - Response: Likert-scale options—Strongly agree, Agree, Neither agree nor disagree, Disagree, Strongly disagree.
  - Comments: additional notes supporting the score.
- Not all recorders used all methods or surveyed all crops.

## Sample and data quality
- 35 respondents across two institutions.
- No specific quality assurance was performed on the data.

## Potential analyses for an Analyst
- Examine correlations between recorder type and agreement with questions (e.g., attitudes toward methods, perceived ease, or perceived effectiveness).
- Compare responses across crops (apples, field beans, oilseed rape) and across survey methods (pan traps, transects, hand pollination).
- Evaluate consistency of responses within recorder types to assess reliability of self-reported experiences.
- Identify gaps where data are missing (which crops/methods were less represented) to guide future data collection or training needs.
- Integrate with external datasets to explore associations between recorder experience and data quality or outcomes (e.g., observer effort, time spent, accuracy of counts).

## Data provenance and accessibility
- Origin: questionnaire data from field surveys conducted by University of Reading and James Hutton Institute in 2015.
- Structure intended to capture both methodological implementation details and respondent perceptions to support meta-analyses of pollinator survey protocols.
- Data note: quality assurance is not documented, which may influence interpretation and modelling efforts requiring data reliability checks.