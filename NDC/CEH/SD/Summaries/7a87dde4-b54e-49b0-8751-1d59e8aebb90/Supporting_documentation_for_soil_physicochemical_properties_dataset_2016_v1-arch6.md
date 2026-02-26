# Details of data structure to CINAg_soils_data_2016_v3.csv

## Overview
- Dataset from grassland fertiliser trial 2016.
- Contains 42 columns and 330 rows.
- Data type: soil chemistry, soil physical properties, and related metrics measured across multiple treatments, sites, times, and depths.

## Dataset purpose and context
- Supplement to supporting documentation for CINAg data series.
- Enables exploration of how inorganic fertilizer treatments affect soil properties in grassland systems.
- Structured to support data discovery, combination with other datasets, and creation of data products for end users.

## Experimental design
- Experiment: Inorganic fertilizer experiment.
- Treatments include: C (Control), U (Urea), IU (Urea inhibitor), AN (Ammonium nitrate).

## Sampling design and timing
- Sampling_times: T0, T1, and T2 (repeated samplings at the start and during the experiment; last harvest at T2).
- Plot: 1 to 16.
- Depths: 0–15 cm, 15–30 cm, 30–60 cm.
- Repeat: 0, 1, or 2 (replicates).

## Location and site codes
- Site codes: NW = North Wyke, HF = Henfaes Farm, EB = Easter Bush.
- Year: Year when samples were taken.

## Key variables (examples)
- Soil ions and nutrients: NH4_mgN_per_kg_soil, NO3_mgN_per_kg_soil, PO4.P_mgP_per_kg_soil, Olsen_P_mgP_per_kg_soil, Na_mg_Na_per_kg_soil, K_mg_K_per_kg_soil, Ca_mgCa_per_kg_soil, Mg_mgMg_per_kg_soil.
- Soil carbon and nitrogen: DOC_mgC_per_kg_soil, DON_mgN_per_kg_soil, Aminoacids_mgN_per_kg_soil, Peptides_and_proteins_mgN_per_kg_soil, MBC_mgC_per_kg_soil, MBN_mgN_per_kg_soil, LOI_perc, totC_perc, totN_perc, CN_ratio, totP_mgP_per_kg, POXC_mgC_per_kg_soil.
- Soil texture and structure: Sand_perc, Silt_perc, Clay_perc, Agg_stability_moist_perc, Agg_stability_dry_perc, Aggr_b20µm_perc, Aggr_b250µm_perc, Aggr_b2000µm_perc.
- Soil physical and chemical properties: Soil_moisture_perc, pH_deionised_water, pH_CaCl2, EC_µS_per_cm, LOI_perc.
- Sample identifiers: Sample_ID (Year_Experiment_Site_Sampling_time_Treatment_Plot_Depths).

## Data use and integration
- The explicit column headers with definitions and units support data cleaning, validation, and integration with other CINAg datasets.
- Enables cross-site, cross-time comparison and depth-specific analysis of fertilizer effects.
- Suitable for building dashboards, self-serve analyses, or reports focusing on soil nutrient dynamics, microbial biomass, and soil health indicators under different fertilizer regimes.

## Practical considerations for data support
- Ensure consistent interpretation of units across columns (as provided by the dataset).
- Align sampling_time and depth_code conventions when merging with additional data.
- Leverage the structured treatment and site codes to stratify analyses or build comparative visuals.