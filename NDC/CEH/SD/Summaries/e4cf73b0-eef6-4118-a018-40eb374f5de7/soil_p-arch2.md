# Soil survey of Moor House, 1965.

## Overview
- Dataset from a soil survey at Moor House, Cumbria, UK, conducted by Mike Hornung as part of his PhD.
- Supporting documentation includes the PhD thesis and a 1993 Journal of Environmental Management paper describing the data database.
- Data were stored in a database described by Cuthbertson (1993).

## Data collection and provenance
- Field data collected as part of a structured soil survey; links between data tables allow integration across horizons and analyses.
- Related documentation and thesis provide definitions, horizon codes, and methodologies referenced by the dataset.

## Data structure and content
- Site Locations (D2SOIL_P.csv)
  - PROF_NO (profile number, unique)
  - EASTING, NORTHING (coordinates)
  - LOCATION, REL_DATA, ALTITUDE
  - GEO_DATA, VEG_DATA (references to geological and vegetation data)
- Horizon analysis (D3SOIL_P.csv)
  - PROF_NO (linked to D2SOIL_P)
  - HORIZON (horizon code as defined in the thesis)
  - FDEPTH, TDEPTH (depth range in cm)
  - REM1, REM2 (remarks)
  - TYPE (ORGANIC or MINERAL)
- Chemical analysis and soil mineralogy (D4SOIL_P.csv)
  - PROF_NO, SMPL_NO (sample identifiers; composite key)
  - FDEPTH, TDEPTH
  - pH, CACO3, FE203, US_SAND, I_SAND, I_SILT, CLAY, US_SILT, BS, CEC, SAT, and many other chemical and physical properties (e.g., Ca, Mg, Na, K, Ti, Mn, P2O5, C, N, C_N, LOI, H2O)
  - Multiple columns with paired values (1 and 2) representing duplicate or alternative measurements for several parameters

## Data quality and management
- Data are described as being verified, quality assured, cleaned, and transformed as part of standard environmental data practices.
- Datasets are stored and intended to be uploaded to appropriate data portals, aligning with standardised data management.

## Reuse and accessibility
- Original sources provide raw data and supporting methodological context (thesis and Cuthbertson 1993 database description).
- The dataset is structured to support cross-reference between location, horizon, and chemical analyses, facilitating broader data integration and reuse beyond a single study.

## Relevance to environmental monitoring
- Provides comprehensive soil health indicators (pH, carbon content, base saturation, cation exchange capacity, texture fractions, nutrient profiles) across soil horizons.
- Enables assessment of soil conditions, mineralogy, fertility status, and potential environmental change over time when integrated with other datasets.

## Potential value and challenges for analysts
- Value: Standardised data structure supports consistent reporting on soil health and policy-relevant environmental performance; easy to combine with other datasets for broader environmental monitoring.
- Challenges: The dataset originates from 1965; standardization harmonization may be needed for modern analytics; ensuring ongoing access to underlying data and accompanying metadata for reproducibility.