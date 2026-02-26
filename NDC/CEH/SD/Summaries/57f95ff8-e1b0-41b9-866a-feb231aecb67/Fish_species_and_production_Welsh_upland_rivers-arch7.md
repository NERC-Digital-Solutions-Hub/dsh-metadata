# Fish species and production of Welsh upland rivers

## Overview
- Study of fish populations in upland Wales during stable base-flow periods.
- Sampling occurred in 2012 (June–September) and in 2013 (July and September).
- Aimed at describing species present and biomass production across study sites; data are suitable for map-based analyses of spatial patterns.

## Experimental design and collection methods
- Survey design: representative 30 m reaches at each site, enclosed with stop nets (mesh size 10 mm2).
- Sampling method: three-pass depletion electrofishing using a battery-powered Pulsed DC Electracatch system (50 Hz); voltage adjusted by site conductivity.
- Per fish data: species identification, fork length (mm), weight (g) measured/recorded; most fish weighed directly.
- Mass estimation: for some fish where mass could not be measured in the field, mass estimated using a length-mass regression model.
  - Model form (example): WM = b3 FL + b1 FL + intercept (with a cubic term to capture nonlinear gains); coefficients provided in a separate file.
- Quality checks: none documented.

## Data collected and units
- For each fish: 
  - Length: millimetres (mm)
  - Weight: grams (g)
  - Additional identifiers: site, season, date, run, species

## Data structure
- Primary dataset: flatbed CSV with eight columns:
  - site_code: sampling site code
  - season: sampling season
  - date: date of collection
  - fish: fish number
  - run: electrofishing run number
  - species: species name
  - length: fish length (mm)
  - weight: fish weight (g)

## Supporting site description data
- File: DURESS_CU_site_description.csv
- Ten columns including:
  - Site_code, Name, Eastings, Northings, Grid
  - Latitude, Longitude, Elevation
  - Survey, Catchment
- Provides spatial context and coordinates for GIS mapping (British National Grid and WGS84 references).

## Data provenance, references, and notes
- Coefficients for length-mass models are provided in a separate file.
- Field methods and references:
  - Beaumont (2011) on electric fishing methods
  - Kruse, Hubert & Rahel (1998) on single-pass electrofishing
  - Maitland (1972) key to freshwater fishes of the British Isles
- Links to references are provided but may not be permanently guaranteed.

## GIS-ready considerations
- Spatial attributes: site_code linked to precise coordinates (Eastings/Northings, Grid, Latitude/Longitude) and elevation; enables mapping of species presence and biomass across sites and catchments.
- Temporal dimension: two-year sampling windows (2012 base-flow period; 2013 mid-year), enabling seasonal/spatial trend analyses.
- Data integration: combine fish data with site descriptions for enhanced spatial analyses; note absence of formal quality control in documentation.