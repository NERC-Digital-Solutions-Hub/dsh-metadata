# Supporting documentation for data: 'Empirical and modelled carbon, nitrogen and phosphorus content of plants and soils from Wardlow Hay Cop, UK'

## Overview
- Supplementary data to Taylor et al. (2021) Biogeosciences, providing empirical C, N, and P data used to calibrate the N14CP model.
- Location: Wardlow Hay Cop, Derbyshire, UK, a long-term nutrient manipulation experiment across two grassland communities (limestone and acidic).
- Data support both empirical analyses and mechanistic modelling of carbon, nitrogen, and phosphorus cycling.

## Data content and purpose
- Empirical data:
  - New estimates of soil organic carbon (SOC) and total nitrogen (SON) stocks from 2019 for limestone and acidic grasslands.
  - Total soil phosphorus data from Horswill et al. (2008) used for model initial values.
  - Stock units converted to model-compatible units (g m^-2) for topsoils (15 cm depth in the model).
- Modelled data:
  - Outputs from the N14CP model, a mechanistic C, N, and P cycling model used to simulate pools and budgets and to compare with empirical estimates.
  - Model calibration targets include inorganic P availability (P Weath0) and organic P access (P CleaveMax).

## Wardlow experimental context
- Wardlow hay cop long-term nutrient manipulation experiment, established in the 1990s, with two grassland types (acidic and limestone) near the Peak District.
- Four nutrient treatments: 0N (control), LN (low N), HN (high N), P (phosphorus addition).
- Treatments replicated across three blocks (A, B, C); nitrogen supplied as NH4NO3 and phosphorus as NaH2PO4.H2O.
- Treatments applied quarterly (post-1995) with annual totals corresponding to the same N and P inputs.

## Sampling, processing, and data transformation
- Sampling design:
  - Six soil cores per grassland-treatment per block; limestone sampled to 10 cm, acidic to 20 cm; cores split into organic and mineral horizons.
  - Bulk density measurements obtained to estimate stocks.
- Laboratory processing:
  - Samples dried, ground, and acid stripped to remove inorganic carbon before IRMS analysis for C and N.
- Data conversion to model units:
  - Empirical C and N percentages converted to 15 cm topsoil equivalents (g m^-2) using horizon depths and bulk densities.
  - Phosphorus data converted from mmol kg^-1 to g m^-2 using molar mass and the same stock calculation approach.
  - For acidic soil, top 15 cm SOC assumed to represent the model topsoil; limestone soil treated as reaching the 15 cm depth.

## Periodicity and timescales
- Empirical data: collected in 2019, after ~24 years of nutrient manipulation.
- Modelling outputs: spans from the onset of widespread N deposition (mid-1800s) to the present; specific plots reference year 2020 for C, N, and P budgets and 1800–2020 for deposition-related changes.

## The N14CP model and calibration
- Model description:
  - N14CP simulates C, N, and P fluxes among plant, topsoil, subsoil, atmosphere, and solution pools with stoichiometric controls and Liebig’s law of the minimum.
  - Calibrates two phosphorus parameters (P Weath0 and P CleaveMax) to match observed data.
  - Implemented in Matlab; inputs include background N deposition, climate data, and plant functional history.
- Outputs used in data files:
  - Modelled C, N, P stocks and budgets; comparisons with empirical data; parameter values; and nutrient treatment responses to N deposition.

## Data files and contents
- Wardlow_empirical_vs_modelled_CNP.csv
  - Comparison of empirical vs. modelled C, N, and P stocks by grassland (Acid/Limestone) and treatment (0N, LN, HN, P); includes Obs, Sim, SE, Diff, and Percent difference.
- Wardlow_mean_CNP_difference.csv
  - Mean differences between simulated and observed values by grassland and nutrient for C, N, P, and AGB_C with SE.
- Wardlow_modelled_P_cleaving.csv
  - P CleaveMax values used by the model and total P cleaved from organic P in 2020 by grassland-treatment.
- Wardlow_modelled_N_deposition.csv
  - Modelled changes in C, N, and P stocks between 1800 and 2020 due to N deposition (0N treatment only); includes Y_1800, Y_2020, Diff, and Per_diff.
- Wardlow_modelled_nutrient_treatments.csv
  - Differences in modelled stocks (C, N, P, AGB_C) across nutrient treatments relative to 0N; includes value, Diff, and Per_diff.
- Wardlow_modelled_CNP_budgets.csv
  - Modelled pool sizes for C, N, and P (e.g., Subsoil_SOC, Topsoil_SOC, Biomass_C, SON, Available_N, Available_P, etc.) used to construct budgets; all values in g m^-2.

## Provenance, references, and lineage
- Key references:
  - Taylor C.R. et al. (accepted) Organic phosphorus cycling may control grassland responses to nitrogen deposition: a long-term field manipulation and modelling study.
  - Davies J.A.C. et al. (2016) Long-term P weathering and recent N deposition control contemporary plant-soil C, N, and P.
  - Horswill P. et al. (2008) Base cation depletion, eutrophication and acidification of species-rich grasslands in response to long-term simulated nitrogen deposition.
  - Morecroft M.D. et al. (1994) Wardlow experimental setup.
- Data are part of the supplementary material for the manuscript and are provided to support model calibration and validation.

## Data quality, completeness, and caveats
- Completeness issue: Total soil phosphorus data were available for only half of the nutrient treatments (control 0N and high N HN); C and N data were collected for all four treatments.
- Data are not raw C and N percentages but model-ready equivalents (topsoil 15 cm, g m^-2), requiring careful interpretation when reusing outside the specific model framework.
- Empirical vs. model comparison highlights discrepancies (documented as differences and percentages) and provides quantitative error metrics (SE).

## Guidance for data reuse and governance
- Use for validating C, N, and P budgets under long-term nutrient manipulations and N deposition scenarios.
- Reproduce model calibration by referring to the two calibrated P parameters (P Weath0, P CleaveMax) and input datasets.
- Ensure awareness of unit conversions and the topsoil depth assumption (15 cm) when comparing to other soil profiles or models.
- Acknowledge incomplete P data and consider this limitation in cross-site or cross-study analyses.
- Maintain traceability to original experiments and references for context and methodological details.