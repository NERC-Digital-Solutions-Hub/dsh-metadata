# Carbon Storage in Intertidal Environments (C-SIDE)

## Overview
- Project title: Carbon Storage in Intertidal Environments (C-SIDE)
- Funded by: NERC (NE/R010846/1)
- Lead or responsible staff: Craig Smeaton
- Collaboration: Universities of St Andrews, Glasgow, York; UKCEH; Bangor; University of Leeds; and other partners
- Focus: GPS locations and elevations of soil sampling sites across UK saltmarshes to support carbon stock assessments

## Data Resource Details
- Resource: Global positioning system (GPS) locations and elevations of soil sampling sites
- Scope: 1323 sampling sites across UK saltmarshes
- Temporal coverage: 2018–2021
- Data format: CSV
- Purpose of data: Support surficial organic carbon (OC) stock calculations, soil carbon stocks and burial rates, and assessment of belowground biomass

## Geographic Coverage and Observations
- Geographic extent: United Kingdom saltmarshes
- Spatial reference: Lat/Long in decimal degrees (WGS84) and corresponding X/Easting, Y/Northing
- Specific extents described: Bounding coordinates provided for UK study area
- Site distribution rationale: All sites located in environmentally comparable regions of Scotland to enable representative comparisons; sites spread around Scotland’s coastline

## Data Content and Metadata
- Core location fields:
  - Marsh_ID: saltmarsh name (text)
  - Site_ID: sample identifier (text)
  - Nation: Scotland, England, Wales (text)
  - Local_authority: local governing authority (text)
  - Marsh_type: Natural, Historic Breach, Managed Realignment (text)
  - Collection_year: year of sample collection (numeric)
- Geospatial fields:
  - Lat_dec_deg: latitude in decimal degrees (numeric)
  - Long_dec_deg: longitude in decimal degrees (numeric)
  - X_easting: easting (numeric)
  - Y_northing: northing (numeric)
  - Elevation_AOD_m: elevation above Ordnance Datum (m) (numeric)
- Sampling metadata:
  - Sampling_method: syringe sampler; narrow (30 mm) gouge corer; wide (60 mm) gouge corer (text)
  - Core_length_cm: length of core retrieved (cm) (numeric)
  - Purpose: surficial OC stock calculations; soil carbon stocks and burial rates; belowground biomass (text)
- Data collection and processing notes:
  - Calibration: real-time corrections via Juniper RTK, Leica Infinity, Trimble GNSS (text)
  - Data processing: no subsequent processing undertaken (NA)
  - Data quality checks: not described (NA)
- Supported formats: CSV (file format)

## Data Collection Methods and Quality Considerations
- GPS and positioning:
  - Collected using multiple GNSS systems with real-time corrections
  - Raw GPS coordinates and elevations provided; no post-hoc processing indicated
- Sampling methods:
  - Syringe sampler and gouge corers (narrow and wide diameters) used to collect sediment cores
- Data scope for analysis:
  - Provides geospatial framework and core length data necessary for carbon stock and burial-rate calculations
- Notes for data users:
  - Data checks and QC procedures are not described in the resource
  - Some fields have NA entries for QC-related details

## Format, Access, and Usage
- Primary data format: CSV
- Access indications: dataset details and metadata are provided; licensing/access terms not specified in the excerpt
- Intended end uses:
  - Enabling researchers and policy-relevant analyses of saltmarsh carbon storage
  - Facilitating self-serve exploration of GIS-compatible location and core data
  - Supporting cross-site comparisons across Scotland and other UK regions

## Implications for Data Support
- Provides a comprehensive, georeferenced dataset enabling carbon stock estimation and burial-rate analysis across UK saltmarshes
- Combines spatial coordinates, elevation, site metadata, and core-length information to support data-driven decision-making on coastal carbon management
- Reflects a multi-institutional collaboration with emphasis on broad geographic coverage and standardized metadata for downstream analyses