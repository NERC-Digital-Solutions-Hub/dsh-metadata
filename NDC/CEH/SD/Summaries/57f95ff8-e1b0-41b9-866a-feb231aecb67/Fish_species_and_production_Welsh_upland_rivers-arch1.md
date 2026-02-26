# Fish species and production of Welsh upland rivers

- Overview
  - Survey of fish populations across upland Wales during stable base-flow periods (June–September 2012; July and September 2013).
  - Aims to characterize species composition and biomass production across study sites.

- Experimental design and sampling regime
  - Sampling at representative 30 m reaches, enclosed with stop nets (mesh size 10 mm2).
  - Three-pass depletion using quantitative electrofishing (Pulsed DC Electracatch), 50 Hz; site-specific voltage based on conductivity.
  - Three passes intended to capture a large proportion of individuals, providing data representative of total abundance.

- Data collection and measurements
  - After each pass: identify species, weigh to the nearest gram, measure fork length to the nearest millimetre.
  - Biomass estimation for some individuals via length-mass regression when direct mass measurement was not possible.

- Length-mass modelling
  - Model: WM = b3 FL + b1 FL + intercept with a cubic term to capture nonlinear mass gain.
  - Species-specific coefficients provided in a separate file.

- Data structure and contents
  - Primary data file: eight columns
    - site_code, season, date, fish (number), run, species, length (mm), weight (g)
  - Supporting dataset: site_description.csv with
    - site_code, name, Eastings/Northings, Grid, Latitude, Longitude, Elevation, Survey, Catchment

- Data processing and quality
  - Field identification, length measurement, and weight recording described.
  - Calibration steps: none specified; formal quality control procedures not described.

- Context and references
  - Methodological references: Beaumont (2011), Kruse et al. (1998), Maitland (1972).
  - Links to references may be found in the CEH Data Catalogue; external links may not be permanent.