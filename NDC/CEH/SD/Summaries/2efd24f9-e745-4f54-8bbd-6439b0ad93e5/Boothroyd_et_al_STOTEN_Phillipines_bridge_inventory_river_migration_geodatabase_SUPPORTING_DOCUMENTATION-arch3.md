# Supporting documentation for: Boothroyd_et_al_STOTEN_Phillipines_bridge_inventory_river_migration_geodatab ase.csv and Boothroyd_et_al_STOTEN_Phillipines_bridge_inventory_river_migration_geodatab ase.shp

- Purpose and scope
  - Provides hydro-morphological and bridge characteristics data for 74 bridges in the Philippines (bridges over 200 m deck length) linked to river migration analysis and planform changes.
  - Includes active river channel width statistics and similarity metrics (RivWidthCloud) derived from remotes sensing, plus related stream and geomorphology descriptors.
  - Output formats: .csv and .shp for bridge, stream, geomorphology, and RivWidthCloud attributes; 592 active channel mask/width files (raster and CSV).

- Data sources and selection criteria
  - Bridge data sourced from the Detailed Bridge Inventory Application (DPWH, 2020), originally covering 8,410 national-road bridges with attributes such as location, length, road type.
  - Selection steps:
    - Filter to permanent bridges with deck length >= 200 m (n = 256).
    - Visual check to confirm location at contemporary river crossings (n = 182).
    - Keep bridges where active channel width > 150 m (≈ five Landsat pixels) resulting in 74 bridges used for analysis.
  - Elevation and hydrology data:
    - Nationwide IfSAR DEM (2013), 5 m resolution; resampled to 30 m for processing.
    - TopoToolbox used for hydrologic corrections and stream network extraction; bridge points snapped to the stream network.

- Derived metrics and methodologies
  - Stream network and geomorphology
    - Extracted upstream area, Strahler stream order, and channel slope (averaged over 0.3 km segments) at each bridge point.
    - Bridge position normalised along trunk stream length to allow comparisons across streams of different lengths.
    - Geomorphic descriptors appended per bridge from contemporary Google Earth imagery: confinement (confined/partly confined/laterally unconfined), number of channel threads, and channel pattern (straight/meandering/wandering/braided).
  - Active river channel change and RivWidthCloud
    - Active channel change (planform adjustment) and RivWidthCloud width statistics computed via Google Earth Engine workflow (details in a separate supporting document).
    - RivWidthCloud outputs per bridge site include: min, max, mean, and standard deviation of active channel width; and (for similarity) counts of width measurements and related metrics.
    - Normalised trunk-stream position and associated width statistics enable cross-bridge comparisons over time.
  - Similarity coefficients for channel change
    - Time-interval based similarity between active channel masks using Jaccard and Dice coefficients (e.g., T1_T2_Jaccard, T1_T2_Dice, T2_T3_Jaccard, etc., including T1_T4 variants).
  - File naming and data organization
    - Active channel masks: FID_Bridge_Name_T*_Active_Channel.tif
    - Width estimates: FID_Bridge_Name_T*_Active_Channel_Widths.csv
    - Each file corresponds to a bridge, a time interval, and specific measurements or descriptors.

- Data contents and structure
  - Bridge inventory characteristics (from DPWH data)
    - Key fields: Bridge_Latitude (B_Lat), Bridge_Longitude (B_Long), Bridge_Name (B_Name), Bridge_ID (B_ID), Bridge_Material (B_Mat), Bridge_Road_Name (B_Rd_Nm), Bridge_Road_Type (B_Rd_Ty), Bridge_Island (B_Is), Bridge_Region (B_Rg), Bridge_Province (B_Pro), Bridge_Deck_Length (B_D_Len, m), Bridge_Deck_Width (B_D_Wid, m), Bridge_Year_Construction (B_Yr_Con), Bridge_Age_2020 (B_Age_2020, yrs), Bridge_No_Abutments (B_No_Abut), Bridge_No_Piers (B_No_Pier), Bridge_Pier_Height (B_Pier_H, m), Bridge_Condition (B_Con).
  - Stream network characteristics (from 30 m DEM analysis)
    - Distances and positions: Bridge_Distance_Channel_Head (B_Dis_Ch, km), Bridge_Distance_Stream_Outlet (B_Dis_So, km), Bridge_Normalised_Distance_Trunk_Stream (B_Norm_Dis, -).
    - Upstream area, order, elevation, slope: Bridge_Upstream_Area (B_Up_Area, km^2), Bridge_Stream_Order (B_S_Ord, -), Bridge_Stream_Elevation (B_S_Elev, m), Bridge_Stream_Slope (B_S_Slope, m/m).
  - Geomorphology characteristics (from imagery)
    - Channel confinement (Cha_Conf), Channel_No_of_Threads (Cha_No_Thr), Channel_Planform (Cha_Plan) with normalised trunk distances.
  - RivWidthCloud characteristics
    - Width statistics along the channel: T*_Min_Wid (Min_Width), T*_Max_Wid (Max_Width), T*_Mean_Wid (Mean_Width), T*_Std_Wid (Std_Dev_Width); Width counts (T*_Wid_Ct) and active channel pixel/area metrics (T*_Active_Channel_No_Pixels, T*_Active_Channel_Area).
  - Similarity coefficient characteristics
    - Jaccard and Dice coefficients for consecutive time intervals (T1_T2_Jaccard, T1_T2_Dice, T2_T3_Jaccard, T2_T3_Dice, T3_T4_Jaccard, T3_T4_Dice, T1_T4_Jaccard, T1_T4_Dice).

- Related documentation and code
  - A detailed Google Earth Engine workflow for active channel change and RivWidthCloud analysis is described in a separate document: Boothroyd_et_al_STOTEN_Google_Earth_Engine_code_SUPPORTING_DOCUMENTATION.rtf.
  - Acknowledges DPWH data providers and project funding (NERC and DOST-PCIEERD Newton Fund grant NE/S003312).

- Data use, governance, and considerations for monitoring frameworks
  - Data are designed to support monitoring infrastructure risk and river migration dynamics by providing a baseline of bridge and channel morphology characteristics.
  - Metadata and openness considerations:
    - Some datasets require public sharing of underlying data, which can be a barrier; project governance emphasizes data provenance, quality assurance, and clear data management practices.
  - Limitations and scope
    - Narrow to 74 bridges with specific criteria; may not cover all critical infrastructure.
    - Data reflect conditions captured up to 2020; updates require new surveys and processing, including time-stamped GEE workflows.
  - Practical utility for monitoring frameworks
    - Enables tracking decadal river migration around major bridges, quantifying planform changes with Jaccard/Dice metrics, and comparing active channel widths (RivWidthCloud) across time.
    - Provides rich contextual information (geomorphology, upstream area, channel order) to interpret observed channel changes and potential infrastructure risk.