# Description

- Deposit of river (fluvial) and surface water (pluvial) flooding maps for the Central Highlands of Vietnam and surrounding provinces (11 provinces total).
- Flood depth estimated at 30 m horizontal grid spacing for 10 return periods (1 in 5, 10, 20, 50, 75, 100, 200, 250, 500, 1000 year).
- Useful for planners and policymakers to identify areas at risk and support policy planning (e.g., Sustainable Development Goals).

## Collection/generation methods

- Generated with an updated version of the global flood model (Fathom 3.0), building on Sampson et al. 2015.
- Updates include: channel conveyance capacity (Neal et al., 2021), design flood estimation (Zhao et al., 2021), and a new 30 m FABDEM elevation dataset (Hawker et al., 2022).
- Model validation against satellite imagery and household survey data (Hawker et al., in prep).

## Nature and Units of recorded values

- Flood inundation depth in metres for 10 design return periods.
- Flood types: fluvial undefended (FUD), fluvial defended (FD), and pluvial (P); file names encode type (FUD, FD, P).
- Coverage: 11 provinces (Binh Dinh, Dak Lak, Dak Nong, Gia Lai, Khanh Hoa, Kon Tum, Lam Dong, Ninh Thuan, Phu Yen, Quang Nam, Quang Ngai).
- Defended vs. undefended: FD adjusts river conveyance to reflect estimated flood defence standards; pluvial maps rely on FABDEM at 30 m resolution.

## Experimental design/Sampling regime

- Ten return periods simulated: 5, 10, 20, 50, 75, 100, 200, 250, 500, 1000 years.
- Rationale: cover common design thresholds and extreme events, including 1 in 100-year threshold used for flood defence design.

## Analytical methods

- Results can be compared with flood observations; skill scores such as critical success index, hit rate, false alarm ratio, and bias can be computed.

## Use in GIS Software

- GeoTiff format for visualization in GIS (e.g., QGIS, ArcMap).
- 0 value denotes 0 m flood depth; recommended to treat 0 as no-data or start color scales at a small flooded value (e.g., 0.1 m).
- Spatial and statistical analyses can be conducted in R or Python.

## Data structure

- 330 GeoTiff files plus 1 readme.
- Per province: 30 flood maps (10 for each flood type).
- Naming convention: Province_FloodType_ReturnPeriod.tif (e.g., Quang_Ngai_FD_1in20.tif).
- FloodType abbreviations: FD = fluvial defended, FUD = fluvial undefended, P = pluvial.
- ReturnPeriod format example: 1in20 (1 in 20 year flood).

## Data governance considerations for Data Stewards

- Metadata and provenance: model version (Fathom 3.0), data sources, and validation references should be captured and maintained.
- Interoperability: distinction between defended and undefended fluvial results; ensure users understand the limitations that defences are not explicit in 30 m FABDEM-based results.
- Quality and provenance controls: ongoing validation against satellite observations and household data; note the pluvial validation challenges due to brief event durations.
- Updates and maintenance: guidance on updating datasets as models or elevation data (FABDEM) are refined; document any changes in file naming or structure.
- Documentation: ensure readme and references (Hawker et al., 2022; Sampson et al., 2015; Neal et al., 2021; Zhao et al., 2021) are accessible for users assessing methods and limitations.

## Quality control

- Model quality assessment described: a new article in press evaluating Fathom 3.0 against the previous version (Fathom 2.0) using satellite flood observations and household surveys.

## References

- Hawker et al. (2022). A 30 m global map of elevation with forests and buildings removed. Environmental Research Letters.
- Sampson et al. (2015). A high-resolution global flood hazard model. Water Resources Research.
- Neal et al. (2021). Estimating river channel bathymetry in large-scale flood inundation models. Water Resources Research.
- Zhao et al. (2021). Design flood estimation for global river networks based on machine learning models. Hydrology and Earth System Sciences.