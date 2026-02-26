# Collection/generation methods

- Domain and purpose
  - DEM domain covering the tidally influenced Conwy estuary, downstream of Cwmlanerch river gauge, extending offshore into Conwy Bay and the Menai Strait.
  - Aims to represent floodplain elevations, flood defences heights, and marine elevations for hydrodynamic modeling; riverbed elevations are not accurately represented and require calibration.

- Data sources and resolutions
  - Seabed bathymetry (Menai Strait, Conwy Bay, estuary mouth to Conwy Bridge)
    - Marine DEMs from OceanWise via Digimap; 1 arc-second resolution; WGS84; bathymetry referenced to local Chart Datum.
  - Land elevations
    - NRW Lidar (73% of catchment): 1 m resolution DTMs/DSMs; OSGB36 projection; elevations referenced to OD; ±0.15 m RMSE.
    - Remaining land (27%): OS Terrain 5 m DTM via Digimap; 5 m resolution; OSGB36; elevations referenced to OD.
  - Flood defences
    - NRW data catalogue: vector shapefiles with locations, type (e.g., wall, embankment), and crest heights.
  - All spatial data integrated in ArcGIS Pro 3.0; rasters mosaicked and resampled to 5 m where appropriate; final continuous surface at 20 m resolution.

- Data processing workflow
  - Datum and projection harmonisation
    - Marine DEM projected to OSGB36; vertical datum converted from Chart Datum to Ordnance Datum (OD) by subtracting 3.85 m.
  - Handling overlaps and gaps
    - In areas where datasets overlapped, a priority scheme was used: underwater areas rely on marine DEM; land areas rely on Lidar DTM; OS Terrain 5 m fills gaps.
  - Surface creation
    - All raster datasets mosaicked into a single raster, converted to points (one point per unique cell), then interpolated to a continuous surface using topo-to-raster interpolation to achieve a 20 m resolution.
  - Flood defences augmentation
    - Flood defence polylines checked against Lidar DSM; missing defences digitised and crest heights estimated from DSM elevations.
    - Augmented polylines buffered by 20 m, rasterised to 20 m, and added to the surface to form the final domain.
  - Riverbed considerations
    - Riverbed elevations not well captured by LiDAR and not fully present in the marine DEM; these regions were estimated and later corrected during calibration.

- Final data characteristics
  - The final DEM is in ASCII format with elevations in metres, vertically referenced to Ordnance Datum (OD), and spatially referenced to the British National Grid.

- Calibration and hydrodynamic model integration
  - Model: Caesar-Lisflood, run in reach mode (upstream discharge and downstream sea level forcing).
  - Boundaries and forcing
    - Upstream: discharge time series (15-minute resolution) at Cwmlanerch gauge; calibration period 1 March–16 April 2021.
    - Downstream: offshore sea levels at Llandudno (15-minute intervals), converted from Chart Datum to OD.
  - Boundary conversions and hydraulic parameters
    - CD to OD offset of -3.85 m applied.
    - Manning’s roughness for river/marine areas: 0.022.
    - Courant number: 0.6; Froude limit: 0.8.
    - Water loss function on floodplains: 0.2 m day⁻¹ (to prevent artificial water accumulation behind defences during overtopping).
    - Output: hydrodynamic component only; water levels exported at 15-minute intervals.
  - Calibration approach and results
    - Channel bathymetry treated as a calibration parameter; adjusted iteratively to match observed water levels from Pont Fawr, Trefriw, and Tal-y-Cafn.
    - Post-calibration performance
      - RMSE: Pont Fawr 0.59 m, Trefriw 0.39 m, Tal-y-Cafn 0.69 m.
      - Kling-Gupta Efficiency (KGE): Pont Fawr 0.90, Trefriw 0.90, Tal-y-Cafn 0.70.
      - Flood peaks RMSE: Pont Fawr 0.57 m, Trefriw 0.19 m, Tal-y-Cafn 0.29 m.
    - Observations
      - Upper estuary show weaker fit (likely due to missing tributaries); overall, model setup captures major peaks and is suitable for research purposes.

- Limitations and notes
  - Riverbed elevations are not accurately represented; required calibration-based correction.
  - LiDAR limitations for inundated areas (refraction effects, water column turbidity) affect river channel elevations.
  - Tributaries of the upper estuary not included in the model domain, contributing to higher errors in that region.
  - Data integration relies on multiple sources with differing resolutions and datums, necessitating careful calibration and validation.

- Supporting figures and references
  - Figure S1: Flowchart of model-domain generation steps.
  - Figure S2: Calibrated domain visuals and time-series comparisons at gauges.
  - References: Gupta et al. 2009; Neal et al. 2021.