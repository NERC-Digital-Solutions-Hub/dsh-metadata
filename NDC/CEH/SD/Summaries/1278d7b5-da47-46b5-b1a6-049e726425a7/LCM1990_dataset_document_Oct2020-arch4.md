# Dataset documentation

## Overview
- Land Cover Map 1990 (LCM1990) is a parcel-based UK land cover map, classified into 21 classes based on UK Biodiversity Action Plan Broad Habitats.
- Created from two-date Landsat-5 composites (30 m resolution); designed to be compatible with later LCM frameworks (LCM2007, LCM2015) to support a 25-year land cover change product.
- Maps land cover (not strictly land use); some classes may not reflect exact land use (e.g., arable area vs. arable land use).
- LCM1990 is a stable, archived dataset with Digital Object Identifiers (DOIs) for citation.

## Data products
- Core vector dataset: polygons with attached metadata (dominant class, source image, uncertainty, pixel counts, etc.). GB has ~6.7 million polygons; NI ~0.9 million.
- 25 m raster: derived from the vector, 3-band GeoTIFF per area:
  - Band 1: dominant LCM1990 class per polygon
  - Band 2: mean per-polygon confidence (from Random Forest)
  - Band 3: percentage of the polygon covered by the modal class
- 1 km raster products: created by aggregating 25 m data to 1 km squares. Outputs include:
  - Dominant cover (1 band) for target and aggregate classes
  - Percentage cover (1 km) for 21 target classes and 10 aggregate classes
  - Note: percentage values are rounded; sums may diverge from 100 near coastlines due to mapping extents.

## Classification, attributes, and uncertainty
- 21 LCM1990 classes are linked to Broad Habitats; some classes are split or refined (e.g., Built-up Areas into Urban/Suburban; Dwarf Shrub Heath into Heather/Heather grassland; Littoral Sediment into Saltmarsh and Littoral sediment).
- Each vector polygon includes:
  - gid: unique parcel identifier
  - hist: list of classes present in the polygon with pixel counts
  - mode: recommended dominant class (1–21)
  - purity: percentage of polygon covered by the modal class
  - conf: mean per-polygon confidence (0–100)
  - stdev: uncertainty standard deviation
  - n: number of pixels in the polygon
  - cmp: composite image source
- Uncertainty per-pixel probability is provided by the Random Forest classifier and is available as per-polygon statistics (and in the 25 m raster).

## Class mapping and documentation
- Tables and appendices define mappings between LCM1990 classes, Broad Habitats, and color codes; Appendix 1–3 cover class interpretations, color mapping, and composite image details.
- The dataset uses a stable parcel framework and a 0.5 ha minimum mapping unit (polygons smaller than 0.5 ha are dissolved).

## Data access and licensing
- 25 m and 1 km rasters are available via the CEH Environmental Information Platform (eip.ceh.ac.uk).
- The full vector product is available on request under licence from CEH (licence fees may apply).
- Coordinate systems:
  - GB: British National Grid
  - NI: Irish National Grid (TM75)
- Data citation: each product has a DOI; publications should cite the DOI (author and date) and full DOI in the references.

## Quality assurance and validation
- Data are produced with defined methods and QA checks, including:
  - Correct projections and spatial completeness
  - Modal class verification for vector polygons
  - Metadata alignment and value ranges (0–100 for raster products)
  - Pixel size accuracy
- Validation has been conducted against external datasets (Countryside Survey, National Forest Inventory, validation points); results to be reported in a separate publication.

## Technical details and access notes
- GB and NI datasets are distributed as uncompressed GeoTIFFs; compression may be used to reduce file sizes.
- Data are intended to be interoperable with LCM2007/2015 frameworks to enable long-term change analyses.
- 0.5 ha minimum mapping unit and MMU considerations affect small features and coastal extents.

## Appendices and supporting information
- Appendix 1: Comments on LCM1990 class definitions and field interpretation (alignment with Broad Habitat definitions).
- Appendix 2: Summary of Broad Habitat definitions (as per JNCC Jackson 2000) for context.
- Appendix 3: Standard LCM color mapping recipe for visualization.
- Appendix 4: Details of composite images used in training and classification.

## How to cite and contact
- For data use, cite the corresponding DOI for the product (GB NI vector, 25 m raster, 1 km targets and aggregates) following guidance in the document.
- For access or licensing questions, contact spatialdata@ceh.ac.uk; main data portal: https://eip.ceh.ac.uk/lcm/lcmdata.

## Acknowledgement and references
- Funded by the Natural Environment Research Council (award NE/R016429/1) as part of the UK-SCAPE programme.
- Key references: Jackson 2000; Morton et al. 2011; Rowland et al. 2020a, 2020b.