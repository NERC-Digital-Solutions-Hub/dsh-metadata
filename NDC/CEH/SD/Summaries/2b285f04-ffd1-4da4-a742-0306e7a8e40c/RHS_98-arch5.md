# River Habitat Survey (RHS) data 1998 [Countryside Survey] Dataset description

## Overview
- Describes River Habitat Survey (RHS) data collected from freshwater streams and rivers using standard 500m sampling units; accreditation required for surveyors and adherence to standard protocols.
- Data are part of Countryside Survey 2000 (Module 2: Freshwater Studies) with accompanying supporting information and technical reports.
- Data ownership and rights: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology; all uses must be acknowledged with the provided acknowledgement text.

## Data collection and structure
- Methodology:
  - Standard 500m sampling unit for physical channel and catchment assessment.
  - Accredited surveyors ensure consistency in recording features; field methods and definitions are aligned with cited handbooks and reports.
  - Data collected on paper field sheets and subsequently entered into a database, then cross-checked against original sheets with corrections made for data-entry errors.
- Data tables and content:
  - STREAM_RHS_SURVEY_main_98.csv
    - Core site details and sections A, B, C, D, J, K, L, M, N, O, P, Q.
    - Key fields include SQUARE (1km square code), SITE_ID, CS_SURVEY (year), COUNTRY, COUNTY07, LC07 (land class 2007), ALTITUDE, SLOPE, FLOW_CATEGORY, CATCHMENT_AREA, STRAHLER_ORDER, HYDRO_UNIT, SURVEY_DATE, and numerous structural/geomorphological descriptors (valley form, riverscape features, bed/material, bank/top dimensions, channel form, woody debris, vegetation, and habitat features).
    - Includes land-use and environmental context, channel features, bed materials, and indicators of habitat condition (e.g., HQA_SCORE, HMS_CLASS).
  - STREAM_RHS_SURVEY_spotcheck_98.csv
    - Spot-check data for RHS sections E, F, and G; includes YEAR, SQUARE, LC07, COUNTY07, etc., plus spot-specific fields for left bank material and related descriptions (LB_MAT, LB_MD1/2, LB_FE1/2, CH_SUB, CH_FLW, etc.).
  - STREAM_RHS_SURVEY_bank_98.csv
    - Bank-related data for RHS sections H and I; covers land use within 50m of banktop (BROAD, CONIF, SCRUB, ORCHARD, WETLAND, OPEN_WATER, etc.), bank profiles (BANK, L_BTOP/L_BTOP_DESC, L_BFAC/L_BFAC_DESC), bank stability and restoration descriptors, and channel vegetation categories (CV_*, etc.), as well as habitat modification and land-use indicators.
- Documentation of fields:
  - Extensive definitions and coding schemes for land classification (LC07), environmental zones (EZ_DESC_07), hydrological units, bank and channel morphology, substrate, vegetation, debris, and habitat quality/modification scores.
  - Numerous predefined categories and codes (e.g., 1–9, Y/N, descriptive text) to standardize data entry and enable comparability across sites and surveys.

## Documentation, metadata, and references
- Primary documentation and supporting materials cited, including:
  - Furse et al. 1998; Countryside Survey 2000; Module 2: Freshwater Studies
  - Dunbar et al. 2010; Countryside Survey: Headwater Streams Report from 2007
  - River Habitat Survey official website and CEH/NERC resources
- Data dictionary and extensive field definitions accompany the dataset to support interpretation and reuse.

## Usage, access, and rights
- Acknowledgement requirement: All uses of Countryside Survey data must acknowledge NERC - CEH; include the standard Countryside Survey acknowledgement text in publications, presentations, and outputs.
- Rights: Countryside Survey data © NERC-CEH; all rights reserved.
- Sharing and discovery: Data are described with detailed metadata and field definitions to facilitate discovery, reuse, and integration with other datasets; recommended practice includes uploading datasets to relevant portals and catalogues.

## Practical considerations for Data Stewards
- Governance and provenance:
  - Clear ownership (NERC-CEH) and usage terms; need to enforce acknowledgement in downstream uses.
  - Historical dataset (1998 RHS within Countryside Survey) with multiple supporting reports; maintain links to source documentation for traceability.
- Standards and interoperability:
  - Comprehensive field dictionary supports consistent data capture and cross-study comparability.
  - Use of standardized codes (LC07, EZ_DESC_07, SQUARE, COUNTRY, etc.) to enable interoperability with other GB datasets.
- Data quality and lifecycle:
  - Data entry workflow (paper → database) with cross-checks against original sheets; corrections recorded to ensure data integrity.
  - Potential for updating datasets with new RHS findings or integrating with additional RHS modules; ensure update mechanisms respect existing data standards and citation requirements.
- Discoverability and attribution:
  - Detailed metadata and explicit acknowledgement requirements improve discoverability and proper attribution in publications and data portals.

## Endnotes and supporting information
- The dataset is accompanied by a suite of related reports and field handbooks that provide context, methodology, and classification schemes used in RHS and Countryside Survey datasets.
- Acknowledgement and copyright notice requirements are explicit and must be applied to all copies and outputs.