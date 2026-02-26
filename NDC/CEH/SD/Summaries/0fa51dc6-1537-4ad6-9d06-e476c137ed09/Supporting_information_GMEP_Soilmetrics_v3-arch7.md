# Glastir Monitoring & Evaluation Programme (GMEP): Soil Metrics 2013-2016

- Objective and scope
  - Welsh Government initiative to monitor Glastir AES schemes and assess soil quality related to climate, biodiversity, soil/water quality, and woodland expansion.
  - Aims to quantify status and trends of soil quality and identify drivers of change (land use, climate, pollution) beyond Glastir interventions.
  - Adopts an ecosystem-based approach with multi-scale data captured in a single visit when possible.

- Survey design and spatial framework
  - 4-year rolling survey cycle (2013–2016) to maximise site coverage and detect spatial and temporal changes cost-effectively.
  - Two components: Wider Wales (baseline estimation and national trends) and Targeted (Glastir priority areas).
  - Common spatial unit: 1 km x 1 km squares; 300 squares sampled over the cycle, with half as Wider Wales and half targeted.
  - Sampling framework aligned with Countryside Survey of Great Britain to enable future data integration.
  - Exclusion criteria: any square >75% urban land or >90% sea excluded.
  - Confidentiality: 10 km resolution mapping to show square distribution.

- Field sampling and locations
  - Within each 1 km square, soil samples collected from 5 randomly dispersed locations when possible.
  - Soil cores: 15 cm long black plastic cores; co-located with vegetation surveys.
  - Samples refrigerated and shipped to CEH ( Bangor and Lancaster ) laboratories within a few days.

- Laboratory protocols and measured soil metrics
  - Soil organic matter and carbon metrics
    - Loss on Ignition (LOI) used to estimate soil organic matter and derive soil carbon concentration (C_TOTAL via LOI × 5.5).
    - LOI: 10 g subsample, dried at 105°C, combusted at 375°C; QA via internal soil standards (2 standards per batch; repeat if LOI deviation > 2 SD).
    - SOC (Total soil carbon) measured after inorganic carbon removal using an Elementar Vario-EL analyser; QA with in-house references.
  - Total nitrogen and phosphorus
    - Total Nitrogen (N_TOTAL) measured with the same instrument; QA with reference materials.
    - Total Phosphorus (P_TOTAL) digested with peroxide and sulfuric acid; colorimetric detection; QA with duplicates and blanks.
  - Olsen phosphorus and pH
    - Olsen-P (POLSEN) measured on arable/improved grassland only; extraction with 0.5 M NaHCO3; colorimetric molybdenum blue; QA with duplicates and blanks.
    - Soil pH (DIW and CaCl2 methods) with internal standards; QA through standard checks.
  - Other soil properties
    - Electrical conductivity (EC) of soil slurry; bulk density (BD) and volumetric water content (VWC) from chemical core; QA with fixed-volume sampling and trained surveyors.
    - Soil water repellency measured by water drop penetration time (WDPT) on air-dried surface; median value from 6 drops; recorded on video for accuracy.
  - Data integration and quality control
    - QA/QC includes two in-house reference materials per batch, duplicate samples, and blanks for select measurements (e.g., P; Olsen P).
    - Derived units (e.g., carbon concentration per kg dry soil) calculated from LOI and QC’d.

- Data structure and metadata
  - Core data file: GMEP_SOIL_METRICS_2013_16.csv
  - Key fields (examples)
    - SQ_ID (1 km square identifier), PLOT_TYPE, PLOTNUM, EASTING_10KM, NORTHING_10KM, LC (Land Classification), YEAR (2013–2016)
    - C_FE_CTOTAL (Total carbon in g/100 g of dry soil), C_FE_LOI (Loss on ignition), C_FE_NTOTAL (Total nitrogen), C_FE_PTOTAL (Total phosphorus)
    - C_FE_POLSEN (Olsen-P, mg/kg, for arable/improved grassland), C_B_PH_DIW (pH in DIW), C_B_PH_CACL2 (pH in CaCl2), C_B_EC (EC in μS/cm)
    - C_FE_BULK_DENSITYGPERCM3 (bulk density), C_FE_VWC (volumetric water content), C_FE_SWRMEDIAN (WDPT; seconds)
  - Spatial coordinates and classification
    - 10 km resolution Easting/Northing for confidentiality; Land Classification (ITE) linked to Bunce et al. 2007
  - Data provenance and references
    - Ties to soil survey methodologies (Avery & Bascomb 1974), Land Classification (Bunce et al. 2007), and Countryside Survey (Emmett et al. 2010/2014)

- GIS and mapping implications
  - Provides a national-scale, 1 km grid of soil properties suitable for map-based visualization and analysis.
  - Enables integration with Countryside Survey datasets for comparative or joint analyses.
  - Derived metrics (e.g., SOC stocks using BD) support estimation of soil carbon stores and climate-related indicators.
  - Spatial confidentiality maintained by disseminating distribution at 10 km resolution.

- Roles, teams, and governance
  - CEH staff and Bangor University lead scientific design, QA, and data management.
  - Field survey teams and laboratory staff conduct sampling, processing, and analysis.
  - Data management and QA are embedded in the workflow to ensure traceability and reproducibility.

- References and further reading
  - Avery, Bascomb (1974); Bunce et al. (2007); Emmett et al. (2010, 2014)
  - PB13297 (2009) on soil carbon significance
  - Glastir Monitoring & Evaluation Programme: First Year Annual Report (2014) and related CEH project reports

- takeaways for GIS specialists
  - A robust, multi-metric soil dataset at 1 km resolution with standardized QA/QC protocols and clear provenance.
  - Suitable for creating GIS-based soil condition maps, trend analyses, and integration with national land classification and other ecosystem datasets.
  - Data governance considerations include confidentiality (10 km data) and alignment with GB Countryside Survey methodologies for future harmonization.