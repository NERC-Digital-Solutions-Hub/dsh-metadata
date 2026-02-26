# Details of data structure to CINAg_digestate_experiment_2017_Soil_physicochemical_properties.csv

- Overview
  - Supplement to CINAg supporting documentation describing the CINAg_digestate_experiment_2017_Soil_physicochemical_properties.csv dataset.
  - Digestate trial conducted in 2017; dataset comprises 35 columns and 180 rows of soil physicochemical properties.
  - Captures sampling across two farm platforms (NW and HF), multiple plots, depths, times, and fertilizer treatments.

- Dataset structure and primary fields
  - Sample_ID: unique sample identifier constructed from Year, Experiment, Site, Sampling_time, Treatment, Plot, and Depths.
  - Year: year of sampling.
  - Site: farm platform (NW = North Wyke, HF = Henfaes Farm).
  - Sampling_date: date of sampling (dd/mm/yyyy).
  - Sampling_time: T1 (initial after digestate application) or T2 (last harvest).
  - Plot: plot numbers.
  - Treatment: C = Control, D = digestate, ADNI = acidified digestate with nitrification inhibitor DMPP.
  - Depth_cm: sampling depth (0-15 cm, 15-30 cm, 30-60 cm).
  - 35 soil properties (examples below) with units:
    - NH4_mgN_per_kg_soil (mg NH4-N kg-1 dry soil)
    - NO3_mgN_per_kg_soil (mg NO3-N kg-1 dry soil)
    - DOC_mgC_per_kg_soil (mg C kg-1 dry soil)
    - DON_mgN_per_kg_soil (mg N kg-1 dry soil)
    - Aminoacids_mgN_per_kg_soil (mg N kg-1 dry soil)
    - Peptides_and_proteins_mgN_per_kg_soil (mg N kg-1 dry soil)
    - MBC_mgC_per_kg_soil (mg C kg-1 dry soil)
    - MBN_mgN_per_kg_soil (mg N kg-1 dry soil)
    - Aggr_b20µm_perc (percentage of aggregates <20 µm)
    - Aggr_b250µm_perc (percentage of aggregates <250 µm)
    - Aggr_b2000µm_perc (percentage of aggregates <2000 µm)
    - Sand_perc, Silt_perc, Clay_perc (soil texture components, %)
    - Soil_moisture_perc (%)
    - LOI_perc (loss-on-ignition, soil organic matter, %)
    - pH_deionised_water (pH in deionised water)
    - pH_CaCl2 (pH in CaCl2)
    - EC_µS_per_cm (electrical conductivity)
    - POXC_mgC_per_kg_soil (permanganate oxidisable carbon)
    - PO4.P_mgP_per_kg_soil (citric acid extractable P)
    - totC_perc (total soil carbon, %)
    - totN_perc (total soil nitrogen, %)
    - CN_ratio (C-to-N ratio)
    - totP_mgP_per_kg (total soil phosphorus, mg P kg-1)
    - Olsen_P_mgP_per_kg_soil (Olsen-P, mg P kg-1)
  - Note: The document lists 35 columns with explanations and units; the example fields above illustrate the types of measurements included.

- GIS relevance and how to use
  - Each Sample_ID can be represented as a geolocated point; depth-stratified observations enable 3D or multi-layer mapping.
  - Site, Plot, Year, Sampling_time, and Treatment provide dimensions for filtering and thematic mapping (e.g., treatment effects over time or across depths).
  - Rich soil-property attributes support choropleth mapping, spatial statistics, and correlation analyses between digestate application and soil health indicators (pH, nutrients, organic matter, texture, moisture).

- Practical integration considerations for GIS workflows
  - Spatial linkage: align Sample_ID records with spatial coordinates via Site/Plot metadata or an external GIS layer; create point features per sample.
  - Depth handling: decide between single-layer analysis with Depth_cm as an attribute or multiple layers (one per depth) to create separate GIS layers.
  - Temporal analysis: utilize Sampling_date and Sampling_time to examine changes between T1 and T2.
  - Data quality: ensure unit consistency and handle potential missing values; verify coordinate system and projection when joining with spatial data.

- Provenance and access notes
  - Part of CINAg data series; a supplement to Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf.
  - File described: CINAg_digestate_experiment_2017_Soil_physicochemical_properties.csv.
  - Focus: digestate trial 2017 soil physicochemical properties across two farm sites.