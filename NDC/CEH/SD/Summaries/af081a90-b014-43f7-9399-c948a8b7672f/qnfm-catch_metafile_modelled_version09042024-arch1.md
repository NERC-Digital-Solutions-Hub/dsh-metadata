# Metafile for the QNFM-CATCH dataset ' Simulated 15-min discharge time-series and baseline simulations for the River Kent following a Natural Flood Management intervention of 'Enhanced Hillslope Storage', Sedgewick, October 2015 to January 2016 '

- Objective and scope
  - Part of the NERC-funded Q-NFM project aiming to quantify flood peak reductions from Nature-based Flood Management (NFM) features across large catchments (1 km2 to >2000 km2).
  - This dataset focuses on one NFM intervention type ('Enhanced Hillslope Storage') applied to the 209 km2 River Kent catchment in Cumbria.
  - Findings discussed in Beven et al. (2022b); 67 simulated time-series are provided for baseline and post-NFM scenarios.

- Data described
  - 15-minute discharge time-series at Sedgwick gauging station (Environment Agency) for 1 Oct 2015 to 17 Jan 2016 (includes Storm Desmond).
  - Observed rainfall field input derived from a new direction-dependent interpolation using Cumbrian Mountains data.
  - Baseline and post-NFM (EHS) simulations produced with Dynamic Topmodel (Lancaster University) version 0.2.1.
  - A wide range of model parameters (Monte Carlo sampling) interpreted through a structured screening process to yield 67 acceptable simulations per scenario.

- Data structure and units
  - Two CSV files: QNFM-CATCH_baseline_datafile.csv and QNFM-CATCH_ehs_datafile.csv.
  - Each file contains:
    - Index, Description (date and time in 15-minute increments from 00:00 01/10/2015 to 23:45 17/01/2016), Units (dd/mm/yyyy hh:mm; Cubic metres per second, m3/s).
    - 67 columns corresponding to unique random parameter sets; column headers are non-meaningful identifiers.
  - Values represent River discharge in m3/s.

- Model implementation and data generation workflow
  - Dynamic Topmodel used as the core distributed catchment model.
  - Process steps:
    1) Select Dynamic Topmodel as the modelling framework.
    2) Establish prior ranges for model parameters (see Table 1 in Beven et al. 2022b).
    3) Monte Carlo sampling: 100,000 simulated discharge datasets per scenario (baseline and post-NFM).
    4) Apply Limits of Acceptability using 2.5–97.5 percentile ranges of runoff coefficients from past events, with timing constraint ±2 h; evaluate across the 2015 period; retain 3,249 datasets per scenario.
    5) Additional evaluation of flood peaks using hydrograph steps from 2005 and 2009; retain 118 datasets per scenario.
    6) Apply saturation-overland-flow criterion: reject simulations where more than 90% of the area has less than 1 mm surface storage at all times; final retention is 67 datasets per scenario.
  - DEM modification to represent Enhanced Hillslope Storage (NFM), based on Hankin et al. 2018 DEM; bund features modelled with a 10-hour residence time (as part of the NFM configuration).
  - Location of EHS features drawn from Working with Natural Processes (WwNP) dataset (Hankin et al. 2018).

- Interpretation and context
  - The final objective is to demonstrate the magnitude of flood peak reductions for events spanning a wide range of return periods, up to an estimated 1-in-500-year event (0.2% exceedance).
  - Results and interpretation detailed in Beven et al. (2022b).

- References and data provenance
  - Beven, K., Lane, S., Page, T., Hankin, B., Smith, P., and Chappell, N.A. 2022a. On (in)validating environmental models. Hydrological Processes 36(10): e14703.
  - Beven, K., Page, T., Hankin, B., Smith, P., Kretzschmar, A., Mindham, D., and Chappell, N. A. 2022b. Deciding on fitness-for-purpose - of models and of natural flood management. Hydrological Processes 36: e14752.
  - Hankin, B., Chappell, N.A., Page, T.J.C., Kipling, K., Whitling, M., and Burgess-Gamble, L. 2018. Mapping the potential for Working with Natural Processes - technical report SC150005/R6. Environment Agency, Bristol.
  - Page, T., Beven, K.J., Hankin, B., and Chappell, N.A. 2022. Interpolation of rainfall observations during extreme rainfall events in complex mountainous terrain. Hydrological Processes 36: e14758.
- Data accessibility
  - Source data includes Sedgwick EA/NRFA gauging data; rainfall input derived for the modelling; dynamic Topmodel implemented via the dynatop R package (v0.2.1).

- Practical relevance for analysts
  - Provides a ready-to-analyze, time-aligned set of baseline and NFM-disrupted discharge simulations with clear documentation of filtering criteria and parameter-space filtering.
  - Enables assessment of flood-peak reduction magnitude across a range of plausible parameterizations and extreme rainfall scenarios.
  - Facilitates replication and cross-dataset comparison through explicit data structure, metadata, and provenance.