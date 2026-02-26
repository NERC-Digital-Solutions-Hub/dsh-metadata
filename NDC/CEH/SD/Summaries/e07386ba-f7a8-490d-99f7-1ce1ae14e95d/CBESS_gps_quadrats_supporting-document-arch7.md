# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) global positioning system (GPS) locations of quadrats in saltmarsh and mudflat habitats

## Overview
- GPS locations and elevations for CBESS monitoring installations in waves, surface elevation, and sedimentation studies.
- Staff responsible: Tom Spencer, Ben Evans.
- Observations collected at six UK sites (three in Essex, three in Morecambe Bay) representing contrasting habitats and sediment types.
- Each site comprises 22 quadrats on unvegetated mudflat and 22 quadrats on salt marsh.

## Sites and Habitats
- Essex sites: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM).
- Morecambe Bay sites: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP) [within the Morecambe Bay grouping].
- Habitat categories: Saltmarsh (SM) and Mudflat (MF).
- Site descriptions reflect contrasting soil types and inundation/creek/vegetation characteristics.

## Data Collection and Timing
- Monitoring window: surveys conducted within two weeks prior to or during the CBESS main sampling campaigns in Winter and Summer 2013.
- GPS equipment: Leica GS08 GNSS system with a 50 mm coordinate quality check threshold (points below threshold rejected).
- Coordinate system: OSGB1936(2) with Northings, Eastings, and elevation relative to Ordnance Datum Newlyn (ODN).
- Quadrats: 1 m x 1 m, oriented NS and EW; locations indicated by the south-east corner of quadrats.

## Data Processing and Calibration
- Data handling: records exported as ASCII text; unnecessary or duplicate data points removed in MS Excel; no additional data transformations performed.
- Calibration: Leica RTK corrections applied in real time where applicable.

## Data Attributes and Structure
- Variables observed: Northing, Easting, Elevation.
- Dataset fields include:
  - Site (e.g., Morecambe: CS/WS/WP; Essex: AH/FW/TM)
  - Habitat (Saltmarsh SM or Mudflat MF)
  - Quadrat (numbered 1–22 per site)
  - Scale (A=1 m; B=1–10 m; C=10–100 m; D=100–upper limit)
  - Easting (m)
  - Northing (m)
  - Elevation (m, relative to OD Newlyn)
  - Season (Winter W or Summer S)
  - Row number and header information (for data sorting and description)

## Data Quality and Notes
- NA values indicate measurements not performed for a given field.
- No subsequent data processing beyond initial QC and Excel cleaning was undertaken.