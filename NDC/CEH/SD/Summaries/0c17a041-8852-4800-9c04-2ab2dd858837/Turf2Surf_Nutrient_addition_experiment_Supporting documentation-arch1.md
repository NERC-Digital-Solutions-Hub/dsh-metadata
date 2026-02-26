# Turf2Surf - Nutrient addition experiment

- Aims and scope
  - Investigate stoichiometric coupling of carbon (C), nitrogen (N), and phosphorus (P) in soils across different land-use intensities.
  - Link plant and soil nutrient status to aboveground and belowground ecosystem processes for potential integration into the JULES model.
  - Use a pilot study to inform nutrient additions for a main, factorial field experiment across multiple sites.

- Experimental design overview
  - Pilot experiment (Nov 2013–Dec 2013): topsoil (0–15 cm) cores from grassland, conifer woodland, and bog subjected to varying C, N, and P additions; tested different C compounds and C:N/C:P ratios; multiple incubation times to optimize CO2 measurement timing; results informed main experiment protocol.
  - Main experiment (Jan–Feb 2014 start; subsequent 4 months of additions): soil cores from four Turf2Surf sites in Conwy catchment (bog, acid grassland, improved grassland, arable field). Intact cores to 100 cm depth were used; top and deep layers separated (0–15 cm and 85–100 cm). Full factorial 8 treatments: Control, C, N, P, CN, CP, NP, CNP; plus a negative HgCl2 control to assess nutrient distribution efficiency.
  - Replication: multiple cores per site/land-use type, co-located with plots measuring plant and soil parameters.

- Treatments and nutrient additions
  - C: added carbon (0.4 mg C g-1 dry soil per day over 3 days; total 1.20 mg C g-1 per core)
  - N and P: added to achieve specified C:N and C:P ratios based on pilot results (e.g., C:N = 10, C:P = 70 in main experiment)
  - Combined treatments: CN, CP, NP, and CNP (with specified C:N and C:P ratios)
  - Additional variations in C forms (glucose, glycine; root-exudate mimics with multiple organic acids and sugars) tested in the pilot
  - Mercury (HgCl2) negative control to evaluate nutrient distribution within cores

- Sampling, incubation, and measurements
  - Incubation temperature: 10°C
  - Gas measurements: CO2 and N2O concentrations and production from the same gas samples
  - Incubation timings:
    - Pilot: initial 2-hour incubations; follow-up measurements at 0, 1, or 2 hours depending on soil type; repeat incubations 1–3 days after second nutrient addition
    - Main: time points after chamber closure (0, then 1–3 hours depending on site); extended sampling to capture delayed responses
  - Water and moisture management: artificial rain solution used to reach field capacity; cores weighed before and after watering; water loss accounted for in nutrient additions
  - Depths and cores: 0–15 cm topsoil and 85–100 cm deep soil cores used; total of 216 cores in main experiment
  - N mineralization (Nmin): measured on control cores after a 4-week flushing with artificial rain solution; 2-week incubation at 10°C; post-incubation extraction with 1 M KCl; nitrate and ammonium analyzed
  - Soil characterization: total dry weight, loss on ignition (LOI) for soil organic matter; drying at 65°C and LOI at 375°C after removing stones/roots
  - Data handling: regular calibration with CO2 standards; N2O measurements included alongside CO2

- Data files and structure
  - Data file 1 (Pilot experiment)
    - Experimental_dataset_Carbon_Nitrogen_and_Phosphorous_additions_to_topsoil_and_subsoil_cores_from_the_Conwy_catchment-pilot_experiment_(2014).csv
    - Columns: A) Campaign; B) Date; C) Soil core number; D) Nutrient treatment; E) Weight at field capacity; F) Weight before incubation; G) Land use type; H) Incubation chamber; I) Time point; J) Time (min); K) CO2 concentration; L) CO2 production
    - Rows: 649
  - Data file 2 (Main experiment)
    - Experimental_dataset_Carbon_Nitrogen_and_Phosphorous_additions_to_topsoil_and_subsoil_cores_from_the_Conwy_catchment-main_experiment_(2014).csv
    - Columns include: Campaign; Date; Unique core number; Plot number; Core number; Nutrient treatment; Carbon/Nitrogen/Phosphorus additions (binary 1/0); Mercury addition (binary); Soil depth (0–15 cm / 85–100 cm); Weights (field capacity, pre-incubation, after water addition); Land use type; Incubation chamber; Time point; Time (min); CO2 concentration; CO2 production; N2O concentration; N2O production; Total soil dry weight; Total LOI weight
    - Rows: 3,889
  - Data file 3 (Nitrogen mineralization)
    - Experimental_dataset_Nitrogen_mineralization_in_topsoil_and_subsoil_cores_from_the_Conwy_catchment_(2014).csv
    - Columns: Date; Unique core number; Plot number; Nutrient treatment; Soil depth; Land use type; NO3-N; NH4-N; Total N mineralization; NO3-N per g organic matter; NH4-N per g organic matter; Total mineralization per g organic matter
    - Rows: 25
  - Note on data provenance: Laboratory work and data analysis conducted by named researchers; calculations and data analysis performed by Sabine Reinsch; data linked to WP2 outputs and broader Turf2Surf objectives

- Key attributes, units, and accessibility
  - Units: CO2 and N2O concentrations (ppm); production (ppm per incubation); Nmin values in mg N per g dry weight or per g organic matter; weights in g; C added per g dry soil (mg C g-1); ratios (C:N, C:P)
  - Source and structure designed to enable integration with ecosystem models (e.g., JULES) and cross-site comparisons across land-use types
  - Data documentation includes explicit column descriptions, measurement methods, and experimental timings to support reproducibility and re-use

- Personnel and acknowledgments
  - Field sampling and laboratory work conducted by a dedicated team; data processing and analyses performed by Sabine Reinsch and colleagues; project components linked to Turf2Surf WP2 and collaborators for plant-soil process integration