# River Habitat Survey (RHS) data 1998 [Countryside Survey] Dataset  description

- Purpose and scope
  - Provides a standardized assessment of the physical structure of freshwater streams and rivers as part of the Countryside Survey.
  - Based on a fixed 500 m sampling unit, requiring accreditation for surveyors; designed for cross-site comparability without specialist geomorphological or botanical expertise.
  - Data collected during the 1998 RHS fieldwork and linked to Countryside Survey 2000 freshwater survey work; data ownership and licensing governed by NERC-CEH.

- Data collection method
  - Field surveys follow standard RHS protocols documented in key field handbooks and reports.
  - Data collected on paper field sheets and subsequently entered into a database with cross-checks against original sheets to correct entry errors.
  - Coverage includes site-level attributes, channel morphology, hydraulics, vegetation, human modifications, and land-use context around banks.

- Data entry and quality assurance
  - Paper-to-database transcription with cross-checking against source sheets.
  - Protocols emphasize consistent recognition of features and surveyor accreditation to ensure recording consistency.
  - Metadata and data quality controls are embedded in the data collection and entry process.

- Data structure and tables (overview of main content)
  - STREAM_RHS_SURVEY_main_98.csv
    - Site details and field survey details across multiple RHS sections (A, B, C, D, J, K, L, M, N, O, P, Q).
    - Key fields include: SQUARE (1 km square code), SITE_ID, CS_SURVEY (survey year), country, county, environmental zone, stream/drain, distance from source, altitude, slope, flow category, catchment area, Strahler order, geology, hydro unit, survey date, adverse conditions, bed visibility, and various habitat and geomorphology indicators (e.g., valley form, riffles/pools, weirs/bridges, bank/bed materials, channel dimensions, vegetation features, and habitat modification scores).
    - Includes habitat quality indicators (HQA_SCORE) and habitat modification scores (HMS_CLASS).
  - STREAM_RHS_SURVEY_spotcheck_98.csv
    - Spot-check data for RHS sections E, F, and G; includes year, square, land class, country, county, spot number, left bank material and modifications, bank features, channel substrate, banktop land use, and related descriptive fields.
  - STREAM_RHS_SURVEY_bank_98.csv
    - Bank-related data for RHS sections H and I; documents land use within 50 m of banktop (various habitat types), bank profiles, bank structure (banktop, bankface, and near-bank features), and associated descriptive fields.
  - Additional notes
    - The dataset includes a comprehensive set of coded and descriptive fields for channel and bank features, vegetation types, land use classifications, and various physical attributes (width, depth, bankfull indicators, embankments, and other hydraulic/geomorphic features).

- Data governance, licensing, and acknowledgement
  - Data are provided by Countryside Survey, owned by NERC - Centre for Ecology & Hydrology; copyright is held by CEH.
  - All uses of Countryside Survey data must acknowledge: “Countryside Survey data owned by NERC - Centre for Ecology & Hydrology” and “Countryside Survey © CEH. All rights reserved.”
  - The RHS dataset is linked to a broader set of Countryside Survey outputs (e.g., official RHS website) and is tied to published technical reports and field handbooks.
  - Access and usage typically require compliance with the acknowledgement and licensing terms; data are described as publicly shareable under these conditions.

- Relevance for monitoring frameworks
  - Provides a robust, standardized baseline of freshwater habitat structure, suitable for evaluating policy impacts and informing future decisions.
  - The structured data model (main survey, spot-checks, and bank data) supports multi-dimensional monitoring of habitat quality, physical modification, and surrounding land use.
  - Rich metadata and explicit field definitions enable reproducibility and comparability across sites and time when integrated with other RHS or Countryside Survey datasets.
  - Data governance and licensing considerations (acknowledgement requirements and copyright) are important for governance, data sharing, and ensuring proper use within monitoring programs.

- Practical considerations for authors of monitoring frameworks
  - Leverage the standardized RHS methodology to minimize data silos and improve comparability across sites and over time.
  - Ensure metadata sufficiency is in place for data provenance, survey protocols, and classification schemes (e.g., land classes, habitat types, structural features).
  - Plan for data-sharing constraints and attribution requirements; establish clear data governance and licensing terms early in project design.
  - Use the multi-table RHS structure (main survey, spot-check, bank) to build comprehensive indicators of habitat condition, modification, and landscape context.