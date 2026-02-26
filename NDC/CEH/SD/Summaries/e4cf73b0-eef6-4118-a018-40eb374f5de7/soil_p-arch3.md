# Soil survey of Moor House, 1965.

- What the dataset is
  - Soil survey data from Moor House, Cumbria, UK, collected in 1965 by Mike Hornung as part of his PhD.
  - Hornung’s PhD thesis is available in supporting documentation and online; the data were stored in a database described by Cuthbertson (1993).

- Data structure and how datasets relate
  - D2SOIL_P.csv (Site locations)
    - PROF_NO: unique profile number (primary key).
    - EASTING, NORTHING: spatial coordinates.
    - LOCATION, REL_DATA, ALTITUDE (m), GEO_DATA, VEG_DATA: descriptive metadata and references to other data.
  - D3SOIL_P.csv (Horizon analysis)
    - PROF_NO: links to D2SOIL_P.
    - HORIZON: horizon code (as defined in the thesis).
    - FDEPTH, TDEPTH (cm): depth range of horizon.
    - REM1, REM2: remarks.
    - TYPE: ORGANIC or MINERAL.
  - D4SOIL_P.csv (Chemical analysis and soil mineralogy)
    - PROF_NO: links to D2SOIL_P; SMPL_NO: sample number (with PROF_NO forming a unique code).
    - FDEPTH, TDEPTH (cm): sample depth range.
    - A wide panel of chemical and mineralogical measurements (e.g., PH, CACO3, FE203, US_SAND, I_SAND, I_SILT, CLAY, LOI, P2O5, C, N, C_N, SI, AL, FE, MG, CA, NA, K, TI, MN, H2O, P, CEC, SAT).
    - Many fields include paired suffixes (1 and 2), indicating two measurement sets for the same sample.

- Metadata and data governance implications
  - Clear field definitions and units are provided for key variables, aiding interpretation and cross-study comparability.
  - PROF_NO serves as the core linking key across datasets; SMPL_NO provides a secondary unique code within a profile.
  - The data are described within a published PhD thesis and a 1993 journal reference, suggesting provenance and a defined database structure, but potential limitations for modern open-data sharing depending on access to the original sources.

- Content scope and potential monitoring uses
  - Captures spatial context (location, altitude), horizon stratigraphy (horizon codes, depths), and detailed soil chemical properties (pH, carbonates, nutritional elements, texture indicators, mineralogy, and cation exchange capacity).
  - Enables assessment of soil health indicators, nutrient status, pH shifts, texture and mineralogical properties, and their depth profiles.
  - The two-measurement-set design (suffix 1/2) supports assessment of measurement variability or replication.

- Practical considerations for monitoring framework authors
  - Data legacy: 1965 data require careful interpretation with thesis-based horizon coding and potential metadata gaps typical of older datasets.
  - Metadata completeness: explicit field definitions and units are present, but users should verify any dataset-transform requirements when integrating with modern data systems.
  - Data coupling: strong linkages between site-level data, horizon data, and chemistry/mineralogy data enable multi-layer environmental health monitoring, provided provenance is maintained.
  - Access and sharing: referenced theses and historical database description imply data are accessible through those sources; openness may depend on repository policies and digitization status.