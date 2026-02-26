# Supporting information for Hydrological modelling simulation data for the River Trent Data

## Overview
- Describes the data structure for hydrological model outputs related to hydroclimatic impacts on low-carbon CCS electricity generation.
- 8-parameter model calibrated with data from Colwick on Trent (station 28009).
- Calibration and structural uncertainty explored via 10,000 parameterisations using Latin hypercube sampling.
- Model performance evaluated with a 4-metric ranking: log-transformed Nash-Sutcliffe Efficiency and absolute differences for Q90, Q95, and Q99 percentile flows.
- Runs use UKCP09 Weather Generator timeseries:
  - 100 samples
  - 3 emissions scenarios: Low, Medium, High
  - 5 future timeslices plus a Control profile (see below)

## Experimental design
- 8-parameter model with calibration uncertainty analyzed across 10,000 parameterisations.
- Structural uncertainty assessed through parameter sampling and model runs.
- Weather inputs generated with UKCP09 Weather Generator:
  - 100 samples
  - Scenarios: Low, Medium, High
  - Timeslices: CTRL (control), 2020s, 2030s, 2040s, 2050s, 2080s

## Data structure and content
- Data archive: Byersetal-ds0.zip (49 MB, compressed) containing datasets ds01 to ds16.
- Filename convention: Q_out_b_XYYs-dsZZ.csv
  - X: emission scenario (L = Low, M = Medium, H = High)
  - YY: timeslice (20s, 30s, 40s, 50s, 80s, CTRL)
  - ZZ: dataset reference number (ds01 to ds16)
- Each dataset consists of 100 hydrological model output time series (columns):
  - Daily mean discharge (m3/s)
  - 28-year length for each combination of emissions scenario and timeslice
  - 10,592 rows per file
  - Each column is a different sample drawn from the UKCP09 change factor vectors
- Spatial context: daily discharge at River Trent, Colwick (station 28009)

## Data structure specifics
- 16 CSV files cover the five future timeslices (2020s, 2030s, 2040s, 2050s, 2080s) plus the Control
- Each CSV has:
  - 100 columns (samples)
  - 28 years of daily discharge data per column
  - Unit: cubic metres per second (m3/s)

## Data units and interpretation
- All fields represent daily mean discharge in m3/s
- Columns reflect different sample parameterisations; rows represent daily values across the 28-year period
- Data enable GIS-based analyses of hydroclimate impacts under multiple climate and emission scenarios

## Access and usage notes
- Archive location: Byersetal-ds0.zip (49 MB, compressed)
- File naming example: Q_out_b_L20s-ds01.csv (Low emissions, CTRL timeslice, dataset ds01)
- Intended use: supporting information for hydrological modelling outputs pertinent to River Trent analyses and related GIS map-based visualisations