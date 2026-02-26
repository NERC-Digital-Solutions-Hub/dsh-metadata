# Benthic organic matter of Welsh upland rivers in response to organic matter addition

## Overview
- A BACI design assessing how benthic organic matter (BOM) responds to added leaf litter in Welsh upland streams.
- Each stream has an upstream reference zone and a downstream experimental zone, separated to ensure independence.
- Seasonal timeline: before period (T1) November 2012–January 2013; after period (T2) January–April 2013 with leaf litter additions; additional litter added February and March 2013 after storm events.

## Experimental Design Details
- Zones: upstream reference vs downstream experimental within each stream.
- Lengths similar; 20–50 m separation between zones.
- Leaf litter manipulation: 1 tonne bags of deciduous leaves (oak, birch, alder) added proportionally to experimental zone; wet weight target ~1.7 kg/m2.
- Additional litter: 630 kg (wet weight) added on 12 February 2013 and 5 March 2013 after two large storm-flow events.

## Data Collection & Laboratory Methods
- BOM collection: six random BOM samples per reach, across five sampling occasions (January–May 2013) using Surber nets (0.1 m2, 330 µm mesh, 10 cm depth).
- On-site preservation in 70% IMS; in-lab processing to separate macroinvertebrates, dry BOM to constant weight, and correct for inorganic content via ash-free conversion.
- Unit of measurement: grams (for BOM stocks; CPOM and FPOM).

## Data Structure & Variables
- Data format: flatbed CSV with 10 columns.
- Key fields:
  - site_code: sampling site identifier
  - landuse: basin land-use
  - region: stream basin
  - time: Before or After manipulation
  - month: sampling month
  - reach: Experimental or Control site
  - replicate: replicate code
  - surber_area: area of the Surber sampler (m2)
  - cpom: coarse particulate organic matter (grams)
  - fpom: fine particulate organic matter (grams)
- Supporting dataset: site_description CSV with 10 columns including site_code, name, Eastings, Northings, Grid, Latitude, Longitude, Elevation, Survey, Catchment.

## Spatial & Temporal Context
- Geographic scope: Welsh upland rivers; mapping potential across streams and catchments.
- Geospatial details available: British National Grid references and coordinates for site locations, enabling map-based visualization of zones (reference vs experimental) and BOM metrics over time.

## GIS-Ready Use Cases
- Join BOM data (cpom, fpom) to site_description via site_code for mapping.
- Create maps showing spatial distribution of BOM before vs after leaf litter addition.
- Visualize differences between upstream reference and downstream experimental zones.
- Integrate with land-use and catchment descriptors to explore drivers of BOM changes.
- Develop time-series or change-detection maps across the T1 to T2 period.