# Benthic organic matter of Welsh upland rivers in response to organic matter addition

## Overview
- Investigates how benthic organic matter (BOM) stocks respond to added leaf litter in Welsh upland rivers using a before-after-control-impact (BACI) design.
- Focuses on spatially-referenced BOM data collected across paired upstream (reference) and downstream (experimental) zones within each stream.
- Data suitable for GIS analysis and map-based visualisation of BOM stocks by site, time, and treatment.

## Experimental design
- BACI setup: Each stream divided into an upstream reference zone and a downstream experimental zone.
- Zones similar in length, habitat structure, slope, flow, substratum, and land use; ~20–50 m separation to ensure independence.
- Time periods:
  - Before period (T1): 61–65 days (early Nov 2012 to early Jan 2013); no manipulation; both zones treated equally.
  - After period (T2): 57–62 days (early Jan 2013 to Mar 2013); experimental zone receives leaf litter addition.
- Leaf litter manipulation:
  - One tonne bags containing oak, birch, and alder leaves added proportionally to match experimental zone area.
  - Vegetable net bags maintained to ensure ~1.7 kg m^-2 wet weight of leaf litter in the experimental zone.
  - Additional leaf litter (630 kg wet weight) added on 12 Feb 2013 and 5 Mar 2013 after two large storm events.
- Sampling periods:
  - Sampling occurred in January, February, March, April, and May 2013.

## Sampling and collection methods
- BOM collection: Six random samples per reach per occasion using a Surber net (area 0.1 m^2; mesh 330 µm; depth 10 cm).
- Preservation: On-site in 70% IMS; lab processing involves separating macroinvertebrates, drying, and weighing the remaining material.
- Processing: Samples dried to constant weight, corrected for inorganic content via ash-free conversion (subset combusted at 550°C for 5 h).
- Measurements: Coarse and fine particulate organic matter (CPOM and FPOM) weighed to 0.01 g.

## Analytical methods and units
- Primary measurements: BOM stocks (grams) of CPOM and FPOM.
- Additional details:
  - Surber net specifics provided for field sampling.
  - Weighting performed to nearest 0.01 g.
- Calibration steps: None reported.
- Quality control: None reported.

## Data structure and format
- Data format: Flatbed comma-separated value (CSV) files.
- Main BOM dataset (10 columns):
  - site_code: sampling site identifier
  - landuse: basin land-use
  - region: stream basin
  - time: Before or After manipulation
  - month: sampling month
  - reach: Experimental or Control site
  - replicate: replication code
  - surber_area: area of the Surber sampler (m^2)
  - cpom: coarse particulate organic matter (grams)
  - fpom: fine particulate organic matter (grams)
- Supplementary file: site_description.csv (10 columns) with geospatial and survey details:
  - site_code, Name, Eastings, Northings, Grid, Latitude, Longitude, Elevation
  - Survey, Catchment
- Data focus: BOM stocks by site, time period, and treatment (Upstream Reference vs Downstream Experimental).

## Site metadata and geospatial information
- Site description includes precise location data (grid references, latitude/longitude, Eastings/Northings, elevation) enabling GIS mapping and spatial analyses.
- Catchment and survey metadata linked to each site for contextual interpretation.

## Notes and considerations
- No calibration or quality-control steps were recorded.
- Data structure supports integration with GIS workflows to explore spatial patterns of BOM response to organic matter addition across streams and time.