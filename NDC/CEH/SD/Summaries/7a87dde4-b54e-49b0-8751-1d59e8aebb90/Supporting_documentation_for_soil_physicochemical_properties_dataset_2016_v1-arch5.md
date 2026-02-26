# Details of data structure to ' CINAg_soils_data_2016_v3.csv '

## Overview
- Supplement describing the data structure for CINAg soils dataset from a grassland fertiliser trial in 2016.
- Dataset characteristics: 42 columns and 330 rows.
- Experiment context: Inorganic fertilizer experiment; grassland soil measurements across multiple depths and times.

## Dataset structure and keys
- Sample_ID: Unique sample identifier formatted as Year_Experiment_Site_Sampling_time_Treatment_Plot_Depths.
- Year: Year samples were taken.
- Site: Farm platform codes (NW = North Wyke, HF = Henfaes Farm, EB = Easter Bush).
- Sampling_date: Date of sampling (dd/mm/yyyy).
- Sampling_time: Timepoints T0, T1, T2 (T2 at last harvest).
- Plot: Plot numbers 1–16.
- Treatment: Fertilizer treatments (C = Control, U = Urea, IU = Urea inhibitor, AN = Ammonium nitrate).
- Depth_cm: Sampling depth categories (0-15 cm, 15-30 cm, 30-60 cm).
- Repeat: Replicate number (0, 1 or 2).

## Measured variables and units (representative examples)
- NH4_mgN_per_kg_soil: Soil extractable ammonium (mg N per kg dry soil).
- NO3_mgN_per_kg_soil: Soil extractable nitrate (mg N per kg dry soil).
- DOC_mgC_per_kg_soil: Dissolved organic carbon (mg C per kg dry soil).
- DON_mgN_per_kg_soil: Organic nitrogen (mg N per kg dry soil).
- Aminoacids_mgN_per_kg_soil: Nitrogen in amino acids (mg N per kg dry soil).
- Peptides_and_proteins_mgN_per_kg_soil: Nitrogen in peptides/proteins (mg N per kg dry soil).
- MBC_mgC_per_kg_soil: Microbial biomass carbon (mg C per kg dry soil).
- MBN_mgN_per_kg_soil: Microbial biomass nitrogen (mg N per kg dry soil).
- Aggr_b20µm_perc, Aggr_b250µm_perc, Aggr_b2000µm_perc: Aggregate size fractions (%).
- Sand_perc, Silt_perc, Clay_perc: Soil texture components (%).
- Agg_stability_moist_perc, Agg_stability_dry_perc: Aggregate stability (%; moist and dry conditions).
- Soil_moisture_perc: Soil moisture (%).
- LOI_perc: Loss-on-ignition (soil organic matter) (%).
- pH_deionised_water, pH_CaCl2: pH in deionised water and CaCl2 (unitless).
- EC_µS_per_cm: Electrical conductivity (µS per cm).
- Na_mg_Na_per_kg_soil, K_mg_K_per_kg_soil, Ca_mgCa_per_kg_soil, Mg_mgMg_per_kg_soil: Base cations (concentration per kg soil; units as listed in column headers).
- POXC_mgC_per_kg_soil: Permanganate oxidisable carbon (available carbon; mg C per kg dry soil).
- PO4.P_mgP_per_kg_soil: Citric acid extractable phosphorus (plant available P; mg P per kg dry soil).
- totC_perc, totN_perc: Total soil carbon and nitrogen content (%).
- CN_ratio: Soil carbon-to-nitrogen ratio (dimensionless).
- totP_mgP_per_kg: Total soil phosphorus content (mg P per kg dry soil).
- Olsen_P_mgP_per_kg_soil: Olsen phosphorus (mg P per kg dry soil).

## Data collection context
- Experiment type: Inorganic fertilizer experiment.
- Sampling framework: Multiple sampling times (T0, T1, T2) across three depths (0–15, 15–30, 30–60 cm) and 16 plots per site.
- Treatments capture fertiliser scenarios (Control, Urea, Urea inhibitor, Ammonium nitrate).

## Data quality and metadata considerations
- Metadata alignment: Ensure Sample_ID components correctly map to Year, Site, Sampling_time, Treatment, Plot, and Depth.
- Units consistency: Validate that all measurements use the specified units and that any conversions are documented.
- Data provenance: Dataset supplements broader CINAg documentation; maintain cross-references to Supporting_documentation_CINAg_experiments_final_check_v2.1.pdf.
- Metadata completeness: Include method of measurement, QC procedures, and any data processing steps (e.g., cleaning/transformations) used before sharing.

## Data governance, sharing, and maintenance
- Data accessibility: Dataset intended for discovery and reuse within CINAg and related ecosystems; ensure clear access conditions and embargo status if applicable.
- Data storage and cataloging: Upload to appropriate data portals and catalogue holdings; assign stable identifiers and versioning (e.g., CINAg_soils_data_2016_v3).
- Documentation: Record work performed on datasets (quality checks, transformations), and provide concise metadata descriptions for users.
- Interoperability considerations: Prepare for integration with other CINAg datasets by following consistent naming conventions, units, and taxonomies.

## Practical next steps for Data Stewards
- Verify and document metadata completeness, including measurement methods and QC steps.
- Ensure retention of original units and provide any needed conversion guidelines for downstream users.
- Map site codes to full site descriptors and update any missing or ambiguous fields in Sample_ID.
- Prepare and publish the dataset with accompanying metadata, cross-references to the supporting CINAg documentation, and clear licensing/access terms.
- Establish update and embargo policies if future data releases are anticipated, and document any sharing limitations.