# Modelled potential carbon storage based on land cover and published carbon storage values in urban landscapes of the South Midlands

## Overview
- Modeling urban carbon storage in Milton Keynes/Newport Pagnell, Bedford, and Luton/Dunstable (UK) using InVEST 3.1.0.
- Two spatial resolutions evaluated: 5 m and 25 m.
- Outputs: two GeoTIFF raster map files with associated metadata and spatial information; units are kilograms of carbon per square meter (kg C/m²).
- Data designed to be viewable/manipulable in GIS software.

## Data inputs and sources
- 5 m land cover map created from Colour Infrared aerial photography (0.5 m) from LandMap Bluesky (2014); dates: Bedford (2 Jun 2009), Luton (30 Jun 2009; 24 Apr 2010), Milton Keynes (8 Jun; 15 Jun 2007; 2 Jun 2009).
- Buildings and water from UK Ordnance Survey MasterMap; paved areas distinguished from vegetation using NDVI threshold.
- Vegetation classified into broadleaf trees, coniferous trees, and grass/herbaceous via image segmentation (eCognition).
- 25 m analysis used a raster OS Land Cover Map 2007 (Digimap 2007).
- Published carbon storage values by land cover type: aboveground carbon from Davies et al. (2011); soil carbon from Edmondson et al. (2014).

## Methods and workflow
- InVEST 3.1.0 employed to estimate carbon storage as an ecosystem service; also used to explore the impact of input data scale (5 m vs 25 m) on results.
- Data processing steps: formal data preparation followed by spatial modelling in InVEST.
- No physical field measurements available for validation at the study scale; emphasis on theoretical model structure and comparability with other studies.

## Outputs and products
- Two GeoTIFF raster maps (plus accompanying metadata and spatial information files) suitable for GIS use.
- Outputs express carbon storage in kg C/m² based on land cover-derived inputs and published carbon storage values.

## Quality and validation
- Quality control described as informal; model results compared to published literature from other UK/European contexts and found broadly comparable.
- Acknowledgement of absence of empirical soil/biomass measurements for direct validation at the urban scale.

## Reproducibility and references
- Software and framework: InVEST 3.1.0 (Natural Capital Project).
- Data sources and processing references include:
  - Davies ZG, Edmondson JL, Heinemeyer A, et al. (2011) for aboveground carbon storage.
  - Edmondson JL, Davies ZG, McCormack SA, et al. (2014) for soil carbon stocks.
  - Grafius DR, Corstanje R, Warren PH, et al. (2016) on scale effects in urban ecosystem service modelling.
  - Landmap Bluesky (2014) CIR data for England and Wales.
  - Tallis HT, Ricketts T, Guerry AD, et al. (2014) InVEST User’s Guide.
  - Trimble (2011) eCognition Developer.
- Full references and data provenance support reproducibility of the modelling approach.

## Limitations and caveats
- Scale effects: comparison between 5 m and 25 m inputs may influence results.
- Data quality and compatibility: 5 m map relies on high-resolution CIR imagery and segmentation; 25 m data relies on existing Land Cover data from 2007, which may be less ideal for urban modelling.
- Absence of empirical validation data at comparable spatial scales; reliance on theoretical model structure and literature alignment.

## Potential uses
- Assessment of urban carbon storage potential as an ecosystem service.
- Comparative analysis across urban areas at different data resolutions.
- Input for policy discussions on urban planning and climate-related ecosystem services.