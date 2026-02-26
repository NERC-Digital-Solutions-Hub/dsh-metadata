# Soil survey of Moor House, 1965.

- Overview
  - Dataset from a soil survey at Moor House, Cumbria, UK conducted in 1965 by Mike Hornung as part of his PhD.
  - Thesis is available in supporting documentation and online at the Durham e-theses repository.
  - Data were stored in a database described by Cuthbertson (1993): A database for environmental research programmes.

- Datasets and structure
  - Site Locations - D2SOIL_P.csv
    - PROF_NO: unique profile number.
    - EASTING, NORTHING: coordinates.
    - LOCATION: location description.
    - REL_DATA: description of related data.
    - ALTITUDE: in metres.
    - GEO_DATA, VEG_DATA: references to geological and vegetation data.
  - Horizon analysis - D3SOIL_P.csv
    - PROF_NO: links to D2SOIL_P.
    - HORIZON: horizon code (defined in thesis pages 474-475 vol 2).
    - FDEPTH, TDEPTH: start and end depths of horizons (cm).
    - REM1, REM2: remarks.
    - TYPE: indicates if horizon is ORGANIC or MINERAL.
  - Chemical analysis and soil mineralogy - D4SOIL_P.csv
    - PROF_NO, SMPL_NO: profile and sample numbers; combined to form a unique code.
    - FDEPTH, TDEPTH: sample depth range (cm).
    - PH, CACO3, FE203, US_SAND, I_SAND, I_SILT, CLAY, US_SILT, BS, CA_1, MG_1, NA_1, K_1, LOI, P2O5, C, N, C_N, SI, AL, FE, MG_2, CA_2, NA_2, K_2, TI, MN, H2O, P, CEC, SAT: various soil chemical and mineralogical properties.
    - Notes: some properties have dual entries (1 and 2) indicating two samples or measurements per profile.
  - Data relationships
    - D2SOIL_P provides location context and links to D3SOIL_P via PROF_NO.
    - D3SOIL_P provides horizon information for each PROF_NO.
    - D4SOIL_P provides chemical/mineral data linked to PROF_NO and SMPL_NO; unique code is PROF_NO + SMPL_NO.

- Data specifics and units
  - ALTITUDE is in metres.
  - FDEPTH and TDEPTH in centimetres.
  - Chemical/metabolic properties include pH, carbonate content, various sand/silt/clay fractions, base saturation, extractable elements, carbon/nitrogen metrics, CEC, and saturation (SAT).
  - Some fields are presented in dual forms (suffixes 1 and 2) to reflect two measurements per profile.

- Provenance and references
  - Original work: Moor House soil survey (1965) by Mike Hornung.
  - Supporting documentation and the related database are described in Cuthbertson (1993).
  - Thesis reference for horizon coding and related methodology: pages 474–475 vol 2 of the Hornung thesis.
  - Online thesis access: http://etheses.dur.ac.uk/9262/1/9262_6193-vo1.PDF

- How the data can be used
  - Integrate across datasets by PROF_NO to analyze soil profiles, horizons, and chemical properties.
  - Use SMPL_NO to disaggregate within a profile for sample-level chemistry.
  - Create soil property tables, horizon-based summaries, or map-derived insights (e.g., depth ranges, mineralogy).
  - Develop data products (dashboards, pivot tables, reports) to enable self-serve exploration of soil characteristics and relationships.

- Potential considerations for users
  - The data date from 1965; appropriate for historical analysis or baseline comparisons but may require careful interpretation for contemporary contexts.
  - Data are spread across multiple CSVs with explicit links; ensure correct joins on PROF_NO and SMPL_NO.
  - Some fields have dual entries (1 vs 2) that should be handled as paired measurements.