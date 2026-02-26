# Details of data structure to CINAg_soils_data_2016_v3.csv

- Purpose: Supplement to supporting documentation; describes the structure of the CINAg soils data for 2016, derived from the grassland fertiliser trial.
- Dataset scope: 42 columns and 330 rows; data collected in 2016 from an inorganic fertilizer experiment.
- Dataset location and naming: CINAg_soils_data_2016_v3.csv; used within CINAg data series documentation.

- Experimental design
  - Experiment type: Inorganic fertilizer experiment (grassland soil trial).
  - Sampling framework: Samples taken at three times (T0, T1, T2) during the experiment; sampling at the start and subsequent harvests.
  - Sites: Farm platforms—NW (North Wyke), HF (Henfaes Farm), EB (Easter Bush).
  - Plot structure: Plot numbers 1–16.
  - Treatments: C = Control, U = Urea, IU = Urea inhibitor, AN = Ammonium nitrate.
  - Depths: 0–15 cm, 15–30 cm, 30–60 cm.
  - Repetitions: Repeat values 0, 1, or 2.
  - Sample_ID: Unique identifier formatted as Year_Experiment_Site_Sampling_time_Treatment_Plot_Depths.

- Cols and data content (examples of measured properties)
  - Soil inorganic and organic nitrogen forms: NH4_mgN_per_kg_soil; NO3_mgN_per_kg_soil; DON_mgN_per_kg_soil; Aminoacids_mgN_per_kg_soil; Peptides_and_proteins_mgN_per_kg_soil; MBN_mgN_per_kg_soil; MBC_mgC_per_kg_soil.
  - Carbon and organic matter: DOC_mgC_per_kg_soil; LOI_perc; totC_perc; totN_perc; CN_ratio; POXC_mgC_per_kg_soil.
  - Microbial and biological indicators: MBM_mgN_per_kg_soil (microbial biomass nitrogen); Aggr and soil structure indicators (Aggr_b20µm_perc; Aggr_b250µm_perc; Aggr_b2000µm_perc; Agg_stability_moist_perc; Agg_stability_dry_perc).
  - Soil physical properties: Soil_moisture_perc; pH_deionised_water; pH_CaCl2; EC_µS_per_cm; Sand_perc; Silt_perc; Clay_perc.
  - Nutrient availability and chemistry: Olsen_P_mgP_per_kg_soil; PO4.P_mgP_per_kg_soil; totP_mgP_per_kg_soil; Na_mg_Na_per_kg_soil; K_mg_K_per_kg_soil; Ca_mgCa_per_kg_soil; Mg_mgMg_per_kg_soil.
  - Other soil indicators: A suite of phosphorus, carbon, nitrogen, and trace element-related metrics as listed above for comprehensive soil health assessment.

- Data standardization and usage
  - Data are collected and organized using standardized field and laboratory procedures; intended to support consistent environmental health assessments over time.
  - Outputs enabled by the data include categorising environmental health against standards and generating outputs such as reports, maps, and charts.
  - Data management: Datasets are stored and uploaded to appropriate data portals; prepared to be linked with other CINAg datasets to enhance value.

- Relevance to environmental monitoring
  - Provides depth- and time-resolved soil nutrient and health indicators under controlled fertilizer treatments.
  - Facilitates evaluation of fertilizer impacts on soil chemistry, carbon dynamics, microbial biomass, and physical soil structure.
  - Supports cross-site comparisons (NW, HF, EB) and temporal monitoring within grassland systems.

- Considerations and limitations
  - Scope is specific to the 2016 grassland fertilizer trial; may require integration with broader CINAg datasets for comprehensive monitoring.
  - Dataset size: 330 samples across 42 columns; suitable for standardised analyses but may require data merging for multi-site policy-level assessments.

- Access and reuse guidance (Analyst perspective)
  - Leverage the metadata to understand column definitions, units, and sampling design.
  - Use the Sample_ID encoding to trace samples by year, site, time point, treatment, plot, and depth.
  - When combining with other CINAg datasets, align on site codes, depth conventions, and sampling times to ensure consistency.