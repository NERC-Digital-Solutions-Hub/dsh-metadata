# The UKCEH Land Cover Map for 2022

## Purpose and Intended Use
- User guide for the UKCEH Land Cover Map 2022 (LCM2022), a multi-dataset product supporting informed decision-making.
- Product comprises seven geospatial datasets (GB and Northern Ireland): 
  - a 10 m classified pixels dataset
  - a land parcels dataset
  - a 25 m pixel (rasterised land parcels) dataset
  - plus a 1 km summary raster product covering GB and NI
- Describes data production, validation, and data accuracy to aid appropriate use and interpretation.

## Product Structure and Datasets
- Datasets (GB and NI):
  - 10 m Classified Pixel datasets
  - 25 m Rasterised Land Parcel datasets
  - Land Parcel (vector) datasets
  - 1 km summary raster products
- Dataset specifics:
  - Coordinate systems: Great Britain in British National Grid (EPSG 27700); Northern Ireland in Irish Grid TM75 (EPSG 29903)
  - Pixel resolutions: 10 m (pixels) and 25 m (rasters)
  - Land parcels: ~6.74 million in GB and ~0.90 million in NI (parcels), with minimum mapped unit ~0.5 ha
  - Lands are classified into 21 UKCEH Land Cover Classes derived from Biodiversity Action Plan (BAP) Broad Habitats
- Dataset contents:
  - 10 m Classified Pixels: two bands (class identifier and associated membership probability)
  - 25 m Rasterised Land Parcels: three bands providing dominant class, confidence, and purity per parcel
  - Land Parcel Product: vector attributes for parcel-level analysis
  - 1 km rasters: dominant class and percentage cover, with area-based rounding nuances near coastlines
- Seasonal and contextual data:
  - Seasonal Composite Images (Sentinel-2, 4 seasons) used for classification
  - Context Rasters (GB and NI) to reduce spectral confusion (e.g., height, slope, distance to roads/buildings, coastal features)

## Data Production and Methodology
- Classification approach:
  - Bootstrap Training: automatic generation of training data from historical LCM maps (LCM2019–LCM2021) to train a Random Forest classifier, minimizing new field data needs
  - Training data filtered to high-confidence pixels (>80% probability) and consistent across years
  - For some classes (e.g., arable, improved grassland) training data sourced from alternative datasets due to rapid change in recent years
- Feature set:
  - Classification Scenes combine four-season Sentinel-2 data with multiple Context Rasters to reduce spectral confusion
  - 40-band setup for GB/49-band setup for NI Classification Scene
- Validation and reproducibility:
  - Validation using 33,107 reference points across 21 classes
  - Overall accuracy reported at 86.1% for LCM2022
  - Validation focused on 25 m Rasterised Land Parcel dataset; 10 m Classified Pixels retain additional detail (not used in formal validation)
- Data processing and software:
  - Bespoke UKCEH software integrating Weka (RF), PostGIS, and GDAL (open source)
  - Processing tiles for GB (~32 Classification Scenes; NI uses a single Scene)
- Land Parcel Spatial Framework:
  - Framework originally from LCM2007, with minor updates for storage and indexing
  - Changes mean LCM2022 parcel identifiers (gid) do not match LCM2015 identifiers for direct cross-version comparison

## Validation, Quality and Known Issues
- Validation outcomes:
  - Overall accuracy: 86.1% (producer’s and user’s accuracies vary by class; detailed Appendix 4 provides confusion matrices)
- Known issues:
  - A small number of polygons missing from vector land parcel products; corresponding nodata areas in 25 m rasterised parcels
  - Impact on 1 km summary rasters is negligible; 10 m classified pixels datasets are unaffected
- Documentation and citation:
  - Each LCM2022 dataset has a DOI; citations listed (Marston et al. 2024, with specific papers for GB, NI, land parcels, 1 km rasters, etc.)
  - Users should cite the relevant dataset DOIs and may consult Marston et al. (2023/2024) for production methods

## Usage, Access and Metadata
- Dataset access and citation:
  - DOIs provided for 10 m classified pixels (GB and NI), 25 m rasterised land parcels (GB and NI), land parcel vectors, and 1 km summary rasters
  - Data products are intended for long-term use with attention to annual methodological updates
- Documentation depth:
  - Appendices provide comprehensive guidance on UKCEH Land Cover Classes, BAP Broad Habitats, and class relationships
  - Appendices 5 and 6 include color prescriptions for mapping UKCEH Classes (including color-blind friendly options)
- Known notes on temporal use:
  - The product is updated annually; method changes may yield real changes as well as methodology-driven differences
  - For cross-year change detection, awareness of methodological evolution is essential

## Appendices and Supporting Documentation
- Appendix 1: Notes on UKCEH Land Cover Classes (class-level definitions and caveats)
- Appendix 2: Biodiversity Action Plan (BAP) Broad Habitats descriptions
- Appendix 3: Full list of UKCEH LCM2022 datasets with DOIs
- Appendix 4: Correspondence matrices (confusion matrices) for validation
- Appendix 5: Recommended color recipe for displaying UKCEH Land Cover Classes
- Appendix 6: Color-blind friendly color recipe
- Additional materials:
  - QGIS symbology files accompanying the data products
  - References to foundational methodological documents (LCM2007/LCM2015/LCM2021, RF literature, and data sources)

## Governance and Data Stewardship Considerations
- Data provenance and versioning:
  - LCM2022 uses Bootstrap Training data from prior LCMs; maintain provenance records for training data and classification runs
  - Be aware of gid changes in the UK Land Parcel Spatial Framework; document version-specific parcel identifiers and relationships
- Metadata and discoverability:
  - Leverage DOIs and published citations to ensure dataset traceability
  - Maintain documentation on dataset structure (10 m pixels, 25 m parcels, vector parcels, 1 km rasters) and their inter-relationships
- Temporal comparability and change detection:
  - Annual updates enable change detection but require careful interpretation due to methodological evolution
  - When comparing with LCM2015 or earlier, note differences in spatial framework and identifiers
- Quality assurance:
  - Reference validation metrics (overall accuracy, class-level accuracies) andAppendix 4 confusion matrices to assess reliability per class
  - Document known issues and their potential impact on analyses
- Licensing, citations and reuse:
  - Use the dataset DOIs and cited literature when distributing analyses or derivative products
  - Consider including the recommended color recipes and mapping guidance to support consistent visualization