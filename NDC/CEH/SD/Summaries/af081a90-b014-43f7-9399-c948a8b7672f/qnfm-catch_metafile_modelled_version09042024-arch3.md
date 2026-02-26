# Metafile for the QNFM-CATCH dataset ' Simulated 15-min discharge time-series and baseline simulations for the River Kent following a Natural Flood Management intervention of 'Enhanced Hillslope Storage', Sedgewick, October 2015 to January 2016 '

## Overview
- Part of the NERC-funded project "Quantifying the likely magnitude of nature-based flood mitigation effects across large catchments" (Q-NFM; grant NE/R004722/1).
- Objective: quantify flood peak reductions from Natural Flood Management (NFM) features within catchments, here focusing on Enhanced Hillslope Storage (EHS) in the River Kent catchment (209 km2).
- Presents simulated 15-minute discharge time-series for baseline and post-NFM scenarios at Sedgwick gauging station, covering 1 Oct 2015 to 17 Jan 2016 (including Storm Desmond).
- 67 simulated, acceptable baseline time-series are provided for comparison with the post-NFM results; findings discussed in Beven et al. (2022b).

## Data scope and purpose
- Data illustrate the magnitude of flood-peak reductions under a range of events up to an estimated 1-in-500 year return (0.2% exceedance frequency).
- Two datasets provided: baseline (QNFM-CATCH_baseline_datafile.csv) and post-NFM (QNFM-CATCH_ehs_datafile.csv).
- Each dataset contains 15-minute discharge values (m3/s) for 67 unique parameter sets, across the period 01/10/2015 00:00 to 17/01/2016 23:45.

## Data structure and units
- File format: CSV.
- Columns:
  - Index, Description (date and time in 15-minute increments), Units (cubic metres per second, m3/s).
  - 67 subsequent columns corresponding to unique random parameter sets; the column identifiers are unique but carry no intrinsic meaning beyond identity.
- Time coverage includes the Storm Desmond period within the 2015–2016 winter season.

## Modelling and collection methods
- Hydrological model: Dynamic Topmodel (latest version used here, 0.2.1).
- Input rainfall field: derived from a new direction-dependent, topographically controlled interpolation using observed rainfall data for the Cumbrian Mountains.
- Parameter sampling: Monte Carlo sampling of prior parameter distributions, with 100,000 simulated discharge datasets generated for baseline and post-NFM scenarios.
- Calibration/selection process:
  - Step 1: define model and prior parameter ranges.
  - Step 2: apply Limits of Acceptability (2.5–97.5 quantiles of runoff coefficients) with timing constraints.
  - Step 3: evaluate hydrograph steps for additional events (largest flood on record, plus timing constraints ±2 h).
  - Step 4: apply saturation-excess overland flow criterion; reject simulations with <10% of area with surface storage >1 mm at any time.
  - Result: 67 surviving discharge datasets for each scenario.
- NFM implementation: Enhanced Hillslope Storage features distributed across the 209 km2 catchment based on the Working with Natural Processes (WwNP) dataset; each bund feature modeled with a residence time of 10 hours.

## Quality control and data curation
- The final 67 simulations per scenario represent the acceptable subset that meet the predefined fitness-for-purpose criteria (Limits of Acceptability and saturation storage thresholds).
- The approach aims to robustly represent flood-peak reductions under EHS within realistic parameter uncertainty.
- The results are intended to support interpretation and comparison with observational baselines, as discussed in associated Beven et al. works.

## Data sharing, governance, and usage notes
- Datasets are shared as CSV files with clearly defined structure and metadata in the metafile.
- Underlying modelling and interpolation methods are documented and cited (Beven et al. 2022a, 2022b; Hankin et al. 2018; Page et al. 2022).
- The dataset supports assessment of natural flood management effectiveness by comparing baseline and post-NFM discharge time-series for the River Kent.
- The multiparameter approach and explicit data selection criteria exemplify transparent data governance and reproducibility considerations for monitoring-framework-type work.

## References
- Beven, K., Lane, S., Page, T., Hankin, B., Smith, P., and Chappell, N.A. 2022a. On (in)validating environmental models. Part 2: Turing-like test for hydrological processes. Hydrological Processes 36(10): e14703.
- Beven, K., Page, T., Hankin, B., Smith, P., Kretzschmar, A., Mindham, D., and Chappell, N.A. 2022b. Deciding on fitness-for-purpose - of models and of natural flood management. Hydrological Processes 36: e14752.
- Hankin, B., Chappell, N.A., Page, T.J.C., Kipling, K., Whitling, M., and Burgess-Gamble, L. 2018. Mapping the potential for Working with Natural Processes - technical report SC150005/R6. Environment Agency, Bristol. 77p.
- Page, T., Beven, K.J., Hankin, B., and Chappell, N.A. 2022. Interpolation of rainfall observations during extreme rainfall events in complex mountainous terrain. Hydrological Processes 36: e14758.