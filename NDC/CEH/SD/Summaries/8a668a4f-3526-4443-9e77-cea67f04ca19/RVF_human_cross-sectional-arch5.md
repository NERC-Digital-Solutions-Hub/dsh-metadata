# Rift Valley fever virus seroprevalence data from people involved in a cross-sectional survey in Tana River and Garissa counties, Kenya (December 2013 - February 2014)

## Overview
- Cross-sectional serosurvey examining Rift Valley fever (RVF) seroprevalence as a case study of disease risk related to land use changes (irrigation schemes) in pastoral rangelands.
- Household-level sampling with a target of 220 households per land-use type; included irrigated, pastoral, and some riverine areas.

## Experimental Design & Sampling Regime
- Primary sampling units: households; subjects aged five years and older.
- Sample size determined by formal power calculation for comparing two proportions, to be 220 households per land-use type.
- Sites: Bura and Hola irrigation schemes (Tana River County) and adjacent areas, plus Ijara and Sangailu divisions (Garissa County).
- Sampling frame created from existing household registers, cleaned, and updated; random selection of households and individuals within households.
- One-stage sampling for a cross-sectional snapshot.

## Field Work & Data Collection
- Ethics: approvals from AMREF Ethics and Scientific Review Committee; community meetings to review objectives and plans; consent obtained at community, household, and individual levels.
- Data collection: electronic forms via Open Data Kit (ODK) on smartphones; GPS coordinates captured but geographic coordinates withheld for ethical reasons.
- Data linkage: barcoded sampling tubes linked to household and individual records; field team included clinicians and technicians; dry ice used for field preservation; samples transported to ILRI facilities and stored in cryo conditions.

## Laboratory Analysis
- Serum immunoglobulin G screening for RVF using an inhibition ELISA assay developed for humans and animals (Paweska et al., 2005).

## Dataset & Metadata
- Data file: DDDAC_Kenya_human RVF seroprevalence.csv
- Contains 23 variables with a detailed description provided (Table 1), covering:
  - Temporal data (dates of sampling)
  - Geographic and administrative units (county, district, division, location, sublocation, village)
  - Household and respondent identifiers (hhid, relationship to household head)
  - Demographics (hhgender, hhage, gender, age, occupation)
  - Sampling site characterization (area: irrigation, pastoral, riverine)
  - Laboratory results (result: positive/negative) and altitude
  - livestock presence at home (livestk_home)
- Data quality controls:
  - ODK used to minimize transcription errors by linking household data
  - Central ODK Aggregate server used to upload data daily
  - Barcoded tubes; field samples linked to household data; duplicate lab analyses
  - Serum/whole-blood samples aliquoted and stored, with duplicates and re-analysis for borderline results

## Data Handling, Storage & Accessibility
- Specimens preserved in dry ice in the field and subsequently stored in liquid nitrogen at the ILRI biorepository.
- Centralized data repository and workflows ensured traceability from field collection to laboratory analysis.
- Some data elements withheld due to ethics (geographic coordinates); blank cells indicate non-recorded or undisclosed data.

## Governance, Ethics & Compliance
- Multi-level consent processes implemented to protect participant rights and confidentiality.
- Metadata and dataset structure documented to support data reuse while respecting ethical and disclosure constraints.
- Clear linkage between sampling, laboratory results, and metadata to support reproducibility and data discovery.

## Practical Considerations for Data Stewards
- Ensure ongoing data governance for similar large-scale serosurveys, including:
  - Documentation of data schemas (variables and descriptions)
  - Metadata that describes sampling design, field procedures, and lab methods
  - Data quality assurances (field validation, duplicate testing, and re-analysis policies)
  - Access controls and ethical protections, especially for geospatial data
  - Provenance tracking from collection to final dataset release
  - Clear guidance on handling missing or undisclosed data elements