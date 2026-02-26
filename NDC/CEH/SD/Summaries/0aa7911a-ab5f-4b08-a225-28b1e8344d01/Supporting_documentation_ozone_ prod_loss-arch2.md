# Modelled annual average production loss due to ozone damage for four global staple crops, 20102012.

## Aim and scope
- Provide a standardized, model-based assessment of ozone-related production losses for maize, rice, soybean, and wheat during 2010–2012.
- Produce outputs suitable for environmental health monitoring and policy performance evaluation, with clear datasets and maps.

## Data sources and collection
- Crop production baseline: FAO Global Agro-Ecological Zones (GAEZ) dataset (year 2000) for 1° × 1° grid; irrigated and non-irrigated production data per crop.
- Gridding and aggregation: 1° × 1° grid built; national production converted to grid cells to estimate 2010–2012 period via a conversion factor based on 1999–2001 vs 2010–2012 production.
- Spatial attributes: hemisphere (Northern/Southern), climate zone (ESDAC JRC Climate Zone layer) assigned to each grid cell.
- Growing periods: 90-day crop-specific windows by climate zone and hemisphere, based on USDA/FAO data; multiple growing seasons considered only for the main period.

## Methodology (how outputs are derived)
- Ozone exposure metric: POD3IAM (phytotoxic ozone dose above 3 nmol m-2 s-1) calculated from the EMEP MSC-W model (daily ozone flux), using hourly inputs (concentration, temperature, VPD, irradiance, soil moisture) for 2010–2012.
- For each crop:
  - Wheat-derived dose-response used to convert POD3IAM to yield loss (reference POD3IAM = 0.1 mmol/m² subtracted; slope 0.64).
  - Maize, rice, and soybean yield losses scaled by their relative ozone sensitivity to wheat, using M7 (7-hour mean ozone) response functions.
  - Grid-cell production loss = crop production (2010–2012 average) × percentage yield loss.
- Outputs: 1° × 1° GIS shapefiles per crop, with production loss in thousand tonnes per grid cell.

## Outputs and data management
- Four GIS shapefiles (one per crop: maize, rice, soybean, wheat) containing:
  - ID: grid cell identifier
  - Zone: climate zone
  - Long_Lat: grid cell center coordinates
  - Hemisphere: Northern/Southern/Far South
  - ProdLoss: annual average production loss (2010–2012) in thousand tonnes
- Data lineage and versioning aligned with standard monitoring practices; outputs suitable for map-based reporting and integration into portals.

## Quality control and validation
- Model validation using Global Atmosphere Watch (GAW) data showed good spatial and temporal concordance between modelled and observed daily maximum ozone (Dmax) and 90-day M7 values (r² 0.88–0.93) with reasonable scatter.
- Stomatal uptake proxy: strong correlation (r² = 0.63) between AET/PET and model-estimated POD3IAM divided by M7, indicating credible stomatal uptake estimation.
- Independent caveats documented:
  - Lack of crop-specific ozone flux–yield relationships for maize, rice, and soybean; relative sensitivity to wheat used instead.
  - Limited maize flux data (only three older varieties) increases uncertainty for maize.
  - Only the main growing period per climate/crop considered; multiple seasons in some regions not represented.
  - Differences in ozone concentration vs. uptake may introduce uncertainties; concentration-based M7 used to drive sensitivity adjustments.

## Data structure details
- Outputs comprise 4 shapefiles (one per crop), each with 1° × 1° grid cells and 5 attribute fields:
  - ID: unique grid square identifier
  - Zone: climate zone
  - Long_Lat: center coordinates (decimal degrees)
  - Hemisphere: Northern, Southern, or Far South
  - ProdLoss: annual average production loss (2010–2012) in thousand tonnes per grid cell

## Miscellaneous and references
- Model framework: EMEP MSC-W chemical transport model (v4.16) for POD3IAM; CLRTAP dose–response relationship for yield loss.
- Primary methodological references: Mills et al. (2018a, 2018b) on ozone yield gaps and model validation; supplementary information details caveats and spatial analysis evaluation.
- Data sources: FAO GAEZ; ES-DA C climate zones (JRC); GAW observational data for validation.

## Relevance for environmental monitoring
- Demonstrates a standardized workflow to convert atmospheric ozone exposure into crop-specific production losses across a global grid.
- Provides readily usable, transparent datasets and maps aligned with monitoring and policy evaluation needs.
- Highlights where data gaps exist and where future species-specific flux data could reduce uncertainty, guiding data integration and collaboration to enhance data value.