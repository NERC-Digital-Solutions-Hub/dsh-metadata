# Collection/generation methods

## Objective and domain
- DEM domain covers the tidally influenced Conwy estuary, downstream of the Cwmlanerch river gauge, extending offshore into Conwy Bay and the Menai Strait.
- Aims to combine multiple data sources to represent land elevation, seabed bathymetry, and flood defences for hydrodynamic modelling.

## Data sources
- Seabed bathymetry (Menai Strait, Conwy Bay, estuary mouth to Conwy Bridge): marine DEMs from OceanWise via Digimap; 1 arc-second resolution; referenced to WGS84 and Chart Datum (CD) at Llandudno.
- Land elevations (73% coverage): NRW LiDAR-based DTMs/DSMs from Digimap; 1 m resolution; OSGB36 grid; elevations referenced to Ordnance Datum (OD) with ±0.15 m RMSE. DTM removes above-ground features; DSM includes them.
- Land elevations (27% coverage): OS Terrain 5 m DTM from Digimap; 5 m resolution; OSGB36; elevations referenced to OD.
- Flood defences: NRW data catalogue with vector shapefiles detailing location, type, and crest height above terrain (in metres).
- All datasets imported into ArcGIS Pro 3.0; rasters mosaicked and resampled to 5 m resolution.

## Data processing and domain construction
- Datum adjustments:
  - Marine DEM projected to OSGB36; converted from Chart Datum to Ordnance Datum by subtracting 3.85 m.
- Layer fusion rules:
  - In areas overlapped by marine DEM, LiDAR DTM, and OS Terrain 5 m DTM, only a single elevation is kept.
  - Permanently underwater areas prioritize marine DEM; LiDAR DTM fills gaps; land areas prioritize LiDAR DTM with OS Terrain 5 m filling gaps.
- Surface generation:
  - Rasters from all sources mosaicked into a single raster, converted to points (one point per raster cell), then interpolated to a continuous surface at 20 m resolution (topo-to-raster method). 20 m chosen to balance domain detail with computational cost.
- Flood defences augmentation:
  - Manually checked Lidar DSM against NRW defences; missing defences digitised with crest heights from DSM elevations.
  - Augmented defence data converted to 20 m buffer polygons, then to 20 m rasters and added to the surface to create the final model domain including defences.

## Model domain capabilities and limitations
- The final DEM can represent floodplain elevations, flood defences, and marine elevations.
- It does not accurately represent riverbed elevations; LiDAR limitations and water/air boundary refraction introduce errors in inundated river channels, requiring calibration.

## Units and data structure
- Elevations: metres; vertically referenced to Ordnance Datum (Newlyn).
- Spatial reference: British National Grid (metres).
- Data format: Digital Elevation Model ASCII.

## Calibration and hydrodynamic modelling
- DEM used with Caesar-Lisflood hydrodynamic model in reach mode; upstream boundary: 15-minute discharge time series from NRW (Cwmlanerch gauge); downstream/offshore boundary: 15-minute sea level time series at Llandudno from BODC, converted from CD to OD.
- Hydraulic parameters: Manning’s n = 0.022; Courant number = 0.6; Froude limit = 0.8; water loss function = 0.2 m/day on floodplains to prevent hinterland water buildup.
- Simulation outputs: 15-minute water levels.

## Calibration and validation results
- Channel bed elevations initially mis-specified due to LiDAR limitations; channel bathymetry treated as calibration parameter (Neal et al., 2022) and adjusted iteratively.
- Final calibration metrics ( Pont Fawr, Trefriw, Tal-y-Cafn ):
  - RMSE: 0.59 m, 0.39 m, 0.69 m
  - Kling-Gupta Efficiency (KGE): 0.90, 0.90, 0.70
- Flood peak RMSE: 0.57 m, 0.19 m, 0.29 m
- Interpretation: Good agreement for flood peaks; weaker performance in upper estuary likely due to missing tributaries; overall model suitable for study purposes.

## Figures and references
- Figure S1: Flowchart of steps to generate the model domain.
- Figure S2: Calibrated domain elevations and time-series comparisons at Pont Fawr, Trefriw, and Tal-y-Cafn.
- References: Gupta et al. (2009); Neal et al. (2021).