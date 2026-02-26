# Supporting information for Hydrological modelling simulation data for the River Trent Data

## Overview
- Describes the data structure for hydrological model outputs related to hydroclimatic impacts on low-carbon CCS electricity generation.
- Authors and affiliations: Byers, Leathard, O'Donnell, Hall, Amezaga (Newcastle University) and Hall (Oxford University).

## Experimental design
- Model: 8-parameter hydrological model based on the Ph.D. work of A. Leathard; set up and calibrated with Colwick, River Trent station 28009 data.
- Uncertainty analysis: Structural uncertainty and calibration uncertainty explored by simulating 10,000 parameterisations via Latin hypercube sampling.
- Performance metrics: 4-metric ranking using: (i) log-transformed Nash-Sutcliffe Efficiency and (ii–iv) absolute differences between observed and simulated for Q90, Q95, and Q99 percentile flows.
- Simulation setup: Runs with UKCP09 Weather Generator timeseries.
  - 100 samples per scenario.
  - 3 emissions scenarios: Low, Medium, High.
  - 6 timeslices (five future 30-year periods plus a Control): 2020s, 2030s, 2040s, 2050s, 2080s, plus Control.
  - Time windows: Control (baseline) and 30-year slices for 2010–2039, 2020–2049, 2030–2059, 2040–2069, 2070–2099, respectively.

## Data structure and contents
- Archive: 16 datasets (ds01–ds16) contained in Byersetal-ds0.zip (49 MB, compressed).
- Filename convention: Q_out_b_XYYs-dsZZ.csv
  - X = emissions scenario (L, M, H for Low, Medium, High)
  - YY = timeslice code (20s for 2020s, 30s for 2030s, 40s for 2040s, 50s for 2050s, 80s for 2080s, CTRL)
  - Z Z = dataset reference number (ds01–ds16)
- Contents: 100 hydrological model output time series (columns) of daily mean discharge (m3/s), each 28 years long, for each combination of emissions scenario and timeslice.
- Structure: 16 .csv files corresponding to the five future timeslices plus Control across the three emission scenarios.
- Each .csv: 100 columns (samples) × ~10,592 rows (daily discharge over 28 years).
- Geographic location: River Trent at Colwick (discharge in m3/s).
- Each column represents a different sample from the UKCP09 change factor vectors.

## Data units and interpretation
- All values are daily mean discharge (m3/s).

## Data accessibility and provenance
- Data files are stored as ds01–ds16 within the Byersetal-ds0.zip archive (49 MB, compressed).
- The datasets are generated to support analysis of hydroclimatic impacts on CCS electricity generation and associated uncertainty via multiple scenarios and timeslices.

## Context and related materials
- Related publication: Hydroclimatic impacts on low-carbon CCS electricity generation (2015; in review).
- The data structure and simulations serve to quantify how hydroclimate variability and emissions scenarios affect river discharge projections used in environmental assessments.