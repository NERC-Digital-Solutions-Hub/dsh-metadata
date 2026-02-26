# Supporting information for Hydrological modelling simulation data for the River Trent Data

## Overview
- Describes the data structure of hydrological model outputs related to the study on hydroclimatic impacts on low-carbon CCS electricity generation.
- Authors and affiliations: Newcastle University (School of Civil Engineering & Geosciences) and University of Oxford (Environmental Change Institute).

## Experimental design
- Model: 8-parameter hydrological model calibrated with Colwick, Trent (station 28009); based on Ph.D. work by A. Leathard.
- Calibration and uncertainty: structural uncertainty and calibration explored by simulating 10,000 parameterisations via Latin hypercube sampling.
- Performance metrics: 4-metric ranking using log-transformed Nash-Sutcliffe Efficiency and absolute differences for observed vs. simulated Q90, Q95, and Q99 percentile flows.
- Weather forcing: UKCP09 Weather Generator timeseries.
  - Scenarios: low, medium, high emissions.
  - Timeslices: five future periods plus a control.
  - Temporal windows: Control plus 2020s (2010–2039), 2030s (2020–2049), 2040s (2030–2059), 2050s (2040–2069), 2080s (2070–2099).

## Data structure and contents
- Archive: Byersetal-ds0.zip (49 MB) containing datasets ds01 to ds16.
- File naming: Q_out_b_XYYs-dsZZ.csv
  - X = emissions scenario (L = low, M = medium, H = high)
  - YY = timeslice (20s, 30s, 40s, 50s, 80s, CTRL)
  - ZZ = dataset reference (ds01–ds16)
- Each CSV contains 100 hydrological model output time series (columns) of daily mean discharge (m3/s) across 28 years per scenario-timeslice.
- Contents: 16 CSV files covering five timeslices (2020s, 2030s, 2040s, 2050s, 2080s) and three emission scenarios (Low, Medium, High), plus Control.
- Structure: each column is a different sample from the UKCP09 change-factor vectors.
- Time resolution: daily discharge values; 10,592 rows per file (28-year span).

## Data units and scope
- Units: daily mean discharge in cubic meters per second (m3/s) for River Trent at Colwick.

## Accessibility and usage notes
- Data hosted as compressed CSVs within the ds01–ds16 set; designed to support exploration of hydroclimatic responses under different climate and emission scenarios.
- Useful for researchers seeking to analyze variability across parameter samples, to reproduce or extend analyses related to CCS electricity generation under future hydrological conditions.

## Relationship to broader work
- Supplements the main paper and supplementary information on hydroclimatic impacts for low-carbon CCS electricity generation (2015, in review).
- Provides a concrete data structure and sample outputs to enable self-serve analysis and further data products.