# Soil survey of Moor House, 1965.

- What the dataset is
  - Soil survey data from Moor House, Cumbria, UK, conducted by Mike Hornung as part of his PhD.
  - PhD thesis available in supporting documentation and online; dataset described in 1993 publication.
  - Data stored in a database described by Cuthbertson (1993) for environmental research programmes.

- Datasets and file structure
  - D2SOIL_P.csv (Site Locations)
    - PROF_NO (unique profile number)
    - EASTING, NORTHING, LOCATION, REL_DATA, ALTITUDE (m), GEO_DATA, VEG_DATA
  - D3SOIL_P.csv (Horizon analysis)
    - PROF_NO (relates to D2SOIL_P)
    - HORIZON, FDEPTH (cm), TDEPTH (cm), REM1, REM2, TYPE (ORGANIC or MINERAL)
  - D4SOIL_P.csv (Chemical analysis and soil mineralogy)
    - PROF_NO, SMPL_NO (sample number; forms unique code with PROF_NO)
    - FDEPTH, TDEPTH, PH, CACO3, FE203, US_SAND, I_SAND, I_SILT, CLAY (1/2), US_SILT (1/2), BS (1/2), and a wide range of element concentrations and soil properties (e.g., CA_1/2, MG_1/2, NA_1/2, K_1/2, LOI_1/2, P2O5_1/2, C, N, C_N, SI_1/2, AL_1/2, FE_1/2, MG_2, CA_2, NA_2, K_2, TI, MN, H2O_1/2, P_1/2, CEC, SAT)
  - Note: PROF_NO links across D2, D3, and D4; SMPL_NO augments D4 data; some fields have dual variants (1/2) representing different measurement schemes.

- Provenance and documentation
  - The dataset stems from a historical soil survey and accompanying PhD work.
  - Supporting documentation includes Hornung’s thesis and the 1993 J. Env. Management publication describing the database structure.

- Data governance and discoverability
  - Core identifiers: PROF_NO (unique profile) with cross-table relationships to enable dataset discovery and integration.
  - Metadata includes units (e.g., ALTITUDE in metres, FDEPTH/TDEPTH in cm, pH, various percentages and mg/g values) and descriptive field meanings.
  - Documentation exists to support data understanding (thesis, database description); potential for inclusion in data portals and catalogues.

- Quality, interoperability, and maintenance considerations
  - Legacy data with multiple linked files and legacy database schema; feasibility of integrating into modern interoperable standards (e.g., standardized soil data vocabularies) should be assessed.
  - Requires careful mapping of fields across D2, D3, and D4 to maintain relational integrity (PROF_NO as the primary linkage).
  - Data normalization and reconciliation of dual-field variants (e.g., 1/2 suffix fields) may be needed for interoperability.

- Challenges relevant to Data Stewards
  - Legacy formats and older database structures may hinder interoperability with contemporary systems.
  - Ensuring timely access and complete metadata for users seeking to reuse site, horizon, and chemical data.
  - Aligning metadata with user needs and potential publishing workflows.

- Recommendations for data stewardship
  - Preserve and document the cross-table relationships (PROF_NO) and the linkage between site, horizons, and chemical data.
  - Create a formal data dictionary and data dictionary extension that clearly maps each field, unit, and variant (1/2) to a standard vocabulary.
  - Consider assigning persistent identifiers and linking to the original thesis and 1993 database description for provenance.
  - Upload to a data portal with accompanying metadata, access instructions, and licensing terms; include references to supporting documentation.
  - Where possible, produce a harmonized version with standardized units and nomenclature to improve interoperability with other soil datasets.

- Potential uses and value
  - Site characterization and soil property analyses by depth and horizon.
  - Comparative studies with other soil surveys and historical environmental datasets.
  - Support for re-use in environmental management, land use planning, and soil science research.