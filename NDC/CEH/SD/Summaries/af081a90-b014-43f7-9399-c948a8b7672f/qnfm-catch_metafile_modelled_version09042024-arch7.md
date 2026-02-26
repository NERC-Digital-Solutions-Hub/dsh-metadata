# Metafile for the QNFM-CATCH dataset ' Simulated 15-min discharge time-series and baseline simulations for the River Kent following a Natural Flood Management intervention of 'Enhanced Hillslope Storage', Sedgewick, October 2015 to January 2016 '

## Overview
- Purpose: quantify flood peak reductions from Natural Flood Management (NFM) features in large catchments, demonstrated for the River Kent (209 km²) using 15-minute discharge data at Sedgwick; period 01 Oct 2015 – 17 Jan 2016 (includes Storm Desmond).
- Datasets: baseline (QNFM-CATCH_baseline_datafile.csv) and post-NFM (QNFM-CATCH_ehs_datafile.csv) time-series, each with 67 surviving parameter-set simulations.
- Scope: 67 simulated discharge time-series per scenario, plus metadata for model runs; results support interpretation of flood peak reductions and ranges of return periods up to 1-in-500 years.
- Context: derived from NERC Q-NFM project; findings discussed in Beven et al. (2022b).

## Data content and structure
- Time axis: 15-minute intervals from 00:00 01/10/2015 to 23:45 17/01/2016.
- Data format: CSV with columns
  - Index: date and time (dd/mm/yyyy hh:mm)
  - Description: River discharge
  - Units: m³/s
  - 67 columns: unique identifiers for each random parameter set (values are identifiers only, not meaningful beyond uniqueness)
- Datasets:
  - Baseline: simulate pre-intervention discharge time-series
  - Post-NFM (Enhanced Hillslope Storage): simulate discharge with distributed hillslope storage features
- Spatial and input context:
  - Observed discharge at EA Sedgwick gauge (Sedgwick) used for calibration/validation
  - Rainfall input field derived from topographically controlled interpolation over Cumbrian Mountains
  - DEM-based representation of NFM features (bunds) across the 209 km² catchment
  - NFM features locations based on Working with Natural Processes (WwNP) dataset; each bund has a 10-hour residence time
- Purpose of results: demonstrate magnitude of flood peak reductions across a range of events, including up to a 1-in-500-year return period.

## Data generation and quality control
- Model: Lancaster Dynamic Topmodel (v0.2.1) used to generate discharge time-series.
- Parameter sampling: Monte Carlo approach with 100,000 simulations; initial prior ranges defined (see Beven et al. 2022b).
- Acceptance criteria:
  - Step 4: Limits of Acceptability (2.5–97.5% quantiles of runoff-coefficient distributions) with timing constraint ±2 h; 3,249 simulations pass.
  - Step 5: additional evaluation using 2005 and 2009 events; 118 pass.
  - Step 6: saturation-excess overland flow area < 10% at any time step; 67 pass.
- Output: two final datasets, each containing 67 viable discharge time-series corresponding to accepted parameter sets.
- Data provenance: model inputs and acceptance criteria described in Beven et al. (2022a, 2022b); DEM and bund locations based on Hankin et al. (2018) and related Beven et al. work.

## How GIS specialists can use
- Compare baseline vs. post-NFM time-series to quantify flood-peak reductions across parameter sets and events.
- Compute statistics such as delta discharge, peak reduction, and return-period implications for policy or planning analyses.
- Integrate with GIS layers:
  - 209 km² catchment boundary and hillslope bund footprints (from DEM and WwNP data)
  - 15-minute time-series can be linked to rainfall and elevation layers for targeted analyses or visualization.
- Use as a data source for hydrograph-based mapping and scenario visualization, while acknowledging uncertainty from the 67 surviving parameter sets.

## Provenance and references
- Data source: River Kent discharge at Sedgwick; period includes Storm Desmond.
- Rainfall input interpolation: Page et al. (2022).
- DEM-based NFM representation: Hankin et al. (2018).
- NFM feature modelling: Enhanced Hillslope Storage (Beven et al. 2022b).
- Validation and interpretation context: Beven et al. (2022a, 2022b); Beven et al. (2022b) for flood-peak reduction interpretation.
- Related technical background: Dynamic Topmodel (Lancaster) and associated methodological steps.