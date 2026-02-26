# Supporting information for Hydrological modelling simulation data for the River Trent

- Experimental setup
  - An 8-parameter hydrological model calibrated using data from Colwick on the River Trent (station 28009).
  - Structural uncertainty and calibration explored via 10,000 parameterisations generated with Latin hypercube sampling.
  - Model performance assessed with a 4-metric ranking: log-transformed Nash-Sutcliffe Efficiency and absolute differences between observed and simulated for Q90, Q95, and Q99 percentile flows.
  - Simulations driven by UKCP09 Weather Generator timeseries:
    - 100 samples
    - Three emissions scenarios: Low, Medium, High
    - Five 30-year timeslices corresponding to future periods and a Control:
      - CTRL (control)
      - 2020s (2010–2039)
      - 2030s (2020–2049)
      - 2040s (2030–2059)
      - 2050s (2040–2069)
      - 2080s (2070–2099)

- Data structure and contents
  - Datasets ds01 to ds16 are in the compressed archive Byersetal-ds0.zip (49 MB).
  - Filename convention: Q_out_b_XYYs-dsZZ.csv
    - X: emissions scenario (L = Low, M = Medium, H = High)
    - YY: timeslice (20s, 30s, 40s, 50s, 80s, CTRL)
    - ZZ: dataset reference number (ds01–ds16)
  - Each CSV contains 100 hydrological model output time series (columns) of daily mean discharge (m3/s) for 28 years, at Colwick.
  - The archive includes 16 CSV files: across five timeslices (2020s, 2030s, 2040s, 2050s, 2080s) and three emissions scenarios plus a Control.
  - Each CSV has 100 columns (samples), representing 100 realizations from the UKCP09 change-factor vectors, and 10,592 rows (28-year daily data).
  - Data units: daily mean discharge in cubic metres per second (m3/s).