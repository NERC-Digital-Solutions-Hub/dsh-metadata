# Fish species and production of Welsh upland rivers

- Overview
  - Study of fish populations in upland Wales during a stable base-flow period (June–September 2012) and in July and September 2013, aiming to assess variations in fish biomass across sites.

- Experimental design and sampling regime
  - Sites: upland Wales; two sampling periods (2012 base-flow; 2013 summer).
  - Method: quantitative electrofishing in representative 30 m reaches enclosed with stop nets (mesh 10 mm2).
  - Procedure: three-pass depletion using Pulsed DC Electracatch; 50 Hz; site-specific conductivity adjustments to optimize salmonid captures.
  - Measurements: after each pass, identify species, weigh to nearest gram, measure fork length to nearest millimetre.
  - Mass data: where mass could not be measured in the field, estimate using a length-mass regression model.
    - Model: WM = b3 FL + b1 FL + intercept (cubic term included to capture nonlinear gains).
    - Species-specific coefficients provided in a separate file.
  - References: Beaumont (2011), Kruse et al. (1998), Maitland (1972) cited; links to references available via CEH Data Catalogue Record (may not be permanent).

- Data collection instruments and steps
  - Field and lab procedures: visual species identification, length measurement, and weight recording.
  - Calibration: none specified.

- Data structure and content
  - Primary data file: flatbed CSV with eight columns
    - site_code: sampling site identifier
    - season: sampling season indicator
    - date: date of sampling
    - fish: fish number and species
    - run: electrofishing run number
    - species: species name
    - length: fish length in millimetres
    - weight: fish weight in grams
  - Supporting data: DURESS_CU_site_description.csv
    - Columns include site_code, Name, Eastings, Northings, Grid, Latitude, Longitude, Elevation, Survey, Catchment
  - Units: length in millimetres; weight in grams.

- Data quality and notes
  - Quality control: none documented.
  - Data considerations: masses for some individuals estimated via regression; regression coefficients provided separately.
  - Data completeness: structure supports cross-site biomass and size distribution analyses, with geolocation and site metadata available.

- Potential data products and uses
  - Dashboards or reports enabling exploration of biomass by site, season, and species.
  - Analyses of relationships between fish size/weight distributions and catchment/location.
  - Self-serve data exploration for stakeholders (e.g., policymakers, conservation groups) interested in upland river fish production.

- Data provenance and access notes
  - References to methodological sources and data catalog records provided; links to external sources may change over time.
  - Data described here can be combined with site metadata to produce location-based insights and visualizations.