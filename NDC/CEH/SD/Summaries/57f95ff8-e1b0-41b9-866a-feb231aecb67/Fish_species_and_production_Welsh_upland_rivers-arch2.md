# Fish species and production of Welsh upland rivers

- Purpose: Survey and quantify fish populations in upland Welsh rivers during stable base-flow periods to understand production and biomass variations across sites.

## Experimental design and sampling regime

- Study periods:
  - Base-flow period: June–September 2012
  - Additional sampling: July and September 2013
- Study area: Upland Wales

## Collection methods and field procedures

- Fish sampling method:
  - Quantitative electrofishing in representative 30 m reaches enclosed with stop nets (mesh size: 10 mm2)
  - Three-pass depletion method using a battery-powered Pulsed DC Electracatch system
  - Pass frequency: 50 Hz; voltage adjusted by site conductivity
  - Objective: obtain data representative of total abundance in upland streams
- Handling and measurements:
  - After each pass, fish placed in stream water holding container
  - Species identification, weight to the nearest gram, and fork length (FL) to the nearest millimeter
  - Mass measurement:
    - Most fish weighed directly; for some individuals mass estimated via length-mass regression when weighing was not accurate
- Reference methods:
  - Length-mass model development based on 2012 data
  - Regression model used: WM = b3 FL + b1 FL + intercept (nonlinear, cubic term to capture mass-length relationship)

## Mass estimation model

- Equation: WM = b3 FL + b1 FL + intercept
- WM: wet mass (g); FL: fork length (mm)
- Rationale: cubic term incorporated to better fit nonlinear mass gain with length
- Model coefficients: species-specific and provided in a separate file
- Data basis: 2012 observed data used to derive the model

## Data structure and storage

- Primary data file:
  - Flatbed CSV with fields (headings include):
    - site_code: sampling site code
    - season (Sampling season)
    - date: sampling date
    - fish: fish number
    - run: electrofishing run number
    - species: species name
    - length: fish length in mm
    - weight: fish weight in g
- Supporting data:
  - DURESS_CU_site_description.csv
  - Site description fields include:
    - Site_code
    - Name
    - Eastings, Northings (British National Grid)
    - Grid
    - Latitude, Longitude (WGS84)
    - Elevation (m)
    - Survey campaigns (e.g., WAWS - Welsh Acid Water Survey)
    - Catchment

## Analytical methods and units

- Identification: visual
- Measurements: length (mm) and weight (g) for each individual
- Data quality: no formal calibration or quality-control steps documented

## Quality control and calibration

- Calibration steps and values: None noted
- Data validation: None described beyond individual measurements and registration in the dataset

## Miscellaneous notes

- The document references external sources for methods and equipment:
  - Beaumont (2011) Electric Fishing: A Complete Guide
  - Kruse, Hubert & Rahel (1998) on single-pass electrofishing for trout abundance
  - Maitland (1972) key to freshwater fishes of the British Isles
- Links to references are provided via the CEH Data Catalogue Record; long-term link stability cannot be guaranteed
- The dataset aims to support monitoring outputs and data reuse for environmental health and policy scrutiny, aligned with standardised monitoring practices and data portal uploads.