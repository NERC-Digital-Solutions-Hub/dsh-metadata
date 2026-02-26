# Boothroyd_et_al_STOTEN_Phillipines_bridge_inventory_river_migration_geodatab ase.csv and Boothroyd_et_al_STOTEN_Phillipines_bridge_inventory_river_migration_geodatab ase.shp

## Overview
- Supporting documentation for the Philippines bridge inventory and river migration geodatabase associated with Boothroyd et al. (2020).
- Dataset covers hydro-morphological and bridge characteristics for 74 bridges (>200 m deck length) in the Philippines.
- Data are available in CSV and SHP formats; active channel masks (TIFF) and channel width estimates (CSV) are provided for each bridge site (592 files total).

## What is included
- Bridge inventory and river migration geodatabase fields and metadata (locations, bridge attributes, and road information).
- Stream network characteristics derived from a 2013 IfSAR DEM, including upstream area, channel slope, and Strahler order.
- Geomorphic descriptors describing confinement, number of channel threads, and channel planform.
- RivWidthCloud-derived active river channel width statistics (min, max, mean, std dev) and related counts.
- Similarity coefficients for active channel change over multiple time intervals (Jaccard and Dice metrics).

## Data contents and key variables
- Bridge characteristics (from DPWH Detailed Bridge Inventory Application):
  - Location and identification: Bridge_Latitude, Bridge_Longitude, Bridge_Name, Bridge_ID.
  - Physical attributes: Bridge_Material, Bridge_Deck_Length, Bridge_Deck_Width, Bridge_Year_Construction, Bridge_Age_2020, Bridge_No_Abutments, Bridge_No_Piers, Bridge_Pier_Height, Bridge_Condition.
  - Road context: Bridge_Road_Name, Bridge_Road_Type.
  - Administrative divisions: Bridge_Island, Bridge_Region, Bridge_Province.
- Stream network characteristics (from 30 m DEM analyses):
  - Distance metrics: Bridge_Distance_Channel_Head, Bridge_Distance_Stream_Outlet, Bridge_Normalised_Distance_Trunk_Stream.
  - Hydrology: Bridge_Upstream_Area, Bridge_Stream_Order, Bridge_Stream_Elevation, Bridge_Stream_Slope.
- Geomorphology descriptors (from Google Earth imagery):
  - Channel_Confinement, Channel_No_of_Threads, Channel_Planform.
- RivWidthCloud metrics (width statistics from GEE analysis):
  - T*_Min_Width, T*_Max_Width, T*_Mean_Width, T*_Std_Dev_Width.
  - T*_Active_Channel_No_Pixels, T*_Active_Channel_Area (active channel mask statistics).
- Similarity coefficients between time steps (RivWidthCloud outputs):
  - T1_T2_Jaccard, T1_T2_Dice, T2_T3_Jaccard, T2_T3_Dice, T3_T4_Jaccard, T3_T4_Dice, T1_T4_Jaccard, T1_T4_Dice.
- File naming convention:
  - Active channel masks: FID_Bridge_Name_T*_Active_Channel.tif.
  - Width estimates: FID_Bridge_Name_T*_Active_Channel_Widths.csv.

## How characteristics were derived
- Bridge data: Retrieved from the DPWH Detailed Bridge Inventory Application (2020). Filtered to permanent bridges with deck length >= 200 m (n=256); visually checked for contemporary river crossings (n=182); retained bridges where active channel width >150 m (n=74).
- Stream network and geomorphology: Using a 2013 IfSAR DEM (5 m, 1 m vertical accuracy), DEM resampled to 30 m; hydrologically corrected with TopoToolbox; bridge points snapped to the stream network; upstream area, slope, and Strahler order extracted; slope averaged over 0.3 km; bridges’ positions normalised along the trunk stream.
- Geomorphology descriptors: Assigned from contemporary Google Earth imagery (confinement, number of threads, channel pattern).
- Active channel change and RivWidthCloud: Google Earth Engine workflow described in the accompanying document Boothroyd_et_al_STOTEN_Google_Earth_Engine_code_SUPPORTING_DOCUMENTATION.rtf.

## Data formats and access
- Formats: SHP (vector), CSV (tabular), TIFF (raster).
- Coverage: 74 bridges (deck length ≥200 m) with 592 time-interval outputs for active channel masks and widths.
- Naming conventions: Time-interval tagging included in FID_Bridge_Name_T*_Active_Channel.* and corresponding widths CSV.

## How this supports data use
- Enables cross-referencing bridge attributes with river morphology and planform change to inform infrastructure planning, risk assessment, and river management.
- Provides self-serve data products: combine bridge data with stream/geomorphology and active channel metrics for analyses, dashboards, or GIS workflows.
- Facilitates integration with DPWH data for policy, planning, and long-term monitoring of bridge resilience to river migration.

## Acknowledgements and references
- Data provided by the Philippines Department of Public Works and Highways (DPWH). Data contributions from DPWH Planning Service and Department of Public Works and Highways.
- Funded by Natural Environment Research Council (NERC) and DOST-PCIEERD Newton Fund grant NE/S003312.
- References include Beechie et al. (2006), Boothroyd et al. (2020a), Brierley & Fryirs (2005), Church (2006), Schwanghart & Scherler (2014), and Yang et al. (2019).