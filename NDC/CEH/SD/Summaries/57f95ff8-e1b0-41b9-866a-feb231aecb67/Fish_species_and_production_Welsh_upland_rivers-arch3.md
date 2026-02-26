# Fish species and production of Welsh upland rivers

## Overview
- A survey of fish populations across upland Wales conducted during base-flow periods in 2012 (June–September) and 2013 (July and September) to document species, sizes, and biomass across multiple sites.
- Data intended to support comparisons of biomass across sites and over time, informing monitoring and management decisions.

## Experimental design and sampling regime
- Sampling period: stable base-flow windows in 2012 and 2013.
- Sites: upland Welsh rivers; representative sampling reaches.
- Objective: assess variation in fish biomass across sites.

## Collection methods
- Method: quantitative electrofishing in representative 30 m reaches enclosed with stop nets (mesh size 10 mm^2).
- Procedure: three-pass depletion using a Pulsed DC Electracatch setup (50 Hz) with site-specific conductivity-adjusted voltage.
- Processing: captured fish were held in stream water between passes, identified to species, weighed to the nearest gram, and fork length measured to the nearest millimetre.
- Mass estimation: for some fish where in-field mass could not be measured, mass was estimated using a length-mass regression model (wet mass WM = b3 FL + b1 FL + intercept; FL = fork length).
- Reference methods: regression model described; coefficients available in a separate file.
- Calibration: none.

## Analytical methods and recorded values
- Measurements: species identification, fork length (mm), weight (g) for each individual.
- Quality control: none indicated.

## Data structure and contents
- Primary data: one flatbed file with eight columns:
  - site_code: sampling site identifier
  - season: sampling season
  - date: collection date
  - fish: fish number and species
  - run: electrofishing run number
  - species: species name
  - length: fish length in mm
  - weight: fish weight in g
- Supporting data: site description file (DURESS_CU_site_description.csv) with ten columns:
  - Site_code, Name, Eastings, Northings, Grid, Latitude, Longitude, Elevation
  - Survey/Catchment information, etc.

## Site and metadata details
- Site descriptions include precise geolocation (British National Grid, latitude/longitude), elevation, and catchment/survey information.
- The site description file provides context for spatial analyses and data governance.

## Supporting documents and references
- Field and analytical context references:
  - Beaumont W.R.C. (2011) Electric Fishing: A Complete Guide to Theory and Practice
  - Kruse C.G., Hubert W.A. & Rahel F.J. (1998)
  - Maitland P.S. (1972)
- Data catalogue notes: links to references can be accessed from the CEH Data Catalogue Record; the EIDC cannot guarantee link persistence.

## Relevance for monitoring frameworks
- Key measures captured:
  - Species composition, individual size (length), and biomass (weight) per fish.
- Strengths for monitoring:
  - Standardized three-pass electrofishing method across sites.
  - Spatially explicit data across upland catchments with accompanying site metadata.
  - Data structure supports aggregation to site-level biomass and species-specific analyses.
- Considerations and limitations:
  - No explicit quality control described.
  - Some mass data rely on length-mass regression (coefficients in a separate file), introducing model-based estimation.
  - Data governance considerations include data sharing of underlying data and metadata; references to data catalogue and link persistence.