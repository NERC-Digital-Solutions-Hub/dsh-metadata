# Supporting documentation for data: 'Empirical and modelled carbon, nitrogen and phosphorus content of plants and soils from Wardlow Hay Cop, UK'

## Overview
- Presents datasets accompanying Taylor et al. (2021) Biogeosciences on organic phosphorus cycling and grassland responses to nitrogen deposition.
- Empirical data include soil organic carbon (SOC) and total nitrogen (SON) stocks from Wardlow Hay Cop, a long-term nutrient manipulation experiment in two grassland types (limestone and acidic) in Derbyshire, UK.
- Phosphorus data (from Horswill et al. 2008) used to initialize the model.
- Data are used to calibrate and drive the N14CP mechanistic C, N, and P cycling model and to generate figures in the manuscript (e.g., 2020 stocks, 1800–present timelines).

## Empirical data and sampling
- Sampling depths: 10 cm (limestone) and 20 cm (acidic) for C and N analyses.
- Phosphorus data were collected in 2003 (not newly collected here).
- Soil cores collected from all three experimental blocks across four nutrient treatments: 0N (control), LN (low N), HN (high N), and P (phosphorus).
- Bulk density cores collected to estimate stocks; samples processed to remove inorganic carbon, ground, and analysed with isotope ratio mass spectrometry (IRMS) for C and N.
- Data collected in 2019 after ~24 years of treatment; P data are from earlier work (2003).

## Conversion to model-compatible data
- Empirical C and N data converted from percent and % N to model-equivalent topsoil stocks (g m^-2) for a 15 cm model topsoil depth.
- Conversion uses horizon depths, bulk density, and IRMS-derived C and N percentages; P data converted from mmol kg^-1 to g m^-2 using molecular weights and the same topsoil approach.
- Limestone topsoil treated as representative of whole model topsoil; acidic soil (sampled to 20 cm) adjusted to estimate the 15 cm topsoil equivalent.

## The N14CP model
- A mechanistic C, N, and P cycling model simulating fluxes among plants, soil (top and subsoil), atmosphere, and solution/leachate.
- Uses stoichiometric C:N:P relationships and Liebig’s law of the minimum; includes some N–P interaction mechanisms.
- Inputs include background N deposition, climate (temperature and precipitation), and plant functional history.
- Phosphorus cycling parameters calibrated to empirical data: P Weath0 (inorganic P availability) and P CleaveMax (organic P access).
- Model implementation: MATLAB.
- Outputs represent best-guess C, N, and P pools and their responses to N deposition and experimental treatments.

## Data files (CSV) and what they contain
- Wardlow_empirical_vs_modelled_CNP.csv
  - Figure 2 comparison of empirical vs modelled C, N, and P stocks; includes Obs, Sim, SE, Diff, and Percent differences.
- Wardlow_mean_CNP_difference.csv
  - Mean difference between simulated and observed data across nutrient treatments with SE.
- Wardlow_modelled_P_cleaving.csv
  - P CleaveMax values used by the model and total P cleaved in 2020 (g m^-2).
- Wardlow_modelled_N_deposition.csv
  - Effects of simulated N deposition (1800–2020) on C, N, P pools and AGB_C for 0N treatment; includes Y_1800, Y_2020, Diff, Per_diff.
- Wardlow_modelled_nutrient_treatments.csv
  - Differences in modelled C, N, P stocks among nutrient treatments relative to 0N (LN, HN, P) with Diff and Per_diff.
- Wardlow_modelled_CNP_budgets.csv
  - Modelled pool sizes used to construct C, N, P budgets (Topsoil/ Subsoil SOC, SON; Biomass_C/N; Available/Fixed N; Weatherable P; Sorbed and Organic P in topsoil/subsoil; Biomass P; etc.).

## Wardlow grasslands and experimental design
- Two grassland types: acidic and limestone, co-located and part of the Wardlow Hay Cop long-term nutrient manipulation experiment (established in 1990).
- Treatments replicated across three blocks (A, B, C) with six cores per grassland-treatment block.
- Treatments: 0N (control), LN (low N), HN (high N), and P (phosphorus); nitrogen supplied as NH4NO3 and phosphorus as NaH2PO4.H2O; additions occur quarterly (annual totals correspond).
- Historical context: Morecroft et al. (1994) detailed the experimental setup; 0N represents background deposition only.

## Model calibration and data provenance
- The N14CP model description and calibration approach are documented in Davies et al. (2016) and the Taylor et al. (2021) study.
- Empirical data used to calibrate phosphorus cycling parameters (P Weath0 and P CleaveMax) to reproduce observed C, N, and P dynamics under N deposition and nutrient treatments.

## Completeness and limitations
- Phosphorus data: available for only half of the nutrient treatments (0N and HN); other P data not collected for all treatments in this dataset.
- Carbon and nitrogen data: collected for all four nutrient treatments.
- Acknowledges limitations in empirical P data and notes that model outputs are calibrated to available data to provide best-guess estimates of Wardlow’s C, N, and P pools and their responses.

## Relevance for environmental monitoring and data reuse
- Demonstrates a standardized approach to converting empirical soil C, N, and P data into model-compatible formats for long-term ecological monitoring.
- Provides an integrated dataset linking field measurements with mechanistic modelling to assess responses to nutrient deposition and management practices.
- The accompanying files enable reproducibility, model validation, and cross-site comparisons when combined with similar monitoring datasets.
- Highlights the value of making underlying data accessible to support transparency and reuse in policy-relevant environmental health and nutrient cycling analyses.