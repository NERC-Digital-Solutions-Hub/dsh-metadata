# Map showing land-use/land-cover and floral cover across an arable landscape centred on the Hillesden Estate, Buckinghamshire, UK

## Overview
- LULC map for a 20 km² agricultural landscape centered on the Hillesden Estate, Buckinghamshire, UK.
- Combines remote-sensed data (LiDAR and hyperspectral) with extensive floral cover data from field surveys.
- Produced as part of a project led by the Centre for Ecology and Hydrology (CEH), funded under the Insect Pollinators Initiative.

## Data collection and sources
- Remote sensing data collected by the NERC Airborne Research and Survey Facility (ARSF) on 28 August 2007 under full leaf canopy.
  - LiDAR: Optech 3033, 1 pulse per m², canopy height model derived from maximum elevation in each 0.5 × 0.5 m cell.
  - Hyperspectral: AISA EAGLE with 252 bands; 22 bands used to derive 30 land cover classes.
- Data processed into 0.5 × 0.5 m grids; fused with height information to distinguish spectrally similar classes by height.
- Manual updates to the map conducted in ArcGIS based on field surveys and landowner information.
- Floral cover data added from field surveys of target plant groups conducted to assess habitat value for bumblebees (spring and summer).

## Floral data collection and sampling
- Field surveys of discrete habitat parcels conducted July–August 2011; 18.7 km² surveyed.
- A stratified random sub-sample of parcels surveyed in April 2011 and 2012 to inform spring habitat map.
- For each polygon, vegetative cover (%) and proportion in flowering for 28 plant groups recorded; floral cover (%) computed as cover × flowering proportion.
- Floral cover sums created for group subsets: all plants, non-crop plants, worker-visited plants, worker-preferred plants (summer), plus spring metrics (all plants, queen-visited plants).
- For 6.5% of the area not surveyed (primarily pasture and edge areas), floral data estimated using mean values from surrounding parcels of the same LULC class within 500 m.

## Data processing and transformation
- Raster data converted to vector format to enable calculation and linkage of floral attributes.
- Processing tools: ERDAS Imagine (v9.0) for initial handling; ArcGIS (v9.3–10.1) for updates and data management.
- Final dataset stored as an ArcGIS shapefile (EIDC) with 7,562 polygons, each representing a discrete habitat parcel.

## Data structure and attributes
- Core polygon attributes:
  - FID: unique feature ID
  - Shape: polygon geometry
  - Full_Code: field survey code linking floral data to remote-sensed data
  - LULC: land-use/land-cover class (10 classes, e.g., Arable, Bare ground, Gardens and urban vegetation, Mixed vegetation, Roads and buildings, Short grass, Water/Waterside, Woody, etc.)
  - Floral cover attributes for summer and spring subsets (Su_all, Su_NC, Su_WV, Su_WP, Sp_all, Sp_QV)
- Floral cover is expressed as percentage cover per polygon.

## Quality assurance and validation
- Data quality checked at all stages by CEH staff.
- Validation included cross-checks against aerial photography and field survey results.
- Manual updates and corrections incorporated from field surveys and landowner information.

## Coverage, units, and accessibility
- Spatial resolution: remote-sensed data in 0.5 × 0.5 m cells; results converted to vector polygons for analysis.
- Projection: British National Grid.
- Output: shapefile with 7,562 habitat parcels; widely usable in GIS software (readable via .shp/.dbf).

## Experimental design and context
- Integrated remote sensing with targeted field floristic surveys to map floral resources across the landscape.
- The combination of LiDAR-derived height data and hyperspectral reflectance allowed subdivision of spectrally similar land covers by height (e.g., hedges vs trees; buildings vs roads).
- Spring and summer floral data provide a habitat-quality layer for pollinators, enabling analyses of habitat value and potential pollinator resources.

## References
- Broughton, R.K. et al. (2014) Agri-environment scheme enhances small mammal diversity and abundance at the farm-scale. Agriculture, Ecosystems & Environment, 192, 122–129.