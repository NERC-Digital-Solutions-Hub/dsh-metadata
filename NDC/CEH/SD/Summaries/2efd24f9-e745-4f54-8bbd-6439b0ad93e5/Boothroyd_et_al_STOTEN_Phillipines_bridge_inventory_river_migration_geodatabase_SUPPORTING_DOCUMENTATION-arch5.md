# Supporting documentation for:
Boothroyd_et_al_STOTEN_Phillipines_bridge_inventory_river_migration_geodatab ase.csv and Boothroyd_et_al_STOTEN_Phillipines_bridge_inventory_river_migration_geodatab ase.shp

## Overview
- Provides hydro-morphological and bridge characteristics for 74 Philippines bridges with deck lengths of 200 m or more.
- Includes: bridge attributes, stream network characteristics, geomorphic descriptors, and RivWidthCloud-based active channel width statistics.
- Data available in CSV, SHP, and associated raster/CSV files (592 files in total: 74 time-intervals x 4 time steps x 2 file types).

## What is included
- Bridge inventory and river migration geodatabase with fields such as:
  - Bridge location: Bridge_Latitude, Bridge_Longitude, Bridge_Name, Bridge_ID
  - Bridge characteristics: Bridge_Material, Bridge_Road_Name, Bridge_Road_Type, Bridge_Deck_Length, Bridge_Deck_Width, Bridge_Year_Construction, Bridge_Age_2020, Bridge_No_Abutments, Bridge_No_Piers, Bridge_Pier_Height, Bridge_Condition
  - Bridge geography/administrative: Bridge_Island, Bridge_Region, Bridge_Province
  - Stream network characteristics: Bridge_Distance_Channel_Head, Bridge_Distance_Stream_Outlet, Bridge_Normalised_Distance_Trunk_Stream, Bridge_Upstream_Area, Bridge_Stream_Order, Bridge_Stream_Elevation, Bridge_Stream_Slope
  - Geomorphology characteristics (from imagery): Channel_Confinement, Channel_No_of_Threads, Channel_Planform
  - RivWidthCloud statistics: T*_Min_Width, T*_Max_Width, T*_Mean_Width, T*_Std_Dev_Width, T*_Active_Channel_No_Pixels, T*_Active_Channel_Area, plus associated normalised metrics
  - Similarity metrics for active river channel masks (e.g., T1_T2_Jaccard, T1_T2_Dice, T2_T3_Jaccard, etc.)
- Data formats and files:
  - Geodatabase: Boothroyd_et_al_STOTEN_Phillipines_bridge_inventory_river_migration_geodatabase.csv and .shp
  - For each bridge site and time interval: FID_Bridge_Name_T*_Active_Channel.tif (active channel mask) and FID_Bridge_Name_T*_Active_Channel_Widths.csv (width statistics)
  - Total: 592 supporting files (74 bridges x 4 time steps x 2 file types)

## How the data were derived
- Source data: Detailed Bridge Inventory Application (DPWH, 2020). Initial set contained 8,410 bridges along national roads with attributes including length, construction year, and road type.
- Bridge selection and filtering:
  - Defined as structures carrying a road over a waterway with clear span ≥ 3 m.
  - Filtered to permanent bridges with deck length ≥ 200 m (n = 256).
  - Visual verification to ensure bridges correspond to contemporary river crossings (n = 182).
  - Retained bridges where active channel width > 150 m (≈ five Landsat pixels) (n = 74).
- Spatial/geomorphometric processing:
  - DEM: 2013 IfSAR, ~5 m resolution; DEM resampled to 30 m for processing.
  - Hydrologic correction and stream network extraction with TopoToolbox; bridge points snapped to the stream network.
  - Extracted: upstream area, channel slope (averaged over 0.3 km), and normalized bridge position along trunk stream.
  - Geomorphic descriptors appended from visual assessment of Google Earth imagery (confinement, number of threads, channel pattern).
- River/migration and width analysis:
  - Active river channel change and RivWidthCloud metrics derived using Google Earth Engine workflows; details described in a separate supporting document.

## Data structure and documentation
- File naming and contents:
  - Active channel masks: FID_Bridge_Name_T*_Active_Channel.tif
  - Channel width estimates: FID_Bridge_Name_T*_Active_Channel_Widths.csv
  - Naming convention explained to assist traceability across time intervals.
- Data dictionary elements:
  - Each field includes a descriptive name, short name, description, and units (e.g., meters for lengths, kilometers for distances, years for construction age, etc.).
  - Includes both inventory metadata (location, road info, bridge attributes) and analysis-derived attributes (geomorphology, stream metrics, RivWidthCloud statistics, similarity coefficients).

## Data provenance, quality, and governance
- Provenance:
  - DPWH bridge inventory data provided by DPWH and Philippines Statistics Division, Planning Service; accessible via DPWH portal.
  - Research conducted under NERC and DOST-PCIEERD-Newton Fund grant (NE/S003312).
- Processing transparency and reproducibility:
  - Detailed methodology for how bridge and stream attributes were derived (DEM processing, topology, snapping, and descriptor calculations) described in the document.
  - Google Earth Engine workflow referenced for active channel change and RivWidthCloud metrics; described in a separate supporting document.
- Data quality considerations:
  - Multi-step QA: verification against contemporary imagery, spatial alignment checks, and consistency between vector (shp/csv) and raster (tif) components.
  - Time-series width and mask data captured across four time intervals to enable change analysis.
- Usage and licensing:
  - Data originate from public DPWH datasets; acknowledgements provided to data providers.
  - Separate code/documentation exists for the GEE analysis; user should cite Boothroyd et al. (2020) and follow DPWH data usage terms as noted in acknowledgements.

## Practical considerations for Data Stewards
- Metadata completeness:
  - Ensure the data dictionary is maintained with field definitions, units, and provenance links.
  - Record the processing steps (DEM source, resampling, TopoToolbox parameters, snapping tolerance) to support reproducibility.
- Interoperability and standards:
  - Maintain consistent coordinate reference system and documentation of spatial references used.
  - Keep time-interval indexing consistent (T1–T4) across all per-bridge active channel and width files.
- Data updates and versioning:
  - Document any re-processing of DEMs, re-collection of bridge data, or changes in inclusion criteria.
  - Provide clear versioning so downstream users can reproduce historical analyses or compare with updated datasets.
- Access and attribution:
  - Preserve and reference DPWH data provenance and funding acknowledgments.
  - Provide guidance on appropriate citation (Boothroyd et al., 2020; related GEE workflow document).

## References and acknowledgments
- Acknowledgements:
  - Philippines Department of Public Works and Highways (DPWH) for bridge inventory data.
  - DPWH, Philippines Statistics Division, Planning Service; DPWH collaboration.
  - Funding: NERC and DOST-PCIEERD Newton Fund grant NE/S003312.
- References for background methods (geomorphology, river patterns, TopoToolbox, RivWidthCloud):
  - Beechie et al. (2006); Church (2006); Brierley & Fryirs (2005); Schwanghart & Scherler (2014); Yang et al. (2019).
- Additional documentation:
  - Google Earth Engine workflow documentation for active channel assessment and RivWidthCloud analysis (Boothroyd et al., STOTEN).