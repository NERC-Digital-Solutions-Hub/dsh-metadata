# Map showing land-use/land-cover and floral cover across an arable landscape centred on the Hillesden Estate, Buckinghamshire, UK

## Overview
- LULC map for a 20 km² agricultural landscape centered on the Hillesden Estate, Buckinghamshire, UK.
- Combines remote sensing (LiDAR and hyperspectral data) with extensive field surveys to add floral cover information.
- Produced as part of a CEH-led project funded under the Insect Pollinators Initiative.

## Data sources and sensors
- LiDAR: Optech ALTM 3033; mean flight altitude ~1190 m; 1 pulse per square metre; canopy height model derived from surface elevations.
- Hyperspectral: AISA EAGLE with 252 bands (400–970 nm); 22 bands used for vegetation discrimination.
- Data collection conducted by the NERC ARSF in late August 2007 under full leaf canopy conditions.
- Initial processing by CEH Earth Observation scientists; subsequent validation against aerial imagery and field data.

## Experimental design and sampling
- Raster data converted to 0.5 x 0.5 m grids; LiDAR-derived height information combined with spectral data to classify land covers.
- 30 land cover classes derived via maximum likelihood on the selected 22 spectral bands; combined with height to differentiate spectrally similar classes (e.g., hedges vs trees; roads vs buildings).
- Simplified to 10 LULC classes: crop, short grass, mixed low vegetation, deciduous trees, field margin, road, hedge, building, water, bare soil/mud.
- Manual map updates performed in ArcGIS, incorporating field survey data and landowner information.

## Floral data collection and metrics
- Field surveys of discrete habitat parcels conducted in July–August 2011 to estimate floral resources.
- Spring habitat map constructed from stratified random sampling across habitat types in April 2011 and 2012.
- For each polygon, vegetative cover and proportion in flower were recorded for 28 plant groups; floral cover (%) computed as cover × flowering proportion.
- Floral data aggregated into subsets:
  - Summer: Su_all (all groups), Su_NC (non-crop), Su_WV (worker-visited), Su_WP (worker-preferred).
  - Spring: Sp_all (all groups), Sp_QV (queen-visited).
- Coverage: 18.7 km² surveyed; remaining 6.5% of area unsurveyed and estimated from the mean of surrounding parcels of the same LULC class within 500 m.

## Data structure and access
- Data converted from raster to vector to enable attribute calculations for floral data.
- Format: ArcGIS shapefile (EIDC shapefile) with 7,562 polygons, each representing a habitat parcel.
- Key attributes:
  - FID: unique feature ID.
  - Full_Code: link to floral data from field surveys.
  - LULC: one of 10 classes listed above.
  - Floral cover attributes for the various Su_* and Sp_* subsets.
- Projection: British National Grid (BNG).
- File structure: shapefile (.shp) with accompanying .dbf and other ArcGIS components; designed to be readable by common GIS tools.

## Data-processing workflow and quality control
- Remote-sensing data handled with ERDAS Imagine (v9.0); subsequent LULC updates in ESRI ArcGIS (v9.3–10.1).
- Field-derived floral data appended to the LULC map; updates and parcel-level changes incorporated from field surveys and landowner input (July–August 2011; spring surveys in 2011–2012).
- Independent error checking and validation against aerial photography and field data conducted by CEH staff.

## Data governance, provenance, and updates
- Full data provenance documented: sensor specifications, flight parameters, processing steps, and field survey methodologies.
- Updates reflect landowner information and field survey results; floral data and habitat classifications linked to corresponding LULC parcels via Full_Code.
- Data designed to be interoperable with standard GIS tools, supporting discoverability and reuse within broader data ecosystems.

## Applications and relevance for data leadership
- Demonstrates end-to-end data lifecycle: acquisition (remote sensing), processing (classification with height constraint), field validation, and iterative updates.
- Provides a robust framework for integrating user needs and field-derived attributes (flowering resources) into a broader data system focused on ecosystem services, pollinator resources, and habitat mapping.
- Highlights data standardization and metadata practices (clear class definitions, linked attributes, vectorization for analysis, and documentation of accuracy checks).

## Limitations and considerations
- Temporal gap between 2007 remote-sensing data and 2011–2012 field updates; some land-cover changes since the original data collection may not be captured.
- 6.5% of the area unsurveyed and inferred from surrounding parcels, introducing estimation uncertainty in those parcels.
- Simplification from 30 initial LULC classes to 10 final classes; users should consider the level of thematic detail required for specific analyses.
- Spatial resolution and integration with other datasets rely on the consistency of the LULC class definitions and floral subsets across the study.

## References
- Broughton, R.K., Shore, R.F., Heard, M.S., Amy, S.R., Meek, W.R., Redhead, J.W., Turk, A. & Pywell, R.F. (2014) Agri-environment scheme enhances small mammal diversity and abundance at the farm-scale. Agriculture, Ecosystems & Environment, 192, 122-129.