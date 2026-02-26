# Modelled average percentage yield loss due to ozone damage for four global staple crops (2010-2012)

- Purpose and scope
  - Quantifies modelled average percentage yield loss due to ozone damage for four global staple crops (maize, rice, soybean, wheat) during 2010–2012.
  - Based on a combination of ozone flux modelling (POD3IAM) and dose–response relationships, with cross-crop adjustment to reflect relative ozone sensitivity.

- Data sources and collection
  - Crop production input data from FAO Global Agro-Ecological Zones (GAEZ) dataset (year 2000) at 0.0833° resolution; aggregated to 1° × 1° grid cells.
  - Climate zone classification using the European Soil Data Centre (ESDAC) GIS layer; grid cells also labeled by hemisphere (Northern/Southern) and irrigation status (irrigated vs non-irrigated).
  - Growing periods: for each climate zone × hemisphere, a 90-day main growing period was defined (as per Mills et al. 2018a), with crop-specific start and end days summarized in supplementary material.
  - Ozone exposure data: EMEP MSC-W chemical transport model (version 4.16) providing daily ozone flux measures (POD3IAM) for irrigated and non-irrigated conditions.

- Methodology for yield loss estimation
  - Wheat baseline: yield loss calculated from POD3IAM using CLRTAP-specified dose–response with POD3IAM baseline subtraction of 0.1 mmol m^-2 and a slope of 0.64.
  - Crop-specific adjustments:
    - For maize, rice, and soybean: initial wheat-based yield loss (derived from POD3IAM) is adjusted by the relative ozone sensitivity, computed as the ratio of each crop’s M7 (7-hour mean ozone concentration) slope to that of wheat.
    - Final yield loss per grid cell = (wheat-based yield loss) × (crop-specific M7 slope relative to wheat).
  - Outputs: four 1° × 1° GIS shapefiles (one per crop) with yield loss values for 2010–2012.

- Data structure and accessibility
  - Each yield-loss shapefile contains grid-cell level data with five attributes:
    - ID: unique grid cell identifier
    - Zone: climate zone
    - Long_Lat: center coordinates of the grid cell
    - Hemisphere: Northern, Southern, or Far South (for Cool temperate)
    - Yield loss: average percentage yield loss due to ozone for 2010–2012

- Quality control and validation
  - Model validation for EMEP-MSC-W outputs against in-situ and satellite-informed ozone data (Global Atmosphere Watch networks).
  - Reported good spatial–temporal representation of ozone, with seasonality and regional variation captured (seasonal metrics Dmax and M7 showing strong model–observation correlation; r^2 between 0.88 and 0.93 in 2012 after outlier handling).
  - Additional checks on stomatal uptake proxy: ratio of actual to potential evapotranspiration (AET/PET) correlated with POD3IAM/M7 proxy (r^2 ≈ 0.63), supporting the model’s uptake estimates.
  - Acknowledged caveats:
    - Limited direct flux–response data for maize, rice, and soybean; reliance on wheat-based flux and cross-crop scaling.
    - Uncertainties in maize data due to limited crop-variety representation (only three older varieties in the underlying data).
    - In multi-season climates, only the most important growing period per crop was used.

- Data governance and context
  - Methodology integrates internationally referenced models and datasets (EMEP/MSC-W, CLRTAP dose–response, GAW validation; FAO/GAEZ input data; ES DAC climate layer).
  - Outputs are publicly describable and shareable as GIS shapefiles, enabling monitoring and policy evaluation related to ozone health impacts on crop yields.
  - Documentation links to full methodological details and validation studies (Mills et al. 2018a, 2018b) for reproducibility and deeper technical understanding.

- Key references and supporting materials
  - Mills et al. (2018a). Closing the global ozone yield gap: Quantification and co-benefits for multi-stress tolerance. Global Change Biology, 24, 4869–4893.
  - Mills et al. (2018b). Ozone pollution will compromise efforts to increase global wheat production. Global Change Biology, 24, 3560–3574.
  - Additional methodological and validation details available in the supplementary information and related technical descriptions of the EMEP model and CLRTAP guidelines.