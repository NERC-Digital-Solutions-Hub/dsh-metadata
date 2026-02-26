# Flood maps for Central Highlands of Vietnam and surrounding Provinces

- A dataset of river (fluvial) and surface water (pluvial) flooding maps covering 11 Vietnamese provinces in the Central Highlands and nearby areas.
- Provides flood inundation depth in metres for 10 design return periods, at 30 m horizontal resolution.

## Scope and purpose
- Intended for planners and policy makers to identify areas at risk and inform policy, including contributions to sustainable development goals.
- Includes three flood types: fluvial undefended (FUD), fluvial defended (FD), and pluvial (P).

## Data and methods
- Model framework: updated version of the global flood model described in Sampson et al. (2015), called Fathom 3.0.
- Key updates:
  - Improved channel conveyance capacity (Neal et al., 2021)
  - Enhanced design flood estimation (Zhao et al., 2021)
  - New 30 m FABDEM elevation dataset (Hawker et al., 2022)
- Validation: model outputs compared with satellite imagery and household survey data (Hawker et al., in prep); quality assessment published alongside the dataset.

## Data structure and naming
- Contents: 330 GeoTIFF files + 1 readme document.
- Provinces: 11 total; for each province, 30 flood maps (10 return periods × 3 flood types).
- File naming convention: Province_FloodType_ReturnPeriod.tif
  - Example: Quang_Ngai_FD_1in20.tif
- Flood type abbreviations:
  - FUD = fluvial undefended
  - FD = fluvial defended
  - P = pluvial
- Return periods (ten): 1in5, 1in10, 1in20, 1in50, 1in75, 1in100, 1in200, 1in250, 1in500, 1in1000

## Experimental design and validation
- Ten return periods to represent a range from frequent to rare events, including the commonly used 1 in 100-year flood design standard.
- Analytical options: enable comparison with flood observations and calculation of skill scores (critical success index, hit rate, false alarm ratio, bias).

## Use in GIS and visualization
- Easiest to view in GIS software (e.g., QGIS, ArcMap) by opening per-province GeoTIFFs.
- Depth interpretation:
  - Values of 0 correspond to 0 m flood depth.
  - Recommend treating 0 as NoData or starting the color ramp at a small flooded value (e.g., 0.1 m) for visualization.
- Spatial and statistical analysis best performed with tools like R or Python.

## Quality, limitations, and considerations
- Quality support: in-press article compares Fathom 3.0 with Fathom 2.0 using satellite observations and household data.
- Limitations:
  - The model does not explicitly include flood defences not visible in 30 m FABDEM data; some defences may be underrepresented or absent (especially where defences are not resolved at this resolution).
  - Pluvial flood validation is challenging due to the short duration of events (minutes to hours).
  - Defences are estimated based on regional standards rather than a comprehensive global defence database.
- Coverage: provinces include Binh Dinh, Dak Lak, Dak Nong, Gia Lai, Khanh Hoa, Kon Tum, Lam Dong, Ninh Thuan, Phu Yen, Quang Nam, Quang Ngai.

## References (key sources)
- Hawker et al., 2022. FABDEM: a 30 m global elevation dataset without forests and buildings.
- Sampson et al., 2015. A high-resolution global flood hazard model.
- Neal et al., 2021. Estimating river channel bathymetry in large-scale flood models.
- Zhao et al., 2021. Design flood estimation for global river networks via machine learning.