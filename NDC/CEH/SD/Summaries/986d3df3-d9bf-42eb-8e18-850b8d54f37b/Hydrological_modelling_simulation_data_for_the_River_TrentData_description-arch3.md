# Supporting information for Hydrological modelling simulation data for the River Trent Data

## Overview
- Describes the data structure for hydrological model outputs related to hydroclimatic impacts on low-carbon CCS electricity generation.
- Based on an 8-parameter model, with calibration, uncertainty analysis, and data sources outlined in the associated paper.
- Model setup and evaluation designed to support robust interpretation of hydrological responses under climate and emissions scenarios.

## Experimental design
- Model framework, calibration uncertainty analysis, and data sources detailed in the associated paper.
- 8-parameter model inspired by the Ph.D. work of Leathard (unpublished) at Newcastle University.
- Calibration performed using data from Colwick on River Trent (station 28009).
- Structural uncertainty and calibration explored by generating 10,000 parameterisations via Latin hypercube sampling.
- Model performance assessed using a 4-metric ranking: log-transformed Nash-Sutcliffe Efficiency and absolute differences between observed and simulated for Q90, Q95, and Q99 percentile flows.
- Simulations run with UKCP09 Weather Generator timeseries, including:
  - 100 samples
  - three emissions scenarios (low, medium, high)
  - five future 30-year timeslices plus a control: CTRL, 2020s (2010–2039), 2030s (2020–2049), 2040s (2030–2059), 2050s (2040–2069), 2080s (2070–2099)

## Data structure
- Datasets ds01 to ds16 contained in the compressed archive Byersetal-ds0.zip (49 MB).
- Filename convention: Q_out_b_XYYs-dsZZ.csv
  - X: emissions scenario (L = low, M = medium, H = high)
  - YY: timeslice (20s, 30s, 40s, 50s, 80s, CTRL)
  - ZZ: dataset reference (ds01 to ds16)
- Contains 100 hydrological model output timeseries (columns) of daily mean discharge (m^3/s), spanning 28 years per scenario/time slice.
- Archive includes 16 CSV files corresponding to five timeslices and three emission scenarios, plus Control profiles.
- Each CSV consists of 100 columns (samples) of 28-year daily discharge timeseries (10,592 rows) at Colwick.
- Each column represents a different sample drawn from the UKCP09 change factor vectors.

## Data content and units
- All fields are daily mean discharge values measured in cubic metres per second (m^3/s).