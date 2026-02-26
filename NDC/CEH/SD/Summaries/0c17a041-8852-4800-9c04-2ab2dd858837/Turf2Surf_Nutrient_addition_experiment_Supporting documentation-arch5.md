# Turf2Surf - Nutrient addition experiment

- Purpose and scope
  - Investigates stoichiometric coupling of carbon (C), nitrogen (N), and phosphorus (P) in soils by applying C, N, and P to soil cores from four land-use types and measuring soil respiration and N2O fluxes.
  - Includes a pilot study to inform nutrient additions and incubation timing, followed by a main experiment across four Turf2Surf sites (bog, acid grassland, improved grassland, and arable land) with cores collected to 100 cm depth.

- Experimental design and timeline
  - Pilot experiment (Nov 2013–Dec 2013):Topsoil (0–15 cm) cores from three land uses; multiple C additions (glucose or glycine), N, P, and combinations (CN, CP, NP, CNP, etc.); multiple incubation times to determine gas emission dynamics; nutrients applied in increments with artificial rain to maintain field capacity.
  - Main experiment (Jan–Feb 2014 collection; nutrients applied over 4 months): Four sites with intact cores (4 cm diameter) from 0–15 cm and 85–100 cm depths, co-located with plots for plant/soil measurements. Full factorial eight treatments: Control, C, N, P, CN, CP, NP, CNP; 1.20 mg C g−1 soil added in three consecutive days; N and P added to achieve C:N = 10 and C:P = 70; additional time points after initial additions to observe postponed responses.
  - Mercury-treated negative control to evaluate nutrient distribution in cores.

- Data collected and measurements
  - Gas flux measurements: CO2 and N2O concentrations and production during incubations; gas samples collected at multiple time points (0, 1–3 hours in pilot; 0, 1, 2, and 3 hours in some main experiments) and analyzed via gas chromatography.
  - Soil and core properties: weights at field capacity and before incubations; post-water-adjusted weights; land-use type; soil depth (0–15 cm topsoil and 85–100 cm deep core segments); total soil dry weight; total LOI (weight of soil organic matter).
  - Nitrogen mineralization: measured in control cores after flushing with artificial rain solution for 4–5 days, then a 2-week incubation at 10 °C; soil extracts analyzed for NO3− and NH4+ (KCl extraction), with totals reported per g dry weight and per g organic matter.
  - Additional methods: soil cores stored at 4 °C to preserve moisture; artificial rain solution composition and pH described; N mineralization data and gravimetric soil organic matter determined.

- Data structure and files
  - Pilot dataset (CSV): Experimental_dataset_Carbon_Nitrogen_and_Phosphorous_additions_to_topsoil_and_subsoil_cores_from_the_Conwy_catchment-pilot_experiment_(2014).csv
    - 12 columns (A–L); 1–649 rows
    - Key fields: Campaign, Date, Soil core number, Nutrient treatment, Land use type, Incubation chamber, Time point, CO2 concentration, CO2 production, with fields for weights and land use.
  - Main experiment dataset (CSV): Experimental_dataset_Carbon_Nitrogen_and_Phosphorous_additions_to_topsoil_and_subsoil_cores_from_the_Conwy_catchment-main_experiment_(2014).csv
    - 24 columns (A–X); 1–3889 rows
    - Key fields: Campaign, Date, Unique core number, Plot number, Core number, Nutrient treatment, indicators for Carbon/Nitrogen/Phosphorus additions, Mercury flag, Soil depth, Weights, Land use type, Incubation chamber, Time point, Gas concentrations/production (CO2 and N2O), Total soil dry weight, Total LOI weight.
  - Nitrogen mineralization dataset (CSV): Experimental_dataset_Nitrogen_mineralization_in_topsoil_and_subsoil_cores_from_the_Conwy_catchment_(2014).csv
    - 12 columns (A–L); 1–25 rows
    - Key fields: Date, Unique core number, Plot number, Nutrient treatment, Soil depth, Land use type, NO3−-N, NH4+-N, Total N mineralization, NO3−-N per g dry weight and per g organic matter, NH4+-N per g dry weight and per g organic matter, Total N per g organic matter.

- Metadata and provenance
  - Project and personnel: Turf2Surf WP2 team members and contributors listed for field sampling, laboratory work, and data analysis; data linked to plant and soil measurements intended for incorporation into the JULES model.
  - Documentation references: Supporting documentation available (e.g., Turf2Surf WP2 Supporting documentation.rtf) for additional context and methods.

- Data quality, standards, and governance considerations
  - Standards and consistency: Detailed descriptions of treatments, depths, land-use categories, and units (e.g., mg N g−1 DW for mineralizable N, g for weights, ppm for gas concentrations) facilitate cross-dataset harmonization.
  - Provenance and traceability: Clear field-to-lab workflow, including replication, chamber IDs, and timepoints; explicit measurement methodologies (GC for CO2/N2O, KCl extraction for mineralization) support reproducibility.
  - Storage and handling: Samples stored at 4 °C when not in use; core weights adjusted to field capacity before nutrient additions; artificial rain solution used to mimic UK rainfall and avoid leaching of nutrients beyond the core.
  - Challenges and considerations for reuse: Multi-site design with different soils and depths (including a bog requiring a different corer) may demand careful standardization; data volumes are substantial, with several thousand rows in the main dataset and multiple time-series gas measurements; alignment of units and column semantics across pilot, main, and mineralization datasets is essential for comparative analyses.

- Potential uses for data stewards and users
  - Data governance: Apply consistent metadata to ensure discoverability and usability across the four land-use types and soil depths; maintain clear linking of core numbers to plots and treatments.
  - Data integration: Combine gas flux data with nitrogen mineralization results and soil properties to parameterize ecosystem models (e.g., JULES) and to study nutrient stoichiometry under varying C, N, P additions.
  - Data quality improvements: Consider harmonizing column naming and units across pilot and main datasets; ensure complete documentation of incubation timings and replicates; preserve links to supporting documentation and methodological references.