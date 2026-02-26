# Modelled potential carbon storage based on land cover and published carbon storage values in urban landscapes of the South Midlands

- The project models potential carbon storage in urban areas of Milton Keynes/Newport Pagnell, Bedford, and Luton/Dunstable, UK, using the InVEST 3.1.0 ecosystem service model.
- Output consists of two GeoTIFF raster map files (5 m and 25 m resolutions) plus associated metadata and spatial information files necessary for GIS use.
- Units are kilograms of carbon per square meter (kg C/m²).

## Overview and purpose
- Aimed to map carbon storage as an ecosystem service and to assess how input data scale (5 m vs 25 m) affects model results.
- No ground-truth measurements were available at comparable scales for empirical validation; emphasis was on theoretical model structure and comparability with similar studies.

## Data products
- Two raster maps (GeoTIFF) representing modeled carbon storage at 5 m and 25 m resolutions.
- Associated metadata and spatial information files required for software compatibility.
- Maps designed for viewing/manipulation in Geographic Information Systems.

## Methodology
- Model: InVEST 3.1.0 (Integrated Valuation of Environmental Services and Tradesoffs).
- Land cover inputs:
  - 5 m: derived from color infrared aerial photography (LandMap Bluesky, CIR, 0.5 m originally; 5 m resampled for analysis).
  - 25 m: raster OS Land Cover Map 2007 (Digimap 2007) used to represent widely available datasets.
- Carbon storage values:
  - Aboveground carbon: literature value from Davies et al. (2011) for urban areas.
  - Soil carbon: literature value from Edmondson et al. (2014).
- Land cover classification (5 m) components:
  - Buildings, water (from OS MasterMap).
  - Paved surfaces separated from vegetation via NDVI threshold.
  - Vegetation categorized into broadleaf trees, coniferous trees, grass/herbaceous using eCognition (Trimble 2011).
- Processing steps:
  - Cir imagery used to generate 5 m land cover; resampling performed for consistency.
  - 25 m map based on existing 2007 land cover datasets.
- Model outputs express carbon storage per unit area using the specified land cover–carbon conversion values.

## Data sources and processing details
- Vegetation and land cover sources:
  - LandMap ( Bluesky 2014) CIR aerial imagery for 5 m analysis.
  - OS MasterMap for buildings and water features.
  - NDVI thresholding to separate vegetation from paved surfaces.
  - eCognition (Trimble 2011) for vegetation class segmentation.
  - OS Land Cover Map 2007 (Digimap 2007) for 25 m analysis.
- Published carbon storage references:
  - Davies et al. (2011) for aboveground carbon.
  - Edmondson et al. (2014) for soil carbon.

## Model and software context
- InVEST 3.1.0 User’s Guide and ecosystem services framework as the underlying approach.
- The Natural Capital Project is the source of the InVEST toolkit.
- Data formats suitable for GIS workflows (GeoTIFF with accompanying metadata).

## Data quality, limitations, and validation
- Quality control described as informal; no empirical ground-truth validation available at comparable scales.
- Results were checked for general consistency with published UK/European studies but rely on theoretical model structure rather than direct measurement.
- Noted that input data scale (5 m vs 25 m) can influence model outcomes; the study explicitly explores this sensitivity.

## Data management, metadata, and discoverability
- Data provided with metadata and spatial information files required by GIS software, enhancing discoverability and reusability.
- Raster formats (GeoTIFF) chosen to facilitate broad access and integration with standard GIS tools.

## Potential uses and cautions for data leaders
- Suitable for ecosystem service assessment, urban planning, and policy discussions around carbon storage in urban landscapes.
- Useful for comparing how data resolution affects ecosystem service outcomes and for informing data collection priorities in urban areas.
- Users should be aware of the informal quality control and lack of ground-truth validation when applying results to decision-making; consider augmenting with local measurements where possible.

## References
- Davies ZG, Edmondson JL, Heinemeyer A, et al. (2011). Mapping an urban ecosystem service: Quantifying above-ground carbon storage at a city-wide scale. Journal of Applied Ecology.
- Edmondson JL, Davies ZG, McCormack SA, et al. (2014). Land-cover effects on soil organic carbon stocks in a European city. Science of the Total Environment.
- Grafius DR, Corstanje R, Warren PH, et al. (2016). The impact of land use/land cover scale on modelling urban ecosystem services. Landscape Ecology.
- Tallis HT, Ricketts T, Guerry AD, et al. (2014). InVEST 3.1.0 User’s Guide.
- Digimap (2007). Land Cover Map 25m.
- Landmap; Bluesky (2014). Colour Infrared data for England and Wales.
- Trimble (2011). eCognition Developer.