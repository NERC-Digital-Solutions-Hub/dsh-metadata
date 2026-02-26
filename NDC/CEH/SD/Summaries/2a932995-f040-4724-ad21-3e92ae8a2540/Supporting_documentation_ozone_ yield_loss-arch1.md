# Modelled annual average percentage yield loss due to ozone damage for four global staple crops, 2010-2012 version 2.

## Overview
- Quantifies modeled annual average percentage yield loss due to ozone for maize, rice, soybean, and wheat for 2010–2012.
- Uses ozone flux-based dose-response (POD3IAM) from the EMEP MSC-W chemical transport model.
- Produces four GIS shapefiles (1° by 1° grid) with estimated yield losses per grid cell for each crop.

## Data collection and grid construction
- A 1° by 1° grid was created using ArcMap (v10.3).
- Crop production data (0.0833° resolution) from FAO Global Agro-Ecological Zones (GAEZ) for 2000; irrigated and non-irrigated production data collected per crop.
- For each crop, total production summed per grid cell; 2010–2012 average production estimated using a conversion factor derived from FAO national production data (based on 1999–2001 vs 2010–2012).
- Grid cells with more than 500 tonnes production included in mapping.
- Each cell classified as irrigated (if >75% irrigated production) or non-irrigated; cells assigned to hemisphere (Northern/Southern) and climate zone (ESDAC/JRC layer).

## Growing periods and climate zoning
- For each hemisphere/climate zone, a 90-day growing period was defined based on main growing seasons (USDA/FAO data).
- 90-day start and end days provided per crop and climate zone (details in Mills et al. 2018a, Table 1).

## Ozone dose-response and yield loss calculations
- Wheat-based dose-response used as the baseline for yield loss estimation:
  - POD3IAM is daily ozone flux integrated over the 90-day growing period.
  - Yield loss for wheat: Percent Yield Loss = (POD3IAM − 0.1) × 0.64, where 0.1 mmol/m² represents pre-industrial/neutral ozone and 0.64 is the slope.
- For maize, rice, and soybean:
  - Relative ozone sensitivity is computed as the ratio of the crop’s M7 (7-hour mean ozone) response slope to that of wheat (see Figure 2 in Mills et al. 2018a):
    - Soybean: RY = −0.0050x + 1.001
    - Wheat: RY = −0.0048x + 0.96
    - Rice: RY = −0.0021x + 0.987
    - Maize: RY = −0.0031x + 1.03
  - Step: calculate wheat-based yield loss from POD3IAM, then multiply by the crop’s relative sensitivity to obtain the final yield loss for that grid cell.
- Outputs: the 1° by 1° grid yield losses are saved as four GIS shapefiles (one per crop).

## Data products and structure
- Four yield loss GIS shapefiles (one per crop).
- Each shapefile contains gridded data (1° × 1°) with five attributes:
  - ID: Unique grid cell identifier.
  - Zone: Climate zone for the grid cell.
  - Long_Lat: Centre coordinates of the grid cell (decimal degrees).
  - Hemisphere: Northern, Southern, or Far South (for Cool temperate) classification.
  - Yloss: Annual average percentage yield loss due to ozone for 2010–2012.

## Quality control and validation
- Model validation described in Mills et al. 2018b:
  - Modelled vs observed daily maximum ozone (GAW sites) shows good agreement; r² 0.88–0.93 after excluding outliers.
  - Dmax (daily max ozone) and M7 (90-day 7-hour mean ozone) validations also support performance.
  - Strong correlation (r² = 0.63) between the AET/PET evapotranspiration ratio and POD3IAM/M7 proxy for growing-season stomatal conductance, indicating reasonable estimation of stomatal uptake.
- This study is pioneering in using ozone flux (POD3IAM) rather than concentration to estimate global crop impacts.
- Noted caveats:
  - Lack of crop-specific flux–yield relationships for maize, rice, and soybean; reliance on wheat-based flux with crop-specific sensitivity adjustment.
  - Maize data based on only three older varieties, increasing uncertainty for maize yields.
  - Some climates have multiple growing seasons; this study uses the most important growing period per crop.
  - Data limitations and uncertainties discussed in supplementary materials (T1) of Mills et al. 2018a.

## Limitations and caveats
- Absence of comprehensive flux–response data for all crops; scaling by relative M7 sensitivity may introduce uncertainty.
- Sparse maize data and potential intra-annual cropping patterns in multi-season climates.
- General uncertainties linked to global-scale modeling, data resolution, and climate-zone classifications.