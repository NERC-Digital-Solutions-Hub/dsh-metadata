# Dataset documentation

- LCM1990 Overview
  - Land Cover Map 1990 (LCM1990) is a parcel-based UK land cover map classifying Landsat-5 imagery (30 m) into 21 classes based on UK Biodiversity Action Plan Broad Habitats.
  - Delivered as vector (polygons with attributes) and raster formats (25 m and 1 km products); core is the vector, from which the 25 m raster is derived.
  - Built to align with LCM2015/LCM2007 spatial frameworks to enable long-term change products (25-year horizon).

- Purpose and scope
  - Maps land cover (not strictly land use) and provides rich metadata, including per-polygon pixel breakdown and classification probabilities.
  - Stable, archived dataset with Digital Object Identifiers (DOIs) for citation.
  - Minimum mappable unit: polygons > 0.5 ha; dissolves parcels < 0.5 ha and linear features < 20 m.

- Data framework and compatibility
  - Uses updated LCM2007/LCM2015 spatial framework for cross-product compatibility.
  - Spatial framework derived from OS MasterMap (GB) and Northern Ireland equivalents; aimed at facilitating integration with other geospatial datasets.
  - Provides both 25 m raster (core 25 m, plus 1 km products) and vector data with extensive attributes.

- Class structure and labeling
  - 21 LCM1990 target classes mapped from 21 Broad Habitats; some are subdivided (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland).
  - Vector polygons carry a unique geometry ID (gid) for unambiguous communication; includes per-polygon class, pixel counts per class, and mean classification probability.
  - Aggregate classes (10) used for 1 km raster products to provide simplified summaries.

- Vector data specifics
  - Approximately 6.7 million polygons for Great Britain and 0.9 million for Northern Ireland.
  - Key attributes include: gid, hist (list of classes by pixel count), mode (recommended display class), purity, conf (mean per-polygon vote from Random Forest), stdev, n (number of pixels), cmp (composite image reference).
  - Rich metadata per polygon, including dominant class and per-class pixel breakdown.

- Raster data specifics
  - 25 m raster: 3-band, where band 1 = dominant class per polygon, band 2 = mean confidence, band 3 = percent of polygon covered by modal class.
  - 1 km rasters: dominant cover (target and aggregate) and percentage cover per class (target 21 bands, aggregate 10 bands). Values are integers; sums may not exactly total 100 due to rounding and coastal/perimeter effects.
  - Data for Great Britain and Northern Ireland provided separately with corresponding projections.
  - File format: uncompressed GeoTIFFs (8-bit unsigned); coordinate systems: GB = British National Grid; NI = Irish Grid (TM75).

- Data access and citations
  - 25 m and 1 km rasters available via CEH Environmental Information Platform (eip.ceh.ac.uk).
  - Full vector product available on request under licence from CEH (licences may apply).
  - DOIs provided for all products (GB vector, GB 25 m, GB 1 km target, GB 1 km dominant, GB 1 km aggregate, NI vector, NI 25 m, NI 1 km target, NI 1 km dominant, NI 1 km aggregate); citations should include author, date, and DOI.
  - Example citation format included in the documentation for incorporating DOIs into publications.

- Quality assurance and validation
  - QA checks cover projections, spatial completeness, modal class presence in polygons (vector), metadata headings, value ranges (0–100 for raster percent products), and pixel size accuracy.
  - Validation against external datasets (e.g., Countryside Survey, National Forest Inventory) conducted; results to be published separately.
  - Documentation notes that field boundary changes are infrequent due to reliance on master cartography; a full validation exercise accompanies product development.

- Access and contact
  - Data access details: CEH Environmental Information Platform; full vector data on request; licence information and fees may apply.
  - For access/inquiries: spatialdata@ceh.ac.uk
  - Further information: https://eip.ceh.ac.uk/lcm/lcmdata and dataset-specific CEH pages.

- Projections and formats at a glance
  - Great Britain: vector and rasters in British National Grid (EPSG 27700) and 25 m/1 km resolutions.
  - Northern Ireland: vector and rasters in TM75 Irish Grid (EPSG 29903) and 25 m/1 km resolutions.
  - Pixel details, extents, and coordinate data provided in the dataset documentation (Table 4 metadata references).

- Notes for GIS use
  - LCM1990 notes that some Broad Habitat distinctions are spectrally challenging and may require ancillary data or field validation for certain classifications.
  - For detailed analysis, retaining gid and per-polygon hist attribute enables reconstruction of class composition within polygons.
  - The 1 km products are suitable for UK-wide modelling in conjunction with meteorological or species distribution data; 25 m and vector products support higher-resolution analyses and map-based data visualisations.

- Related literature and references
  - DOIs and references for the GB and NI vector/raster products are provided to enable precise data citation and reproducibility.
  - Cited background papers and appendices provide further context on Broad Habitat definitions and class mappings.