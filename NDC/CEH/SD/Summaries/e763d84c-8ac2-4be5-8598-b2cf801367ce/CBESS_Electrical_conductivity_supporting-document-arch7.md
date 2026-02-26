# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) soil electrical conductivity on salt marsh sites at Morecambe Bay and Essex

## Overview
- A dataset capturing soil electrical conductivity (EC) as a proxy for salinity across saltmarsh and mudflat habitats.
- Based on 10 g soil samples from the top 5 cm, collected in 1 m x 1 m quadrats.
- Part of CBESS, with fieldwork conducted in Winter and Summer 2013; additional Essex winter sampling 2–6 March 2013.

## Spatial and Temporal Coverage
- Locations:
  - Essex: Abbotts Hall (AH), Fingringhoe Wick (FW), Tillingham Marshes (TM)
  - Morecambe Bay: Cartmel Sands (CS), Warton Sands (WS), West Plain (WP)
- Coordinates provided for each site (approximate lat/long).
- Seasons: Winter (W) and Summer (S) 2013; Essex winter sampling window noted separately (2–6 March 2013).

## Habitat and Site Context
- Saltmarsh sites chosen to represent contrasting soil types:
  - Essex: clay soils
  - Morecambe Bay: sandy soils
- Regional differences in inundation, creek structure, and dominant vegetation.
- Grazing context:
  - Essex sites grazed by hare and Brent geese.
  - Morecambe Bay sites grazed by sheep (Cartmel Sands, Warton Sands) with winter grazing by geese; some areas lightly grazed.

## Sampling and Laboratory Methods
- Procedure:
  - 10 g soil mixed with 25 ml deionised water (1:2.5 dilution).
  - Shaken ~30 minutes; conductivity measured at 20°C using a Jenway 4320 meter.
  - Electrical conductivity used as a salinity proxy; raw value multiplied by 2.5 to correct for dilution.
- Calibration: not applicable/readily stated as none.
- Data quality control: not explicitly described.

## Variables and Data Structure
- Key variable: Electrical conductivity (mS cm^-1) as a proxy for salinity.
- Data fields (as described in dataset metadata):
  - Row Number (sorting index)
  - Season (Winter W / Summer S)
  - Location (Morecambe M / Essex E)
  - Site (CS, WS, WP for Morecambe; AH, FW, TM for Essex)
  - Habitat (Mudflat MF / Saltmarsh SM)
  - Quadrat Number (1–22)
  - Scale (A = 1 m; B = 1–10 m; C = 10–100 m; D = 100–upper limit)
  - Electrical (raw mS cm^-1, uncorrected)
- File format: Excel workbook (conductivity data), with a corrected value column derived by multiplying raw conductivity by 2.5.

## Data Access and Documentation
- Staff responsible: Hilary Ford.
- Dataset describes field procedures, site descriptions, and the translation of lab measurements to a GIS-ready format (per-quadrat, spatial scales, and site metadata).

## GIS Relevance and Potential Uses
- Enables spatial visualization of salinity proxies across saltmarsh and mudflat habitats at multiple sites.
- Facilitates aggregation by site, habitat, season, or scale (A–D) for landscape-level analyses in GIS.
- Supports investigations into how grazing regimes, soil type, and inundation influence salinity patterns.

## Limitations and Considerations
- Calibration procedures and quality control details are limited in the metadata.
- Temporal coverage is restricted to 2013 (Winter and Summer, with an additional Essex winter window).
- Coordinate reference system not specified; coordinates are given but CRS would need to be defined for GIS use.