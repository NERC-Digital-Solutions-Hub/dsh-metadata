# Modelled potential carbon storage based on land cover and published carbon storage values in urban landscapes of the South Midlands

## Overview
- Study area: urban regions of Milton Keynes/Newport Pagnell, Bedford, and Luton/Dunstable in the South Midlands, UK.
- Objective: model potential carbon storage as an ecosystem service using land cover data at two spatial resolutions (5 m and 25 m) and published carbon storage values by land cover.
- Outputs: two GeoTIFF raster map files (with metadata and spatial information) representing carbon storage; units are kilograms of carbon per square meter (kg C/m^2).
- Modelling framework: InVEST 3.1.0 to estimate carbon storage across the urban landscape and to compare effects of input data scale on results.

## Data inputs and processing
- 5 m analysis
  - Land cover map created from colour infrared aerial photography at ~0.5 m resolution (LandMap CIR) with imagery dates: Bedford (2 Jun 2009), Luton (30 Jun 2009; 24 Apr 2010), Milton Keynes (8–15 Jun 2007; 2 Jun 2009).
  - Buildings and water features identified from UK Ordnance Survey MasterMap; paved surfaces separated from vegetation using NDVI threshold.
  - Vegetation classified into broadleaf trees, coniferous trees, and grass/herbaceous via image segmentation in eCognition.
  - Land cover map resampled to 5 m for modelling.
- 25 m analysis
  - Based on raster OS Land Cover Map 2007 (Digimap 2007) as the land cover input.
- Carbon storage values
  - Aboveground carbon: Davies et al. (2011).
  - Soil carbon: Edmondson et al. (2014).
  - Both sources provide published urban land cover–specific storage values used in the model.
- Model inputs and outputs
  - InVEST 3.1.0 User’s Guide and Natural Capital Project resources used to configure modelling.
  - Outputs are two GeoTIFF raster maps plus associated metadata and spatial information suitable for GIS analysis.

## Modelling approach and scale comparison
- Aim: quantify carbon storage as an ecosystem service across the study area and assess the impact of input data scale on model results (5 m vs 25 m).
- Approach relies on established data sources and standard modelling parameters to ensure comparability with similar urban studies.

## Quality control and limitations
- Quality control: informal checks; model results were compared with published studies from other UK/European locations for consistency.
- Limitations: no direct empirical soil or aboveground carbon measurements were available at comparable scale for validation at the time; emphasis placed on the theoretical structure and comparability of model parameters and outputs.

## Relevance for environmental monitoring and use
- Provides a standardized, reproducible method to estimate urban carbon storage across multiple cities and resolutions.
- Facilitates monitoring of carbon storage changes over time and supports policy discussions on urban carbon management and land cover planning.
- The dual-scale analysis aids analysts in understanding how input data resolution affects estimated carbon storage, informing data selection for future monitoring efforts.