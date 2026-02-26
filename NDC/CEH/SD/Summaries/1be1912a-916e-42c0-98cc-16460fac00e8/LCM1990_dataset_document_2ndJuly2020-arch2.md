# Dataset documentation

## Overview

- Land Cover Map 1990 (LCM1990) is a UK parcel-based land cover map created from Landsat-5 two-date composites at ~30 m resolution.
- Contains 21 land cover classes based on UK Biodiversity Action Plan Broad Habitat definitions; designed for compatibility with LCM2015 and to enable long-term change analysis (25-year horizon).
- Maps land cover (not strictly land use); some classes may not directly indicate land use (e.g., grass used for recreation vs. grazing).
- Stable, archived dataset with Digital Object Identifiers (DOIs) for citation; aimed to support environmental monitoring and policy performance assessments over time.
- Minimum mappable unit is >0.5 ha; polygons <0.5 ha and narrow features are dissolved into surrounding landscape.

## Data products and structure

- Vector data set
  - Polygons with 8 key attributes plus a unique geometry identifier (gid); GB: ~6.7 million polygons, NI: ~0.9 million.
  - Attributes include dominant class (mode), pixel counts per class within the polygon, uncertainty metrics, and a per-polygon confidence (conf) and standard deviation (stdev) of the classification.
  - hist attribute lists all classes present in the polygon and their pixel counts; recommended to retain gid for unambiguous communication.
- Raster data sets
  - 25 m raster: 3 bands per polygon (dominant class, per-polygon confidence, and percent area covered by the modal class).
  - 1 km raster: aggregates derived from the 25 m data to provide dominant class and percentage cover for both 21 target classes and 10 aggregate classes.
  - Projection and extents differ between GB (British National Grid) and NI (TM75 Irish Grid).
- Class structure
  - 21 target LCM1990 classes based on Broad Habitats; some classes are split for greater detail:
    - Built-up Areas and Gardens -> Urban and Suburban
    - Dwarf Shrub Heath -> Heather and Heather grassland
    - Littoral Sediment -> Saltmarsh and Littoral sediment
  - Table mapping provided links LCM1990 classes to Broad Habitats and aggregate counterparts.
- Metadata and uncertainty
  - Rich polygon-level metadata including dominant class probability and per-pixel uncertainty from the classifier (Random Forest).
  - Uncertainty information included in both vector (per-polygon) and raster outputs.

## Data access and citation

- Access
  - 25 m and 1 km raster data available via the CEH Environmental Information Platform (eip.ceh.ac.uk).
  - Full vector product available on request from CEH (licensing may apply).
- Citation (DOIs)
  - All LCM1990 products have individual DOIs for proper citation in publications.
  - Examples: GB vector, GB 25 m raster, GB 1 km percentage/dominant targets, NI equivalents.
  - Include authors and year in text and full DOI in references.
- Map projections
  - GB vector/raster: British National Grid; NI vector/raster: TM75 Irish Grid.

## Quality assurance and validation

- QA checks ensure accuracy of projections, spatial completeness, and correct polygon modal class in vector products; 0–100 value range checks for raster percentages; correct pixel sizes for rasters.
- Validation against other datasets (e.g., Countryside Survey, National Forest Inventory) conducted; results to be reported in a separate publication.
- The dataset uses a consistent object-based framework aligned with LCM2007/LCM2015 to enable cross-era comparisons.

## Usage notes and considerations

- Purpose and interpretation
  - LCM1990 provides a spectral-based land cover map; some land cover classes may not map cleanly to land use without ancillary data.
- Spatial resolution and aggregation
  - 25 m detail used for vector rasters; 1 km products summarize 25 m data for broad-scale modelling (e.g., weather, species distribution).
- Data granularity
  - The vector product offers rich metadata but larger file sizes; the 25 m raster is more compact and easier for processing.
- Data sensitivity and reproducibility
  - Do not omit the gid or misinterpret per-polygon hist and confidence fields; cite DOIs when using outputs in research.
- Related materials
  - Appendices provide detailed class definitions, standard color mappings, and information on composites used for classification.

## Appendices (highlights)

- Appendix 1: Detailed class interpretations and mapping notes for LCM1990 classes.
- Appendix 2: Summary of Biodiversity Action Plan Broad Habitats definitions (JNCC Jackson 2000).
- Appendix 3: Standard LCM color-mapping recipes for class visualization.
- Appendix 4: Composite images and metadata used in the classification process.

## Acknowledgements and references

- Funded by Natural Environment Research Council (NE/R016429/1) as part of UK-SCAPE National Capability.
- Key references: Jackson (2000) Broad Habitat definitions; Morton et al. (2011) LCM2007 methodology; Rowland et al. (2020a, 2020b) Land Cover Change 1990-2015.
- Contact and further information: CEH Environmental Information Platform and spatialdata@ceh.ac.uk.