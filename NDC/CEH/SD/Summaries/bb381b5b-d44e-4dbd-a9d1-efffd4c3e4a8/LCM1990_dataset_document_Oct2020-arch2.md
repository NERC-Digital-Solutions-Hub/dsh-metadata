# Dataset documentation

## Overview
- Land Cover Map 1990 (LCM1990) is a parcel-based UK land cover map classified into 21 classes, based on UK Biodiversity Action Plan Broad Habitat definitions.
- Created from two-date Landsat-5 composites (30 m) and aligned with the LCM2015 framework to enable long-term change analyses (25 years).
- Replaces the previous LCMGB; designed for compatibility with other geospatial data and to support diverse monitoring applications.
- Data products include vector (parcels), 25 m raster, and 1 km dominant/percentage cover outputs; all distributed with DOIs for citation.

## Data products and structure
- Vector data set: polygons with metadata per parcel; eight key attributes include dominant class, uncertainty, pixel counts, and communication-friendly identifiers; GB and NI totals: ~6.7M GB polygons and ~0.9M NI polygons; 21 target classes.
- Raster data sets:
  - 25 m raster: 3-band product (dominant class, per-polygon confidence, and modal-class coverage percentage).
  - 1 km raster: products summarise 25 m results into dominant and percentage cover for both 21 target classes and 10 aggregate classes.
  - Separate GB and NI data sets reflect different projections.

## Classes and mapping
- LCM1990 uses 21 classes derived from Broad Habitats; some classes are subdivided where spectral signals allow (e.g., Built-up Areas and Gardens into Urban and Suburban; Dwarf Shrub Heath into Heather and Heather grassland; Littoral Sediment into Littoral sediment and Saltmarsh).
- Table 2 (and Appendix 1) maps LCM1990 classes to Broad Habitats; Appendix 2 provides summarized Broad Habitat definitions.

## Spatial framework and data details
- Spatial framework designed for compatibility with LCM2007/LCM2015; polygons reflect real-world boundaries and facilitate cross-product comparisons.
- Minimum mappable area: >0.5 ha; parcels smaller than 0.5 ha and linear features under 20 m dissolved into surrounding landscape.
- Coordinate systems: GB in British National Grid; NI in Irish Grid (TM75); separate GB and NI rasters for projection consistency.

## Data quality, uncertainty, and validation
- Rich per-polygon metadata: dominant class, class composition, mean probability, and per-polygon confidence (from Random Forest classifier).
- Uncertainty information included in both vector and 25 m raster outputs.
- QA checks cover projections, spatial completeness, modal class presence, value ranges (0–100 for rasters), and pixel size accuracy.
- Full validation against Countryside Survey, National Forest Inventory, and validation points; results published separately.

## Access, licensing, and citation
- Data access:
  - 25 m and 1 km rasters: CEH Environmental Information Platform (eip.ceh.ac.uk).
  - Full vector product: available on request under licence from CEH.
- DOIs exist for all LCM1990 products (GB and NI) to enable precise citation.
- Citation guidance: include authors and year in-text; provide full DOI in references (examples given in the document).
- Contact for access and queries: spatialdata@ceh.ac.uk.

## Usage notes and caveats
- LCM1990 maps land cover, not always directly inferring land use; some land use distinctions require field validation.
- Some grassland classifications (e.g., Neutral and Calcareous Grasslands) can be spectrally similar to Improved Grassland; aggregation of classes may be appropriate for certain analyses.
- Coastal and water-related classes near coastline may have mapping limitations due to MMU and spectral/terrain factors.
- 1 km products use percentage sums that may not total exactly 100% due to rounding; coastal pixels may sum to less than 100%.

## Projections, extent, and scale
- GB and NI data are provided separately to reflect distinct projections.
- GB: British National Grid; NI: TM75 Irish Grid.
- 25 m raster provides high-detail outputs; 1 km rasters are suitable for broad UK-scale modelling with other datasets (e.g., meteorology, species distribution).

## Appendix highlights (for interpretation and colour mapping)
- Appendix 1: Notes on class mappings and behavior of specific Broad Habitats in LCM1990 (e.g., woodland types, grasslands, wetlands, urban categories).
- Appendix 2: Summary of Biodiversity Action Plan Broad Habitats (definitions and distinctions).
- Appendix 3: Standard colour-mapping recipe for LCM1990 classes.
- Appendix 4: Composite images used during LCM1990 production.

## Data provenance and references
- Methods build on prior LCM iterations (LCM2007, LCM2015) and align with UK CEH mapping standards.
- Acknowledges NERC funding (NE/R016429/1) and related Rowland et al. publications on land cover change and data products.
- Key references include Jackson (2000), Morton et al. (2011), Rowland et al. (2020a, 2020b).