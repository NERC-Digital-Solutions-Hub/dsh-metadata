# Supporting documentation for data: 'Empirical and modelled carbon, nitrogen and phosphorus content of plants and soils from Wardlow Hay Cop, UK'

- Purpose and context
  - Datasets accompany a Taylor et al. manuscript (2021, Biogeosciences) and are used to produce figures and calibrate the mechanistic model described.
  - Provide empirical soil carbon (SOC), total nitrogen (SON), and total phosphorus (P) stocks for two grassland types at Wardlow Hay Cop, enabling comparison with model outputs and supporting mechanistic understanding of carbon and nutrient cycling under long-term nitrogen deposition and nutrient manipulation.

- Study site and experimental design
  - Wardlow Hay Cop, Derbyshire, UK: two co-located grassland communities (limestone and acidic soils).
  - Long-term nutrient manipulation experiment established in the 1990s; treatments include:
    - 0N (control, background N deposition)
    - LN (low nitrogen)
    - HN (high nitrogen)
    - P (phosphorus addition)
  - Treatments applied monthly since 1995 (and bi-monthly since 2017); nutrient additions use NH4NO3 for N and NaH2PO4·H2O for P.
  - Sampling: 6 soil cores per grassland-treatment combination, across 3 blocks (A, B, C); limestone sampled to 10 cm, acidic to 20 cm; horizons separated into organic and mineral for analysis.
  - Sampling period: summer 2019 for C and N analyses; phosphorus data drawn from 2003 (Horswill et al., 2008).

- Data types and conversions
  - Empirical data:
    - Soil C and N (% and stocks) converted to model-compatible topsoil units (15 cm depth) expressed as g m^-2.
    - Phosphorus data (mmol kg^-1) converted to g m^-2 using molecular weights and the same topsoil conversion approach.
  - Completeness:
    - C and N data available for all four nutrient treatments.
    - P data available for only half of the treatments (control 0N and high nitrogen HN); lacking complete P measurements for all treatments.
  - Processing workflow:
    - Bulk density and horizon depths used to estimate soil mass.
    - Acid stripping to remove inorganic carbon prior to IRMS analysis for C and N.
    - Empirical topsoil depth is adjusted differently for limestone (assumed 15 cm) and acidic soil (10 cm organic + half of mineral horizon to total 15 cm).

- The N14CP model
  - A mechanistic carbon, nitrogen, and phosphorus cycling model simulating pools across plants, soil (topsoil and subsoil), atmosphere, and leachates.
  - Stoichiometric relationships and Liebig’s law of the minimum guide nutrient flows; N-P interactions included.
  - Calibrated to Wardlow data by fitting two phosphorus cycling parameters (P Weath0 and P CleaveMax).
  - Inputs include background N deposition, climate (temperature and precipitation), and plant functional history (land-use history proxy).
  - Outputs present modeled SOC, SON, and P stocks and compare with empirical data; datasets reflect model topsoil units (15 cm) and are primarily model-derived.

- Data files and scope
  - Wardlow_empirical_vs_modelled_CNP.csv
    - Compares empirical versus modeled C, N, and P stocks by grassland (Acid/Limestone) and treatment (0N, LN, HN, P); includes observed and simulated values, standard errors, differences, and percent differences.
  - Wardlow_mean_CNP_difference.csv
    - Summary of mean differences between simulated and observed data with standard error, across treatments and grasslands.
  - Wardlow_modelled_P_cleaving.csv
    - Model parameter P CleaveMax by grassland-treatment and the modeled annual P cleaved from the organic P pool in 2020.
  - Wardlow_modelled_N_deposition.csv
    - Modelled effects of N deposition (1800–2020) on C, N, P stocks for 0N treatment (baseline) across grasslands; includes year-anchored stocks and diffs.
  - Wardlow_modelled_nutrient_treatments.csv
    - Modelled stocks for C, N, P (and AGB C) under different nutrient treatments relative to 0N; shows absolute and percentage differences after 1995.
  - Wardlow_modelled_CNP_budgets.csv
    - Modelled pool sizes used to construct C, N, and P budgets (topsoil and subsoil C, N, various pools like available and biomass pools) for both grasslands; all values in g m^-2.
  - References included for model description and empirical data sources.

- Relevance for monitoring frameworks
  - Provides a concrete case of integrating empirical field data with a process-based model to monitor and predict responses of soil carbon and nutrient stocks to nutrient deposition and management.
  - Demonstrates data transformation and harmonization steps needed to compare empirical measurements with modelled outputs (unit conversions, depth adjustments, topsoil framing).
  - Highlights the role of calibrating key model parameters (P weathering and organic P access) to observed data, a central activity in monitoring frameworks that rely on predictive modeling.
  - Illustrates handling data gaps (incomplete P data) and documenting these limitations for transparent interpretation and governance.
  - Emphasizes data provenance, sharing of underlying data, and the importance of metadata quality when data are used for policy-relevant dashboards, reports, or governance processes.

- Key considerations and challenges for monitoring use
  - Data gaps: incomplete phosphorus data across all treatments; careful interpretation required when integrating P stocks into budgets and indicators.
  - Metadata and transformation: explicit description of horizon depths, bulk densities, and conversion procedures necessary for reproducibility and governance checks.
  - Data governance and openness: model-calibrated outputs rely on sharing both empirical and model-derived data; consider access controls and documentation to enable reuse while protecting data provenance.
  - Communicating complex results: translating model–data differences and budgets into clear indicators for policy evaluation and decision-making.

- Notes on availability and usage
  - Datasets are linked to a published manuscript and provide data to reproduce figures and calibrate the N14CP model.
  - Model outputs represent best-guess estimates, with explicit comparisons to empirical data and quantified differences to support uncertainty assessment in monitoring contexts.