# Glastir Monitoring and Evaluation Programme: Soil Monitoring

- Purpose
  - Welsh Government monitoring to assess the effectiveness of Glastir AES interventions on the environment, focusing on climate change, biodiversity, soil and water quality, and woodland expansion.
  - Collect evidence on soil status and trends to understand drivers of change beyond Glastir measures and to support national reporting and policy decisions.

- Scope and Approach
  - Ecosystem-based, multi-scale data collection with an emphasis on integration across metrics.
  - 4-year rolling survey to maximize site coverage while enabling year-on-year monitoring of spatial and temporal change.
  - Two main components:
    - Wider Wales Component: baseline estimation and national trend reporting.
    - Targeted Component: links to Glastir priority areas.
  - Common spatial unit of 1 km square to enable data integration, including with Countryside Survey of Great Britain.
  - Confidentiality: 1 km squares are plotted at 10 km resolution on maps.

- Sampling Design
  - Total of 300 x 1 km survey squares over the four-year cycle.
  - Sampling frame constructed to balance environmental heterogeneity:
    - Half squares randomly sampled within strata defined by the Land Classification of Great Britain.
    - Other half targeted at Glastir priority areas.
  - Exclusions: squares with >75% urban land or >90% sea.

- Field Sampling and Data Collection
  - Within each square, soils are sampled from 5 randomly dispersed locations.
  - Soil cores: 15 cm long, 2 cm diameter, collected to coincide with vegetation surveys.
  - Samples refrigerated and shipped within days to CEH laboratories (Bangor/Lancaster) for analysis.

- Laboratory Protocols and Measured Metrics
  - Soil Organic Matter and Carbon
    - Loss on Ignition (LOI) to estimate organic matter and carbon concentration (C_FE_LOI) using a 10 g subsample, dried and combusted; carbon concentration derived as C_FE_LOI × 5.5.
    - Oxygen removal of inorganic carbon prior to SOC measurement; SOC determined with Elementar Vario-EL C/N analyzer.
    - Quality control: two internal standards per batch; repeat if LOI varies >2 SD from historic mean.
  - Total Soil Carbon and Nitrogen (SOC and TN)
    - Post-digestion analysis (inorganic carbon removed) using CEH SOP; results reported as C_TOTAL and N_TOTAL.
    - Quality control with in-house reference materials.
  - Phosphorus
    - Total Phosphorus (P_TOTAL) via acid digestion and colorimetric molybdenum blue method; QC with duplicates and blanks every 25 samples.
    - Olsen Phosphorus (POLSEN) measured in arable/improved grassland habitats using Olsen reagent and flow analysis; QC similar to P_TOTAL.
  - Soil pH
    - pH in deionized water (DIW) and pH in CaCl2, following standard soil survey methods; QC with internal standards.
  - Electrical Conductivity (EC)
    - Soil slurry EC measured after suspending 10 g soil in 25 mL DIW; QC with internal standards.
  - Bulk Density and Volumetric Water Content
    - Dry bulk density derived from a 15 cm chemical core; volumetric water content calculated from bulk density and gravimetric water content; QC and standardized sampling sleeves and training.
  - Soil Water Repellency
    - Water Drop Penetration Time (WDPT) measured on air-dried soil surface; six drops per sample; timing captured on video for accuracy; median value used; QC via standardized handling.

- Data Management and Output
  - Primary dataset: GMEP_SOIL_METRICS_2013_16.csv
    - Key fields include square ID, plot type, plot number, 10 km easting/northing, Land Classification, year (2013–2016), and multiple soil metrics (C_TOTAL, LOI, TN, P_TOTAL, POLSEN, pH_DIW, pH_CACL2, EC, Bulk Density, VWC, SWR).
    - Derived quantities:
      - C_FE_CTOTAL, C_FE_LOI, C_FE_NTOTAL, C_FE_PTOTAL, C_FE_POLSEN
      - C_B_PH_DIW, C_B_PH_CACL2
      - C_B_EC
      - C_FE_BULK_DENSITY_GPERCM3
      - C_FE_VWC
      - C_FE_SWRMEDIAN
  - Data are designed to be compatible with legacy Countryside Survey data to facilitate future integration.
  - Confidential mapping: 1 km squares are represented at 10 km resolution to protect sensitive location data.

- Quality Assurance and Quality Control
  - Use of internal standards in each batch; repeat analyses if QC criteria are not met.
  - Duplicates and blanks included for P analyses; moisture and calibration controls applied for all measurements.
  - Ongoing QA/QC oversight by CEH staff with defined roles for laboratory and data management.

- Roles and Collaboration
  - CEH-led with collaboration across laboratories (Lancaster, Bangor) and Bangor University.
  - Field survey teams and management support a broad network to execute sampling and data handling.
  - Data management and QA overseen by dedicated CEH personnel.

- Context and References
  - Grounded in a broader policy context, including Defra soil strategies and prior Countryside Survey methodologies.
  - Key references include Avery & Bascomb (1974), Bunce et al. (2007), Emmett et al. (2010, 2014), and Glastir Monitoring & Evaluation Programme annual reporting.