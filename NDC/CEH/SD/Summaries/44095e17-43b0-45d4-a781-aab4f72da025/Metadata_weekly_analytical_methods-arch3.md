# LOCATION OF ANALYTICAL DATA PRE-CONCENTRATION PRIOR TO ANALYSIS TO IMPROVE

- Overview
  - A comprehensive data dictionary for water-quality analyses across multiple sites, detailing pre-concentration, analytical methods, QC, and metadata for a wide range of chemical species in river and related samples.
  - Aimed at supporting environmental health monitoring, policy scrutiny, and informed decision-making by documenting data provenance, measurement techniques, and data quality considerations.

- Key data elements and structure
  - Analytes and determinations
    - Large suite including metals (Al, Sb, As, Ba, Be, Cd, Cs, Cr, Co, Cu, Fe, Pb, Ni, Mo, Zn, U, V, W, Mn, Se, Sn, Ti, Li, Li, etc.), metalloids, nutrients (nitrate NO3-N, nitrite NO2-N, ammonium NH4-N, orthophosphate PO4), ions (Cl, Br, F, SO4, NO3), and organic/inorganic carbon species (DOC, DON, Total dissolved nitrogen), pH, conductivity, and other hydrological indicators.
    - Each analyte entry includes: DETERMINAND, UNITS, LQDC (low quantification/detection), QUOTE TO, START/END dates, LOCATION OF ANALYSIS, ANALYTICAL METHOD QC QUALIFIER, FILTRATION, PRESERVATION, METHOD, and DETECTION LIMIT NOTES.
  - Metadata and QC
    - Data quality codes (LQDC) and data qualifier codes (e.g., 10–17 for raw data, detection limits, data anomalies, etc.), plus references to ISO 17025 accreditation status where applicable.
    - Information on instrument types and QA/QC practices (ICP-OES, ICP-MS, IC, Autoanalyzers, etc.), and comments on data provenance and averaging when multiple methods exist.
  - Sampling and time structure
    - Sampling types: grab samples (stream/borehole) and time-integrated inputs (rainfall, throughfall, cloud water, etc.).
    - Time-stamping conventions: exact sample collection times; volume-weighted sampling times computed from rainfall and runoff data; year-mean sampling derived from volume-weighted timing.
    - Site-level hydrology: catchment areas (km²) used for conversions between streamflow (cumecs) and area-weighted runoff (mm/15 min).
  - Site and catchment information
    - Site names and codes (e.g., Lower Hore A, Tanllwyth K, Upper Hafren G, etc.) with corresponding catchment areas for hydrological calculations.
  - Data governance and usage
    - Notes on averaging across multiple methods when present; emphasis on maintaining provenance and clear interpretation through QC codes and method descriptors.
    - Data can support policy evaluation through long-term time series of concentrations and fluxes, and through derived hydrological metrics (area-weighted runoff, rainfall-derived loads).

- Hydrology and data conversion
  - Flow to runoff conversion
    - Formulas to convert cumecs to mm/15 min: mm/15min = cumecs × 0.9 / catchment area (km²).
    - Conversion back to cumecs: cumecs = mm/15min × catchment area / 0.9.
  - Sampling timing and flux estimation
    - Time stamps indicate sample collection; input samples are interval-based; rivers are grab samples at the collection time.
    - Volume-weighted sampling times and year means are computed to better align precipitation and runoff for flux analyses.

- Relevance for policy monitoring
  - Provides a richly documented, QA-controlled set of water-quality indicators across multiple catchments, enabling assessment of policy effects on pollutant concentrations and nutrient fluxes.
  - Facilitates flux/ load estimation through area-weighted runoff and rainfall-derived inputs, aiding interpretation of anthropogenic impacts and remediation effectiveness.
  - Supports trend analysis with detailed metadata, including QC qualifiers and method changes, essential for robust policy evaluation.

- Challenges and considerations for governance
  - Complexity and longevity of the dataset require rigorous metadata upkeep, consistent QC applications, and transparent data-sharing practices.
  - Method changes and detections limits necessitate careful handling of data qualifiers (e.g., raw vs. processed, below-detection data, time-of-sampling issues).
  - Inter-organ data sharing barriers and the need for standardized SOPs and QA processes to enable integrated policy analysis across agencies.