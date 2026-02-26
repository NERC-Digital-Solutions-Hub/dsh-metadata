# Boothroyd_et_al_STOTEN_Phillipines_bridge_inventory_river_migration_geodatabase

## Overview
- Dataset describing the Philippines bridge inventory and river migration geodatabase linked to Boothroyd et al. (2020).
- Contains hydro-morphological and bridge characteristics for 74 bridges (deck length > 200 m) in the Philippines.
- Includes active river channel information: masks and width statistics (592 files in total) for each bridge site.
- Available in CSV and SHP formats, plus raster masks of active channels.

## What the dataset includes
- Bridge inventory attributes (from the Detailed Bridge Inventory Application, DPWH):
  - Location (latitude, longitude), bridge name and ID, material, road name and type, region/province/island.
  - Structural details: deck length and width, year of construction, age as of 2020, number of abutments and piers, pier height, overall condition.
- Stream network and geomorphology descriptors:
  - Upstream area, distance along trunk stream, channel slope (averaged over 0.3 km), Strahler stream order.
  - Normalised position of the bridge along the trunk stream.
  - Geomorphic context: confinement (confined, partly confined, laterally unconfined), number of channels, channel planform (straight, meandering, wandering, braided).
- RivWidthCloud and channel width statistics:
  - Active channel width metrics: min, max, mean, standard deviation, and number of width measurements.
  - Similarity metrics for active channel masks across time: Jaccard and Dice coefficients (between adjacent time intervals and cumulatively).
- Active channel and width data:
  - 592 active-channel mask/width files (per bridge and time interval), named in a consistent scheme (e.g., FID_Bridge_Name_T*_Active_Channel.tif and corresponding _Widths.csv).

## How the bridge and river characteristics were derived
- Bridge selection from DPWH Detailed Bridge Inventory:
  - Initial set: 8,410 bridges along national roads.
  - Filter: permanent bridges with deck length ≥ 200 m (n = 256).
  - Visual check: sites at contemporary river crossings (n = 182) and active channel width > 150 m (n = 74) retained.
- Stream network and geomorphology:
  - 2013 nationwide IfSAR DEM (5 m resolution; ~1 m vertical accuracy) used for topographic analysis.
  - DEM resampled to 30 m; flowed routing with TopoToolbox to derive stream network.
  - Bridge points snapped to the stream network; attributes extracted at each point: upstream area, slope, order.
  - Channel slope averaged over 0.3 km segments.
  - Geomorphic descriptors appended from contemporary imagery (Google Earth) to characterize confinement, number of threads, and planform.
- Active channel change and RivWidthCloud:
  - Google Earth Engine workflow described in a supporting document for assessing active channel change and RivWidthCloud statistics.
  - Similarity coefficients (Jaccard and Dice) calculated for multiple time-interval pairings (T1–T2, T2–T3, T3–T4, and T1–T4).

## File structure and naming
- Active channel masks: FID_Bridge_Name_T*_Active_Channel.tif
- Active channel widths: FID_Bridge_Name_T*_Active_Channel_Widths.csv
- Descriptions of naming: identifier code, bridge name, time-interval for both mask and width files.

## Dataset schema and key fields
- Bridge-level fields (examples):
  - Bridge_Latitude, Bridge_Longitude, Bridge_Name, Bridge_ID
  - Bridge_Material, Bridge_Road_Name, Bridge_Road_Type
  - Bridge_Island, Bridge_Region, Bridge_Province
  - Bridge_Deck_Length, Bridge_Deck_Width, Bridge_Year_Construction, Bridge_Age_2020
  - Bridge_No_Abutments, Bridge_No_Piers, Bridge_Pier_Height, Bridge_Condition
- Stream network fields (examples):
  - Bridge_Distance_Channel_Head, Bridge_Distance_Stream_Outlet, Bridge_Normalised_Distance_Trunk_Stream
  - Bridge_Upstream_Area, Bridge_Stream_Order, Bridge_Stream_Elevation, Bridge_Stream_Slope
- Geomorphology fields (examples):
  - Channel_Confinement, Channel_No_of_Threads, Channel_Planform
- RivWidthCloud and similarity fields (examples):
  - T*_Min_Width, T*_Max_Width, T*_Mean_Width, T*_Std_Dev_Width
  - T*_Active_Channel_No_Pixels, T*_Active_Channel_Area
  - T1_T2_Jaccard, T1_T2_Dice, T2_T3_Jaccard, T2_T3_Dice, T3_T4_Jaccard, T3_T4_Dice, T1_T4_Jaccard, T1_T4_Dice

## Acknowledgements and data sources
- Data sourced from the Philippines Department of Public Works and Highways (DPWH); bridge data via DPWH Detailed Bridge Inventory Application.
- Additional data contributions from the Philippines Statistics Division, Planning Service, and DPWH.
- Funded by Natural Environment Research Council (NERC) and DOST-PCIEERD Newton Fund grant NE/S003312.

## Potential uses for analysts
- Analyze correlations between bridge characteristics and river migration/planform change.
- Assess active channel width changes and their relation to geomorphology and bridge type.
- Support infrastructure planning and resilience by identifying sites with significant channel change or vulnerability.
- Integrate with other spatial datasets to enhance risk assessment and decision-making at local to national scales.
- Reproduce or extend the Google Earth Engine analyses for active channel change and RivWidthCloud metrics.

## Notes on scope and limitations
- Based on 2013 IfSAR DEM for hydrological analysis; processing constraints led to a 30 m resampled DEM.
- Final dataset covers 74 bridges with active channel widths exceeding 150 m, out of an initial pool of 8,410 DPWH bridges.
- Time intervals for active channel data are defined by the T1–T4 scheme documented in the related supporting materials.