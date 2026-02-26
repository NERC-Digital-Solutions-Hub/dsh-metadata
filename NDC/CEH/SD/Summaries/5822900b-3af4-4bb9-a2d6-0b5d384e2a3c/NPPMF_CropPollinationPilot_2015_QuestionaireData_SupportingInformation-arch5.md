# NPPMF_CropPollinationPilot_2015_QuestionnaireData

## Overview
- Data on responses from 35 recorders about pollinator surveys on three crops: apples, field beans, and oilseed rape.
- Collected from teams at the University of Reading and the James Hutton Institute (Scotland).
- Participants included novices, experienced researchers, and farmers/agronomists.

## Data Structure and Content
- Questionnaire-style dataset with:
  - Crop, Site (RD = Reading, JHI = James Hutton Institute), and Recorder (unique code per individual)
  - Recorder type (Novice, Research, Farmer/Agronomist)
  - Survey method (Overall or specific method)
  - Question (statement scored by the recorder)
  - Response options: Strongly agree, Agree, Neither agree nor disagree, Disagree, Strongly disagree
  - Comments (supporting notes)
- Columns capture both the measurement (Question) and the respondent’s stance (likert-style scale) plus qualitative feedback.

## Survey Methods and Protocols
- Recorders conducted pollinator/pollination surveys on flowering crops using three main methods: pan trapping, transect walking, and hand pollination with plant bagging.
- Transect protocol: 50 m transect with observations in a 1 m² moving window.
- Pan trapping: three colored water trap arrays along the same 50 m transect; insects collected and identified after the survey.
- Hand pollination and plant bagging: flowers bagged to exclude visits, hand pollination performed, and flowers counted/marked with cable ties.

## Provenance and Metadata
- Each data row ties to:
  - Crop type, field/site, and a recorder code (RD or JHI)
  - Recorder type and the survey method used
- Recorders were given detailed written protocols for each method prior to data collection.

## Data Quality and Gaps
- Quality Assurance: No specific quality assurance was performed.
- Data limitations: not all recorders used all methods; not all crops were surveyed by all recorders; potential inconsistencies across recorders and sites.
- Absence of QA implies potential data quality concerns requiring cleaning, validation, and documentation of any missing data or method applicability.

## Governance, Sharing, and Preservation Implications
- Rich metadata on survey methods and protocols supports data reuse, but the lack of QA necessitates careful interpretation.
- Anonymization considerations: recorders are identified by codes; ensure appropriate de-identification and usage rights when sharing publicly.
- Documentation should accompany the dataset to preserve provenance and method details for future users.

## Recommendations for Data Stewards
- Implement metadata standards to consistently capture crop, site, recorder, recorder type, survey method, each question, responses, and comments.
- Introduce a QA/validation step to assess data integrity, handle missing values, and reconcile method-specific responses.
- Document data provenance, versioning, and any transformations or cleaning performed.
- Define clear sharing licenses and access conditions; consider embargoes if needed and ensure appropriate anonymization where required.