# Modelled potential carbon storage based on land cover and published carbon storage values in urban landscapes of the South Midlands

## Aim
- Model potential carbon storage as an ecosystem service across urban areas of Milton Keynes/Newport Pagnell, Bedford, and Luton/Dunstable, UK.
- Compare model results using input data at two spatial scales (5 m and 25 m).

## Data and inputs
- InVEST 3.1.0 ecosystem service models used to estimate carbon storage.
- Land cover inputs as two rasters:
  - 5 m resolution: derived from colour infrared aerial photography (LandMap Bluesky) with NDVI-based vegetation separation; buildings and water from OS MasterMap; vegetation classified into broadleaf trees, coniferous trees, and grass/herbaceous; data resampled to 5 m for modelling.
  - 25 m resolution: raster OS Land Cover Map 2007 (Digimap 2007).
- Carbon storage values by land cover drawn from published literature:
  - Aboveground carbon: Davies et al. (2011).
  - Soil carbon: Edmondson et al. (2014).
- Outputs in the form of two GeoTIFF raster maps with accompanying metadata; units are kilograms of carbon per square meter (kg C/m^2).

## Modelling approach
- Use InVEST 3.1.0 to estimate urban carbon storage as an ecosystem service.
- Parameterisation based on literature values for urban land cover; assess sensitivity to input data scale by comparing 5 m vs 25 m inputs.
- Quality control focus on theoretical soundness and comparability with other UK/European studies; no physical field measurements available at comparable scale for empirical validation.

## Outputs
- Two GeoTIFF raster files (5 m and 25 m analyses) plus metadata and spatial information required for software use.
- Clear presentation of results and conclusions in reports, with data sources tracked.

## Validation and limitations
- No direct empirical validation due to lack of comparable-scale soil/aboveground carbon measurements at the time.
- Informal quality control; results are evaluated for consistency with published studies rather than ground-truth verification.
- Acknowledges potential scale-related impacts on modelling outcomes (as explored by comparing 5 m and 25 m inputs).

## Data sources and references
- Modelling framework: InVEST 3.1.0 (Tallis et al. 2014; Natural Capital Project).
- Primary data sources for land cover:
  - 5 m: LandMap Bluesky CIR aerial imagery (2009–2010 dates vary by area).
  - 25 m: OS Land Cover Map 2007 (Digimap 2007).
  - Buildings and water: OS MasterMap.
- Vegetation classification: NDVI-based separation and eCognition (Trimble 2011).
- Published carbon storage values by land cover:
  - Davies ZG, Edmondson JL, Heinemeyer A, et al. (2011).
  - Edmondson JL, Davies ZG, McCormack SA, et al. (2014).
- Related methodological context: Grafius DR, Corstanje R, Warren PH, et al. (2016) on the impact of land use/land cover scale on urban ecosystem service modelling.
- Additional references and software/tool notes:
  - Landmap; Bluesky (2014) CIR data for England and Wales.
  - Digimap (2007) Land Cover Map 25m.