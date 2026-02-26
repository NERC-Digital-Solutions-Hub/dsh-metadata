# Countryside Survey: Soils 2019 – UKCEH Soil Metrics and Rolling Monitoring Program

- Purpose and scope
  - National-scale, rolling soil monitoring to detect direction and magnitude of soil change across the UK and understand interactions of multiple pressures on soil condition and function.
  - Focus on key soil properties and co-located vegetation to inform policy, land management, and climate-related insights.
  - Rolling programme aims to address changes in soil condition over time, enabling comparisons with past surveys since 1978.

- Monitoring design and rolling program
  - Adopts a rolling survey with a five-year cycle or 500 squares total; 100 squares visited annually to balance spatial coverage and temporal monitoring.
  - Sample selection builds on the Countryside Survey framework, using stratification by the Land Classification of Great Britain (ITE 2007) to ensure national and sub-national representativeness.
  - Exclusion criteria: any square with >75% urban land or >90% sea excluded.
  - Objective: detect spatial variation and temporal trends while buffering against climate year-to-year fluctuations.

- Sampling design and field implementation
  - Within each year, 100 x 1km squares are sampled; in each square, five predetermined, randomly dispersed soil sampling locations are used alongside vegetation X-plots.
  - Soil cores are taken to a depth of approximately 0-15 cm using a 15 cm long C-core.
  - History of sampling locations refined over time (1978, 1990, 1998, 2007, and 2019) to ensure accurate relocation.
  - Cores are refrigerated and sent to laboratories for analysis; vegetation data accompany soil sampling.

- Metrics, laboratory protocols, and analytical methods
  - Field/lab methods are aligned with long-standing soil survey protocols (ITE Land Classification; CS methods).
  - Key soil metrics include:
    - Soil carbon groups based on Loss on Ignition (LOI) and depth of organic layers; classification into mineral, humus mineral, organo-mineral, and organic soils.
    - Depth of organic horizons (peaty layers) to determine peat classification.
    - Soil pH in deionised water (DIW) and in 0.01M CaCl2.
    - Electrical conductivity (EC) of soil slurry.
    - Hygroscopic water content, LOI, and CaCO3 via thermogravimetric analysis (TGA).
    - Soil carbon concentration derived from LOI with conversions to align with legacy CS data (0.55 factor).
    - Bulk density, porosity, and fine earth moisture metrics, including gravimetric and volumetric water content.
    - Olsen-Phosphorus (P Olsen) and Total Phosphorus (TP) via colorimetric methods after extraction/digestion.
    - Total soil organic carbon (SOC) and total nitrogen (TN) using standard elemental analysis after removing inorganic carbon.
  - Quality control is embedded at multiple steps:
    - Internal standards and duplicate samples in each batch for pH, LOI, CaCO3, and other analyses.
    - Calibration checks, blanks, and reference materials (two in-house references per batch; Performed checks with Acetanilide standard).
    - Specific QA criteria (e.g., ±2 standard deviations for internal standards, 95-100% CaCO3 recovery).

- Data structure and accessibility
  - Primary data file: UKCEHCS_SOIL_METRICS_2019.csv with fields including SQ_ID, PLOT_ID, YEAR, land classification, habitat descriptors, depth of peaty horizons, LOI groupings, pH measurements, EC, moisture metrics, LOI, CaCO3, C concentrations, SOC, TN, CN ratio, Olsen-P, TP, and related derived metrics.
  - Data are designed to be integrated with vegetation metrics and other Countryside Survey outputs for ecosystem-level interpretation.
  - Data management responsibilities include rolling program design, sample archiving, data analysis, and public sharing of underlying data where appropriate, aligned with data governance.

- Annual analysis and outputs
  - The program contributes to an ongoing rolling analysis of soil change since 1978, with annual outputs that identify changes in soil organic matter (LOI) and soil pH (in water).
  - Outputs include summary figures and relationships (e.g., LOI vs. porosity, bulk density vs. LOI, pH vs. LOI, EC vs. LOI, calcite vs. LOI, LOI vs water content, LOI vs porosity).
  - The dataset supports national and sub-national interpretation of soil status, carbon stocks, soil carbon density, and changes over time in relation to vegetation and land-use shifts.

- Context within policy and monitoring framework
  - The Countryside Survey forms a science platform under UK-SCAPE to address soil status and dynamics at national scale, informing soil health, carbon policy, land management, and environmental health monitoring.
  - Designed to address research questions on interactions of pressures, carbon pools, soil acidity, compaction, phosphorus availability, and feedbacks between vegetation and soil conditions.

- Challenges and data governance implications for authors
  - Data gaps and access barriers are acknowledged in general monitoring contexts (data availability, metadata quality, timely access, and data sharing constraints).
  - Complexity of communicating multi-metric soil information to stakeholders and policymakers is recognized; clear interpretation and visualization are essential.
  - Robust metadata, standardised data formats, and governance processes are critical to ensure data quality, comparability with legacy CS data, and openness.

- References and provenance
  - Methodological foundations draw on long-running CS reports and technical manuals (e.g., Emmett et al.; Reynolds et al.; Bunce et al.; Scott, 2008; UKCEH-CS vegetation datasets).
  - Documentation includes detailed QA procedures and links to field manuals and land classification schemes to support reproducibility and policy relevance.