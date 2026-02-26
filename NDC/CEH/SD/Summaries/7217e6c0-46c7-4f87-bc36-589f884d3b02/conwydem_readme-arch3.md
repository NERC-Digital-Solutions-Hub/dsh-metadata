# Conwy estuary model domain generation and calibration for hydrodynamic modelling

- Purpose and scope
  - Develop a high-resolution digital elevation model (DEM) domain for the DEM domain covering the tidally influenced Conwy estuary, including Conwy Bay and the Menai Strait, to support hydrodynamic modelling of flood risk.
  - Integrate multiple data sources to represent land elevations, seabed bathymetry, and existing flood defences; calibrate the model against observed water levels to enable accurate flood monitoring and scenario analysis.

- Data collection and sources
  - Seabed bathymetry (Menai Strait, Conwy Bay, estuary mouth): marine DEMs from OceanWise, accessed via Digimap; 1 Arc Second resolution; referenced to WGS84 and local Chart Datum (CD) at Llandudno.
  - Land elevations (catchment, 73% covered by lidar): NRW lidar-derived DTMs/DSMs at 1 m resolution; OSGB36 projection; elevations referenced to Ordnance Datum (OD) with ~±0.15 m RMSE.
  - Remaining land elevations (27%): OS Terrain 5 m DTM via Digimap; OSGB36 projection; elevations referenced to OD.
  - Flood defences: NRW data catalogue (vector shapefiles) detailing location, type (wall, embankment), and crest height above terrain (metres); projected to British National Grid.

- Data processing and domain creation
  - Imported all spatial data into ArcGIS Pro 3.0; mosaicked rasters and resampled to 5 m resolution.
  - Datum adjustments and masking:
    - Marine DEM projected to OSGB36; convert elevations from Chart Datum to OD (Elevation OD = Elevation CD − 3.85 m).
    - For overlapping datasets, marine DEM prioritized in permanently underwater areas; Lidar DTM preferred for land areas; OS Terrain 5 m DTM used to fill gaps.
  - Creation of a continuous surface:
    - All rasters mosaicked into a single surface, converted to points, then interpolated to a continuous surface at 20 m resolution using topo-to-raster interpolation.
  - Flood defences integration:
    - Manually checked Lidar DSM against NRW defences; added missing defences by digitising crest heights from DSM elevations.
    - Augmented defences as 20 m buffers, converted to 20 m raster cells, and added to the surface to produce the final model domain.
  - riverbed representation:
    - The final domain could represent floodplain elevations, flood defences, and marine elevations but lacked accurate riverbed elevations; riverbed values were estimated from Lidar data and later corrected during calibration due to LiDAR limitations in inundated areas.

- Nature and units
  - Final DEM elevations: metres, vertically referenced to Ordnance Datum (Newlyn); spatial reference: British National Grid (metres).
  - Data structure: Digital Elevation Model ASCII format.

- Calibration steps and values
  - Hydrodynamic model: Caesar-Lisflood, run in reach mode (upstream discharge and downstream water levels drive the model).
  - Boundaries:
    - Upstream: discharge time series (m3/s) from Cwmlanerch gauge; 15-minute resolution; period: 1 March–16 April 2021.
    - Offshore: sea level time series from BODC, converted from Chart Datum to OD; 15-minute resolution; same period.
  - Hydrodynamic settings: Manning’s n = 0.022; Courant number = 0.6; Froude limit = 0.8; applying a water loss function of 0.2 m/day on floodplains to prevent artificial backwater behind defences.
  - Calibration approach:
    - Compare simulated water levels with observed data at Pont Fawr, Trefriw (NRW gauges) and Tal-y-Cafn (pressure logger; OD relative).
    - Initial DEM adjustments addressed incorrect channel bed elevations due to LiDAR limitations by calibrating channel bathymetry as per Neal et al. (2022).
    - Stepwise DEM adjustments to achieve better agreement between simulated and observed water levels.
  - Calibration outcomes:
    - Final DEM RMSE: Pont Fawr 0.59 m, Trefriw 0.39 m, Tal-y-Cafn 0.69 m.
    - Kling-Gupta Efficiency (KGE): Pont Fawr 0.90, Trefriw 0.90, Tal-y-Cafn 0.70.
    - Flood peak RMSE: Pont Fawr 0.57 m, Trefriw 0.19 m, Tal-y-Cafn 0.29 m.
    - Notes: improved RMSE for flood peaks indicates better capture of peak magnitudes; upper estuary may be affected by missing tributaries, but overall setup is suitable for study goals.

- Outputs and limitations
  - Outputs: hydrodynamic simulations producing 15-minute interval water levels for model evaluation and scenario analysis.
  - Limitations:
    - Riverbed elevations rely on LiDAR-derived estimates that can underrepresent inundated channel depths due to optical limitations and water–air interface effects.
    - Upper estuary may be missing tributaries, contributing to elevated discrepancies in some locations.
  - Implications for monitoring:
    - The calibrated domain provides a robust basis for flood risk monitoring and policy support, with documented uncertainties and a transparent calibration approach.

- Relevance to monitoring frameworks and governance
  - Demonstrates an end-to-end workflow for assembling integrated, quality-checked spatial data from multiple sources to support environmental health monitoring and decision-making.
  - Emphasizes the need for data provenance, metadata, and calibration transparency (e.g., dataset origins, coordinate transformations, and validation metrics).
  - Highlights data gaps (e.g., riverbed elevations, tributary representation) and how calibration can mitigate some impacts while acknowledging remaining uncertainties.