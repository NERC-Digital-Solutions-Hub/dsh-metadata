# Description

- The deposit contains river (fluvial) and surface water (pluvial) flooding maps for the Central Highlands of Vietnam and surrounding provinces, covering 11 provinces in total.
- Flood depth is estimated at a 30 m horizontal grid spacing for 10 return periods, ranging from 1 in 5 to 1 in 1000 year events.
- Intended audience: planners and policymakers to identify areas at risk and inform policy (including sustainable development goals).

- Collection and generation
  - Based on an updated global flood model (Fathom 3.0) described by Sampson et al. (2015).
  - Updates include improved channel conveyance capacity (Neal et al., 2021), better design flood estimation (Zhao et al., 2021), and a new 30 m FABDEM elevation dataset (Hawker et al., 2022).
  - Model validation conducted by comparison with satellite imagery and household survey data (Hawker et al., in prep).

- Nature and units of recorded values
  - Flood inundation depth in metres for 10 design return periods: 1 in 5, 10, 20, 50, 75, 100, 200, 250, 500, and 1000 years.
  - Flood types: fluvial undefended (FUD), fluvial defended (FD), and pluvial (P).
  - File naming indicates flood type: FD = fluvial defended, FUD = fluvial undefended, P = pluvial.
  - For these regions, FD and FUD show little difference due to assumed flood defence standards; defences not explicitly represented if not visible in the 30 m FABDEM resolution.
  - Note: validation does not explicitly include defences not visible in the elevation data.

- Quality control
  - An in-press article compares Fathom 3.0 to Fathom 2.0 using satellite flood observations and a household survey.

- Data structure
  - 330 GeoTiff files plus 1 readme document.
  - For each of 11 provinces, there are 30 flood maps (10 per flood type).
  - Filenames follow Province_FloodType_ReturnPeriod.tif (e.g., Quang_Ngai_FD_1in20.tif).
  - Return periods represented as 5, 10, 20, 50, 75, 100, 200, 250, 500, 1000 (years).

- Experimental design / sampling
  - Ten return periods simulated to cover common design and hazard perspectives, from frequent (5-year) to rare (1000-year), including the 100-year design relevance.

- Analytical methods
  - Results can be compared with flood observations to compute skill scores (e.g., critical success index, hit rate, false alarm ratio, bias).
  - Observations typically come from remote sensing, photographs, news articles, and wrack marks.

- Use in GIS software
  - GeoTiffs are easily visualized in GIS (QGIS, ArcMap).
  - Practical notes: value 0 denotes 0 m depth; consider treating 0 as no-data or use a color palette starting above 0 (e.g., 0.1 m) to indicate flooded areas.
  - Spatial and statistical analyses are well-suited to R or Python.

- Coverage specifics
  - Provinces included: Binh Dinh, Dak Lak, Dak Nong, Gia Lai, Khanh Hoa, Kon Tum, Lam Dong, Ninh Thuan, Phu Yen, Quang Nam, Quang Ngai.

- References (key supporting literature)
  - Hawker et al. 2022; Martinis et al. 2015; Neal et al. 2021; Sampson et al. 2015; Zhao et al. 2021.