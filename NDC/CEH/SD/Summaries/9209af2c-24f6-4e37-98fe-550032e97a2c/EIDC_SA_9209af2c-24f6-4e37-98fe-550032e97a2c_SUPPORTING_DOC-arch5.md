# Modelled potential carbon storage based on land cover and published carbon storage values in urban landscapes of the South Midlands

## Overview
- Modelling potential carbon storage for urban areas of Milton Keynes/Newport Pagnell, Bedford, and Luton/Dunstable, UK.
- Uses InVEST 3.1.0 to estimate ecosystem service provision (carbon storage) from land cover data at two spatial resolutions (5 m and 25 m).
- Data presented as two GeoTIFF raster files with accompanying metadata and spatial information; units are kilograms of carbon per square meter (kg C/m²).

## Data products
- Two GeoTIFF raster maps (5 m and 25 m) representing modeled carbon storage.
- Associated metadata and spatial information files required by GIS software.
- Documentation aligned with the InVEST modelling framework and literature values.

## Data sources and inputs
- Land cover inputs:
  - 5 m analysis: land cover map created from colour infrared aerial photography (0.5 m resolution) from LandMap Spatial Discovery; imagery dates: Bedford (2 Jun 2009), Luton (30 Jun 2009 and 24 Apr 2010), Milton Keynes (8–15 Jun 2007 and 2 Jun 2009).
  - 25 m analysis: raster OS Land Cover Map 2007 (Digimap 2007).
  - Built and water features derived from UK Ordnance Survey MasterMap; paved surfaces separated from vegetation via normalised difference vegetation index (NDVI) threshold; vegetation classified into broadleaf trees, coniferous trees, and grass/herbaceous (via eCognition).
- Carbon storage values:
  - Aboveground carbon: Davies et al. (2011).
  - Soil carbon: Edmondson et al. (2014).
- Modelling framework: InVEST 3.1.0 User’s Guide (Tallis et al., 2014).
- Supporting sources and data provenance indexed in references.

## Modelling approach and tools
- Purpose: quantify urban carbon storage as an ecosystem service and compare the effect of input data scale (5 m vs 25 m).
- Methodology: parameterised InVEST models using land cover inputs and published carbon storage values by land cover type.
- Quality control: informal rather than rigorous empirical validation; model results compared with published UK/European studies for conceptual soundness and comparability.
- Data processing: land cover reclassification and segmentation to align with modelling needs; resampling to a consistent 5 m resolution for modelling and analysis.

## Provenance, metadata, and governance
- Data created for specific study area and published with metadata and spatial information files necessary for GIS workflows.
- Documentation references primary modelling framework (InVEST) and the literature underpinning the carbon storage values.
- Clear traceability of inputs ( imagery dates, data sources, NDVI-based classification) and outputs (GeoTIFFs with unit, scale, and spatial reference).

## Quality, validation, and limitations
- No direct physical measurements of soil or aboveground carbon at comparable scale available for validation at the time; reliance on literature-based carbon storage values.
- Informal quality control, with emphasis on theoretical model structure and cross-study comparability rather than empirical validation.
- Potential limitations related to:
  - Differences in input data quality across 5 m and 25 m datasets.
  - Use of legacy OS and LandMap data with varying resolutions and coverage.
  - Uncertainties in land cover classification and NDVI-based separation of surfaces.

## Reuse, access, and governance considerations
- Data are suitable for GIS-based analysis of urban carbon storage and ecosystem service assessment.
- Units are kg C/m²; two spatial resolutions enable scale-specific analysis and comparison.
- Stakeholders (data stewards, researchers, city planners) should note provenance, data sources, and limitations when applying results to policy or planning.
- Consider updating or refreshing inputs if new land cover or carbon storage parameter values become available; maintain metadata to reflect any changes.

## References
- Davies ZG, Edmondson JL, Heinemeyer A, et al. (2011). Mapping an urban ecosystem service: Quantifying above-ground carbon storage at a city-wide scale. Journal of Applied Ecology, 48, 1125-1134.
- Digimap (2007). Land Cover Map 25m. 1:250000.
- Edmondson JL, Davies ZG, McCormack SA, et al. (2014). Land-cover effects on soil organic carbon stocks in a European city. Science of the Total Environment, 472, 444-453.
- Grafius DR, Corstanje R, Warren PH, et al. (2016). The impact of land use/land cover scale on modelling urban ecosystem services. Landscape Ecology, 31, 1509-1522.
- Landmap; Bluesky (2014). Colour Infrared (CIR) data for England and Wales.
- Tallis HT, Ricketts T, Guerry AD, et al. (2014). InVEST 3.1.0 User’s Guide.
- Trimble (2011). eCognition Developer.