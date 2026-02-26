# Soil organic matter fractions

## Overview
- SOM is heterogeneous, comprising pools with different residence times.
- The study uses density fractionation to separate SOM into discrete pools: DOC, LF, OF, and MAOM, with DOC and OF discarded for analysis; LF and MAOM analysed for carbon and nitrogen.
- OF is derived by mass balance from the remaining fractions.
- Aims align with modelling SOM turnover and stabilization mechanisms (association with minerals, aggregation, litter sources).

## Background and Survey context
- UKCEH Countryside Survey provides a rolling national assessment of soil and vegetation since 1978, with a new rolling program from 2019–2023 supported by UK-SCAPE (NERC).
- Design: 500 x 1-km squares over five years; 100 squares visited annually; squares excluded if urban >75% or sea >90%.
- Objective: detect changes in soil condition and function at national scale; topsoil condition measurements co-located with vegetation assessments.
- This study focuses on soil metrics, particularly SOM fractions, within the rolling framework.

## Sampling design and field procedures
- Random stratified sampling within the Land Classification of Great Britain; 1-km squares selected; 100 visited per year.
- Within each square, up to 5 randomly dispersed X-Plots for topsoil sampling.
- Archived soil materials: 100 samples subjected to density fractionation in spring 2022.
- Core method: 15 cm black plastic core, soil collected concurrent with vegetation surveys.

## Laboratory methods and fractionation
- Loss-on-Ignition (LOI), hygroscopic water, and CaCO3 content determined by Thermo-Gravimetric Analysis (TGA) with staged heating (25–1000°C).
  - Hygroscopic moisture content calculation from weight loss at 105°C.
  - SOM content derived from weight loss between 105°C and 375°C; calculations convert LOI to SOM (g per g or %).
  - Calcite-C content derived from weight losses between 650°C and 1000°C; corrected to obtain carbonate-C fraction.
- SOM density fractionation (LF and MAOM) using sodium polytungstate (SPT) density separation (1.8 g cm-3).
  - LF: filtration of supernatant after density separation; dried to weigh LF fraction.
  - OF: obtained by processing the pellet via ultrasonic disruption and separation steps; discarded fraction is used to compute OF-C and OF-N by difference.
  - MAOM: remaining pellet treated to remove SPT, dried to weigh MAOM fraction.
- Carbon and nitrogen analysis: Total C and N measured on LF, MAOM, and archived bulk soil using Elementar analyzer (SOP3102, UKAS-accredited) at UKCEH Lancaster.
- Quality controls: two internal standards per batch and 10% replicated samples to ensure accuracy/precision.

## Data structure and composition
- Dataset consists of 13 columns and 101 rows; records include year, square ID, and fraction metrics.
- Key fractions and metrics:
  - LF_C_gperg, MAOM_C_gperg, OF_C_gperg, POM_C_gperg (carbon fractions for LF, MAOM, occluded, and particulate organic matter)
  - LF_N_gperg, MAOM_N_gperg, OF_N_gperg, POM_N_gperg (nitrogen fractions)
  - SOC_gperg (soil organic carbon corrected for calcite-C)
  - TN_gperg (total soil nitrogen)
  - SOM_gperg (som content by LOI)
- Calculations and corrections:
  - SOC calculated as total carbon minus calcite-C; hygroscopic water corrections applied to LF, MAOM, SOC, etc.
  - POM_C and POM_N derived as LF + OF (with OF-C and OF-N set to zero if negative due to measurement uncertainty before summation).
  - OF-C and OF-N derived as total SOC minus LF-C and MAOM-C; OF corrections ensured non-negative values.
  - Fractions are expressed per g soil or g per g soil, as specified.
- Data provenance:
  - Related publications include topsoil physico-chemical properties from the UKCEH Countryside Survey (2018–2019, 2020), with associated data portals.
  - Funding: UK-SCAPE (NERC) and AI4SoilHealth project support.

## Key considerations for analysts
- Data quality and harmonization:
  - Calculations include corrections for hygroscopic water and calcite-C content; uncertainties handled by setting negative OF values to zero.
  - Robust QC via internal standards and replicates; analysis follows UKAS-accredited SOP3102.
- Scale and design implications:
  - Rolling five-year survey with annual sampling permits assessment of spatial and temporal changes at national scale; some squares are excluded due to urban/sea coverage.
- Applicability:
  - Data enable analysis of carbon and nitrogen distribution across LF and MAOM pools, contributing to understanding of SOM stabilization and turnover in GB soils.
- Data accessibility:
  - Data and related topline publications are cataloged in national data centres (e.g., NERC EDS EIDC) for reuse and modelling purposes.