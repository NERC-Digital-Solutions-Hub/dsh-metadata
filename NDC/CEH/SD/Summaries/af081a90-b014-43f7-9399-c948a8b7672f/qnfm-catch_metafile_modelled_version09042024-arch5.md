# Metafile for the QNFM-CATCH dataset ' Simulated 15-min discharge time-series and baseline simulations for the River Kent following a Natural Flood Management intervention of 'Enhanced Hillslope Storage', Sedgewick, October 2015 to January 2016 '

## Overview
- Describes a NERC-funded project (Q-NFM) aimed at quantifying flood peak reductions from Natural Flood Management (NFM) interventions, applied to the River Kent catchment (209 km2) using Enhanced Hillslope Storage (EHS).
- Provides 67 simulated 15-minute river discharge time-series for both a baseline scenario and a post-NFM (EHS) scenario, covering 1 Oct 2015 to 17 Jan 2016 (includes Storm Desmond).
- Results interpreted in Beven et al. (2022b); all 67 time-series pertain to the same observation period with two scenario sets.

## Data structure and contents
- Observed data: 15-minute discharge at the Environment Agency Sedgwick gauging station.
- Modelling: Dynamic Topmodel (Lancaster University) with a rainfall field derived from a direction-dependent, topographically controlled interpolation (Page et al., 2022).
- Dataset files:
  - QNFM-CATCH_baseline_datafile.csv
  - QNFM-CATCH_ehs_datafile.csv
- CSV format:
  - Index: date and time in 15-minute increments (00:00:00 01/10/2015 to 23:45:00 17/01/2016).
  - Description: "River discharge".
  - Units: m3/s.
  - 67 data columns: unique identifiers for each random parameter set; these IDs are placeholders with no intrinsic meaning beyond identifiability.
  - Each row corresponds to a 15-minute time step; each of the 67 columns contains the discharge value for that parameter set.
- Time window includes the Storm Desmond period.

## Modelling and data generation workflow
- Model version: Dynamic Topmodel (v0.2.1), publicly available via CRAN (dynatop package).
- Parameter sampling workflow (Condition Tree Approach):
  1) Select Dynamic Topmodel as the modelling framework.
  2) Establish a prior range of model parameters (see Beven et al., 2022b, Table 1).
  3) Monte Carlo sampling of prior parameter distributions, yielding 100,000 simulated discharge datasets per scenario (baseline and post-NFM).
  4) Apply Limits of Acceptability (LOA) using 2.5–97.5 percentile ranges of runoff coefficients from past events, plus a ±2 h timing constraint; rank hydrograph time steps for the 2015 period. This preserved 3,249 datasets per scenario.
  5) Additional LOA evaluation using hydrograph steps from 2005 and 2009; this reduced to 118 datasets per scenario.
  6) Saturation excess evaluation: discard simulations with less than 10% of the area having surface storage >1 mm at any time step; final retention is 67 datasets per scenario.
- NFM scenario specifics: Enhanced Hillslope Storage locations determined from the WwNP dataset (Hankin et al., 2018); each bund feature modeled with a 10-hour residence time.

## Data provenance and references
- Beven, K., Lane, S., Page, T., Hankin, B., Smith, P., and Chappell, N.A. 2022a. On (in)validating environmental models. Part 2: Turing-like tests for hydrological processes.
- Beven, K., Page, T., Hankin, B., Smith, P., Kretzschmar, A., Mindham, D., and Chappell, N.A. 2022b. Deciding on fitness-for-purpose — of models and of natural flood management.
- Hankin, B., Chappell, N.A., Page, T.J.C., Kipling, K., Whitling, M., and Burgess-Gamble, L. 2018. Mapping the potential for Working with Natural Processes – technical report SC150005/R6.
- Page, T., Beven, K.J., Hankin, B., and Chappell, N.A. 2022. Interpolation of rainfall observations during extreme rainfall events in complex mountainous terrain.
- The modelling aims and interpretation of results are discussed in Beven et al. (2022b).

## Data governance and quality considerations for Data Stewards
- Clear provenance: links to modelling approach, dataset scope, and supporting literature for validation and interpretation.
- Standardized data format: two CSV files with consistent time indexing, units, and 15-minute resolution; metadata fields explicitly describe time, description, and units.
- Reproducibility: detailed modelling pipeline (Monte Carlo sampling, LOA criteria, and saturation checks) allows replication and auditing of the 67 surviving scenarios.
- Metadata and discoverability: filenames and column headers are designed to identify parameter-set results; however, the 67 IDs are non-descriptive and would benefit from a separate, persistent mapping table to improve interpretability.
- Interoperability: model version and input data sources are cited; the rainfall field interpolation method and DEM adjustments for EHS are documented to support cross-dataset comparisons.
- Data stewardship considerations:
  - Ensure availability of the two CSV datasets with clear documentation of the 67 parameter IDs (mapping table recommended).
  - Maintain links to the modelling software (Dynamic Topmodel v0.2.1) and the input datasets (rainfall interpolation method, WwNP dataset for EHS features).
  - Archive supporting references and Beven et al. papers to aid users in interpretation of the results and limitations.
  - Note the interpretation caveat: results pertain to a single catchment, a specific NFM intervention type, and a finite set of acceptable model realizations; applicability to other settings requires careful validation.

## Practical implications for use
- Useful for illustrating potential flood peak reductions due to a specific NFM intervention within a defined catchment and time window.
- Provides a reproducible, QA-filtered set of model realizations suitable for impact assessment and methodological benchmarking.
- Appropriate for data discovery, citation-backed reuse, and integration with related datasets in hydrological modelling and NFM evaluation efforts.