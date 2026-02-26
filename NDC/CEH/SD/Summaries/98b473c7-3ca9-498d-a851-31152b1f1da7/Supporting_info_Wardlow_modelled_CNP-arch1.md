# Supporting documentation for data: 'Empirical and modelled carbon, nitrogen and phosphorus content of plants and soils from Wardlow Hay Cop, UK'

## Overview
- Supplementary datasets for Taylor et al. (2021) Biogeosciences; empirical data to calibrate a C, N and P cycling model (N14CP) for Wardlow Hay Cop.
- Empirical data include soil organic carbon (SOC), total nitrogen (SON), and total phosphorus (P) stocks from two grasslands; used to calibrate the model.
- Wardlow is a long-term nutrient manipulation experiment in Derbyshire, UK, with two grassland types (lime-stone and acidic).
- Depths: 10 cm (limestone) and 20 cm (acidic) for C and N analyses; P data from 2003.
- Data are converted into model-compatible units (g m^-2) for a model topsoil depth of 15 cm.
- Model outputs are primarily modelled data, calibrated using empirical data; includes comparisons between empirical and modelled estimates.

## Empirical data
- New empirical estimates of SOC and SON stocks for Wardlow Hay Cop soils from two grasslands (acidic and limestone).
- Wardlow long-term nutrient manipulation experiment established in the mid-1990s.
- Four nutrient treatments: 0N (control), LN (low N), HN (high N), and P (phosphorus).
- Nutrient additions: NH4NO3 for N; NaH2PO4·H2O for P; monthly additions (1995–2017), bi-monthly since 2017.
- Phosphorus data from Horswill et al. (2008) incorporated into the model.
- Sampling and analysis conducted in 2019; P data from 2003.

## Brief methodology
- Soil cores collected from 3 experimental blocks, across 4 treatments (0N, LN, HN, P).
- Bulk density cores taken; organic/mineral horizon depths recorded for stock estimation.
- Samples processed: sieved, dried, ground; inorganic carbon removed with acid; C and N measured by isotope ratio mass spectrometry (IRMS).
- Plant-available and related pools derived in modelling steps.

## Purpose of data collection
- Assess effects of long-term nutrient treatment on SOC and SON stocks.
- Inform and calibrate a mechanistic C, N and P cycling model (N14CP) to simulate carbon and nutrient dynamics at Wardlow.

## Periodicity of data
- Empirical data collected in 2019 (after ~24 years of treatment).
- Modelling spans longer timescales (from the Holocene onward); model outputs for 2020 C, N and P budgets.

## Data collector
- Christopher Taylor (PhD student), under supervision of Gareth Phoenix and Jessica Davies (University of Sheffield and Lancaster University).

## Completeness
- Complete C and N data for all four treatments.
- Phosphorus data available for only half of the nutrient treatments: 0N (control) and HN (high nitrogen) are specified; other P data are missing due to resource/time limitations.

## Modelled data
- Most data are model outputs derived from empirical data to calibrate two phosphorus cycling parameters (P Weath0 and P CleaveMax).
- Model outputs include: modelled SOC, SON, and P stocks; comparisons with empirical data; calibrated parameters; modelled C, N and P budgets across treatments; and responses to N deposition and nutrient manipulation.
- Model developed in Matlab.

## The Wardlow grasslands
- Wardlow hay cop long-term nutrient manipulation experiment with two co-located grassland types: acidic and limestone.
- Established in 1990 to study effects of atmospheric N deposition.
- Treatments replicated within Wardlow: 0N, LN, HN, and P.
- Nutrient additions are quarterly in the model timescale; annual N and P inputs equivalent across treatments.

## Details of sampling / observation locations
- 6 soil cores per grassland-treatment per block (0N, LN, HN, P).
- 3 blocks (A, B, C); limestone sampled to 10 cm; acidic to 20 cm; cores divided into organic and mineral horizons.
- Fresh soil stored in a cold room; analysed within months for organic C and total N.

## Conversion of empirical to modelled SOC and total N and P
- Empirical data converted to model topsoil units (15 cm depth) expressed as g m^-2.
- Conversion uses horizon mass (via depth × bulk density), scaling from % C and % N to g m^-2; P data converted from mmol kg^-1 to g m^-2 via molar mass and similar depth-based conversion.
- Limestone SOC applied to whole model topsoil depth (15 cm); acidic soil adjusted to represent the top 15 cm by distributing the 10 cm organic horizon mass accordingly.

## The N14CP model
- Mechanistic model of C, N and P cycling among plant, soil (topsoil/subsoil), atmosphere, and solution/leachate pools.
- Stoichiometric relationships and Liebig’s law of the minimum govern flows; includes some N–P interaction mechanisms.
- Input drivers: background N deposition, climate (temp and precip), and plant functional history (land-use history analogue).
- Calibration focuses on two phosphorus cycling parameters: P Weath0 (inorganic P availability) and P CleaveMax (organic P access).
- Outputs represent the best-guess C, N and P pools and their responses to N deposition and nutrient treatments.
- Implemented in Matlab; figures produced in Matlab.

## Data files
- Wardlow_empirical_vs_modelled_CNP.csv: Comparison of empirical vs. modelled C, N, P stocks; includes observed (Obs) and simulated (Sim) values with differences.
  - Contents distinguish between grassland type (Acid/Limestone), nutrient treatment (0N, LN, HN, P).
- Wardlow_mean_CNP_difference.csv: Mean differences between simulated and observed data across treatments; includes standard error.
- Wardlow_modelled_P_cleaving.csv: P CleaveMax used by the model and total P cleaved in 2020 by grassland-treatment.
- Wardlow_modelled_N_deposition.csv: Modelled effects of N deposition (1800–2020) on C, N, P pools for 0N treatment.
- Wardlow_modelled_nutrient_treatments.csv: Differences in modelled C, N, P stocks across nutrient treatments relative to 0N; data after 1995.
- Wardlow_modelled_CNP_budgets.csv: Modelled pool sizes for budgets (Subsoil_SOC, Topsoil_SOC, Biomass_C, Subsoil_SON, Topsoil_SON, Available_N, Fixed_N, Biomass_N, Weatherable_P, Subsoil_sorbed_P, Subsoil_SOP, Topsoil_sorbed_P, Topsoil_SOP, Available_P, Biomass_P).

## References
- Taylor C. R. et al. (accepted). Organic phosphorus cycling may control grassland responses to nitrogen deposition: a long-term field manipulation and modelling study. Biogeosciences.
- N14CP model description: Davies et al. (2016), Global Biogeochemical Cycles.
- Empirical data sources: Horswill et al. (2008); Morecroft et al. (1994). Wardlow experimental setup details.