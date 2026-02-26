# A modelled dataset derived from national datasets, describing the distribution of woody linear feature boundaries in Great Britain

## Overview
- Provides national coverage of woody linear features (hedges and lines of trees) in Great Britain via a predictive modelling approach, circumventing the need for costly field mapping.
- Aims to support GIS-based analyses and map-based data products for biodiversity, landscape function, and policy/societal audiences.

## What the dataset represents
- Linear features with a high likelihood of being woody, identified within a linear framework built from a simplified OS MasterMap used in Land Cover Map 2007.
- Boundaries selected by applying masking (areas unlikely to contain woody features: elevations >350 m, urban areas, woodland, coastal tidal zones) and height-based criteria derived from a 5 m digital elevation model.

## How it was created (Method)
- Data sources:
  - OS MasterMap Land-Form Panorama
  - Land Cover Map 2007
  - NEXTMap 5 m digital elevation data
- Processing steps:
  - Mask areas where woody features are unlikely to be detected.
  - Compute boundary height attributes from the DEM; apply height thresholds for vegetation along the boundary:
    - Minimum vegetation height: -0.13 m
    - Maximum vegetation height: 58 m
    - Mean vegetation height: 0.58 m
  - Classify and output features with a high likelihood of being woody linear features.
- Scale and validation:
  - National-scale outputs are concordant with Countryside Survey (CS) results and published statistics.
  - Validation and comparison across scales discussed in Scholefield et al. (2016).

## Dataset structure
- Data type: vector with SHAPE as Geometry
- SHAPE_LENGTH: numeric, length of each feature in metres
- Geometry: POLYLINE representing the woody linear feature boundary

## Data sources and rights
- OS MASTERMAP, OS LAND-FORM PANORAMA (Public Sector Mapping Agreement; reproduced by permission)
- NEXTMAP Digital Elevation Data
- Countryside Survey 2007 mapped estimates of linear feature lengths in Great Britain
- Copyright and licence notes:
  - Crown Copyright, dataset 2016; Licence number 100017572

## Practical use for GIS specialists
- Enables inclusion of hedgerows and woody boundaries in GIS analyses, landscape connectivity models, and biodiversity assessments where field data are sparse.
- Allows integration with other raster/vector datasets while handling differing resolutions and data quality.

## Limitations and caveats
- Based on model predictions rather than exhaustive field mapping; inherent uncertainties in boundary delineation.
- Data coverage limited to areas where the masking and height-based approach can reliably detect features.
- Requires consideration of data provenance and licensing when combining with other datasets.

## References and further reading
- Carey et al. (2008) Countryside Survey: UK results from 2007
- Morton et al. (2011) Final report for LCM2007 – The New UK Land Cover Map
- Scholefield et al. (2016) A model of the extent and distribution of woody linear features in rural Great Britain (and related materials)
- Brown et al. (2014) Countryside Survey 2007 mapped estimates of linear feature lengths in Great Britain