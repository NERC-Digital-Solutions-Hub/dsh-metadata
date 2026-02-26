# Map showing land-use/land-cover and floral cover across an arable landscape centred on the Hillesden Estate, Buckinghamshire, UK

## Overview
- A land-use/land-cover (LULC) map of a ~20 km² agricultural landscape surrounding the Hillesden Estate, UK.
- Combines remote-sensing data (LiDAR and hyperspectral) with manual field updates and floral-cover data from comprehensive field surveys.
- Project led by the Centre for Ecology and Hydrology (CEH), funded under the Insect Pollinators Initiative.

## Data sources and remote sensing
- Remote sensing collected by the NERC Airborne Research and Survey Facility (ARSF) on 28 August 2007 under full leaf canopy.
- LiDAR: Optech 3033; ground sampling rate ~1 pulse/m²; used to create canopy height models.
- Hyperspectral: AISA EAGLE with 252 bands (400–970 nm); 30 selected bands used for vegetation discrimination.
- Data processed to 0.5 × 0.5 m grids; ERDAS Imagine and ArcGIS used for processing and analysis.

## Field surveys and floral cover data
- Manual updates to LULC in ArcGIS based on field surveys (July–August 2011) and landowner information.
- Every mapped habitat parcel (7562 polygons) surveyed to estimate percentage vegetative cover and percentage in flower for 28 plant groups.
- Floral cover calculated for multiple subsets:
  - Su_all, Su_NC, Su_WV, Su_WP (summer; various plant groups)
  - Sp_all, Sp_QV (spring; queen-visited groups)
- Spring habitat map developed from stratified random sub-samples in April 2011 and 2012; unsampled parcels estimated using surrounding parcel data.

## Data structure and outputs
- Land-use and floral data converted from raster to vector; stored as an ArcGIS shapefile (EIDC) with 7,562 polygons.
- Attributes include:
  - LULC class (e.g., Arable, Bare ground, Gardens and urban vegetation, Mixed vegetation, Roads and buildings, Short grass, Water/Waterside, Woody, etc.)
  - Full_Code linking floral data to remote-sensed data
  - Floral cover metrics (Su_all, Su_NC, Su_WV, Su_WP, Sp_all, Sp_QV) and related fields
- Data format suitable for GIS applications; underlying tabular data (.dbf) accessible to standard software.

## Processing and software
- Data handling: ERDAS Imagine (v9.0) for initial processing; ArcGIS (v9.3–10.1) for map updates and integration.
- Workflow combined LiDAR-derived canopy height with hyperspectral land-cover discrimination to produce a 10-class LULC map, then refined using field-derived floral data.

## Applications for monitoring frameworks
- Integrates landscape structure (LULC) with floral-resource availability, enabling assessment of pollinator habitat quality across landscapes.
- Provides a reproducible framework for evaluating habitat value of different land uses and the effectiveness of agri-environment schemes.
- Data can inform policy-relevant monitoring of environmental health indicators, such as pollinator resources, habitat connectivity, and change in floral resources over time.

## Data quality, governance, and accessibility
- Quality checks include error verification against aerial photography and field surveys; verifications conducted by CEH staff.
- Data openly linked to metadata through field, remote-sensing, and GIS provenance; however, as a project-specific dataset, governance and sharing policies should be defined at the use-case level.
- Explicit effort to ground remote-sensed classifications in in-field measurements to improve reliability and interpretability for policy monitoring.

## Limitations and challenges
- Some area not surveyed (6.5%), mainly pasture and edge-access areas; floral data for these polygons estimated from similar surrounding parcels.
- The need to transform and harmonize datasets (raster to vector, ensure compatibility with various GIS platforms) can require careful metadata and documentation.
- Ongoing data updates and ensuring currency of floral and LULC information are needed to maintain usefulness for monitoring.

## References
- Broughton, R.K., Shore, R.F., Heard, M.S., Amy, S.R., Meek, W.R., Redhead, J.W., Turk, A. & Pywell, R.F. (2014) Agri-environment scheme enhances small mammal diversity and abundance at the farm-scale. Agriculture, Ecosystems & Environment, 192, 122-129.