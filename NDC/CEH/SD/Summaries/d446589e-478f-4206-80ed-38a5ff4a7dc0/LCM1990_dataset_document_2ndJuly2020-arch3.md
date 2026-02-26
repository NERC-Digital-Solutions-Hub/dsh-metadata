# Dataset documentation

## Overview
- Land Cover Map 1990 (LCM1990) is a UK parcel-based land cover map created from Landsat-5 imagery (30 m) classified into 21 classes.
- Classes are aligned to UK Biodiversity Action Plan Broad Habitat definitions; designed to support diverse data products and long-term monitoring.
- Built to be compatible with later LCM products (e.g., LCM2015) to enable 25 years of land cover change analysis.
- Provides both vector (parcels) and raster (25 m and 1 km) data products, with extensive metadata and uncertainty information.

## Data products and structure
- Vector data
  - 6.7 million polygons for Great Britain; 0.9 million for Northern Ireland.
  - Each parcel has a unique geometry identifier (gid) and attributes including dominant class, per-polygon class breakdown, mean classification probability, and related metadata.
  - 21 target LCM1990 classes; minimum mappable area of >0.5 ha; polygons smaller than 0.5 ha are dissolved.
  - Eight key attributes per polygon (including hist, mode, purity, conf, stdev, n, cmp).
- Raster data
  - 25 m raster (GB and NI separate projections): 3 bands per pixel (dominant class, per-polygon RF confidence, percent cover by modal class).
  - 1 km raster products: dominant cover for target and aggregate classes; and percentage cover for 21 target classes and 10 aggregate classes (rounded values may not sum exactly to 100% due to rounding and coastal edge effects).
  - Spatial framework built to maximise compatibility with LCM2015 for long-term change analysis.
- Class mapping and metadata
  - Table-based mapping between LCM1990 classes and aggregate classes; appendices describe broad habitat definitions and color mappings for visualization.
  - Rich metadata per polygon, including dominant class, pixel breakdown, and classification confidence.

## Data access and citation
- Access via CEH Environmental Information Platform (eip.ceh.ac.uk); full vector product available on request (licensing may apply).
- All LCM1990 products have individual DOIs; DOIs provided for GB and NI products to facilitate citation and reproducibility.
- Example citation format provided; guidance on data citation and DOIs available (eidc.ceh.ac.uk).
- Contact: spatialdata@ceh.ac.uk; further information at the CEH LCM1990 pages.

## Quality assurance and validation
- Data created with defined methods and code, produced by trained staff.
- QA checks include projection validation, spatial completeness, modal class verification, filename/headings consistency, value ranges (0–100 for raster percentages), and pixel size validation.
- Full validation against external datasets (e.g., Countryside Survey, National Forest Inventory) conducted; results to be reported in a separate publication.

## Use for monitoring and limitations
- Suitable as a long-term environmental monitoring base for policy scrutiny and decision-making, especially when integrated with other datasets (e.g., climate, biodiversity, and habitat data).
- Strengths: archived, parcel-based framework; per-polygon metadata and uncertainty; multiple resolutions (25 m and 1 km) for varied analyses; DOIs for reproducible usage.
- Limitations and caveats
  - Some land cover vs. land use distinctions are ambiguous; vegetation types may be spectrally separable but not always reflect management/intended use.
  - Certain habitat classes (e.g., Fen, Marsh and Swamp; Bog; Grasslands) can be misclassified due to spectral similarity and spatial resolution.
  - Coastal and fringe areas have special considerations; 1 km products may aggregate or approximate real-area percentages near coastlines.
  - LCM1990 is a stable, archived product; updates or revisions are not implied within this documentation.
  - Potential data access barriers due to licensing and metadata completeness; GDPR-like or governance barriers may apply in some contexts.

## Classification scheme and documentation
- 21 LCM1990 target classes tied to Broad Habitat definitions (Appendix 2) such as Broadleaved Woodland, Coniferous Woodland, Arable and Horticulture, Various Grasslands, Bracken, Heath, Fen/Marsh/Swamp, Bog, Water bodies, Inland Rock, Built-Up Areas and Gardens, and Coastal/Littoral habitats.
- Appendix 1 provides mapping nuances and interpretation notes for each Broad Habitat (e.g., woodland composition, grassland distinctions, and coastal classifications).
- Appendix 3 provides standard LCM color mappings for visualization.
- Appendix 4 documents the composite images used in the classification process.

## Citing and references
- Data are distributed with DOIs for each product (GB vector, GB 25 m, GB 1 km dominant/percentage products, NI vector, NI 25 m, NI 1 km products).
- References to methodological reports and related LCM products (e.g., Rowland et al. 2020 for Land Cover Change 1990–2015) are provided for context and methodological grounding.

## Contact and further information
- Data access and documentation available at CEH LCM1990 pages: https://eip.ceh.ac.uk/lcm/lcmdata
- For access details, licensing, and additional information, contact spatialdata@ceh.ac.uk.