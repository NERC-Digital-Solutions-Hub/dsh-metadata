# Details of data structure to ' CINAg_soils_data_2016_v3.csv '

- Dataset origin and scope
  - Grassland fertiliser trial from 2016.
  - Inorganic fertilizer experiment.
  - 42 columns (attributes) and 330 rows (samples).

- Dataset structure and identifiers
  - Sample_ID: unique sample identifier encoded as Year_Experiment_Site_Sampling_time_Treatment_Plot_Depths.
  - Year: year samples were taken.
  - Site: farm platforms (NW = North Wyke, HF = Henfaes Farm, EB = Easter Bush).
  - Sampling_date: date of sampling (dd/mm/yyyy).
  - Sampling_time: sampling occasions (T0, T1, T2).
  - Plot: plot numbers 1–16.
  - Treatment: fertilizer treatments (C = Control, U = Urea, IU = Urea inhibitor, AN = Ammonium nitrate).
  - Depth_cm: soil depths (0–15 cm, 15–30 cm, 30–60 cm).
  - Repeat: replication indicator (0, 1, or 2).

- Spatial and temporal dimensions relevant for GIS
  - Spatial dimension is represented at the site/plot level (NW, HF, EB) rather than explicit coordinates.
  - Temporal dimension captured by Sampling_date and Sampling_time (T0, T1, T2), enabling time-series analysis per plot/depth/treatment.

- Key data categories and example attributes
  - Soil inorganic and organic nitrogen forms: NH4_mgN_per_kg_soil, NO3_mgN_per_kg_soil, CN_ratio, totN_perc.
  - Carbon and organic matter: DOC_mgC_per_kg_soil, DON_mgN_per_kg_soil, MBC_mgC_per_kg_soil, LOI_perc, totC_perc.
  - Nitrogen and phosphorus pools: Aminoacids_mgN_per_kg_soil, Peptides_and_proteins_mgN_per_kg_soil, Olsen_P_mgP_per_kg_soil, totP_mgP_per_kg.
  - Soil biology/aging indicators: MB N_mgN_per_kg_soil, POXC_mgC_per_kg_soil.
  - Soil physical properties and texture: Sand_perc, Silt_perc, Clay_perc, EC_µS_per_cm, Soil_moisture_perc, pH_deionised_water, pH_CaCl2, Agg_stability_moist_perc, Agg_stability_dry_perc.
  - Exchangeable bases and salinity indicators: Na_mg_Na_per_kg_soil, K_mg_K_per_kg_soil, Ca_mgCa_per_kg_soil, Mg_mgMg_per_kg_soil.
  - Other soil chemistry/characteristics: PO4.P_mgP_per_kg_soil, Olsen_P_mgP_per_kg_soil, LOI (loss on ignition), EC (electrical conductivity).

- Units and scale notes
  - Nutrients and carbon: mg N or mg C per kg soil (dry soil).
  - Percentages: soil texture fractions, LOI, soil carbon/nitrogen contents.
  - pH: unitless.
  - EC: µS per cm.
  - Depth: cm (0–15, 15–30, 30–60).

- Primary use cases for GIS specialists
  - Build map layers by site, plot, depth, and time (T0/T1/T2) to visualize spatial patterns in soil properties.
  - Create attribute tables for each plot-depth-time combination to drive choropleth or graduated symbol maps of key soil indicators (e.g., NH4, NO3, pH, SOC, texture fractions).
  - Join with spatial farm boundary layers to contextualize within management units and treatments.
  - Support analysis of treatment effects by spatially linking fertilizer treatments with measured soil properties.
  - Enable time-series GIS analyses by filtering on Sampling_time (T0/T1/T2) to observe changes over the trial period.
  - Prepare data for rasterization or interpolation where appropriate, using depth-annotated attributes to create 3D soil property visualizations.