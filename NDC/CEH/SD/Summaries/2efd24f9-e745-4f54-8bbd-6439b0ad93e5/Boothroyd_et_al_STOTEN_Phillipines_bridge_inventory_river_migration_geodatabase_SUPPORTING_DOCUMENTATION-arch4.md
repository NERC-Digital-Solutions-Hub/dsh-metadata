# Supporting documentation for: Boothroyd_et_al_STOTEN_Phillipines_bridge_inventory_river_migration_geodatab ase.csv and Boothroyd_et_al_STOTEN_Phillipines_bridge_inventory_river_migration_geodatab ase.shp

## Overview
- Provides the Philippines bridge inventory and river migration geodatabase associated with Boothroyd et al. (2020).
- Includes hydro-morphological and bridge characteristics for 74 bridges (deck length > 200 m) in the Philippines.
- Data types: bridge characteristics, stream network characteristics, geomorphic characteristics, similarity coefficients for active river channel change, and RivWidthCloud-derived active channel width statistics.
- Active channel masks (raster) and channel width estimates (CSV) are provided for each bridge site, totaling 592 files.
- Available formats: CSV and SHP; related raster and CSV files accompany the dataset.

## Data content and structure
- Bridge inventory attributes (from DPWH Detailed Bridge Inventory Application):
  - Location: Bridge_Latitude, Bridge_Longitude, Bridge_Name, Bridge_ID, Bridge_Material, Bridge_Road_Name, Bridge_Road_Type.
  - Description and identifiers: Island, Region, Province, and Bridge_Island metadata.
  - Physical attributes: Bridge_Deck_Length (m), Bridge_Deck_Width (m), Bridge_Year_Construction, Bridge_Age_2020 (years), Bridge_No_Abutments, Bridge_No_Piers, Bridge_Pier_Height (m), Bridge_Condition.
- Stream network characteristics (from 30 m DEM analysis):
  - Distances: Bridge_Distance_Channel_Head, Bridge_Distance_Stream_Outlet, Bridge_Normalised_Distance_Trunk_Stream.
  - Morphometric: Bridge_Upstream_Area, Bridge_Stream_Order, Bridge_Stream_Elevation, Bridge_Stream_Slope.
- Geomorphology characteristics (from Google Earth imagery):
  - Channel_Confinement, Channel_No_of_Threads, Channel_Planform.
- RivWidthCloud characteristics (width extraction metrics):
  - Width statistics: Min, Max, Mean, Std_Dev for active channel width (per bridge and along trunk distance).
  - Count of width samples: T*_Widths_Count.
- Similarity coefficient characteristics (active channel mask comparisons across time intervals):
  - T1_T2_Jaccard, T1_T2_Dice, T2_T3_Jaccard, T2_T3_Dice, T3_T4_Jaccard, T3_T4_Dice, T1_T4_Jaccard, T1_T4_Dice.
- Naming conventions:
  - Active channel masks: FID_Bridge_Name_T*_Active_Channel.tif
  - Active channel widths: FID_Bridge_Name_T*_Active_Channel_Widths.csv

## Derivation methods and processing steps
- Bridge data source and filtering:
  - Source: Detailed Bridge Inventory Application (DPWH, 2020) with 8,410 bridges along national roads.
  - Definition: road over a waterway with clear span ≥ 3 m.
  - Filtering: permanent bridges with deck length ≥ 200 m (n=256); visual verification for crossing contemporary rivers (n=182); active channel width > 150 m (n=74) selected for analysis.
- Stream network and geomorphology:
  - DEM: 2013 IfSAR DEM (5 m, high vertical accuracy); resampled to 30 m due to processing constraints.
  - Hydrological correction and stream extraction via TopoToolbox; bridge points snapped to stream network.
  - Extracted at-bridge metrics: upstream area, channel slope, Strahler order; slope averaged over 0.3 km segments.
  - Bridge position normalization: distance along trunk stream from channel head to bridge, divided by total trunk length to outlet.
  - Qualitative geomorphic descriptors appended from Google Earth imagery: confinement, number of threads, channel pattern.
- Active channel change and width analysis:
  - Active river channel change (planform adjustment) and RivWidthCloud analyses performed in Google Earth Engine (GEE); detailed workflow described in separate supporting document.
- Data organization:
  - Comprehensive metadata describing fields, units, and relationships between bridge, stream, geomorphology, and width metrics.

## Metadata, fields, and data quality
- Extensive metadata accompanying the dataset, including descriptions, units, and short names for all fields.
- Provenance and data lineage emphasized:
  - DPWH data provide primary bridge attributes.
  - DEM-based hydrology and geomorphology derivations.
  - Visual validation and cross-referencing with Google Earth imagery.
- Data quality considerations:
  - Selection criteria introduce a bias toward large, recent, or wide channels (may exclude smaller or older structures).
  - Active channel width and planform metrics rely on remote sensing and GIS-derived methods, with validation linked to the supporting GEE workflow.

## Access, usage, and governance implications for Data Leaders
- Centralized, well-documented data asset with explicit lineage from national inventories to GIS-derived products.
- Rich metadata and standardized attribute naming support discoverability, interoperability, and governance.
- Suitable for infrastructure risk assessment, river migration analyses, and policy planning related to river-bridge interactions.
- Facilitates cross-domain collaboration: bridge engineers, geomorphologists, and data stewards can co-own data products and contribute improvements.

## Acknowledgements and references
- Acknowledges DPWH for bridge inventory data; DPWH Statistics Division and related agencies.
- Funded by NERC and DOST-PCIEERD Newton Fund grant NE/S003312.
- Key references include Beechie et al. (2006), Church (2006), Schwanghart & Scherler (2014), Yang et al. (2019), Boothroyd et al. (2020a) and related methodological sources.