# Supporting documentation for:
Boothroyd_et_al_STOTEN_Phillipines_bridge_inventory_river_migration_geodatab ase.csv and Boothroyd_et_al_STOTEN_Phillipines_bridge_inventory_river_migration_geodatab ase.shp

- Overview
  - Datasets cover the Philippines bridge inventory and river migration geodatabase related to Boothroyd et al. (2020).
  - Includes hydro-morphological and bridge characteristics for 74 bridges (>200 m deck length) plus stream network, geomorphic descriptors, similarity coefficients for river planform change, and RivWidthCloud-derived active channel width statistics.
  - Available in .csv and .shp formats; active channel masks (.tif) and channel width estimates (.csv) provided for each bridge site (592 files total).

- Data provenance and selection criteria
  - Based on the Detailed Bridge Inventory Application (DPWH, 2020).
  - From an initial set of 8,410 bridges, filtered to permanent bridges with deck length >= 200 m (n = 256). Visual checks ensured contemporary river crossings (n = 182) and active channel width > 150 m (n = 74) were retained.

- Derivation of stream network and geomorphology
  - Used a 2013 IfSAR 5 m DEM (5 m resolution, ~1 m vertical RMSE) for topographic analysis.
  - DEM resampled to 30 m; hydrologically corrected with TopoToolbox; stream network extracted.
  - Bridge points snapped to the stream network; for each bridge: upstream area, channel slope, and Strahler order extracted; slope averaged over 0.3 km.
  - Bridge position normalized as trunk-stream length from channel head to bridge divided by total trunk length.
  - Geomorphic descriptors appended from Google Earth imagery: confinement (confined, partly confined, or laterally unconfined), number of channel threads, and channel pattern (straight, meandering, wandering, braided).

- Similarity coefficients and RivWidthCloud statistics
  - Google Earth Engine workflow documented separately (Boothroyd_et_al_STOTEN_Google_Earth_Engine_code_SUPPORTING_DOCUMENTATION.rtf).
  - Active river channel change assessed via planform change and RivWidthCloud analysis; includes Jaccard and Dice similarity across time intervals (T1–T2, T2–T3, T3–T4, T1–T4).

- Contents and naming of the geodatabase
  - Bridge inventory characteristics (from DPWI): identifiers, location, name, material, road name/type, status, deck measurements, age, abutments/pier counts, pier height, condition.
  - Stream network characteristics (from 30 m DEM analysis): distances to channel head/outlet, normalized trunk distance, stream order, elevation, slope.
  - Geomorphology descriptors (from imagery): channel confinement, number of threads, channel planform.
  - RivWidthCloud characteristics: width statistics (min, max, mean, std) and pixel counts; active channel pixel metrics and area.
  - Similarity coefficient characteristics: number of active-channel pixels and area.
  - File naming conventions:
    - Active channel masks: FID_Bridge_Name_T*_Active_Channel.tif
    - Widths per bridge: FID_Bridge_Name_T*_Active_Channel_Widths.csv

- Data quality, scope, and limitations
  - Based on publicly available DPWH data and satellite/DEM analyses; limitations include potential data gaps, resolution differences, and the relatively small bridge sample (n = 74) for broad generalizations.

- Acknowledgements
  - DPWH for bridge inventory data; data contributed by Philippines Statistics Division, Planning Service, and DPWH.
  - Funded by NERC and DOST-PCIEERD Newton Fund grant NE/S003312.

- References (selected)
  - Beechie, T.J. et al. 2006. Channel pattern and river-floodplain dynamics.
  - Boothroyd, R.J. et al. 2020a. National-scale assessment of decadal river migration at critical bridge infrastructure in the Philippines.
  - Brierley, G.J. & Fryirs, K.A. 2005. Geomorphology and River Management.
  - Church, M. 2006. Bed material transport and morphology of alluvial river channels.
  - Schwanghart, W. & Scherler, D. 2014. TopoToolbox 2.
  - Yang, X. et al. 2019. RivWidthCloud: Google Earth Engine algorithm for river width extraction.