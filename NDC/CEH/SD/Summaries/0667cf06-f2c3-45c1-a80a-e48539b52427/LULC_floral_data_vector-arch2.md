# Map showing land-use/land-cover and floral cover across an arable landscape centred on the Hillesden Estate, Buckinghamshire, UK

## Purpose and scope
- Creates a land-use/land-cover (LULC) map for a 20 km² agricultural landscape centered on Hillesden Estate, UK.
- Integrates remote-sensed data with field survey data on floral cover to support environmental monitoring, particularly pollinator habitat assessment.
- Part of the Centre for Ecology and Hydrology project funded under the Insect Pollinators Initiative.

## Data sources and sensors
- LiDAR: Optech ALTM (surface height to canopy height) collected by NERC ARSF; 1 pulse per m²; captured August 28, 2007 at ~1190 m altitude.
- Hyperspectral: AISA Eagle (252 bands, 400–970 nm) collected by ARSF; processed to aid vegetation discrimination.
- Aerial photography and field surveys used for validation and updates.

## Experimental design and sampling
- Remote-sensed data processed into 0.5 × 0.5 m grids.
- 30 land-cover classes derived from 22 selected hyperspectral bands via maximum likelihood classification; combined with LiDAR height to differentiate spectrally similar land covers.
- Simplified to 10 LULC classes: crop, short grass, mixed low vegetation, deciduous trees, field margin, road, hedge, building, water, bare soil/mud.
- Field surveys conducted July–August 2011 to determine floral cover for discrete habitat parcels; spring habitat map built from stratified random samples in April 2011 and 2012.
- For 6.5% of area inaccessible due to landowner restrictions, floral data were estimated using means from surrounding parcels of the same LULC class within 500 m.

## Floral data collection and calculation
- Surveyors measured vegetative cover (%) and proportion in flower for 28 plant groups.
- Floral cover (%) for each group = vegetative cover × proportion in flower.
- Floral cover summed to produce:
  - Su_all: all recorded plant groups in summer
  - Su_NC: non-crop plant groups in summer
  - Su_WV: worker-visited plant groups in summer
  - Su_WP: worker-preferred plant groups in summer
  - Sp_all: all groups in spring
  - Sp_QV: queen-visited plant groups in spring
- 18.7 km² of landscape fully surveyed; remaining 6.5% estimated from comparable parcels.

## Data structure and formats
- Spatial data converted from raster to vector to enable attribute calculations.
- Output stored as an ArcGIS shapefile (EIDC) with 7562 polygons, each representing a discrete habitat parcel.
- Key attributes:
  - FID: unique feature ID
  - Shape: polygon geometry
  - Full_Code: field-survey link to remote-sensed data
  - LULC: 10-class category (e.g., Arable, Bare ground, Mixed Vegetation, Hedge, etc.)
  - Floral cover attributes: Su_all, Su_NC, Su_WV, Su_WP, Sp_all, Sp_QV, etc.
- Data projection: British National Grid.

## Analytical workflow and tools
- Remote-sensing processing: ERDAS Imagine; canopy height model from LiDAR data.
- GIS processing and map updates: ESRI ArcGIS (v9.3–v10.1).
- Data integration: linking floral survey results to corresponding LULC polygons; annual updates based on field data and landowner information.

## Outputs and potential uses for environmental monitoring
- A high-resolution LULC map tied to quantified floral resources per habitat parcel.
- Enables assessment of pollinator habitat quality and floral resource distribution across an arable landscape.
- Supports monitoring of environmental health and policy performance over time by providing standardized, reproducible datasets suitable for time-series analyses.

## Quality assurance and validation
- Data validation against aerial photography and field survey data conducted during QA.
- Manual map updates performed in ArcGIS with input from field surveys and landowner information.
- Floral data quality checked by CEH botanists; cross-validated during project progress.

## Access, reuse, and metadata
- Dataset structured for broad GIS compatibility (shapefile with accompanying tabular data).
- Designed to be stored and accessible through standard environmental data portals and GIS workflows.

## Reference framework and related work
- Methodology linked to broader research on pollinator-friendly habitats; reference to Broughton et al. (2014) on agri-environment schemes and biodiversity outcomes.