# Dataset documentation

- LCM2015 (Land Cover Map 2015) provides UK parcel-based land cover maps classified into 21 Broad Habitat classes, using two-date Landsat-8 (30 m) composites and, where needed, AWIFS data (60 m).
- Outputs are designed for a broad user base and include a core vector product, a 25 m raster, and 1 km aggregated products; the vector and raster share detailed per-polygon information, while 1 km products provide summary coverage.

- Data products
  - Core vector data: 6.7 million polygons (GB) and 0.9 million (NI) with rich attributes.
  - 25 m raster: two-band image per polygon — band 1 = dominant class; band 2 = mean per-polygon probability from Random Forest.
  - 1 km rasters: dominant class and percentage cover for both 21 target classes and 10 aggregate classes (rounded to integers; total may differ slightly from 100% due to rounding).
  - Data formats cover a range of applications; GB and NI datasets are provided separately due to different projections.

- Classification and methodology
  - 21 classes based on UK Biodiversity Action Plan Broad Habitats (JNCC Jackson, 2000).
  - Uses a Random Forest classifier (instead of Maximum Likelihood) with ancillary data included as inputs, enabling multi-modal training and reducing need for spectral sub-classes.
  - Training areas built from a stable set (areas classified the same in 2000 and 2007) plus targeted coastal and poorly mapped classes; extensive manual refinement is avoided by integrating ancillary data into the classification step.
  - No segmentation is used in the LCM2015 spatial framework, improving consistency for change mapping; segmentation in LCM2007 caused inconsistencies.

- Output differences and methodological changes (from LCM2007)
  - Montane class removed; inland upland areas reclassified spectrally (use LCM2007 for Montane distribution).
  - Rough grassland removed; grassland types align with JNCC Broad Habitats without relying on soil data.
  - 25 m raster includes a second band with probability; vector data includes mean polygon probability.
  - No spectral sub-classes; Random Forest handles multi-modal data without sub-class grouping.
  - Spatial framework uses per-pixel classification; no segmentation in LCM2015; fixed some spatial framework errors.

- Spatial scope and scale
  - UK-wide land cover mapping (Great Britain and Northern Ireland) with separate projections:
    - GB: British National Grid (EPSG 27700)
    - NI: TM75 Irish Grid (EPSG 29903)

- Classes and labeling
  - 21 LCM2015 target classes (aligned to JNCC Broad Habitats), with some internal subdivisions (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment subdivided into Saltmarsh and Littoral sediment).
  - Each parcel has a unique geometry id (gid) to support unambiguous communication; retain gid for data use and development.

- Metadata, uncertainty, and data quality
  - Rich metadata at polygon level; includes dominant class, pixel counts per class, mean probability, and per-polygon uncertainty (0–255 scale) with standard deviation.
  - Per-polygon probability from Random Forest provides an uncertainty estimate; 1 km products include aggregated uncertainty considerations.
  - Minimum mappable area: >0.5 ha; parcels smaller than 0.5 ha or very narrow lines dissolved into surrounding landscape.

- Data access and licensing
  - 1 km raster data available via CEH Environmental Information Platform (eip.ceh.ac.uk).
  - Full vector and 25 m raster products available on request under licence from CEH; some applications may incur licence fees.
  - Each product has its own DOI; cited data enable reproducibility.

- Citing and DOIs
  - DOIs provided for GB vector, GB 25 m, GB 1 km target classes, GB 1 km aggregate classes, and NI equivalents; use DOI citations in publications to ensure traceability (examples provided in the document).

- Usage notes and cautions
  - LCM2015 is a stable, archived dataset; use caution when mapping change or interpreting differences over time due to differences in methods and data sources between versions.
  - Output differences vs. LCM2007 include removal of segmentation, updated classification algorithms, and integration of ancillary data into the classification process.
  - LCM2015 maps land cover rather than land use; some land uses may not be distinguishable spectrally (e.g., recreation grass vs. grazed grass).

- Accessing and using the data
  - Data access portals and contact: CEH Spatial Data Team; spatialdata@ceh.ac.uk; online application forms for full vector/25 m products.
  - For UK-wide products, reference the respective DOIs when citing in research and reports.

- Additional references and appendices
  - Appendices provide mappings between LCM2015 classes and Broad Habitats definitions, color mappings, and composite image details used in the 2015 production.
  - Foundational background and methodological details are grounded in Jackson (2000) and Morton et al. (2011).