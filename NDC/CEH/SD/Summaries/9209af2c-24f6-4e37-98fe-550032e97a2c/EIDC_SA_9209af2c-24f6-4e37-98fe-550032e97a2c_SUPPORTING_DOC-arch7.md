# Modelled potential carbon storage based on land cover and published carbon storage values in urban landscapes of the South Midlands

## Overview
- Modelling potential carbon storage for urban areas in Milton Keynes/Newport Pagnell, Bedford, and Luton/Dunstable, UK.
- Uses InVEST 3.1.0 ecosystem service model to estimate carbon storage as an urban ecosystem service.
- Compares model results across two input data resolutions (5 m and 25 m).

## Data inputs and preprocessing
- Land cover inputs:
  - 5 m resolution: created from Colour Infrared (CIR) aerial photography (0.5 m) from LandMap; dates vary by city.
  - 25 m resolution: raster OS Land Cover Map 2007 (Digimap 2007).
- Ancillary data:
  - Buildings and water features derived from UK Ordnance Survey MasterMap.
  - Paved surfaces separated from vegetation using a Normalised Difference Vegetation Index (NDVI) threshold.
- Vegetation classification (5 m):
  - Broadleaf trees, coniferous trees, grass/herbaceous via image segmentation in eCognition (Trimble 2011).
- Processing:
  - 5 m land cover map resampled to 5 m for modelling; alignment across data types facilitated feasibility.
- Scale comparison focus: evaluation of how input data scale (5 m vs 25 m) affects model outputs.

## Carbon storage values and literature basis
- Published literature values used for urban land cover carbon storage:
  - Aboveground carbon: Davies et al. (2011).
  - Soil carbon: Edmondson et al. (2014).

## Modelling framework
- InVEST 3.1.0 User’s Guide and model suite used to estimate ecosystem services (carbon storage) with user-supplied parameters.
- Model parameters and results intended to be comparable with other UK/European studies.

## Outputs
- Two GeoTIFF raster map files representing potential carbon storage.
- Associated metadata and spatial information files required by GIS software.
- Units: kilograms of carbon per square meter (kg C/m^2).

## Quality assurance and validation
- Quality control conducted informally; model results compared to published literature from other UK/European locations.
- No empirical field measurements available at a scale comparable to validate results; emphasis on theoretical soundness of model structure and parameters.

## Study area
- Urban landscapes covered: Milton Keynes/Newport Pagnell, Bedford, and Luton/Dunstable in the South Midlands.

## Software, data sources, and references
- Software/tools:
  - InVEST 3.1.0 (Integrated Valuation of Environmental Services and Tradeoffs).
  - eCognition (for image segmentation and vegetation classification).
- Data sources:
  - CIR aerial imagery from LandMap Spatial Discovery project (Bluesky, 2014).
  - OS MasterMap for buildings and water.
  - NDVI-based vegetation separation.
  - OS Land Cover Map 2007 (25 m).
- References include:
  - Davies et al. (2011); Edmondson et al. (2014); Grafius et al. (2016); Tallis et al. (2014); Landmap/Blu sky (2014); Trimble (2011); Digimap (2007); and related works.