# Supporting information for Hydrological modelling simulation data for the River Trent Data

- The document provides the data structure and content for hydrological model outputs used in the associated hydroclimatic impact study on low-carbon CCS electricity generation (Byers et al., 2015).

## Experimental design and model framework
- An 8-parameter hydrological model calibrated using Colwick on Trent (station 28009).
- Structural uncertainty and calibration explored by simulating 10,000 parameterisations via Latin hypercube sampling.
- Model performance assessed with a 4-metric ranking incorporating:
  - Nash-Sutcliffe efficiency (log-transformed flows)
  - Absolute differences between observed and simulated 90th, 95th, and 99th percentile flows (Q90, Q95, Q99).
- Simulations run with UKCP09 Weather Generator time series:
  - 100 samples
  - 3 emission scenarios (low, medium, high)
  - 5 future 30-year timeslices (plus a Control)

## Timeslices and scenarios
- Timeslices referenced: Control, 2020s (2010–2039), 2030s (2020–2049), 2040s (2030–2059), 2050s (2040–2069), 2080s (2070–2099).
- Note: While described as five future timeslices, the list includes six categories (Control plus five future periods), indicating six total timeslices used in the simulations.

## Data structure and contents
- Data are organized into datasets ds01 to ds16 within a compressed archive named Byersetal-ds0.zip (approximately 49 MB).
- Filename convention: Q_out_b_XYYs-dsZZ.csv
  - X: emissions scenario (L = low, M = medium, H = high)
  - YY: timeslice (20s, 30s, 40s, 50s, 80s, CTRL)
  - ZZ: dataset reference number (ds01 to ds16)
- Each dataset contains 100 hydrological model output time series (columns) of daily mean discharge (m³/s) across 28 years.
- Archive contains 16 CSV files corresponding to the five future timeslices plus Control, under three emission scenarios and multiple samples.
- Each CSV file comprises 100 columns (samples) and 10,592 rows (28 years of daily discharge data).

## Data units and interpretation
- All values are daily mean discharge in cubic meters per second (m³/s).
- Each column represents a different sample from the UKCP09 change factor vectors, enabling analysis of uncertainty in hydrological responses under different climate scenarios.

## Access and provenance
- The data support the analysis of hydroclimatic impacts on energy systems, particularly for low-carbon CCS electricity generation.
- Data are designed to be integrated with the associated paper and supplementary information, providing transparent provenance and a clear naming scheme for traceability and reuse.