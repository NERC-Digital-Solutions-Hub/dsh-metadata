# Supporting documentation for Boothroyd_et_al_STOTEN_Phillipines_bridge_inventory_river_migration_geodatab ase.csv and Boothroyd_et_al_STOTEN_Phillipines_bridge_inventory_river_migration_geodatab ase.shp

## What this dataset is
- A geodatabase and accompanying files describing the Philippines bridge inventory and river migration for 74 bridges with deck lengths greater than 200 m.
- Contains hydro-morphological and bridge characteristics, stream network and geomorphic descriptors, and similarity/rivwidth statistics indicating river planform changes.
- Outputs are provided in CSV, SHP (vector), and TIFF (raster) formats; 592 active-channel width and channel-mask files accompany the dataset.

## How the data were derived
- Bridge characteristics:
  - Based on the DPWH Detailed Bridge Inventory Application (2010s data).
  - From an initial set of 8,410 bridges, filtered to permanent bridges with deck length ≥200 m (n=256), then visually validated for contemporary river crossings (n=182), and finally retained where active channel width >150 m (n=74).
  - A bridge is defined as a road-carrying structure over a waterway with a clear span ≥3 m between supports.
- Stream network and geomorphology:
  - Used a 2013 IfSAR DEM (5 m resolution, 1 m vertical RMSE) for topographic analysis.
  - DEM resampled to 30 m; TopoToolbox applied for hydrologic correction and stream-network extraction.
  - Bridge points snapped to the stream network; upstream catchment area, channel slope, and Strahler order extracted; slope averaged over 0.3 km.
  - Bridge positions normalised along trunk stream length; geomorphic descriptors added from Google Earth imagery (confinement, number of threads, channel pattern).
- Active channel change and RivWidthCloud:
  - Active river channel change and RivWidthCloud width statistics generated via Google Earth Engine workflows (details in a separate supporting document).
- Metadata and structure:
  - Detailed field definitions cover bridge attributes, stream-network metrics, geomorphology descriptors, RivWidthCloud statistics, and similarity coefficients.

## What is included in the geodatabase
- Bridge inventory characteristics (from DPWH data): latitude, longitude, name, ID, material, road name/type, location (island, region, province), deck length/width, year of construction, age, number of abutments/piers, pier height, bridge condition.
- Stream network characteristics (from 30 m DEM analysis): distance to channel head, distance to outlet, normalised trunk distance, upstream area, stream order, elevation, slope.
- Geomorphology characteristics (from imagery): confinement, number of channels/threads, channel planform.
- RivWidthCloud characteristics: width statistics (minimum, maximum, mean, std dev) along with pixel counts.
- Similarity coefficient characteristics: Jaccard and Dice indices across successive time intervals (e.g., T1–T2, T2–T3, T3–T4, and T1–T4) for active-channel masks.
- Active channel masks and width estimates: named files following FID_Bridge_Name_T*_Active_Channel.tif and corresponding _Widths.csv (592 total files).

## File formats and naming conventions
- Active-channel masks: FID_Bridge_Name_T*_Active_Channel.tif
- Channel width estimates: FID_Bridge_Name_T*_Active_Channel_Widths.csv
- Time-interval naming reflects the Google Earth Engine analysis timeline and is described in the accompanying documentation.

## How this supports environmental monitoring
- Delivers a standardised, geo-referenced dataset to assess river migration and active channel dynamics around critical infrastructure.
- Enables cross-bridge, cross-time comparisons of planform changes and river-width changes, supporting assessment of environmental health, sediment dynamics, and infrastructure risk.
- Data are suitable for integration with other environmental datasets to increase data value and enable broader analyses beyond a single study.

## Access and usage notes
- Data originate from the Philippines DPWH and national statistics resources; usage requires acknowledgment of the listed sources and the NERC-DOST Newton Fund grant.
- The dataset emphasizes reproducible methods with explicit workflows and descriptors, facilitating replication and extension.

## Acknowledgements
- DPWH for bridge inventory data; data provided via the Detailed Bridge Inventory Application.
- Data contributed by the Philippines Statistics Division, Planning Service, and DPWH.
- Research supported by NERC and DOST-PCIEERD under NE/S003312.

## References (methodological context)
- Geomorphology and river-management frameworks (Beecchie et al. 2006; Church 2006).
- Topographic analysis tools (TopoToolbox; Schwanghart & Scherler, 2014).
- River width extraction and RivWidthCloud methodology (Yang et al., 2019).