# Dataset documentation

## Overview
- LCM2015 is a parcel-based UK land cover map produced from satellite imagery (Landsat-8 30 m, supplemented with AWIFS 60 m) to classify into 21 Broad Habitat–based classes.
- Update and expansion from LCM2007, with a per-polygon, real-world boundary framework and rich metadata for governance, discovery, and reuse.
- Data are available in multiple formats (vector, 25 m raster, 1 km percentage/dominant products) and come with DOIs for citation.

## Data products and formats
- Vector data: polygons with 9 attached attributes (e.g., dominant class, pixel counts per class, uncertainty, gid).
- 25 m raster: two-band product; band 1 = dominant class, band 2 = mean per-polygon RF probability.
- 1 km products: dominant class (1 km), dominant aggregate class (1 km), 21-band percentage cover (1 km), 10-band aggregate percentage cover (1 km).
- Great Britain and Northern Ireland provided separately with appropriate projections.
- Minimum mappable unit: parcels > 0.5 ha; linear features < 20 m dissolved.

## Classification and methodology
- Classifier: Random Forest ( replaces previous Maximum Likelihood).
- Training data: initial stable areas (from 2000 and 2007) plus coastal additions and poorly mapped classes; no need for spectral sub-classes.
- Ancillary data: integrated as input data (not post-classification rules), enabling objective knowledge-based enhancements.
- Spatial framework: no segmentation in LCM2015; per-pixel classification improves change-mapping suitability.
- Handling of mixed woodland updated: training uses pure stands with per-pixel classification and polygon-level modal label.
- Outputs reflect land cover (not always equal to land use); per-pixel probabilities are provided for uncertainty.

## Data governance, metadata, and uncertainty
- Rich metadata: detailed polygon attributes, pixel counts per class, mean probability, and gid for unambiguous communication.
- Uncertainty: per-polygon mean probability from Random Forest; provided for vector and 25 m rasters.
- DOIs: each product has a DOI for citation; GB and NI datasets have separate DOIs (vector, 25 m raster, 1 km percentage/dominant and aggregate classes).

## Data access and licensing
- 1 km raster data accessible via CEH Environmental Information Platform (eip.ceh.ac.uk).
- Full vector and 25 m raster products: available on request under license; fees may apply.
- Contacts: spatialdata@ceh.ac.uk and CEH licensing information pages.
- Data citation: DOIs should be cited in publications to ensure reproducibility.

## Spatial coverage, projection, and data structure
- Projections: GB vector/raster in British National Grid; NI vector/raster in Irish National Grid.
- Vector dataset: approximately 6.7 million polygons (GB) and 0.9 million (NI).
- Core products: vector from which 25 m raster and 1 km products are derived; DOI-based data provenance and versioning (Version 1.2 as of May 2017).

## Class definitions and documentation
- 21 LCM2015 target classes based on UK Broad Habitats (JNCC definitions); several classes are subdivided (e.g., Built-up Areas and Gardens into Urban/Suburban).
- Appendix materials provide detailed class definitions, colour mappings, and mapping recipes for standardization.

## Data quality notes and caveats
- Differences from LCM2007 include removal of Montane and Rough Grassland classes, changes to 25 m raster structure, and simplified probability reporting; users should review changes when migrating scripts.
- Complexities in change mapping arise from real change versus classification error; the document cautions against using LCM2015 for current-state change mapping without considering these differences.
- Some rounding effects exist in 1 km percentage products; coastal areas may show underestimation in certain classes.

## Usage and references
- LCM2015 is a stable, archived dataset with DOIs aimed at repeatable use in research and policy.
- Publication and data citation recommendations are provided, including example DOI citations and guidance for including author/date in-text citations.

## Contact and further information
- Primary contact: spatialdata@ceh.ac.uk
- Additional information: CEH LCM2015 project pages and EIDP platforms; data papers in preparation.