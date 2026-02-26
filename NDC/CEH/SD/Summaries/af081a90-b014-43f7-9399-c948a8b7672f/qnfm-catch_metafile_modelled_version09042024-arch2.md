# Metafile for the QNFM-CATCH dataset ' Simulated 15-min discharge time-series and baseline simulations for the River Kent following a Natural Flood Management intervention of 'Enhanced Hillslope Storage', Sedgewick, October 2015 to January 2016 '

## Aim and context
- Part of the NERC-funded Q-NFM project to quantify potential flood peak reductions from nature-based flood mitigation across large catchments (1 km2 to >2,000 km2).
- Focuses on one NFM intervention type (Enhanced Hillslope Storage, EHS) in the River Kent catchment (209 km2) with simulated results for baseline and post-NFM scenarios.
- Results are intended to inform understanding of flood peak reductions and are discussed in Beven et al. (2022b).

## Data and modeling approach
- Observed data: 15-minute discharge at the Environment Agency Sedgwick gauge for 1 Oct 2015 to 17 Jan 2016 (includes Storm Desmond).
- Hydrological model: Lancaster University Dynamic Topmodel (latest version at the time, v0.2.1).
- Rainfall input: direction-dependent, topographically controlled interpolation using observed rainfall data for the Cumbrian Mountains (Page et al., 2022).
- Parameter sampling: Monte Carlo approach with 100,000 simulated datasets using an initial wide parameter space; filtering via Limits of Acceptability (LoA) to retain plausible simulations.
- NFM representation: EHS features modeled via a modified DEM based on Hankin et al. (2018), representing bunds on hillslopes; EHS residence time set to 10 hours.
- Interpretive framework: The resulting simulations are used to assess flood peak reductions across events with a range of return periods up to ~1-in-500-year (0.2% exceedance).

## Data structure and content
- Two CSV datasets:
  - QNFM-CATCH_baseline_datafile.csv (baseline scenario)
  - QNFM-CATCH_ehs_datafile.csv (post-NFM scenario)
- Data format:
  - Index, Description = date and time (15-minute increments) from 00:00 01/10/2015 to 23:45 17/01/2016.
  - Units = m3/s.
  - Columns: 67 columns corresponding to unique identifiers for each random parameter set; the identifiers are purely unique and carry no inherent meaning.
  - Each row represents a time step; each column contains the simulated river discharge for a given parameter set.
- Purpose: present 67 “acceptable” baseline and 67 corresponding post-NFM time-series after filtering.

## Collection, generation, and quality control
- Simulation workflow (Dynamic Topmodel v0.2.1):
  - Step 1: Select model (Dynamic Topmodel).
  - Step 2: Establish prior parameter ranges (see Beven et al. 2022b, Table 1).
  - Step 3: Monte Carlo sampling to produce 100,000 datasets for baseline and post-intervention.
  - Step 4: Apply Limits of Acceptability to hydrograph steps using 2.5 to 97.5 percentile runoff coefficients and timing constraints within ±2 hours, retaining 3,249 datasets per scenario.
  - Step 5: Additional evaluation using 2005 and 2009 floods (LoA criteria), retaining 118 datasets per scenario.
  - Step 6: Filter by saturation excess overland flow; require less than 10% area with surface storage >1 mm at any time step, yielding 67 surviving river discharge datasets per scenario.
- Data sources and features:
  - EHS locations informed by Working with Natural Processes (WwNP) dataset (Hankin et al., 2018).
  - Each modeled bund feature has a 10-hour residence time in the simulations.
- Documentation and references:
  - Beven et al. 2022a, 2022b; Hankin et al. 2018; Page et al. 2022 provide methodological and data sources.

## How to use and interpret
- The two datasets allow direct comparison of baseline vs post-NFM flood peaks for 67 parameter realizations across Oct 2015–Jan 2016, including the 1-in-500-year scale.
- Use the dataset for assessing potential magnitude of flood peak reductions due to Enhanced Hillslope Storage within the River Kent catchment.
- Interpretations and broader conclusions are discussed in Beven et al. (2022b).

## Remarks and references
- The results are tied to the NERC project “Quantifying the likely magnitude of nature-based flood mitigation effects across large catchments” (QNFM).
- Key references:
  - Beven, K., Lane, S., Page, T., Hankin, B., Smith, P. & Chappell, N.A. 2022a. On (in)validating environmental models. Hydrological Processes.
  - Beven, K., Page, T., Hankin, B., Smith, P., Kretzschmar, A., Mindham, D., & Chappell, N. A. 2022b. Deciding on fitness-for-purpose - of models and of natural flood management. Hydrological Processes.
  - Hankin, B., et al. 2018. Mapping the potential for Working with Natural Processes - technical report SC150005/R6.
  - Page, T., Beven, K.J., Hankin, B., & Chappell, N.A. 2022. Interpolation of rainfall observations during extreme rainfall events in complex mountainous terrain. Hydrological Processes.