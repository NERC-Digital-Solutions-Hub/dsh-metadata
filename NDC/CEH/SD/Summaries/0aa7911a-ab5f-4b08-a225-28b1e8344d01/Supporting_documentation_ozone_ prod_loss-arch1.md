# Modelled annual average production loss due to ozone damage for four global staple crops, 20102012.

## Overview
- Estimates annual average production loss due to ozone for maize, rice, soybean, and wheat for 2010–2012.
- Uses a spatial 1° x 1° grid to map losses and produces four separate GIS shapefiles (one per crop).
- Combines ozone exposure modelling with crop-specific dose–response relationships to derive yield and production losses.

## Data sources and grid construction
- Grid and cropping data
  - 1° by 1° grid created in ArcMap (v10.3).
  - FAO Global Agro-Ecological Zones (GAEZ) crop production data (2000) used; irrigated vs non-irrigated production collected per crop.
  - For each crop, total production is summed per grid cell; only cells with more than 500 tonnes were included.
  - 2010–2012 average production per grid cell estimated with a conversion factor from FAO national data (based on 1999–2001 vs 2010–2012 differences).
- Spatial classification
  - Grid cells classified as irrigated if >75% irrigated production; otherwise non-irrigated.
  - Each cell assigned to a hemisphere (Northern or Southern) and a climate zone from the ESDSAC JRC GIS layer.
- Growing period foundation
  - 90-day growing periods defined per climate zone and hemisphere (main growing season per crop), primarily using USDA and FAO data.
  - Table of 90-day periods provided for maize, rice, soybean, and wheat.

## Ozone exposure and yield loss calculation
- Ozone exposure model
  - EMEP MSC-W chemical transport model (version 4.16) used to compute daily ozone flux (POD3IAM) for 2010–2012.
  - Outputs include irrigated and non-irrigated POD3IAM values per grid cell.
  - For each grid cell, a 90-day POD3IAM value is computed using the climate-specific growing period; irrigated cells use irrigated values, non-irrigated cells use rain-limited values.
- Baseline adjustment
  - Subtract a reference POD3IAM of 0.1 mmol/m2 (representing pre-industrial/ natural ozone levels) before calculating yield loss.
  - Yield loss is calculated with Percent Yield Loss = (POD3IAM − 0.1) × 0.64, where 0.64 is the slope of the wheat dose–response relationship used as a common baseline.

## Crop-specific yield loss estimation
- Wheat baseline
  - The CLRTAP 2017 dose–response is used to convert POD3IAM to percent yield loss for wheat.
- Other crops (maize, rice, soybean)
  - Since crop-specific flux–response data are lacking, yield loss for maize, rice, and soybean is estimated by:
    - Computing wheat yield loss as above.
    - Multiplying by the relative ozone sensitivity, which is the ratio of each crop’s M7 (7-hour mean ozone) slope to the wheat M7 slope.
  - M7 response functions (slopes) used:
    - Soybean, RY = -0.0050x + 1.001
    - Wheat, RY = -0.0048x + 0.96
    - Rice, RY = -0.0021x + 0.987
    - Maize, RY = -0.0031x + 1.03
  - These give relative sensitivity values to scale the wheat-based loss to maize, rice, and soybean.
- Production loss per grid cell
  - Production loss (thousand tonnes) = Crop production (thousand tonnes) × (percent yield loss / 100).
  - Loss values are summed across grid cells to yield the final grid-wide losses per crop.

## Data outputs and structure
- Outputs
  - Four GIS shapefiles (one per crop: maize, rice, soybean, wheat), each at 1° x 1° resolution.
- Attributes per shapefile
  - ID: Unique grid cell identifier.
  - Zone: Climate zone for the grid cell.
  - Long_Lat: Center coordinates of the grid cell (decimal degrees).
  - Hemisphere: Northern, Southern, or Far South (for wheat/maize under Cool temperate climate) based on latitude.
  - ProdLoss: Annual average production loss due to ozone (thousand tonnes) for 2010–2012.

## Quality control and validation
- Model validation
  - EMEP model performance assessed against Global Atmosphere Watch (GAW) site observations; good spatial and temporal concordance during peak ozone periods.
  - Comparisons of Dmax (daily max) and M7 (90-day 7-hour mean) against observed data from GAW stations show high correlations (r^2 ≈ 0.88–0.93) with low scatter.
  - Stomatal uptake proxy validation: ratio of actual to potential evapotranspiration (AET/PET) plotted against POD3IAM/M7 shows strong correlation (r^2 ≈ 0.63).
- Caveats and limitations
  - Lack of species-specific ozone flux–response data for maize, rice, and soybean; reliance on wheat flux with a relative sensitivity scaling.
  - Maize data limited to three older varieties, increasing uncertainty for maize.
  - Only the most important growing period per climate is used in multi-season contexts (e.g., India), potentially missing secondary seasons.
  - Caveats discussed in detail in Mills et al. 2018a/b supplementary information.

## References and further information
- Mills, G. et al. (2018a). Closing the global ozone yield gap: Quantification and co-benefits for multi-stress tolerance. Global Change Biology.
- Mills, G. et al. (2018b). Ozone pollution will compromise efforts to increase global wheat production. Global Change Biology.
- CLRTAP 2017. Modelling and Mapping Manual.
- FAO/GAEZ data and ES DAC JRC climate zone layer references.