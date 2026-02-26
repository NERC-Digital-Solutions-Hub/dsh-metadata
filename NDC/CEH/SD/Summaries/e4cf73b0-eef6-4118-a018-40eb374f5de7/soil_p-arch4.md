# Soil survey of Moor House, 1965.

## Overview
- Data from a soil survey at Moor House, Cumbria, UK, conducted by Mike Hornung as part of his PhD.
- Hornung’s PhD thesis is available in supporting documentation and online at a provided URL.
- The data were stored in a database described by Cuthbertson (1993) in Journal of Environmental Management.

## Data structure and contents
- Three CSV files describe the dataset:
  - D2SOIL_P.csv (Site Locations)
    - Key fields: PROF_NO (unique profile number), EASTING, NORTHING, LOCATION, REL_DATA, ALTITUDE (m), GEO_DATA, VEG_DATA.
  - D3SOIL_P.csv (Horizon analysis)
    - Key fields: PROF_NO (links to D2SOIL_P), HORIZON, FDEPTH (cm), TDEPTH (cm), REM1, REM2, TYPE (organic or mineral).
  - D4SOIL_P.csv (Chemical analysis and soil mineralogy)
    - Key fields: PROF_NO (links to D2SOIL_P), SMPL_NO (sample number; with Profile number forms a unique code), FDEPTH, TDEPTH, PH, CACO3, FE203, US_SAND, I_SAND, I_SILT, CLAY (two variants), US_SILT (two variants), BS, various extractable metals/elements (CA_1/2, MG_1/2, NA_1/2, K_1/2, TI_1/2, MN_1/2, etc.), C, N, C_N, SI, AL, FE, MG_2, CA_2, NA_2, K_2, P, LOI, P2O5, CEC, SAT.
- Replication indicators: many fields include suffixes 1 and 2, indicating duplicate measurements or alternative samples within a profile.
- Cross-file relationships: PROF_NO ties the D2 (site), D3 (horizons), and D4 (chemical/mineralogy) data; SMPL_NO provides unique sample identifiers within profiles.

## Provenance and accessibility
- Original data collection date: 1965.
- Collected for a PhD study by Mike Hornung; thesis available in supporting documentation and online.
- Long-term storage referenced via Cuthbertson (1993), describing how the data were stored in a database for environmental research.

## Data relationships and discovery
- Data are organized to support integrated soil profiles:
  - Profile-level data (D2) link to horizon data (D3) and chemical/mineralogical data (D4) through PROF_NO.
  - Sample-level details (D4) include SMPL_NO and depth ranges (FDEPTH/TDEPTH) for context within each profile.
- Metadata hints include units for altitude and depths; other fields are described but some units are not always explicit.

## Data quality, gaps, and governance
- Not explicitly stated in the text; potential considerations for data leaders:
  - Age of data (1965) may raise questions about current relevance and comparability.
  - Replicate fields (suffixes 1/2) suggest multiple measurements per profile; need clear documentation of what each replicate represents.
  - Some fields have undefined or missing units; cross-file consistency and metadata completeness may be required.
  - Data standards and naming consistency across fields (e.g., CLAY variants, SILT variants) should be clarified.

## Potential applications and recommendations for Data Leaders
- Historical baseline: use as a reference point for soil properties in Moor House for environmental and ecological studies.
- Integrated data use: leverage the cross-file structure (site, horizons, chemistry) to build comprehensive soil profiles in analyses.
- Data governance actions:
  - Develop a complete data dictionary and metadata to accompany the three files.
  - Align field naming and units; document replication meanings (1 vs 2) and sampling methodology.
  - Implement data quality checks and lineage tracking; ensure discoverability and proper attribution to Hornung and the 1993 database description.
- Accessibility and reuse:
  - Maintain links to provenance sources (Hornung’s thesis, the 1993 database description) to support reproducibility.
  - Consider digitization or modernization efforts to facilitate integration with contemporary data standards and GIS workflows.