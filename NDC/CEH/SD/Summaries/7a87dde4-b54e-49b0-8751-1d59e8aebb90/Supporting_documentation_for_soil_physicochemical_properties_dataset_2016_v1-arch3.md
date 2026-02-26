# Details of data structure to CINAg_soils_data_2016_v3.csv

## Overview
- Supplement to supporting documentation for CINAg experiments.
- Data originate from a grassland fertiliser trial conducted in 2016.
- The dataset comprises 42 columns and 330 rows.
- Captures soil chemical, physical, and biological properties across treatments, depths, sites, and sampling times.

## Experimental design and sampling
- Experiment: Inorganic fertilizer experiment.
- Sampling framework uses multiple factors:
  - Year of sampling
  - Site: NW (North Wyke), HF (Henfaes Farm), EB (Easter Bush)
  - Plot numbers: 1–16
  - Depths: 0–15 cm, 15–30 cm, 30–60 cm
  - Sampling_time: T0, T1, T2
  - Treatment: C (Control), U (Urea), IU (Urea inhibitor), AN (Ammonium nitrate)
  - Repeat: 0, 1, or 2
- Each row represents a unique sample identified by a composite Sample_ID built from Year, Experiment, Site, Sampling_time, Treatment, Plot, and Depths.

## Data structure and content
- Column headers followed by explanations and units.
- Primary identifiers:
  - Sample_ID: unique sample identifier
  - Year, Site, Sampling_date, Sampling_time, Plot, Depth_cm, Repeat
- Multiple soil properties measured, spanning chemical, biological, and physical domains.
- Depth-wise measurements allow comparison across soil horizons (0–15 cm, 15–30 cm, 30–60 cm).
- Time-series elements through T0, T1, T2 sampling points.

## Key variable categories (representative examples)
- Nutrients and inorganic forms: NH4_mgN_per_kg_soil, NO3_mgN_per_kg_soil, Olsen_P_mgP_per_kg_soil, PO4.P_mgP_per_kg_soil
- Organic and total pools: DOC_mgC_per_kg_soil, DON_mgN_per_kg_soil, Aminoacids_mgN_per_kg_soil, Peptides_and_proteins_mgN_per_kg_soil, totC_perc, totN_perc, CN_ratio
- Microbial/biochemical indicators: MBC_mgC_per_kg_soil, MBN_mgN_per_kg_soil, POXC_mgC_per_kg_soil
- Soil chemistry and buffering: pH_deionised_water, pH_CaCl2, EC_µS_per_cm, Na_mg_Na_per_kg_soil, K_mg_K_per_kg_soil, Ca_mgCa_per_kg_soil, Mg_mgMg_per_kg_soil
- Soil physical and structural properties: Aggr_b20µm_perc, Aggr_b250µm_perc, Aggr_b2000µm_perc, Sand_perc, Silt_perc, Clay_perc, Agg_stability_moist_perc, Agg_stability_dry_perc, Soil_moisture_perc, LOI_perc
- Carbon and phosphorus pools: totP_mgP_per_kg, Olsen_P_mgP_per_kg_soil
- Miscellaneous soil health indicators: POXC (available carbon), CN_ratio, etc.

## Data quality, metadata and governance considerations
- Dataset includes explicit units and explanations for each column, aiding transparency and reproducibility.
- Metadata is embedded at the column level, supporting provenance and traceability across sampling events.
- Structure supports data cleaning, transformation, and quality assurance processes aligned with monitoring and reporting needs.
- As a structured data resource, it facilitates data sharing and the construction of dashboards or reports for monitoring environmental health indicators in grassland systems.

## Relevance for monitoring and decision-making
- Enables assessment of fertilizer treatments on soil chemical, biological, and physical properties over time and with depth.
- Supports comparative analyses across sites and plots to inform management decisions and policy evaluations.
- The explicit, well-documented schema helps practitioners identify which variables are available, their units, and how samples are organized, supporting transparent reporting and data governance.