# Dataset documentation

- LCM1990 is a parcel-based UK land cover map created from two-date Landsat-5 data (30 m resolution), classified into 21 classes aligned with UK Biodiversity Action Plan Broad Habitats. It uses an updated LCM2007 spatial framework to ensure polygonal mapping aligned with real-world boundaries and compatibility with other datasets.
- The product suite includes both vector and raster data to support diverse applications, with a focus on enabling analysis and self-service use.

## Data products and formats

- Vector data set
  - Polygons with attached attributes per parcel (gid, dominant class, per-polygon class breakdown, confidence metrics, and processing metadata).
  - Key attributes: gid, hist (class composition per polygon), mode (recommended display class 1–21), purity, conf, stdev, n, cmp (composite image).
  - Coverage: ~6.7 million polygons (GB) and ~0.9 million polygons (Northern Ireland).
- Raster data sets
  - 25 m raster (GB and NI): 3-band TIFF
    - Band 1: dominant LCM1990 class per polygon
    - Band 2: mean per-polygon confidence (RF vote-based)
    - Band 3: percentage of polygon area covered by the modal class
  - 1 km raster products (GB and NI): aggregate and percentage-cover products derived from the 25 m raster
    - Dominant cover (1 band) for target and aggregate classes
    - Percentage cover (21 bands for target; 10 bands for aggregates)
  - All rasters are 8-bit unsigned GeoTIFFs; coordinate systems differ by region (GB: British National Grid; NI: TM75 Irish Grid). The GB and NI rasters are provided separately to reflect distinct projections.
- Data volumes and resolution details
  - 25 m raster extents and resolution specified; 1 km products produced from 25 m data; coastal areas subject to rounding and percentage calculations.

## Class structure and mapping

- 21 LCM1990 classes based on UK Broad Habitats (with some refined splits, e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather Grassland; Littoral/Supra-littoral splits for coastal habitats).
- Tables and appendices map LCM1990 classes to Broad Habitats and provide standard color mappings for visualization.
- LCM1990 maps land cover (not strictly land use); some areas (e.g., recreation grass) may be ambiguous between land cover and land use.

## Data provenance and quality

- Spatial framework and class definitions are designed to maximise compatibility with LCM2015 and to enable long-term land cover change analyses (e.g., 25-year change products).
- DOIs exist for all products to support citation and reproducibility (GB vector, GB 25 m raster, GB 1 km percentage target class, GB 1 km dominant target class, GB 1 km aggregate percentages; NI equivalents listed similarly).
- Rich metadata: per-polygon attributes include detailed class composition, dominant class, and processing provenance; per-polygon uncertainty (confidence) and standard deviation are provided; per-pixel probability from Random Forest classifier is included in both vector and 25 m raster formats.
- Quality assurance: formal checks on projections, spatial completeness, modal class presence in polygons, value ranges (0–100 for percentage products), and pixel size accuracy; a full validation against external datasets is conducted with results to be published separately.

## Data access and citation

- Access: CEH Environmental Information Platform (eip.ceh.ac.uk) for 25 m and 1 km raster data; full vector product available on request (licence may apply).
- Licensing: some users may incur licence fees for certain applications.
- Citation guidance: each product has a DOI; cite with author(s) and date in-text and include full DOI citation in references (examples provided in the documentation).

## Projections and geographic coverage

- Vector and raster data are provided separately for Great Britain and Northern Ireland.
- Projections: GB vector in British National Grid; NI vector in Irish National Grid; corresponding raster products follow the same regional projections (EPSG: GB 27700 and NI 29903 for the 25 m and 1 km rasters, respectively).

## Access and contact

- Data access portal: https://eip.ceh.ac.uk/
- Vector data: available under licence on request from CEH; contact spatialdata@ceh.ac.uk for details.
- Additional information: CEH LCM1990 data page and related dataset documentation.

## Usage notes and considerations

- The dataset serves as a stable, archived product with long-term compatibility and methodology continuity (to enable multi-decadal analyses).
- A minimum mappable area threshold (>0.5 ha) and dissolution rules apply during production, which may affect small parcels and linear features.
- The 1 km raster products may show slight summation discrepancies due to rounding; coastal pixels may have totals that do not sum exactly to 100.
- LCM1990 provides both detailed polygon metadata and higher-level raster summaries to support a range of analytical approaches, including modelling and cross-dataset integration.

## Additional information

- Appendices cover detailed class definitions, BAP Broad Habitats descriptions, standard color mappings, and composite imagery used in the data production.
- Related background and companion studies underpinning the methodology and classification approach (e.g., LCM2007/LCM2015 lineage) are cited for users seeking deeper context.
- Acknowledgements and references note NERC CEH support and foundational habitat classification literature.