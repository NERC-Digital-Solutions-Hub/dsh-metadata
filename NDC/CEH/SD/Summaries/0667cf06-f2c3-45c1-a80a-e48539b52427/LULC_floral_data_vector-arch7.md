# Map showing land-use/land-cover and floral cover across an arable landscape centred on the Hillesden Estate, Buckinghamshire, UK

## Overview
- GIS-focused land-use/land-cover (LULC) map for a 20 km² agricultural landscape centered on Hillesden Estate, UK.
- Combines remote sensing (LiDAR and hyperspectral data) with manual updates and floral cover data from field surveys.
- Project led by the Centre for Ecology and Hydrology (CEH), funded under the Insect Pollinators Initiative.
- Aims to support analysis of habitats for pollinators (notably bumblebees) through integrated LULC and floral cover information.

## Data Sources and Sensors
- LiDAR: Optech ALTM 3033; surface height and canopy height modeled from 0.5 m grid cells.
- Hyperspectral: AISA EAGLE (252 bands; 400–970 nm); 0.5 x 0.5 m grid after processing.
- Data processing: ERDAS Imagine (v9.0) and ESRI ArcGIS (v9.3–10.1); validation against aerial photos and field data; manual updates in ArcGIS.
- Floral data: appended after field surveys conducted by CEH botanists.

## Experimental Design and Sampling
- Remote sensing collected on 28 August 2007 under full leaf canopy; altitude ~1190 m.
- Land cover classification: 30 classes derived from 22 EAGLE bands via maximum likelihood; height information from LiDAR used to separate spectrally similar classes (e.g., hedges vs. trees; buildings vs. roads).
- Final LULC map simplified to 10 classes: crop, short grass, mixed low vegetation, deciduous trees, field margin, road, hedge, building, water, bare soil/mud.
- Field survey scope: every discrete habitat parcel surveyed in July–August 2011 to quantify vegetative cover and flowering (% cover for 28 plant groups).
- Spring data: stratified random subsample surveyed in April 2011 and 2012 to estimate spring floral cover.
- Processing tools: ArcGIS used for updates; raster-to-vector conversion to enable floral attribute calculations.

## Floral Data Collection and Attributes
- Floral cover (%) calculated by combining vegetative cover with proportion in flower for 28 plant groups.
- Floral metrics computed per polygon:
  - Su_all: summer floral cover of all recorded plant groups
  - Su_NC: summer floral cover of non-crop groups
  - Su_WV: summer floral cover of worker-visited groups
  - Su_WP: summer floral cover of worker-preferred groups
  - Sp_all: spring floral cover of all groups
  - Sp_QV: spring floral cover of queen-visited groups
- Area coverage: 18.7 km² surveyed; remaining 6.5% unsurveyed (mostly pasture and edge areas) imputed using mean values from surrounding same-LULC parcels within 500 m.

## Data Structure and Output
- Data converted from raster to vector; ArcGIS shapefile with 7,562 polygons (habitat parcels).
- Key attributes:
  - LULC: one of the ten classes described above
  - Full_Code: field-survey linkage code to floral data
  - FID and Shape: standard GIS identifiers
  - Floral attributes: Su_all, Su_NC, Su_WV, Su_WP, Sp_all, Sp_QV
- Projection/units: British National Grid; polygonal vector features with associated floral data.

## LULC Class Categories
- Arable
- Bare ground
- Gardens and urban vegetation
- Mixed Vegetation
- No Data
- Roads and Buildings
- Short grass
- Sown floral habitat
- Water/Waterside
- Woody (hedges and trees)

## Quality Assurance and Validation
- Data processing and updates validated by CEH staff.
- Floral data validated against field survey results and cross-checked with landowner information.
- Error checking performed at all stages, including comparison with aerial photography and field data.

## References
- Broughton, R.K. et al. (2014) Agri-environment scheme enhances small mammal diversity and abundance at the farm-scale. Agriculture, Ecosystems & Environment, 192, 122-129.