# Supporting information for Hydrological modelling simulation data for the River Trent Data

- Purpose and scope
  - Describes the data structure for hydrological model outputs related to the paper “Hydroclimatic impacts on low-carbon CCS electricity generation” (2015, in review).
  - Supports understanding and reuse of 100 hydrological model output time series (daily mean discharge) across multiple climate scenarios and future timeslices.

- Experimental design
  - Model: 8-parameter hydrological model (based on PhD work of Alex Leathard).
  - Data source: Colwick on Trent (station 28009).
  - Calibration and uncertainty: structural uncertainty and calibration explored by simulating 10,000 parameterisations via Latin hypercube sampling.
  - Evaluation: 4-metric ranking using log-transformed Nash-Sutcliffe Efficiency and absolute differences at Q90, Q95, and Q99 percentile flows.
  - Climate forcing: UKCP09 Weather Generator timeseries.
    - 100 samples per scenario
    - 3 emissions scenarios: Low, Medium, High
    - 5 future 30-year timeslices
      - Control
      - 2020s (2010–2039)
      - 2030s (2020–2049)
      - 2040s (2030–2059)
      - 2050s (2040–2069)
      - 2080s (2070–2099)

- Data structure and contents
  - Archive: Byersetal-ds0.zip (49 MB, compressed)
  - Datasets: ds01 to ds16 contained within
  - Filename convention: Q_out_b_XYYs-dsZZ.csv
    - X: emissions scenario (L = Low, M = Medium, H = High)
    - YY: timeslice (20s, 30s, 40s, 50s, 80s, CTRL)
    - ZZ: dataset reference number (ds01–ds16)
  - Data volume: 100 hydrological model output time series per file (columns)
  - Temporal footprint: 28-year daily discharge series per column (10,592 rows)
  - Spatial/temporal focus: River Trent at Colwick
  - Data content: each column is a different sample drawn from the UKCP09 change factor vectors
  - Units: daily mean discharge in cubic meters per second (m3/s)

- Data units and formats
  - All fields represent daily mean discharge in m3/s
  - 16 CSV files across five timeslices and three emissions scenarios, plus Control profiles

- Provenance and documentation
  - Authors and affiliations: Byers, Leathard, O’Donnell, Hall, Amezaga (Newcastle University) and Hall (University of Oxford)
  - Context: Part of data supporting hydroclimatic impact analysis for CCS electricity generation
  - Archive organization supports discovery by dataset and timeslice, with explicit naming conventions

- Metadata and governance considerations for Data Stewards
  - Ensure metadata includes: dataset identifiers (ds01–ds16), scenario codes (L/M/H), timeslice codes (20s/30s/40s/50s/80s/CTRL), temporal coverage (28 years), unit (m3/s), and spatial location (Colwick station 28009)
  - Maintain provenance: link datasets to the paper and supplementary information; capture model version, calibration approach (Latin hypercube sampling), and performance metrics used
  - Data sharing and access: provide access via the compressed archive (Byersetal-ds0.zip) and clearly document file naming conventions for interoperability
  - Data quality and updates: monitor for updates or new timeslices/scenarios; document any revisions to dataset mappings or parameterisations
  - Storage considerations: handle large, multi-file CSVs; ensure integrity of 49 MB compressed archive and the 10,592-row files

- Practical notes for reuse
  - Useful for researchers needing multi-scenario hydrological outputs under UKCP09 forcing across multiple future periods
  - Facilitates comparative analysis of discharge regimes at Colwick under low/medium/high emissions and various timeslices
  - Provides a consistent structure to support model validation, uncertainty assessment, and downstream impact studies for CCS-related electricity scenarios