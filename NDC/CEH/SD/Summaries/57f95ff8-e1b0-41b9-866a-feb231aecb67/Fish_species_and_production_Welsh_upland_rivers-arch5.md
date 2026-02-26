# Fish species and production of Welsh upland rivers

- Overview
  - Dataset records fish populations surveyed at upland Welsh study sites during stable base-flow periods: June–September 2012 and July and September 2013.
  - Aims to quantify species composition and biomass across sites, supporting data discovery, reuse, and governance for large datasets.

- Data collection and measurement methods
  - Sampling in representative 30 m reaches enclosed with stop nets.
  - Three-pass depletion using battery-powered Pulsed DC Electracatch electrofishing (50 Hz); voltage adjusted for site conductivity.
  - After each pass: identify species, weigh to the nearest gram, and measure fork length to the nearest millimetre.
  - Biomass assessment: most fishes weighed in the field; for some individuals mass estimated via length-mass regression (WM = b3 FL + b1 FL + intercept) to account for measurement limits.
  - Length-mass model coefficients are provided in a separate file; references cited for methodology (Beaumont 2011; Kruse et al. 1998; Maitland 1972).
  - Calibration steps: none documented.
  - Analytical methods: visual species identification, length measurement, and weight measurement.
  - Units: length in millimetres; weight in grams.

- Data structure and content
  - Primary data file: flatbed file with eight columns:
    - site_code: sampling site identifier
    - season: sampling season
    - date: date of sampling collection
    - fish: fish number and species
    - run: electrofishing run number
    - species: species name
    - length: fish length in millimetres
    - weight: fish weight in grams

- Supporting metadata and site information
  - Auxiliary file: DURESS_CU_site_description.csv
    - site_code, Name, Eastings, Northings, Grid, Latitude, Longitude, Elevation
    - Survey (campaign) and Catchment (river catchment) details
  - Site data provide geographic context (grid references and coordinates) to aid data discovery and spatial analyses.

- Quality, provenance, and limitations
  - Quality Control: not documented within the dataset description.
  - Data provenance is clear in terms of collection protocol and measurement methods, with mass estimation for some individuals introducing measurement uncertainty.
  - References to external sources for methodology are provided, though links may not be permanently stable.

- Access, reuse, and governance considerations
  - Data are described and catalogued (CEH Data Catalogue context) with cross-referenced references; external links may degrade over time.
  - For data stewardship:
    - Maintain clear metadata and stable references for methodologies and coefficient files.
    - Ensure provenance, units, and column definitions remain consistent to support reuse across studies.
    - Monitor and document any updates to site descriptions or regression coefficients to preserve data integrity.