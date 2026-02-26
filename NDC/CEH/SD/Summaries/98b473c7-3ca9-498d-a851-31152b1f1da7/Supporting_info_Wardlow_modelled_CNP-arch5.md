# Supporting documentation for data: 'Empirical and modelled carbon, nitrogen and phosphorus content of plants and soils from Wardlow Hay Cop, UK'

- Purpose and scope
  - Provides empirical and modelled C, N, and P data related to Taylor et al. (2021) Biogeosciences.
  - Data used to produce figures in the manuscript and to calibrate the N14CP mechanistic model of C, N, and P cycling.

- Dataset types and contents
  - Empirical data: new estimates of soil organic carbon (SOC) and total nitrogen (SON) stocks from Wardlow Hay Cop grasslands; phosphorus data from 2003 (from Horswill et al., 2008) included for model input.
  - Modelled data: outputs from the N14CP model, including SOC, SON, total P stocks, modelled budgets, and comparisons with empirical data.
  - Model calibration data: two phosphorus cycling parameters (P Weath0 and P CleaveMax) calibrated to the Wardlow data.
  - Comparative and diagnostic files: empirical vs. modelled CNP, mean differences, P cleaving, simulated N deposition effects, nutrient-treatment differences, and CNP budgets by grassland and treatment.

- Study site and experimental design
  - Wardlow Hay Cop long-term nutrient manipulation experiment, Derbyshire, UK; two grassland types (acidic and limestone).
  - Established mid-1990s; four nutrient treatments: 0N (control), LN (low N), HN (high N), and P (phosphorus).
  - Treatments applied monthly (until 2017, then bi-monthly); NH4NO3 used for N, NaH2PO4.H2O for P.
  - Experimental setup includes three blocks (A, B, C) with six soil cores per grassland-treatment combination.

- Data collection and processing details
  - Empirical sampling in 2019 (approximately 24 years of nutrient treatment); P data largely from 2003.
  - Depths for sampling: limestone grassland to 10 cm; acidic grassland to 20 cm.
  - Soil cores split into organic and mineral horizons; bulk density measured to estimate stocks; SOC and SON determined via IRMS after acid-stripping to remove inorganic carbon.
  - Phosphorus data converted to model-compatible units using established conversions; data stored in cold room and processed within months of collection.
  - Empirical data converted to modelled “topsoil” units (15 cm depth) expressed as g m^-2; limestone treated as effectively 15 cm topsoil; acidic soil adjusted from 20 cm to represent 15 cm topsoil.

- Model description and integration
  - N14CP model: mechanistic C, N, and P cycling across plant, soil (topsoil and subsoil), atmosphere, and leachate; uses Liebig’s law of the minimum with N-P interactions considered.
  - Model inputs required: background N deposition, climate data (temperature, precipitation), and plant functional history (land-use analogue).
  - Calibration: empirical data used to calibrate two phosphorus parameters (P Weath0 and P CleaveMax) for each grassland-treatement combination.
  - Output types: modeled SOC, SON, P stocks; modelled budgets; comparisons with empirical data; P cleaving and N deposition effects.

- Data files and formats
  - Wardlow_empirical_vs_modelled_CNP.csv (CSV, ~1.48 KB): compares empirical and simulated C, N, and P stocks for each grassland-treatment; includes Obs, Sim, SE, Diff, and Percent differences.
  - Wardlow_mean_CNP_difference.csv (CSV, ~209 bytes): mean differences and standard errors between simulated and observed data by grassland and nutrient.
  - Wardlow_modelled_P_cleaving.csv (CSV, ~236 bytes): modelled P cleaving parameter (P CleaveMax) and P cleaved in 2020 by grassland-treatment.
  - Wardlow_modelled_N_deposition.csv (CSV, ~1.34 KB): modelled effects of N deposition (1800–2020) on C, N, P pools for 0N treatment.
  - Wardlow_modelled_nutrient_treatments.csv (CSV, ~1.00 KB): differences in modelled C, N, P, and AGB_C across nutrient treatments relative to 0N.
  - Wardlow_modelled_CNP_budgets.csv (CSV, ~1.60 KB): modelled pool sizes (Subsoil_SOC, Topsoil_SOC, Biomass_C, Subsoil_SON, Topsoil_SON, Available_N, Fixed_N, Biomass_N, Weatherable_P, Subsoil_sorbed_P, Subsoil_SOP, Topsoil_sorbed_P, Topsoil_SOP, Available_P, Biomass_P) used to construct C, N, and P budgets.
  - All data relate to Wardlow, with clear grassland (Acid/Limestone) and treatment (0N, LN, HN, P) identifiers; units are grams per square metre (g m^-2) for stocks and budgets where stated.

- Data provenance, quality, and limitations
  - Primary empirical data collected by Christopher Taylor (PhD student) under supervision of Gareth Phoenix and Jessica Davies.
  - Model outputs are calibrated to empirical data; majority of data are model-derived rather than raw measurements.
  - Completeness note: phosphorus data are incomplete for half of the nutrient treatments (control 0N and high nitrogen HN missing); remaining C and N data exist for all four treatments.
  - Publication status: data accompany a manuscript accepted for Biogeosciences (Taylor et al., 2021); no DOI available at publication time; refer to catalogue record for full citation.
  - Data sources and model documentation cited for reproducibility: Davies et al. 2016 (N14CP model); Horswill et al. 2008 (P data source); Morecroft et al. 1994 (Wardlow experimental setup).

- Governance, usage, and reuse notes
  - Documentation includes detailed methodology, conversion procedures, and model assumptions to support reproducibility and data reuse.
  - Data intended to support figures and model calibration; suitable for researchers analyzing long-term nutrient cycling, CNP budgets, and model-data integration.
  - Recommend cataloging with persistent identifiers (DOIs/DOIs for data products) and comprehensive metadata, including variable definitions, column formats, and provenance.
  - Consider providing raw empirical data alongside processed/modelled datasets, along with clear licensing information and update plans if additional data are collected.