# Dataset documentation

## Introduction
- LCM2015 (Land Cover Map 2015) is a UK parcel-based land cover map produced by classifying satellite data into 21 Broad Habitat-based classes.
- Uses two-date composite imagery, primarily Landsat-8 (30 m) with supplementary AWIFS (60 m) as needed.
- Aims to support diverse monitoring needs; notes that LCM2015 is intended for land cover mapping (not directly land use) and is prone to real-change plus classification error, especially for change mapping.

## Background
- LCM2015 updates the 2007 Land Cover Map, updating the spatial framework and aligning with UK Broad Habitat definitions.
- The product is built from polygons reflecting real-world boundaries to improve interpretability and compatibility with other geospatial data.
- The spatial framework is derived from generalised digital cartography (OSMM for GB; LPS Large-scale Vector for NI) and refined with rural boundary data.
- Differences from previous LCMs reflect evolving user needs, data availability, computational power, and a move toward faster, more repeatable production.

## Differences from LCM2007
- Output data differences:
  - Montane class removed; now mapped as Inland Rock or upland habitats based on spectral data.
  - Rough grassland class removed; grassland types now align with JNCC Broad Habitats without a separate rough category.
  - 25 m raster becomes a two-band image (classification band + mean per-polygon probability in band 2).
  - Probability data: top-5 spectral subclasses replaced by mean per-polygon probability; not provided for 1 km products.
  - No spectral sub-classes due to shift to Random Forest classifier.
  - Spatial framework: segmentation-based polygons removed; no per-image segmentation for the spatial framework.
  - Mixed woodland training changed: training uses pure stands; pixels are summarized to polygon-level labels.
- Methodology differences:
  - New Random Forest classifier (handles multi-model training data; avoids spectral-subclass grouping).
  - Stable training areas approach: initial stable areas defined from 2000 and 2007, extended for coastal and hard-to-map classes.
  - Ancillary data (e.g., altitude, soil) are part of input data rather than post-classification rules, making enhancements objective and integral.
- Map scope and labeling:
  - LCM2015 maps land cover (not land use) and provides extended metadata, uncertainty measures, and a stable archival product with DOIs.

## Data products and structure
- 21 target classes based on UK Broad Habitats (with some finer subdivisions in specific groups like Built-up Areas, Dwarf Shrub Heath, and Littoral categories).
- Core data products:
  - Vector data set (core product)
  - 25 m raster
  - 1 km percentage cover products (for both 21 target classes and 10 aggregate classes)
  - Dominant cover products at 1 km
- Spatial coverage:
  - Great Britain and Northern Ireland provided separately with appropriate coordinate systems (GB: British National Grid; NI: TM75 Irish Grid).
- Vector data set:
  - About 6.7 million polygons in GB and 0.9 million in NI.
  - Attributes include dominant class, source image, per-polygon uncertainty, pixel counts per class, and modal class (dominant).
- 25 m raster:
  - Two-band raster: band 1 = dominant LCM2015 class; band 2 = mean per-polygon probability.
- 1 km raster (aggregate products):
  - Dominant class at 1 km (21 classes and 10-aggregate classes)
  - Percentage cover at 1 km for each class and aggregate class (values are integers; sums may slightly differ from 100 due to rounding)
- Metadata and uncertainty:
  - Rich metadata for each polygon; polygon-level breakdown of pixel counts across all classes; mean probability per polygon.
  - Uncertainty is derived from the Random Forest classifier and is available in vector (unc) and raster band 2.
  - Minimum mappable area: >0.5 ha; polygons smaller than 0.5 ha or linear features <20 m dissolved into surrounding landscape.
- Unique labeling:
  - Each parcel has a gid (geometry id) for unambiguous communication and traceability.

## Metadata, uncertainty, and data governance
- LCM2015 provides per-polygon uncertainty values and a breakdown of class composition within each polygon (pix_dist).
- Metadata-rich vector products facilitate audit and reproducibility, with clear provenance of sources and composite imagery.
- Data are archived with DOIs to enable citation and traceability in publications.

## Data access and licensing
- 1 km raster products are publicly accessible via the CEH Environmental Information Platform (eip.ceh.ac.uk).
- Full vector and 25 m raster products are available under licence on request from CEH; licensing fees may apply.
- Data citation is encouraged via DOIs; each product has its own DOI.
- Examples of DOIs and citation guidance are provided for Great Britain and Northern Ireland products.

## Projections and data presentation
- GB data: British National Grid; NI data: TM75 Irish Grid.
- Data are presented in multiple formats to suit applications (vector with rich attributes, 25 m raster with probability information, and 1 km aggregated products).

## Citing LCM2015 (DOIs)
- Each product (vector GB, 25 m raster GB, 1 km percentage and dominant target classes GB, 1 km aggregate classes GB, and corresponding NI products) has a DOI for proper citation.
- Citations should include authors and date in-text and full DOI in the references.

## Practical considerations and cautions
- LCM2015 is a stable, archived product intended for long-term use; caveat: not ideal for change mapping in its current state due to differences in methods and outputs across versions.
- Users should review methodological changes and ensure scripts or workflows from LCM2007 are adapted for LCM2015 outputs.
- The product suite provides both high-detail (vector, 25 m) and broad-scale (1 km) data to support different monitoring needs and integration with other data sources.

## Additional information and contact
- Data access and further information are available via CEH portals and the LCM2015 project pages.
- Queries can be directed to the spatialdata@ceh.ac.uk.