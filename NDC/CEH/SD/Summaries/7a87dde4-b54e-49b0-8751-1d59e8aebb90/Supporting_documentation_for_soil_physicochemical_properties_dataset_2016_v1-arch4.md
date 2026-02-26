# Details of data structure to CINAg_soils_data_2016_v3.csv

- Overview
  - A dataset from a grassland fertiliser trial conducted in 2016.
  - Contains 42 columns and 330 rows.
  - Data originate from an inorganic fertilizer experiment across three sites (NW = North Wyke, HF = Henfaes Farm, EB = Easter Bush).
  - Includes measurements of soil chemical, biological, and physical properties at multiple depths and timepoints.

- Dataset structure and schema
  - Primary identifier: Sample_ID, a unique ID encoded as Year_Experiment_Site_Sampling_time_Treatment_Plot_Depths.
  - Key contextual fields:
    - Year: year samples were taken
    - Site: NW, HF, or EB
    - Sampling_date: date of sampling (dd/mm/yyyy)
    - Sampling_time: T0, T1, or T2
    - Plot: 1–16
    - Treatment: C (Control), U (Urea), IU (Urea inhibitor), AN (Ammonium nitrate)
    - Depth_cm: 0–15, 15–30, or 30–60
    - Repeat: 0, 1, or 2
  - Data structure note: 42 columns cover a range of soil chemistry, biology, physical properties, and nutrient pools.

- Key variable categories and representative fields
  - Inorganic and organic soil nutrients and pools
    - NH4_mgN_per_kg_soil, NO3_mgN_per_kg_soil
    - DOC_mgC_per_kg_soil, DON_mgN_per_kg_soil
    - Aminoacids_mgN_per_kg_soil, Peptides_and_proteins_mgN_per_kg_soil
    - MBC_mgC_per_kg_soil, MBN_mgN_per_kg_soil
  - Soil texture, structure, and organic matter indicators
    - Aggr_b20µm_perc, Aggr_b250µm_perc, Aggr_b2000µm_perc
    - Sand_perc, Silt_perc, Clay_perc
    - Agg_stability_moist_perc, Agg_stability_dry_perc
    - LOI_perc (loss-on-ignition)
  - Soil chemical properties and salinity
    - pH_deionised_water, pH_CaCl2
    - EC_µS_per_cm
    - Na_mg_Na_per_kg_soil, K_mg_K_per_kg_soil
    - Ca_mgCa_per_kg_soil, Mg_mgMg_per_kg_soil
  - Plant-availability and nutrient pools
    - POXC_mgC_per_kg_soil, PO4.P_mgP_per_kg_soil
    - Olsen_P_mgP_per_kg_soil
  - Total and ratio metrics
    - totC_perc, totN_perc, CN_ratio
    - totP_mgP_per_kg

- Data governance and usability notes
  - Each column includes a header explanation and unit specification.
  - The dataset is a structured extract intended to support analysis of fertilizer treatments, depth, site, and time effects on soil properties.
  - Units are typically mg/kg for nutrients, percentages for soil constituents and texture, and µS/cm for EC.
  - As a supplementary data structure reference, it complements broader CINAg supporting documentation and should be used in conjunction with it for full context and metadata.

- How this supports data leadership needs
  - Enables end-to-end view of the data system: multi-site, multi-depth, and multi-timepoint data linked by a consistent Sample_ID schema.
  - Facilitates data discovery and integration with other CINAg datasets through explicit fields (Year, Site, Sampling_time, Treatment, Plot, Depth_cm).
  - Supports governance of data quality and metadata: explicit units, clear column explanations, and measurable properties across soil chemistry, biology, and physics.
  - Suitable for iterative analytics and user-centered reporting on fertilizer impacts, while enabling reproducibility through a well-documented data structure.