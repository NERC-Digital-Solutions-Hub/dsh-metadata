# Collection/generation methods

- Objective: Develop a high-quality digital elevation model (DEM) for the DEM domain in the DEM domain covering the Conwy estuary (tidally influenced), combining seabed bathymetry, land elevations, and existing flood defences to support hydrodynamic modelling (Caesar-Lisflood) and flood risk analysis.

- Key outcome: A continuous surface that represents floodplain elevations, coastal/marine elevations, and flood defences, with a final resolution of 20 m and spatial alignment to the British National Grid and Ordnance Datum.

## Data sources and provenance

- Seabed bathymetry for Menai Strait, Conwy Bay, and Conwy estuary mouth to Conwy Bridge:
  - From OceanWise marine DEMs via Digimap.
  - Resolution: 1 Arc Second; referenced to WGS84 (CD for local datum).
- Land elevations:
  - 73% surveyed by Natural Resources Wales (NRW) using Lidar; DTMs and DSMs from Digimap; 1 m raster; OSGB36; elevations tied to Ordnance Datum (OD) with ±0.15 m RMSE.
  - Remaining 27% from OS Terrain 5 m DTM (national coverage; 5 m raster; OSGB36; elevations referenced to OD).
- Flood defences:
  - Locations and heights from NRW data catalogue; vector shapefiles (BNG) detailing defences and crest heights.
- Tools: All spatial data imported into ArcGIS Pro 3.0 and processed.

## Data processing workflow

- Datum harmonisation and resampling:
  - Marine DEM projected to OSGB36 and converted from Chart Datum (CD) to OD (Elevation OD = Elevation CD − 3.85 m).
  - Overlaid datasets masked to ensure a single elevation per location:
    - Underwater areas: marine DEM prioritized; fill gaps with Lidar DTM or OS Terrain 5 m DTM.
    - Land areas: Lidar DTM prioritized; fill gaps with OS Terrain 5 m DTM.
- Raster mosaicking and surface construction:
  - All rasters mosaicked into a single raster, converted to points per raster cell, then interpolated to a continuous surface (topo-to-raster) at 20 m resolution to balance detail and computational cost.
- Flood defence integration:
  - Manually checked Lidar DSM against NRW data; digitised missing defences; crest heights estimated from DSM elevations.
  - Augmented defences by buffering 20 m to polygons and converting to 20 m rasters; added to the surface to produce the final domain surface including defences.
- Documentation:
  - A flowchart (Figure S1) summarizes the steps; calibration procedure focuses on aligning river and coastal elevations.

## Model domain details and limitations

- Domain capabilities:
  - Represents floodplain elevations, flood defences, and marine elevations.
- Limitations:
  - Riverbed elevations are not accurately represented due to LiDAR limitations in inundated areas and water–air boundary effects in lidar-derived elevations.
  - Riverbed correction focused on calibration (channel bathymetry) to improve match with observations (Neal et al., 2022).

## Calibration, validation, and performance

- Hydrodynamic modelling:
  - Used Caesar-Lisflood in reach mode with upstream discharge (Cwmlanerch gauge) at 15-minute resolution for 1 March–16 April 2021.
  - Offshore boundary: measured sea levels at Llandudno (OD-adjusted) at 15-minute intervals.
  - Boundary conditions and hydrodynamic settings:
    - Manning’s n for channels and marine areas: 0.022
    - Courant number: 0.6
    - Froude limit: 0.8
    - Water loss function for floodplains: 0.2 m/day (applied only to floodplains)
- Calibration and results:
  - Compared simulated water levels to gauges at Pont Fawr, Trefriw (NRW), and Tal-y-Cafn (pressure logger, OD).
  - Iterative adjustments to channel bed elevations (calibration of channel bathymetry) to match observed levels.
  - Performance metrics (final DEM calibration):
    - RMSE: Pont Fawr 0.59 m, Trefriw 0.39 m, Tal-y-Cafn 0.69 m
    - Kling-Gupta Efficiency (KGE): Pont Fawr 0.90, Trefriw 0.90, Tal-y-Cafn 0.70
  - Flood peak RMSE: Pont Fawr 0.57 m, Trefriw 0.19 m, Tal-y-Cafn 0.29 m
- Limitations and notes:
  - Upper estuary performance may be affected by missing tributaries; overall setup suitable for the study’s aims.
  - Channel bathymetry calibration is essential due to initial LiDAR limitations in inundated channel areas.

## Data format, structure, and access

- Final DEM data:
  - Format: ASCII Digital Elevation Model (DEM)
  - Units: Elevations in metres, vertically referenced to Ordnance Datum (Newlyn)
  - Spatial reference: British National Grid (meters)
- Calibration period data and sources:
  - Upstream discharge: NRW gauge data, 15-minute, 1 March–16 April 2021
  - Offshore sea levels: BODC, 15-minute, converted to OD
- Outputs:
  - Hydrodynamic model-ready surface including elevations and defences
  - Surface resolutions and datums clearly documented to ensure reproducibility

## Quality control, uncertainties, and limitations

- Data provenance and interpolation methods are documented; calibration against multiple gauges provides confidence in domain realism.
- LiDAR and inundation boundary effects necessitated calibration of river channel bathymetry to achieve acceptable RMSE and NSE/KGE scores.
- Acknowledgement of missing tributaries and riverbed precision as potential sources of residual uncertainty, particularly in the upper estuary.

## References

- Gupta, H.V., Kling, H., Yilmaz, K.K., Martinez, G.F. (2009). Decomposition of the mean squared error and NSE performance criteria: Implications for improving hydrological modelling.
- Neal, J., Hawker, L., Savage, J., Durand, M., Bates, P., Sampson, C. (2021). Estimating River Channel Bathymetry in Large Scale Flood Inundation Models. Water Resources Research.