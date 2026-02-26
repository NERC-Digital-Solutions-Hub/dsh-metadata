# Glastir Monitoring & Evaluation Programme

- Purpose and scope
  - Welsh AES monitoring to assess effectiveness of management bundles on soil quality and to quantify soil status and trends.
  - Aims to identify how drivers (land use, climate, pollution) affect soil outcomes beyond Glastir interventions.
  - Integrates multi-metric, ecosystem-focused data across scales, primarily via a standardized 1 km square unit.

- Survey design and sampling
  - 4-year rolling survey (2013–2016) with two components: Wider Wales baseline/national trends and Targeted Glastir priority areas.
  - Sample frame: 300 x 1 km squares over the cycle; half randomly selected (Wider Wales) and half targeted at Glastir priorities.
  - Sampling framework aligned with Countryside Survey GB methodology to enable future data integration.
  - Spatial handling: common 1 km grid; confidentiality maintained by plotting at 10 km.
  - Exclusions: squares with >75% urban land or >90% sea.
  - Data captured to support national and sub-national indicators.

- Field data collection
  - In each 1 km square, collect soil samples from 5 randomly dispersed locations using a 15 cm C-core; co-located vegetation surveys.
  - Samples refrigerated and shipped to CEH laboratories (Bangor and Lancaster) within a few days.

- Laboratory methods and analytes
  - Soil organic matter and carbon
    - Loss on Ignition (LOI) measured on 10 g sub-sample; LOI (%) converted to soil carbon concentration (C_FE_CARBO_CONC_GPERKG = LOI × 5.5).
    - Total soil carbon (SOC, C_FE_CTOTAL) measured after inorganic carbon removal using a CEH/UKAS-accredited SOP3102 method with a Vario EL analyzer.
    - Quality control with in-house reference materials; repeat runs if LOI variance exceeds 2 SD.
  - Total nitrogen and phosphorus
    - Total nitrogen (C_FE_NTOTAL) and total phosphorus (C_FE_PTOTAL) quantified; P measured via digestion and colorimetric methods.
    - Olsen phosphorus (C_FE_POLSEN) measured on arable/improved grassland habitats; data corrected for moisture and blanks.
    - Quality control includes duplicates and matrix-matched blanks every 25 samples.
  - Soil pH and electrical conductivity
    - pH in deionized water (C_B_PH_DIW) and CaCl2 (C_B_PH_CACL2) with internal standard QC.
    - Electrical conductivity (C_B_EC) measured on soil suspension; QC via internal standards.
  - Physical soil properties
    - Bulk density of fine earth (C_FE_BULK_DENSITYGPERCM3) from the chemical core; used to convert % C to carbon stocks.
    - Volumetric water content (C_FE_VWC) derived from bulk density and gravimetric water content.
    - Water repellency (C_FE_SWRMEDIAN) measured as Water Drop Penetration Time with video timing for accuracy.
  - Data structure
    - All metrics recorded in GMEP_SOIL_METRICS_2013_16.csv, with fields for SQ_ID, PLOT_TYPE, PLOTNUM, coordinates, year, LC (Land Classification), and all measured/derived variables.
    - Derived units and data dictionary included (e.g., LOI→C conversions, units, and descriptions).

- Quality assurance and quality control (QA/QC)
  - Internal soil standards run with each batch; anomalies trigger repeats if variance from historical values exceeds 2 SD.
  - Duplicate samples and blanks used for P-total, Olsen P, and other analyses; calibration and blank corrections applied.
  - Strict QC protocols throughout digestion, analysis, and data handling to ensure data reliability.

- Data product and data dictionary
  - Primary dataset: GMEP_SOIL_METRICS_2013_16.csv containing:
    - Spatial and sampling identifiers (SQ_ID, PLOT_TYPE, PLOTNUM)
    - Spatial coordinates at 10 km resolution and Land Classification (LC)
    - Year (2013–2016)
    - Measured soil metrics: C_FE_CTOTAL, C_FE_LOI, C_FE_NTOTAL, C_FE_PTOTAL, C_FE_POLSEN, C_B_PH_DIW, C_B_PH_CACL2, C_B_EC, C_FE_BULK_DENSITYGPERCM3, C_FE_VWC, C_FE_SWRMEDIAN, plus derived C_FE_CARBO_CONC_GPERKG
  - Derived units and QA/QC scripts are available (R scripts for deriving units and performing QA/QC).

- References and methodology context
  - Key methodological references include: Avery & Bascomb (1974), Bunce et al. (2007), Emmett et al. (2010, 2014), and Defra soil strategy documents.
  - Linking framework to Countryside Survey GB for future data integration and national reporting.

- Data management, roles, and teams
  - CEH staff lead QA, soil preparation, lab analysis, and data QA/QC; roles span lab management, sample processing, and data management.
  - Bangor University and field survey teams contribute sampling, field coordination, and data collection.
  - Field teams and project coordination ensure consistent sample collection, handling, and shipment to laboratories.

- Practical implications for data use
  - Enables assessment of Glastir interventions on soil quality and carbon dynamics over time.
  - Provides multi-parameter soil health indicators for climate, biodiversity, and water quality outcomes.
  - Facilitates cross-year trend analysis, regional comparisons, and integration with GB-wide soil datasets for broader policy and environmental insights.