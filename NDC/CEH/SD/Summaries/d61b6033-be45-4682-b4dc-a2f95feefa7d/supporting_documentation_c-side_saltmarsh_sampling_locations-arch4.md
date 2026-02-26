# Global positioning system (GPS) locations and elevations of soil sampling sites across UK saltmarshes between 2018 - 2021

## Overview
- Project: Carbon Storage in Intertidal Environments (C-SIDE)
- Funding: NERC (NE/R010846/1)
- Lead staff: Craig Smeaton (Staff Responsible)
- Research team: 16 contributors from multiple universities and UK CEH

## Dataset scope and provenance
- Data Resource ID: GPS locations and elevations of soil sampling sites across UK saltmarshes (2018–2021)
- Description: GPS locations and elevations recorded for 1,323 sampling sites across UK saltmarshes
- Geographic extent: United Kingdom (data presented in decimal degrees with WGS84 coordinates and also as X Easting and Y Northing)
- Site context: Sites selected to represent saltmarsh environments, sediment types, and organic carbon (OC) content
- Data status: No subsequent processing has been undertaken (raw observations)

## Data content and structure
- Key variables include:
  - Lat_dec_deg, Long_dec_deg: Latitude and longitude in decimal degrees (WGS84)
  - X_easting, Y_northing: Planar coordinates (Easting, Northing)
  - Elevation_AOD_m: Elevation above Ordnance Datum (m)
  - Collection_year: Year of sample collection
  - Marsh_ID, Site_ID: Descriptors for saltmarsh locations
  - Nation: Scotland, England, Wales
  - Local_authority: Local authority responsible for the saltmarsh
  - Marsh_type: Natural, Historic Breach, Managed Realignment
  - Sampling_method: Syringe sampler; Narrow (30 mm) gouge corer; Wide (60 mm) gouge corer
  - Core_length_cm: Length of core retrieved (cm)
  - Purpose: Surficial OC stock calculations; Soil C stocks and burial rates; Soil C stocks; Belowground biomass (roots)
- Data format: .csv
- Data completeness indicators: NA in the data dictionary indicates no data in cells

## Spatial and temporal coverage
- Observation period: 2018–2021
- Location descriptions: All sites located in similar environmental regions of Scotland to enable comparability; sites chosen around Scotland’s coastline to reflect saltmarsh conditions, sediment types, and OC content (with inclusion of Scotland, England, and Wales)

## Data quality, processing, and standards
- Calibration and corrections: Juniper RTK corrections in real time; Leica Infinity real-time correction; Trimble GNSS correction service
- Data quality checks: Not applicable / not provided (Data checking procedures marked as NA)
- Processing: No additional processing beyond initial data collection; raw GPS coordinates and elevations

## Metadata, formats, and access
- Data formats: CSV file
- Coordinate reference systems: Lat/Long in decimal degrees (WGS84); Easting/Northing provided as complementary coordinates
- Elevation reference: Elevation above Ordnance Datum Newlyn (AOD)
- Metadata detail: Includes dataset description, site identifiers, and variable definitions; data dictionary notes NA indicating missing values
- Accessibility: Described with dataset-level details; direct access method not specified beyond the CSV format and the Data Resource ID

## Stakeholders and contributors
- Institutions involved: University of St Andrews, University of Glasgow, University of York, University of Leeds, Bangor University, UK CEH
- Contributing researchers: 16 named team members across multiple UK institutions
- Purpose alignment: Data intended to support surficial OC stock calculations, soil carbon stocks and burial rates, and assessment of belowground biomass in UK saltmarshes

## Practical implications for Data Leaders
- Demonstrates end-to-end data asset creation, including provenance, coordinate systems, and raw data status
- Highlights importance of metadata completeness (coordinate references,Elevation reference, sampling methods, core lengths, and purposes)
- Illustrates challenges of large, multi-site biological/geospatial data (scattered site locations, diverse marsh types, and cross-regional coordination)
- Emphasizes need for ongoing data governance: documentation of processing steps, QA procedures, and updates to metadata as data are reused and expanded