# River Habitat Survey (RHS) data 1998 [Countryside Survey] Dataset  description

## Overview
- Describes the 1998 River Habitat Survey (RHS) data from the Countryside Survey, with copyright by NERC - Centre for Ecology & Hydrology.
- Complements field handbooks and technical reports from Countryside Survey 2000 and 2007 headwater streams; official RHS website referenced.
- Data capture focuses on the physical structure of freshwater streams and rivers using standardized sampling units (500 m length per site) and 1 km square sampling sites; surveyors must be accredited to ensure consistency.
- Data were collected on paper field sheets, entered into a database, and cross-checked against original sheets to correct data-entry errors.
- Version: 1 (19/10/2016).

## What RHS measures and data scope
- Assesses physical river/channel structure rather than requiring expert geomorphology or botany; aims for consistent recognition of features across sites.
- 1 km square sampling framework with multiple field survey components collected during a single RHS site visit.
- Key data outputs include site details, field survey sections, land classification, hydrology, channel morphology, substrate/flow characteristics, vegetation, bank features, land use around banks, and habitat quality/ modification scores.
- Data designed to support broad analyses of river habitat condition and habitat quality across GB.

## Data structure and main data tables
- STREAM_RHS_SURVEY_main_98.csv
  - Description: Core site and field-survey details, covering sections A, B, C, D, J, K, L, M, N, O, P, and Q.
  - Notable fields:
    - SQUARE: 1 km square sampling site code
    - SITE_ID: Site identifier within the square
    - CS_SURVEY: Year of survey (formatted as 'CS' + year, e.g., CS2000 for 1998 data)
    - COUNTRY, COUNTY07: Administrative location
    - LC07, LC07_NUM: Land classification (2007 classification system)
    - SURVEY_DATE: Date of survey
    - HYDRO_UNIT: Hydrological Unit/Area
    - VALLEY_FORM, VALLEY_TERR: Valley form and terraces
    - Riffle/Pool/Run/Boils/Glides/Pools/Run descriptors: Structural channel features
    - CH_REALIGN, CH_OVER_DEEP, BED_MATERIAL/ DESCRIPTION: Channel morphology and bed materials
    - BANKFULL_LEFT/RIGHT, BKTOP_HT_LEFT/RIGHT: Bank full metrics and banktop heights
    - WATER_WIDTH, WATER_DEPTH: Channel dimensions
    - TREES_L/R, SH_CHANNEL, OVERHANG, EX_B_ROOTS, UW_T_ROOTS, FALLEN_TREES, C_WOODY_DEB, etc.: Vegetation in and around the channel
    - MATURE_ISLAND, VEG_MCB/VEG_SB/UNVEG_*: Depositional features and vegetation characteristics
    - HQA_SCORE: Habitat Quality Score
    - HMS_CLASS: Habitat Modification Scores Class
    - ANIMALS, L_MANAGE, MAJ_IMP, etc.: Overall habitat characteristics and management aspects
  - Emphasizes provided definitions and coding for many fields (e.g., numeric and text codes, missing value markers like -9).

- STREAM_RHS_SURVEY_spotcheck_98.csv
  - Description: Spot-check data for RHS sections E, F, and G.
  - Notable fields:
    - YEAR, SQUARE, LC07/LC07_NUM, COUNTRY, COUNTY07
    - SPOT: Spot-check number; details on left bank material (LB_MAT, LB_MAT_DESC), bank modifications, marginal features, channel substrates, and related descriptions
  - Captures supplementary and descriptive information to supplement main site surveys.

- STREAM_RHS_SURVEY_bank_98.csv
  - Description: RHS data for sections H and I (sweep-up).
  - Notable fields:
    - BANK: Left or right bank surveyed
    - BANK-related land use within 50 m of banktop (OPEN_WATER, R_PASTURE, URBAN, etc.)
    - LAND USE categories and near-bank attributes (BROAD, CONIF, SCRUB, ORCHARD, WETLAND, IRRIG, PARK, URBAN, etc.)
    - Detailed bank profile attributes (banktop/bankface structures, reinforcement types, embankments, channel geometry)
    - CV_* fields describing vegetation types along the channel (liverworts/mosses/lichens, emergent herbs, reeds/sedges, etc.)
    - Channel features and bank profile descriptors (L_BTOP, L_BFAC, R_BTOP, R_BFAC, USE5_L/USE5_R, etc.)
    - Habitat and modification scores (HQA_SCORE, HMS_CLASS) continued from main table
  - Emphasizes comprehensive near-bank land use and structural attributes, with numerous coded options and descriptive fields.

- Data usage and attribution
  - All RHS data must be acknowledged as Countryside Survey data owned by NERC - Centre for Ecology & Hydrology.
  - Acknowledgement required in copies, publications, and presentations: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology” and copyright statement for Countryside Survey data.

## Data quality, methods, and governance
- Field data collection followed standard protocols and required accreditation of surveyors to ensure consistency.
- Paper field sheets were entered into a database and cross-checked against the original sheets; data-entry errors corrected.
- The dataset leverages established field manuals and technical reports (e.g., Countryside Survey 2000 module 2 freshwater studies) to support interpretation and comparability.
- Some fields use coded values (text/numeric) with explicit descriptions; missing values are represented by placeholders (e.g., -9) in several fields.

## Practical use and considerations for data support
- Suitable for creating self-serve data products (dashboards, pivot-style reports) that enable users to explore river habitat structure and quality across sites.
- Enables cross-site comparisons by standardizing site identifiers (SQUARE, SITE_ID) and survey year (CS_SURVEY).
- Rich in near-bank land-use context and channel morphology, enabling analyses of relationships between bank features, land use, and habitat quality or modification status.
- Consider data completeness and coding when integrating with other datasets; ensure proper acknowledgement and refer to the cited handbooks and reports for interpretation of complex fields.

## Appendix: Key references and access notes
- Core references include:
  - Furse et al. 1998; Countryside Survey 2000; Module 2: survey of freshwater habitats
  - Dunbar et al. 2010; Countryside Survey: Headwater Streams Report from 2007
  - CEH/River Habitat Survey official website
- Access considerations:
  - Data are provided with detailed field definitions and should be used in line with the Countryside Survey data license and acknowledgement requirements.
  - The dataset is designed to be integrated with other RHS outputs and related GB-wide hydromorphological data for broader ecological and policy-relevant analyses.