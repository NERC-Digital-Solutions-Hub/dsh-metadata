# Details of data structure to CINAg_digestate_experiment_2017_Soil_physicochemical_properties.csv

- Purpose and context
  - Supplemental document for data series described in Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf
  - Describes the data structure for the CINAg_digestate_experiment_2017_Soil_physicochemical_properties.csv dataset
  - Dataset pertains to the 2017 digestate trial and captures soil physicochemical properties

- Dataset scope and structure
  - Contains 35 columns and 180 rows
  - Dataset theme: soil physicochemical properties collected during the 2017 digestate experiment
  - Primary experiment identifier: Organic_fertilizer (treatment context)
  - Sampling design
    - Sites: Farm platforms NW (North Wyke) and HF (Henfaes Farm)
    - Treatments: C (Control), D (digestate), ADNI (acidified digestate with nitrification inhibitor DMPP)
    - Depths: 0-15 cm, 15-30 cm, 30-60 cm
    - Sampling times: T1 (initial after digestate application), T2 (last harvest)
    - Plot numbers and sampling dates (dd/mm/yyyy)
  - Data collected across multiple related domains (representative columns)
    - Soil chemistry and nutrients: NH4, NO3, PO4.P, Olsen_P, totC, totN, CN_ratio, totP, pH (deionised water and CaCl2), EC
    - Soil organic matter and carbon/nitrogen pools: LOI, DOC, DON, Aminoacids, Peptides_and_proteins, MBC, MBN
    - Soil texture and structure: Sand_perc, Silt_perc, Clay_perc, Aggr_b20µm_perc, Aggr_b250µm_perc, Aggr_b2000µm_perc
    - Other soil properties: Soil_moisture_perc, POXC_mgC_per_kg_soil
  - Selected example column headers (representative)
    - Sample_ID, Year, Site, platform, Sampling_date, Sampling_time, Plot, Treatment, Depth_cm
    - NH4_mgN_per_kg_soil, NO3_mgN_per_kg_soil, DOC_mgC_per_kg_soil, DON_mgN_per_kg_soil
    - Aminoacids_mgN_per_kg_soil, Peptides_and_proteins_mgN_per_kg_soil, MBC_mgC_per_kg_soil, MBN_mgN_per_kg_soil
    - Aggr_b20µm_perc, Aggr_b250µm_perc, Aggr_b2000µm_perc, Sand_perc, Silt_perc, Clay_perc
    - pH_deionised_water, pH_CaCl2, EC_µS_per_cm, POXC_mgC_per_kg_soil
    - PO4.P_mgP_per_kg_soil, totC_perc, totN_perc, CN_ratio, totP_mgP_per_kg, Olsen_P_mgP_per_kg_soil

- Metadata, data quality, and governance implications
  - Explicit focus on data provenance and structure to enable scoping for monitoring and policy evaluation
  - Metadata considerations implied by the structure (units specified for many columns; documented temporal and depth dimensions)
  - Data quality workflow implied: data quality assurance, cleaning, transformation, analysis, and clear presentation in reports, charts, or dashboards
  - Data sharing and openness considerations: underlying data should be shared where appropriate; metadata completeness and accessibility can be barriers
  - Potential data governance needs: ensuring consistent units,Temporal and spatial alignment, documentation of treatments and sampling protocols, and maintaining up-to-date metadata to facilitate reuse

- Relevance for monitoring frameworks
  - Provides comprehensive, depth-resolved soil health indicators under different fertilizer treatments
  - Enables assessment of how digestate application and nitrification-inhibitor use influence soil chemistry, organic matter, microbial biomass, carbon/nitrogen cycles, and soil physical properties
  - Supports evaluation of policy-relevant questions on soil quality, nutrient management, and sustainable agricultural practices through structured, machine-readable data
  - The multi-domain dataset (chemical, biological, physical, and structural soil properties) supports integrated environmental health assessments and monitoring outputs (e.g., dashboards, trend analyses)

- Practical considerations for use
  - Ensure alignment of units and depth/timing when integrating with other data series
  - Leverage the T1 vs T2 sampling framework to analyze temporal changes following digestate application
  - Be mindful of potential data gaps or metadata gaps that could affect comparability across sites or years
  - Address data access considerations and governance to enable appropriate public sharing and provenance tracking