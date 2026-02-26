# Modelled annual average production loss due to ozone damage for four global staple crops, 20102012.

## Overview
- Purpose: Estimate production losses for maize, rice, soybean, and wheat caused by ozone exposure during 2010–2012.
- Output: Four GIS shapefiles (one per crop) containing gridded production loss data at 1° by 1° resolution.
- Scope: Uses a combination of ozone flux modelling and crop-specific sensitivity to derive yield and production losses globally.

## Data sources and preprocessing
- Spatial framework:
  - Grid: 1° by 1° cells; production data originally at 0.0833° resolution (FAO GAEZ, year 2000) aggregated to 1° cells.
  - Filtering: Only grid cells with >500 tonnes total production included.
  - Classification: Each cell labeled as irrigated or non-irrigated based on a 75% irrigated production threshold.
  - Regions: Each cell assigned to a hemisphere (North/South) and a climate zone using the ES DAC JRC Climate Zone raster.
- Growing periods:
  - For each hemisphere/climate zone combination, a 90-day growing period was defined per crop (driven by USDA/FAO data).
  - Table S1 provides the exact start and end days for maize, rice, soybean, and wheat across climate zones.

## Modelling approach
- Ozone flux modelling:
  - Employed the EMEP MSC-W (version 4.16) chemical transport model to calculate daily ozone flux (POD3 IAM) during 2010–2012.
  - Outputs include irrigated (no soil water limitation) and non-irrigated (rain-limited) POD3IAM for each grid cell and crop.
- Yield loss calculation:
  - For wheat: percent yield loss = (POD3IAM − 0.1) × 0.64, where 0.1 mmol/m2 is a pre-industrial reference POD3IAM and 0.64 is the slope of the yield-response relationship.
  - For maize, rice, soybean: relative ozone sensitivity is derived by comparing each crop’s 7-hour mean ozone (M7) response slope to that of wheat; the wheat-based loss is scaled by this ratio.
  - Final grid-cell yield loss per crop = wheat-based yield loss × (crop M7 slope / wheat M7 slope).
- Production loss calculation:
  - Production loss (thousand tonnes) = crop production (thousand tonnes; 2010–2012 average per grid cell) × (percent yield loss / 100).
  - Losses are summed into the 1° by 1° grid and saved as separate shapefiles per crop.

## Outputs and data structure
- Outputs:
  - Four GIS shapefiles (one per crop: maize, rice, soybean, wheat).
- Data attributes per shapefile (5 fields):
  - ID: Unique grid cell identifier.
  - Zone: Climate zone for the cell.
  - Long_Lat: Centre coordinates of the 1° grid cell (decimal degrees).
  - Hemisphere: Northern, Southern, or Far South (for Wheat/Maize in Cool temperate climates).
  - ProdLoss: Annual average production loss (thousand tonnes) for 2010–2012.

## Quality control and validation
- Model validation:
  - Compared model outputs to Global Atmosphere Watch (GAW) observations; showed good spatial and temporal alignment of ozone metrics.
  - Dmax and M7 comparisons at GAW stations yielded r2 between 0.88 and 0.93 with low scatter.
  - Validation of stomatal uptake proxy (AET/PET) against POD3IAM/M7 indicated a strong correlation (r2 ≈ 0.63), supporting the uptake-based approach.
- Novelty: This study is among the first to use ozone flux (POD3IAM) rather than concentration alone for global crop yield impact assessments.

## Caveats and limitations (relevance to GIS work)
- Data limitations:
  - Species-specific ozone flux data are lacking for maize, rice, and soybean; the approach uses a wheat-based flux with crop-specific scaling.
  - Maize data are especially uncertain due to only three available varieties in underlying data.
- Temporal and climatic considerations:
  - In some climates, multiple cropping seasons exist; only the most important growing period per crop was used.
  - Potential differences in ozone uptake across crops under varying environmental conditions are captured primarily through M7-based concentration differences, not direct flux data.
- Data resolution and standards:
  - Grid-based approach relies on a mix of coarse and fine-resolution data; consistency across datasets (production, climate zones, ozone metrics) is essential for reproducibility.
- Users should interpret results with these uncertainties in mind, particularly for maize and in regions with multiple growing seasons.

## Sources and references
- Primary methodology and model validation papers:
  - Mills et al. (2018a) Closing the global ozone yield gap: Quantification and co-benefits for multi-stress tolerance. Global Change Biology.
  - Mills et al. (2018b) Ozone pollution will compromise efforts to increase global wheat production. Global Change Biology.
- Data layers and models:
  - FAO Global Agro-Ecological Zones (GAEZ) dataset.
  - ES DAC/JRC Climate Zone raster layer.
  - EMEP MSC-W chemical transport model (version 4.16).
  - GAW observational data for validation.