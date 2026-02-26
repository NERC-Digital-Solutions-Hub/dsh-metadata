# Details of data structure to CINAg_digestate_experiment_2017_Soil_physicochemical_properties.csv

- This document is a supplement to the supporting documentation for CINAg experiments and describes the data structure for the soil physicochemical properties dataset from the 2017 digestate trial.
- Dataset: CINAg_digestate_experiment_2017_Soil_physicochemical_properties.csv
- Size: 35 columns, 180 rows
- Scope: Data collected during the 2017 digestate experiment

## Dataset composition and scope

- Data originate from a digestate trial in 2017.
- Each row represents a sample with associated metadata and measurements.
- Sampling context:
  - Year: Year samples were taken
  - Site: Farm platform codes (NW = North Wyke, HF = Henfaes Farm)
  - Sampling_date: Date of sampling (dd/mm/yyyy)
  - Sampling_time: T1 (beginning of experiments after digestate application) and T2 (last harvest)
  - Plot: Plot numbers
  - Treatment: C = Control, D = digestate, ADNI = acidified digestate with nitrification inhibitor DMPP
  - Depth_cm: Soil depth categories (0-15 cm, 15-30 cm, 30-60 cm)

## Column definitions and units

- Sample_ID: Unique sample identifier (Year_Experiment_Site_Sampling_time_Treatment_Plot_Depths)
- Depth_cm: Depth category; one of 0-15, 15-30, 30-60
- NH4_mgN_per_kg_soil: Ammonium in mg N per kg soil (dry soil)
- NO3_mgN_per_kg_soil: Nitrate in mg N per kg soil (dry soil)
- DOC_mgC_per_kg_soil: Dissolved organic carbon in mg C per kg soil
- DON_mgN_per_kg_soil: Organic nitrogen in mg N per kg soil
- Aminoacids_mgN_per_kg_soil: Nitrogen in amino acids (mg N per kg soil)
- Peptides_and_proteins_mgN_per_kg_soil: N in peptides and proteins (mg N per kg soil)
- MBC_mgC_per_kg_soil: Microbial biomass carbon (mg C per kg soil)
- MBN_mgN_per_kg_soil: Microbial biomass nitrogen (mg N per kg soil)
- Aggr_b20µm_perc: Aggregates smaller than 20 µm (%)
- Aggr_b250µm_perc: Aggregates smaller than 250 µm (%)
- Aggr_b2000µm_perc: Aggregates smaller than 2000 µm (%)
- Sand_perc: Soil sand content (%)
- Silt_perc: Soil silt content (%)
- Clay_perc: Soil clay content (%)
- Soil_moisture_perc: Soil moisture content (%)
- LOI_perc: Loss-on-ignition (soil organic matter, %)
- pH_deionised_water: pH in deionised water
- pH_CaCl2: pH in calcium chloride
- EC_µS_per_cm: Electrical conductivity (µS/cm)
- POXC_mgC_per_kg_soil: Permanganate oxidisable carbon (available carbon) (mg C per kg soil)
- PO4.P_mgP_per_kg_soil: Citric acid extractable phosphorus (plant available P) (mg P per kg soil)
- totC_perc: Total soil carbon content (%)
- totN_perc: Total soil nitrogen content (%)
- CN_ratio: Soil C-to-N ratio
- totP_mgP_per_kg: Total soil phosphorus content (mg P per kg)
- Olsen_P_mgP_per_kg_soil: Olsen-phosphorus (mg P per kg soil)

## Data structure, collection design, and potential usage

- The dataset is organized per sample with accompanying metadata (year, site, date, time, plot, depth) and a suite of soil physicochemical measurements.
- The three depth categories enable analysis of vertical gradients in response to digestate treatments.
- Treatments allow comparisons among control, digestate, and acidified digestate with nitrification inhibitor.
- Measurements cover inorganic N (NH4, NO3), organic N (DON, amino acids, peptides/proteins), carbon pools (DOC, POXC, LOI, totC, etc.), microbial biomass (MBC, MBN), soil texture and structure (sand/silt/clay, aggregate fractions), moisture and basic chemical properties (pH, EC), and plant-available nutrients (Olsen_P, PO4_P).
- The data are suited to analyzing correlations, model-based predictions, and treatment effects on soil chemistry and fertility at different soil depths and time points.
- Meta information and provenance (data source, trial year, site codes) support data traceability and reuse.