# Supporting documentation for data: 'Empirical and modelled carbon, nitrogen and phosphorus content of plants and soils from Wardlow Hay Cop, UK'

## Overview
- Provides supporting data for Taylor et al. (2021) Biogeosciences, including empirical measurements and model outputs used to calibrate the N14CP mechanistic C, N and P cycling model.
- Datasets include empirical soil C, N stocks and P data from Wardlow Hay Cop and modelled equivalents, along with comparisons, budgets, and parameter calibrations.
- Most data are model outputs derived from calibrating phosphorus cycling parameters; primary use is to reproduce figures and assess model performance.

## The Wardlow experimental context
- Wardlow Hay Cop is a long-term nutrient manipulation experiment in two grassland types (limestone and acidic) established in the mid-1990s in Derbyshire, UK.
- Treatments: 0N (control), LN (low N), HN (high N), and P (phosphorus addition).
- Treatments applied monthly (1995) and bi-monthly (2017 onwards); replicated across three blocks (A, B, C).
- Sampling: six soil cores per grassland-treatment combination; depths 10 cm (limestone) and 20 cm (acidic); soil cores split into organic and mineral horizons for C and N analyses; P data from 2003 study (Horswill et al., 2008).

## Data types, units, and conversion
- Empirical data collected in 2019 (C and N) and 2003 for P; used to calibrate the C, N and P model.
- Raw empirical data are converted to model-compatible topsoil units (15 cm depth) and expressed in g m^-2:
  - SOC, SON, and total phosphorus stocks converted from % and mmol kg^-1 to g m^-2 using horizon depths and bulk density.
  - For the acidic soil (20 cm), estimates adjusted to represent a 15 cm model topsoil depth.
- P data for the empirical set are partially incomplete: total soil P data available for only half of the nutrient treatments (0N and HN missing).

## The N14CP model
- A mechanistic model of C, N and P cycling across plants, topsoil, subsoil, atmosphere, and solution/leachate pools.
- Uses Liebig’s law of the minimum with some N–P interaction mechanisms.
- Inputs include background N deposition, climate (temperature, precipitation), and plant functional type history (land-use history analogue).
- Calibration targets: two phosphorus cycling parameters—P_Weath0 (inorganic P availability) and P_CleaveMax (organic P access).
- Implementation: MATLAB; outputs used to generate figures in the manuscript.

## Data files and contents
- Wardlow_empirical_vs_modelled_CNP.csv
  - Compares empirical vs. modelled C, N, and P stocks by grassland (Acid/Limestone) and treatment (0N, LN, HN, P); includes Obs, Sim, Diff, and Percent differences; related to Figure 2.
- Wardlow_mean_CNP_difference.csv
  - Mean differences between simulated and observed data across treatments with SE.
- Wardlow_modelled_P_cleaving.csv
  - P_CleaveMax values used per grassland-treatment and P_Cleaved_2020 totals (P cleaved from organic P) for 2020.
- Wardlow_modelled_N_deposition.csv
  - Modelled effects of N deposition (1800–2020) on C, N, and P pools; notes changes for 0N treatment only (Figure 4 context).
- Wardlow_modelled_nutrient_treatments.csv
  - Differences in modelled C, N and P stocks across nutrient treatments relative to 0N; post-1995 time-series context (after dashed line on axis).
- Wardlow_modelled_CNP_budgets.csv
  - Modelled pool sizes used to construct C, N and P budgets; includes subsoil/topsoil SOC, SON, available/fixed N, biomass carbon/nitrogen, weatherable/sorbed P pools, SOP/sorbed P, available P, and biomass P.
- References and provenance notes accompany each file, linking to the study and model descriptions (Taylor et al. accepted 2021; Davies et al. 2016 for N14CP; Horswill et al. 2008; Morecroft et al. 1994).

## Completeness and limitations
- Completeness: C and N data collected for all four nutrient treatments across both grasslands; P data available for only half of the treatments (0N and HN missing).
- Data are largely model-derived outputs calibrated to empirical data; empirical data are used to validate and compare model predictions.

## Usage and provenance
- Data intended to support figures and model calibration for Wardlow C, N and P dynamics under long-term N deposition and nutrient manipulations.
- Data collectors: Christopher Taylor (PhD student), with supervision from Gareth Phoenix and Jessica Davies.
- Primary references:
  - Taylor et al. (2021) Biogeosciences (accepted, DOI not yet available)
  - Davies et al. (2016) Global Biogeochemical Cycles (N14CP model)
  - Horswill et al. (2008) Environmental Pollution (P data source)
  - Morecroft et al. (1994) Journal of Ecology (Wardlow experimental setup)

## Contact and related materials
- Supporting materials accompany the manuscript and provide direct access to CSV data files and their associated figure references (e.g., figures 2, 4, and 5).