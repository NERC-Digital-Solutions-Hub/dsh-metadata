# Modelled average percentage yield loss due to ozone damage for four global staple crops (2010-2012)

## Purpose
- Quantify global crop yield losses due to ozone for maize, rice, soybean, and wheat during 2010–2012.
- Provide 1° × 1° grid cell estimates to support assessments of ozone impact on food production.

## Data sources
- Ozone exposure and flux: EMEP MSC-W chemical transport model (POD3IAM) and 90-day growing-period adjustments.
- Crop production baselines: FAO Global Agro-Ecological Zones (GAEZ) dataset (year 2000) with irrigated and non-irrigated classifications.
- Climate zones and geography: ES DAC/JRC climate zone GIS layer; hemisphere classification.
- Validation data: Global Atmosphere Watch (GAW) network measurements for model validation (Dmax, M7).

## Collection/Generation
- 1° by 1° grid cells created in ArcMap; crop production aggregated to grid cells and filtered to cells with >500 tonnes production.
- Each grid cell labeled as irrigated or non-irrigated; assigned to Hemisphere and climate zone.
- For each crop, a 90-day growing period was defined per climate zone/hemisphere using USDA/FAO data.
- POD3IAM values computed per grid cell; irrigated vs non-irrigated flux used accordingly.

## Methodology
- Wheat yield loss: Percent yield loss = (POD3IAM − 0.1) × 0.64, where 0.1 mmol/m² is a pre-industrial reference, and 0.64 is the dose-response slope.
- Other crops (maize, rice, soybean): use the same formula to obtain wheat-based yield loss, then scale by crop-specific relative ozone sensitivity to wheat (ratio of their M7 response slope to wheat’s).
- Sum yield losses into four 1° grid GIS shapefiles (one per crop); computations reflect the most important growing period per climate, recognizing multiple seasons in some regions.

## Data structure and outputs
- Four GIS shapefiles (one per crop: maize, rice, soybean, wheat) at 1° × 1° resolution.
- Attributes per grid cell:
  - ID: Unique grid cell identifier
  - Zone: Climate zone
  - Long_Lat: Center coordinates (decimal degrees)
  - Hemisphere: Northern, Southern, or Far South
  - Yield loss: Average percentage yield loss for 2010–2012

## Quality Control and validation
- Model validation against GAW data showed good spatial-temporal concordance; r² for Dmax and M7 between 0.88 and 0.93 with minimal scatter.
- Strong correlation between simulated POD3IAM-based uptake proxy (POD3IAM/M7) and evapotranspiration ratio (AET/PET) as a check on stomatal uptake estimates.
- Study notes uncertainties and caveats, including limited crop-specific ozone flux data (maize, rice, soybean) and reliance on wheat as the reference for flux-based yield loss adjustments.

## Caveats and limitations
- Absence of crop-specific ozone flux–yield relationships for maize, rice, and soybean; relative sensitivity to wheat used as a proxy.
- Maize data limited to three older varieties, increasing uncertainty for that crop.
- Only the single most important growing period per crop is used in regions with multiple seasons.
- Global-scale analysis implies uncertainties related to regional variability in climate, management, and data resolution.

## Access and references
- Data and methodological references:
  - Mills et al. (2018a) Closing the global ozone yield gap: multi-stress tolerance; Global Change Biology.
  - Mills et al. (2018b) Ozone pollution will compromise efforts to increase global wheat production; Global Change Biology.
  - Supplementary Information and dose–response figures for crop sensitivities.
- Data sources: FAO/GAEZ, ES DAC/JRC climate zones, EMEP MSC-W model, GAW network.